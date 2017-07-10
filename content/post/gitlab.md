---
title: "GitLab pipelines"
date: 2017-07-10T14:00:05+03:00
tags: [ "dev" ]
---

CI от GitLab - это нечто волшебное!

Крайне простой синтаксис конфига и сборка на основе Docker образа похитили моё сердце.
Прошло смутное время этих ваших дженкинсов, которые пока настроишь - веру в жизнь потеряешь!

Сейчас вся моя сборка этого блога делается с помощью этого простейшего конфига:

```
image: felicianotech/docker-hugo:0.22.1

before_script:
  - 'which ssh-agent || ( apt-get update -y && apt-get install openssh-client -y )'
  - mkdir -p ~/.ssh
  - eval $(ssh-agent -s)
  - '[[ -f /.dockerenv ]] && echo -e "Host *\n\tStrictHostKeyChecking no\n\n" > ~/.ssh/config'

stages:
  - build
  - deploy

build:
  stage: build
  script:
    - HUGO_ENV=production hugo

deploy:
  stage: deploy
  script:
    - ssh-add <(echo "$STAGING_PRIVATE_KEY")
    - scp -P22 -r public/* root@neonxp.net:/var/www/neonxp.net
```

Надо будет и рабочие проекты перевести на эти рельсы.

P.S. И самое главное, всё это счастье - беплятно, то есть, даром!
