---
source-hash: 82f8eb0792e7d1e839f270fe978f42afb1342112ba3154466d07b464ea6b59b9
sidebar_position: 18
title:  Плагіни
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import AndroidStore from '@site/src/components/buttons/AndroidStore.mdx';
import AppleStore from '@site/src/components/buttons/AppleStore.mdx';
import LinksTelegram from '@site/src/components/_linksTelegram.mdx';
import LinksSocial from '@site/src/components/_linksSocialNetworks.mdx';
import Translate from '@site/src/components/Translate.js';
import InfoIncompleteArticle from '@site/src/components/_infoIncompleteArticle.mdx';
import InfoAndroidOnly from '@site/src/components/_infoAndroidOnly.mdx';




## Огляд {#overview}

Плагіни значно розширюють функціональність OsmAnd. Кожен з них розроблений для вирішення конкретного завдання або випадку використання, наприклад, запису поїздки, доступу до статей Вікіпедії в автономному режимі, візуалізації даних про рельєф або надання виду на рівні вулиць.

Плагіни можуть бути внутрішніми, активованими в програмі OsmAnd, або зовнішніми, окремо встановленими програмами. Сторонні плагіни працюють через API OsmAnd і можуть отримувати доступ до даних OsmAnd.


## Налаштування плагіна {#configure-plugin}

