---
source-hash: c8d86e0d815539ea1395efc415de2d8d02dbf19117cd20b4d4915ea3473d7023
sidebar_position: 7
title:  Paramètres de navigation
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



## Aperçu {#overview}

Pour une navigation réussie, il est important de configurer correctement les paramètres appropriés en fonction de vos besoins et de votre mode de déplacement (en voiture, à pied, à cheval ou à ski). Cet article décrit les paramètres de base de l'itinéraire, les [invites vocales](#voice-prompts), les [alertes d'écran](#screen-alerts), le [comportement de la carte pendant la navigation](#map-during-navigation) et l'[apparence des lignes d'itinéraire](#customize-route-line). Il détaille également les paramètres du véhicule tels que la [vitesse par défaut](#default-speed) et la [vitesse maximale/minimale](#road-speeds), le [type de moteur](#fuel-used-by-motor) pour le calcul du CO2, la [capacité du réservoir de carburant](#fuel-tank-capacity) et la [taille/le poids](#size-parameters), qui peuvent affecter l'itinéraire. L'ajustement de ces paramètres vous aidera à tirer le meilleur parti d'OsmAnd et à atteindre votre objectif sans délai inutile.

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_overview_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Paramètres de navigation iOS](@site/static/img/navigation/navigation_settings_overview_ios.png)

</TabItem>

</Tabs>

### Comment ouvrir {#how-to-open}

