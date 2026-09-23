# Journal de Prompts — GET409-Systeme-Pointage

> Tenu par le **Master Prompt Engineer**. Chaque prompt de la bibliothèque S1 est adapté au contexte de l'équipe (tous les `[crochets]` remplacés).
> Outil utilisé : Claude (claude.ai).

| # | Prompt | Technique | Objectif | Résultat |
|---|---|---|---|---|
| S1 | Découverte | Zero-shot contextualisé | Identifier 3 problèmes du secteur | [docs/cadrage-defi.md](./docs/cadrage-defi.md) |
| S2 | Interview IA | Rôle + format imposé | Générer le guide d'interview d'empathie | [docs/guide-interview.md](./docs/guide-interview.md) |
| S3 | Générateur de HMW | Rôle + contraintes | Formuler 5 énoncés « Comment pourrions-nous… ? » | [hmw.md](./hmw.md) |
| S4 | Carte d'empathie | Markdown prompting | Produire la carte d'empathie au format strict | [carte-empathie.md](./carte-empathie.md) |

---

## Prompt S1 — Découverte

```text
Tu es un expert en gestion des ressources humaines dans les entreprises
(PME) au Sénégal.
Identifie les 3 principaux problèmes que rencontrent les responsables RH et
directions d'entreprises dans la gestion des présences de leurs employés
(personnel de bureau et équipes terrain) à Dakar, dans un contexte
d'entreprises multi-sites, d'employés en mission chez les clients,
d'émargement papier et WhatsApp, d'embouteillages et de coupures
d'électricité ponctuelles.
Pour chaque problème, indique :
- La cause principale
- L'impact sur la vie quotidienne
- Une piste de solution technologique accessible
```

**Relecture critique :** aucune statistique non vérifiée n'est conservée dans le livrable (risque d'hallucination) ; les problèmes sont formulés comme des situations typiques à confirmer sur le terrain.

## Prompt S2 — Guide d'interview

```text
Tu es un UX Researcher spécialisé dans les usages numériques en Afrique de l'Ouest.
Je dois interviewer une responsable RH d'une PME de services qui vit à
Dakar (siège au Plateau) et fait face au problème suivant :
les présences des employés sont relevées sur des feuilles d'émargement sur
trois sites et par WhatsApp pour les techniciens terrain, ce qui rend la paie
lente et contestée par les employés.
Génère un guide d'interview d'empathie avec :
1. 3 questions d'ouverture (briser la glace)
2. 5 questions d'exploration en profondeur (utilisant 'Pourquoi ?' et 'Racontez-moi...')
3. 2 questions sur les aspirations et les gains attendus
Format : questions numérotées, courtes, sans jargon technique.
```

**Relecture critique :** vérification qu'aucune question n'est fermée (oui/non) ni ne suggère une solution (pas de « Aimeriez-vous une application ? ») ; ajout d'une question sur ce qui a déjà été essayé.

## Prompt S3 — Générateur de HMW

```text
Tu es un facilitateur en Design Thinking.
Voici les observations clés de notre interview avec une responsable RH d'une
entreprise multi-sites à Dakar :
Observation 1 : Elle recompte à la main les feuilles d'émargement de trois
sites chaque fin de mois.
Observation 2 : Les techniciens terrain contestent régulièrement les journées
ou retards qui leur sont retenus ("j'étais chez le client").
Observation 3 : Certains employés signent pour des collègues absents, et
personne ne peut le vérifier sur les sites distants.
La frustration principale identifiée est :
elle n'a aucune donnée de présence fiable et partagée, ce qui rend la paie
lente, contestable et source de conflits.
Génère 5 énoncés 'Comment pourrions-nous...' (HMW) qui reformulent cette
frustration en opportunité de conception.
Critères : ni trop vague, ni trop précis, ne propose pas encore de solution.
Format : liste numérotée, 1 phrase par énoncé.
```

**Relecture critique :** vérification qu'aucun énoncé n'impose une solution (pas de « application », « QR code », « biométrie »). HMW n°1 retenu (voir justification dans [hmw.md](./hmw.md)).

## Prompt S4 — Carte d'empathie (livrable final)

