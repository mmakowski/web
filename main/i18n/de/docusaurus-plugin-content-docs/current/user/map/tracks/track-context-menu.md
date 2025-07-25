---
source-hash: 8897fb3aebb172bbef2674a2dea9f5e516873f9949d5d72db7b3e2032bea15b3
sidebar_position: 4
title:  Track-Kontextmenü
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import AndroidStore from '@site/src/components/buttons/AndroidStore.mdx';
import AppleStore from '@site/src/components/buttons/AppleStore.mdx';
import LinksTelegram from '@site/src/components/_linksTelegram.mdx';
import LinksSocial from '@site/src/components/_linksSocialNetworks.mdx';
import Translate from '@site/src/components/Translate.js';
import InfoIncompleteArticle from '@site/src/components/_infoIncompleteArticle.mdx';
import ProFeature from '@site/src/components/buttons/ProFeature.mdx';
import InfoAndroidOnly from '@site/src/components/_infoAndroidOnly.mdx';




## Überblick {#overview}

Das *Track-Kontextmenü* bietet Informationen über den *[Track](../../personal/tracks/index.md)* sowohl in Text- als auch in [grafischer](#altitude--speed-graphs) Form. Es ermöglicht Ihnen, Informationen hinzuzufügen, Änderungen vorzunehmen, zu bearbeiten und verschiedene andere Aktionen mit dem Track durchzuführen. Sie können das *Track-Kontextmenü* aufrufen, indem Sie einfach den gewünschten Track auf der Karte antippen oder das Menü *[Meine Orte](../../personal/myplaces.md)* (*<Translate android="true" ids="shared_string_menu,shared_string_my_places,shared_string_gpx_files"/>*) verwenden. Möglicherweise müssen Sie den Track-Ordner öffnen und den gewünschten Track durch Antippen auswählen.

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Übersicht Track-Kontextmenü Android](@site/static/img/personal/tracks/track_context_overview_andr_1.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Übersicht Track-Kontextmenü iOS](@site/static/img/personal/tracks/track_context_overview_2_ios.png)

</TabItem>

</Tabs>


## Track-Übersicht {#track-overview}

