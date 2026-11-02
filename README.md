# Proko24

Édition numérique de la correspondance de Serge Prokofiev pour l’année 1924 : outils, conventions et fichiers TEI.

Proko24 est le laboratoire méthodologique de **ProKorresp**, projet d’édition critique de l’ensemble de la correspondance de Prokofiev (environ 12 000 lettres, dans une dizaine de langues, majoritairement en russe d’orthographe antérieure à 1918). L’année 1924 sert de corpus d’essai : on y fixe la chaîne de production et la doctrine d’encodage avant de passer à l’échelle.

Le projet est mené par Nicolas Moron (Université de Rouen Normandie, UR 3229 CÉRÉdI) dans le cadre d’une habilitation à diriger des recherches.

## Principes éditoriaux

- **Transcription diplomatique d’abord.** Le texte du manuscrit est conservé tel quel ; toute régularisation, résolution d’abréviation ou correction est explicite (`orig`/`reg`, `abbr`/`expan`, `sic`/`corr`), jamais silencieuse.
- **Production par couches.** Chaque lettre déclare son niveau d’encodage, de N1 (transcription publiable) à N5 (facsimilé fin). Dans un fichier de niveau N, une absence signifie « non applicable », jamais « oublié ».
- **Identifiants stables.** Un identifiant publié ne change jamais ; les autorités portent un préfixe de type (`per_`, `pla_`, `org_`, `wrk_`) et les œuvres de Prokofiev sont identifiées par leur numéro d’opus.
- **IA sous contrôle humain.** Les étapes automatisées (HTR, suggestions d’entités) sont systématiquement validées par l’éditeur.

## Chaîne de production

1. **Dépôt des images** sur [Nakala](https://nakala.fr) (Huma-Num) : un identifiant pérenne par lettre.
2. **Manifestes IIIF** générés à partir de Nakala pour l’import dans Transkribus.
3. **Reconnaissance d’écriture (HTR)** et correction dans Transkribus, avec typage des régions (en-tête, date, formule d’appel, corps, formule finale, post-scriptum, annotations…).
4. **Conversion PAGE XML → TEI** par un convertisseur dédié, qui applique la doctrine d’encodage : régularisation selon le décret orthographique de 1918, distinction langue / alphabet, contrôle des homoglyphes, un `<surface>` par page, déclaration du niveau.
5. **Archivage** des exports PAGE XML au moment de la conversion, puis **versionnement** des fichiers TEI dans ce dépôt.

## État d’avancement (novembre 2026)

- **Catalogue** : 580 lettres recensées pour 1924.
- **Doctrine d’encodage** : socle de conventions en version 1.4 (30 octobre 2026), couvrant identifiants, facsimilé, typage des régions Transkribus, balises en ligne, archivage et déclaration des couches.
- **Lettre de référence** : SPA_2490, encodée et validée, sert de modèle canonique.
- **Convertisseur PAGE → TEI** : aligné sur le socle ; testé sur les 18 lettres de janvier 1924 (40 pages) sans perte de texte.
- **Autorités** : fichiers TEI générés pour les personnes (105 notices), les lieux et les œuvres, en cours de vérification.
- **Nakala** : identifiants attribués pour les lettres de janvier et février 1924.
- **Cartographie** : carte interactive des échanges de 1924 (lieux d’expédition et de réception, filtres par langue et par mois, interface bilingue).

## Prochaines étapes

- Conversion par lot à partir des exports Transkribus.
- Retypage systématique des régions avant conversion en masse.
- Validation automatique des fichiers TEI (ODD / Schematron).
- Génération automatique des pages HTML de lecture (transcription et facsimilé côte à côte).
- Publication des dépôts Nakala et mise en ligne de l’édition, hébergée par l’Université de Rouen Normandie.

## Contenu du dépôt

| Dossier | Contenu |
|---|---|
| `TEI Files/` | Fichiers TEI des lettres et fichiers d’autorités |
| `Manifests iiiF/` | Manifestes IIIF, par mois |
| `app_nakala_to_iiif/` | Générateur de manifestes IIIF à partir de Nakala |
| `app_TEI_generator/` | Générateur TEI |
| `assets/` | Ressources graphiques |

## Sources et droits

Les manuscrits sont conservés à la Serge Prokofiev Archive (Columbia University). Conditions de réutilisation des images et des transcriptions : à voir avec les Archives et la famille Prokofiev.

## Contact

Nicolas Moron · Université de Rouen Normandie, CÉRÉdI · ORCID [0000-0001-7861-3382](https://orcid.org/0000-0001-7861-3382)