```markdown
# ROLE
Tu es un UX Researcher expert en Design Thinking pour des projets d'innovation
sociale en Afrique.

## PERSONA DE NOTRE EQUIPE
- Prénom, âge, profession : Ndèye Fatou Sarr, 39 ans, responsable RH
- Localisation : Dakar (siège au Plateau), Sénégal — PME de services, 3 sites
  + techniciens en intervention chez les clients
- Problème principal : présences notées sur feuilles papier et WhatsApp puis
  ressaisies dans Excel ; paie lente, retenues et heures sup contestées
- Equipement digital : smartphone Android, ordinateur portable, Excel, WhatsApp
- Revenus approximatifs : cadre salariée d'une PME
- Contexte familial : mariée, 2 enfants ; trajets entre le siège et les sites

## OBSERVATIONS DE NOS INTERVIEWS
- Ce qu'elle a dit : « Chaque fin de mois, je passe mes soirées à recompter
  les feuilles de présence. Et après, un technicien vient me dire qu'on lui a
  retiré une journée alors qu'il était chez un client. »
- Ce qu'elle a fait : elle photographie les feuilles, reçoit celles des autres
  sites et les messages des techniciens par WhatsApp, puis ressaisit tout dans Excel.
- Emotion principale détectée : épuisement et anxiété

## TACHE
Génère la Carte d'Empathie complète.

## FORMAT DE SORTIE STRICT
### 1. Ce qu'il/elle PENSE ET RESSENT
- [Préoccupation profonde 1]
- [Préoccupation profonde 2]
- [Aspiration secrète]
### 2. Ce qu'il/elle VOIT
- [Élément environnement 1]
- [Élément environnement 2]
### 3. Ce qu'il/elle ENTEND
- [Influence sociale 1]
- [Influence sociale 2]
### 4. Ce qu'il/elle DIT ET FAIT
- [Comportement observable 1]
- [Citation directe]
### 5. FRUSTRATIONS (Pains)
- [Douleur principale]
- [Obstacle majeur]
### 6. ASPIRATIONS (Gains)
- [Résultat désiré 1]
- [Besoin profond]
```

**Relecture critique :** sortie complétée par l'équipe (tableau du persona, point de vue du directeur et des équipes terrain) et ajout d'une note éthique par le Responsable Impact.

---

## Leçons retenues

1. Un prompt contextualisé (lieu, utilisateur, contraintes locales) donne des réponses bien plus exploitables qu'un prompt vague.
2. Il faut toujours relire : l'IA peut avancer des chiffres non vérifiés ou glisser une solution dans un HMW.
3. Le format Markdown strict (S4) produit un livrable directement déposable sur GitHub.

---

# Séance 2 — Journal de Prompts (5 prompts métier)

> Format imposé par le cours (S2, diapo 14) : technique, prompt exact, résumé de la réponse, note /5 avec justification, itération.
> Outil : Claude. Tenu par le Master Prompt Engineer (Oluwadara Emmanuel Ebeh).
> Les réponses ont été générées avec Claude pendant la préparation des livrables S2 ; les notes /5 sont l'évaluation de l'équipe. Si un prompt obtient moins de 3/5 en le rejouant en séance, documenter la reformulation dans la colonne Itération.

| # | Technique | Objectif | Note |
|---|---|---|---|
| P1 | Zero-Shot | 3 principaux problèmes du persona | v1 4/5 → v2 5/5 (itération) |
| P2 | Zero-Shot | 5 idées de fonctionnalités pour le MVP | 4/5 |
| P3 | Few-Shot | Compléter un 3e couple Défi → Solution | 4/5 |
| P4 | Chain-of-Thought | Cause → obstacle → solution | 5/5 |
| P5 | Libre | Affiner le HMW définitif (P-HMW) | 5/5 |

## P1 — Zero-Shot

**Prompt envoyé :**

```text
Tu es consultant en gestion des ressources humaines pour les PME au Sénégal.
Identifie les 3 principaux problèmes de Ndèye Fatou Sarr, responsable RH d'une
PME de services à Dakar (3 sites + techniciens en intervention chez les clients,
environ 70 employés), dans la gestion des présences de ses employés, et propose
une piste de solution numérique pour chacun.
Réponds sous forme de liste numérotée, en français.
```

