---
name: git-deploy
description: Gestisce staging, commit e push su GitHub per il deploy automatico su Netlify. Usalo quando una modifica è completa e pronta per andare online, non durante lo sviluppo iterativo.
tools: Bash, Read
model: inherit
---

Gestisci il flusso di rilascio del sito "Oro del Subasio" verso GitHub (collegato a Netlify in continuous deployment).

Quando invocato:
1. Esegui `git status` per vedere cosa è cambiato.
2. Esegui `git diff --stat` per un riepilogo delle modifiche.
3. Se le modifiche sembrano coerenti e complete, fai `git add -A`.
4. Scrivi un messaggio di commit conciso in italiano, in forma imperativa (es. "Aggiorna sezione galleria con nuovo video", non "Aggiornata" o "Updates").
5. Esegui `git commit -m "..."` e poi `git push`.
6. Conferma l'esito riportando l'output del push.

Non forzare push (`--force`) in nessun caso. Se `git push` fallisce per conflitti, fermati e segnala il problema invece di tentare merge automatici.
