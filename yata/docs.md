# deepchar

[github.com/deepchar](https://github.com/deepchar) *Transliteration with sequence-to-sequence models and transfer learning*

<img src="/favicon.ico" align="left"/>

<details><summary><strong>About transliteration</strong></summary>

About half of the billions of internet users speak languages written in non-Latin alphabets, like Russian, Arabic, Persian, Hebrew, Chinese, Korean, Japanese, Greek, Armenian, Georgian, Mongolian, Hindi and Tamil.  Very often, they haphazardly use the Latin alphabet to write those languages.

`Привет` => `Privet` , `Privyet`, `Priwjet`, ...  
`كيف حالك` => `kayf halk`, `keyf 7alek`, ...  
`Բարև Ձեզ` => `Barev Dzez`, `Barew Dzez`, ...  
`ხაჭაპური` => `xachapuri`, ...

So a growing share of user-generated text content is in these "Latinized" or "romanized" formats known as *translit*, *arabizi*, *Greeklish* and so on that are difficult to parse, search or even identify.

Transliteration is the task of automatically converting this content back into the native canonical format.

`Privet` => `Привет`    
`Privyet` => `Привет`    
`Priwjet` => `Привет`  
...
`Aydpes aveli sirun e.` => `Այդպես ավելի սիրուն է:`

You can read more about what makes this problem non-trivial at [*Automatic transliteration with LSTM*](http://yerevann.github.io/2016/09/09/automatic-transliteration-with-lstm/) and [*Interpreting neurons in an LSTM network*](https://yerevann.github.io/2017/06/27/interpreting-neurons-in-an-LSTM-network/).

Transliteration can be seen as a special case of *translation*, *style transfer* or *spelling correction*.

Therefore deepchar can be used for tasks like translation between Serbian and Croatian or Hindi and Urdu, applying British style to American English.

It can also be used for case correction, punctuation correction and inserting the non-ASCII characters or accent marks for all the languages written in the Latin alphabet - Spanish, French, Italian, German, Turkish and most others - that have non-ASCII characters.  (This task may be called *diacritic restoration*, but *ə*, *œ*, *ß* and *ı* are not diacritics.)

Another flavour of this task is transliteration of named entities.  Instead of mapping many inputs to one output (n:1), it maps one input to many outputs (1:n).  You can read more about that in [deepchar/entities](/entities).

</details>

### Our approach

Our baseline approach is to train **character-level sequence-to-sequence** models on generated data.

Besides our modification to character-level, [Sockeye](https://github.com/awslabs/sockeye) and [Fairseq](https://github.com/pytorch/fairseq) are standard modern implementations of sequence-to-sequence, developed primarily for machine *translation* but in principle applicable to a wide range of tasks with sequence input and sequence output

Sockeye was developed by AWS Labs on Apache MXNet, and Fairseq was developed by Facebook AI Research on PyTorch.  Fairseq models can be launched and scaled in production with [pytorch/translate](https://github.com/pytorch/translate).

#### Transfer learning

Universal or languageless models can solve numerous problems when scaling to hundreds of languages.

From a research perspective, many difficult aspects of the transliteration task - ambiguity, named entities, long-distance dependencies, out-of-distribution data - are similar between two or more languages, so accuracy can be improved for many languages, especially smaller languages.

From an engineering perspective, accuracy held equal, it is more practical to launch one model per target language or even one model for all languages, 

From a product perspective, it is also ideal, because in the real world the data even from the same user contains multiple languagese, 

Training universal or languageless models requires only a change in datasets or data generation, and more computing power to train each model, but no fundamental change in the neural network architecture.  It can be as simple as adding examples of English sentences.

Read more about the results of transfer learning in **Benchmarks**.

#### Semi-supervised learning

The transliteration problem is characterised by near total lack of parallel data from the real world.  Data generation techniques give us great baseline results, but are skewed from real-world data in obvious and subtle ways.

Can we use *unlabelled* real-world source-side data to generate more realistic parallel data?  Can we use *unlabelled* target-side data to train better models?

#### Adversarial learning

In adversarial learning, the training essentially asks to see the output for specific inputs.  Intuition tells us that learning a good transliteration model should actually require very few examples *if they are the right examples*, especially if we have unlabelled data.

Can we train good models on a greatly reduced dataset?  Can we reduce the dataset more optimally?  Can we reduce the dataset even more if we let the model choose to see examples dynamically during training?

### Datasets

Constrained by lack of parallel corpora, and inspired by similar approaches to transliteration and other sequence-to-sequence tasks like grammar correction, we rely primarily on **data generation**.

See the [deepchar/data](https://github.com/deepchar/data) repo

### Benchmarks

See the [deepchar/benchmarks](https://github.com/deepchar/benchmarks) repo

### Results

TODO

### References

Sockeye

> *Sockeye: A Toolkit for Neural Machine Translation* 2017/2018 [arXiv](https://arxiv.org/abs/1712.05690)  
> Felix Hieber, Tobias Domhan, Michael Denkowski, David Vilar, Artem Sokolov, Ann Clifton and Matt Post  
> Amazon Web Services Labs

Fairseq

> *Convolutional Sequence to Sequence Learning* [arXiv](https://arxiv.org/abs/1705.03122)  
> Jonas Gehring, Michael Auli, David Grangier, Denis Yarats, Yann N. Dauphin  
> Facebook AI Research

See repos like [deepchar/entities](https://github.com/deepchar/entities) for more specific references