**Réponse IA (résumé) :** (1) émargement papier non fiable et signatures pour un collègue ; (2) consolidation manuelle de la paie sur plusieurs jours ; (3) présence des techniciens terrain invérifiable. Pistes : pointage mobile, calcul automatique, pointage lié à la mission.
**Note : 4/5** — pertinent et ancré dans le persona ; les pistes restent générales et doivent être confrontées à de vraies RH (hypothèse C1).
**Itération :** oui — la réponse v1 était une liste difficile à réutiliser et ses pistes restaient générales. P1 a été rejoué avec un format de sortie contraint (tableau), comme le propose le cours pour approfondir le Zero-Shot. Voir P1 v2 ci-dessous.

### P1 v2 — Zero-Shot · format tableau (itération)

**Ce qui a changé :** format de sortie imposé (tableau à 5 colonnes), contrainte éthique ajoutée (pas de suivi continu), et une colonne « hypothèse à valider » pour relier chaque problème à la S3.

**Prompt envoyé :**

```text
Tu es consultant en gestion des ressources humaines pour les PME au Sénégal.
Identifie les 3 principaux problèmes de Ndèye Fatou Sarr, responsable RH d'une
PME de services à Dakar (3 sites + techniciens en intervention chez les clients,
environ 70 employés), dans la gestion des présences de ses employés.
Contrainte : aucune solution ne doit reposer sur un suivi GPS en continu.
Réponds uniquement par un tableau Markdown à 5 colonnes :
Problème | Cause principale | Impact pour la RH | Piste numérique | Hypothèse à valider en S3
Une ligne par problème, 15 mots maximum par cellule, en français.
```

**Réponse IA (résumé) :**

| Problème | Cause principale | Impact pour la RH | Piste numérique | Hypothèse à valider en S3 |
|---|---|---|---|---|
| Émargement non fiable | Feuille papier signée sans contrôle, parfois pour un collègue | Aucune preuve en cas de litige | Pointage personnel vérifié sur le lieu au moment du pointage | Les employés acceptent de pointer avec leur téléphone |
| Consolidation manuelle | Feuilles des sites reçues en photo WhatsApp, ressaisie Excel | 3 à 4 jours par mois, erreurs de paie | Récapitulatif mensuel calculé et exporté automatiquement | L'export convient au logiciel ou au tableur de paie |
| Terrain invérifiable | Techniciens chez les clients, simple message WhatsApp | Contestations des retenues | Pointage « mission » validé par le chef d'équipe | Le chef d'équipe valide dans la journée |

**Note : 5/5** — directement réutilisable : chaque ligne relie un problème à une user story (US-01, US-03, US-05) et à une hypothèse testable ; la contrainte anti-surveillance est respectée.
**Itération :** non nécessaire. Le tableau a servi de base à [docs/hypotheses-validation.md](./docs/hypotheses-validation.md) et au backlog S3.
**Leçon :** à prompt identique, imposer un format de sortie plus contraignant produit un livrable plus exploitable (v1 4/5 → v2 5/5).

## P2 — Zero-Shot

**Prompt envoyé :**

```text
Tu es product manager spécialisé dans les MVP pour les PME d'Afrique de l'Ouest.
Notre persona : Ndèye Fatou Sarr, responsable RH d'une PME de services à Dakar,
3 sites + techniciens chez les clients, employés équipés de smartphones,
coupures d'électricité fréquentes.
Notre HMW : "Comment pourrions-nous permettre à la responsable RH d'une PME dakaroise multi-sites d'obtenir chaque jour, sans ressaisie, une preuve de présence fiable et acceptée par chaque employé — au bureau comme en mission — afin de clôturer les éléments de paie en moins d'une journée et sans contestation ?"
Propose 5 idées de fonctionnalités pour notre MVP. Pour chacune : 1 phrase de
description et le problème du persona qu'elle résout.
Réponds sous forme de tableau, en français.
```

