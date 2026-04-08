# CLAUDE.md — Projet Signature Email KMOOVE

## Objectif
Signature email HTML professionnelle pour Coralie Rodriguez, compatible tous clients email (Gmail, Outlook, Apple Mail, Thunderbird).

## Informations signature
- **Nom :** Coralie Rodriguez
- **Poste :** Co-fondatrice
- **Société :** KMOOVE
- **Téléphone :** +33 7 43 39 77 08
- **Email :** coralie@kmoove-pro.com
- **Site web :** https://apa-kmoove.com/
- **Lieux :** Lyon / Paris / Lille

## Images (3) — hébergées sur GitHub Pages
| Image | Fichier | URL publique | Taille |
|-------|---------|-------------|--------|
| Photo portrait Coralie | `photo-coralie.jpeg` | `https://kmoovegame104.github.io/email-assets/images/photo-coralie.jpeg` | 6 Ko |
| Badge UGAP | `badge-ugap.jpg` | `https://kmoovegame104.github.io/email-assets/images/badge-ugap.jpg` | 7 Ko |
| Prix Salon des Sports 2025 | `prix-salon-sports.jpg` | `https://kmoovegame104.github.io/email-assets/images/prix-salon-sports.jpg` | 9 Ko |

**Total images : 22 Ko** (compressées depuis 960 Ko — ratio x43)

## Hébergement
- **Repo :** KMOOVEGAME104/email-assets (public)
- **GitHub Pages :** https://kmoovegame104.github.io/email-assets/
- **Branche :** master

## Contraintes techniques anti-spam
- Layout 100% en `<table>` (pas de flexbox/grid — incompatible Outlook)
- CSS inline uniquement (pas de `<style>` block — ignoré par Gmail)
- Images avec `width` + `height` explicites en pixels (empêche le zoom)
- `display: block` sur toutes les images (empêche espacement fantôme)
- `border="0"` sur toutes les images (empêche bordure de lien bleue)
- Images compressées < 10 Ko chacune (anti-spam + chargement rapide)
- HTTPS obligatoire (HTTP = bloqué par Gmail)
- Pas de base64 (bloqué par Gmail, Outlook)
- Pas de SVG (non supporté par beaucoup de clients)
- Pas d'emojis Unicode dans le texte (certains clients les affichent mal) — utiliser `&#xxxxx;` HTML entities
- SPF/DKIM/DMARC configurés sur kmoove-pro.com (confirmé par l'utilisateur)

## Fichiers
- `signature.html` — Signature HTML complète (prête à copier-coller)
- `images/` — Dossier des images compressées (source + hébergées sur GitHub Pages)

## Notes importantes
- Ce CLAUDE.md est SPÉCIFIQUE à ce projet (dossier SIGNATURE uniquement)
- Ne pas confondre avec les CLAUDE.md des projets KMOOVE (jeux Python)
- Mémoire de ce projet stockée dans le memory/ de ce dossier projet uniquement
