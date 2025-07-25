---
source-hash: 56e675ee7bba3e19ed4b22cb159f2939d58b0959b64b16aa30eb1a5eaeb05b9d
sidebar_position: 2
title:  AIS Vessel Tracker
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


<InfoIncompleteArticle/>

<InfoAndroidOnly />

## Огляд {#overview}

Плагін **AIS Vessel Tracker** відображає позиції [Автоматичної ідентифікаційної системи (AIS)](https://en.wikipedia.org/wiki/Automatic_identification_system) та детальну інформацію про судна поблизу. Дані AIS отримуються через мережеве з'єднання від зовнішнього приймача AIS.

:::caution ВІДМОВА ВІД ВІДПОВІДАЛЬНОСТІ
**Цей плагін є хобі-проєктом і не призначений для забезпечення надійності чи точності. НЕ покладайтеся на це програмне забезпечення для навігації чи безпеки життя.**
:::


## Необхідні параметри налаштування {#required-setup-parameters}

Можливість використання онлайн-карт автоматично ввімкнена у версії OsmAnd для iOS. Щоб відображати онлайн-карти в Android, потрібно зробити наступні налаштування:

1. [Увімкніть](../plugins/index.md#enable--disable) плагін **AIS vessel tracker** у *Головному меню → Плагіни → AIS vessel tracker*.
2. Налаштуйте [налаштування AIS](../map/raster-maps.md#select-raster-maps)
3. Налаштуйте **з'єднання з сервером AIS** або підключіть **зовнішній приймач AIS**.
4. Перевірте, чи відображаються судна на карті OsmAnd.

## Судна на карті {#vessels-on-the-map}

AIS працює на *УКХ-частотах* (161.975 МГц та 162.025 МГц) і має обмежений діапазон сигналу через поширення в межах прямої видимості.

***Типовий діапазон прийому AIS:***

- 15–20 морських миль (28–37 км)
- Залежить від висоти антени, умов навколишнього середовища та перешкод

***Відображення AIS на карті:***

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![AIS vessel tracker](@site/static/img/plugins/ais/ais.png)

</TabItem>

</Tabs>

При правильному налаштуванні на карті з'являться позиції суден. Основні функції:

- Судна рухаються відповідно до швидкості та курсу в реальному часі.
- Нові судна динамічно з'являються та зникають з видимої області.
- Натискання на судно відкриває детальну інформацію.


### Інформація про судно AIS {#ais-vessel-information}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![AIS vessel tracker](@site/static/img/plugins/ais/ais_menu.png)  
![AIS vessel tracker](@site/static/img/plugins/ais/ais_menu_2.png)

</TabItem>

</Tabs>

Судна AIS передають три типи даних:

1. Статична інформація (незмінні дані).  
    *Надсилається кожні **6 хвилин** або за запитом.*

    - **Назва судна** (*якщо встановлено*)  
    - **MMSI (Maritime Mobile Service Identity)** (*Унікальний 9-значний ідентифікатор судна*)
    - **Номер IMO** (*якщо доступний*)  
    - **Позивний**  
    - **Тип судна** (*наприклад, вантажне, пасажирське, рибальське судно*)  
    - **Розміри судна** (*довжина та ширина*)  
    - **Позиція антени AIS** (*відносно корпусу судна*)  

2. Динамічна інформація (дані в реальному часі).  
    *Надсилається з різними інтервалами залежно від швидкості та маневрування.*

    - **Координати судна (широта та довгота)**  
    - **Курс над землею (COG)**  
    - **Швидкість над землею (SOG)**  
    - **Курс** (*напрямок носа*)
    - **Статус судна** (*в русі, на якорі, маневрує тощо*)  
    - **Швидкість повороту (ROT)** (*швидкість зміни курсу*)  
    - **Час останнього оновлення**  

3. Інформація про рейс (встановлюється екіпажем вручну).  
    *Надсилається кожні **6 хвилин**, встановлюється екіпажем вручну*

    - **Порт призначення**
    - **Орієнтовний час прибуття (ETA)**  
    - **Осадка** (*глибина судна під поверхнею води*)  
    - **Тип вантажу** (*якщо передається*)
    - **Кількість людей на борту** (*необов'язково*)  

### Символи та легенди AIS {#ais-symbols-and-legends}

[Настанови щодо представлення символів AIS](https://www.e-navigation.nl/sites/default/files/sn_circ243-rev.2_-_guidelines_for_the_presentation_of_navigation-related_symbols_terms_and_abbreviations.pdf)

| Символи             | Опис   |
|---------------------|---------------|
| | |
| **Символи типів суден** |    |
| *Зелений трикутник*    | Вантажне судно    |
| *Синій трикутник*     | Пасажирське судно |
| *Чорний трикутник*    | Рибальське судно |
| *Жовтий трикутник*   | Буксир       |
| *Червоний трикутник*      | Танкер        |
| *Білий трикутник*    | Військове судно |
| *Помаранчевий трикутник*   | Спеціальне судно (наприклад, лоцманське, криголам) |
| *Миготливий червоний трикутник* | Судно в біді |
| | |
| **Символи навігаційних засобів** |    |
| *Зелений буй*              | Правий маркер (права сторона каналу) |
| *Червоний буй*                | Лівий маркер (ліва сторона каналу) |
| *Символ якоря*           | Район якірної стоянки |
| *Символ судна (SS)*        | Поромний або пасажирський термінал |
| *Символ портового крана*       | Вантажний порт |
| *Чорне коло*            | Офшорна платформа |
| | |
| **Індикатори стану** |    |
| *Суцільний трикутник*  | Рухоме судно |
| *Порожній трикутник* | На якорі або пришвартоване |
| *Обертова стрілка*  | Виконує маневр |
| *Червона миготлива іконка* | Аварійне сповіщення |
| *Помаранчевий знак оклику* | Повідомлення про безпеку AIS |
| | |
| **Індикатори маршруту та швидкості** |    |
| *Тонка синя лінія*  | Запланований маршрут |
| *Пунктирна лінія*     | Минулий трек |
| *Іконка годинника*      | Орієнтовний час прибуття (ETA) |
| *Іконка хвилі*       | Швидкість над водою |

## Налаштування плагіна {#plugin-settings}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

*<Translate android="true" ids="shared_string_menu,plugins_menu_group,plugin_ais_tracker_name,shared_string_settings"/>*

![AIS settings](@site/static/img/plugins/ais/ais_settings_2.png)  

</TabItem>

</Tabs>

Плагін *AIS vessel tracker* пропонує різні налаштування для персоналізації навігації та взаємодії для користувачів з обмеженими можливостями. Ці налаштування застосовуються для всіх [профілів](../personal/profiles.md) в OsmAnd.

| Налаштування |  Опис  | Приклад  |
|---------|---------------|----------|
| | | |
| **Налаштування IP-адреси** | | |
| Протокол   | Виберіть протокол для отримання даних AIS | `UDP/TCP` |
| IP-адреса | Визначте IP-адресу джерела даних AIS (якщо використовується TCP) | `192.168.200.16` |
| TCP-порт   | Визначте номер TCP-порту для даних AIS | `4001` |
| UDP-порт   | Визначте UDP-порт для прийому AIS в OsmAnd  | `10110` |
| | | |
| **Таймаут прийому сигналу AIS** | |  |
| Таймаут для втрачених об'єктів AIS     | Судна зникають, якщо сигнал не надходить протягом встановленого часу | `3 - 20 хв` |
| Таймаут для видимості судна      | Іконки суден змінять стан, якщо сигнал не надходить | `2 - 15 хв / Вимкнено` |
| | | |
| **Сповіщення про найближчу точку зближення (CPA)** | | |
| Час попередження CPA | Судно позначається червоним, якщо час до CPA нижче цього ліміту | `1 - 60 хв / Вимкнено` |
| Відстань попередження CPA | Судно позначається червоним, якщо відстань до CPA нижче цього ліміту | `0.02 - 2 морські милі` |


### Режим симуляції AIS {#ais-simulation-mode}

> *Ви можете симулювати позиції суден AIS за допомогою [плагіна OsmAnd Development](../plugins/development.md).*

1. **Завантажте текстові файли даних AIS**:

    - [AIS Test 1](https://github.com/user-attachments/files/18689404/ais_test_1.txt)
    - [AIS Test 2](https://github.com/user-attachments/files/18689405/ais_test_2.txt)
    - [Single 3](https://github.com/user-attachments/files/18689403/333.txt)

2. **Завантажте дані AIS в OsmAnd**  
Відкрийте *<Translate android="true" ids="shared_string_menu,plugins_menu_group,development,shared_string_settings,ais_load_data"/>* і виберіть один із завантажених файлів.

3. **Перегляньте судна AIS на карті**  
Іконки суден з'являться на основі симульованих даних. Натисніть на іконку судна, щоб переглянути детальну інформацію.


## Пов'язані статті {#related-articles}

- [Взаємодія з картою](../../user/map/interact-with-map.md)
- [Глобальні налаштування](../../user/personal/global-settings.md)
- [Векторні карти (стилі карт)](../../user/map/vector-maps.md)
- [Морський плагін](../../user/plugins/nautical-charts.md)

> *Останнє оновлення: березень 2025*