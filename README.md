## Задание
Исследовать сайт https://lifehacker.ru/ и предложить способы оптимизации его загрузки.

### Какие использованны инструменты?

- [gtmetrix](https://gtmetrix.com)

- [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)

- Chrome DevTools

Контент отображатеся достаточно медленно:
- Шапка появляется через секунду
- Первый текст появляется через 2 секунды
- загрузка DOM 3.5 сек
- полная загрузка 11-14 сек

### Как улулчшить?

**JS**
- использовать атрибуты ```async/defer```
- использовать ```<link rel="preload" ... as="script">```
- перенести скрипты вниз документа перед ```</body>```
- минифициоровать те скрипты, которые не минифицированны

**CSS**
- инлайново подключить стили необходимые для начальной отрисовки основного контента
- минифицировать css
- использовать ```<link rel="preload" ... as="style">```

**Fonts**
- использовать ```<link rel="preload" ... as="font">```
- в стилях использовать свойство ```font-display: ...;```

**Multimedia**
- использовать формат WebP
- сжать изображения

