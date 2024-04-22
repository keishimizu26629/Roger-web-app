

```Gemfile
source 'https://rubygems.org'
gem 'rails'
```
Gemfile.lock
```
cd frontend
yarn init
yarn add react react-dom
```
docker-compose run --rm front sh -c 'npx create-react-app . --template typescript'

docker compose run --rm api rails new . -f -B -d postgresql --api

docker compose run --rm api sh
docker compose run --rm front sh
docker compose run api bin/rails secret
docker compose run --rm front npx create-react-app . --template typescript
docker compose run --rm front npx create-next-app@latest temp-app --typescript



エラーメモ
・bundle lock --add-platform aarch64-linux
RUN bundle lock --add-platform aarch64-linux && \
    bundle install && \
    rm -rf ~/.bundle/ "/usr/local/bundle"/ruby/*/cache "/usr/local/bundle"/ruby/*/bundler/gems/*/.git && \
    bundle exec bootsnap precompile --gemfile
・docker compose run api bin/rails secret
・RAILS_ENV="production" \　の削除
my-web-app-api-1  | ArgumentError: Missing `secret_key_base` for 'production' environment, set this string with `bin/rails credentials:edit` (ArgumentError)
my-web-app-api-1  |
my-web-app-api-1  |         raise ArgumentError, "Missing `secret_key_base` for '#{Rails.env}' environment, set this string with `bin/rails credentials:edit`"
my-web-app-api-1  |               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
my-web-app-api-1  | /rails/config/environment.rb:5:in `<main>'
my-web-app-api-1  | Tasks: TOP => db:prepare => db:load_config => environment
my-web-app-api-1  | (See full trace by running task with --trace)
my-web-app-api-1 exited with code 1
