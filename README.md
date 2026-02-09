# Qianyi Shen's Personal Website

This repository contains the source code for my personal website, which is built using the [Academic Pages](https://academicpages.github.io/) template. The website is hosted on GitHub Pages and can be accessed at [https://ethanqy.github.io/](https://ethanqy.github.io/).

## Deployment

This website can be automatically deployed using GitHub Actions. Whenever changes are pushed to the `main` branch, the website will be automatically built and deployed to GitHub Pages.

Sometimes, it is necessary to pre-build the website locally before pushing changes to GitHub. This can be achieved by a local Ruby environment with the necessary dependencies installed. The following steps can be used to build the website locally:

1) Install Ruby, recommended version: `3.2.10`.
2) Choose 'MSYS2 and MINGW development toolchain' when installing Ruby.
3) Install the required gems by running the following command in the terminal:
   ```bash
   gem install bundler jekyll
   ```
4) Navigate to the root directory of the repository and run the following command to build the website:
   ```bash
   bundle config set path vendor/bundle
   bundle install
   ```
5) After the installation is complete, you can build the website by running:
   ```bash
    bundle exec jekyll serve
    ```
    Expect the website to be available at `http://localhost:4000/` after the build process is complete.
