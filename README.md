# TORA – Étude de la Torah

Application web pour étudier chaque jour le bloc de la parachat hachavoua, ou n'importe quelle parachat du Houmach. Elle fonctionne dans le navigateur, sans installation, et peut être ajoutée à l'écran d'accueil d'un téléphone.

Adresse du site : https://tinyvel.github.io/tora/

## Fonctions

**Écran d'accueil**
- **Paracha de la semaine** : le bloc du jour (dimanche = 1er bloc, …, chabbat = 7e), avec des boutons pour lire un autre bloc.
- **Houmach** : les cinq livres, puis la liste des parachiot de chaque livre, puis la parachat avec les mêmes fonctions que celle de la semaine.
- **Marque-pages** : la liste enregistrée.

**Pour chaque verset**
- Texte hébreu, Targoum Onkelos (araméen), commentaire de Rachi.
- Appui court sur un mot : sa traduction. Appui long puis glissement : sélection et copier-coller.
- Drapeaux 🇫🇷 / 🇬🇧 : langue des traductions.
- Clic sur le numéro de verset ou sur « Rachi » : traduction du verset ou du commentaire.
- Correction manuelle de la traduction de Rachi, conservée.
- Lampe : note personnelle sur le verset ou sur Rachi.
- Appui long sur le numéro de verset ou sur le nom d'un commentateur : ajout aux marque-pages (📍).

**Commentateurs**
- **O.H.** : Or HaChaïm.
- **S.H.** : Siftei Chakhamim.
- **G.A.** : Gur Aryeh.
- **RMBN** : Ramban (quand il existe pour le verset).

Chaque lien ouvre une fenêtre avec l'hébreu en haut et le français en bas. Un appui sur un mot met en évidence son équivalent approximatif dans l'autre zone. La traduction française est modifiable et la correction est conservée.

## Sources

- **Textes et calendrier : [Sefaria](https://www.sefaria.org)**. Parachat de la semaine, découpage en 7 blocs, texte hébreu, Onkelos, Rachi, Or HaChaïm, Siftei Chakhamim, Gur Aryeh, listes des parachiot. Les textes sont téléchargés à chaque ouverture et ne sont pas stockés dans ce dépôt. Chaque texte a sa propre licence, indiquée sur Sefaria.
- **Siftei Chakhamim** : édition « Sifsei Chachomim Chumash », Metsudah Publications, 2009, selon Sefaria.
- **Traductions françaises** : automatiques, avec le traducteur en ligne de Google (adresse publique non officielle) et MyMemory en secours. L'application traduit en priorité l'anglais fourni par Sefaria, qui donne de meilleurs résultats que l'hébreu. Ces traductions peuvent contenir des erreurs et ne remplacent pas une traduction humaine.

## Données personnelles

Notes, corrections de traduction et marque-pages sont enregistrés dans le navigateur de chaque utilisateur, sur son appareil. Rien n'est envoyé à un serveur et rien n'est stocké dans ce dépôt. Les boutons de sauvegarde et de restauration, en bas de page, permettent de déplacer ou de protéger ces données.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | L'application complète (page, styles et code) |
| `manifest.webmanifest` | Permet d'ajouter l'application à l'écran d'accueil |
| `sw.js` | Mise en cache du fichier de l'application |
| `icon-192.png`, `icon-512.png` | Icônes de l'application |

## Publier une nouvelle version

1. Dans le dépôt, onglet **Code**, cliquer sur **Add file**, puis **Upload files**.
2. Envoyer le nouvel `index.html` (même nom : il remplace l'ancien).
3. Cliquer sur **Commit changes**.
4. Attendre la coche verte dans l'onglet **Actions**, puis recharger le site avec Ctrl + F5.

Le site est publié par GitHub Pages depuis la branche `main`, dossier racine.

## Limites connues

- Les traductions automatiques sont approximatives, surtout pour l'hébreu rabbinique.
- La mise en évidence des mots équivalents est une estimation.
- Le découpage en 7 blocs peut manquer pour certaines parachiot doubles.
- Le fonctionnement hors connexion n'est pas prévu : les textes ont besoin de Sefaria.

## À faire

- Mettre à jour le guide d'utilisation.
- Optimiser le code : supprimer le code mort, regrouper les parties dupliquées, mettre en mémoire les textes déjà chargés.
