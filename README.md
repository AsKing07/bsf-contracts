# bsf-contracts

Dépôt commun des **contrats d'API** (fichiers OpenAPI) des produits du programme B-School Factory. Il sert à se coordonner entre les quatre groupes : quand un groupe change un champ, il ouvre une pull request et les autres la voient.

> **État : amorçage.** Le dépôt est créé (ticket BSF-43). Aucun contrat n'est encore publié.

**Pas de code. Pas de CI. Aucun secret** : ce dépôt est le plus largement lisible, rien de sensible n'y entre.

## Structure

| Dossier | Contrat de |
|---|---|
| `auth/` | Service d'authentification (`bsf-auth`) |
| `portail/` | Portail B-School Factory |
| `referentiel/` | Référentiel de compétences |
| `passeport/` | Passeport Digital |

Un fichier OpenAPI par produit, nommé `openapi.yaml`, dans son dossier.

## Conventions communes (proposées, à valider entre les groupes)

- API REST en JSON, décrite en OpenAPI 3.x, **versionnée** dans le chemin (`/v1/...`).
- Identifiants : **UUID v4**.
- Dates et heures : **ISO 8601 en UTC**.
- Format d'erreur uniforme, pagination, filtrage et tri documentés dans chaque contrat.
- On référence une compétence par son **identifiant**, jamais par un libellé copié.

## Proposer un changement

1. Créer une branche (ou un fork si vous n'avez pas les droits d'écriture) : `feat/BSF-xx-slug`.
2. Modifier le contrat du produit concerné.
3. Ouvrir une pull request en remplissant le modèle : nature du changement, consommateurs impactés, exemples.
4. Obtenir la relecture d'au moins une personne du groupe **consommateur** avant de fusionner.

Un changement qui casse la compatibilité (retrait ou renommage d'un champ, changement de type) passe par une **nouvelle version** du contrat.

## Contribuer

Voir [CONTRIBUTING.md](CONTRIBUTING.md).

## Licence

Les contrats de ce dépôt sont publiés sous licence [MIT](LICENSE) : les quatre groupes du programme peuvent les réutiliser, les copier et les adapter librement.

## Maintenance

Initié par la squad Portail ; chaque groupe maintient le contrat de son propre produit.
