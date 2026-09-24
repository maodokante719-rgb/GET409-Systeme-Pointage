# L4 — Réflexion éthique · Systeme-Pointage (S3)

> Livrable L4 · Version Word déposée sur e-Academy : [livrables/GET409-Systeme-Pointage_L4_Reflexion_Ethique_S3.docx](../../livrables/GET409-Systeme-Pointage_L4_Reflexion_Ethique_S3.docx)
> Rédigée à partir du prompt Chain-of-Thought P9 du [journal de prompts](../../journal-prompts.md#p9--chain-of-thought--réflexion-éthique-sur-notre-agent), puis resserrée pour tenir dans le format du modèle L4 du cours.

| | |
|---|---|
| **Équipe** | Systeme-Pointage |
| **Projet** | Agent Rapport d'Anomalies (Dify) |
| **Persona** | Ndèye Fatou Sarr · 39 ans · Responsable RH · Dakar Plateau (3 sites + terrain) · Smartphone Android + PC portable · Abonnement payé par l'entreprise |
| **Outil IA** | Dify.ai (workflow) — openai/gpt-oss-120b — GroqCloud |

## Contexte

Notre workflow Dify à deux agents aide Ndèye Fatou à préparer la paie : à partir d'un extrait de pointages, le Chercheur classe les anomalies (retard, absence, oubli de départ, hors zone, mission non validée, heures sup) et le Rédacteur produit un rapport avec des actions de vérification. Une erreur touche directement le salaire d'un employé : l'analyse CoT (P9 du L3) a retenu trois risques.

## Risque 1 — Retenue sur salaire injuste

| | |
|---|---|
| **Description** | Une règle ambiguë ou un pointage mal lu peut transformer une mission en « absence ». En test, un retard à 08h31 a été compté +21 min (depuis 08h10) au lieu de 31. Si le rapport part tel quel en paie, un technicien est pénalisé à tort : c'est la contestation que notre HMW veut supprimer. |
| **Garde-fou technique** | Le Chercheur n'invente rien et répond INSUFFISANT si des données manquent ; le Rédacteur ne formule que des vérifications et termine par un avertissement. En V2, les totaux sont calculés par l'application, le LLM ne fait que rédiger. |
| **Garde-fou organisationnel** | Aucune retenue sans validation de la RH ; l'employé peut contester avec justificatif sous 48 h (US-04), chaque correction est tracée. Les règles horaires sont validées par la direction. |

## Risque 2 — Données personnelles envoyées hors du Sénégal

| | |
|---|---|
| **Description** | Chaque exécution envoie à GroqCloud des noms, horaires et lieux de pointage d'employés qui n'en sont pas informés. Sans déclaration ni information, ce traitement ne respecte pas la loi n° 2008-12, et il renforce la peur d'être surveillé, déjà relevée en interview. |
| **Garde-fou technique** | Remplacer les noms par des matricules avant l'envoi (correspondance gardée dans l'application) ; transmettre seulement le statut « sur site / hors zone », jamais de coordonnées GPS. |
| **Garde-fou organisationnel** | Déclaration du traitement à la CDP, charte d'usage affichée et information des employés sur ce qui est envoyé à l'IA et pourquoi. |

## Risque 3 — Dépendance à un fournisseur gratuit

| | |
|---|---|
| **Description** | Pendant le TP, Kimi-K2 puis Llama-3.1-8b sont devenus inaccessibles sans préavis (erreur 404), et l'offre gratuite plafonne à 8 000 tokens/min. Si cela arrive la veille de la clôture de paie, Ndèye Fatou revient aux recomptes manuels. |
| **Garde-fou technique** | Configurer un modèle de repli dans Dify (gpt-oss-20b, testé et fonctionnel) et analyser site par site pour rester sous le quota ; le récapitulatif mensuel de l'application reste utilisable sans IA. |
| **Garde-fou organisationnel** | Le Tech Lead teste le workflow chaque début de mois et suit les annonces de Groq ; une procédure manuelle de secours est remise à la RH. |

## Recommandation finale

**→ Phase recommandée : Pilote contrôlé**

Un mois de paie sur l'agence de Pikine, noms pseudonymisés, chaque rapport comparé au recompte manuel de la RH. Passage au déploiement si au moins 95 % des anomalies sont correctes, aucune retenue appliquée sans validation humaine et moins de contestations qu'avec la feuille papier.
