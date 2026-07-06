# Remote Repository Setup

## Current Remotes
backup    git@github.com:SU57-FELON/techstart-api-backup.git (fetch)
backup    git@github.com:SU57-FELON/techstart-api-backup.git (push)
origin    git@github.com:SU57-FELON/techstart-api.git (fetch)
origin    git@github.com:SU57-FELON/techstart-api.git (push)
origin    git@github.com:SU57-FELON/techstart-api-backup.git (push)
  
## Tracking Branches
  develop d7b03c5 [origin/develop] Bump version to 1.1.0-dev
 - main    54ca1eb [origin/main] Merge branch 'main' of github.com:SU57-FELON/techstart-api

## Fork Workflow Summary
- Original repository: https://github.com/SU57-FELON/awesome-calculator
- Fork repository: https://github.com/SU57-FELON/awesome-calculator-fork
- Upstream configuration: `git remote add upstream git@github.com:SU57-FELON/awesome-calculator.git`

## Backup Strategy
- Primary remote: origin
- Backup remote: backup
- Sync command: `git push origin main`

## Lessons Learned
Команда `fetch` обновляет локальное представление об удалённых ветках, не трогая рабочие файлы — так можно
увидеть, что изменилось на сервере, перед переключением. Push отклоняется, когда на сервере есть коммиты,
которых нет локально; чтобы это решить, нужно сначала сделать `pull`, при необходимости разрешить конфликт
вручную, и только потом снова `push`. Двойной push в backup настраивается через `git remote set-url --add --push
origin` — после этого обычный `git push origin` автоматически отправляет изменения сразу в два репозитория.
