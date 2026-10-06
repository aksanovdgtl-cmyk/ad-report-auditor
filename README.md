# Аудитор рекламных отчетов / Ad Report Auditor

Проверка рекламного отчета из Google Ads, Meta Ads, Яндекс Директа или Telegram Ads. Показывает KPI, расходы без результата и сигналы ошибок аналитики. Принимает CSV и Excel, отдает аудит в CSV.

Автор: [Марат Аксанов](https://aksanov.digital/about), [Aksanov.Digital](https://aksanov.digital).

## Онлайн-версии

- [ad-report-auditor](https://aksanov.digital/tools/advertising/ad-report-auditor)

Весь каталог: [инструменты для маркетинга и бизнеса](https://aksanov.digital/tools).

## Запуск

Скачайте или клонируйте репозиторий. Откройте `index.html` в современном браузере. Сборка и регистрация не нужны. Для локального сервера:

```sh
python3 -m http.server 8080
```

Откройте `http://localhost:8080`. Страницы инструмента:

- `index.html`

## Данные и зависимости

Вводные и загруженные отчеты обрабатываются в браузере. Код инструмента не отправляет их на сервер и не подключается к рекламным аккаунтам. В этой версии нет счетчиков сайта и скриптов Tilda.

SheetJS CE 0.20.3, Apache-2.0. Библиотека загружается с официального CDN SheetJS для Excel. Ее код не включен в репозиторий; CSV обрабатывается собственным кодом. В автономной версии зависимость обновлена с 0.18.5, расчетные правила сохранены.

Для загрузки внешней библиотеки нужен интернет. В запросах к CDN передаются обычные сетевые данные, включая IP; содержимое загруженного отчета туда не отправляется. Внешние изображения из исходной страницы также могут загружаться с CDN. Пользовательские шрифты не включены, используется системный запасной шрифт из исходного стека.

## Ограничения

Выводы строятся по загруженному файлу и выбранным целям. Инструмент не видит настройки кабинета, атрибуцию и сделки вне отчета. Перед изменением рекламы проверьте выводы по первичным данным.

## Проверки

```sh
npm install
npm test
```

Проверки используют синтетические вводные, расчетные примеры и файлы. Зависимости из `devDependencies` нужны для тестов; для открытия инструмента установка npm-пакетов не требуется.

## Исходная версия

Код выделен из опубликованных страниц Aksanov.Digital 2026-10-06. Расчетные формулы и пороги сохранены. HTML, CSS и JavaScript разнесены по файлам; внутренние ссылки ведут на исходный сайт. Источники и контрольные суммы фрагментов: [provenance.json](provenance.json).

## Как сослаться

Используйте кнопку GitHub «Cite this repository» или файл [CITATION.cff](CITATION.cff). В статье, презентации или описании своей доработки можно указать:

> Марат Аксанов. Аудитор рекламных отчетов. Aksanov.Digital. https://aksanov.digital/tools/advertising/ad-report-auditor

Ссылка на онлайн-версию при упоминании инструмента приветствуется. MIT требует сохранить уведомление об авторстве и текст лицензии в копиях кода; добавлять ссылку на сайт по условиям лицензии не требуется.

## Лицензия

[MIT](LICENSE), copyright 2026 Marat Aksanov. Лицензия относится к коду и документации этого проекта. Сторонние библиотеки и внешние медиа остаются под собственными лицензиями.

## English

Analyze advertising report exports locally in the browser. Review KPI, spend without conversions and tracking signals for Google Ads, Meta Ads, Yandex Direct and Telegram Ads. CSV and Excel input; CSV findings export.

Author: [Marat Aksanov](https://aksanov.digital/about). Original tools and methodology: [Aksanov.Digital](https://aksanov.digital/tools).

Open `index.html` in a modern browser, or serve the folder with `python3 -m http.server 8080`. No build step or account is required. Input data stays in the browser. Excel features require the pinned third-party CDN library noted above. This source snapshot excludes Tilda runtime and analytics. See [CITATION.cff](CITATION.cff) for attribution and [LICENSE](LICENSE) for MIT terms.
