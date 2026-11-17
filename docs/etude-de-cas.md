# Étude de cas — Le Pont des Saveurs

## Problème

Comment démontrer la capacité à concevoir un site de restaurant pour un portfolio, sans client réel ni informations commerciales vérifiées ? Le site doit rester honnête tout en présentant une carte, des coordonnées, une navigation et les bases du référencement.

## Solution réalisée à cette étape

Une page en HTML natif, sans framework, avec cinq sections. La carte réunit neuf plats du Sénégal, de Côte d’Ivoire et du Congo. Les prix et coordonnées sont explicitement fictifs. Le lien d’évitement, les titres ordonnés, les listes et le tableau d’horaires donnent une structure exploitable au clavier et par les lecteurs d’écran.

Le head contient les métadonnées de partage, une URL canonique et un objet JSON-LD Restaurant cohérent avec les informations affichées. Une photo Pexels créditée illustre uniquement l’ambiance ; aucun plat n’est associé à une image inexacte. Les fichiers WebP restent sous 100 Ko et la police est préparée localement.

## Apprentissages de cette étape

- Choisir une balise selon son rôle : `address` pour les coordonnées, `table` pour les jours et horaires, `ul` pour les plats.
- Distinguer la structure HTML, la présentation CSS et les comportements JavaScript : la page actuelle est volontairement sans CSS, à la demande du porteur du projet.
- Faire correspondre les données structurées à ce que lit le visiteur ; une syntaxe valide ne garantit ni classement Google ni résultat enrichi.
- Prévoir le sous-dossier GitHub Pages dans les URL de ressources.
- Mesurer et documenter les vérifications, sans inventer de scores ni confondre émulation mobile et téléphone réel.

## Suite prévue

Créer le CSS mobile d’abord, appliquer Lora avec `@font-face`, puis ajouter le seul comportement JavaScript : le menu mobile. Ensuite, mesurer Lighthouse Mobile dans Chrome en navigation privée, vérifier le clavier et les lecteurs d’écran, tester sur un téléphone réel et remplacer la capture intermédiaire par celle du rendu final.
