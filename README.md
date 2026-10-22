# PromptAcademy – site vitrine

Site statique (HTML/CSS/JS, sans build), prêt pour GitHub Pages.

```
index.html          page unique du site
assets/video.mp4    vidéo de présentation (60 s)
assets/poster.jpg   image affichée avant le chargement de la vidéo
assets/icon.png     symbole du logo (aussi utilisé comme favicon)
assets/logo-full.png logo complet (aperçu de partage sur les réseaux)
.nojekyll           désactive le traitement Jekyll de GitHub
```

## Mise en ligne sur GitHub Pages

1. Créez un dépôt sur GitHub (par exemple `promptacademy-site`), public.
2. Déposez le **contenu** de ce dossier à la racine du dépôt :
   - via l'interface web : *Add file → Upload files*, glissez tous les fichiers et le dossier `assets`, puis *Commit changes* ;
   - ou en ligne de commande :
     ```bash
     git init
     git add .
     git commit -m "Site PromptAcademy"
     git branch -M main
     git remote add origin https://github.com/VOTRE-COMPTE/promptacademy-site.git
     git push -u origin main
     ```
3. Dans le dépôt : *Settings → Pages → Build and deployment*, choisissez **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis *Save*.
4. Après une à deux minutes, le site est accessible à l'adresse
   `https://VOTRE-COMPTE.github.io/promptacademy-site/`.

> Le fichier `.nojekyll` commence par un point : il peut être masqué par votre explorateur de fichiers. Pensez à l'inclure (il n'est pas obligatoire, mais recommandé).

## Utiliser le domaine promptacademy.fr (optionnel)

1. *Settings → Pages → Custom domain* : saisissez `promptacademy.fr` puis *Save* (GitHub crée un fichier `CNAME`).
2. Chez votre registraire DNS, ajoutez :
   - 4 enregistrements **A** pour `promptacademy.fr` vers `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` ;
   - un enregistrement **CNAME** pour `www` vers `VOTRE-COMPTE.github.io`.
3. Une fois le domaine vérifié, cochez **Enforce HTTPS**.

## Modifier le contenu

Tout le texte se trouve dans `index.html` : catalogue des formations (section `id="formations"`), FAQ (`id="faq"`), adresse e-mail (`id="mail"`).
Pour remplacer la vidéo, gardez le nom `assets/video.mp4` (format MP4/H.264, moins de 100 Mo).
