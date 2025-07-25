---
source-hash: fb9912804ef2b1009e063e1cb1e5c8220b279d2fee5b64bf122b770e595651c9
sidebar_position: 1
title: Planowanie trasy
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

## Przegląd {#overview}

Narzędzie **Planowanie trasy** (*Menu → Planowanie trasy*) to potężna funkcja aplikacji OsmAnd, która umożliwia [tworzenie nowych tras](#create-new-route) jako śladów GPX, [edycję i dodawanie nowych segmentów](#segments) do już zapisanych śladów, [mierzenie odległości](#distance-measurement) na mapie oraz [dołączanie segmentów śladu](#attach-track-to-roads) do najbliższej dostępnej drogi przy użyciu różnych profili nawigacyjnych. Funkcja ta została zaprojektowana do działania w *trybie offline*.

Trasa składa się z zestawu segmentów między określonymi punktami. Segmenty mogą być liniami prostymi lub trasami dostosowanymi do wybranego profilu. Trasę można zapisać jako GPX do późniejszego importu, edycji i [nawigacji](../navigation/setup/gpx-navigation.md).

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android](@site/static/img/plan-route/plan_route_overview_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route ios](@site/static/img/plan-route/plan_route_overview_ios.png)

</TabItem>

</Tabs>

## Główne przypadki użycia {#main-use-cases}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Przejdź do: *<Translate android="true" ids="shared_string_menu,plan_a_route"/>*

