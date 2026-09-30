# Flower Shop

Интернет-магазин цветов и букетов: каталог с категориями, слайдеры, фильтры по цене и типу цветов, поиск и избранное.

![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![React Router](https://img.shields.io/badge/React_Router-CA4245?logo=reactrouter&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![Swiper](https://img.shields.io/badge/Swiper-6332F6?logo=swiper&logoColor=white)

## Страницы

| Путь | Что там |
|---|---|
| `/` | Главная: баннер, категории, популярные букеты |
| `/filter` | Каталог с фильтрами по цене и цветам, поиск |
| `/favorites` | Избранные товары |

## Архитектура

```mermaid
flowchart LR
    App[App.jsx + Router] --> Header
    App --> Home[Home]
    App --> Filter[Filter]
    App --> Fav[Favorites]
    Home --> Categories & Products & CardBouquet
    Filter --> BlockFilter & SearchInput & Popups[FilterPrice / FlowerFilter]
    Popups --> RangeInput
```

## Карта проекта

```
flower-shop/
└── src/
    ├── App.jsx                   # Роутинг
    ├── pages/
    │   ├── Home/                 # Главная
    │   ├── filter/               # Каталог с фильтрами
    │   └── favorites/            # Избранное
    ├── components/
    │   ├── Header/               # Шапка и навигация
    │   ├── Categories/           # Категории товаров
    │   ├── Products/             # Сетка товаров
    │   ├── CardProduct/, CardBouquet/   # Карточки
    │   ├── ButtonSlider/, ButtonShow/   # Кнопки слайдера и «показать ещё»
    │   ├── SearchInput/, InputFilter/, BlockFilter/
    │   ├── RangeInput/           # Двойной ползунок цены
    │   └── popups/               # Попапы фильтров: цена, цветы, категории
    ├── utils/                    # Общие функции
    └── assets/                   # Изображения
```

## Запуск

```bash
npm install
npm run dev
```
