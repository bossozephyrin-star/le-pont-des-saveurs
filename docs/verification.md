# Vérifications — étape HTML sans CSS

Date : 17 novembre 2026.

| Contrôle | Résultat |
| --- | --- |
| Validateur W3C Nu | Réussi : aucune erreur ni avertissement. Rapport brut : `validation-w3c.json`. |
| Description SEO | 138 caractères. |
| Images | WebP, 1200 px de large, moins de 100 Ko chacune ; Open Graph 1200 × 630. |
| CSS et JavaScript de menu | Reportés à la prochaine étape à la demande de l’utilisateur. |
| Lighthouse Mobile, Chrome privé | Non exécuté ; Chrome n’est pas installé aux emplacements usuels. Aucun score revendiqué. À mesurer après le CSS et le JS. |
| Téléphone réel | Non effectué : nécessite un appareil physique et une vérification humaine. |

## Protocole pour la version finale

1. Ouvrir l’URL publiée dans Chrome, en navigation privée, puis DevTools → Lighthouse → Mobile. Exporter le rapport HTML et relever performance, accessibilité, bonnes pratiques et SEO.
2. Vérifier le lien d’évitement au clavier, le focus visible, le menu avec Entrée/Espace, la fermeture par Échap et par lien, et le retour du focus.
3. Repasser le validateur W3C et le Rich Results Test de Google après toute modification.
4. Sur un téléphone réel : portrait/paysage, zoom, débordements, liens d’ancres, lisibilité, carte et navigation. Ne pas appeler le numéro fictif ni lui envoyer de message.
5. Conserver les résultats datés et une capture du rendu final. L’objectif Lighthouse ≥ 90 reste à vérifier.
