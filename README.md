# Résumés de cours FMSB

Web app : l'étudiant colle un cours, importe un PDF ou photographie ses pages, et reçoit un résumé avec formules (LaTeX), exemples médicaux résolus, pièges d'examen et quiz.

## Lancer en local
    npm install
    cp .env.example .env      # puis mets ta clé dans ANTHROPIC_API_KEY
    node --env-file=.env server.js
Ouvre http://localhost:3000

## Déployer (ex. Render ou Railway)
1. Pousse le dossier sur GitHub (le fichier `.env` est ignoré).
2. Crée un « Web Service » Node : build `npm install`, start `npm start`.
3. Ajoute les variables d'environnement : `ANTHROPIC_API_KEY` (obligatoire), `ACCESS_CODE`, `HOURLY_LIMIT`, `MODEL`.
4. Partage l'URL (et le code d'accès) aux étudiants.

## Maîtriser les coûts
- Mets une limite de dépense mensuelle sur ta clé dans la console Anthropic.
- `ACCESS_CODE` + `HOURLY_LIMIT` évitent les abus.
- `MODEL=claude-haiku-5-5` réduit le coût par résumé.

## Pistes suivantes
Comptes étudiants, historique des fiches, export Word/PDF, mode « questions sur mon cours », cache des résumés identiques.
