# Guide de Déploiement - StrategyQuest

Votre site est un site statique (un seul fichier HTML), ce qui le rend très facile à déployer. Voici plusieurs options :

## Option 1 : GitHub Pages (Recommandé - Gratuit et Simple)

### Étapes :

1. **Activer GitHub Pages dans votre dépôt :**
   - Allez sur https://github.com/sarda2/StrategyQuest
   - Cliquez sur **Settings** (Paramètres)
   - Dans le menu de gauche, cliquez sur **Pages**
   - Sous **Source**, sélectionnez **Deploy from a branch**
   - Choisissez la branche **main** et le dossier **/ (root)**
   - Cliquez sur **Save**

2. **Votre site sera disponible à :**
   - `https://sarda2.github.io/StrategyQuest/` (HTTPS automatique ✅)

3. **Mise à jour automatique :**
   - Chaque fois que vous poussez des modifications sur la branche `main`, le site se met à jour automatiquement

---

## Option 2 : Netlify (Gratuit, très rapide)

### Méthode 1 : Via l'interface web

1. Allez sur https://www.netlify.com
2. Créez un compte (ou connectez-vous avec GitHub)
3. Cliquez sur **Add new site** → **Import an existing project**
4. Connectez votre dépôt GitHub `StrategyQuest`
5. Netlify détectera automatiquement que c'est un site statique
6. Cliquez sur **Deploy site**
7. Votre site sera disponible immédiatement avec une URL comme `https://strategyquest-xxx.netlify.app` (HTTPS automatique ✅)

### Méthode 2 : Via Netlify CLI

```bash
# Installer Netlify CLI
npm install -g netlify-cli

# Se connecter
netlify login

# Déployer
cd /Users/sardavictoire/Documents/GitHub/StrategyQuest
netlify deploy --prod
```

---

## Option 3 : Vercel (Gratuit, excellent pour les performances)

### Via l'interface web :

1. Allez sur https://vercel.com
2. Créez un compte (ou connectez-vous avec GitHub)
3. Cliquez sur **Add New Project**
4. Importez votre dépôt `StrategyQuest`
5. Vercel détectera automatiquement la configuration
6. Cliquez sur **Deploy**
7. Votre site sera disponible avec une URL comme `https://strategy-quest.vercel.app` (HTTPS automatique ✅)

### Via Vercel CLI :

```bash
# Installer Vercel CLI
npm install -g vercel

# Déployer
cd /Users/sardavictoire/Documents/GitHub/StrategyQuest
vercel --prod
```

---

## Option 4 : Cloudflare Pages (Gratuit, très rapide)

1. Allez sur https://pages.cloudflare.com
2. Connectez-vous avec votre compte Cloudflare
3. Cliquez sur **Create a project**
4. Connectez votre dépôt GitHub `StrategyQuest`
5. Configurez :
   - **Framework preset** : None (ou Static)
   - **Build command** : (laissez vide)
   - **Build output directory** : /
6. Cliquez sur **Save and Deploy**
7. Votre site sera disponible avec une URL comme `https://strategyquest.pages.dev` (HTTPS automatique ✅)

---

## Recommandation

**Pour commencer rapidement : GitHub Pages** est la meilleure option car :
- ✅ Votre dépôt est déjà sur GitHub
- ✅ Configuration en 2 minutes
- ✅ Gratuit
- ✅ Mise à jour automatique à chaque push
- ✅ URL personnalisable

**Pour de meilleures performances : Netlify ou Vercel** offrent :
- ✅ CDN global plus rapide
- ✅ HTTPS automatique
- ✅ URL personnalisée gratuite
- ✅ Analytics intégrés (optionnel)

---

## Commandes utiles

### Vérifier que tout est à jour avant de déployer :

```bash
cd /Users/sardavictoire/Documents/GitHub/StrategyQuest
git status
git add .
git commit -m "Préparation pour déploiement"
git push origin main
```

---

## Personnalisation de l'URL (optionnel)

### GitHub Pages :
- Allez dans Settings → Pages
- Vous pouvez ajouter un domaine personnalisé

### Netlify/Vercel :
- Dans les paramètres du projet, vous pouvez changer le nom du site
- Vous pouvez aussi ajouter un domaine personnalisé

---

## HTTPS - Sécurité

✅ **HTTPS est automatiquement activé** sur toutes les plateformes mentionnées ci-dessus (GitHub Pages, Netlify, Vercel, Cloudflare Pages).

✅ **Le code a été configuré** avec des meta tags de sécurité qui :
- Forcent l'upgrade automatique de HTTP vers HTTPS
- Activent HSTS (HTTP Strict Transport Security) pour une sécurité renforcée

Aucune configuration supplémentaire n'est nécessaire - votre site sera toujours servi en HTTPS une fois déployé.

---

## Support

Si vous rencontrez des problèmes, vérifiez que :
- ✅ Votre fichier `index.html` est à la racine du dépôt
- ✅ Vous avez bien poussé vos modifications sur GitHub
- ✅ La branche `main` est bien sélectionnée dans les paramètres

