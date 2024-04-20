

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
docker-compose run --rm frontend sh -c 'npx create-react-app プロジェクト名 --template typescript'

docker compose run backend rails new . --force