![Plan a route android](@site/static/img/plan-route/plan-route-menu-andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Przejdź do: *<Translate ios="true" ids="shared_string_menu,plan_route"/>*

![Plan a route ios](@site/static/img/plan-route/plan-route-menu-ios.png)

</TabItem>

</Tabs>

### Tworzenie nowej trasy {#create-new-route}

Aby utworzyć nowy ślad w formacie GPX, użyj głównej funkcji narzędzia *Planowanie trasy*. Wcześniejsze utworzenie trasy ma wiele zalet, w przeciwieństwie do nagrywania bieżącego śladu za pomocą *[Wtyczki nagrywania podróży](../plugins/trip-recording.md)*. Możesz [dodać](#adding-points) dowolną liczbę punktów do trasy, [usunąć i przenieść je](#point-context-menu), zmienić typy tras według [segmentów](#route-between-points) i uzyskać [szczegółowe informacje o trasie](#graph).

Domyślnie typ routingu będzie odpowiadał wcześniej wybranemu profilowi, dotknij ikony routingu, aby wybrać, w jaki sposób aplikacja ma obliczyć segment do połączenia punktów. Dostępny profil powinien być skonfigurowany [oddzielnie](../navigation/routing/osmand-routing.md#routing-types).

Możesz **powiększać i pomniejszać** w celu łatwego umieszczania punktów podczas tworzenia lub edycji śladu. Po **pomniejszeniu** punkty na śladzie stają się niewidoczne, co pozwala na lepszy widok całej długości śladu i mapy jako całości. Widoczny pozostaje tylko ostatnio dodany punkt i wskaźnik do dodawania następnego punktu.

### Modyfikowanie istniejącego śladu GPX {#modify-existing-gpx-track}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Przejdź do: *<Translate android="true" ids="shared_string_menu,plan_a_route,plan_route_open_existing_track"/> / <Translate android="true" ids="plan_route_import_track"/>*

</TabItem>

<TabItem value="ios" label="iOS">

Przejdź do: *<Translate ios="true" ids="shared_string_menu,plan_route,plan_route_open_existing_track"/>*

</TabItem>

</Tabs>

Narzędzie *Planowanie trasy* umożliwia modyfikowanie istniejącego śladu GPX, a także [zaimportowanego śladu](../personal/tracks/manage-tracks.md#import). Jeśli jednak musisz wykluczyć dużą liczbę punktów na podstawie ogólnych kryteriów, [<Translate android="true" ids="shared_string_gps_filter"/>](../map/tracks/track-context-menu.md#gps-filter) może być bardziej odpowiednim narzędziem.

### Pomiar odległości {#distance-measurement}

![Plan a route android](@site/static/img/plan-route/plan_route_lines_andr.png)

*Planowanie trasy* to szybki i łatwy sposób na zmierzenie odległości między punktami.

- Wybierz metodę planowania trasy *Linia prosta*. Między punktami zostanie narysowana linia przerywana.
- [Dodaj](#adding-points) pierwszy punkt na mapie, z którego zostanie narysowana linia.
- Przesuń mapę, aby określić odległość i azymut. Informacje zostaną wyświetlone w polu z listą punktów pod mapą.

:::note
*Linia prosta* jest potrzebna i będzie używana w obszarach nieobjętych danymi routingu, takich jak obszary poza drogami i poza śladami.
:::

### Uzyskiwanie danych wysokościowych {#get-elevation-data}

<InfoAndroidOnly />

![Plan a route android](@site/static/img/plan-route/plan_route_graph_4_andr.png)

Jeśli w istniejącym śladzie brakuje [danych wysokościowych](../map/tracks/track-context-menu.md#calculating-missing-elevation), można je dodać za pomocą następujących narzędzi:

- [Użyj pobliskich dróg](#attach-track-to-roads). Ten tryb wykorzystuje mapy offline do znalezienia najbliższych dróg do zbudowania śladu, więc dane wysokościowe zostaną pobrane z dołączonych dróg. Geometria śladu może być dostosowana.
- [Użyj map terenu](../map/tracks/track-context-menu.md#calculating-missing-elevation). ([OsmAnd Pro](../purchases/android.md#pro-features)) Tryb oblicza wysokość na podstawie danych map terenu (3D). Różnica między wysokościami zarejestrowanymi przez Twoje urządzenie może być wykorzystana do korekcji wysokości. Geometria śladu pozostaje niezmieniona.

### Dołącz ślad do dróg {#attach-track-to-roads}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route snap-road-ios](@site/static/img/plan-route/plan_route-snap_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route snap-road-ios](@site/static/img/plan-route/plan_route-snap_ios.png)

</TabItem>

</Tabs>

Ustawienie **Dołącz do dróg** umożliwia dołączenie nagranego lub zaimportowanego śladu do dróg z map offline OsmAnd w celu uzyskania dodatkowych informacji:

- Poprawne informacje o zakrętach dla [Nawigacji po śladzie](../navigation/setup/gpx-navigation.md#how-to-follow-the-track) (szczególnie na rondach).
- Nazwy ulic i informacje o pasach ruchu.
- Dane wysokościowe.
- [Atrybuty drogi](../navigation/setup/route-details.md#road-attributes).

Możesz wybrać [wartość progową](../navigation/setup/gpx-navigation.md#attach-to-the-roads) dla odległości, jaką uproszczone punkty śladu mogą mieć od oryginalnych punktów śladu.

:::note Ikona nieokreślonego profilu
Jeśli wybierzesz ślad i obok ikony *Ustawienia* zostanie wyświetlona ikona profilu ***nieokreślonego*** ("?"), dotknij jej, aby wybrać, czy dołączyć ślad do dróg, czy po prostu połączyć punkty prostą linią i traktować go jako nagrany ślad.
:::

<!--
### Add Route Points to Navigation from GPX {#add-route-points-to-navigation-from-gpx}

If you import a GPX file containing a route (with `<rtept>` elements), OsmAnd will display the route on the map but will not automatically convert the route points into a turn-by-turn navigation list.

To generate navigation instructions:

1. Open the GPX file from *My Places → Tracks*.
2. Tap the track to open it.
3. Tap the point menu (⋮) and choose **Add to Navigation**.
4. OsmAnd will convert the route points into a full navigation route with instructions.

> **NOTE:** *You may still use [Attach to roads](#attach-track-to-roads) to adjust geometry before converting to navigation.*
-->

## Punkty i segmenty {#points--segments}

### Dodawanie punktów {#adding-points}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android](@site/static/img/plan-route/plan_route_points_list_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route ios](@site/static/img/plan-route/plan_route_points_list_ios.png)

</TabItem>

</Tabs>

Aby zmierzyć odległość lub zaplanować podróż, dodawaj punkty w miejscu *Wskaźnika* jeden po drugim i dotknij przycisku *Dodaj punkt*. Uzyskując dostęp do **listy punktów** poniżej, możesz zmieniać kolejność punktów, usuwać je lub uzyskiwać dostęp do konkretnego [menu kontekstowego punktu](#point-context-menu).

:::note
Możesz również **Cofnąć**/**Ponowić** każdą akcję wykonaną w planowaniu trasy.
:::

### Trasa między punktami {#route-between-points}

Dodane punkty w edytorze mogą być połączone jako linia prosta lub jako trasa między punktami wybranego profilu. *Trasa między punktami* może być dostępna na kilka sposobów:

1. Z menu *Opcje* *→* *Trasa między punktami*.
2. Dotknij *ikony profilu* w lewym dolnym rogu ekranu mapy. Nie na górnej ikonie, otworzy się menu Konfiguruj mapę.
3. W *[menu kontekstowym punktu](#point-context-menu) → Zmień typ trasy przed/po*.

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android](@site/static/img/plan-route/plan_route_between_points_andr.png) ![Plan a route android](@site/static/img/plan-route/plan_route_change-route-type_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route ios](@site/static/img/plan-route/plan_route_between_points_ios.png) ![Plan a route ios](@site/static/img/plan-route/plan_route_change-route-type_ios.png)

</TabItem>

</Tabs>

Możesz zmienić trasę między 2 konkretnymi punktami lub między wieloma punktami:

- *Cały ślad*. Cały ślad zostanie przeliczony przy użyciu wybranego profilu.
- *Następny segment*. Tylko następny segment zostanie przeliczony przy użyciu wybranego profilu.
- *Zmień typ trasy przed/po punkcie*. W *menu kontekstowym punktu* możesz zmienić sposób obliczania trasy dla odcinka od tego punktu do najbliższego lub do punktu końcowego. Ustawienie zawiera informacje o odległości od tego punktu do początku lub końca trasy, lub do następnego/poprzedniego punktu.
- *Przelicz trasy*. Możesz użyć przeliczania trasy bez zmiany typu profilu. Ikona profilu wyświetlana na planowanej trasie w narzędziu nie zmieni się, ale typ trasy będzie odpowiadał wybranemu. Może to być potrzebne do znalezienia alternatywnych tras.

### Segmenty {#segments}

Segment śladu to zbiór punktów połączonych bez **przerw**. W narzędziu do planowania trasy możliwe jest:

- Łączenie segmentów: opcja [Połącz segmenty](#point-context-menu) usuwa przerwę do wcześniej oddzielonych segmentów.
- Dzielenie lub tworzenie nowych, niepołączonych sekcji śladu. Aby utworzyć nową, użyj opcji [Rozpocznij nowy segment](#point-context-menu) lub wybierz funkcję [Podziel](#point-context-menu) z menu kontekstowego punktu.

### Menu kontekstowe punktu {#point-context-menu}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android](@site/static/img/plan-route/plan_route_points_menu_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route ios](@site/static/img/plan-route/plan_route_points_menu_ios.png)

</TabItem>

</Tabs>

Każdy punkt na Twojej trasie ma swoje menu kontekstowe. Pokazuje ono *numer kolejny* punktu, *odległość od początku trasy*, funkcję przenoszenia go na mapie i usuwania, a także zestaw akcji z sekcjami trasy przed i po tym punkcie. Aby edytować, dotknij wymaganego punktu na [liście punktów](#adding-points) lub bezpośrednio na mapie.

- ***Informacje o punkcie***. Liczba punktów na liście. Odległość do pierwszego punktu jest oparta na ustawionym typie routingu, odległość może się zmienić po przeliczeniu na nowy typ, jeśli parametr *Trasa między punktami* zostanie zmieniony.

- ***<Translate ios="true" ids="move_point"/>***. Umożliwia zmianę położenia punktu na mapie. Przesuwaj mapę za pomocą gestów, aby zmienić położenie punktu. Wskaźnik punktu będzie znajdował się w centrum widocznej części mapy.

- ***<Translate ios="true" ids="add_point_after"/>***. Przesuń mapę, aby dodać punkt po wybranym punkcie. Możesz dodać tyle punktów, ile chcesz, dopóki nie dotkniesz anuluj lub zastosuj.

- ***<Translate ios="true" ids="add_point_before"/>***. Przesuń mapę, aby dodać tyle punktów, ile potrzeba po wybranym punkcie na segmencie między tym punktem a następnym.

- ***<Translate ios="true" ids="trim_before"/>***. Możesz przyciąć cały odcinek trasy, punkty i segmenty, od początku do wybranego punktu. Odległość do przycięcia jest wskazana pod nazwą opcji.

- ***<Translate ios="true" ids="trim_after"/>***. Możesz przyciąć trasę, punkty i segmenty, od ostatniego dodanego punktu do wybranego punktu. Odległość do przycięcia jest wskazana pod nazwą opcji.

- ***<Translate ios="true" ids="plan_route_split_before"/>***. Umożliwia podzielenie trasy przed wybranym punktem na oddzielne, niepołączone segmenty.

- ***<Translate ios="true" ids="plan_route_split_after"/>***. Umożliwia podzielenie trasy po wybranym punkcie na oddzielne, niepołączone segmenty.

- ***<Translate ios="true" ids="join_segments"/>***. Ostatni punkt na jednym z podzielonych segmentów i następny na liście punktów na drugim segmencie mają to ustawienie połączenia.

- ***<Translate ios="true" ids="change_route_type_before"/>***. Możesz zmienić typ routingu skonfigurowany dla dostępnego profilu, między punktami na poprzednim segmencie lub dla wszystkich segmentów od początku trasy do wybranego punktu.

- ***<Translate ios="true" ids="change_route_type_after"/>***. Możesz zmienić typ routingu między punktami na następnym segmencie lub dla wszystkich segmentów od wybranego punktu do ostatniego dodanego punktu.

- ***<Translate ios="true" ids="delete_point"/>***. Usuń wybrany punkt z trasy. Podobnie jak usuwanie punktu z listy.

### Trasy multimodalne {#multimodal-routes}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android-routeline](@site/static/img/plan-route/plan-route-routeline-android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route ios-screen](@site/static/img/plan-route/plan-route-routeline-ios.png)

</TabItem>

</Tabs>

Korzystając z narzędzia *Planowanie trasy* i opcji [Trasa między punktami](#route-between-points), możesz tworzyć trasy multimodalne, gdzie na przykład pierwsza część może być trasą *rowerową*, druga część trasą *prostą*, a następnie *pieszą*. Należy pamiętać, że nawigacja na trasach multimodalnych nie jest dostępna, więc musisz wybrać jeden z najbardziej odpowiednich profili, aby móc śledzić instrukcje krok po kroku.

## Edytor {#editor}

### Zapisz trasę {#save-route}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android](@site/static/img/plan-route/plan_route_save_changes_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route ios](@site/static/img/plan-route/plan_route_save_changes_ios.png)

</TabItem>

</Tabs>

Po [dodaniu](#adding-points) co najmniej jednego punktu do mapy, możesz użyć opcji zapisu. Wszystkie ślady zapisane w *Planowaniu trasy* można znaleźć w głównym *<Translate android="true" ids="shared_string_menu"/> → <Translate android="true" ids="shared_string_my_places"/> →* *[<Translate android="true" ids="show_gpx"/>](../personal/tracks/manage-tracks.md)*.

Istnieją cztery sposoby zapisu:

- ***Szybki zapis***. Przycisk ***Gotowe*** / ***Zapisz*** (dla istniejących śladów) w prawym górnym rogu umożliwia szybkie zapisanie zmian i wyjście z narzędzia *Planowanie trasy*. Nazwa jest generowana na podstawie bieżącej daty.
- ***Zapisz zmiany*** w [menu Opcje](#options) umożliwia zapisanie zmian w pliku i kontynuowanie planowania trasy.
- ***Zapisz jako nowy ślad*** w [menu Opcje](#options) otwiera okno dialogowe, w którym określasz nazwę śladu i folder, w którym trasa zostanie zapisana.
- ***Dodaj zmiany do śladu***. Dołącza utworzony ślad jako [oddzielny segment](#segments) do innego istniejącego śladu. Zmian w wybranym śladzie *nie można cofnąć*.

:::note Opcja uproszczonego śladu
Podczas zapisywania nowego śladu możesz wybrać opcję śladu ***Uproszczony***, aby ślad był zgodny z innymi aplikacjami innych firm. Technicznie, ślad zostanie zapisany bez instrukcji routingu jako czysto geometryczny ślad.
:::

### Opcje {#options}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android-options](@site/static/img/plan-route/plan_route_menu_options_3_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route ios-options](@site/static/img/plan-route/plan_route_menu_options_ios.png)

</TabItem>

</Tabs>

- [<Translate android="true" ids="route_between_points"/>](#route-between-points). Pokazuje wybrany profil aplikacji (domyślnie jest to linia prosta). Dotknięcie tej akcji jest równoznaczne z dotknięciem przycisku *Profil*, który otwiera [menu profili](../personal/profiles.md) aplikacji.
- **<Translate ios="true" ids="gpx_start_new_segment"/>** (*iOS*) lub **<Translate android="true" ids="plan_route_add_new_segment"/>** (*Android*). Rysuje nowe segmenty trasy, które nie łączą się z poprzednim segmentem.
- [<Translate android="true" ids="shared_string_save_changes"/>](#save-route). Jeśli jest to nowy ślad bez powiązania z istniejącym, otwiera się menu *Zapisz jako nowy ślad*. Po dodaniu nowych segmentów do otwartego lub zaimportowanego śladu pojawia się powiadomienie o zapisaniu pliku GPS w pamięci, po czym można kontynuować tworzenie następnego segmentu.
- [<Translate android="true" ids="save_as_new_track"/>](#save-route). Zapisuje trasę jako ślad GPX.
- [<Translate android="true" ids="add_to_a_track"/>](#save-route). Dodaje trasę do śladu z folderu śladów i zapisuje nowy ślad.
- [<Translate android="true" ids="shared_string_navigation"/>](../navigation/setup/gpx-navigation.md). Rozpoczyna nawigację z Twojej pozycji do punktu końcowego, korzystając z narysowanej trasy.
- **<Translate android="true" ids="reverse_route"/>**. Zamieniasz punkt *Startowy* trasy z ostatnio dodanym punktem. Ustawienia segmentów trasy nie zmieniają się po zastosowaniu Odwróć.
- [<Translate android="true" ids="attach_to_the_roads"/>](#attach-track-to-roads). Tworzy przybliżoną trasę. Każdy punkt na śladzie jest dopasowywany do najbliższej dozwolonej drogi na mapie zgodnie z wybranym profilem i odległością progową.
- [<Translate android="true" ids="shared_string_gps_filter"/>](../map/tracks/track-context-menu.md#gps-filter) (tylko Android). Możesz odfiltrować punkty trasy, które nie pasują do wybranego typu routingu, usunąć niepotrzebne dane lub skorygować niedokładne dane. Filtr GPS będzie działał tylko wtedy, gdy typ routingu jest określony jako *Linia prosta*. <!-- Android only(No!!!) with Straight line routing. **?How to use?** **When are additional details needed to calculate a route when switching to another type of routing?** -->
- [<Translate android="true" ids="get_altitude_data"/>](#get-elevation-data) (*tylko Android*). Ta opcja jest wyświetlana w menu tylko wtedy, gdy brak danych wysokościowych. Dzięki tej [opcji](#get-elevation-data) możesz obliczyć wysokość, korzystając z *danych mapy terenu* lub użyć danych z pobranych map, aby znaleźć *pobliskie drogi*.
- ***<Translate android="true" ids="shared_string_clear_all"/>***. Całkowicie archiwizuje wszystkie Twoje działania. Na mapie pozostaje "artefakt" - przerywane linie właśnie wyczyszczonej trasy. Znika przy następnym dodaniu nowych punktów. Możesz anulować funkcję Wyczyść wszystko za pomocą przycisku Cofnij akcję. Funkcja nie wpływa na niezmienione części tras otwartych w narzędziu.

### Wykres {#graph}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Plan a route android](@site/static/img/plan-route/plan_route_graph_5_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Plan a route snap-road-ios](@site/static/img/plan-route/plan_route-snap_ios.png)

</TabItem>

</Tabs>

Podczas planowania trasy [wykres](../navigation/setup/route-details.md#elevation-graph) wyświetla informacje o wysokości trasy i procentowym nachyleniu, a także możesz dotknąć dowolnego miejsca na wykresie, aby wyświetlić wskaźnik z konkretnymi danymi.

- Dla **Androida** wykres jest wyświetlany w zakładce *Wykres* podczas tworzenia lub otwierania śladu oraz podczas [Nawigacji](../navigation/setup/gpx-navigation.md) za pomocą *Planowania trasy*.
- Dla **iOS** wykres jest dostępny tylko poprzez menu *[Opcje](#options) → Nawigacja*.

Podczas obliczania trasy do nawigacji w *Planowaniu trasy* możesz znaleźć dodatkowe informacje o śladzie, takie jak [Informacje o wysokości](../navigation/setup/route-details.md#elevation-info) i [Atrybuty drogi](../navigation/setup/route-details.md#road-attributes), a także użyć narzędzia [Analizuj na mapie](../navigation/setup/route-details.md#analyse-on-map). Dotknij przycisku *Szczegóły* pod wykresem.

## Powiązane artykuły {#related-articles}

- [Pokaż ślad na mapie](../map/tracks/index.md)
- [Analizuj na mapie](../map/tracks/index.md#analyze-track-on-map)
- [Menu kontekstowe śladu](../map/tracks/track-context-menu.md)
- [Nawigacja po śladzie](../navigation/setup/gpx-navigation.md)
- [Nagrywanie podróży](../plugins/trip-recording.md)

> *Ostatnia aktualizacja: maj 2025*