# Qianyi Shen's Personal Website

This repository contains the source code for my personal website, which is built using the [Academic Pages](https://academicpages.github.io/) template. The website is hosted on GitHub Pages and can be accessed at [https://ethanqy.github.io/](https://ethanqy.github.io/).

## Deployment

This website can be automatically deployed using GitHub Actions. Whenever changes are pushed to the `main` branch, the website will be automatically built and deployed to GitHub Pages.

Sometimes, it is necessary to pre-build the website locally before pushing changes to GitHub. This can be achieved by a local Ruby environment with the necessary dependencies installed.

### macOS

<!-- change the README into English -->
1. Install Ruby 3.2 (Recommended: 3.2.x)
   ```bash
   brew install ruby@3.2
   ```

2. Add Homebrew's Ruby to PATH (otherwise the terminal will use the system's Ruby 2.6, causing `bundle` to error). Add a line to `~/.zshrc` at the end (use the first line for Apple Silicon, the second line for Intel Mac):
   ```bash
   export PATH="/opt/homebrew/opt/ruby@3.2/bin:$PATH"
   # export PATH="/usr/local/opt/ruby@3.2/bin:$PATH"
   ```
   Save and execute `source ~/.zshrc` or open a new terminal. Use `ruby -v` to confirm that 3.2.x is displayed.

3. Install Bundler:
   ```bash
   gem install bundler
   ```

4. Enter the repository root directory and install dependencies:
   ```bash
   cd /path/to/EthanQY.github.io   # change to your repository path
   bundle config set path vendor/bundle
   bundle install
   ```

5. Start local preview:
   ```bash
   bundle exec jekyll serve
   ```
   Open `http://localhost:4000/` in the browser to view the site.

> The Gemfile in this repository contains `liquid >= 4.0.4` to be compatible with Ruby 3.2 (to avoid the `undefined method 'tainted?'` error). If port 4000 is occupied, you can use `bundle exec jekyll serve --port 4001` to specify another port.

### Windows



1. Install Ruby, recommended version `3.2.10`; select "MSYS2 and MINGW development toolchain" during installation.
2. Execute `gem install bundler jekyll` in the terminal.
3. Execute `bundle config set path vendor/bundle` in the repository root directory, then execute `bundle install`.
4. Execute `bundle exec jekyll serve`, open http://localhost:4000/ in the browser.