Щоб отримати доступ до функціональності плагіна, його спочатку потрібно [увімкнути](#enable--disable), а деякі плагіни вимагають [придбання](#purchase) перед використанням. Потім, в деяких випадках, необхідно активувати певний шар карти або [налаштувати](#plugin-settings) профіль користувача.


### Увімкнути / Вимкнути {#enable--disable}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Перейдіть до: *<Translate android="true" ids="shared_string_menu,plugin_settings"/> →  &#65049; → Увімкнути*

![Enable plugins Android](@site/static/img/settings/plugins_enable_android.png) ![Plugin example Android](@site/static/img/settings/plugin_example_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

Перейдіть до: *<Translate ios="true" ids="shared_string_menu,plugins_menu_group"/> → &#10003;*

![Enable plugins iOS](@site/static/img/settings/plugins_enable_ios.png) ![Plugin example iOS](@site/static/img/settings/plugin_example_ios.png)

</TabItem>

</Tabs>

### Придбання {#purchase}

Більшість плагінів доступні безкоштовно, лише плагіни зі списку нижче вимагають придбання ліцензії [OsmAnd+ або OsmAnd Pro](../purchases/index.md) для використання:

- [Топографія](../plugins/topography.md)
- [3D Рельєф](../plugins/topography.md#3d-relief) (функція плагіна Топографія)
- [Вікіпедія](../plugins/wikipedia.md)
- [Морський вигляд карти](../plugins/nautical-charts.md)
- [Погода](../plugins/weather.md)

Детальну інформацію про придбання програми можна знайти в розділі [Придбання](../purchases/).

### Функції плагінів {#plugin-features}

Плагіни OsmAnd можуть доповнювати такі групи функцій: **Шари**, **Віджети**, **Дії контекстного меню**, **Дії бічної панелі**, **Стиль карти**, **Джерело карти**, **Профіль**.

🤖 *- тільки для версії OsmAnd для Android.*

| Назва плагіна | Функції |
|:------------|:-------|
| [Вікіпедія](#wikipedia) | [Шар карти](../plugins/wikipedia.md#download-wikipedia-packages), [Контекстне меню](../plugins/wikipedia.md#wikipedia-languages) |
| [Онлайн карти](#online-maps) |[Шар карти](../plugins/online-map.md#configure-map-source) |
| [Запис поїздки](#trip-recording) | [Віджет](../plugins/trip-recording.md#widgets), [Профіль](../plugins/trip-recording.md#profile-settings) |
| [Топографія](#topography) | [Шар карти](../plugins/topography.md#hillshade-slope-and-altitude-layers) |
| [3D Рельєф](#topography) 🤖  | [Шар карти](../plugins/topography.md#3d-relief) |
| [Погода](../plugins/weather.md) | [Шар карти](../plugins/weather.md#display-weather-on-the-map), [Віджет](../plugins/weather#weather-widgets), [Екран](../plugins/weather.md#configure-screen) |
| [Морський вигляд карти](#nautical-map-view) | [Стиль карти](../plugins/nautical-charts.md#nautical-map-style), [Профіль](../plugins/nautical-charts.md#nautical-options)  |
| [Вигляд лижної карти](#ski-map-view) | [Стиль карти](../plugins/ski-maps.md#set-winter-style), [Профіль](../plugins/ski-maps.md#skiing-profile) |
|[Аудіо/відео нотатки](#audiovideo-notes) 🤖  | [Шар карти](../plugins/audio-video-notes.md#show-all-on-the-map), [Контекстне меню](../plugins/audio-video-notes.md#create), [Віджет](../plugins/audio-video-notes.md#recording-widget) |
|[Редагування OpenStreetMap](#openstreetmap-editing)| [Шар карти](../plugins/osm-editing.md#how-to-use) |
|[Позиція паркування](#parking-position) | [Контекстне меню](../plugins/parking.md#set-a-point), [Віджет](../plugins/parking.md#parking-widget) |
|[Mapillary](#mapillary) | [Шар карти](../plugins/mapillary.md#map-layer), [Контекстне меню](../plugins/mapillary.md#map-context-menu) , [Віджет](../plugins/mapillary.md#mapillary-widget)|
|[Зовнішні датчики](#external-sensors) 🤖  | [Віджет](../plugins/external-sensors.md#widgets) |
|[Доступність](#accessibility) 🤖  | [Спеціальні налаштування](../plugins/accessibility.md#plugin-settings) |
| [Розробка OsmAnd](#osmand-development) | [Спеціальні налаштування](../plugins/development.md#plugin-settings) |
| [OsmAnd Tracker](#osmand-tracker) 🤖  | [Шар карти](../plugins/osmand-tracker.md#active-marker-on-the-osmand-map), [Віджет](../plugins/osmand-tracker.md#osmand-tracker-widget), [Контекстне меню](../plugins/osmand-tracker.md#active-marker-on-the-osmand-map) |
| [AIS відстеження суден](#ais-vessel-tracker) 🤖  |  [Спеціальні налаштування](../plugins/ais-tracker.md#plugin-settings) |


### Налаштування плагінів {#plugin-settings}

:::caution ПРИМІТКА
Лише плагін розробки OsmAnd та плагін редагування OSM змінюють налаштування для всіх профілів. Решта плагінів налаштовуються для кожного профілю окремо.
:::

Більшість плагінів надають специфічні налаштування профілю або глобальні налаштування, до яких можна отримати доступ через:

- *Головне меню → Плагіни → Назва плагіна → Налаштування (&#x2699 для ios)* або
- *Головне меню → Налаштування → Профіль → [Налаштування плагіна](../personal/profiles.md#plugin-settings)*.

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Settings plugin Android 1](@site/static/img/plugins/development/access_plugin_settings_andr_2.png) ![Settings plugin Android 2](@site/static/img/plugins/development/access_plugin_settings_andr_1.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Settings plugin iOS 1](@site/static/img/plugins/development/access_plugin_settings_ios_2.png) ![Settings plugin iOS 2](@site/static/img/plugins/development/access_plugin_settings_ios_1.png)

</TabItem>

</Tabs>

Наступні плагіни надають власні налаштування:

🤖 *- тільки для версії OsmAnd для Android.*

| Назва плагіна | Налаштування |
|:------------|:-------|
| [Запис поїздки](#trip-recording) | Налаштування [режимів роботи](../plugins/trip-recording.md#recording-parameters) запису поїздки |
| [Погода](#weather) | Налаштування одиниць вимірювання для відображення погодних явищ |
|[Аудіо/відео нотатки](#audiovideo-notes) 🤖  | Вибір [формату відео, терміну зберігання тощо](../plugins/audio-video-notes.md#plugin-settings) |
|[Редагування OpenStreetMap](#openstreetmap-editing)| Вказати [логін](../plugins/osm-editing.md#plugin-settings) користувача |
|  [Зовнішні датчики](#external-sensors) 🤖  | Підключення до зовнішнього пристрою [Налаштування](../plugins/external-sensors.md#settings) |
|  [Доступність](#accessibility) 🤖  | [Налаштування](../plugins/accessibility.md#plugin-settings) дозволяють використовувати функції доступності [Android](https://www.android.com/accessibility/) в OsmAnd. |
| [Розробка OsmAnd](#osmand-development) | [Налаштування плагіна](../plugins/development.md#plugin-settings) дозволяють увімкнути спеціальні функції для розробників або досвідчених користувачів |
|  [OsmAnd Tracker](#osmand-tracker) 🤖  | Усі налаштування конфігуруються в окремій програмі |
| [AIS відстеження суден](#ais-vessel-tracker) | [Налаштування плагіна](../plugins/ais-tracker.md#plugin-settings) дозволяють увімкнути спеціальні налаштування |

### Дії плагінів {#plugin-actions}

**<Translate android="true" ids="reset_plugin_to_default"/>** - *за допомогою цієї опції налаштування плагіна можна скинути до значень за замовчуванням*.
**<Translate android="true" ids="copy_from_other_profile"/>** - *налаштування плагіна можна скопіювати з іншого профілю*.


## Список плагінів {#plugins-list}


### [Вікіпедія](./wikipedia.md) {#wikipedia}

Наявність Вікіпедії під час подорожі допоможе вам дізнатися більше про місця, які ви відвідуєте. Вона доступна в автономному режимі та показує статті Вікіпедії, пов'язані з цікавими місцями, прямо на карті.

### [Онлайн карти](./online-map.md) {#online-maps}

Онлайн карти OsmAnd є значним доповненням до бази даних OpenStreetMap, яка вже присутня в програмі. За допомогою цього плагіна ви можете додавати шари до своєї карти з інформацією з різних джерел.

### [Запис поїздки](./trip-recording.md) {#trip-recording}

Щоб розповісти історію про те, де ви були, дані GPS, такі як широта та довгота вашого місцезнаходження, можуть бути записані та збережені у файл, а потім повторно використані, покращені, доповнені шляховими точками, надані для навігації, поширені серед друзів тощо.

### [Топографія](./topography.md) {#topography}

Топографічна інформація, така як контурні лінії, затінення пагорбів, схили, 3D рельєф, допомагає візуально оцінити рельєф місцевості, побачивши висоту, рельєф, екстремуми, крутизну, точки однакової висоти тощо.

### [Морський вигляд карти](./nautical-charts.md) {#nautical-map-view}

Морський вигляд карти надає детальне графічне представлення океанів, морів, прибережних районів та річок, щоб допомогти вам орієнтуватися на воді, бачити популярні маршрути руху, перешкоди на водному шляху, гавані, якірні стоянки та інші важливі орієнтири.

### [Вигляд лижної карти](./ski-maps.md) {#ski-map-view}

Вигляд лижної карти показує зимові кольори та траси для спуску або бігових лиж, а також канатні дороги, крісельні підйомники, об'єкти та послуги поблизу, що корисно для навігації в таких місцях, як зони відпочинку, гірськолижні курорти та сноупарки.

### [Аудіо/відео нотатки](./audio-video-notes.md) {#audiovideo-notes}

Створюйте аудіо/відео нотатки для майбутнього використання, наприклад, щоб запам'ятати подію, сцену або взаємодію. Створені аудіо/відео нотатки доступні з *Моїх місць*, а також на карті як окремий шар користувацьких історій та думок, прив'язаних до геолокації. Тільки для Android.

### [Позиція паркування](./parking.md) {#parking-position}

Встановіть точку на карті, де ваш автомобіль залишено на вулиці, та повідомте свій календар, коли закінчиться час паркування. Це полегшить вам відстеження часу та місця розташування вашого автомобіля.

### [Редагування OpenStreetMap](./osm-editing.md) {#openstreetmap-editing}

Плагін редагування OpenStreetMap дозволяє вам робити внесок у OpenStreetMap, глобальну спільноту, яка створює всеосяжну карту світу та надає загальнодоступні актуальні дані з відкритим вихідним кодом.

### [Mapillary](./mapillary.md) {#mapillary}

Переглядайте види вулиць ваших маршрутів або цікавих місць, надані [Mapillary](https://www.mapillary.com/) (потрібне підключення до Інтернету).

### [Доступність](./accessibility.md) {#accessibility}

Плагін доступності робить функції доступності пристрою безпосередньо доступними в OsmAnd. Тільки для Android.

### [Зовнішні датчики](./external-sensors.md) {#external-sensors}

Підключіть зовнішні датчики для відображення їх даних в OsmAnd та збереження інформації в записах треків.

### [Показники транспортного засобу](./vehicle-metrics.md) {#vehicle-metrics}

Підключіть сканер OBD-II для відображення даних транспортного засобу в OsmAnd та збереження інформації в записах треків.

### [Погода](./weather.md) {#weather}

Показує погодинний прогноз на поточний день та на 7 днів вперед.

### [Розробка OsmAnd](./development.md) {#osmand-development}

Плагін розробки OsmAnd призначений для розробників та досвідчених користувачів. Він дозволяє імітувати навігаційні маршрути, перевіряти продуктивність рендерингу екрана тощо.

### [OsmAnd Tracker](./osmand-tracker.md) {#osmand-tracker}

OsmAnd Tracker допомагає вам бачити, де знаходяться ваші контакти на карті в OsmAnd. Тільки для Android.

### [AIS відстеження суден](./ais-tracker.md) {#ais-vessel-tracker}

Відображення позицій AIS та інформації про навколишні судна. Дані AIS отримуються через мережу від зовнішнього приймача AIS.

## [Створення власного плагіна](./custom.md) {#create-a-custom-plugin}

Ви можете створити власний плагін, дотримуючись статті *Користувацький пакет*.


_______

> *Останнє оновлення: Березень 2025*