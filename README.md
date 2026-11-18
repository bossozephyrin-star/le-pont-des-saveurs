# Le Pont des Saveurs

Site vitrine de démonstration pour un **restaurant fictif à Brazzaville**, réalisé par Adriano Bosso, étudiant en Systèmes d’Information et Génie Logiciel.

Site publié sur GitHub Pages : https://bossozephyrin-star.github.io/le-pont-des-saveurs/

## Pourquoi ce projet ?

Présenter dans un portfolio une base de site de restaurant claire, accessible et légère, réunissant les cuisines du Sénégal, de Côte d’Ivoire et du Congo. Aucun avis, récompense, chiffre commercial ou établissement réel n’est revendiqué.

## État actuel : HTML et CSS mobile d’abord

Le site comprend les fondations CSS, l’en-tête, l’accueil et les cinq sections en une colonne. Les images de plats sont hébergées localement. Le JavaScript du menu viendra après le CSS ; le seul script actuel est un bloc de données JSON-LD non exécutable.

- Cinq sections, un seul `main`, un seul `h1`, puis des titres hiérarchisés.
- Lien d’évitement, ancres, listes de plats, coordonnées dans `address` et horaires dans `table` avec `caption` et en-têtes `scope`.
- Neuf plats, trois par pays, avec descriptions et prix fictifs en FCFA.
- Navigation toujours visible ; bouton du futur menu mobile désactivé. Après le CSS, `script.js` sera chargé avec `defer` et gérera ouverture, fermeture, Échap et clic sur un lien.
- Métadonnées, canonical, Open Graph et JSON-LD `Restaurant` correspondant au contenu visible et signalant la démonstration.
- Coordonnées et horaires inventés. Un seul numéro volontairement invalide : `+000000000000`, affiché tel quel et utilisé dans `tel:` et le JSON-LD ; `wa.me/000000000000` reprend exactement les mêmes chiffres sans le `+`. Il sert à illustrer le parcours, pas à tester un véritable appel ou une conversation WhatsApp.
- Carte Google Maps du quartier du Plateau, récupérée via « Partager / Intégrer une carte », avec titre, chargement différé et mention d’emplacement indicatif. Ce n’est pas la position d’un restaurant réel.

## Choix de structure

Les plats sont des **listes `ul`**, car ils constituent des éléments d’une même carte, pas des articles autonomes. Un lecteur d’écran peut annoncer le nombre d’éléments. Les pays portent un `h3` et les plats un `h4`, sans saut de niveau.

## Images et crédits

Photo d’ambiance de **Rachel Claire**, [Pexels, photo 4577715](https://www.pexels.com/photo/interior-of-restaurant-with-served-table-4577715/), utilisée selon la [licence Pexels](https://www.pexels.com/license/). Elle est explicitement illustrative et ne représente pas le restaurant fictif.

Sept photos de plats ont été sélectionnées sur Wikimedia Commons : yassa poulet, thieboudienne, mafé, kédjenou, alloco, poulet moambé et liboke. Les auteurs, liens vers les fiches sources, licences et transformations figurent dans le pied de page et dans [les crédits détaillés](docs/credits-photos.md). L’attiéké poisson braisé et le saka-saka restent sans photo faute de cliché retenu suffisamment adapté. Aucune image de Pinterest ou Google Images n’est utilisée.

| Fichier | Dimensions du fichier | Taille |
| --- | --- | --- |
| `assets/ambiance.webp` | 1200 × 800 | 68 570 octets |
| `assets/og-image.webp` | 1200 × 630 | 52 588 octets |

Recadrage et conversion WebP à qualité 75 avec Pillow/libwebp : **Squoosh était inaccessible** lors de la réalisation initiale. La photo d’accueil ne charge pas en lazy ; ses attributs `width="1200" height="800"` correspondent au fichier. Les photos de plats font 800 px de large et moins de 56 Ko chacune, avec `loading="lazy"`, un texte alternatif et leurs dimensions réelles. Le CSS conserve les proportions avec `max-width: 100%` et `height: auto`. L’image Open Graph n’est pas téléchargée par la page elle-même.

Favicon SVG original représentant un pont. Aucun service d’image distant n’est appelé au chargement de la photo.

Vérification du 18 novembre 2026 : le fichier source est identique (SHA-256) à la photo téléchargée depuis `https://images.pexels.com/photos/4577715/pexels-photo-4577715.jpeg?auto=compress&cs=tinysrgb&w=1200`. Le fichier hero correspond exactement au recadrage 1200 × 800 de cette source. La fiche Pexels attribue bien la photo 4577715 à Rachel Claire.

## Polices

Une famille : **Lora**, latin, graisses 400 et 700 en WOFF2, téléchargée via [google-webfonts-helper](https://gwfh.mranftl.com/fonts/lora?subsets=latin). Licence dans `fonts/OFL-Lora.txt`. La graisse 400 est préchargée ; les déclarations `@font-face` utilisent `font-display: swap`.

## Lancer localement

Aucune compilation ni dépendance applicative. Ouvrir `index.html`, ou, avec Python installé, lancer depuis le dépôt :

```sh
python -m http.server 8000
```

Puis ouvrir http://localhost:8000/ et arrêter le serveur avec Ctrl+C.

## Déploiement

GitHub Pages : Settings → Pages → Deploy from a branch → `main` → `/ (root)`.
Tous les chemins de ressources locales sont relatifs sans slash initial. Les URL canonical, Open Graph et JSON-LD sont absolues pour décrire correctement la page publique.

`og:locale` utilise `fr_FR`, exemple documenté dans le [protocole Open Graph](https://ogp.me/#optional). Le guide [Meta pour webmasters](https://developers.facebook.com/documentation/sharing/webmasters) renvoie à une liste de locales prises en charge ; cette liste n’a pas pu être consultée lors de la vérification. Nous retenons `fr_FR` sans prétendre que le protocole général interdit `fr_CG`. Cela ne change ni `lang="fr"` ni le pays `CG` de l’adresse.

Le JSON-LD sert à démontrer la connaissance du format et mentionne la démonstration. **Aucun résultat enrichi n’est attendu pour ce restaurant fictif** : la validation technique ne fait pas de lui un commerce réel.

## Vérifications et suite

Consulter [le rapport de vérification](docs/verification.md) pour les résultats réellement obtenus. Les scores Lighthouse définitifs et le test sur téléphone réel seront à reprendre après le CSS et le JavaScript. L’objectif 90/100 dans les quatre catégories n’est **pas un score acquis**.

L’étude de cas de cette étape se trouve dans [docs/etude-de-cas.md](docs/etude-de-cas.md).

Capture historique du 17 novembre 2026, avant les corrections éditoriales du 18 novembre, dans une fenêtre de 390 × 844 pixels, sans CSS (ce n’est pas un test sur téléphone physique) :

![Version HTML sans CSS au format mobile](docs/mobile-html.jpg)
