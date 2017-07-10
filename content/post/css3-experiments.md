---
title: "Немного свежего CSS3"
date: 2017-07-10T01:29:15+03:00
tags: ["dev", "css"]
---

Выделил немного времени и посмотрел что может современный CSS:

<p data-height="500" data-theme-id="0" data-slug-hash="ZyqZog" data-default-tab="css,result" data-user="NeonXP" data-embed-version="2" data-pen-title="CSS3 Features Test" class="codepen">See the Pen <a href="https://codepen.io/NeonXP/pen/ZyqZog/">CSS3 Features Test</a> by Alexander NeonXP Kiryukhin (<a href="https://codepen.io/NeonXP">@NeonXP</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Думаю, на днях найду время и подробно распишу про css3 гриды, т.к. про них весьма мало информации. Главное не забыть.

А пока что я могу сказать? Ещё бы удобные вложения, типа

```
content {
  p {

  }
}
```

вместо

```
content {

}
content > p {

}
```

и можно будет выкинуть эти ваши LESS и SASS на свалку истории!

Ну а верстать гридами - это просто счастье. Это настолько просто и очевидно, что поражаюсь, почему это появяется только сейчас? Нахрена мы страдали этими чертовыми таблицами, а потом float:left, float:right, clear:both? Флоаты вообще для обтекания объектов (например, картинок) текстом, а не для позиционирования! Флексы были уже ближе к правде, но все равно ещё не до конца. А вот теперь, наконец-то, мы дома!

Жаль IE опять портит всю малину. По сути он только и не работает с ними (ну и стабильный сафари не совсем корректно работает, но ему жить осталось пара месяцев).
