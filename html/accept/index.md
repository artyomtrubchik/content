---
title: "Атрибут `accept`"
description: "При выборе прикрепляемого файла этот атрибут покажет только разрешённые типы"
authors:
  - tanugladkih
related:
  - html/input
  - html/form
  - html/label
tags:
  - doka
  - placeholder
---

## Кратко

Атрибут `accept` добавляется тегу [`<input>`](/html/input/). Он позволяет указать, файлы какого типа пользователю нужно прикрепить.

## Пример

```html
<form method="post">
  <label for="cat-picture">Прикрепите фото кота</label>
  <input
    type="file"
    id="cat-picture"
    name="cat-picture"
    accept=".jpg, .jpeg, .png"
  >

  <button>Прикрепить</button>
</form>
```

## Как пишется

Атрибут `accept` может принимать строку значений:

1. `'audio/*'` — принимает звуковые файлы любого формата.
1. `'video/*'` — принимает видео любого формата.
1. `'image/*'` — принимает изображения любого формата.
1. Строка типа MIME без расширений.
1. Расширения файла, перед которыми стоит точка. Например: `.jpg`, `.pdf`, `.docx` и так далее.

Можно указать несколько значений, а ещё их можно сочетать, например:

```html
<input type="file" name="cat-pic-video" accept="video/*, .jpg, .jpeg, .png">
```

## Как понять

Важно понимать, что атрибут `accept` лишь показывает пользователю в открывшемся диалоговом окне файлы типов, которые вы указываете в значении атрибута, но не фильтрует их. Проверка типов файлов должна происходить на стороне сервера. Без этого ничто не помешает пользователю прикрепить скучный текстовый документ, хотя вы ждали фото котика.

## Подсказки

💡 Что делать, если у пользователя несколько котов и он хочет показать вам всех? Поможет атрибут [`multiple`](/html/multiple/).