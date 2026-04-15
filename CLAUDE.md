# CLAUDE.md — Projet Signatures Email KMOOVE

## Objectif
Signatures email HTML professionnelles pour l'équipe KMOOVE, compatibles tous clients email (Gmail, Outlook, Apple Mail, Thunderbird). Anti-spam optimisé, ergonomie maximale.

---

## CONSIGNES PERMANENTES (à appliquer à CHAQUE modification)

### RÈGLE 1 — Double livraison obligatoire
À chaque modification de signature, mettre à jour dans le dossier de la personne :
- **`signature-<domaine>.html`** — fichier HTML complet (pour prévisualiser dans un navigateur)
- **`CODE-<domaine>.txt`** — code HTML brut prêt à copier-coller directement dans le client email

### RÈGLE 2 — Anti-spam obligatoire
Chaque signature DOIT respecter TOUTES ces règles anti-spam :
- Layout 100% `<table>` (jamais flexbox/grid — incompatible Outlook)
- CSS inline uniquement (jamais de `<style>` block — ignoré par Gmail)
- `width` + `height` fixes en pixels sur CHAQUE image (empêche le zoom)
- `display: block` sur toutes les images (empêche espacement fantôme)
- `border="0"` sur toutes les images (empêche bordure bleue de lien)
- Images compressées < 10 Ko chacune (total signature < 25 Ko)
- HTTPS obligatoire partout (HTTP = bloqué par Gmail)
- Hébergement github.io (domaine de confiance, jamais blacklisté)
- Jamais de base64 (bloqué par Gmail, Outlook)
- Jamais de SVG (non supporté par beaucoup de clients)
- Jamais de JavaScript (bloqué partout)
- Ratio texte/images équilibré (assez de texte visible)
- Alt text descriptif sur chaque image (affichage si images bloquées)
- Liens vers domaine propre (apa-kmoove.com) — jamais de shorteners (bit.ly, etc.)
- Pas de mots spam dans le HTML ("gratuit", "offre", "cliquez ici")

