# YTM Studio

Application web statique (100 % côté client, responsive PC & mobile) pour générer des playlists YouTube Music sur-mesure grâce à **Gemini AI** et les créer directement sur votre compte via **Google Identity Services (OAuth 2.0)** et **YouTube Data API v3**.

## Fonctionnalités

- **100 % privé et statique** : la clé API Gemini, le modèle choisi, le Client ID Google OAuth et vos profils sont stockés uniquement dans le `localStorage` du navigateur (jamais dans le code).
- **Critères complets** : humeurs, contexte, objectif, curseur Énergie/Tempo, curseur Connus vs Découvertes, prise en compte optionnelle de vos **Titres aimés** (filtrés sur la catégorie Musique), époques, langues, nombre de titres, exclusions strictes et texte libre.
- **Système de profils** : sauvegarder, charger et supprimer vos combinaisons de critères dans `localStorage`.
- **Flux en 2 temps** :
  1. Prévisualisation interactive avec suppression de titres à l'unité, édition du titre/description/visibilité et champ d'ajustement/régénération Gemini.
  2. Création en 1 clic sur YouTube Music avec barre de progression en direct et lien direct vers la playlist sur YouTube Music.

## Configuration Google Cloud Console

1. Activez **YouTube Data API v3** dans votre projet Google Cloud.
2. Configurez l'**Écran de consentement OAuth** (ajoutez votre adresse Google dans les *Utilisateurs tests* si l'application est en mode Test).
3. Créez un **ID client OAuth 2.0** de type **Application Web**.
4. Dans **Origines JavaScript autorisées**, renseignez :
   - `https://mrteliot38.github.io`
5. Ouvrez le site déployé (`https://mrteliot38.github.io/ytm-studio/`), cliquez sur **Paramètres API**, puis saisissez votre clé API Gemini, votre modèle Gemini et votre Google OAuth Client ID.
