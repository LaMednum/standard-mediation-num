# Schéma de données des lieux de médiation numérique
Ce schéma permet de modéliser les différents attributs des lieux de médiation numérique. 

## Contexte
Il existe un réel besoin d’une vision nationale, complète et actualisée de l’offre de médiation numérique

Des acteurs de la médiation numérique, notamment les hubs, ont produit de nombreuses données de recensement des lieux et des offres de médiation mais souvent, ces productions ne respectent pas le même format, rendant alors impossible une vision formalisée, complète et partagée de l’offre nationale de médiation numérique. 

### La standardisation : une solution pour fédérer les données ?

La standardisation permet de décrire l'offre de médiation numérique de manière harmonisée. Elle repose sur un travail de concertation dans lequel des utilisateurs représentatifs ont défini un schéma de données qui décrit le format des fichiers, les différents champs, les valeurs possibles…

### Un travail qui contribue à la construction d'une cartographie nationale et d'une multitude d’usages

En lien étroit avec ces travaux, l’ANCT mène actuellement un projet de cartographie nationale de l’offre de médiation numérique. Les données seront ouvertes pour développer une multitude d’usages : guider les usagers vers une structure de médiation numérique, accompagner les acteurs territoriaux dans le développement de l’offre, analyser l’adéquation entre l’offre et le besoin pour les publics fragiles…

## Construction collaborative du schéma de données 

Ce travail est piloté par l’Agence nationale pour la cohésion des territoires (ANCT) et La MedNum avec l’appui de Datactivist. La concertation autour du schéma s'est structurée autour de cercles concentriques : un comité de pilotage propose des arbitrages autour des suggestions de ce groupe ouvert de contributeurs. Près d'une cinquantaine de personnes ont participé à chacun des trois ateliers de travail, et 120+ commentaires ont permis d'aboutir une version finale du schéma de données.

## Les enjeux soulevés 

Pour favoriser le lien avec le référencement des lieux d'insertion, le schéma de données s'appuie sur les champs de définition d'un lieu proposé dans le schéma de données de data.inclusion. 

#### Identifiant : 
La question de l'usage du SIRET ou du RNA comme identifiant unique a posé de nombreuses questions. Une facilitation de collecte est proposée grâce à un identifiant choisi localement. Le SIRET ou le RNA restent toutefois nécessaires pour faciliter l'exploitation des donénes avec d'autres bases (donnée pivot). 
#### Services : 
La liste des services proposés par les structures a été limitée à 15 valeurs d'une grannularité validée collectivitement en COPIL et en atelier. Les demandes d'ajout de services dans les commentaires font émerger le besoin de documenter chaque valeur en précisant les sous-catégories qu'elle recouvre.
#### Accessibilité / Accueil handicap : 
Des échanges avec l’équipe d’acceslibre ont fait émerger le besoin, pour les personnes en situation de handicap, d’avoir accès à beaucoup d’informations sur les lieux recevant du public. Un champ “accessibilité PMR” ne suffit pas et conduit nécessairement la personne à téléphoner au lieu pour un complément d’information. 
Afin de répondre aux besoins des publics concernés, un atelier ouvert a validé le fait d’encourager les lieux à remplir leur profil sur acceslibre et à en mettre le lien dans le schéma de données. 
Ce remplissage prend quelques minutes et le champ n’est pas obligatoire. 

##Description du schéma

La documentation des champs du schéma est accessible ici *insérer lien schema.data.gouv.fr*. 

Un [gabarit](https://github.com/LaMednum/standard-mediation-num/blob/main/Schema_lieux_mediation_numerique_gabarit.xlsx) au format tableur est également prévu pour faciliter la publication d'un jeu de données au format du schéma.

##Format de fichier

Le format de fichier retenu pour la publication des données est le CSV (Comma Separated Values, valeurs séparées par des virgules).

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de formatage suivantes :

*l’encodage des caractères est UTF-8,
*le séparateur des colonnes est la virgule,
*le séparateur des nombres décimaux est le point,
*le séparateur de valeurs multiples dans un champ est le point-virgule,
*si un champ contient une virgule, il doit être entouré de guillemets doubles,
*chaque ligne doit avoir le même nombre de champs,
*le type MIME ou Content-Type est text/csv.

###Recommandations pour le nommage des fichiers :
Les fichiers doivent, sauf exception et autant que possible, respecter les règles de nommage suivantes :

AAAAMMJJ_idProducteur_lieux-de-mediation-numerique_territoire.csv

*AAAAMMJJ : Date de création du fichier
*idProducteur :  Numéro SIRET ou RNA sur 14 chiffres pour identifier le producteur
*lieux_de_mediation_numerique : nom du fichier, en minuscules non accentuées
*territoire : Nom du territoire concerné, non accentué (exemple : RegionSud)
*extension : Si les règles de formatage sont respectées, l'extension est .csv

Exemple : 20220725_123456789_lieux-médiation-numérique_Bordeaux.csv

###Recommandations pour la mise en conformité :
Ces conseils reprennent ceux du [Schéma des données locales publié par Open Data france](https://scdl.opendatafrance.net/docs/recommandations-relatives-aux-jeux-de-donnees.html)

Les fichiers doivent comporter :
*Toutes les colonnes, y compris celles dont les cellules ne sont pas renseignées, dans le bon ordre, et avec des en-têtes correctement nommées sur la première ligne (nom correspondant strictement au schéma)
*Autant de lignes que nécessaire comprenant des cellules dont les valeurs peuvent être obligatoires (elles doivent être impérativement renseignées) ou optionnelles (elles sont seulement recommandées ou soumises à condition de disponibilité / pertinence)
*Traitement des cellules vides (absence de valeur ou valeur équivalente à 0) : ces cellules doivent être laissées vides. Dans le cas où une valeur numérique est égale à zéro elle doit être écrite 0.0 (zéro [point] zéro), et, dans le cas où des caractères spéciaux sont utilisés pour remplacer des valeurs manquantes (ex. "-" ou "NaN"), cela doit être mentionné dans les métadonnées.
*Les dates doivent être formées selon la norme 8601 : YYYY-MM-DD.

