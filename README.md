# GET409 — Systeme-Pointage

> Plateforme de gestion du pointage (présences, retards, heures supplémentaires) pour les entreprises au Sénégal.
> Module GET 409 — Atelier IA · Swiss UMEF University, Campus de Dakar · 2025-2026 · Séances 1-2 (Empathize → Define → Ideate)

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

### ✅ HMW définitif (S2)

> **Comment pourrions-nous permettre à la responsable RH d'une PME dakaroise multi-sites d'obtenir chaque jour, sans ressaisie, une preuve de présence fiable et acceptée par chaque employé — au bureau comme en mission — afin de clôturer les éléments de paie en moins d'une journée et sans contestation ?**

Détail et justification : [docs/hmw-definitif.md](./docs/hmw-definitif.md) · Alignement avec le sprint S3 : [docs/hmw-alignement.md](./docs/hmw-alignement.md)

<details>
<summary>HMW draft S1</summary>

> Comment pourrions-nous aider la responsable RH d'une entreprise dakaroise multi-sites à disposer de présences fiables et vérifiables de tous ses employés, au bureau comme sur le terrain, afin de préparer la paie sans ressaisie ni litiges en fin de mois ?

Les 5 formulations étudiées en S1 : [hmw.md](./hmw.md)
</details>

## Séance 2 — Idéation, VPC et HMW définitif

### Value Proposition Canvas (résumé)

| 👤 Profil client — Ndèye Fatou (RH de PME multi-sites) | 💡 Proposition de valeur — Systeme-Pointage |
|---|---|
| **Jobs :** savoir chaque jour qui est présent (3 sites + terrain) ; consolider les présences pour la paie ; compter juste les heures sup ; répondre aux contestations avec des preuves | **Produits & services :** pointage depuis le téléphone vérifié au moment du pointage ; code QR de site ; tableau de bord RH du jour ; récapitulatif mensuel + historique employé |
| **Pains :** épuisement et peur de l'erreur de paie ; pointage pour un collègue ; terrain invérifiable ; peur de la surveillance | **Pain relievers :** récapitulatif automatique ; pointage personnel vérifié ; pointage « mission » validé ; vérification ponctuelle + charte d'usage |
| **Gains :** paie en moins d'une journée ; source de vérité partagée ; aucun matériel à acheter ; temps RH libéré | **Gain creators :** export prêt pour la paie ; historique partagé + correction tracée ; smartphones existants ; tableau de bord du jour |

**FIT :** chaque Pain a son Pain Reliever — FIT validé ([docs/vpc.md](./docs/vpc.md)) · PDF : [livrables/GET409-Systeme-Pointage_VPC_S2.pdf](./livrables/GET409-Systeme-Pointage_VPC_S2.pdf)

### Backlog S3 (user stories MUST)

1. **US-01** — Pointage arrivée/départ vérifié depuis le téléphone
2. **US-03** — Récapitulatif mensuel + export pour la paie
3. **US-02** — Tableau de bord RH du jour

Détail : [docs/backlog-s3.md](./docs/backlog-s3.md)

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

## Livrables S2

- [x] Value Proposition Canvas (6 blocs) — [docs/vpc.md](./docs/vpc.md) · PDF dans [livrables/](./livrables/GET409-Systeme-Pointage_VPC_S2.pdf)
- [x] HMW définitif — [docs/hmw-definitif.md](./docs/hmw-definitif.md) (repris en tête de ce README)
- [x] Journal de Prompts — 5 prompts P1 → P5 notés /5 — [journal-prompts.md](./journal-prompts.md)
- [x] 6 Chapeaux de Bono — [docs/chapeaux-bono.md](./docs/chapeaux-bono.md)
- [x] Contraintes MVP — [docs/contraintes-mvp.md](./docs/contraintes-mvp.md)
- [x] Hypothèses de validation — [docs/hypotheses-validation.md](./docs/hypotheses-validation.md)
- [x] Métriques de succès — [docs/metriques-succes.md](./docs/metriques-succes.md)
- [x] Traçabilité 6 Chapeaux → VPC — [docs/vpc-connections.md](./docs/vpc-connections.md)
- [x] Backlog S3 — [docs/backlog-s3.md](./docs/backlog-s3.md)
- [x] Pitch proposition de valeur (draft) — [docs/pitch-vpc-draft.md](./docs/pitch-vpc-draft.md)
- [x] Alignement HMW / backlog — [docs/hmw-alignement.md](./docs/hmw-alignement.md)
- [x] Préparation jury — [docs/hmw-jury.md](./docs/hmw-jury.md)
- [ ] Script démo S6 (docs/hmw-demo.md) — après la construction du MVP

## Workflow Git

Chaque livrable est préparé sur sa propre branche, puis fusionné dans `main` par une Pull Request relue par un membre de l'équipe.

| Livrable | Branche | Contenu |
|---|---|---|
| Livrable 1 (S1) | `feature/livrable1` | Fiche d'équipe, carte d'empathie, HMW draft, guide d'interview |
| Livrable 2 (S2) | `feature/livrable2` | 6 Chapeaux, VPC, HMW définitif, contraintes, hypothèses, métriques, backlog S3, journal de prompts |
| Livrable 3 (S3) | `feature/livrable3` | à venir |

Convention :

1. Créer la branche depuis `main` : `feature/livrableN`.
2. Un commit par livrable, avec un message explicite (`feat(SN): …` / `docs: …`).
3. Ouvrir une Pull Request `feature/livrableN` → `main`, la faire relire, puis fusionner.
4. Marquer la version rendue avec un tag `livrable-N`.

## Organisation du dépôt

```
GET409-Systeme-Pointage/
├── README.md               ← carte d'identité du projet (HMW définitif)
├── fiche-equipe.md         ← S1 · fiche d'équipe
├── carte-empathie.md       ← S1 · carte d'empathie
├── hmw.md                  ← S1 · HMW draft (5 formulations)
├── journal-prompts.md      ← S1 + S2 · journal de prompts
├── docs/
│   ├── cadrage-defi.md         ← S1 · problèmes du secteur
│   ├── guide-interview.md      ← S1 · guide + notes d'interview
│   ├── chapeaux-bono.md        ← S2 · 6 Chapeaux
│   ├── contraintes-mvp.md      ← S2 · contraintes non négociables
│   ├── hypotheses-validation.md← S2 · ce qu'on valide en S3
│   ├── metriques-succes.md     ← S2 · ce qu'on mesure en S6
│   ├── vpc.md                  ← S2 · Value Proposition Canvas
│   ├── vpc-connections.md      ← S2 · traçabilité Chapeaux → VPC
│   ├── backlog-s3.md           ← S2 · user stories S3
│   ├── pitch-vpc-draft.md      ← S2 · bloc pitch soutenance
│   ├── hmw-definitif.md        ← S2 · HMW définitif
│   ├── hmw-alignement.md       ← S2 · filtre sprint S3
│   └── hmw-jury.md             ← S2 · préparation soutenance
└── livrables/              ← PDF (fiche d'équipe, carte d'empathie, VPC)
```

## Prochaines étapes

- **S3** — Construction des agents IA (livrable 3).
- **S4** — Prototype MVP avec Bolt.new.
