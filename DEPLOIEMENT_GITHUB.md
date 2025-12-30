# 🚀 GUIDE DE DÉPLOIEMENT GITHUB

## ÉTAPE 1 : Préparer les fichiers

### ✅ Vérifications avant déploiement :
- [ ] Tous les tests locaux sont réussis
- [ ] Le site fonctionne parfaitement en local
- [ ] Les sauvegardes fonctionnent
- [ ] Le mot de passe fonctionne

---

## ÉTAPE 2 : Créer un dépôt GitHub

### Si vous n'avez pas encore de dépôt :

1. **Aller sur GitHub.com**
2. **Cliquer sur le "+" en haut à droite**
3. **Sélectionner "New repository"**
4. **Remplir les informations :**
   - Repository name : `grades-judo` (ou autre nom)
   - Description : "Site de gestion des passages de grades judo"
   - Public ou Private : à votre choix
   - Ne PAS cocher "Initialize with README" (on en a déjà un)
5. **Cliquer sur "Create repository"**

---

## ÉTAPE 3 : Pousser le code sur GitHub

### Méthode A : En ligne de commande

Ouvrir un terminal dans le dossier `grades-judo 2` :

```bash
# Initialiser git (si pas déjà fait)
git init

# Ajouter tous les fichiers
git add .

# Faire un commit
git commit -m "Site grades-judo avec corrections complètes"

# Ajouter le remote (remplacer YOUR-USERNAME et REPO-NAME)
git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git

# Pousser sur GitHub
git push -u origin main
```

### Méthode B : GitHub Desktop

1. Ouvrir GitHub Desktop
2. File > Add Local Repository
3. Sélectionner le dossier `grades-judo 2`
4. Publish repository
5. Choisir le nom et la visibilité
6. Cliquer sur "Publish"

---

## ÉTAPE 4 : Activer GitHub Pages

1. **Aller sur votre dépôt GitHub**
2. **Cliquer sur "Settings"** (icône engrenage)
3. **Dans le menu de gauche, cliquer sur "Pages"**
4. **Dans "Source" :**
   - Branch : `main`
   - Folder : `/ (root)`
5. **Cliquer sur "Save"**
6. **Attendre 1-2 minutes**

---

## ÉTAPE 5 : Accéder au site

Votre site sera disponible à :
```
https://YOUR-USERNAME.github.io/REPO-NAME/
```

Par exemple :
```
https://fabriceetchristiane-star.github.io/grades-judo/
```

---

## 🔧 PROBLÈMES COURANTS

### Le site ne s'affiche pas
**Solutions :**
1. Attendre 2-3 minutes
2. Vérifier que GitHub Pages est bien activé (Settings > Pages)
3. Vérifier l'URL (bien mettre /nom-du-repo/ à la fin)
4. Rafraîchir avec Ctrl + F5

### Les CSS ne chargent pas
**Solutions :**
1. Vérifier que tous les fichiers sont bien sur GitHub
2. Vérifier les chemins dans index.html
3. Attendre le build complet

### Les sauvegardes ne fonctionnent pas en ligne
**Normal !** Les sauvegardes sont dans le localStorage de chaque navigateur.
Chaque utilisateur aura ses propres données.

---

## 📝 COMMANDES GIT UTILES

### Mettre à jour après des modifications :
```bash
# Ajouter les fichiers modifiés
git add .

# Commit avec message
git commit -m "Description des changements"

# Pousser sur GitHub
git push
```

### Voir l'état des fichiers :
```bash
git status
```

### Voir l'historique :
```bash
git log
```

---

## 🎯 APRÈS LE DÉPLOIEMENT

### ✅ À vérifier sur le site en ligne :
- [ ] La page d'accueil s'affiche correctement
- [ ] Les liens du menu fonctionnent
- [ ] Les images s'affichent
- [ ] La connexion professeur fonctionne
- [ ] L'interface admin est accessible
- [ ] Le règlement s'affiche

### ⚠️ Différences en ligne vs local :
- Les données localStorage sont par utilisateur
- Chaque navigateur aura ses propres sauvegardes
- Il faudra recréer le contenu dans l'admin en ligne

---

## 🔐 SÉCURITÉ

### Changer le mot de passe pour la version en ligne :

1. Ouvrir `auth.js`
2. Modifier la ligne :
```javascript
return password === "Hadjime@2026";
```
3. Mettre un nouveau mot de passe
4. Commit et push
5. Attendre que GitHub Pages se mette à jour

---

## 📊 STATISTIQUES GITHUB PAGES

Pour voir les statistiques de votre site :
1. GitHub > Insights (menu du dépôt)
2. Traffic (voir les visiteurs)

---

## 🆘 AIDE SUPPLÉMENTAIRE

### Documentation officielle :
- GitHub Pages : https://pages.github.com/
- Git : https://git-scm.com/doc

### Communauté :
- Stack Overflow
- GitHub Community

---

## ✅ CHECKLIST FINALE

Avant de partager le lien :

- [ ] Le site est en ligne
- [ ] Toutes les pages fonctionnent
- [ ] Le mot de passe est sécurisé
- [ ] Les images s'affichent
- [ ] Le CSS est bien chargé
- [ ] Test sur mobile
- [ ] Test sur différents navigateurs

---

## 🎉 C'EST EN LIGNE !

Vous pouvez maintenant partager le lien avec :
- Votre club de judo
- Vos élèves
- D'autres professeurs

**N'oubliez pas de donner le mot de passe uniquement aux personnes autorisées !**

---

*Guide créé le 21 Décembre 2025*
*Pour le site Grades Judo*
