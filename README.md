# Города и регионы России со склонениями

> Russia cities and regions JSON dataset

## Описание файлов

- `russia-regions.json` - регионы Российской Федерации: **83 субъекта**
- `russia-cities.json` - населённые пункты со статусом города: **1102 города**, включая регион каждого из них

В списки входят коды ФИАС, принадлежность регионам и столицам, склонения названий по падежам и много другой информации.

Названия географических объектов указаны с буквой «Ё», где это необходимо. В поле `name_alt` указано название города с заменой буквы «ё» на «е».

Москва и Санкт-Петербург являются городами федерального значения, поэтому регионом для них указаны сами города.

Города в составе городов федерального значения (Зеленоград, Троицк и т.п.) в список не входят.

## Актуальность данных

Всего городов: 1102 — данные на 2023 год. В 2023 году статус города получили населённые пункты Колтуши Ленинградской области и Ачхой-Мартан Чеченской Республики.

Численность населения указана по итогам переписи населения на 1 октября 2021 года.

## Описание полей

В квадратных скобках указан номер в списке источников данных

```jsonc
{
  "name": "Олёкминск", // название города на русском языке [2]
  "name_alt": "Олекминск", // название города на русском языке с заменой буквы «ё» [2]
  "label": "olyokminsk", // уникальная метка города, дефисы и пробелы заменены на подчёркивания. Может использоваться в url, разметке рекламных кампаний и подобных задачах
  "type": "Город", // тип объекта полностью [1]
  "typeShort": "г", // тип объекта кратко [1]
  "contentType": "city", // тип объекта [1]
  "id": "1402300100000", // КЛАДР код объекта [1]
  "okato": "98241501000", // код ОКАТО [1]
  "oktmo": "98641101001", // код ОКТМО [1]
  "guid": "c3aba7f3-caf7-443f-a906-8d79e6ec37f6", // ФИАС код объекта [1]
  "isDualName": false, // признак города с неуникальным названием
  "isCapital": false, // признак столицы региона
  "zip": 678100, // почтовый индекс [1]
  "population": 8398, // население [2]
  "yearFounded": 1635, // год основания или первое упоминание (не для всех городов это цифровое значение) [2]
  "yearCityStatus": 1783, // год присвоения статуса города. При неоднократном присвоении статуса указан год последнего присвоения [2]
  "name_en": "Olyokminsk", // название на английском языке [5]
  "namecase": {
    // склонение названия по падежам [6]
    "nominative": "Олёкминск", // именительный
    "genitive": "Олёкминска", // родительный
    "dative": "Олёкминску", // дательный
    "accusative": "Олёкминск", // винительный
    "ablative": "Олёкминском", // творительный
    "prepositional": "Олёкминске", // предложный
    "locative": "Олёкминске" // местный (для ответа на вопрос «где?» следует использовать его)
  },
  "coords": { "lat": 60.3758006, "lon": 120.4060878 }, // координаты [7]
  "timezone": { // часовой пояс [8]
      "tzid": "Asia/Yakutsk",
      "abbreviation": "YAKT",
      "utcOffset": "UTC+09:00",
      "mskOffset": "MSK+06"
  },
  "region": {
    // информация о регионе объекта, эта часть также выделена в отдельный список регионов
    "name": "Саха /Якутия/", // название на русском языке [1]
    "label": "yakutiya", // человекочитаемая уникальная метка
    "type": "Республика", // тип объекта полностью [1]
    "typeShort": "Респ", // тип объекта кратко [1]
    "contentType": "region", // тип объекта [1]
    "id": "1400000000000", // КЛАДР код объекта [1]
    "okato": "98000000000", // код ОКАТО [1]
    "oktmo": "98000000", // код ОКТМО [1]
    "guid": "c225d3db-1db6-4063-ace0-b3fe9ea3805f", // ФИАС код объекта [1]
    "code": "14", // порядковый код региона [3]
    "iso_3166-2": "RU-SA", // код ISO 3166-2 [4]
    "population": 995686, // население [3]
    "yearFounded": 1922, // год образования [3]
    "area": 3083523, // площадь в км² [3]
    "fullname": "Республика Саха /Якутия/", // полное официальное наименование
    "unofficialName": "Якутия", // неофициальное наименование (необязательное поле)
    "name_en": "Republic of Sakha (Yakutia)", // название на английском языке [5]
    "district": "Дальневосточный", // принадлежность к федеральному округу [2]
    "namecase": {
      // склонения полного наименования [6]
      "nominative": "Республика Саха /Якутия/",
      "genitive": "Республики Саха /Якутия/",
      "dative": "Республике Саха /Якутия/",
      "accusative": "Республику Саха /Якутия/",
      "ablative": "Республикой Саха /Якутия/",
      "prepositional": "Республике Саха /Якутия/",
      "locative": "Республике Саха /Якутия/"
    },
    "capital": {
      // столица или административный центр региона, значения полей как у города
      "name": "Якутск",
      "label": "yakutsk",
      "id": "1400000100000",
      "okato": "98401000000",
      "oktmo": "98701000001",
      "contentType": "city"
    }
  }
}
```

