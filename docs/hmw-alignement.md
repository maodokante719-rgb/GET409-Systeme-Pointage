## Alignement HMW — Backlog S3 — Systeme-Pointage

> Livrable S2 · Prompt P-HMW-ALIGNEMENT · Inputs : [hmw-definitif.md](./hmw-definitif.md) + [backlog-s3.md](./backlog-s3.md)

### HMW Définitif

"Comment pourrions-nous permettre à la responsable RH d'une PME dakaroise multi-sites d'obtenir chaque jour, sans ressaisie, une preuve de présence fiable et acceptée par chaque employé — au bureau comme en mission — afin de clôturer les éléments de paie en moins d'une journée et sans contestation ?"

### Tableau d'Alignement

| US | Story résumée | Persona /2 | Problème /2 | Contexte /2 | Total /6 | Décision |
|---|---|---|---|---|---|---|
| US-01 | Pointage vérifié arrivée/départ | 2 | 2 | 2 | 6/6 | CONSTRUIRE |
| US-02 | Tableau de bord RH du jour | 2 | 2 | 1 | 5/6 | CONSTRUIRE |
| US-03 | Récapitulatif mensuel + export paie | 2 | 2 | 2 | 6/6 | CONSTRUIRE |
| US-04 | Historique employé + correction | 1 | 2 | 2 | 5/6 | CONSTRUIRE si le temps le permet |
| US-05 | Pointage « mission » validé | 1 | 2 | 1 | 4/6 | CONSTRUIRE si le temps le permet |
| US-06 | Assistant IA questions RH (Dify) | 2 | 1 | 0 | 3/6 | REPORTER |
| US-07 | Pointage hors ligne | 1 | 1 | 1 | 3/6 | REPORTER |

### Sprint S3 — Ordre de construction

1. US-01 — Pointage vérifié — Score : 6/6
2. US-03 — Récapitulatif mensuel + export — Score : 6/6
3. US-02 — Tableau de bord du jour — Score : 5/6

### User Stories Reportées

- US-06 → Score 3/6 → Raison : utile pour la RH mais ne produit ni preuve de présence ni clôture de paie.
- US-07 → Score 3/6 → Raison : répond à un risque réel mais trop coûteux pour une équipe no-code en S3 ; à reprendre après le MVP.

### Décision de sprint

En S3, l'équipe Systeme-Pointage construira 3 user stories dans cet ordre. La démo S6 prouvera le HMW si US-01 et US-03 fonctionnent en live : un pointage fait devant le jury apparaît dans le récapitulatif exporté.
