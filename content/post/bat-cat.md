---
title: "🦇 Bat - как Cat только лучше"
date: 2018-11-16T14:00:17+03:00
subtitle: ""
tags: ["разное", "микрозаметка"]
---

## Очередная микрозаметка.

Существует очень приятная замена класичекой утилите `cat` - `bat`. [https://github.com/sharkdp/bat](https://github.com/sharkdp/bat)

Написано на расте, но это не главное. Главное - оно дает удобный просмотр (как в `less`), нумерацию строк (!!!), и подсветку синтаксиса.

![bat](https://camo.githubusercontent.com/9d3d89364f2cc83ace8f29646a6236bc15ea1da0/68747470733a2f2f696d6775722e636f6d2f724773646e44652e706e67)

Для себя я накидал пару сниппетов, которые помогают мне в работе:

## Просмотр неформатированного json

```
bat ФАЙЛ.json | json_pp | bat -l json
```

## Для xml

```
xmllint --pretty 3 --format ФАЙЛ.xml | bat
```

Обе команды используют встроенные в macOS инструменты. Не знаю, заработает ли в этих ваших линуксах.

P.S. это первый пост для блога, который я набираю в прекрасном редакторе `micro`([https://github.com/zyedidia/micro](https://github.com/zyedidia/micro)). Очень рекомендую.