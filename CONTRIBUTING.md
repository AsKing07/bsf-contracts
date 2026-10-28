# Contribuer aux contrats

Ce dépôt est un point de coordination entre groupes. Les règles servent à ce que chaque changement soit **visible** et **relu par ceux qu'il touche**.

## Branches et commits

- `main` est protégée : **aucune poussée directe**, tout passe par une pull request.
- Branches courtes : `feat/BSF-xx-slug`, `fix/BSF-xx-slug`, `docs/...`.
- Commits au format Conventional Commits avec la clé du ticket : `feat(auth): ajoute l'endpoint JWKS (BSF-11)`.
- Un groupe sans droit d'écriture passe par un **fork**.

## Règles de fond

- **Une pull request par changement de contrat**, pour qu'elle soit relisible.
- Un changement **compatible** (ajout d'un champ optionnel, d'un endpoint) peut être fusionné après relecture.
- Un changement **incompatible** (retrait, renommage, changement de type) exige une nouvelle version du contrat.
- Un contrat publié dans ce dépôt est une promesse : on ne l'implémente pas autrement sans en discuter.
- Le contrat doit contenir des **exemples** de requête et de réponse.

## Ce qui ne doit jamais être versionné

Secrets, jetons, URL internes, données personnelles réelles. Les exemples utilisent des données **fictives**.
