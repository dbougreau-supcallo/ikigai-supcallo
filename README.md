# 🌟 Outil IKIGAI — Pôle Sup Marcel Callo

Outil interactif d'orientation professionnelle basé sur la philosophie japonaise de l'IKIGAI.

## 🚀 Déploiement GitHub Pages (5 minutes)

### Étape 1 — Créer le dépôt GitHub
1. Va sur [github.com](https://github.com) → **New repository**
2. Nom : `ikigai-callo` (ou ce que tu veux)
3. Visibilité : **Public** (obligatoire pour GitHub Pages gratuit)
4. Clique **Create repository**

### Étape 2 — Uploader les fichiers
```bash
# Option A : via l'interface GitHub (plus simple)
# Glisse-dépose tous les fichiers de ce dossier dans ton dépôt

# Option B : via Git (terminal)
git clone https://github.com/TON-USERNAME/ikigai-callo.git
cp -r * ikigai-callo/
cd ikigai-callo
git add .
git commit -m "Initial deploy IKIGAI Callo"
git push
```

### Étape 3 — Activer GitHub Pages
1. Ton dépôt → **Settings** → **Pages** (menu gauche)
2. Source : **Deploy from a branch**
3. Branch : **main** / **(root)**
4. **Save** → attends 2 minutes
5. Ton URL sera : `https://TON-USERNAME.github.io/ikigai-callo/`

## 📧 Configurer l'envoi d'email (optionnel)

Pour que le bouton "Recevoir par email" envoie vraiment un email :

1. Crée un compte gratuit sur [emailjs.com](https://emailjs.com)
2. Crée un **Email Service** (Gmail ou autre)
3. Crée un **Email Template** avec ces variables :
   - `{{prenom}}`, `{{ikigai_sentence}}`, `{{ce_que_jaime}}`
   - `{{mes_talents}}`, `{{le_monde}}`, `{{ma_valeur}}`
   - `{{filiere}}`, `{{entreprise}}`, `{{missions}}`, `{{date}}`
4. Dans `index.html`, remplace les 3 lignes :
   ```js
   const EMAILJS_SERVICE_ID = "service_XXXXX";   // → ton Service ID
   const EMAILJS_TEMPLATE_ID = "template_XXXXX"; // → ton Template ID
   const EMAILJS_PUBLIC_KEY = "XXXXXXXXXXXXX";   // → ta Public Key
   ```

> Sans configuration EmailJS, le bouton ouvre le client email local (mailto:) — ça marche quand même.

## 📄 Fonctionnalités

- ✅ Parcours IKIGAI en 4 dimensions (20 min)
- ✅ Navigation libre entre les étapes
- ✅ Classement par importance des passions
- ✅ Échelle d'intensité pour les causes et secteurs
- ✅ Radar de compétences dynamique
- ✅ Génération PDF téléchargeable (jsPDF)
- ✅ Envoi par email (EmailJS ou mailto)
- ✅ Impression optimisée (Ctrl+P → PDF)
- ✅ Mode "Proche" — répondre pour quelqu'un
- ✅ Plan d'action personnalisé
- ✅ Recommandations filière + alternance + RDV Callo
- 🔜 V3 : Backend Supabase pour la fonction "proche" temps réel

## 🏫 Contact

**Pôle Sup' Marcel Callo**  
21 avenue Etienne Gason — 35600 Redon  
📧 contact@lyceemarcelcallo.org  
📞 02 99 71 41 33  
🌐 [lyceemarcelcallo.org](https://lyceemarcelcallo.org)

---
*Outil IKIGAI © 2024 Pôle Sup Marcel Callo — Inspiré de la philosophie japonaise de l'ikigai*

## 📂 Configurer les liens Google Drive

Dans `index.html`, recherche et remplace ces 4 placeholders par tes vrais liens Drive :

| Placeholder | À remplacer par |
|---|---|
| `VOTRE_DOSSIER_ID` | ID du dossier Drive principal Callo |
| `FICHES_METIERS_ID` | ID du sous-dossier "Fiches métiers" |
| `CV_LETTRES_ID` | ID du sous-dossier "CV & Lettres" |
| `ORIENTATION_ID` | ID du sous-dossier "Orientation" |

### Comment trouver l'ID d'un dossier Drive ?
1. Ouvre le dossier sur drive.google.com
2. L'URL ressemble à : `https://drive.google.com/drive/folders/1aBcDeFgHiJkLmNoPqRsTuVwXyZ`
3. L'ID est la partie après `/folders/` → ici `1aBcDeFgHiJkLmNoPqRsTuVwXyZ`
4. Assure-toi que le dossier est partagé en **"Toute personne avec le lien peut consulter"**

### Mise à jour des documents
Les conseillers ajoutent directement leurs fichiers dans les dossiers Drive.
L'outil affiche toujours la dernière version — aucune modification du code nécessaire.

---

## 🗺️ Roadmap

| Version | Statut | Contenu |
|---|---|---|
| V1 | ✅ Livré | Parcours IKIGAI de base |
| V2 | ✅ Livré | Classement passions, intensité causes, radar, PDF, email |
| V2.1 | ✅ Livré | Logo Callo, section Ressources Drive, zéro erreur console |
| V3 | 🔜 En cours | Supabase : liens proches réels, sauvegarde profils, back office conseiller |
