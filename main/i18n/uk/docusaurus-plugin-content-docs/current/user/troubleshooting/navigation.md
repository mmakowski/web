---
source-hash: 4279e8b0f36e69d2e860ec2e48cb3a48d0b171f309dc5569b62b8e5d94ae87fa
sidebar_position: 3
title: Навігація
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import AndroidStore from '@site/src/components/buttons/AndroidStore.mdx';
import AppleStore from '@site/src/components/buttons/AppleStore.mdx';
import LinksTelegram from '@site/src/components/_linksTelegram.mdx';
import LinksSocial from '@site/src/components/_linksSocialNetworks.mdx';
import Translate from '@site/src/components/Translate.js';
import InfoIncompleteArticle from '@site/src/components/_infoIncompleteArticle.mdx';



## Розрахунок маршруту {#route-calculation}

### Розрахунок маршруту повільний {#route-calculation-is-slow}

*Android*. OsmAnd використовує два різні **офлайн-рушії маршрутизації**: *рушій на основі Java* та *нативний рушій (C++)*.

- *Рушій на основі Java* використовується в [Безпечному режимі](../plugins/development.md#safe), але він приблизно в 10 разів повільніший за нативний рушій. Він також має суворі обмеження пам’яті, що може призвести до помилок, таких як *Недостатньо пам’яті для обчислення*. Якщо ви зіткнулися з цією проблемою, перейдіть до *Плагіни → Розробка OsmAnd → Налаштування →* [*Безпечний режим*](../plugins/development.md#safe) і переконайтеся, що ця опція вимкнена.
- *Нативний рушій (C++)* забезпечує кращу продуктивність, але його ефективність залежить від пам’яті та можливостей процесора вашого пристрою. Зазвичай, нативна маршрутизація добре працює для маршрутів до 300 км, з часом розрахунку маршруту від 15 секунд до 4 хвилин. Якщо процес займає більше 4 хвилин, бажано зупинитися, оскільки програма може вийти з ладу.


### Як розрахувати маршрути довше 250 км? {#how-to-calculate-routes-longer-than-250km}

1. Якщо програма не показує маршрут після 7-8 хвилин розрахунку, розгляньте можливість [розміщення проміжних точок](../navigation/setup/route-navigation.md#route-recalculation) (наприклад, виберіть місця на автомагістралях). 3-4 проміжні точки буде достатньо для розрахунку навіть 1000 км маршрутів.

2. Для топових пристроїв ви можете збільшити пам’ять до 512 МБ або 1024 МБ - [Пам’ять, виділена для маршрутизації](../plugins/development.md#memory-allocated-for-routing).

3. Для версії Android ви можете створити профіль навігації з онлайн-маршрутизацією або маршрутизацією сторонніх розробників (BRouter). Докладніше про це читайте [тут](../navigation/routing/brouter.md).

### Розрахунок 50 км маршрутів для пішоходів {#calculation-of-50-km-routes-for-pedestrians}

Якщо ви використовуєте профіль **Пішки** в OsmAnd, програма може вийти з ладу при розрахунку маршрутів довше 50 км. Ця проблема виникає саме тоді, коли в налаштуваннях навігації вибрано [**Стандартна маршрутизація A***](../navigation/guidance/navigation-settings.md#development-settings). Кілька факторів можуть сприяти цій проблемі:

- Довжина маршруту перевищує 50 км.
- Кількість прямих точок на маршруті перевищує 1 мільйон.
- Ви використовуєте мобільний пристрій для розрахунку маршруту, що не рекомендується для маршрутів такої довжини. Розгляньте можливість використання веб-версії для кращої продуктивності.

Щоб уникнути збоїв з маршрутами подібної відстані, ви можете переключитися на інші типи профілів, наприклад **Велосипед**.


## Розрахований маршрут здається неправильним {#the-calculated-route-does-not-seem-correct}

Щоб відстежити проблеми з неправильними або неоптимальними маршрутами, будь ласка, відкрийте нове повідомлення в [обговореннях Github](https://github.com/osmandapp/OsmAnd/discussions) або [проблемі Github](https://github.com/osmandapp/Osmand/issues) і якомога детальніше вкажіть наступну інформацію:

- Яку версію OsmAnd ви використовуєте, на якому пристрої?
- Ви використовуєте офлайн-карти, запропоновані для завантаження в додатку OsmAnd, чи онлайн (плиткові / растрові) карти?
- Якщо ви використовуєте офлайн-карти, вкажіть точну назву файлу карти, де виникає проблема з маршрутизацією, та дату її видання.
- Вкажіть, чи використовували ви офлайн-маршрутизацію в додатку OsmAnd, чи будь-якого онлайн-провайдера маршрутизації, такого як YOURS, OpenRouteService або OSRM.
- Який профіль маршрутизації вибрано в додатку OsmAnd (автомобіль, велосипед чи пішохід)?
- Будь ласка, якомога точніше вкажіть початкову та кінцеву точки вашого маршруту. Якщо можливо, вкажіть назву міста та назву вулиці для кожної. Також може бути корисним [Permalink](https://wiki.openstreetmap.org/wiki/Permalink) з openstreetmap.org.
- Розкажіть про очікуваний маршрут і про те, як маршрутизує OsmAnd.

## Інформація про дорогу {#road-information}

### OsmAnd показує лише деякі камери контролю швидкості {#osmand-only-shows-some-speed-cams}

Завдяки геоданим, взятим з проєкту OpenStreetMap, наразі існує два методи інтеграції камер контролю швидкості в необроблені дані OSM:

- Точка (названа "вузлом" в термінології OSM) шляху позначена тегом "highway=speed_camera", див. вікі OSM за адресою [highway=speed_camera](https://wiki.openstreetmap.org/wiki/Tag%3Ahighway%3Dspeed_camera)
- Група елементів даних OSM об'єднана в так зване "відношення", яке містить більше елементів, ніж один вузол, для опису напрямку, який охоплює камера контролю швидкості. Див. [Relation:enforcement](https://wiki.openstreetmap.org/wiki/Relation:enforcement).

Наразі OsmAnd може використовувати лише елементи, що складаються з одного вузла. Аналіз відношень буде додано в майбутньому випуску.


## Голосова навігація {#voice-navigation}

### Чому я маю використовувати голос TTS замість записаного голосу? {#why-should-i-use-a-tts-voice-instead-of-a-recorded-voice}

Голоси **Text-to-Speech (TTS)** динамічно генерують голосові підказки, дозволяючи їм вимовляти назви вулиць, назви місць та номери автомагістралей. На відміну від цього, **записані голоси** обмежені попередньо записаними фразами і не можуть вимовляти конкретні назви чи номери.

*Переваги TTS над записаними голосами:*

- Вимовляє назви вулиць та динамічну інформацію.
- Регулярно оновлюється новими функціями.
- Пропонує кращу гнучкість для навігації.

Щоб використовувати TTS в OsmAnd, на вашому пристрої має бути встановлений **рушій TTS**. Багато пристроїв мають попередньо встановлений рушій TTS, але за необхідності можна встановити додаткові. [Список підтримуваних рушіїв TTS та мов для Android](https://accessibleandroid.com/list-of-languages-with-available-tts-engines-on-android/).

Для детальних інструкцій щодо налаштування та коригування голосових підказок зверніться до: [Посібник з налаштування голосової навігації](../navigation/guidance/voice-navigation.md).

### TTS не працює належним чином? Виконайте ці кроки, щоб виправити це {#tts-does-not-function-properly-follow-these-steps-to-fix-it}

Проблеми з **Text-to-Speech (TTS)** зазвичай пов’язані з **системними налаштуваннями Android**, а не з самим додатком OsmAnd.

1. Переконайтеся, що встановлено рушій TTS.

    - Відкрийте *Налаштування пристрою → Мова та введення → Параметри Text-to-Speech*.
    - Перевірте, чи встановлено **рушій TTS** (наприклад, Google TTS, Samsung TTS, Pico).
    - Якщо рушій не встановлено, виберіть *“Встановити більше…”* і завантажте сумісний.
    - [Список підтримуваних рушіїв TTS та мов.](https://accessibleandroid.com/list-of-languages-with-available-tts-engines-on-android/)

2. Перевірте налаштування мови TTS.

    - Виберіть мову, яку ви хочете використовувати, в *Налаштуваннях Android → Параметри Text-to-Speech*.
    - Натисніть *“Прослухати приклад”*, щоб перевірити, чи працює рушій TTS.
    - Якщо ви нічого не чуєте, оновіть або перевстановіть рушій TTS.

3. Налаштуйте параметри голосової навігації OsmAnd.

    - Відкрийте *OsmAnd → Меню → Налаштувати профіль → Налаштування навігації → Голосові підказки*.
    - Виберіть сумісну *Мову → TTS*.
    - Перевірте голосові підказки, перейшовши до *Меню → Плагіни → Увімкнути розробку OsmAnd → Налаштування → Тестувати голосові підказки*.

#### Додаткові кроки {#additional-steps}

- *Оновіть Google TTS*. Відкрийте Google Play Store, знайдіть **Google Text-to-Speech** та оновіть його.
- *Симулюйте навігацію*. Натисніть *Кнопку навігації → Налаштування → Симулювати навігацію*, щоб перевірити, чи відтворюється голосове керівництво.
- *Перевстановіть OsmAnd*:
   - **Створіть резервну копію налаштувань:** *Меню → Налаштування → Експорт у файл*.
   - Видаліть OsmAnd, потім перевстановіть його з магазину додатків.
   - Відновіть налаштування: *Меню → Налаштування → Імпорт файлу*.

Для додаткового усунення несправностей відвідайте:

- [Посібник з голосової навігації](../navigation/guidance/voice-navigation.md)
- [Імпорт/Експорт налаштувань](../personal/import-export.md)


## Інше {#other}

### Навігація зупиняється, коли екран вимкнено {#navigation-stops-while-screen-is-off}

- [Та сама проблема](../troubleshooting/track-recording-issues.md#the-system-may-kill-background-apps-to-save-power) із записом треку у фоновому режимі.