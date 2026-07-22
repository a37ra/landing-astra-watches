# Astra — Luxury Watches Landing Page

Одностраничный лендинг для вымышленного бренда премиальных часов **Astra**. Сделан на чистых HTML/CSS/JS без сборщиков и фреймворков.

🔗 **Демо:** https://a37ra.github.io/landing-astra-watches/

## О проекте

Лендинг рассказывает историю бренда через несколько тематических секций:

- **Hero** - заглавный экран с крупным изображением часов
- **Logo Cloud** - блок "As Featured In" с бегущей лентой логотипов
- **Philosophy** - философия бренда (4 карточки с иконками)
- **Vision** - имиджевый блок "See the Big Picture"
- **Why Astra** - сравнительная таблица: Astra vs Classic Luxury vs Smartwatches
- **Quote** - цитата клиента с фото
- **Precision** - детальный разбор конструкции часов (3 пункта + фото)
- **Inquire CTA** - призыв к действию для связи
- **Footer** - навигация и контакты

## Стек

- **HTML5** - семантическая разметка
- **CSS3** - адаптивная верстка, кастомные шрифты (Crimson Text, DM Sans, Roboto Mono через Google Fonts)
- **Vanilla JS** - без зависимостей:
  - плавное появление блоков при скролле через `IntersectionObserver`
  - поддержка `prefers-reduced-motion` (анимации отключаются для пользователей с соответствующей настройкой ОС)
  - фолбэк для браузеров без поддержки `IntersectionObserver`

## Структура проекта

```
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
└── assets/
    ├── logo.png / logo.webp
    ├── hero-watch.png / .webp
    ├── watchdetail.png / .webp
    ├── watchredonsilk.png / .webp
    ├── watchblackmramorhorizon.png / .webp
    ├── ronaldowthwatchvision.png / .webp
    └── logoipsum/
```

## Особенности реализации

- **Оптимизация изображений** - везде используется `<picture>` с WebP-версией и PNG-фолбэком, атрибуты `width`/`height` заданы явно для предотвращения layout shift
- **Ленивая загрузка** - некритичные изображения помечены `loading="lazy"`, hero-изображение - `fetchpriority="high"`
- **Анимации появления (`reveal`)** - элементы с классом `.reveal` анимированно проявляются при попадании во вьюпорт; задержка анимации настраивается через `data-reveal-delay` (в миллисекундах), а элементы с `data-reveal-immediate` показываются сразу при загрузке страницы
- **Доступность** - учтены `prefers-reduced-motion`, `alt`-тексты, декоративные изображения скрыты через `aria-hidden`

## Запуск локально

Проект не требует сборки - достаточно открыть `index.html` в браузере, либо поднять любой локальный сервер, например:

```bash
npx serve .
```

или

```bash
python3 -m http.server
```

## Деплой

Сайт задеплоен через **GitHub Pages** из этого репозитория: https://a37ra.github.io/landing-astra-watches/

## Лицензия

Проект создан в учебных/демонстрационных целях, бренд Astra - вымышленный.
