# CLAUDE.md — Projet Signature Email KMOOVE

## Objectif
Signature email HTML professionnelle pour Coralie Rodriguez, compatible tous clients email.

## Informations signature
- **Nom :** Coralie Rodriguez
- **Poste :** Fondatrice
- **Société :** KMOOVE
- **Téléphone :** +33 7 43 39 77 08
- **Email :** coralie@kmoove-pro.com
- **Site web :** https://apa-kmoove.com/
- **Lieux :** Lyon / Paris / Lille

## Images (3)
1. `photo-coralie.jpg` — Photo portrait Coralie Rodriguez
2. `badge-ugap.png` — Badge "Produit sélectionné par UGAP" (fond blanc, logo rouge)
3. `prix-salon-sports.png` — Prix de l'Innovation Salon des Sports et Parasports 2025

## Hébergement images
- **GitHub Pages** sur repo KMOOVEGAME104/email-assets (ou similaire)
- URLs format : `https://kmoovegame104.github.io/email-assets/images/<fichier>`
- Les images DOIVENT être en URL publique pour compatibilité email universelle

## Contraintes techniques (signature email)
- Layout 100% en `<table>` (pas de flexbox/grid)
- CSS inline uniquement (pas de `<style>` block)
- Images avec `width` + `height` explicites (évite le zoom)
- `display: block` sur toutes les images
- `border="0"` sur toutes les images
- Largeur max signature : ~600px
- Pas de base64 (bloqué par Gmail, Outlook)
- Pas de SVG (non supporté par beaucoup de clients)

## Fichiers
- `signature.html` — Signature HTML complète
- `images/` — Dossier local des images source (à uploader sur GitHub Pages)