### RÈGLE 3 — Layout horizontal (v2.0 — 2026-04-15)
- **Layout 3 colonnes** : Photo+Infos | Séparateur rouge vertical | Phrase marketing + Badges
- Photo en cercle (88x88px) — pro et humain
- Informations hiérarchisées : nom > poste > tel > email > site > LinkedIn > lieu
- **Colonne droite** : phrase marketing (13px bold #444) + cibles (11px #888) + badges UGAP (180x77) et Prix (180x51) côte à côte
- Séparateur rouge vertical KMOOVE (#E30613, 3px, 145px hauteur)
- Police Arial (universelle, lisible)
- Tailles : nom 18px bold, poste 14px rouge, coordonnées 13px gris
- Phrase marketing : "Solutions interactives, ludiques et sportives de prévention et de santé"
- Cibles : "EHPAD - IME - Maison Sport Santé - Agglomération - Entreprise"
- Mention légale discrète (9px, gris clair) — seul élément sous le layout horizontal
- Icône LinkedIn cliquable (14x14px) vers le profil de chaque personne

### RÈGLE 4 — Mise à jour systématique
Quand l'utilisateur demande un changement de signature :
1. Modifier TOUS les fichiers `.html` de la personne concernée
2. Modifier TOUS les fichiers `CODE-*.txt` correspondants
3. Si changement global (badges, design, layout) → modifier TOUS les dossiers
4. Recompresser les images si nouvelles images ajoutées
5. Git push sur GitHub Pages
6. Mettre à jour ce CLAUDE.md si infos changent

---

## Structure des dossiers
```
SIGNATURE/
  images/                          ← Images partagées (badges, photos)
  Coralie Rodriguez/
    signature-kmoove-pro.html      ← Prévisualisation navigateur
    signature-kmoove-sales.html
    signature-kmoove-ventes.html
    CODE-kmoove-pro.txt            ← Code HTML brut à copier-coller
    CODE-kmoove-sales.txt
    CODE-kmoove-ventes.txt
  Karim Mounassib/
    signature-kmoove.html
    signature-kmoove-pro.html
    signature-kmoove-sales.html
    signature-kmoove-ventes.html
    CODE-kmoove.txt
    CODE-kmoove-pro.txt
    CODE-kmoove-sales.txt
    CODE-kmoove-ventes.txt
  Olivier Carduner/
    signature-kmoove.html
    signature-kmoove-pro.html
    signature-kmoove-sales.html
    signature-kmoove-ventes.html
    CODE-kmoove.txt
    CODE-kmoove-pro.txt
    CODE-kmoove-sales.txt
    CODE-kmoove-ventes.txt
```

## Équipe KMOOVE — Signatures

### Coralie Rodriguez — Co-fondatrice
| Adresse email | Fichier HTML | Code à copier | Statut |
|---------------|-------------|---------------|--------|
| coralie@kmoove-pro.com | `signature-kmoove-pro.html` | `CODE-kmoove-pro.txt` | OK |
| coralie@kmoove-sales.com | `signature-kmoove-sales.html` | `CODE-kmoove-sales.txt` | OK |
| coralie@kmoove-ventes.com | `signature-kmoove-ventes.html` | `CODE-kmoove-ventes.txt` | OK |
- **Téléphone :** +33 7 43 39 77 08
- **Site web :** https://apa-kmoove.com/
- **Lieux :** Lyon / Paris / Lille
- **LinkedIn :** https://www.linkedin.com/in/coralie-rodriguez-99511619a/
- **Photo :** `images/photo-coralie.jpeg` (6 Ko)

### Karim Mounassib — Fondateur
| Adresse email | Fichier HTML | Code à copier | Statut |
|---------------|-------------|---------------|--------|
| karim@kmoove.com | `signature-kmoove.html` | `CODE-kmoove.txt` | OK |
| k.mounassib@kmoove-pro.com | `signature-kmoove-pro.html` | `CODE-kmoove-pro.txt` | OK |
| k.mounassib@kmoove-sales.com | `signature-kmoove-sales.html` | `CODE-kmoove-sales.txt` | OK |
| k.mounassib@kmoove-ventes.com | `signature-kmoove-ventes.html` | `CODE-kmoove-ventes.txt` | OK |
- **Téléphone :** +33 7 43 39 77 08
- **Site web :** https://apa-kmoove.com/
- **Lieux :** Lyon / Paris / Lille
- **LinkedIn :** https://www.linkedin.com/in/karimmounassib-gamification-/
- **Photo :** `images/photo-karim.jpeg` (5 Ko)

### Olivier Carduner — Directeur Commercial
| Adresse email | Fichier HTML | Code à copier | Statut |
|---------------|-------------|---------------|--------|
| olivier@kmoove.com | `signature-kmoove.html` | `CODE-kmoove.txt` | OK |
| olivier@kmoove-pro.com | `signature-kmoove-pro.html` | `CODE-kmoove-pro.txt` | OK |
| olivier@kmoove-sales.com | `signature-kmoove-sales.html` | `CODE-kmoove-sales.txt` | OK |
| olivier@kmoove-ventes.com | `signature-kmoove-ventes.html` | `CODE-kmoove-ventes.txt` | OK |
- **Téléphone :** +33 7 43 39 77 08
- **Site web :** https://apa-kmoove.com/
- **Lieux :** Lyon / Paris / Lille
- **LinkedIn :** https://www.linkedin.com/in/ocarduner3aconseil/
- **Photo :** `images/photo-olivier.jpeg` (4 Ko)

## Images partagées — GitHub Pages
| Image | URL publique | Taille |
|-------|-------------|--------|
| Photo Coralie | `https://kmoovegame104.github.io/email-assets/images/photo-coralie.jpeg` | 6 Ko |
| Photo Karim | `https://kmoovegame104.github.io/email-assets/images/photo-karim.jpeg` | 5 Ko |
| Photo Olivier | `https://kmoovegame104.github.io/email-assets/images/photo-olivier.jpeg` | 4 Ko |
| Icone LinkedIn | `https://kmoovegame104.github.io/email-assets/images/icon-linkedin.png` | < 1 Ko |
| Badge UGAP | `https://kmoovegame104.github.io/email-assets/images/badge-ugap.jpg` | 7 Ko |
| Prix Salon Sports | `https://kmoovegame104.github.io/email-assets/images/prix-salon-sports.jpg` | 9 Ko |

## Hébergement
- **Repo :** KMOOVEGAME104/email-assets (public)
- **GitHub Pages :** https://kmoovegame104.github.io/email-assets/
- **SPF/DKIM/DMARC :** configurés sur kmoove-pro.com, kmoove-sales.com, kmoove-ventes.com

## Processus pour ajouter/modifier un collègue
1. Placer la photo dans `images/photo-prenom.jpg`
2. Compresser (200x200px, JPEG quality 75, < 10 Ko)
3. Demander : nom, poste, téléphone, adresses email
4. Créer `signature-<domaine>.html` + `CODE-<domaine>.txt` pour chaque adresse
5. Vérifier checklist anti-spam (RÈGLE 2)
6. `git push` → GitHub Pages met à jour automatiquement
7. Donner le code HTML (fichier CODE-*.txt) au collègue

## Notes
- Ce CLAUDE.md est SPÉCIFIQUE à ce dossier SIGNATURE uniquement
- Ne pas confondre avec les CLAUDE.md des projets KMOOVE (jeux Python)
