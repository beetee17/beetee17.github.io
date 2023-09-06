# Testing the site locally with Jekyll

The following content is taken from the [github docs](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).

## Prerequisites

Before you can use Jekyll to test a site, you must:

- Install Jekyll.
- Create a Jekyll site. For more information, see "Creating a GitHub Pages site with Jekyll."

We recommend using Bundler to install and run Jekyll. Bundler manages Ruby gem dependencies, reduces Jekyll build errors, and prevents environment-related bugs. To install Bundler:

1. Install Ruby. For more information, see "Installing Ruby" in the Ruby documentation.
2. Install Bundler. For more information, see "Bundler."

**Tip:** If you see a Ruby error when you try to install Jekyll using Bundler, you may need to use a package manager, such as RVM or Homebrew, to manage your Ruby installation. For more information, see "Troubleshooting" in the Jekyll documentation.

## Building your site locally

1. Open Terminal.
2. Navigate to the publishing source for your site. For more information, see "Configuring a publishing source for your GitHub Pages site."
3. Run `bundle install`.
4. Run your Jekyll site locally.

```
$ bundle exec jekyll serve

> Configuration file: /Users/octocat/my-site/\_config.yml
> Source: /Users/octocat/my-site
> Destination: /Users/octocat/my-site/\_site
> Incremental build: disabled. Enable with --incremental
> Generating...
> done in 0.309 seconds.
> Auto-regeneration: enabled for '/Users/octocat/my-site'
> Configuration file: /Users/octocat/my-site/\_config.yml
> Server address: http://127.0.0.1:4000/
> Server running... press ctrl-c to stop.
```

> Note: If you've installed Ruby 3.0 or later (which you may have if you installed the default version via Homebrew), you might get an error at this step. That's because these versions of Ruby no longer come with webrick installed. To fix the error, try running bundle add webrick, then re-running bundle exec jekyll serve.

To preview your site, in your web browser, navigate to http://localhost:4000.