**Réponse IA (résumé) :** pointage mobile vérifié par zone, code QR de site, tableau de bord du jour, récapitulatif mensuel exportable, historique employé avec demande de correction.
**Note : 4/5** — idées directement reliées aux douleurs du persona ; il manquait l'alternative pour les employés sans smartphone.
**Itération :** non nécessaire (≥ 3/5) ; l'alternative pour les employés sans smartphone a été ajoutée par l'équipe dans les contraintes (C5) et les hypothèses (C2). Les 5 idées ont alimenté le Chapeau Vert et le backlog S3.

## P3 — Few-Shot

**Prompt envoyé :**

```text
Tu es ingénieur produit spécialisé dans les outils RH pour les PME d'Afrique de l'Ouest.
Voici des exemples de défis et leurs solutions :

DÉFI : Les employés signent la feuille d'émargement pour un collègue absent.
SOLUTION : Pointage personnel depuis le téléphone, avec vérification du lieu au
moment du pointage.

DÉFI : La RH passe 3 à 4 jours par mois à ressaisir les présences dans Excel.
SOLUTION : Calcul automatique du récapitulatif mensuel à partir des pointages,
export prêt pour la paie.

DÉFI : Les techniciens en intervention chez un client ne peuvent pas prouver
leur présence et contestent les journées retenues.
SOLUTION :
```

**Réponse IA (résumé) :** « Pointage "mission" à l'arrivée chez le client, rattaché à l'ordre d'intervention et validé par le chef d'équipe, sans suivi de position en continu. »
**Note : 4/5** — le format Défi → Solution est parfaitement imité et la solution respecte la contrainte anti-surveillance ; la validation par le chef d'équipe reste à tester sur le terrain.
**Itération :** non nécessaire. Réponse reprise dans le VPC (Pain Reliever « pointage mission ») et le backlog (US-05).

## P4 — Chain-of-Thought

**Prompt envoyé :**

```text
Tu es un expert en gestion des ressources humaines en Afrique de l'Ouest.
Analyse le problème suivant : dans les PME multi-sites de Dakar, les présences
des employés sont relevées sur papier et par WhatsApp, ce qui rend la paie
lente, contestable et source de conflits.
Réfléchis étape par étape :
Étape 1 : Identifie la cause principale du problème dans le contexte de Dakar.
Étape 2 : Décris l'obstacle principal qui empêche une solution classique
(pointeuse biométrique, logiciel RH de grand groupe) de fonctionner.
Étape 3 : Propose une solution technologique accessible à la responsable RH
d'une PME.
Développe chaque étape avant de conclure.
```

**Réponse IA (résumé) :** Étape 1 — aucune preuve de présence individuelle et vérifiable, surtout hors du siège. Étape 2 — les pointeuses sont fixes, coûteuses, dépendantes de l'électricité et inutiles pour le terrain ; les logiciels RH sont trop lourds pour une PME. Étape 3 — pointage sur les téléphones existants, vérifié au moment du pointage, avec récapitulatif mensuel automatique.
**Note : 5/5** — raisonnement structuré, vérifiable à chaque étape, sans chiffre inventé ; il a directement nourri les contraintes C1 et C5.
**Itération :** non nécessaire.

## P5 — Libre (P-HMW : HMW définitif)

**Prompt envoyé :**

```text
Tu es un expert en Design Thinking et en formulation de problématiques pour des
projets d'innovation sociale en Afrique de l'Ouest.
Voici notre travail de S2 :
Notre HMW draft S1 :
"Comment pourrions-nous aider la responsable RH d'une entreprise dakaroise
multi-sites à disposer de présences fiables et vérifiables de tous ses employés,
au bureau comme sur le terrain, afin de préparer la paie sans ressaisie ni
litiges en fin de mois ?"
Insights clés des 6 Chapeaux de Bono :
- Chapeau Blanc : la consolidation des présences prend 3 à 4 jours par mois.
- Chapeau Noir : fraude au pointage et rejet d'un outil perçu comme de la surveillance.
- Chapeau Bleu : comment prouver la présence d'un technicien chez un client sans
  suivre sa position en continu ?
FIT Check du VPC :
- Pain principal couvert : pointage pour un collègue → pointage personnel vérifié
- Pain secondaire couvert : terrain invérifiable → pointage « mission » validé
Notre persona : Ndèye Fatou Sarr · 39 ans · responsable RH · PME de services,
Dakar Plateau · smartphone Android
À partir de ces éléments, propose 3 versions améliorées de notre HMW définitif.
Pour chaque version, indique :
- En quoi elle est plus précise que le draft S1
- Quel risque du Chapeau Noir elle intègre
- Si elle est trop précise / trop large / bien calibrée
Puis recommande la version la plus solide pour guider notre prototypage en S3.
FORMAT DE SORTIE STRICT — Markdown pur, sans introduction, sans conclusion.
```

