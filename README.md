# Docker, Ruby on Rails, PostgreSQL sample

## do

```sh
docker-compose build
docker-compose run web bin/rake db:create db:migrate db:seed
docker-compose up
```

dinghy はプライベート DNS サーバを立てて下さるので、`docker-compose.yml` で
```yaml
web:
  build: .
  ...
  environment:
    VIRTUAL_HOST: railssample.docker
```
などと指定して、
http://railssample.docker などとアクセスする。

## References

- docker-compose で Rails の開発環境を作る - Qiita - http://qiita.com/skyriser/items/2cf98b747ed6577cc5ee

## appendix
- OSXでDockerを超高速化するdinghy - Qiita - http://qiita.com/masuidrive/items/d71ee1881fffb6ad098f
