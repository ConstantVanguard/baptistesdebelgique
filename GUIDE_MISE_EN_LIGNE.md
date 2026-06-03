# Guide de mise en ligne — baptistesdebelgique.be

## Fichiers du site

| Fichier | Rôle |
|---|---|
| index.html | Page d'accueil (registre + vie protestante + lien reverend.be) |
| foi.html | Confession de foi baptiste |
| vie-protestante.html | Événements AEEBLF + annuaire des églises |
| contact.html | Formulaire de contact "Nous rejoindre" |
| merci.html | Page de confirmation après envoi du formulaire |
| style.css | Feuille de style partagée |

## Étape 1 — Acheter le domaine sur GoDaddy

1. Connectez-vous sur godaddy.com
2. Cherchez **baptistesdebelgique.be**
3. Achetez-le (~12-15€/an)
4. Dans les paramètres DNS, on configurera plus tard le lien vers GitHub Pages

## Étape 2 — Créer le repo GitHub

1. Allez sur github.com (votre compte ConstantVanguard)
2. Cliquez "New repository"
3. Nom : **cbb** (ou **baptistesdebelgique**)
4. Public, cochez "Add a README"
5. Créez le repo

## Étape 3 — Uploader les fichiers

1. Dans le repo, cliquez "Add file" → "Upload files"
2. Glissez tous les fichiers (les 5 HTML + style.css)
3. Commit

## Étape 4 — Activer GitHub Pages

1. Dans le repo → Settings → Pages
2. Source : "Deploy from a branch"
3. Branch : main, dossier / (root)
4. Save
5. Attendez 2-3 minutes, le site sera accessible sur constantvanguard.github.io/cbb

## Étape 5 — Connecter le domaine GoDaddy

1. Dans GitHub → Settings → Pages → Custom domain → entrez : www.baptistesdebelgique.be
2. Cochez "Enforce HTTPS"
3. Dans GoDaddy → DNS → ajoutez :
   - Type CNAME, Nom: www, Valeur: constantvanguard.github.io
   - Type A, Nom: @, Valeur: 185.199.108.153
   - Type A, Nom: @, Valeur: 185.199.109.153
   - Type A, Nom: @, Valeur: 185.199.110.153
   - Type A, Nom: @, Valeur: 185.199.111.153
4. Attendez 24-48h pour la propagation DNS

## Étape 6 — Configurer le formulaire de contact

1. Allez sur https://formspree.io/
2. Créez un compte gratuit (avec info@reverend.be)
3. Créez un nouveau formulaire
4. Copiez l'ID du formulaire (ex: xabcdefg)
5. Dans contact.html, remplacez "VOTRE_ID_FORMSPREE" par cet ID
6. Gratuit jusqu'à 50 messages/mois

## À personnaliser

- **Les chiffres du registre** (index.html) : remplacez 12, 47, 8 par vos vrais chiffres
- **L'annuaire des églises** (vie-protestante.html) : vérifiez que les liens sont corrects
- **Les événements** (vie-protestante.html) : à mettre à jour 2-3 fois par an depuis associationbaptiste.org/Agenda.php