Cette section présente les paramètres de navigation nécessaires au calcul et au traçage d'un itinéraire, que vous pouvez définir pour le profil sélectionné. Ce menu comprend les paramètres pour la [préparation de l'itinéraire](../setup/route-navigation.md), l'[écran de la carte pendant la navigation](../guidance/map-during-navigation.md), et ce que vous définissez dans les *paramètres de navigation* affecte directement l'affichage des données dans les [détails de l'itinéraire](../setup/route-details.md).

Il existe trois façons d'accéder au menu des paramètres de navigation.

- Allez dans le *Menu → Paramètres*, sélectionnez le *Profil* requis, et appuyez sur *Paramètres de navigation*.

- Appuyez sur l'icône *Navigation* sur l'écran de la carte, puis sélectionnez l'*icône Paramètres → Paramètres de navigation*.

- Allez dans le *<Translate android="true" ids="shared_string_menu,shared_string_navigation,shared_string_settings,routing_settings_2"/>* principal.

:::info
Le profil par défaut *Parcourir la carte* n'a pas de paramètres de navigation.
:::


## Type de navigation {#navigation-type}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_type_offline_andr.png) ![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_type_online_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Paramètres de navigation iOS](@site/static/img/navigation/navigation_settings_type_ios.png)

</TabItem>

</Tabs>

La navigation est une partie importante d'un voyage, et choisir *le bon type* de navigation peut rendre votre voyage beaucoup plus facile. Le type de navigation que vous choisissez peut dépendre de votre mode de déplacement et de votre connexion Internet.

- **Navigation en ligne**
Elle utilise principalement un système de routage spécial ou un site web qui permet à l'application OsmAnd de tracer un itinéraire basé sur les informations actuelles et d'autres facteurs. Vous pouvez en savoir plus sur le choix du meilleur itinéraire en ligne dans l'article [Routage en ligne](../routing/online-routing.md). Ce type de navigation n'est disponible que pour la *version Android* de l'application.

- **Navigation hors ligne**
Elle ne nécessite pas d'accès à Internet et offre une sélection plus large de [types de navigation](../routing/osmand-routing.md#routing-types) qui peuvent être utilisés pour calculer un itinéraire. Parmi eux, on trouve le *vélo, le bateau, la voiture, la marche, le ski* et la *ligne droite*. Il existe actuellement 13 types de routage de base, ainsi qu'un type de routage externe [BRouter](../routing/brouter.md) qui offre des possibilités de routage supplémentaires.

Le type de navigation détermine les règles utilisées pour calculer les itinéraires. Si vous avez besoin d'un type de navigation spécifique, vous pouvez **importer votre propre fichier de routage *XML* modifié**. Pour en savoir plus sur les règles de routage, consultez notre [page GitHub](https://github.com/osmandapp/OsmAnd-resources/blob/master/routing). Il existe également un article distinct sur le format XML et son utilisation, [Style de rendu de carte](../../../technical/osmand-file-formats/osmand-rendering-style.md), qui peut vous aider à créer un fichier d'itinéraire.


## Paramètres d'itinéraire {#route-parameters}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_route_parameters_1_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Paramètres de navigation iOS](@site/static/img/navigation/navigation_settings_route_parameters_1_ios.png)

</TabItem>

</Tabs>

Les **<Translate android="true" ids="route_parameters"/>** sont des paramètres qui déterminent comment l'application calculera un itinéraire pour atteindre une destination, en tenant compte de facteurs tels que le type de transport, les priorités de routage, les conditions d'itinéraire, la complexité de l'itinéraire et les préférences de l'utilisateur.

Pour chaque [profil](../../personal/global-settings.md#default-profile), à l'exception de *Parcourir la carte*, OsmAnd sélectionne par défaut le [type de navigation](#navigation-type) optimal et les [paramètres d'itinéraire](../routing/osmand-routing.md#routing-types) pertinents. Cependant, vous pouvez choisir n'importe quel type et modifier les paramètres en fonction de vos préférences et des conditions externes du voyage à venir.

Tous les paramètres d'itinéraire sont décrits en détail dans les sections correspondantes de la documentation :
*[Routage voiture (Camion, Moto)](../routing/car-based-routing.md), [Routage vélo (VTT)](../routing/bicycle-based-routing.md), [Routage mobylette](../routing/moped-routing.md), [Routage piéton](../routing/pedestrian-routing.md), [Routage transports en commun](../routing/public-transport-navigation.md), [Routage équestre](../routing/horse-routing.md), [Routage ski](../routing/ski-routing.md), [Routage train](../routing/train-routing.md), [Routage bateau](../routing/boat-navigation.md), [Routage point à point](../routing/direct-to-point-routing.md), [Routage ligne droite](../routing/straight-line-routing.md), [Routage en ligne](../routing/online-routing.md), [Routage BRouter](../routing/brouter.md)*.


### Recalculer l'itinéraire {#recalculate-route}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_route-recalculation1_andr.png)
![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_route-recalculation2_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Paramètres de navigation iOS](@site/static/img/navigation/navigation_settings_route-recalculation1_ios.png)
![Paramètres de navigation iOS](@site/static/img/navigation/navigation_settings_route-recalculation2_ios.png)

</TabItem>

</Tabs>

Le paramètre **Calcul d'itinéraire** modifie automatiquement l'itinéraire calculé lorsque vous vous en écartez ou que vous roulez dans la direction opposée. Dans les deux cas, ce paramètre vous aide à maintenir votre direction de voyage et à atteindre votre destination sans perdre de temps à chercher manuellement un nouvel itinéraire.

| Paramètre | Description | Remarque |
|:------------|:---------------|:---------------|
| *<Translate android="true" ids="route_recalculation_dist_title"/> en cas de déviation* | <Translate android="true" ids="recalculate_route_distance_promo"/> | Si les [invites vocales](../guidance/voice-navigation.md#voice-settings) sont activées, OsmAnd annonce que l'itinéraire est en cours de recalcul. |
| *Recalculer l'itinéraire en cas de direction inverse* | Votre itinéraire sera recalculé si vous vous déplacez vers le point de départ. | Avec ce paramètre désactivé, le mouvement vers le point de départ n'est pas considéré comme une déviation du chemin (tant qu'il suit l'itinéraire calculé). |


### Paramètres de développement {#development-settings}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Aller à : *Menu → Paramètres → profil de l'application → Paramètres de navigation → Paramètres d'itinéraire → Développement*

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_development_1_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Aller à : *Menu → Paramètres → profil de l'application → Paramètres de navigation → Paramètres d'itinéraire → Développement*

![Paramètres de navigation iOS](@site/static/img/navigation/navigation_settings_development_1_ios.png)

</TabItem>

</Tabs>

Les paramètres de la section **Développement** sont principalement destinés aux utilisateurs avancés et ne sont disponibles que lorsque le [plugin de développement OsmAnd](../../plugins/development.md) est activé.

| Paramètre | Description |
|:------------|:---------------|
| *Type de routage* (*Android*) / *Algorithme de routage* (*iOS*) | <ul><li>**A*** 2 phases (*Android*) / **A*** (*iOS*) ajoute une phase supplémentaire à l'algorithme par défaut pour améliorer la qualité de l'itinéraire calculé. Cette option peut être utile pour trouver des itinéraires dans des réseaux routiers vastes et complexes, mais le calcul de l'itinéraire peut prendre plus de temps.</li><li>**A* classique** (*Android*) / **Hiérarchies routières** (*iOS*) optimise la planification d'itinéraire en privilégiant les routes principales et les autoroutes, minimisant le nombre de virages et de jonctions sur l'itinéraire. Particulièrement efficace sur de longues distances.</li><li>**HH (Hiérarchies routières) x Java** (*Android uniquement*) est basé sur l'implémentation de structures de données hiérarchiques pour optimiser la recherche de chemin sur une carte, en tenant compte des contraintes d'exécution et de la consommation des ressources de l'appareil, et est réalisé sur la plateforme Java.</li><li>**HH (Hiérarchies routières) x C++** (*Android uniquement*) est un algorithme qui utilise le langage de programmation C++ pour traiter efficacement les données du réseau routier et construire des itinéraires optimaux à l'aide de structures de données hiérarchiques. Il est optimisé pour un traitement rapide de grandes quantités de données et est particulièrement efficace pour naviguer sur des cartes avec de nombreux réseaux routiers.</li></ul> |
| *Approximation GPX* (*Android uniquement*) | <ul><li>L'approximation GPX **basée sur le routage** en **C++ et Java** utilise les données d'itinéraire pour approximer les traces GPS avec les itinéraires routiers existants, ce qui améliore la précision de la trace et réduit sa taille.</li><li>Les approximations GPX **basées sur la géométrie** en **C++ et Java** fonctionnent sur la base de principes géométriques pour approximer rapidement et précisément les traces GPS, permettant un traitement efficace de grandes quantités de données.</li></ul> |
| *Zoom automatique* | <ul><li>**Discret** vous permet de zoomer sur la carte à un niveau de détail spécifique mesuré en quelques étapes discrètes.</li><li>**Lisse** offre un changement progressif de l'échelle de la carte avec des effets d'animation fluides sans à-coups ni sauts.</li></ul> |
| *<Translate android="true" ids="use_live_routing"/>* (*Android uniquement*) | Utiliser les [mises à jour OsmAnd Live](../../personal/maps-resources.md#osmand-live) pendant le routage. Notez que nous recommandons d'utiliser cette option à des fins de test uniquement. |

<!--
| Parameter | Description | Note |
|:------------|:---------------|:---------------|
| *<Translate android="true" ids="use_live_routing"/>* | Allows using [OsmAnd Live updates](../../personal/maps-resources.md#osmand-live) while routing. Note, that we recommend using this option for testing purposes only. |
| *<Translate android="true" ids="use_two_phase_routing"/>* | Adds an extra phase to the default (A*) algorithm to improve the quality of the calculated route. This option may be useful for finding routes in large and complex road networks, although it may take more time for route calculation. |
| *<Translate android="true" ids="use_fast_recalculation"/>* | <Translate android="true" ids="use_fast_recalculation_desc"/> |
-->


## Invites vocales {#voice-prompts}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

- *<Translate android="true" ids="shared_string_menu,configure_profile,routing_settings_2,voice_announces"/>*
- *<Translate android="true" ids="shared_string_menu,shared_string_navigation,shared_string_settings,shared_string_sound,shared_string_settings"/>*

![Paramètres de navigation vocale Android](@site/static/img/navigation/voice/voice_promt-settings.png)

</TabItem>

<TabItem value="ios" label="iOS">

- *<Translate ios="true" ids="shared_string_menu,shared_string_settings,application_profiles,routing_settings_2,voice_announces"/>*
- *Bouton <Translate ios="true" ids="routing_settings"/>* *(ou <Translate ios="true" ids="shared_string_menu,shared_string_navigation"/>) → Choisir le profil → <Translate ios="true" ids="shared_string_settings,routing_settings_2,voice_announces"/>*

![Paramètres de navigation vocale iOS](@site/static/img/navigation/voice/voice_promt-settings-ios.png)

</TabItem>

</Tabs>

La première partie de l'article *[Invites vocales / Notifications](./voice-navigation.md)* décrit en détail comment configurer les invites vocales.

Les instructions audio pendant la navigation vous aident, en tant que conducteur ou piéton, à atteindre votre destination tout en [naviguant sur un itinéraire sélectionné](../setup/route-navigation.md). Elles contiennent des informations sur les virages, les directions de conduite, les panneaux de signalisation, les distances jusqu'à votre destination et d'autres facteurs pouvant affecter votre navigation.

Si vous sélectionnez une trace comme point de destination, vous devez utiliser l'option [Attacher aux routes](../setup/gpx-navigation.md#attach-to-the-roads) pour que les invites vocales fonctionnent correctement.

Les *invites vocales* vous permettent de vous concentrer sur la route et de ne pas être distrait par la carte ou le dispositif de navigation. Elles améliorent également la sécurité de conduite, réduisent le temps nécessaire pour naviguer en terrain inconnu et peuvent être utiles pour différents [types d'itinéraires](../routing/osmand-routing.md#routing-types).


## Alertes d'écran {#screen-alerts}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Aller à : *<Translate android="true" ids="shared_string_menu,configure_profile,routing_settings_2"/>*

![Paramètres de navigation](@site/static/img/navigation/navigation_settings_screen-alerts_new_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Aller à : *<Translate ios="true" ids="shared_string_menu,shared_string_settings,application_profiles,routing_settings_2"/>*

![Paramètres de navigation](@site/static/img/navigation/navigation_settings_screen-alerts_new_ios.png)

</TabItem>

</Tabs>

Le paramètre de navigation **Alerte d'écran** active le [**Widget d'alertes**](../../widgets/nav-widgets.md#alert-widget). *Détails :*

- Lorsque vous approchez d'un des obstacles pris en charge sur la route, des notifications apparaissent dans le coin inférieur gauche de la carte.
- Si vous configurez les [*invites vocales et textuelles*](../../navigation/guidance/voice-navigation.md) disponibles dans l'application OsmAnd, vous aurez un voyage plus confortable et plus sûr.
- L'apparence et le moment des invites dépendent de vos paramètres de vitesse. Vous pouvez les trouver [dans l'article](../../../technical/algorithms/voice-prompt-triggering.md).
- Le comportement des *Alertes d'écran* est également affecté par le paramètre [Afficher les points le long de l'itinéraire](../../navigation/guidance/map-during-navigation.md#show-points-along-the-route).

Vous pouvez ***sélectionner les alertes*** que vous souhaitez voir sur l'écran de l'application pendant la navigation :

- **Limite de vitesse** ([informations OSM Wiki](https://wiki.openstreetmap.org/wiki/Speed_limits)). Dans le paramètre Alertes d'écran, la *Limite de vitesse* n'est affichée à l'écran qu'avec les *Avertissements de trafic* activés. Si vous souhaitez voir les limites de vitesse pendant la navigation sans autres avertissements, utilisez le [widget](../../widgets/nav-widgets.md#speed-limit).
- **Avertissements de trafic** ([informations OSM Wiki](https://wiki.openstreetmap.org/wiki/Key:hazard#Traffic_hazards)). Des informations supplémentaires peuvent être trouvées dans l'article [Écran de la carte pendant la navigation](https://osmand.net/docs/user/navigation/guidance/map-during-navigation/#traffic-warnings).
- **Passages piétons** ([informations OSM Wiki](https://wiki.openstreetmap.org/wiki/Tag:crossing%3Duncontrolled)).
- **Radars** ([informations OSM Wiki](https://wiki.openstreetmap.org/wiki/Tag:highway%3Dspeed_camera)). Pour plus d'informations sur le paramètre Radar dans OsmAnd, lisez [Types d'alertes](../../widgets/nav-widgets.md#alert-types) et l'article *Paramètres globaux*, section [Légal](../../personal/global-settings.md#legal).
- **Tunnels** ([informations OSM Wiki](https://wiki.openstreetmap.org/wiki/Key:hazmat#Tunnel_restrictions)).

:::note
Les types d'avertissements ont une apparence visuelle différente, qui dépend de la région de voyage. OsmAnd ne vise pas à présenter des panneaux de signalisation 100 % identiques, mais souligne certaines similitudes.
:::


## Carte pendant la navigation {#map-during-navigation}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Aller à : *<Translate android="true" ids="shared_string_menu,configure_profile,routing_settings_2,map_during_navigation"/>*

</TabItem>

<TabItem value="ios" label="iOS">

Aller à : *<Translate ios="true" ids="shared_string_menu,shared_string_settings,application_profiles,routing_settings_2,map_during_navigation"/>*

</TabItem>

</Tabs>

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_map-during-1_andr.png)

La **carte est utilisée pendant la navigation** pour déterminer votre position, planifier votre itinéraire et l'orientation du terrain. Pendant la navigation, vous pouvez visualiser la carte avec *auto-centrage*, la déplacer et *zoomer/dézoomer* pour voir la zone requise. La carte peut également afficher des marqueurs indiquant des points d'intérêt, des itinéraires, des conditions météorologiques, des panneaux de signalisation et d'autres objets pour vous aider à naviguer. La carte peut être mise à jour en *temps réel* et affiche des *informations à jour* qui peuvent affecter la planification de l'itinéraire.

Vous pouvez apprendre comment le comportement de la carte change pendant la navigation dans l'article [Écran de la carte pendant la navigation](../guidance/map-during-navigation.md).

## Personnaliser la ligne d'itinéraire {#customize-route-line}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Aller à : *<Translate android="true" ids="profile_type_user_string,shared_string_settings,configure_profile,routing_settings_2,customize_route_line"/>*

![Paramètres de navigation](@site/static/img/navigation/navigation_settings_route-line_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Aller à : *<Translate ios="true" ids="shared_string_menu,shared_string_settings,application_profiles,routing_settings_2,customize_route_line"/>*

![Paramètres de navigation](@site/static/img/navigation/navigation_settings_route-line_ios.png)

</TabItem>

</Tabs>

Avec le paramètre **Personnaliser la ligne d'itinéraire**, vous pouvez choisir l'apparence de la ligne d'itinéraire qui sera visible sur la carte pendant la navigation. Vous pouvez sélectionner la *couleur*, la *largeur de la ligne* et l'affichage des *flèches de virage* sur celle-ci. Pour chaque profil, vous pouvez choisir une vue de ligne différente. Tous ces paramètres sont décrits en détail dans l'article *Écran de la carte pendant la navigation* dans la section [Apparence de la ligne d'itinéraire](../../navigation/guidance/map-during-navigation.md#route-line-appearance).


## Paramètres du véhicule {#vehicle-parameters}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Aller à : *<Translate android="true" ids="shared_string_menu,configure_profile,routing_settings_2"/>*

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_vehicle-parameters_1_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Aller à : *<Translate ios="true" ids="shared_string_menu,shared_string_settings,application_profiles,routing_settings_2"/>*

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_vehicle-parameters_ios.png)

</TabItem>

</Tabs>

Pour un calcul d'itinéraire optimal dans OsmAnd, vous devez prendre en compte les paramètres de véhicule suivants :

1. Définissez la [*vitesse par défaut* ou les *vitesses routières*](#default-speed--road-speeds), ainsi que la [vitesse minimale et maximale](#road-speeds) du véhicule. Cela aidera l'application à déterminer le temps nécessaire pour effectuer l'itinéraire et lui permettra de choisir le meilleur itinéraire, en tenant compte des limites de vitesse sur les différents segments de route.
2. Spécifiez le [*type*](#fuel-used-by-motor) de carburant utilisé par le moteur. Cela permettra à l'application d'estimer les émissions de CO2.
3. Saisissez la [*capacité de votre réservoir*](#fuel-tank-capacity) pour suivre précisément votre niveau de carburant et votre consommation.
4. Définissez les [*paramètres de taille et de poids*](#size-parameters) de votre véhicule, ce qui peut aider l'application à calculer l'itinéraire optimal et à éviter les obstacles sur la route en raison des restrictions.

La configuration correcte des paramètres dans l'application OsmAnd vous aidera à éviter les problèmes lors de la navigation sur un itinéraire, à choisir le plus approprié en fonction du type de véhicule et des restrictions routières, et à calculer le temps de votre voyage.


### Paramètres de taille {#size-parameters}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Aller à : *<Translate android="true" ids="shared_string_menu,configure_profile,routing_settings_2"/>*

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_sizes2_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Aller à : *<Translate ios="true" ids="shared_string_menu,shared_string_settings,application_profiles,routing_settings_2"/>*

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_sizes2_ios.png)

</TabItem>

</Tabs>

Les paramètres du véhicule affectent la navigation et la construction de l'itinéraire car ils déterminent la disponibilité des routes, des ponts, des ferries, des barrages et d'autres infrastructures. Si la hauteur, la largeur, la longueur ou le poids d'un véhicule dépasse les valeurs admissibles pour certaines sections de route, le système de navigation OsmAnd trouvera un itinéraire alternatif pour éviter les obstacles en cours de route.

- Les unités de mesure correspondront aux paramètres sélectionnés dans *Paramètres généraux → [Unités et formats](../../personal/profiles.md#units--formats)*.
- Les paramètres du véhicule peuvent être définis manuellement.
- Si vous sélectionnez manuellement le paramètre de mesure du véhicule, l'application vous proposera la valeur la plus proche de la liste prédéfinie. Ceci est nécessaire pour éviter les erreurs et construire l'itinéraire plus correctement.
- Vous pouvez choisir les paramètres du véhicule dans une liste de tailles prédéfinie.
- Ne définissez pas la taille, *Aucune*, ce qui signifie qu'aucune restriction sur le paramètre sélectionné ne sera appliquée.

#### Limites {#limits}

**1.** [**<Translate android="true" ids="routing_attr_weight_name"/> limite**](https://wiki.openstreetmap.org/wiki/Key:maxweight) - <Translate android="true" ids="weight_limit_description"/> Le paramètre Poids n'est disponible que dans les types de navigation tels que [*Voiture, Camion* et *Moto*](../../navigation/routing/car-based-routing.md).

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_weight_andr.png)

**2.** [**<Translate android="true" ids="routing_attr_height_name"/> limite**](https://wiki.openstreetmap.org/wiki/Key:maxheight) - <Translate android="true" ids="height_limit_description"/> Le paramètre Hauteur n'est disponible que dans les types de navigation tels que *[Voiture, Camion, Moto](../../navigation/routing/car-based-routing.md)* et *[Bateau](../../navigation/routing/boat-navigation.md)*.

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_height_andr.png)
![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_height_boat_andr.png)

**3.** [**<Translate android="true" ids="routing_attr_length_name"/> limite**](https://wiki.openstreetmap.org/wiki/Key:maxlength) - <Translate android="true" ids="lenght_limit_description"/> Le paramètre Longueur n'est disponible que dans les types de navigation tels que [*Voiture, Camion* et *Moto*](../../navigation/routing/car-based-routing.md).

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_length_andr.png)

**4.** [**<Translate android="true" ids="routing_attr_width_name"/> limite**](https://wiki.openstreetmap.org/wiki/Key:maxwidth) - <Translate android="true" ids="width_limit_description"/> Le paramètre Largeur n'est disponible que dans les types de navigation tels que *[Voiture, Camion, Moto](../../navigation/routing/car-based-routing.md)* et *[Bateau](../../navigation/routing/boat-navigation.md)*.

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_width_andr.png)
![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_width_boat_andr.png)

Les limites des paramètres du véhicule peuvent être importantes pour la navigation et la sécurité routière. Certaines de ces restrictions peuvent inclure :

1. Restrictions sur les véhicules circulant dans certaines zones urbaines.
2. Restrictions sur la circulation des véhicules sur des sections de route spécifiques, telles que les ponts, les tunnels à espace limité, les passages inférieurs à faible hauteur, les virages complexes ou d'autres structures.
3. Les limites de poids par essieu de véhicule peuvent être particulièrement importantes pour les camions.
4. Restrictions pour les véhicules circulant dans certaines conditions, telles que des températures élevées, des routes mouillées ou enneigées, la nuit ou par temps de visibilité limitée.

Ces restrictions peuvent être importantes pour la navigation et doivent être prises en compte lors de la planification d'un itinéraire. Si un véhicule dépasse les limites, cela peut entraîner des problèmes de sécurité routière, des dommages aux infrastructures, des amendes pour accident et d'autres conséquences juridiques. Par conséquent, les conducteurs doivent examiner attentivement l'itinéraire et s'assurer que la hauteur de leur véhicule respecte les limites.


### Paramètres de carburant {#fuel-parameters}

#### Carburant utilisé par le moteur {#fuel-used-by-motor}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Itinéraire de navigation Android](@site/static/img/navigation/route/navigation_settings_fuel_motor_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Itinéraire de navigation iOS](@site/static/img/navigation/route/navigation_settings_fuel_motor_ios.png)

</TabItem>

</Tabs>

Si vous sélectionnez le type de moteur dans les paramètres du véhicule, les [***données d'empreinte CO2***](../../navigation/setup/route-details.md#elevation-info) seront affichées au-dessus du graphique dans les [Détails de l'itinéraire](../setup/route-details.md).
Six types de carburant sont disponibles : ***Essence, Diesel, GPL, GNC, Électrique*** et ***Hybride***.

**Applicabilité :**

Le paramètre **Carburant utilisé par le moteur** n'est disponible que dans les types de navigation basés sur un véhicule tels que [*Voiture, Moto et Camion](../../navigation/routing/car-based-routing.md)*.


#### Capacité du réservoir de carburant {#fuel-tank-capacity}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_tank_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Paramètres de navigation Android](@site/static/img/navigation/navigation_settings_tank_ios.png)

</TabItem>

</Tabs>

Le paramètre **Capacité du réservoir de carburant** vous permet de suivre plus précisément le niveau de carburant et la consommation de votre véhicule en fournissant le volume total de votre réservoir. L'unité de mesure de la capacité de carburant est déterminée par les paramètres configurés dans *Menu → Configurer le profil → Paramètres généraux → Unités et formats → Unité de volume*. Pour des instructions détaillées sur la configuration des Unités et formats, reportez-vous à l'article [Profil (Paramètres)](https://osmand.net/docs/user/personal/profiles#units--formats).

OsmAnd prend en charge les unités de capacité suivantes :

- Gallons - **gal**. Cette abréviation est utilisée pour représenter à la fois les **gallons impériaux** et les **gallons américains**, selon vos préférences d'unité sélectionnées.
- Litres - **l**. L'unité métrique pour la capacité.

**Applicabilité :**

Le paramètre **Capacité du réservoir de carburant** n'est disponible que dans la navigation basée sur un véhicule. Pour les types de navigation tels que *Vélo*, *Équitation*, *À pied* et *Ski*, ce paramètre n'est pas affiché dans les Paramètres du véhicule.

En saisissant la capacité exacte de votre réservoir de carburant, l'application peut offrir une expérience plus personnalisée, notamment :

- Un suivi précis du carburant restant en fonction de votre consommation.
- Une planification d'itinéraire améliorée avec des arrêts de ravitaillement optimisés en fonction de la taille de votre réservoir.


### Vitesse par défaut / Vitesses routières {#default-speed--road-speeds}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Paramètres de navigation](@site/static/img/navigation/navigation_settings_speeds_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Paramètres de navigation](@site/static/img/navigation/navigation_settings_speeds_ios.png)

</TabItem>

</Tabs>

Pour tous les types de navigation, la vitesse minimale et maximale autorisée, par défaut et par route, peut être différente, selon certaines valeurs ([Limites de vitesse par défaut](https://wiki.openstreetmap.org/wiki/Default_speed_limits)) et restrictions pour les véhicules. La vitesse est également définie par certains incréments pour rendre les paramètres de l'application utilisables au maximum. Pour les profils *Marche*, *Équitation* et *Vélo*, par petits incréments équivalents à 0,1 km/h ([Unités et formats](https://osmand.net/docs/user/personal/profiles#units--formats)), et pour les autres profils, par incréments équivalents à 1 km/h.
Les paramètres de vitesse déterminent quand les [annonces vocales](../guidance/voice-navigation.md) sont activées.

Ces paramètres sont utilisés comme vitesse pour estimer l'[heure d'arrivée](../../widgets/nav-widgets.md#time-to-intermediate) lorsque la vitesse ne peut pas être déterminée à partir des données cartographiques :

- pour le profil sélectionné ;
- si les routes utilisées n'ont pas de limites de vitesse, ce qui peut également affecter le routage ;
- si des traces générées par l'utilisateur ou importées sont sélectionnées.


#### Vitesse par défaut {#default-speed}

La **vitesse par défaut** est la vitesse de déplacement prédéfinie. Elle est utilisée pour calculer l'heure d'arrivée et déterminer l'itinéraire optimal en fonction de la vitesse de déplacement que l'application considère typique pour ce mode de transport. Par exemple, voiture, transports en commun, piéton, ou la vitesse que vous définissez manuellement.


#### Vitesses routières {#road-speeds}

<InfoAndroidOnly />

![Paramètres de navigation](@site/static/img/navigation/navigation_settings_speeds-r_andr.png)


<!--
<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Navigation Settings](@site/static/img/navigation/navigation_settings_speeds-r_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Navigation Settings](@site/static/img/navigation/navigation_settings_speeds-r_ios.png)

</TabItem>

</Tabs>

:::note
Ces paramètres sous iOS sont disponibles dans *Menu → Paramètres → profil de l'application → Paramètres de navigation → Paramètres d'itinéraire → Vitesses routières*.
:::

-->

- **Vitesse minimale**
Le paramètre définit la vitesse de conduite minimale pour tous les types de routes sur l'itinéraire. Il augmente la priorité pour les routes avec une vitesse recommandée inférieure à la vitesse minimale.
- **Vitesse maximale**
Le paramètre définit la vitesse de conduite maximale et diminue la priorité pour les routes avec une vitesse possible supérieure à la vitesse maximale.


## Guidage détaillé de la trace {#detailed-track-guidance}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Aller à : *<Translate android="true" ids="shared_string_menu,configure_profile,routing_settings_2,detailed_track_guidance"/>*

![Attacher aux routes 1](@site/static/img/navigation/gpx/detailed_track_guidance_1_andr.png) ![Paramètres de navigation Android](@site/static/img/navigation/gpx/detailed_track_guidance_2_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Aller à : *<Translate ios="true" ids="shared_string_menu,shared_string_settings,application_profiles,routing_settings_2"/>* → *Guidage détaillé de la trace*

![Paramètres de navigation](@site/static/img/navigation/detailed_track_guidance_1_ios.png) ![Paramètres de navigation](@site/static/img/navigation/detailed_track_guidance_2_ios.png)

</TabItem>

</Tabs>

La fonctionnalité **Guidage détaillé de la trace** améliore la précision de la navigation routière lors de l'utilisation d'**itinéraires basés sur des traces**. Lorsque vous sélectionnez une trace comme destination, vous pouvez activer le paramètre [Attacher aux routes](../setup/gpx-navigation.md#attach-to-the-roads) à partir du menu [Suivre la trace](../setup/gpx-navigation.md#follow-track-options). Cela garantit que la trace est alignée avec les routes existantes pour une navigation plus fluide et plus précise.

Il existe deux options pour utiliser le *Guidage détaillé de la trace* :

- **<Translate android="true" ids="ask_every_time"/>** (*paramètres par défaut*) – L'option *Attacher aux routes* apparaîtra dans la section [Détails de l'itinéraire](../setup/route-details.md) chaque fois qu'un itinéraire basé sur une trace est calculé. Cela vous permet de décider d'appliquer ou non l'attachement aux routes pour chaque session de navigation.

- **<Translate android="true" ids="shared_string_always"/>** – Le processus d'attachement aux routes sera appliqué automatiquement pour chaque itinéraire de *navigation par trace* sans nécessiter de confirmation manuelle.

Pour plus d'informations sur l'utilisation de la navigation basée sur des traces, visitez [Navigation par trace](../setup/gpx-navigation.md).


## Articles connexes {#related-articles}

- [Paramètres d'itinéraire](../routing/osmand-routing.md#routing-types)
- [Préparation de l'itinéraire](../setup/route-navigation.md)
- [Navigation par trace](../setup/gpx-navigation.md)
- [Navigation par marqueurs](../setup/markers-navigation.md)
- [Détails de l'itinéraire](../setup/route-details.md)
- [Écran de la carte pendant la navigation](./map-during-navigation.md)
- [Invites vocales / Notifications](./voice-navigation.md)
- [Android Auto](../auto-car.md)
- [CarPlay](../car-play.md)

> *Dernière mise à jour : avril 2025*