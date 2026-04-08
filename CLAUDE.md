# CLAUDE.md — Projet Signatures Email KMOOVE

## Objectif
Signatures email HTML professionnelles pour l'équipe KMOOVE, compatibles tous clients email (Gmail, Outlook, Apple Mail, Thunderbird). Anti-spam optimisé.

## Structure des dossiers
```
SIGNATURE/
  images/                      ← Images partagées (badges UGAP, Prix)
  Coralie Rodriguez/           ← 3 signatures (pro, sales, ventes)
    signature-kmoove-pro.html
    signature-kmoove-sales.html
    signature-kmoove-ventes.html
  Karim Mounassib/             ← À compléter (photo + infos + signatures)
  Olivier Cardiner/            ← À compléter (photo + infos + signatures)
```

## Équipe KMOOVE — Signatures

### Coralie Rodriguez — Co-fondatrice
| Adresse email | Fichier signature | Statut |
|---------------|-------------------|--------|
| coralie@kmoove-pro.com | `Coralie Rodriguez/signature-kmoove-pro.html` | OK |
| coralie@kmoove-sales.com | `Coralie Rodriguez/signature-kmoove-sales.html` | OK |
| coralie@kmoove-ventes.com | `Coralie Rodriguez/signature-kmoove-ventes.html` | OK |
- **Téléphone :** +33 7 43 39 77 08
- **Site web :** https://apa-kmoove.com/
- **Lieux :** Lyon / Paris / Lille
- **Photo :** `images/photo-coralie.jpeg` (6 Ko, compressée)

### Karim Mounassib — À compléter
- Photo : à fournir → placer dans `images/photo-karim.jpg`
- Poste, téléphone, adresses email : à fournir

### Olivier Cardiner — À compléter
- Photo : à fournir → placer dans `images/photo-olivier.jpg`
- Poste, téléphone, adresses email : à fournir

## Images partagées (badges) — hébergées sur GitHub Pages
| Image | Fichier | URL publique | Taille |
|-------|---------|-------------|--------|
| Photo Coralie | `photo-coralie.jpeg` | `https://kmoovegame104.github.io/email-assets/images/photo-coralie.jpeg` | 6 Ko |
| Badge UGAP | `badge-ugap.jpg` | `https://kmoovegame104.github.io/email-assets/images/badge-ugap.jpg` | 7 Ko |
| Prix Salon Sports 2025 | `prix-salon-sports.jpg` | `https://kmoovegame104.github.io/email-assets/images/prix-salon-sports.jpg` | 9 Ko |

## Hébergement images
- **Repo :** KMOOVEGAME104/email-assets (public)
- **GitHub Pages :** https://kmoovegame104.github.io/email-assets/
- **Branche :** master

## Checklist anti-spam (appliquée à TOUTES les signatures)
- [x] Layout 100% `<table>` (pas de flexbox/grid — incompatible Outlook)
- [x] CSS inline uniquement (pas de `<style>` block — ignoré par Gmail)
- [x] `width` + `height` fixes en pixels sur chaque image (empêche le zoom)
- [x] `display: block` sur toutes les images (empêche espacement fantôme)
- [x] `border="0"` sur toutes les images (empêche bordure bleue de lien)
- [x] Images compressées < 10 Ko chacune (total < 25 Ko)
- [x] HTTPS partout (HTTP = bloqué par Gmail)
- [x] Hébergement github.io (domaine de confiance, jamais blacklisté)
- [x] Pas de base64 (bloqué par Gmail, Outlook)
- [x] Pas de SVG (non supporté par beaucoup de clients)
- [x] Pas de JavaScript (bloqué partout)
- [x] Ratio texte/images correct (assez de texte visible)
- [x] SPF/DKIM/DMARC configurés sur kmoove-pro.com (confirmé)
- [x] Alt text descriptif sur chaque image (affichage si images bloquées)
- [x] Liens vers domaine propre (apa-kmoove.com) — pas de shorteners

## Processus pour ajouter un nouveau collègue
1. Placer la photo dans `images/photo-prenom.jpg`
2. Compresser (200x200px, JPEG quality 75, < 10 Ko)
3. Demander : nom, poste, téléphone, adresses email
4. Dupliquer un fichier signature existant → changer nom/poste/email/photo
5. `git push` → GitHub Pages met à jour les images automatiquement
6. Donner le code HTML au collègue

## Notes
- Ce CLAUDE.md est SPÉCIFIQUE à ce projet (dossier SIGNATURE uniquement)
- Ne pas confondre avec les CLAUDE.md des projets KMOOVE (jeux Python)
