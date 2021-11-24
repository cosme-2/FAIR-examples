# DOCUMENTATION

*VERSION FRANÇAISE [ENGLISH VERSION BELOW]*

## Contenu des dossiers et des fichiers

La racine du dossier contient deux schémas: un pour le jeu des données (où chaque notice est une unité dans un array de json file) et l'autre pour une notice. La différence entre les schémas: dans le schéma de jeu des données toutes les notices (notice = objet json) sont regroupées dans un array, dans le schéma pour un ficher avec une seule notice il n'y pas de construction d'un array des notices, chaque notice reste un seul objet json.

**N.B.** Les champs "description" de certains mots-clés du schéma ne sont pas remplis (il est marqué "Field description"). Pour avoir plus de précisions sur le contenu de ces champs vous pouvez contacter les responsables du corpus (voir section “Auteur(s) du jeu des données”).

**schemas [annotated]**. Les exemples annotés des schémas. À ne pas oublier que le json pur n'autorise pas les commentaires; la version commentée ne pourra pas donc être validée. Ce sont des modèles des schémas basés sur des données fictives. L'objectif de ces modèles est d’indiquer les principaux éléments et la structure d'un schéma. Pour des schémas basés sur les données réelles du corpus, utilisez les schémas non annoté.

## Encodage des caractères

Certains champs des bases des données TELMA peuvent contenir les restes des balises XML. Ces balises sont, en général, un héritage de l'encodage des fichiers XML d'origine qui ont été importés dans TELMA. Le plus souvent, ces balises ont été utilisées pour marquer soit les différents styles de caractères (italique, gras, etc.), soit, par exemple, pour encoder de différentes parties du discours diplomatique d'un acte. Dans la majorité des cas (mais pas toujours), les champs qui contiennent ce type de balisage sont les champs avec les parties textuelles importantes (par exemple, "analyse", "transcription", etc.). 

Afin de préserver l'interopérabilité des documents numériques, ces balises ont été, le plus souvent, encodées en "entités HTML". Par exemple, le signe `<` devient une entité HTML `&lt;`. (Sur les entités HTML voir, par exemple: [Entité](https://developer.mozilla.org/fr/docs/Glossary/Entity) ou [Liste des entités de caractère de XML et HTML](https://fr.wikipedia.org/wiki/Liste_des_entit%C3%A9s_de_caract%C3%A8re_de_XML_et_HTML))

Cependant, le système d'export des données de la plateforme TELMA ne possède pas un modèle défini d'encodage et, pour cette raison, dans certains cas ce ne sont pas des entités HTML, mais le caractère d'échappement "barre oblique inversée" qui a été utilisé pour l'encodage des balises XML. Par exemple, certains éléments des balises `<span class="small-caps">` peuvent être échappés avec la barre oblique inversée pour devenir `<span class=\"small-caps\">`. (Sur ce point, voir par exemple [Caractère d'échappement](https://fr.wikipedia.org/wiki/Caract%C3%A8re_d%27%C3%A9chappement)).

Ces différents types d'encodage doivent alors être pris en compte lors de l'analyse et le traitement des données.

## Validation des schémas

Il existe plusieurs outils pour valider un schéma json. Voir: [Validators](https://json-schema.org/implementations.html#validators). Le plus simple est utilisé les outils en ligne, par exemple [jschon.dev | JSON Schema Validator](https://jschon.dev) ou [JSON Schema Lint](https://jsonschemalint.com/#!/version/draft-07/markup/json).

---

# DOCUMENTATION

*ENGLISH VERSION [VERSION FRANÇAISE PLUS HAUT]*

## Folders & files content

The root of this folder contains two schemas: first for the json file with whole dataset (where each record is a item array) and the second one for a file with only one record. The difference between these two schemas: on one hand, in the dataset schema, all items (where items = record) is a json object and they are grouped together in an array json object) are grouped together in an array; on other hand, in the single record schema, there is no construction of an array of records, each record remains a single json object.

**N.B.** The "description" fields of certain json schema keywords are not filled (it's just noted "Field description"). For more details on the content of these fields, you can contact the persons in charge of the corpus (see section “Author(s) of the dataset”).

**schemas [annotated]**. The scheama annotated examples. Remember that pure json does not allow comments; so the annotated version can't be validated. These a schemas models based on the fictif data. The purpose of these models is to indicate the main elements and schema structure. For a schemas based on the real corpus data, use the not annotated schemas. 

## Character encoding

Some TELMA database fields can contain the remains of XML tags. These tags are, in general, a legacy of the original XML files that were imported into TELMA. Most often, these tags have been used to mark the different styles (italics, bold, etc.), or, for example, to encode different diplomatic parts of the act. In many cases (but not always), the fields that contain this type of markup are the ones which contain significant textual parts (e.g., "analysis", "transcript", etc.).

In order to preserve the interoperability of digital documents, these tags have been encoded (in majority cases) in "HTML entities". For example, the sign `<` becomes an HTML entity `&lt;`. (On HTML entities see, for example: [Entity](https://developer.mozilla.org/en-US/docs/Glossary/Entity) or [List of XML and HTML character entity references](https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references)).

However, the TELMA platform's data export system does not have a stable encoding model and, for this reason, in some cases they are not HTML entities, but the "backslash" escape character which was used for encoding XML tags. For example, some elements of the `<span class="small-caps">` tags can be escaped with the backslash to become `<span class=\"small-caps\">`. (On this point, see for example [Escape character](https://en.wikipedia.org/wiki/Escape_character)).

These different types of encoding must be taken into account while dealing with this data.

## Schemas validation

There are several tools to validate a json schema. See: [Validators](https://json-schema.org/implementations.html#validators). The simplest way is to use the online tools, for example [jschon.dev | JSON Schema Validator](https://jschon.dev) ou [JSON Schema Lint](https://jsonschemalint.com/#!/version/draft-07/markup/json).
