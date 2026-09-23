## Contraintes MVP — Systeme-Pointage

> Livrable S2 · Prompt P-CHAPEAUX-CONTRAINTES (étape 02) · Input : Chapeaux Blanc et Noir de [chapeaux-bono.md](./chapeaux-bono.md)

### Persona

Ndèye Fatou Sarr · 39 ans · Responsable RH · PME de services, Dakar (siège au Plateau, 3 sites + terrain) · Smartphone Android ; employés équipés de smartphones (à vérifier, voir H-C2)

### Contraintes Non Négociables

#### Contrainte 1

**Critère :** Le MVP DOIT fonctionner sur les smartphones existants des employés, sans matériel à acheter.
**Origine :** Chapeau Blanc (employés déjà équipés) + Chapeau Jaune
**Élimine :** pointeuse biométrique, badge RFID, borne fixe.

#### Contrainte 2

**Critère :** Le MVP NE DOIT PAS suivre la position des employés en continu ; la position n'est vérifiée qu'au moment du pointage.
**Origine :** Chapeau Noir (rejet de la surveillance, loi n° 2008-12)
**Élimine :** suivi GPS en temps réel, historique de trajets, carte des déplacements.

#### Contrainte 3

**Critère :** Le MVP DOIT rendre impossible le pointage pour un collègue (identifiant personnel + vérification du lieu ou code QR du site).
**Origine :** Chapeau Noir (fraude au pointage)
**Élimine :** feuille d'émargement numérique partagée, pointage par un tiers sans validation.

#### Contrainte 4

**Critère :** Le MVP DOIT produire un récapitulatif mensuel par employé (heures, retards, absences, heures sup) exportable sans ressaisie.
**Origine :** Chapeau Blanc (3-4 jours de ressaisie)
**Élimine :** tout circuit qui repasse par Excel à la main.

#### Contrainte 5

**Critère :** Le MVP DOIT enregistrer l'heure réelle du pointage même si le réseau coupe, ou proposer une alternative (validation par le chef de site).
**Origine :** Chapeau Noir (coupures d'électricité et réseau instable)
**Élimine :** un pointage qui échoue silencieusement sans trace.

### Fonctionnalités Éliminées

- Reconnaissance faciale / biométrie → éliminée par C1 (matériel) et C2 (données sensibles).
- Suivi GPS continu des techniciens → éliminé par C2.
- Gestion complète de la paie (bulletins, cotisations) → hors HMW : on prépare les éléments de paie, on ne remplace pas le logiciel de paie.
- Messagerie interne → hors HMW, WhatsApp est déjà utilisé.

### Critère de Validation Final

Le MVP est valide si et seulement si : un employé peut pointer en moins de 30 secondes depuis son téléphone sur son lieu de travail, sans pouvoir le faire pour un autre, et la RH obtient le récapitulatif mensuel sans ressaisir une seule ligne.