**Réponse IA (résumé) :** 3 versions — A (bien calibrée), B (trop précise, limitée aux techniciens), C (trop large). Version recommandée : A.
**Note : 5/5** — les 3 versions sont nettement différentes, l'évaluation est justifiée, et la version A passe les 3 questions de validation du cours.
**Itération :** non nécessaire. Résultat commité dans [docs/hmw-definitif.md](./docs/hmw-definitif.md).

---

## Prompts de la séquence S2 du cours (notés /5)

| Prompt du cours | Fichier produit | Note | Commentaire |
|---|---|---|---|
| P-CHAPEAUX (étape 01) | [docs/chapeaux-bono.md](./docs/chapeaux-bono.md) | 4/5 | 3 insights par chapeau ; insights sans verbatim retirés à la relecture |
| P-CHAPEAUX-CONTRAINTES (étape 02) | [docs/contraintes-mvp.md](./docs/contraintes-mvp.md) | 5/5 | 5 contraintes formulées en critères DOIT / NE DOIT PAS |
| P-CHAPEAUX-HYPOTHESES (étape 03) | [docs/hypotheses-validation.md](./docs/hypotheses-validation.md) | 4/5 | Hypothèses classées par criticité ; délais S3 à confirmer par l'équipe |
| P-CHAPEAUX-METRIQUES (étape 04) | [docs/metriques-succes.md](./docs/metriques-succes.md) | 4/5 | Métrique Nord mesurable sans technologie ; cibles à ajuster après C1 |
| P-VPC-1 + P-VPC-2 (étape 05) | [docs/vpc.md](./docs/vpc.md) | 5/5 | Chaque Pain a son Pain Reliever — FIT validé |
| P-VPC-CONNECTIONS (étape 06) | [docs/vpc-connections.md](./docs/vpc-connections.md) | 4/5 | 2 éléments non tracés (≤ 2, conforme) |
| P-VPC-BACKLOG (étape 07) | [docs/backlog-s3.md](./docs/backlog-s3.md) | 5/5 | 3 US MUST (entre 2 et 4, conforme) |
| P-VPC-PITCH | [docs/pitch-vpc-draft.md](./docs/pitch-vpc-draft.md) | 4/5 | Chiffres présentés comme objectifs, pas comme résultats |
| P-HMW-ALIGNEMENT | [docs/hmw-alignement.md](./docs/hmw-alignement.md) | 5/5 | Ordre de construction S3 : US-01, US-03, US-02 |
| P-HMW-JURY | [docs/hmw-jury.md](./docs/hmw-jury.md) | 4/5 | 5 questions + 2 pièges, réponses traçables dans le dépôt |
| P-HMW-DEMO | [docs/hmw-demo.md](./docs/hmw-demo.md) | 4/5 | Version S2 prévisionnelle : script complet, métriques réelles à compléter en S6 |

## Leçons retenues (S2)

1. **Zero-Shot** : la formule Rôle + Contexte + Tâche + Format du cours suffit à obtenir une réponse exploitable (P1, P2 : 4/5) ; imposer un format de sortie contraint (tableau) la rend directement réutilisable (P1 v2 : 5/5).
2. **Few-Shot** : deux exemples suffisent pour imposer le format et le ton de la réponse (P3).
3. **Chain-of-Thought** : le raisonnement étape par étape donne une analyse vérifiable, sans chiffre inventé (P4).
4. Relire chaque sortie avec la question « est-ce qu'on l'a entendu en interview ? » évite d'intégrer des idées hors sujet.
