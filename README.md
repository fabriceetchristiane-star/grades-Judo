# 🥋 Guide des Grades Judo

Site web complet pour la gestion et la consultation des passages de grades de judo (1er au 6ème Dan).

## 📋 Fonctionnalités

### Pour les Pratiquants
- ✅ Consultation des techniques par grade (1er au 6ème Dan)
- ✅ Accès aux katas requis
- ✅ Règlement officiel des passages de grade
- ✅ **Téléchargement de documents PDF officiels**
- ✅ Nouveautés et mises à jour réglementaires
- ✅ Interface responsive (mobile, tablette, desktop)

### Pour les Professeurs
- 🔐 Espace administrateur protégé par mot de passe
- ✏️ Modification du contenu des grades
- 📄 **Gestion des documents PDF** (upload, catégorisation, suppression)
- 📝 Gestion des 5 sections du règlement :
  - Règlement Général
  - Guide des Juges
  - Critères d'Évaluation
  - Procédure Examen
  - Nouveautés
- 🔄 Mise à jour des nouveautés
- 💾 Sauvegarde automatique dans le navigateur

## 🚀 Démarrage Rapide

### Utilisation Locale
1. Télécharger ou cloner le dépôt
2. Ouvrir `index.html` dans un navigateur web
3. Pour accéder à l'admin : descendre en bas de page et utiliser le mot de passe

### Déploiement sur GitHub Pages
1. Fork ou push le projet sur votre compte GitHub
2. Aller dans Settings > Pages
3. Source : Deploy from a branch
4. Branch : main / root
5. Cliquer sur Save
6. Le site sera disponible à : `https://votre-username.github.io/nom-du-repo/`

## 🔐 Accès Administrateur

**Mot de passe par défaut :** `Hadjime@2026`

Pour changer le mot de passe :
1. Ouvrir le fichier `auth.js`
2. Modifier la ligne : `return password === "Hadjime@2026";`
3. Remplacer par votre nouveau mot de passe

## 📁 Structure des Fichiers

```
grades-judo/
│
├── index.html              # Page d'accueil
├── admin.html              # Interface d'administration
├── documents.html          # Page documents PDF publique
├── reglement.html          # Page règlement public
├── techniques.html         # Page techniques
├── katas.html             # Page katas
├── philosophie.html       # Page philosophie
├── 1er-dan.html           # Page 1er Dan
├── 2eme-dan.html          # Page 2ème Dan
├── ... (autres grades)
│
├── auth.js                # Système d'authentification
├── styles.css             # Feuille de styles
│
├── images/                # Dossier images
│   └── logo-grades.png
│
├── uploads/               # Documents uploadés
│   ├── Gestion des Katas/
│   ├── Gestion des Techniques/
│   ├── Gestion des Vidéos/
│   └── Gestion du Règlement/
│
└── _archive/              # Anciens fichiers archivés
```

## 💾 Stockage des Données

Les données sont stockées dans le **localStorage** du navigateur :

### Clés utilisées :
- `grades_judo_session` - Session de connexion
- `grade-1er-dan` à `grade-6eme-dan` - Contenus techniques
- `nouveaute-1-titre`, `nouveaute-1-desc` - Nouveautés
- `reglement-general` - Règlement général
- `reglement-juges` - Guide des juges
- `reglement-criteres` - Critères d'évaluation
- `reglement-procedure` - Procédure examen
- `reglement-nouveautes` - Nouveautés réglementaires
- **`documentsData`** - Documents PDF uploadés

⚠️ **Important :** Les données sont stockées localement dans le navigateur. Pour transférer les données :
1. Exporter via les outils développeur (F12 > Application > Local Storage)
2. Ou recréer le contenu dans le nouveau navigateur/ordinateur

## 📄 Gestion des Documents PDF

### Pour ajouter un document :
1. Se connecter à l'admin
2. Aller dans l'onglet "Documents PDF"
3. Sélectionner un fichier PDF
4. Remplir le titre et la description
5. Choisir la catégorie
6. Cliquer sur "Uploader le Document"

### Catégories disponibles :
- 📜 Règlement Général
- 👔 Juges & Arbitres
- ✅ Critères de Notation
- ⚙️ Procédures
- ⭐ Nouveautés
- 📁 Autres

Les documents sont visibles publiquement sur la page **documents.html**.

## 🎨 Personnalisation

### Couleurs
Modifier dans `styles.css` ou dans les balises `<style>` de chaque page.

### Logo
Remplacer `images/logo-grades.png` par votre logo.

### Contenu
Tout le contenu est modifiable via l'interface admin (pas besoin de toucher au code).

## 🔧 Corrections Récentes

### Version du 28 Décembre 2024
- ✅ **Système de gestion de documents PDF unifié**
- ✅ Upload de documents avec titre, description et catégorie
- ✅ Page publique de consultation des documents
- ✅ Correction du stockage localStorage (clé `documentsData`)
- ✅ Nettoyage du projet (fichiers archivés dans `_archive/`)

### Version du 21 Décembre 2024
- ❌ Suppression du bouton admin non protégé en page d'accueil
- ✅ Conservation de l'accès professeur protégé en footer
- ✅ Ajout des 5 sections complètes de règlement
- ✅ Renommage "Nouveautés 2024" → "Nouveautés"
- ✅ Correction du système de sauvegarde localStorage

## 🐛 Dépannage

### Les documents n'apparaissent pas sur documents.html
1. Vérifier que vous avez uploadé via l'admin (onglet Documents PDF)
2. Vérifier dans F12 > Application > Local Storage que la clé `documentsData` existe
3. Rafraîchir la page documents.html
4. Vérifier la console pour les erreurs JavaScript

### Les sauvegardes ne fonctionnent pas
1. Vérifier que JavaScript est activé
2. Ouvrir la console (F12) et chercher les erreurs
3. Vérifier que le localStorage n'est pas plein (limite ~5-10MB)
4. Essayer dans un autre navigateur

### Impossible d'accéder à l'admin
1. Vérifier le mot de passe : `Hadjime@2026`
2. Vider le cache du navigateur
3. Vérifier que `auth.js` est bien chargé (F12 > Console)

## 📱 Compatibilité

- ✅ Chrome / Edge (recommandé)
- ✅ Firefox
- ✅ Safari
- ✅ Mobile (iOS / Android)

## 📞 Support

Pour toute question ou problème :
1. Vérifier la console navigateur (F12)
2. Vérifier le localStorage (F12 > Application > Local Storage)
3. Consulter ce README

## 📄 Licence

Ce projet est libre d'utilisation pour les clubs de judo et les professeurs.

## 🎯 Roadmap

Améliorations futures possibles :
- [ ] Export/Import des données
- [ ] Système de backup automatique
- [ ] Upload de vidéos
- [ ] Gestion multi-utilisateurs
- [ ] Base de données en ligne
- [ ] Application mobile native

---

**Développé avec ❤️ pour la communauté Judo**

*Dernière mise à jour : 28 Décembre 2024*
