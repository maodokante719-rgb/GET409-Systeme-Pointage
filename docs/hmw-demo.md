## Script Démo S6 — Systeme-Pointage

> Livrable S2 · Prompt P-HMW-DEMO · Inputs : [hmw-definitif.md](./hmw-definitif.md) + [metriques-succes.md](./metriques-succes.md)
> **Version S2 (prévisionnelle).** Le MVP sera construit en S3-S5 : les passages « à mesurer » seront remplacés par les valeurs réelles du pilote avant la démo S6. Aucun résultat n'est inventé ici.

### HMW à prouver

"Comment pourrions-nous permettre à la responsable RH d'une PME dakaroise multi-sites d'obtenir chaque jour, sans ressaisie, une preuve de présence fiable et acceptée par chaque employé — au bureau comme en mission — afin de clôturer les éléments de paie en moins d'une journée et sans contestation ?"

### MVP démontré

Une application web où l'employé pointe son arrivée et son départ depuis son téléphone, avec vérification du lieu uniquement au moment du pointage (zone du site ou code QR). La responsable RH voit les présences du jour par site et exporte en un clic le récapitulatif mensuel prêt pour la paie.
Outils prévus : Bolt.new (application) · Dify (agent qui signale les anomalies du mois) · GitHub.
User stories montrées : US-01 (pointage vérifié) et US-03 (récapitulatif + export) — voir [backlog-s3.md](./backlog-s3.md).

### Matériel nécessaire

- Un smartphone Android (employé de démo) avec l'application ouverte et un compte de test
- Un laptop projeté avec le tableau de bord RH ouvert
- Un code QR de site imprimé (alternative sans GPS)
- Une feuille d'émargement papier et une capture de groupe WhatsApp (situation « avant »)
- Les données réelles du pilote de 30 jours : export du mois, registre des contestations, fiche de temps de clôture de la RH

### Script — 5 minutes chrono

#### Bloc 1 — La situation avant · 45 secondes

**Dire :** « Voici Ndèye Fatou, responsable RH d'une PME de 70 employés sur trois sites à Dakar. Chaque fin de mois, elle recompte des feuilles comme celle-ci et des messages WhatsApp de techniciens. Trois à quatre jours de ressaisie, et chaque mois des employés contestent leurs retenues parce que personne n'a de preuve. »
**Montrer :** la feuille d'émargement papier (avec deux signatures de la même écriture) puis la capture WhatsApp « je suis chez le client ».
**Le jury voit :** un problème concret, quotidien, sans aucune preuve fiable.

#### Bloc 2 — Le MVP en action · 2 minutes 30

**Dire :** « Un membre du jury va jouer l'employé. Il pointe son arrivée depuis ce téléphone. »
**Montrer :** le jury appuie sur « Pointer mon arrivée » ; l'application vérifie la position au moment du pointage et affiche « Sur site — 18 h 42 ».
**Le jury voit :** un pointage en moins de 30 secondes, horodaté et vérifié.

**Dire :** « Maintenant, j'essaie de pointer pour lui depuis un autre compte, hors du site. »
**Montrer :** la tentative est refusée ou marquée « hors zone » ; puis le pointage par code QR pour un employé sans GPS.
**Le jury voit :** on ne peut plus pointer pour un collègue ; les employés non équipés ont une alternative.

**Dire :** « Côté RH, Ndèye Fatou voit en temps réel qui est présent, en retard, absent ou en mission. Et en fin de mois, un clic. »
**Montrer :** le tableau de bord du jour (le pointage du jury apparaît), puis l'export du récapitulatif mensuel avec la liste des anomalies signalées par l'agent Dify.
**Le jury voit :** le pointage fait devant lui se retrouve dans l'export de paie, sans ressaisie.

#### Bloc 3 — Les métriques réelles · 1 minute

**Dire :** « Nous avons testé l'outil pendant 30 jours sur un site. Voici les trois chiffres que nous nous étions engagés à mesurer. »
**Montrer :** le tableau de bord S6 défini dans [metriques-succes.md](./metriques-succes.md).
**Le jury voit :**

| Indicateur | Cible | Réel |
|---|---|---|
| Métrique Nord — temps de clôture des éléments de paie | < 1 jour (contre 3 à 4 jours) | à mesurer en S6 |
| P1 — part des jours travaillés avec un pointage d'arrivée | ≥ 90 % | à mesurer en S6 |
| A1 — pointages « position imprécise » | alerte si > 15 % | déclenchée / non déclenchée |

#### Bloc 4 — La réponse au HMW · 45 secondes

**Dire :** « Notre question était : comment donner à la RH une preuve de présence fiable, acceptée par chaque employé, pour clôturer la paie en moins d'une journée. La réponse : un pointage personnel vérifié au moment où il est fait, jamais de suivi en continu, et un récapitulatif qui sort tout seul. Un pointage, une preuve, zéro ressaisie. »
**Montrer :** le HMW définitif affiché, à côté du temps de clôture réel mesuré.
**Le jury voit :** la promesse du HMW comparée à un chiffre mesuré.

### Questions jury anticipées

- **Q :** « N'est-ce pas de la surveillance ? » → **R :** La position est vérifiée uniquement au moment du pointage, jamais en continu (contrainte C2). L'employé voit ses propres pointages et peut demander une correction justifiée.
- **Q :** « Et si le réseau ou le GPS ne marche pas ? » → **R :** Le code QR du site sert d'alternative, et l'alerte A1 nous prévient si plus de 15 % des pointages sont imprécis. Le pointage hors ligne (US-07) est prévu après le MVP.

### Signal de succès de la démo

La démo est réussie si le pointage fait par un membre du jury apparaît, sans aucune ressaisie, dans le récapitulatif mensuel exporté à l'écran.
