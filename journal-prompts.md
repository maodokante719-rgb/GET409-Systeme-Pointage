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
