# Vérifications — étape HTML sans CSS

## Corrections du 18 novembre 2026

- Numéro volontairement invalide `+000000000000` identique dans le texte, le lien `tel:` et le JSON-LD. Les deux liens WhatsApp utilisent les mêmes chiffres, sans le `+` : `000000000000`.
- Mentions de démonstration regroupées dans l’en-tête et le footer ; prix affichés sans neuf répétitions de « Prix fictif ». Note de chantier sur la police retirée du footer, informations conservées dans le README.
- Dimensions lues dans les fichiers : ambiance 1200 × 800 (68 570 octets), Open Graph 1200 × 630 (52 588 octets). Les attributs HTML 240 × 160 conservent exactement le ratio 3:2. Leur petite taille d’affichage est volontaire en attendant le CSS.
- Les quatre ressources demandées répondent HTTP 200 avec le type attendu : WebP, WebP, SVG, WOFF2.
- Crédit Rachel Claire / Pexels 4577715 vérifié sur la fiche de la photo ; source téléchargée à nouveau et empreinte SHA-256 comparée. Le recadrage du hero reproduit exactement le fichier utilisé.
- `og:locale` changé en `fr_FR`, exemple de la documentation officielle Open Graph. La liste complète des locales Meta n’a pas pu être consultée ; aucune affirmation de rejet systématique de `fr_CG` n’est faite.
- Nouvelle validation W3C : aucune erreur ni avertissement ; `validation-w3c.json` contient ce dernier résultat.
- Aucun CSS ni JavaScript de menu ajouté. Le JSON-LD reste une illustration pédagogique, sans attente de résultat enrichi pour un établissement fictif.
- Iframe Google Maps conservée avec `loading="lazy"`. Son impact reste à mesurer avec Lighthouse ; si nécessaire, prévoir une image statique du quartier correctement sourcée et un lien Google Maps, au lieu du contenu embarqué.

## Contrôles historiques du 17 novembre 2026

Date : 17 novembre 2026.

| Contrôle | Résultat |
| --- | --- |
| Validateur W3C Nu | Réussi : aucune erreur ni avertissement. Rapport brut : `validation-w3c.json`. |
| Description SEO | 138 caractères. |
| Structure et ressources | Un main, un h1, cinq sections, neuf plats, identifiants uniques, ancres et références ARIA valides ; ressources locales présentes et chemins sans slash initial. |
| GitHub Pages | Publication depuis main, dossier racine ; réponse HTTP 200 et contenu vérifié dans le navigateur. |
| Google Rich Results Test | Deux éléments valides détectés : commerce local et organisation, tous deux issus du Restaurant. Aucun problème critique. Champs facultatifs absents : priceRange et postalCode. |
| Clavier | Lien d’évitement activé avec Entrée : URL #contenu, focus effectivement sur main#contenu. |
| Navigation | Lien Infos pratiques testé, arrivée sur #infos-pratiques. |
| Carte | Iframe Google Maps chargée et contrôles de carte présents après accès à la section. |
| Fenêtres mobiles simulées | Pas de débordement horizontal à 390 px ni à 320 px. Photo chargée. Zéro feuille de style dans le document. |
| Capture | mobile-html.jpg, fenêtre 390 × 844 ; vue intermédiaire sans CSS. |
| Images | WebP, 1200 px de large, moins de 100 Ko chacune ; Open Graph 1200 × 630. |
| CSS et JavaScript de menu | Reportés à la prochaine étape à la demande de l’utilisateur. |
| Lighthouse Mobile, Chrome privé | Non exécuté ; Chrome n’est pas installé aux emplacements usuels. Aucun score revendiqué. À mesurer après le CSS et le JS. |
| Téléphone réel | Non effectué : nécessite un appareil physique et une vérification humaine. |

[Résultat Google consulté](https://search.google.com/test/rich-results/result?id=DViRXApVan4egaXcLii4DQ), exploration affichée par l’outil : 17 novembre 2026 à 20:09:20. Cette validation technique ne garantit ni indexation ni affichage enrichi ; les informations restent celles d’un restaurant fictif. Aucun code postal ni avis n’a été ajouté pour faire disparaître artificiellement une recommandation.

## Protocole pour la version finale

1. Ouvrir l’URL publiée dans Chrome, en navigation privée, puis DevTools → Lighthouse → Mobile. Exporter le rapport HTML et relever performance, accessibilité, bonnes pratiques et SEO.
2. Vérifier le lien d’évitement au clavier, le focus visible, le menu avec Entrée/Espace, la fermeture par Échap et par lien, et le retour du focus.
3. Repasser le validateur W3C et le Rich Results Test de Google après toute modification.
4. Sur un téléphone réel : portrait/paysage, zoom, débordements, liens d’ancres, lisibilité, carte et navigation. Ne pas appeler le numéro fictif ni lui envoyer de message.
5. Conserver les résultats datés et une capture du rendu final. L’objectif Lighthouse ≥ 90 reste à vérifier.
