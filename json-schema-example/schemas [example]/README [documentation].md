# DOCUMENTATION

*VERSION FRANÇAISE [ENGLISH VERSION BELOW]*

## Contenu des dossiers et des fichiers

La racine du dossier contient deux schémas: un pour le jeu des données (où chaque notice est une unité dans un array de json file) et l'autre pour une notice. La différence entre les schémas: dans le schéma de jeu des données toutes les notices (notice = objet json) sont regroupées dans un array, dans le schéma pour un ficher avec une seule notice il n'y pas de construction d'un array des notices, chaque notice reste un seul objet json.

**N.B.** Les champs "description" de certains mots-clés du schéma ne sont pas remplis (il est marqué "Field description"). Pour avoir plus de précisions sur le contenu de ces champs vous pouvez contacter les responsables du corpus (voir section “Auteur(s) du jeu des données”).

**schemas [annotated]**. Les exemples annotés des schémas. À ne pas oublier que le json pur n'autorise pas les commentaires; la version commentée ne pourra pas donc être validée. Ce sont des modèles des schémas basés sur des données fictives. L'objectif de ces modèles est d’indiquer les principaux éléments et la structure d'un schéma. Pour des schémas basés sur les données réelles du corpus, utilisez les schémas non annoté.

## Validation des schémas

Il existe plusieurs outils pour valider un schéma json. Voir: [Validators](https://json-schema.org/implementations.html#validators). Le plus simple est utilisé les outils en ligne, par exemple [jschon.dev | JSON Schema Validator](https://jschon.dev) ou [JSON Schema Lint](https://jsonschemalint.com/#!/version/draft-07/markup/json).

---

# DOCUMENTATION

*ENGLISH VERSION [VERSION FRANÇAISE PLUS HAUT]*

## Folders & files content

The root of this folder contains two schemas: first for the json file with whole dataset (where each record is a item array) and the second one for a file with only one record. The difference between these two schemas: on one hand, in the dataset schema, all items (where items = record) is a json object and they are grouped together in an array json object) are grouped together in an array; on other hand, in the single record schema, there is no construction of an array of records, each record remains a single json object.

**N.B.** The "description" fields of certain json schema keywords are not filled (it's just noted "Field description"). For more details on the content of these fields, you can contact the persons in charge of the corpus (see section “Author(s) of the dataset”).

**schemas [annotated]**. The scheama annotated examples. Remember that pure json does not allow comments; so the annotated version can't be validated. These a schemas models based on the fictif data. The purpose of these models is to indicate the main elements and schema structure. For a schemas based on the real corpus data, use the not annotated schemas. 

## Schemas validation

There are several tools to validate a json schema. See: [Validators](https://json-schema.org/implementations.html#validators). The simplest way is to use the online tools, for example [jschon.dev | JSON Schema Validator](https://jschon.dev) ou [JSON Schema Lint](https://jsonschemalint.com/#!/version/draft-07/markup/json).
