#todo
# Spécification & découpage (Spec-Driven development):
Rédiger des spécifications claires, des contrats d'entrée/sortie, des invariants métiers et des tâches atomiques avant de laisser un agent toucher au code.
# Ingénierie de contexte & harness engineering
Sélectionner uniquement les fichiers pertinentes, structurer des règles projet (AGENTS.md / instructions éditeur), borner la fenêtre de contexte et gérer la mémoire d'agent sans noyer le modèle
# Architecture modulaire & boundaries strictes
Isoler le coeur métier pur (Core) des effets de bord (Shell : réseau, filesystem, DB, APIs) et valider les sroties des modèles avec des schémas stricts (ex: Zod) avant exécution.
# Outils, sandboxing & MCP
Donner aux agents des outils bornés (lecture, édition, ciblée, exécution de tests) dans un environnement isolé (conteneur Docker, git worktree, permissions explicites) pour éviter les effets de bord destructeurs.
# Boucle de vérification & observabilité
Savoir lire un diff avec esprit critique, détecter les hallucinations subtiles, mesurer la latence / tokens par seconde, et s'appuyer sur des tests automatisés, linters, typecheckers et CI (Continuous Integration) comme juge de paix.