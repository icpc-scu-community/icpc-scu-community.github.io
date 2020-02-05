# SCU ICPC Community

## Development and local testing

### Option 1 (Ruby Installed) :gem:

Inside the repo directory, execute the following:

```bash
gem install bundler
bundle install
bundle exec jekyll serve --watch
```

### Option 2 (Docker Installed) :heart: :whale:

**Remove** _`Gemfile.lock`_ first, if exists.

```bash
docker run -it --rm -v "$PWD":/usr/src/app -p "4000:4000" starefossen/github-pages
```
