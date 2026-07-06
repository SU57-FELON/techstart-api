# Remote Repositories Assignment 

## Repository Links

### Open Source Contribution
 - Original repository: https://github.com/SU57-FELON/awesome-calculator
 - Fork repository: https://github.com/SU57-FELON/awesome-calculator-fork
 - Feature branch: feature/multiply

### Corporate Project
 - Main repository: https://github.com/SU57-FELON/techstart-api
 - Backup repository: https://github.com/SU57-FELON/techstart-api-backup

## Verification Commands

Run these commands in techstart-api-local:

      git remote -v | grep -c "push"
      git branch -r | wc -l

Expected output:
 - First command: 3 (origin has 2 push URLs — techstart-api + techstart-api-backup — plus the backup remote;
 multiple push URLs configured)
 - Second command: 4 remote branches (backup/main, origin/HEAD, origin/develop, origin/main)
