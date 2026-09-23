## Backlog S3 — Systeme-Pointage

> Livrable S2 · Prompt P-VPC-BACKLOG (étape 07) · Inputs : [vpc.md](./vpc.md) + [contraintes-mvp.md](./contraintes-mvp.md)
> Outils de construction S3 : Bolt.new + Dify + GitHub

### HMW Définitif

"Comment pourrions-nous permettre à la responsable RH d'une PME dakaroise multi-sites d'obtenir chaque jour, sans ressaisie, une preuve de présence fiable et acceptée par chaque employé — au bureau comme en mission — afin de clôturer les éléments de paie en moins d'une journée et sans contestation ?"

### User Stories MUST

*(À construire obligatoirement en S3)*

#### US-01

**Story :** En tant qu'employé, je veux pointer mon arrivée et mon départ depuis mon téléphone sur mon lieu de travail afin que ma présence soit enregistrée sans feuille papier.
**Priorité :** MUST
**Outil :** Bolt.new
**Effort :** moyen
**Adresse :** Pain Reliever « pointage personnel vérifié »
**Critère d'acceptation :** un employé connecté pointe en moins de 30 secondes ; l'heure et le statut du lieu (sur site / hors zone) sont enregistrés ; un second compte ne peut pas pointer à sa place.

#### US-02

**Story :** En tant que responsable RH, je veux voir sur un tableau de bord qui est présent, en retard, absent ou en mission aujourd'hui, par site, afin de ne plus relancer chaque site sur WhatsApp.
**Priorité :** MUST
**Outil :** Bolt.new
**Effort :** moyen
**Adresse :** Gain Creator « tableau de bord du jour »
**Critère d'acceptation :** le tableau de bord affiche les pointages du jour en moins de 5 secondes, filtrables par site.

#### US-03

**Story :** En tant que responsable RH, je veux obtenir en fin de mois un récapitulatif par employé (jours travaillés, retards, absences, heures supplémentaires) exportable afin de clôturer la paie en moins d'une journée.
**Priorité :** MUST
**Outil :** Bolt.new (calcul + export) · Dify (agent qui signale les anomalies du mois)
**Effort :** élevé
**Adresse :** Pain Reliever « récapitulatif mensuel automatique » + Gain Creator « export prêt pour la paie »
**Critère d'acceptation :** l'export du mois est généré en un clic et correspond aux pointages ; la liste des anomalies (oubli de départ, hors zone) est affichée.

### User Stories SHOULD

*(À construire si le temps le permet)*

#### US-04

**Story :** En tant qu'employé, je veux consulter l'historique de mes pointages et demander une correction avec un justificatif afin que mes heures soient reconnues comme justes.
**Priorité :** SHOULD
**Outil :** Bolt.new
**Effort :** moyen
**Adresse :** Gain Creator « source de vérité partagée »
**Critère d'acceptation :** la demande de correction est visible par la RH, qui l'accepte ou la refuse ; chaque décision est tracée.

#### US-05

**Story :** En tant que technicien, je veux pointer « en mission » chez un client, validé par mon chef d'équipe, afin que ma journée soit comptée sans message WhatsApp.
**Priorité :** SHOULD
**Outil :** Bolt.new
**Effort :** moyen
**Adresse :** Pain Reliever « pointage mission validé »
**Critère d'acceptation :** le pointage mission apparaît dans le tableau de bord avec le statut « en attente » puis « validé ».

### User Stories COULD

*(Roadmap post-MVP)*

#### US-06

**Story :** En tant que responsable RH, je veux poser une question en langage naturel (« qui a le plus de retards ce mois-ci ? ») afin d'obtenir une réponse chiffrée sans construire de tableau.
**Priorité :** COULD
**Outil :** Dify
**Effort :** moyen
**Adresse :** Gain Creator « temps RH libéré »
**Critère d'acceptation :** l'agent répond à 5 questions types à partir des données de pointage.

#### US-07

**Story :** En tant qu'employé, je veux que mon pointage soit enregistré avec son heure réelle même en cas de coupure réseau afin de ne pas être pénalisé.
**Priorité :** COULD
**Outil :** Autre (développement spécifique)
**Effort :** élevé
**Adresse :** Contrainte C5
**Critère d'acceptation :** un pointage fait hors ligne est transmis au retour du réseau avec son heure d'origine.

### Sprint S3

**Semaine 1 :** US-01 (pointage vérifié) + US-02 (tableau de bord du jour)
**Semaine 2 :** US-03 (récapitulatif mensuel + export), puis US-04 si avance
**Démo S6 :** US-01 et US-03 en live — un pointage fait devant le jury apparaît dans le récapitulatif exporté
