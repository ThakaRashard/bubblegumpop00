<img  alt="image" src="https://github.com/user-attachments/assets/d2597459-0312-482e-becd-6c5109840ae4" />

[link](https://bitbucket.org/rashard-podaac/bubblegumpop/src/master/)
[![.github/workflows/ci.yaml](https://github.com/pages-themes/hacker/actions/workflows/ci.yaml/badge.svg)](https://github.com/pages-themes/hacker/actions/workflows/ci.yaml) [![Gem Version](https://badge.fury.io/rb/jekyll-theme-hacker.svg)](https://badge.fury.io/rb/jekyll-theme-hacker)
![Screenshot 2025-06-13 12 28 54 PM](https://github.com/user-attachments/assets/b9c1e36c-221c-43f9-b7e7-44c1d5bde37e)
![Screenshot 2025-06-13 12 28 46 PM](https://github.com/user-attachments/assets/f7848e80-a074-4ba8-b188-450b5607ebf2)

![Screenshot 2025-06-13 12 28 54 PM](https://github.com/user-attachments/assets/4b54e950-fd01-48e8-ac75-573c65b5c71d)
![Screenshot 2025-06-13 10 22 23 AM](https://github.com/user-attachments/assets/d84353c8-e7d2-4991-bde2-42481abb5ca8)
![Screenshot 2025-06-13 10 33 22 AM](https://github.com/user-attachments/assets/1b0d0839-e658-4734-9cc9-879403fc7a59)

To use the Hacker theme:

1. Add the following to your site's `_config.yml`:

    ```yml
    remote_theme: pages-themes/hacker@v0.2.0
    plugins:
    - jekyll-remote-theme # add this line to the plugins list if you already have one
    ```

2. Optionally, if you'd like to preview your site on your computer, add the following to your site's `Gemfile`:

    ```ruby
    gem "github-pages", group: :jekyll_plugins
    ```

## Customizing

### Configuration variables

Hacker will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" (unquoted) to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

### Layouts

If you'd like to change the theme's HTML layout:

1. For some changes such as a custom `favicon`, you can add custom files in your local `_includes` folder. The files [provided with the theme](https://github.com/pages-themes/hacker/tree/master/_includes) provide a starting point and are included by the [original layout template](https://github.com/pages-themes/hacker/blob/master/_layouts/default.html).
2. For more extensive changes, [copy the original template](https://github.com/pages-themes/hacker/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
3. Create a file called `/_layouts/default.html` in your site
4. Paste the default layout content copied in the first step
5. Customize the layout as you'd like

### Customizing Google Analytics code

Google has released several iterations to their Google Analytics code over the years since this theme was first created. If you would like to take advantage of the latest code, paste it into `_includes/head-custom-google-analytics.html` in your Jekyll site.

### Overriding GitHub-generated URLs

Templates often rely on URLs supplied by GitHub such as links to your repository or links to download your project. If you'd like to override one or more default URLs:

1. Look at [the template source](https://github.com/pages-themes/hacker/blob/master/_layouts/default.html) to determine the name of the variable. It will be in the form of `{{ site.github.zip_url }}`.
2. Specify the URL that you'd like the template to use in your site's `_config.yml`. For example, if the variable was `site.github.url`, you'd add the following:
    ```yml
    github:
      zip_url: http://example.com/download.zip
      another_url: another value
    ```
3. When your site is built, Jekyll will use the URL you specified, rather than the default one provided by GitHub.

*Note: You must remove the `site.` prefix, and each variable name (after the `github.`) should be indent with two space below `github:`.*

For more information, see [the Jekyll variables documentation](https://jekyllrb.com/docs/variables/).

## Roadmap

See the [open issues](https://github.com/pages-themes/hacker/issues) for a list of proposed features (and known issues).

## Project philosophy

The Hacker theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.

## Contributing

Interested in contributing to Hacker? We'd love your help. Hacker is an open source project, built one contribution at a time by users like you. See [the CONTRIBUTING file](docs/CONTRIBUTING.md) for instructions on how to contribute.

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/pages-themes/hacker`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` once before the test script will work.
