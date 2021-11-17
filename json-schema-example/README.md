# Contenu du dossier

*N.B. Les exemples des dossiers "schemas" seront utilisés pour produire les schémas de chaque corpus; pensez donc à changer "NOM_DU_CORPUS" (dans les intitulés des fichiers et à l'intérieur du code) pour les noms réels des corpus.*

*N.B. Remplacer les $id des schémas par URL où les schémas seront hébergés.*

*N.B. Chaque dossier contient également les versions annotées des schémas (marqué comme [annotated]). À ne pas oublier que le json pur n'autorise pas les commentaires; la version commentée ne pourra pas donc être validée.*


## data [examples]

Ce dossier contient les exemples des données json structurées selon les schémas json mis en place (voir dossier "schemas").

Le dossier contient deux fichiers exemple: i) dataset - l'exemple d'un fichier qui contient le jeu de données d'un corpus; ii) record - l'exemple d'un fichier qui ne contient que les données sur une notice.

## schemas [example]

Ce dossier contient tous les schémas json.

Ce dossier est également un modèle de l'organisation de la documentation pour un dépôt d'un corpus.

La racine du dossier contient deux schémas: un pour le jeu des données (où chaque notice est une unité dans un array de json file) et l'autre pour une notice. La différence entre les schémas: dans le schéma de jeu des données toutes les notices (notice = objet json) sont regroupées dans un array, dans le schéma pour un ficher avec une seule notice il n'y pas de construction d'un array des notices, chaque notice reste un seul objet json.

### schemas [annotated]

Les versions annotées des schémas. À ne pas oublier que le json pur n'autorise pas les commentaires; la version commentée ne pourra pas donc être validée.


## TEST_schemas [with subschemas]

### full.schema

Ce dossier contient un schéma s'appuyer sur les sous-schémas (avec Json pointer et $Ref); un sous-schéma décrit les données communes à tous les corpus (auteurs, intitulé, date de la création, etc.) et un autre décrit les champs spécifiques à chaque corpus. De fait, pour éviter la redondance du code et pour faciliter sa maintenance, il est plus opportun de diviser un schéma complexe en plusieurs sous-schémas. De surcroît, cette approche permet d'avoir un seul schéma principal (le choix entre un schéma de "jeu des données" et celui d'une "notice unique" se fait directement à l'intérieur du code).

Cependant, en pratique, il peut parfois s'avérer beaucoup plus difficile à parser et à valider les fichiers contre des schémas qui utilisent les Json Pointer et $Ref (sur ce point, voir infra *Validation des schémas*). Pour faciliter l'usage des schémas au plus grand nombre, il a été alors choisir de prendre comme le schéma principal le schéma plus verbeux et plus long, mais plus facile à valider et à parser (voir supra *schemas*).

N.B. Pour valider le schéma qui utiliser les références aux sous-schémas (Json pointer avec $Ref) (voir dossier *schemas [with subschemas]/full.schema*), il faut utiliser les parsers plus spécifiques, par exemple: [JSON Schema $Ref Parser](https://github.com/APIDevTools/json-schema-ref-parser)

### subschemas

#### dataset.common-info

Ce sous-schéma représente les informations communes (intitulé, auteurs, date de la création, etc.) d'un corpus.

#### specific-fields
