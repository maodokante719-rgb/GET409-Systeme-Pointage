## Préparation Jury — HMW — Systeme-Pointage

> Livrable S2 · Prompt P-HMW-JURY · Inputs : [hmw-definitif.md](./hmw-definitif.md) + [vpc-connections.md](./vpc-connections.md)
> Les réponses renvoient aux fichiers du dépôt ; les résultats chiffrés seront ajoutés après la démo S6.

### HMW Définitif

"Comment pourrions-nous permettre à la responsable RH d'une PME dakaroise multi-sites d'obtenir chaque jour, sans ressaisie, une preuve de présence fiable et acceptée par chaque employé — au bureau comme en mission — afin de clôturer les éléments de paie en moins d'une journée et sans contestation ?"

### Les 5 Questions Probables

#### Question 1

**Le jury demande :** « Pourquoi ne pas simplement installer une pointeuse biométrique ? »
**Ce qu'il teste :** la connaissance des contraintes du persona.
**Votre réponse :** Une pointeuse est fixe : elle ne couvre ni les sites distants ni les techniciens chez les clients, qui sont justement la source des litiges. Elle coûte cher pour une PME et dépend de l'électricité. Notre contrainte C1 impose de fonctionner sur les téléphones existants.
**Fichier à ouvrir :** docs/contraintes-mvp.md — Contrainte 1

#### Question 2

**Le jury demande :** « Comment empêchez-vous un employé de pointer pour un collègue ? »
**Ce qu'il teste :** la robustesse de la solution face au risque principal.
**Votre réponse :** C'est notre premier risque du Chapeau Noir. Le pointage est personnel et vérifié sur le lieu (zone du site ou code QR). Nous le testons en S3 avec une tentative de fraude simulée : c'est l'hypothèse critique C3.
**Fichier à ouvrir :** docs/hypotheses-validation.md — Hypothèse C3

#### Question 3

**Le jury demande :** « N'est-ce pas un outil de surveillance des employés ? »
**Ce qu'il teste :** la dimension éthique et légale.
**Votre réponse :** Non : la position est vérifiée uniquement au moment du pointage, jamais en continu (contrainte C2). Les données personnelles sont traitées dans le cadre de la loi sénégalaise n° 2008-12, et une charte d'usage est présentée aux employés. L'employé voit ses propres pointages et peut demander une correction.
**Fichier à ouvrir :** docs/contraintes-mvp.md — Contrainte 2 · carte-empathie.md — Note du Responsable Impact

#### Question 4

**Le jury demande :** « Comment saurez-vous que votre MVP fonctionne ? »
**Ce qu'il teste :** la capacité à mesurer l'impact.
**Votre réponse :** Notre Métrique Nord est le temps de clôture des éléments de paie : de 3-4 jours aujourd'hui à moins d'une journée sur un pilote de 30 jours. Nous suivons aussi le taux de pointage et le nombre de contestations.
**Fichier à ouvrir :** docs/metriques-succes.md — Métrique Nord

#### Question 5

**Le jury demande :** « Pourquoi cette fonctionnalité et pas une autre ? »
**Ce qu'il teste :** la traçabilité des décisions produit.
**Votre réponse :** Chaque user story MUST répond à un Pain Reliever du VPC, lui-même relié à un chapeau. Exemple : US-01 (pointage vérifié) → Pain Reliever « pointage personnel vérifié » → Pain « pointage pour un collègue » → Chapeau Noir.
**Fichier à ouvrir :** docs/backlog-s3.md → docs/vpc.md → docs/vpc-connections.md

### Les 2 Questions Pièges

#### Piège 1

**Le jury demande :** « Votre persona est fictif. Qu'est-ce qui prouve que le problème existe ? »
**Pourquoi c'est un piège :** le jury teste l'honnêteté méthodologique.
**Stratégie de réponse :** reconnaître que l'interview S1 était un jeu de rôle, montrer que c'est documenté, et présenter les entretiens réels prévus.
**Phrase d'ouverture :** « Vous avez raison, notre interview S1 était simulée et nous l'avons indiqué dans nos livrables. C'est pourquoi notre première hypothèse critique, C1, est de valider le problème auprès de 5 RH réelles dès la S3… »

#### Piège 2

**Le jury demande :** « Et si les employés n'ont pas de smartphone ou pas de données mobiles ? »
**Pourquoi c'est un piège :** le jury cherche la population exclue par la solution.
**Stratégie de réponse :** montrer que le risque est identifié et qu'une alternative existe.
**Phrase d'ouverture :** « C'est notre hypothèse critique C2 : nous la mesurons avec un questionnaire d'équipement. Pour les employés non équipés, le code QR du site ou la validation par le chef de site servent d'alternative… »

### Réflexe en soutenance

« Bonne question — laissez-moi ouvrir le fichier correspondant dans notre dépôt GitHub pour vous montrer comment nous l'avons documenté. »
