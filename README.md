# Système de coordonnées de référence PROJ Verniquet

Ce dépot contient les fichiers PROJ de définition du système de coordonnées projeté utilisé dans l'« Atlas du plan général de la ville de Paris » levé sous la direction d'Edme Verniquet entre 1784 et 1791.

Il a été utilisé durant le [projet ANR SoDUCo ](https://soduco.github.io/) pour géoréférencer les différents exemplaires du plan de Verniquet ainsi que ses réutilisations au XIX<sup>e</sup> à partir uniquement des coordonnées du carroyage d'un plan.

Deux formats de définition sont disponibles:
- `verniquet.wkt` : PROJ *Well Known Text*
- `verniquet.proj` : chaîne PROJ. Son usage est déconseillé et n'est fourni que dans un souci de compatibilité avec d'anciens SIG.

L'atlas de Verniquet et sa triangulation font l'objet d'une étude critique en cours. Les premières analyses ont été présentées au séminaire SoDUCo-BnF le 11 avril 2022.

 [![](https://img.shields.io/badge/HAL-Presentation-red)](...) [![](https://img.shields.io/badge/PDF-Presentation-blue)](./supplementary/SODUCO_seminar_2-2022_04_02.pdf)

## 🌐 Description 

Dans le repère du plan de Verniquet, les coordonnées 2D d'un point de l'espace correspondent à sa distance **en toises du Châtelet** au [méridien de Paris ](https://fr.wikipedia.org/wiki/M%C3%A9ridien_de_Paris) et à une perpendiculaire de ce méridien passant à l'observatoire de Paris, dont la position est donnée par un carnet de relevés conservé aux Archives Nationales (voir [Références](#références)).

Le plan de Paris ayant été levé localement par triangulation, sans considération de la rotondité de la terre, le SCR est muni d'une [projection azimutale équidistante](https://en.wikipedia.org/wiki/Azimuthal_equidistant_projection).
Il est appuyé sur le système géodésique [RGF93 v2](https://epsg.io/9776).

> [!IMPORTANT]  
L'unité attendue des coordonnées dans le SCR Verniquet est la **toise du Châtelet**, fixée à `1.94903631` mètres. Il est possible d'utiliser ce SCR avec des coordonnées en mètres :
> - en supprimant le paramètre `+to_meter` dans `verniquet.proj`;
> - en remplaçant les occurences de `LENGTHUNIT["toise",1.94903631]` par `LENGTHUNIT["metre",1]` dans `verniquet.wkt`.

## ⚠️ Limitations

1. Le système de coordonnées n'est pertinent qu'à grande échelle et pour l'espace parisien.

3. Il n'est adapté à des usages tenant nécessitant de prendre en compte l'altitude.


# 📚 Références
> Pronteau, J. (1986). Edmé Verniquet (1727-1804): architecte et auteur du" grand plan de Paris"(1785-1791). Commission des travaux historiques, Sous-commission de recherches d'histoire municipale contemporaine.

> « Atlas des opérations trigonométriques pour la Ville de Paris par Edme Verniquet, mathématicien. ». Archives Nationales, [MC/ET/LVIII/648/A](https://www.siv.archives-nationales.culture.gouv.fr/siv/rechercheconsultation/consultation/ir/consultationIR.action?irId=FRAN_IR_054362&udId=c-9jd6kmfjf-z7pptc8ktikb&details=true&gotoArchivesNums=false&auSeinIR=true). Date inconnue, probablement avant 1791.


# 🙏 Remerciements
Nous remercions chaleureusement l'[observatoire de Paris](https://www.observatoiredeparis.psl.eu/) pour avoir autorisé la réalisation des relevés topographiques ayant permis de mesurer la position du point d'origine du repère du système de coordonnées du plan.

# 💬 Citer ce travail
> TODO
