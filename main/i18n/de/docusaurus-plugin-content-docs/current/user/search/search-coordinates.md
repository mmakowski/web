---
source-hash: bf99678e5242473057ed7799710f80ba10f57eb3f3795a53a0ac3600858d896c
sidebar_position: 6
title:  Koordinatensuche
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import AndroidStore from '@site/src/components/buttons/AndroidStore.mdx';
import AppleStore from '@site/src/components/buttons/AppleStore.mdx';
import LinksTelegram from '@site/src/components/_linksTelegram.mdx';
import LinksSocial from '@site/src/components/_linksSocialNetworks.mdx';
import Translate from '@site/src/components/Translate.js';
import InfoIncompleteArticle from '@site/src/components/_infoIncompleteArticle.mdx';



## Überblick {#overview}

**OsmAnd Koordinatensuche** ermöglicht es Ihnen, einen bestimmten Ort anhand von Breiten- und Längengrad zu finden. Diese Art der Suche hilft, einen Ort genau zu identifizieren. Sie ist besonders nützlich für Gebiete, die keine genauen Adressen haben, oder für spezifische geografische Aufgaben wie die Erstellung von Geofences oder die präzise Positionierung im Freiraum.

OsmAnd bietet mehrere Möglichkeiten, zum *Suchwerkzeug → [Adressen-Such-Tab](../search/search-address.md)* zu gelangen, wo sich die **Koordinatensuche** befindet.

