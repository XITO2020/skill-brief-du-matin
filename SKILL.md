---
name: brief-du-matin
description: Prépare le brief du matin de Naim à partir de ce qui est déjà écrit (ETAT-COURANT, NAIM-INBOX, derniers journaux, prompts en attente du Second cerveau, sorties des tâches planifiées, agenda de la semaine) et le trie en trois paniers, urgent, à savoir, à ignorer, avec le rendez-vous ou la décision qui attend Naim aujourd'hui. N'envoie rien, ne modifie rien d'autre que le brief. Déclenche-le dès que Naim écrit « brief », « brief du matin », « qu'est-ce qui m'attend », « par quoi je commence », « résumé de la journée », ou au début d'une journée de travail. Candidat à une tâche planifiée quotidienne, sur décision de Naim.
---

# Brief du matin (pilier « Coordination »)

Source : vidéo v2 de `docs/solutions-second-brain/`. Principe : rendre le travail visible, puis efficace, puis
automatique, et seulement ensuite déléguer. On commence par lire, jamais par agir.

## Lire, dans cet ordre (tout est local)

1. `cortex/project-manager/ETAT-COURANT.md`. S'il date de plus de 7 jours, le dire en première ligne.
2. `cortex/project-manager/NAIM-INBOX.md` : les items non dépouillés.
3. Les journaux de la veille et du jour : `cortex/project-manager/journal/*/AAAA-MM-JJ.md`.
4. `_obsidian-vault/raw/prompts/` : les prompts en `statut: nouveau` ou `envoye-claude` sans livrable.
5. `cortex/project-manager/AGENDA_SEMAINE.md` s'il existe.
6. Les sorties récentes des tâches planifiées (radar, trading, etc.) dans le coffre ou les journaux.
7. Boîte mail : **seulement** si l'agent `agents/guichet-mail` tourne et que Naim l'a demandé. Jamais de lecture de
   Proton en direct, jamais d'envoi.

## Trier

- **Urgent** : ce qui bloque de l'argent entrant (tuveuxun, Dueria, Raisup), une date limite, une décision que seul Naim
  peut prendre.
- **À savoir** : état des chantiers, résultats des tâches planifiées.
- **À ignorer aujourd'hui** : ce qui peut attendre, dit franchement.

Rythme de Naim (feedback_wellbeing_guardrails, révisé 14/10/2026) : ~12 h par jour, 7 jours sur 7, par choix.
Calibrer le brief sur cette journée-là ; si les urgences dépassent même 12 h, le dire et classer.

## Livrable

`_obsidian-vault/outputs/AAAA-MM-JJ-brief.md`, 30 lignes maximum : une phrase d'ouverture (la chose la plus importante du
jour), les trois paniers, puis « Par quoi commencer » avec **une seule** première action. Aucune autre écriture.
