# GET409 — Systeme-Pointage

> Plateforme de gestion du pointage (présences, retards, heures supplémentaires) pour les entreprises au Sénégal.
> Module GET 409 — Atelier IA · Swiss UMEF University, Campus de Dakar · 2025-2026 · Séance 1 (Empathize → Define)

## Notre équipe

| Prénom Nom | Rôle | GitHub | E-mail GitHub |
|---|---|---|---|
| Oumar Mbodou Seid | Chef de Produit (PM) | @SaidOmar2 | oumarseid22@gmail.com |
| Maodo Kanté | Dev Fullstack · Tech Lead | @maodokante719-rgb | Kantechangency@gmail.com |
| Oluwadara Emmanuel Ebeh | DevSecOps · Master Prompt Engineer · Dev UI (No-Code) · Responsable Impact | @manuelebeh | ebehemmanuel2003@gmail.com |

## Notre défi

- **Secteur :** Gestion d'entreprise / Ressources humaines — gestion des présences et du temps de travail des employés dans les entreprises (PME) de Dakar, Sénégal
- **Utilisateur cible :** la responsable RH d'une entreprise multi-sites (personnel de bureau + équipes terrain en mission chez les clients)
- **Problème en 1 phrase :** les présences sont relevées sur des feuilles d'émargement papier, par WhatsApp et dans Excel, ce qui rend la préparation de la paie lente, contestable et source de conflits.

### Énoncé HMW retenu (fil directeur du projet)

> **Comment pourrions-nous aider la responsable RH d'une entreprise dakaroise multi-sites à disposer de présences fiables et vérifiables de tous ses employés, au bureau comme sur le terrain, afin de préparer la paie sans ressaisie ni litiges en fin de mois ?**

Les 5 formulations étudiées et la justification du choix : [hmw.md](./hmw.md)

## Carte d'empathie (livrable obligatoire S1)

> Livrable obligatoire S1 · Généré avec le Prompt S4 (Carte d'Empathie Markdown) puis relu et corrigé par l'équipe.
> Sources : cadrage du défi (Prompt S1) + interview d'empathie simulée en jeu de rôle (Prompt S2, voir [docs/guide-interview.md](./docs/guide-interview.md)).
> Le persona est **fictif** : il synthétise des situations typiques du secteur, il ne décrit pas une personne réelle.

### Persona

| | |
|---|---|
| **Prénom, âge, profession** | Ndèye Fatou Sarr, 39 ans, responsable des ressources humaines |
| **Localisation** | Dakar (siège au Plateau), Sénégal — PME de services avec 3 sites (siège, agence de Pikine, dépôt de Diamniadio) et des techniciens en intervention chez les clients |
| **Effectif géré** | environ 70 employés : personnel administratif, techniciens terrain, agents de dépôt |
| **Problème principal** | Les présences sont relevées sur des feuilles d'émargement (une par site) et par messages WhatsApp pour les équipes terrain, puis ressaisies dans Excel : la préparation de la paie prend plusieurs jours et les retards, absences et heures supplémentaires sont souvent contestés. |
| **Équipement digital** | Smartphone Android, ordinateur portable, Excel, WhatsApp (groupes par site et par équipe), logiciel de paie basique |
| **Revenus approximatifs** | Cadre salariée, revenu mensuel moyen pour une PME dakaroise |
| **Contexte familial** | Mariée, 2 enfants scolarisés ; trajets entre le siège et les sites dans les embouteillages |

### Observations de l'interview

- **Ce qu'elle a dit :** « Chaque fin de mois, je passe mes soirées à recompter les feuilles de présence. Et après, un technicien vient me dire qu'on lui a retiré une journée alors qu'il était chez un client. »
- **Ce qu'elle a fait :** elle photographie les feuilles d'émargement, reçoit par WhatsApp celles des autres sites et les messages « je suis arrivé chez le client » des techniciens, puis ressaisit tout dans Excel.
- **Émotion principale détectée :** épuisement mêlé d'anxiété (peur de l'erreur de paie et du conflit avec les employés).

---

#### 1. Ce qu'elle PENSE ET RESSENT

- Elle a peur de se tromper dans la paie : une erreur coûte de l'argent à l'entreprise ou crée un conflit avec un employé.
- Elle se sent seule responsable de chiffres qu'elle ne peut pas vérifier : elle ne sait pas si une signature ou un message WhatsApp correspond à une vraie présence.
- Elle a l'impression de passer plus de temps à faire de la saisie qu'à faire son vrai métier (recrutement, formation, climat social).
- **Aspiration secrète :** être reconnue par la direction comme une responsable RH stratégique, pas comme « celle qui compte les signatures ».

#### 2. Ce qu'elle VOIT

- Trois feuilles d'émargement, dont celles des sites distants qui arrivent en retard, incomplètes ou en photo floue par WhatsApp.
- Des signatures ajoutées après coup, des heures d'arrivée arrondies, des cases vides pour les jours de mission ou de récupération.
- Des techniciens qui démarrent directement chez les clients et dont personne ne peut confirmer l'heure d'arrivée.
- Un fichier Excel qui grossit chaque mois, avec des formules que personne d'autre ne sait maintenir.