## Источники данных

1. [База ФИАС](https://fias.nalog.ru/) через сервис [ФИАС в облаке](https://kladr-api.ru/)
2. [Список городов России - Wikipedia](https://ru.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D0%B3%D0%BE%D1%80%D0%BE%D0%B4%D0%BE%D0%B2_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8)
3. [Список субъектов России - Wikipedia](https://en.wikipedia.org/wiki/Federal_subjects_of_Russia#List)
4. [ISO 3166-2:RU - Wikipedia](https://ru.wikipedia.org/wiki/ISO_3166-2:RU)
5. [List of cities and towns in Russia - Wikipedia](https://en.wikipedia.org/wiki/List_of_cities_and_towns_in_Russia)
6. [Morphos](https://github.com/wapmorgan/Morphos)
7. [ru-cities - Github](https://github.com/epogrebnyak/ru-cities)
8. [Time in Russia - Wikipedia](https://en.wikipedia.org/wiki/Time_in_Russia)

## Города с неуникальными названиями

Обратите внимание на города с одинаковыми названиями, поиск по первому вхождению названия сыграет злую шутку, не делайте так. Каждый город с неуникальным названием имеет признак `isDualName: true`

Список городов с повторяющимися названиями:

- Берёзовский - Кемеровская область
- Берёзовский - Свердловская область
- Благовещенск - Амурская область
- Благовещенск - Республика Башкортостан
- Гурьевск - Калининградская область
- Гурьевск - Кемеровская область
- Железногорск - Красноярский край
- Железногорск - Курская область
- Заречный - Пензенская область
- Заречный - Свердловская область
- Киров - Калужская область
- Киров - Кировская область
- Кировск - Ленинградская область
- Кировск - Мурманская область
- Красноармейск - Московская область
- Красноармейск - Саратовская область
- Краснознаменск - Калининградская область
- Краснознаменск - Московская область
- Краснослободск - Волгоградская область
- Краснослободск - Республика Мордовия
- Мирный - Архангельская область
- Мирный - Республика Саха (Якутия)
- Михайловск - Свердловская область
- Михайловск - Ставропольский край
- Никольск - Вологодская область
- Никольск - Пензенская область
- Озёрск - Калининградская область
- Озёрск - Челябинская область
- Приморск - Калининградская область
- Приморск - Ленинградская область
- Радужный - Владимирская область
- Радужный - Ханты-Мансийский АО
- Советск - Калининградская область
- Советск - Кировская область
- Советск - Тульская область
- Фокино - Брянская область
- Фокино - Приморский край

## Contributions

Исправления, дополнения, идеи с благодарностью принимаю в issue или PR, пишите!

Created by Timur Arbaev https://github.com/arbaev
