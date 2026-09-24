# Jeu de test — Agent Dify Systeme-Pointage (S3)

> Données **fictives** (noms et horaires inventés pour le test). Aucune donnée réelle d'employé n'est envoyée au modèle.
> Les 2 questions testent les 2 branches du SI/SINON (procédure S4 du cours).

## Question 1 — précise → branche ELSE (rapport complet)

À coller dans le champ « query » :

```text
Anomalies de pointage de l'agence de Pikine, semaine du 15 au 19 septembre 2026.
Données de pointage (employé ; date ; arrivée ; départ ; lieu) :
Moussa Fall ; 15/09 ; 08h04 ; 17h02 ; Pikine
Moussa Fall ; 16/09 ; 08h31 ; 17h05 ; Pikine
Moussa Fall ; 17/09 ; 08h02 ; — ; Pikine
Aïssatou Ba ; 15/09 ; 07h55 ; 19h10 ; Pikine
Aïssatou Ba ; 16/09 ; 07h58 ; 17h00 ; Pikine
Cheikh Ndiaye ; 15/09 ; 08h00 ; 17h00 ; Hors zone (Guédiawaye)
Cheikh Ndiaye ; 16/09 ; mission client (non validée par le chef d'équipe) ; 16h45 ; Mission
Cheikh Ndiaye ; 17/09 ; aucun pointage ; — ; —
```

**Résultat attendu (vérifié à la main)** : 6 anomalies.

| Employé | Date | Anomalie attendue | Détectée par l'agent |
|---|---|---|---|
| Moussa Fall | 16/09 | Retard (08h31) | ✅ |
| Moussa Fall | 17/09 | Oubli de départ | ✅ |
| Aïssatou Ba | 15/09 | Heures sup (départ 19h10) | ✅ |
| Cheikh Ndiaye | 15/09 | Hors zone (Guédiawaye) | ✅ |
| Cheikh Ndiaye | 16/09 | Mission non validée | ✅ |
| Cheikh Ndiaye | 17/09 | Absence | ✅ |

Faux positifs : 0 (les journées normales du 15/09 de Moussa Fall et du 16/09 d'Aïssatou Ba ne sont pas signalées).

## Question 2 — vague → branche IF (INSUFFISANT)

```text
Retards ?
```

**Résultat attendu** : `INSUFFISANT : …` sans passer par le Rédacteur.