- Die [Suchschaltfläche](../widgets/map-buttons.md#search) auf dem Kartenbildschirm der Anwendung.
- Gehen Sie zum Android-Haupt-*Menü → Suchen → Adressen-Tab → Koordinatensuche*.
- Wenn Sie eine Route vorbereiten, tippen Sie auf *Navigation → Ziel festlegen → Suchfeld → Adressen-Tab → Koordinatensuche*.


## Verwendung {#how-to-use}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Koordinatensuche Android](@site/static/img/search/coordinates_search_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Koordinatensuche iOS](@site/static/img/search/coordinates_search_ios.png)

</TabItem>

</Tabs>

Koordinaten können in jedem verfügbaren Format eingegeben werden, der gefundene Ort wird jedoch in dem Format angezeigt, das unter *Profil konfigurieren → Allgemeine Einstellungen → Einheiten & Formate* angegeben ist.

- Um die Koordinatensuche zu verwenden, können Sie diese einzeln in jedes entsprechende Feld eingeben oder zuvor kopierte Koordinaten in das Suchfeld einfügen oder darin eingeben. Die Anwendung fordert Sie auf, einen geeigneten Ort auszuwählen.
- Die Koordinatensuche konvertiert automatisch ein Koordinatenformat in ein anderes, wenn das angegebene Format im Feld mit der Liste geändert wird.
- Tippen Sie auf den vorgeschlagenen Ort, und das [Kartenkontextmenü](../map/map-context-menu.md#select-any-point-long-tap) wird geöffnet.
- Weitere Informationen finden Sie hier: [Geographische Koordinaten](https://en.wikipedia.org/wiki/Geographic_coordinate_system).


**Umfang der Koordinatensuchfunktion**:

- *Präziser Ort*. Die Koordinatensuche liefert einen genauen Ort. Sie können präzise Koordinaten eingeben, die Sie beispielsweise aus anderen Quellen wie einer Karte, einem GPS-Gerät oder Online-Diensten erhalten haben.
- *Orte ohne Adresse*. Koordinaten sind besonders nützlich, wenn es um Orte geht, die keine genaue Adresse haben, oder wenn die Adresse unbekannt ist. Zum Beispiel kann es sich um ein abgelegenes Gebiet, einen Punkt auf See oder einen Berggipfel handeln. Durch die Eingabe von Koordinaten können Sie solche Orte finden und dorthin navigieren, ohne die Adresse kennen zu müssen.
- *Standortfreigabe*. Die Suche nach Koordinaten bietet eine bequeme Möglichkeit, Informationen einzugeben. Sie können Koordinaten manuell eingeben oder aus anderen Quellen kopieren. Dies kann nützlich sein, wenn Sie Standorte mit anderen teilen oder zuvor erhaltene Koordinaten verwenden.


## Koordinatenformat {#coordinate-format}

Es gibt mehrere Möglichkeiten, Koordinaten für die Suche einzugeben. Um jede davon zu verwenden, ist es sehr wichtig, die Eingaberegeln zu befolgen, da die Anwendung sonst den Ort nicht finden kann.

1. **<Translate android="true" ids="navigate_point_format_D"/>**

    ![Koordinatensuche Android](@site/static/img/search/coordinates_search_degrees_andr.png)

    **Dezimalkoordinaten (Grad)**. In diesem Format werden Breiten- und Längengradkoordinaten im Dezimalformat geschrieben, z. B. 52,37022° Breite und 4,89517° Länge für Amsterdam. Diese Eingabemethode ist einfach zu verwenden und am gebräuchlichsten. Mehr über das Dezimalkoordinatenformat können Sie [hier](https://en.wikipedia.org/wiki/Decimal_degrees) lesen.

    - *Eingaberegeln*. Breiten- und Längengradkoordinaten werden im Dezimalformat geschrieben, wobei die Breite von -90 bis 90 und die Länge von -180 bis 180 reicht.
    - *Am häufigsten verwendet*. Dezimalkoordinaten werden häufig in Navigationsanwendungen, GPS-Geräten, Webkarten und anderen Geopositionierungsdiensten verwendet.

2. **<Translate android="true" ids="navigate_point_format_DM"/>**

    ![Koordinatensuche Android](@site/static/img/search/coordinates_search_DM_andr.png)

    **Grad und Minuten (DM)**. In diesem Format werden Breiten- und Längengradkoordinaten mit Grad und Minuten aufgezeichnet. Zum Beispiel 37:46.29 Breite und -122:25.10 Länge für San Francisco. Dieses Format kann weniger genau sein und länger dauern, um eingegeben zu werden.
    - *Eingaberegeln*. Breiten- und Längengradkoordinaten werden in einem Format geschrieben, das Grad (:) und Minuten (:) verwendet.
    - *Am häufigsten verwendet*. Das DM-Format findet sich häufig in der Seenavigation, Luftfahrt, Astronomie und topographischen Kartierungssystemen.

3. **<Translate android="true" ids="navigate_point_format_DMS"/>**

    ![Koordinatensuche Android](@site/static/img/search/coordinates_search_DMS_andr.png)

    **Grad, Minuten und Sekunden (DMS)**. Das DMS-Koordinatenformat zeichnet geografische Koordinaten auf, bei denen die Werte in Grad, Minuten und Sekunden angegeben sind. Grad (DDD) können Werte von 0 bis 180 für die Länge und 0 bis 90 für die Breite annehmen. Positive Werte geben Ostlänge und Nordbreite an, negative Werte Westlänge und Südbreite. Minuten (MM) können Werte von 0 bis 59 annehmen. Sekunden (SS.S) stellen den Dezimalbruch einer Sekunde dar und können ebenfalls von 0 bis 59,9 reichen.
    - *Eingaberegeln*. Breiten- und Längengradkoordinaten werden in einem Format geschrieben, das Grad (:), Minuten (:) und Sekunden (.) verwendet.
    - *Am häufigsten verwendet*. Das DMS-Format wird häufig in der Geodäsie, Navigationsanwendungen, Kartografie, Astronomie und anderen Bereichen verwendet, in denen eine detailliertere Darstellung von Standortkoordinaten erforderlich ist.

4. **<Translate android="true" ids="navigate_point_format_utm"/>**

    ![Koordinatensuche Android](@site/static/img/search/coordinates_search_UTM_andr.png)

    **UTM (Universales Transversales Mercator-System)**. In diesem Format werden Koordinaten unter Verwendung der UTM-Zone sowie der Ost- und Nordrichtung angegeben. Für Amsterdam könnten die Koordinaten beispielsweise ungefähr wie folgt lauten: Zone 31, Ostrichtung 581000, Nordrichtung 5809000. Die Eingabe von Koordinaten im UTM-Format erfordert möglicherweise eine gewisse Vertrautheit mit dem System und ist möglicherweise komplexer als andere Formate, bietet jedoch eine gute Genauigkeit und erfüllt globale Geopositionierungsstandards. Mehr über das UTM-Format können Sie [hier](https://en.wikipedia.org/wiki/Universal_Transverse_Mercator_coordinate_system) lesen.
    - *Eingaberegeln*. Koordinaten werden in einem Format aufgezeichnet, das die UTM-Zone sowie Ost- und Nordversätze verwendet.
    - *Am häufigsten verwendet*. Das UTM-Format wird häufig in der Vermessung, Kartierung und geographischen Informationssystemen zur Messung und Navigation verwendet.

5. **<Translate android="true" ids="navigate_point_format_olc"/>** ((OLC) - 9F2X4WFJ+7W (Open Location Code repräsentiert Fläche 9m x 14m))

    ![Koordinatensuche Android](@site/static/img/search/coordinates_search_OLC_andr.png)

    **Open Location Code (OLC)**, auch bekannt als **Plus Code**, ist ein globales Standortkodierungssystem. Es ist eine Kombination aus Buchstaben und Zahlen, um den Breiten- und Längengrad jedes Ortes auf dem Planeten anzugeben. Beispiel für einen OLC-Code für Amsterdam: 9F3WCVWG+FP. In diesem Beispiel gibt "9F3WCVWG" ein grobes Raster an, und "+FP" gibt einen Ort innerhalb dieses Bereichs an. Lesen Sie mehr [hier](https://en.wikipedia.org/wiki/Open_Location_Code).
    - *Eingaberegeln*.
        - Der OLC-Code besteht aus 4 bis 14 Zeichen, bei denen es sich um Buchstaben von "C" bis "Z" (mit Ausnahme von "I" und "O") und Zahlen von "2" bis "9" handeln kann.
        - Der Code beginnt mit einem globalen Präfix, das einen Kontinent oder ein Gebiet angibt.
        - Es folgen Gruppen von Zeichen, die durch Punkte getrennt sind. Jede Gruppe repräsentiert einen engeren Bereich.
        - Zur Klärung des Standorts werden Buchstaben und Ziffern im OLC-Code durch weitere Zeichen ergänzt.
    - *Am häufigsten verwendet*. OLC wird häufig in Gebieten verwendet, in denen keine präzisen Adressen verfügbar oder schwer zu ermitteln sind, wie z. B. in abgelegenen Gebieten, Wüsten oder Ozeanen. Es wird auch häufig in Anwendungen und Diensten im Zusammenhang mit Geopositionierung, Zustellung, Notdiensten und anderen Bereichen verwendet, in denen eine präzise Standortbestimmung ohne die Verwendung traditioneller Adressen erforderlich ist.

6. **<Translate android="true" ids="navigate_point_mgrs"/>**

    ![Koordinatensuche Android](@site/static/img/search/coordinates_search_MGRS_andr.png)

    **MGRS (Military Grid Reference System)**. Dies ist ein Koordinatensystem, das häufig in militärischen Anwendungen verwendet wird. Es basiert auf dem UTM-System und wird durch ein zusätzliches Raster von Quadraten ergänzt. Ein Beispiel für Koordinaten im MGRS-Format für einen Ort in Australien könnte wie folgt lauten: 55HBE1234567890. In diesem Beispiel steht "55H" für die MGRS-Zone und "BE" für das Quadrat, in dem sich der Ort befindet. "123456" steht für den Ostversatz und "7890" für den Nordversatz innerhalb dieses Quadrats. MGRS werden häufig in Bereichen verwendet, die eine hohe Genauigkeit und Georeferenzierung erfordern. Sie sind besonders nützlich in Umgebungen, in denen Adressen möglicherweise nicht klar oder verfügbar sind, wie z. B. bei militärischen Operationen oder Expeditionen in abgelegenen Gebieten. Mehr über das MGRS-Format können Sie [hier](https://en.wikipedia.org/wiki/Military_Grid_Reference_System) lesen.
    - *Eingaberegeln*. Die Koordinaten bestehen aus einer MGRS-Zone, einem Quadrat und zwei weiteren Ziffern, die Ost- und Nordversätze angeben.
    - *Am häufigsten verwendet*. Das MGRS-Format wird häufig in der militärischen Navigation und Kommunikation verwendet und kann auch für Outdoor-Enthusiasten und Wanderer nützlich sein.

7. **Schweizer Gitter** (CH1903) und **Schweizer Gitter** (CH1903+)

    ![Koordinatensuche Android](@site/static/img/search/coordinates_search_Swiss_andr.png)

    **Schweizer Koordinatensystem**. Schweizer Gitter (CH1903) und Schweizer Gitter (CH1903+) sind Koordinatensysteme, die in der Schweiz zur Positionierung weit verbreitet sind. Beide Formate basieren auf dem CH1903-System, das 1903 eingeführt wurde und auf der Projektion des Schweizer Internationalen Gitters basiert. Beispielkoordinaten im Schweizer Gitter (CH1903)-Format — Ost: 600000; Nord: 200000. Im Schweizer Gitter (CH1903+)-Format — Ost: 600300; Nord: 200400. Mehr über das geografische Koordinatensystem Schweizer Gitter können Sie [hier](https://en.wikipedia.org/wiki/Swiss_coordinate_system) lesen.
    - *Eingaberegeln*.
        - Koordinaten im CH1903-Format bestehen aus zwei Komponenten: Ost und Nord.
        - Ost ist in Metern von einem Punkt namens Luzerner Achse (null Ost) angegeben.
        - Nord ist in Metern vom Äquator angegeben.
        - Das CH1903+-Format verwendet die gleichen Eingaberegeln wie CH1903, jedoch mit präziseren Werten.
        - CH1903+ enthält Korrekturen, um Verschiebungen in den Koordinaten zu berücksichtigen, die durch tektonische Bewegungen in der Schweiz verursacht werden.
    - *Am häufigsten verwendet*. Die Formate Schweizer Gitter (CH1903) und Schweizer Gitter (CH1903+) werden in der Schweiz für geodätische Messungen, Kartographie, geographische Informationssysteme sowie im Bau- und Ingenieurwesen verwendet. Diese Formate bieten ein lokales Koordinatensystem, das spezifisch für die Schweiz ist.


> Für jedes Profil kann separat ein anderes Koordinatenformat eingestellt werden. Gehen Sie dazu zu *Allgemeine Einstellungen → [Koordinatenformat](../personal/profiles.md#units--formats)*.


<!--

## Troubleshooting {#troubleshooting}

https://github.com/osmandapp/OsmAnd/issues/14081

https://github.com/osmandapp/OsmAnd/issues/16114

https://github.com/osmandapp/OsmAnd/issues/14081

-->


## Verwandte Artikel {#related-articles}

- [Alles suchen](./search-all.md)
- [Adresse suchen](./search-address.md)
- [Suchverlauf](./search-history.md)
- [POI suchen](./search-poi.md)


> *Zuletzt aktualisiert: Juli 2024*