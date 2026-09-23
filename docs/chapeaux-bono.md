# 6 Chapeaux de Bono — Systeme-Pointage

> Livrable S2 · Prompt P-CHAPEAUX (étape 01) · Facilitateur : Oumar Mbodou Seid (PM) · Scribe : Oluwadara Emmanuel Ebeh (Prompt Engineer)
> Sources : carte d'empathie S1 ([../carte-empathie.md](../carte-empathie.md)) et interview simulée S1 ([guide-interview.md](./guide-interview.md)).

## HMW analysé

"Comment pourrions-nous aider la responsable RH d'une entreprise dakaroise multi-sites à disposer de présences fiables et vérifiables de tous ses employés, au bureau comme sur le terrain, afin de préparer la paie sans ressaisie ni litiges en fin de mois ?"

## 🤍 Chapeau Blanc — Faits & Données

- La RH de notre persona gère environ 70 employés sur 3 sites (siège au Plateau, Pikine, Diamniadio) plus des techniciens en intervention chez les clients.
- Les présences sont relevées sur des feuilles d'émargement papier et par messages WhatsApp, puis ressaisies dans Excel : la consolidation prend 3 à 4 jours par mois (interview S1, Q6).
- Au Sénégal, la durée légale du travail est de 40 heures par semaine (Code du travail) : au-delà, les heures supplémentaires sont majorées — les compter juste a un impact direct sur la paie.

## ❤️ Chapeau Rouge — Émotions & Intuitions

- La RH est épuisée et anxieuse : « Chaque fin de mois, je passe mes soirées à recompter les feuilles de présence. »
- Les techniciens se sentent injustement sanctionnés quand une journée passée chez un client leur est retenue.
- Tout le monde redoute le « flicage » : « Je ne veux pas surveiller les gens, je veux juste des chiffres sur lesquels tout le monde est d'accord. »

## 🖤 Chapeau Noir — Risques & Critique

- Fraude au pointage : un employé peut pointer pour un collègue absent si le pointage n'est pas personnel et vérifié.
- Rejet par les employés si l'outil est vécu comme de la surveillance permanente (et risque juridique au regard de la loi n° 2008-12 sur les données personnelles).
- Coupures d'électricité et réseau instable : un pointage qui échoue au mauvais moment recrée des litiges.

## 💛 Chapeau Jaune — Optimisme & Valeur

- Passer de 3-4 jours à moins d'une journée pour préparer les éléments de paie libère du temps RH pour le recrutement et la formation.
- Une source de vérité partagée (employé, chef d'équipe, RH) met fin aux contestations sans preuve et apaise le climat social.
- Les employés ont déjà un smartphone et utilisent WhatsApp au quotidien : pas de matériel à acheter, contrairement à une pointeuse biométrique.

## 💚 Chapeau Vert — Créativité & Idées

- Et si l'employé pointait depuis son propre téléphone, avec une vérification du lieu uniquement au moment du pointage ?
- Et si un code QR affiché à l'accueil de chaque site servait de preuve de présence sur place ?
- Et si chaque employé recevait un récapitulatif de ses heures et pouvait contester en joignant un justificatif (bon d'intervention, photo) ?

## 💙 Chapeau Bleu — Processus & Organisation

- Valider le HMW définitif avec ces insights, puis construire le VPC (docs/vpc.md) en traçant chaque élément à un chapeau.
- Transformer le Chapeau Noir en contraintes MVP et en hypothèses à tester dès la S3.
- Définir une Métrique Nord mesurable en démo S6 : le délai de clôture des éléments de paie.

## 🔵 Synthèse Chapeau Bleu

**HMW révisé :** Comment pourrions-nous permettre à la responsable RH d'une PME dakaroise multi-sites d'obtenir chaque jour, sans ressaisie, une preuve de présence fiable et acceptée par chaque employé — au bureau comme en mission — afin de clôturer les éléments de paie en moins d'une journée et sans contestation ?

**Risques prioritaires :** fraude au pointage (pointer pour un collègue) / rejet de l'outil perçu comme de la surveillance

**Question ouverte :** Comment prouver la présence d'un technicien chez un client sans suivre sa position en continu ?