Wenn Sie einen Track antippen, öffnet sich der erste Bildschirm des *Track-Kontextmenüs* - der Reiter *Übersicht*. Auf diesem Reiter finden Sie eine Zusammenfassung des ausgewählten Tracks (*[Infopanel](#info-panel)*) und können die gängigsten Aktionen mit dem Track über das *[Track-Aktionsmenü](#track-actions)* ausführen. Sie können [Beschreibung und Serviceinformationen](#description-and-info) zu Ihrem Track sehen, wenn Sie den Reiter "Übersicht" nach oben ziehen.

<!--
You can [short tap](../../map/map-context-menu.md#select-route-short-tap-for-android) on the track on the map → <Translate android="true" ids="shared_string_overview"/> → click to "eye" button for not showing the track on the map.
-->

### Infopanel {#info-panel}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Infopanel Übersicht Android](@site/static/img/personal/tracks/track_context_info_panel_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Infopanel Übersicht iOS](@site/static/img/personal/tracks/track_context_info_panel_ios.png)

</TabItem>

</Tabs>

Oben im Informationsfeld sehen Sie den Namen des Tracks und das Symbol, das zu seiner Kennzeichnung verwendet wird (*nur Android*). Der Trackname kann über die Umbenennungsfunktion im [Optionsmenü](#options) geändert werden. Einige Tracks (meist die *[Reiseführer](../../plan-route/travel-guides.md#manage-as-gpx-track)*) können eine kurze *[Beschreibung](#description-and-info)* und (oder) ein Bild unter dem *Tracknamen* haben. Ein Pfeil zeigt die *Richtung zum nächsten Punkt des Tracks* von [Mein Standort](../../map/interact-with-map#my-location-and-zoom) an.

Das Infopanel bietet auch Informationen zu Folgendem:

- *<Translate android="true" ids="distance"/>*. Zeigt die Tracklänge an.
- *<Translate android="true" ids="altitude_ascent"/>* / *<Translate android="true" ids="altitude_descent"/>*. Zeigt die Gesamtsumme der Auf- und Abstiege während der Tour an.
- *<Translate android="true" ids="altitude_range"/>*. Zeigt die minimale und maximale Höhe auf einem Track an.

:::note
Falls Ihr Track in OsmAnd oder einer anderen Tracking-App erstellt wurde (sodass seine Punkte [`time` und `speed`](../../plugins/trip-recording#recorded-gpx-file)-Tags haben), enthält das Informationspanel auch Informationen über *<Translate android="true" ids="average_speed"/>*, *<Translate android="true" ids="max_speed"/>*, *<Translate android="true" ids="shared_string_time_span"/>* (*Android*) oder *<Translate ios="true" ids="total_time"/>* (*iOS*) (die Zeitspanne zwischen Start- und Endpunkt des Tracks), *<Translate android="true" ids="shared_string_time_moving"/>* (die Summe der Fahrzeit).
:::

### Track-Aktionen {#track-actions}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Track-Kontextmenü Übersicht Android 3](@site/static/img/personal/tracks/track_context_actions_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Track-Kontextmenü Übersicht iOS 3](@site/static/img/personal/tracks/track_context_actions_ios.png)

</TabItem>

</Tabs>

- **Anzeigen / Ausblenden** Schaltflächen. Ändert die Sichtbarkeit des Tracks auf der Karte.
- [Erscheinungsbild](./appearance.md). Passen Sie das Erscheinungsbild Ihres Tracks an.
- **Track bearbeiten** (*Android*). Öffnet den Track im [Routenplaner-Tool](../../plan-route/create-route.md).
- **Exportieren** (*iOS*). Ermöglicht Ihnen den [Export eines Tracks](../../personal/tracks/manage-tracks.md#export).
- **Wegbeschreibung**. Öffnet den Track im Modus *[Navigation](../../navigation/setup/gpx-navigation.md#start-gpx-navigation)*.


### Optionen {#options}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Track-Menü Optionen Android](@site/static/img/personal/tracks/track_menu_options_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Track-Menü Optionen Android](@site/static/img/personal/tracks/track_menu_options_ios.png)

</TabItem>

</Tabs>

Das Menü **Optionen** ermöglicht Ihnen die Verwaltung und Änderung des ausgewählten Tracks mit verschiedenen Tools und Einstellungen.

- **<Translate android="true" ids="shared_string_show_on_map"/>** – Steuert die Sichtbarkeit des Tracks auf der Karte.
- **<Translate android="true" ids="shared_string_appearance"/>** – Öffnet das Menü [Erscheinungsbild](../tracks/appearance.md), um Farbe, Breite und Transparenz des Tracks anzupassen.
- **<Translate android="true" ids="follow_track"/>** (*Android*) / **<Translate ios="true" ids="shared_string_navigation"/>** (*iOS*) – Startet die [Navigation nach Track](../../navigation/setup/gpx-navigation.md) und richtet Ihre Route am ausgewählten Track aus.

<br/>

- **<Translate android="true" ids="join_segments"/>** (*nur Android*) – Fügt Tracksegmente zusammen, um Lücken zu füllen.
- **<Translate android="true" ids="analyze_on_map"/>**. Öffnet das Tool [Auf Karte analysieren](../tracks/index.md#analyze-track-on-map-analyze-track-on-map), um Höhe, Geschwindigkeit und Distanz des Tracks zu überprüfen.
- **<Translate android="true" ids="analyze_by_intervals"/>** (*nur Android*) - Analysiert den Track nach Zeit- oder Distanz-[Intervallen](./track-context-menu.md#split-interval).

<br/>

- **<Translate android="true" ids="shared_string_share"/>** – Exportiert den ausgewählten Track im GPX-Format.
- **<Translate android="true" ids="upload_to_openstreetmap"/>** - [Lädt](../../plugins/osm-editing.md#upload-gps-track) den ausgewählten Track zu OpenStreetMap hoch.

<br/>

- **<Translate android="true" ids="edit_track"/>** - Öffnet das Tool [Route planen](../../plan-route/create-route.md) zum Bearbeiten des Tracks.
- **Track duplizieren** (*nur iOS*) – Erstellt und speichert eine Kopie des Tracks.
- **<Translate android="true" ids="rename_track"/>** – Ermöglicht das Ändern des Tracknamens.
- **<Translate android="true" ids="change_folder"/>** – Verschiebt den Track in einen anderen Ordner oder erstellt einen neuen.

<br/>

- **<Translate android="true" ids="shared_string_gps_filter"/>** (*nur Android*) - Ermöglicht das [Filtern von Trackpunkten](#gps-filter), um die Genauigkeit zu verbessern.
- **<Translate android="true" ids="altitude_correction"/>** (*nur Android*) - Um [Höhendaten zu erhalten](#calculate-missing-elevation), [hängen Sie Ihren Track an Straßen an](../../navigation/setup/gpx-navigation.md#attach-to-the-roads) oder berechnen Sie ihn offline (benötigt [Geländekarten](../../plugins/topography.md#download-maps)).
- **<Translate android="true" ids="simulate_your_location"/>** (*nur Android*) - [Simuliert Ihre Position](../../plugins/development.md#gpx-track-simulation) anhand eines GPX-Tracks.

<br/>

- **<Translate android="true" ids="shared_string_delete"/>**. Löscht den Track.


### Beschreibung und Info {#description-and-info}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Beschreibung und Info Android](@site/static/img/personal/tracks/track_context_overview_1_andr.png) ![Beschreibung und Info Android](@site/static/img/personal/tracks/track_context_overview_2_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Beschreibung eines Tracks iOS](@site/static/img/personal/tracks/track_context_overview_ios_4-1.png)

</TabItem>

</Tabs>

Dieser Abschnitt des Reiters *Übersicht* zeigt ***Tag-Daten*** und ***alle allgemeinen Informationen*** an.

- **Beschreibung**. Die Schaltfläche *<Translate android="true" ids="shared_string_edit"/>* (*Android*) / *<Translate ios="true" ids="context_menu_edit_descr"/>* (*iOS*) wird zum Bearbeiten der Trackbeschreibung verwendet. Tag `desc`.

- **Allgemein**. Enthält Informationen über die *GPX-Dateigröße*, den *Dateipfad* und das *Erstellungsdatum* mit dem `time`-Tag.

- **Info**. Tags: *Schlüsselwörter* - `keywords`, &nbsp;*Link* - `link`, &nbsp;*Aktivität* - `activities`.

- **Autor**. Tags: *Autor* - `author`, &nbsp;*Name* - `name`, &nbsp;*E-Mail-Adresse* - `email`, &nbsp;*Link* - `link`.

- **Urheberrecht**. Tags: *Urheberrecht* - `copyright`, &nbsp;*Autor* - `author`, &nbsp;*Jahr* - `year`, &nbsp;*Lizenz* - `license`.

- **Zusätzlich**. Alle Tags aus dem Abschnitt ***Erweiterungen***:&nbsp; `address`,&nbsp; `icon`,&nbsp; `background`,&nbsp; `color`,&nbsp; `country`,&nbsp; `state`,&nbsp; `telephone`,&nbsp; `postcode`,&nbsp; `start_date`,&nbsp; `desc`.


<details>

<summary>Beispiel XML-Code einer GPX-Datei</summary>

```xml
 <metadata>
    <name>GPX File Example</name>
    <desc>Example GPX file with various tags</desc>
    <author>
      <name>Author Name</name>
      <email id="your" domain="email.com" />
      <link href="https://yourwebsite.com" />
    </author>
    <copyright author="OsmAnd B.V">
      <year>2023</year>
      <license>https://github.com/osmandapp/OsmAnd/blob/master/LICENSE</license>
    </copyright>
    <link href="http://docs.osmand.net" />
    <time>2023-12-13T12:00:00Z</time>
    <keywords>gpx, osmand, hiking</keywords>
    <extensions>
      <osmand:address>Floyd Avenue (The Fan) 907, Richmond</osmand:address>
      <osmand:icon>place_town</osmand:icon>
      <osmand:background>circle</osmand:background>
      <osmand:color>#ff4e4eff</osmand:color>
      <osmand:country>United States</osmand:country>
      <osmand:state>Virginia</osmand:state>
      <osmand:telephone>(804) 828-0100</osmand:telephone>
      <osmand:postcode>23284</osmand:postcode>
      <osmand:start_date>Thursday, June 8, 2023</osmand:start_date>
      <osmand:desc>Boardwalks are walkways that cross over water or marshy ground. They are typically made of wood or other smooth materials and are accessible to wheelchairs. Please check with your park to see if there are accessible trails available. Boardwalks are often near parking lots, so expect large crowds.</osmand:desc>
    </extensions>
  </metadata>

```

</details>


### Track-Informationsaktivität {#track-information-activity}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Track-Informationsaktivität](@site/static/img/personal/tracks/track_info_activity_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Track-Informationsaktivität](@site/static/img/personal/tracks/track_info_activity_ios.png)

</TabItem>

</Tabs>


Die Funktion *Aktivität* in OsmAnd ermöglicht es Ihnen, aufgezeichnete GPX-Tracks mit spezifischen Aktivitäten zu versehen, um sie später zu analysieren und in Ordnern zu organisieren.

- [Aktivitäts-Tags für GPX-Tracks](../../plugins/trip-recording.md#recording-settings). Beim Aufzeichnen eines GPX-Tracks können Sie einen Aktivitätstyp zuweisen. Diese Aktivitätskennzeichnung hilft Ihnen, Tracks initial zu kategorisieren.
- [Aktivitätsfilter](../../personal/tracks/smart-folder.md#search-filter). Sie können die aufgezeichneten GPX-Tracks nach Aktivität filtern, wodurch Sie sich auf das Finden spezifischer Aufnahmetypen konzentrieren können, wie z.B. alle Rad- oder Wandertracks.
- [Aktivitätstypen verwalten](../../personal/tracks/manage-tracks.md#selection-mode). Sie können den Aktivitätstyp für ausgewählte Ordner oder Tracks über den Auswahlmodus im Reiter "Tracks" des Menüs "Meine Orte" ändern.
- **Aktivitätsliste**. Die Aktivitätskategorien und -gruppen sind in den OsmAnd-Ressourcen definiert. Für Entwickler und Mitwirkende wird die Aktivitätsliste in einem strukturierten Format unter [activities.json](https://github.com/osmandapp/OsmAnd-resources/blob/master/poi/activities.json) gepflegt, das die verfügbaren Aktivitätsgruppen und -typen detailliert beschreibt.


## Höhen-/Geschwindigkeitsdiagramme {#altitude--speed-graphs}

Auf dem Reiter *<Translate android="true" ids="shared_string_gpx_track"/>* finden Sie Informationen zum Track in grafischer Form. Über den Schalter können Sie auswählen, welche Daten im Diagramm angezeigt werden sollen: separate Daten zur *[<Translate android="true" ids="altitude"/>](#altitude)*, zur *[Geschwindigkeit](#speed)* (diese Option ist nur für aufgezeichnete Tracks verfügbar) oder alles zusammen (*[<Translate android="true" ids="shared_string_overview"/>](#overview-information)*).

Interaktion mit dem Diagramm:

- ***Einen Punkt auf dem Diagramm platzieren***. Wenn Sie die Informationen an einem bestimmten Punkt eines Tracks sehen möchten, können Sie an einer beliebigen Stelle auf das Diagramm tippen, und ein Zeiger mit den Werten wird angezeigt. Gleichzeitig erscheint ein blauer Marker auf der Karte, der auf diesen Ort auf dem Track zeigt.
- ***Vergrößern/Verkleinern***. Sie können [Zwei-Finger-Bewegungen](../../map/interact-with-map.md#gestures) verwenden, um für eine detailliertere Ansicht zu vergrößern und zu verkleinern. Nach dem Vergrößern können Sie das Diagramm nach rechts und links verschieben, was einer Vorwärts- und Rückwärtsbewegung entlang der Route entspricht.
- ***Zusätzliche Informationen***. Die rechte Seite des Diagramms enthält Daten zur niedrigsten, höchsten und durchschnittlichen Höhe, Steigung und Geschwindigkeit. Am unteren Rand des Diagramms sehen Sie die Distanzmarkierungen.


### Übersichts-Informationen {#overview-information}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Kontext-Track-Menü Diagramme Android](@site/static/img/personal/tracks/track_menu_graph_1_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Kontext-Track-Menü Diagramme iOS](@site/static/img/personal/tracks/track_menu_graph_2_ios.png)

</TabItem>

</Tabs>

Auf dem Reiter **Übersicht** sehen Sie Parameter wie:

- *<Translate android="true" ids="distance"/>*. Die Summe der gesamten zurückgelegten Strecke auf dem Track oder die Länge des Tracks selbst.
- *<Translate android="true" ids="shared_string_time_span"/>*. Das Zeitintervall zwischen Start- und Endpunkt des Tracks.
- *<Translate android="true" ids="shared_string_start_time"/>* Die genaue Zeit, zu der die Aufzeichnung des Tracks beginnt.
- *<Translate android="true" ids="shared_string_end_time"/>*. Die Endzeit der Trackaufzeichnung.

Die aktiven **Schaltflächen** ermöglichen den Zugriff auf Aktionen wie:

- Die Schaltfläche **<Translate android="true" ids="analyze_on_map"/>** öffnet das Menü [Track analysieren](../tracks/index.md#analyze-track-on-map) für den Track.
- Die Schaltfläche **<Translate android="true" ids="shared_string_options"/>** öffnet ein Menü mit:

  - *Bearbeiten* öffnet den Track im [Routenplaner-Tool](../../plan-route/index.md).
  - *Löschen* ermöglicht das Entfernen des ausgewählten Trackelements.
  - *Intervall teilen* öffnet die Funktion [Intervall teilen](#split-interval) für den Track.


### Geschwindigkeit {#speed}

:::note Nur aufgezeichnete Tracks
Dieser Reiter ist nur bei aufgezeichneten Tracks sichtbar. Punkte auf diesem Tracktyp haben **[`speed`](../../plugins/trip-recording#recorded-gpx-file)**-Tags.
:::

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Track-Diagramm Geschwindigkeit Android](@site/static/img/personal/tracks/track_graph_speed_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Track-Diagramm Geschwindigkeit iOS](@site/static/img/personal/tracks/track_graph_speed_3_ios.png)

</TabItem>

</Tabs>

Das Diagramm **Geschwindigkeit** zeigt Metriken wie:

- *<Translate android="true" ids="average_speed"/>*. Zeigt die Durchschnittsgeschwindigkeit während der Fahrt an.
- *<Translate android="true" ids="max_speed"/>*. Zeigt die maximale Geschwindigkeit während der Fahrt an.
- *<Translate android="true" ids="moving_time"/>*. Zeigt die Gesamtzeit der reinen Bewegung während der Fahrt an.
- *<Translate android="true" ids="distance_moving"/>*. Zeigt die angepasste Distanz der Fahrt an.


### Höhe {#altitude}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Track-Diagramm Höhe Android](@site/static/img/personal/tracks/track_graph_altitude_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Track-Diagramm Höhe iOS](@site/static/img/personal/tracks/track_graph_altitude_2_ios.png)

</TabItem>

</Tabs>

Das Diagramm **Höhe** zeigt Metriken wie:

- *<Translate android="true" ids="average_altitude"/>*. Zeigt die durchschnittliche Höhe über dem Meeresspiegel auf der Route an.
- *<Translate android="true" ids="altitude_range"/>*. Die höchste und niedrigste auf der Route aufgezeichnete Höhe.
- *<Translate android="true" ids="altitude_ascent"/>*. Der kumulative Höhengewinn über dem Meeresspiegel entlang der Route.
- *<Translate android="true" ids="altitude_descent"/>*. Der kumulative Höhenverlust entlang der Route.

**Höhendaten abrufen.**
Wenn auf der Route *keine Höheninformationen* vorhanden sind, können Sie diese auf folgende Weisen hinzufügen:

- *Schaltfläche "Höhe berechnen" → [Nahegelegene Straßen verwenden](../../plan-route/create-route.md#get-elevation-data)*. Verwendet eine Offline-Karte, um nahegelegene Straßen und Höhendaten zu finden. Ermöglicht die Anpassung der Trackgeometrie.
- [Geländekarten verwenden](#calculate-missing-elevation). Verwendet Geländekarten, um Höhendaten zu erhalten. Die Trackgeometrie bleibt unverändert.


### Fehlende Höhe berechnen {#calculate-missing-elevation}

:::note OsmAnd Pro Abonnement
Die Offline-Höhenberechnungsfunktion ist nur für [**OsmAnd Pro Abonnenten**](../../purchases/android.md#pro-features) verfügbar <ProFeature />.
:::

<InfoAndroidOnly />

Diese Funktion ermöglicht es Ihnen, das Höhenprofil für GPX-Tracks offline für jedes Gelände zwischen 70 Grad nördlicher Breite und 70 Grad südlicher Breite zu berechnen, basierend auf [Geländekartendaten](../../plugins/topography.md#download-maps). *Geländekarten (3D) sollten zuvor heruntergeladen werden*.

1. Laden Sie [Geländekarten (3D)](../../plugins/topography.md#download-maps) für die gewünschte Region herunter.
2. Wenn der Track keine Höhendaten enthält, gehen Sie zum Track-Kontextmenü (*Track-Kontextmenü → <Translate android="true" ids="shared_string_gpx_track,altitude,calculate_altitude"/>*), wählen Sie *Geländekarten verwenden*, und nach der Berechnung erhalten Sie ein Track-Diagramm basierend auf den Geländedaten.

    ![Track-Diagramm Höhe Android](@site/static/img/personal/tracks/calculate_elevation_2.png) ![Track-Diagramm Höhe Android](@site/static/img/personal/tracks/calculate_elevation_10.png) <!--![Track-Diagramm Höhe Android](@site/static/img/personal/tracks/calculate_elevation_4.png) ![Track-Diagramm Höhe Android](@site/static/img/personal/tracks/calculate_elevation_3.png) -->

3. Wenn Sie eine Route mit dem [Routenplaner-Tool](../../plan-route/create-route.md#graph) über die Methode *Gerade Linie* erstellen und keine Höhendaten im Diagramm vorhanden sind, müssen Sie:
    - Auf *Höhendaten abrufen* tippen und dann *Geländekarten verwenden* auswählen.
    - Nach der Berechnung erhalten Sie das vollständige Höhen-/Steigungsdiagramm Ihrer Route basierend auf den Geländedaten.

  ![Track-Diagramm Höhe Android](@site/static/img/personal/tracks/calculate_elevation_9.png) ![Track-Diagramm Höhe Android](@site/static/img/personal/tracks/calculate_elevation_5.png)


## Punkte / Wegpunkte {#points--waypoints}

Wegpunkte sind eine der auf der Karte verfügbaren Punktarten. Im Allgemeinen können es Trackpunkte sein, die Teil von GPX-Dateien sind. Eine detaillierte Beschreibung finden Sie im Artikel [Punkte auf der Karte](../../map/point-layers-on-map.md).

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Kontext-Track-Menü Punkte Android](@site/static/img/personal/tracks/track_context_points_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Kontext-Track-Menü Punkte iOS](@site/static/img/personal/tracks/track_context_points_ios.png)

</TabItem>

</Tabs>

In diesem Reiter *Punkte*:

- [Trackpunktdaten anzeigen](#display-custom-gpx-tags) und Ihre Trackpunkte (Wegpunkte und Routenpunkte) ändern, [löschen und Wegpunkte](#points--waypoints) zu einem Track hinzufügen.
- [Gruppe (Ordner) von Punkten](#waypoint-groups) erstellen und ändern.


### Wegpunkt zu einem Track hinzufügen {#add-waypoint-to-a-track}

Wegpunkte können zum aktuell aufgezeichneten Track oder zu jedem Track aus der Liste [*Meine Orte → Tracks*](../../personal/tracks/manage-tracks.md) hinzugefügt werden:

- Verwenden Sie das [Karten-Kontextmenü](../../map/map-context-menu.md#-add--edit-track-waypoint--add--edit-track-waypoint).
  - Wegpunkte werden automatisch angezeigt, wenn der ausgewählte Track auf der Karte aktiviert ist.
  - [Langes Tippen](../../map/map-context-menu.md#select-any-point-long-tap) auf die Karte an einer beliebigen ausgewählten Stelle, um einen Wegpunkt zu erstellen.
  - Sie können Informationen über den Wegpunkt im geöffneten [Karten-Kontextmenü](../../map/map-context-menu.md#-add--edit-track-waypoint) festlegen.

- Verwenden Sie die Schaltfläche [Wegpunkt hinzufügen](#points--waypoints) im Track-Kontextmenü.

- Fügen Sie einen Wegpunkt als [Schnellaktionsschaltfläche](../../widgets/quick-action.md#my-places) hinzu.

#### Wegpunkt erstellen {#create-waypoint}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Wegpunkt hinzufügen](@site/static/img/personal/tracks/add_waypoint_1_andr.png) ![Wegpunkt hinzufügen](@site/static/img/personal/tracks/add_waypoint_2_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Wegpunkt hinzufügen](@site/static/img/personal/tracks/add-track-waypoint-ios-1.png) ![Wegpunkt hinzufügen](@site/static/img/personal/tracks/add_waypoints_2_ios.png)

</TabItem>

</Tabs>

Tippen Sie auf die Schaltfläche *Wegpunkt hinzufügen*, um den Bildschirm zur Wegpunkterstellung zu öffnen (dieser Bildschirm ist dem [Favoriten-Kontextmenü](../../personal/favorites.md#create) ähnlich).

1. **Fügen Sie** den *Namen* des Wegpunkts, die *Adresse* des ausgewählten Ortes und eine *Beschreibung* (optional) hinzu.
2. **Wählen Sie** eine Gruppe aus.

    - Wählen Sie zuvor erstellte Gruppenkategorien aus oder erstellen Sie eine neue.
    - Erstellen Sie einen Namen und ein Erscheinungsbild für die neue Wegpunktgruppe. Dies wird in der Anwendung auch als *neue Kategorie* bezeichnet.
    - Das **Symbol**, die **Symbolfarbe** und die **Form** werden für alle neuen Wegpunkte verwendet, die der Gruppe hinzugefügt werden.

3. **Erscheinungsbild**-Einstellung:

    - Wählen Sie ein [**Symbol**](../../personal/favorites.md#favorite-icons) aus der Liste aller POI-Kategoriesymbole.
    - Wählen Sie die **Farbe** des Symbols.
    - Wählen Sie dann die **Form** des Symbols: *Kreis, Achteck, Quadrat*.

4. **Ersetzen** Sie bei Bedarf einen anderen Punkt durch diesen.


### Aktionen mit Gruppen {#actions-with-groups}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Track-Menü Gruppenmenü Android](@site/static/img/personal/tracks/track_menu_group_menu_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Track-Menü Gruppenmenü iOS](@site/static/img/personal/tracks/track_menu_group_menu_ios.png)

</TabItem>

</Tabs>

Das *Drei-Punkte-Menü* ( &#8285; ) öffnet das Wegpunkt-*Gruppenmenü*.

**Aktionen:**

- **<Translate android="true" ids="shared_string_show_on_map"/>** - Ermöglicht das Anzeigen oder Ausblenden von Gruppen-Wegpunkten auf der Karte. Oder Sie können die [Bildschirm-Schaltfläche](#points--waypoints) verwenden, um Gruppen-Wegpunkte auf der Karte anzuzeigen oder auszublenden.
- **<Translate android="true" ids="shared_string_rename"/>** - Ändert den Namen der Gruppe.
- **<Translate android="true" ids="change_default_appearance"/>** - Ändert die Anzeigeoptionen für eine Gruppe von Wegpunkten.
- **<Translate android="true" ids="add_group_to_markers"/>** oder **Entfernen** (*nur Android*) - Verschiebt Gruppen-Wegpunkte in die Liste [Kartenmarkierungen](../../personal/markers.md).
- **<Translate android="true" ids="copy_to_map_favorites"/>** (*nur Android*) - Verschiebt Gruppen-Wegpunkte zu [Favoriten](../../personal/favorites.md).
- **<Translate android="true" ids="add_to_navigation"/>** (*nur Android*) - Erstellt eine Route zwischen Wegpunkten. Der erste und letzte Punkt werden zum Start und Ziel der Route, und die restlichen werden in Zwischenpunkte umgewandelt.
- **<Translate android="true" ids="shared_string_delete"/>** - Löscht eine Gruppe von Wegpunkten.


### Wegpunktgruppen {#waypoint-groups}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Track-Menü Gruppe Karte Android](@site/static/img/personal/tracks/waypoints_group_map_android.png) ![Track-Menü Gruppe Karte Android](@site/static/img/personal/tracks/waypoints_group_map_1_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Track-Menü Gruppe Karte iOS](@site/static/img/personal/tracks/waypoints_group_map_ios.png) ![Track-Menü Gruppe Karte iOS](@site/static/img/personal/tracks/waypoints_group_map_1_ios.png)

</TabItem>

</Tabs>

Verwalten Sie die Sichtbarkeit von Gruppen auf der Karte: Wenn Sie einen Track ausblenden, wird die gesamte Gruppe ebenfalls ausgeblendet.

Sie können Gruppen-Wegpunkte auf der Karte mit der Schaltfläche in der oberen rechten Ecke des Kontextmenüs des Tracks auf der Karte ein- oder ausschalten. Tippen Sie darauf und wählen Sie die gewünschte Aktion.

### Benutzerdefinierte GPX-Tags anzeigen {#display-custom-gpx-tags}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Punkte](@site/static/img/personal/tracks/waypoints_tag_info_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Punkte](@site/static/img/personal/tracks/waypoints_tag_info_ios.png)

</TabItem>

</Tabs>

<details>

<summary>Beispiel XML-Code von Wegpunkt-Tags</summary>

```xml
  <wpt lat="40.123456" lon="-73.987654">
    <ele>100</ele>
    <time>2024-04-04T13:12:11Z</time>
    <name>Waypoint 1</name>
    <desc>Long description</desc>
    <link href="http://docs.osmand.net" />
    <type></type>
    <cmt>Short comment for the waypoint.</cmt>
    <extensions>
      <osmand:country>United States</osmand:country>
      <osmand:address>Floyd Avenue (The Fan) 907, Richmond</osmand:address>
      <osmand:color>#ff4e4eff</osmand:color>
      <osmand:background>circle</osmand:background>
      <osmand:icon>place_town</osmand:icon>
      <osmand:postcode>23284</osmand:postcode>
      <osmand:telephone>(804) 828-0100</osmand:telephone>
      <osmand:state>Virginia</osmand:state>
      <osmand:start_date>Thursday, June 8, 2023</osmand:start_date>
    </extensions>
  </wpt>
```

</details>

<details>

<summary>Beispiel XML-Code von Routenpunkt-Tags</summary>

```xml
  <rte>
    <name>Route 1</name>
    <desc>A sample route</desc>
    <rtept lat="40.123456" lon="-73.987654">
      <ele>110</ele>
      <name>Route Point 1</name>
      <desc>Point 1 of the route</desc>
      <extensions>
        <osmand:country>United States</osmand:country>
        <osmand:address>Floyd Avenue (The Fan) 907, Richmond</osmand:address>
        <osmand:color>#ff4e4eff</osmand:color>
        <osmand:background>circle</osmand:background>
        <osmand:icon>place_town</osmand:icon>
        <osmand:postcode>23284</osmand:postcode>
        <osmand:telephone>(804) 828-0100</osmand:telephone>
        <osmand:state>Virginia</osmand:state>
        <osmand:start_date>Thursday, June 8, 2023</osmand:start_date>
      </extensions>
    </rtept>
  </rte>
```

</details>

**Tags:**

| Parameter | Beschreibung |
| --- | --- |
| `lat` | **Breitengrad** ist eine der geografischen Koordinaten, mit der Sie einen Standort bestimmen können. |
| `lon` | **Längengrad** ist eine weitere der geografischen Koordinaten, mit der Sie einen Standort bestimmen können. |
| `time` | **Zeitstempel** ist das Datum und die Uhrzeit, zu der der Punkt aufgezeichnet wurde. |
| `name` | **Name** ist der Name des Punktes. Alle Zeichen sind erlaubt. |
| `desc` | **Beschreibung** enthält zusätzliche Informationen über den Punkt. |
| `type` | **Gruppe auswählen** ist der Name des OsmAnd-Ordners, in dem dieser Wegpunkt gespeichert ist. |
| `cmt` | **Kommentar** ist ein kurzer Kommentar zu einem Punkt. |
| `link` | **Link** ist ein Link zu beliebigen Quellen. |
| `ele` | **Höhe** ist die Höhe eines Punktes. |


**Erweiterungen:**

| Erweiterung | Beschreibung |
| --- | --- |
| `osmand:icon` | **Symbol** ist der Name des von Ihnen ausgewählten Symbols. |
| `osmand:color` | **Farbe** ist die Farbe im HEX-Format. |
| `osmand:background` | **Hintergrund** ist die Form des Symbols, z.B. ein Kreis, Achteck oder Quadrat. |
| `osmand:country` | **Land** ist der Name des Landes. |
| `osmand:address` | **Adresse** ist die Adresse. |
| `osmand:postcode` | **Postleitzahl** ist die Postleitzahl. |
| `osmand:telephone` | **Telefon** ist die Telefonnummer. |
| `osmand:state` | **Bundesland** ist der Name des Bundeslandes. |
| `osmand:start_date` | **Startdatum** sind die Planungsdaten eines Punktes. |

Wegpunkte werden zusammen mit dem Track in der [GPX-Datei](../../../technical/osmand-file-formats/osmand-gpx.md) gespeichert. Jeder dieser Wegpunkte hat seinen eigenen Satz von Tags zur Beschreibung. Alle Tags, die direkt mit der Beschreibung von Wegpunkten zusammenhängen und direkt in der OsmAnd-Anwendung bearbeitet werden können, sind in diesem Abschnitt aufgeführt.
Um die Wegpunktbeschreibung zu ändern, können Sie einen der folgenden Wege gehen:

1. Suchen Sie den gewünschten Track in der Liste des Reiters *<Translate android="true" ids="shared_string_menu,shared_string_my_places,shared_string_gpx_files"/>*.
2. Tippen Sie auf den Track auf der Karte, wenn er in der [Liste der sichtbaren](../tracks/index.md#display-tracks-on-the-map) enthalten ist.
3. Tippen Sie auf den gewünschten Wegpunkt, wenn er auf der Karte [sichtbar](../../personal/tracks/manage-tracks.md#track-menu) ist.

    Dann tippen Sie im [Tracks-Kontextmenü](./track-context-menu.md) auf *Punkte*, das Feld des gewünschten Ordners mit verfügbaren Wegpunkten und den gesuchten Wegpunkt. Wählen Sie das Menü *Aktionen →* **GPX-Wegpunkt bearbeiten** und nehmen Sie Änderungen vor. Sie können das Erstellungsdatum eines Punktes, den *Zeitstempel*, in der Anwendung nicht ändern.

**Amenity-Tags**, die zusätzliche Informationen wie Öffnungszeiten oder Telefonnummern beschreiben, die spezifisch für den POI sind, übernehmen diese Informationen aus OpenStreetMap-Daten oder Daten, die Sie beim Erstellen des POI eingegeben haben. Sie können solche Tags und [benutzerdefinierte Tags](#display-custom-gpx-tags) nur im Code der GPX-Datei bearbeiten, die Sie mit jedem Texteditor auf Ihrem Gerät öffnen können.


## Intervall teilen {#split-interval}

<InfoAndroidOnly />

Sie können den Track in Intervalle unterteilen, z. B. nach Distanz und Zeit, und ihn analysieren.

Teilen Sie den Track nach Distanz oder Zeitintervall.
*<Translate android="true" ids="shared_string_options,analyze_by_intervals"/>*

![Track-Split-Intervall-Bildschirm Android](@site/static/img/personal/tracks/track_split_interval_android.png) ![Track-Split-Intervall-Bildschirm Zeit Android](@site/static/img/personal/tracks/track_split_interval_time_android.png)


## GPS-Filter {#gps-filter}

<InfoAndroidOnly />

*<Translate android="true" ids="shared_string_options,shared_string_gps_filter"/>*

![GPS-Filter-Bildschirm Android](@site/static/img/personal/tracks/gps_filter_android.png)

<!-- A user can filter points of a GPX track by Smoothing, Speed, Altitude, and Min GPS Precision for saving new track without excluded points. -->

Dieser Filter ermöglicht es Ihnen, Ihre Trackstatistiken zu verbessern, indem Sie unnötige oder falsche Daten ausschließen. Sie können Trackpunkte herausfiltern, die nicht zu Ihren Trackparametern passen, und erhalten so ein genaueres Diagramm und eine visuelle Routenlinie ohne Verzerrungen oder Aufzeichnungsrauschen. Sie können Änderungen mit Filtern wie *Glättung*, *Geschwindigkeit*, *Höhe* und *GPS-Genauigkeit* vornehmen, die gefilterte Punkte vom aktuellen Track ausblenden. Außerdem können Sie im Menü *Statistiken* überprüfen, wie Ihre Änderungen im Diagramm angezeigt werden, bevor Sie sie speichern. Sie können auch *Auf Original zurücksetzen* und *Als Kopie speichern* Ihres Tracks in diesem Filter, ohne den Originaltrack zu speichern.

<!-- In the screen you see the map (with [zoom buttons](../../map/interact-with-map.md#my-location-and-zoom), [my location button](../../map/interact-with-map.md#my-location-and-zoom), my track location button), buttons "Reset" and "&#8285;"(Actions), part with two menus: **Filter** and **Statistics**.

- "&#8285;"(Actions) button opens the "Actions" part of the "Filter" or "Statistics" menu.
- "&#8634;" button allows you to reset the track to the original.
- "My track location" button allows you to move the map to your track.-->

Die Android GPS-Filter-App-Seite enthält Folgendes:

- Eine Karte mit einem gespeicherten Track und einer zusätzlichen Schaltfläche, *Mein Track-Standort* (richtet einen Track an der Mitte einer Karte aus).
- Schaltflächen *Aktualisieren* und *Menü* oben (*Menü* öffnet das Feld *Aktion* am unteren Rand der Seite).
- Blöcke *Filter*, *Statistiken*, *Aktion*.


### Filtermenü {#filter-menu}

In diesem Menü können Sie einige Parameter Ihres Tracks wie *Glättung*, *Geschwindigkeit*, *Höhe* oder *GPS-Genauigkeit* mithilfe von Filtern ändern. Das Menü ist in einen *Punkte-Teil* und einen *Aktionen-Teil* unterteilt.

| ***Punkte*** |
|:------------|
|Dieser Teil zeigt die Anzahl der Punkte nach dem Filtern und die Gesamtzahl der Punkte auf dem ausgewählten Track vor der Anwendung der Filter an.|
|![GPS-Filter-Bildschirm Punkte-Nummern Android](@site/static/img/personal/tracks/gps_filter_points_numbers_android.png) |
| ***Aktionen*** |
|*Glättung*. Legt den Schwellenwert für den Abstand zwischen Punkten fest. Trackpunkte, die mindestens diesen Abstand vom letzten sichtbaren Punkt entfernt sind, werden ausgeblendet. Alle Punkte auf dem Track, deren Abstand voneinander geringer ist als der vom Filter ausgewählte Abstand, werden ausgeblendet. Trackpunkte werden vom letzten sichtbaren Punkt aus gezählt. Beachten Sie, dass hohe Schwellenwerte die Trackgeometrie zu stark vereinfachen können.|
|![GPS-Filter-Glättungsnummern Android](@site/static/img/personal/tracks/gps_filter_smoothing_android.png) |
|*Geschwindigkeit*. Nur die Trackpunkte, die dem ausgewählten Geschwindigkeitsintervall entsprechen, werden im Diagramm und auf der Karte angezeigt, die anderen werden ausgeblendet.|
|![GPS-Filter-Geschwindigkeitsnummern Android](@site/static/img/personal/tracks/gps_filter_speed_android.png) |
|*Höhe*. Nur die Trackpunkte, die dem ausgewählten Höhenintervall entsprechen, werden im Diagramm und auf der Karte angezeigt, die anderen werden ausgeblendet.|
|![GPS-Filter-Höhennummern Android](@site/static/img/personal/tracks/gps_filter_altitude_android.png) |
|*GPS-Genauigkeit*. Legt den maximal zulässigen Wert für HDOP fest. Punkte mit einem höheren Wert werden ausgeblendet.|
|![GPS-Filter-Präzisionsnummern Android](@site/static/img/personal/tracks/gps_filter_precision_android.png) |


### Statistiken {#statistics}

![GPS-Filter-Diagramm Android](@site/static/img/personal/tracks/gps_filter_graph_statistics_andr.png)

Der Reiter "Statistiken" zeigt Informationen zum **geänderten** Track an, d.h. zum Track ohne gefilterte Werte. Dies wird in den Statistikblöcken und Diagrammdaten angezeigt.

- Der Teil *Daten* zeigt Statistiken ähnlich dem [Filtermenü](#filter-menu).
- Der Teil *Diagramm* zeigt drei Arten von Diagrammen nach Parametern an: Übersicht, Höhe und Geschwindigkeit. Diese Funktionalität ist eine Kopie des [Track-Diagramms](#altitude--speed-graphs).

### Aktionen {#actions}

![GPS-Filter-Aktion Android](@site/static/img/personal/tracks/gps_filter_action_android.png)

Die Liste der Aktionen ist am unteren Rand des Reiters **Filter** oder **Statistiken** verfügbar. OsmAnd wendet alle am Track vorgenommenen Änderungen an, ohne die Datei zu aktualisieren, aber Sie können die Änderungen manuell speichern.

- *<Translate android="true" ids="reset_to_original"/>*. Ermöglicht das Zurücksetzen der Parameter auf ihren ursprünglichen Zustand.
- *<Translate android="true" ids="save_as_copy"/>*. Ermöglicht das Speichern des Tracks als neuen Track.
- *<Translate android="true" ids="save_changes_into_file"/>*. Ermöglicht das Überschreiben des Tracks mit den neuen Parametern.


## Verwandte Artikel {#related-articles}

- [GPX-Tracks](../../personal/tracks/manage-tracks.md)
- [Tracks auf der Karte](./track-context-menu.md)
- [Navigation nach Track](../../navigation/setup/gpx-navigation.md)
- [Route planen](../../plan-route/index.md)
- [Plugin "Reiseaufzeichnung"](../../plugins/trip-recording.md)
- [Auf Karte analysieren](../index.md#analyze-track-on-map)

> *Zuletzt aktualisiert: November 2024*