#### 3. Ce qu'elle ENTEND

- Le directeur général : « Pourquoi les heures supplémentaires ont encore augmenté ce mois-ci ? »
- Les techniciens : « J'étais en intervention chez le client, c'est pour ça que je n'ai pas signé. »
- Les employés du siège : « Tout le monde sait que certains signent pour les collègues absents. »
- Les collègues RH d'autres entreprises : « Une pointeuse biométrique coûte cher, elle ne couvre pas le terrain et tombe en panne à la première coupure d'électricité. »

#### 4. Ce qu'elle DIT ET FAIT

- Elle recompte à la main les jours de présence, retards et heures supplémentaires de chaque employé à la fin du mois.
- Elle relance les chefs de site et les chefs d'équipe un par un sur WhatsApp pour confirmer les présences.
- Elle garde des photos des feuilles et des captures WhatsApp sur son téléphone « au cas où » il y aurait une contestation.
- **Citation directe :** « Je ne veux pas surveiller les gens, je veux juste des chiffres sur lesquels tout le monde est d'accord. »

#### 5. FRUSTRATIONS (Pains)

- **Douleur principale :** 3 à 4 jours de ressaisie et de vérification chaque fin de mois, avec un risque d'erreur à chaque étape.
- **Obstacle majeur :** aucune preuve fiable de présence — la signature papier est facile à falsifier, et impossible à contrôler à distance sur les autres sites et sur le terrain.
- Des litiges réguliers avec les employés sur les retenues pour retard ou absence et sur les heures supplémentaires, qui abîment le climat social.
- Des outils coûteux ou inadaptés (pointeuses biométriques fixes et sensibles aux coupures, logiciels RH conçus pour les grands groupes).

#### 6. ASPIRATIONS (Gains)

- **Résultat désiré 1 :** voir en temps réel qui est présent, en retard, absent ou en mission, sur chaque site et sur le terrain, sans se déplacer.
- **Résultat désiré 2 :** obtenir automatiquement, en fin de mois, le total des heures travaillées, retards et heures supplémentaires par employé, prêt pour la paie.
- **Besoin profond :** une source de vérité unique, acceptée à la fois par la direction et par les employés, qui met fin aux contestations.
- Un outil simple, utilisable depuis un téléphone, qui respecte la vie privée des employés (pas de suivi permanent).

---

### Note du Responsable Impact (points de vigilance éthique)

- **Vie privée :** toute vérification de position doit se limiter au moment du pointage — aucun suivi GPS en continu, y compris pour les équipes terrain.
- **Données personnelles :** traiter les données des employés conformément à la loi sénégalaise n° 2008-12 sur la protection des données à caractère personnel (autorité de contrôle : CDP).
- **Équité :** prévoir un droit de correction et de justification (retard lié à une panne, une mission, un rendez-vous client, etc.) pour éviter qu'un outil de contrôle devienne un outil de sanction automatique.
- **Inclusion :** prévoir une alternative pour les employés sans smartphone ou sans connexion.

> Version fichier : [carte-empathie.md](./carte-empathie.md)

## Livrables S1

- [x] Fiche équipe — [fiche-equipe.md](./fiche-equipe.md) (version PDF pour e-Academy)
- [x] Dépôt GitHub public `GET409-Systeme-Pointage` + README initialisé
- [x] Carte d'empathie (4 quadrants + Pains & Gains) — [carte-empathie.md](./carte-empathie.md) (version PDF pour e-Academy)
- [x] Énoncé HMW — [hmw.md](./hmw.md)
- [x] Cadrage du défi (Prompt S1) — [docs/cadrage-defi.md](./docs/cadrage-defi.md)
- [x] Guide d'interview + notes d'interview (Prompt S2) — [docs/guide-interview.md](./docs/guide-interview.md)
- [x] Journal de prompts (S1 → S4) — [journal-prompts.md](./journal-prompts.md)

## Organisation du dépôt

```
GET409-Systeme-Pointage/
├── README.md              ← carte d'identité du projet
├── fiche-equipe.md        ← fiche d'équipe (livrable obligatoire)
├── carte-empathie.md      ← carte d'empathie (livrable obligatoire S1)
├── hmw.md                 ← énoncés « Comment pourrions-nous… ? »
├── journal-prompts.md     ← prompts utilisés et résultats
├── docs/
│   ├── cadrage-defi.md    ← Prompt S1 : 3 problèmes du secteur
│   └── guide-interview.md ← Prompt S2 : guide + notes d'interview
```

## Prochaines étapes

- **S2** — Idéation (6 chapeaux de Bono), Value Proposition Canvas, approfondissement du Prompt Engineering.
- **S3** — Construction des agents IA (livrable 3).
- **S4** — Prototype MVP avec Bolt.new.
