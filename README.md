# Héon

Navigateur web pour Mac, inspiré d’Arc : onglets verticaux, espaces, dossiers, Peek, split view, bloqueur de publicités et une barre de commande pour tout faire au clavier. Construit sur Electron (moteur Chromium).

Ce dépôt ne contient que les installeurs de Héon et ce mode d’emploi.

## Installer

1. **[Télécharger la dernière version](https://github.com/Andre27aj/heon-versions/releases/latest)** : dans « Assets », le fichier `Heon-X.Y.Z-arm64.dmg` (Mac avec puce Apple : M1, M2, M3, M4…).
2. Ouvrir le `.dmg` et glisser **Héon** dans le dossier **Applications**.
3. **Premier lancement** : Héon n’est pas notarié par Apple (c’est payant), macOS le bloque donc la première fois.
   - Ouvrir Héon une fois (macOS affiche un avertissement), puis aller dans **Réglages Système → Confidentialité et sécurité**, tout en bas : **« Ouvrir quand même »** à côté de Héon, et confirmer.
   - Ou, dans le Terminal : `xattr -dr com.apple.quarantine /Applications/Heon.app`
4. Au premier lancement, Héon propose d’importer tes espaces, onglets épinglés et favoris d’**Arc** (et, dans les réglages, depuis Chrome, Brave, Edge ou Safari).

## Mises à jour

Héon vérifie au démarrage, puis toutes les heures, si une nouvelle version est publiée ici. Si oui, une notification « Héon X.Y.Z est prête » apparaît : **Redémarrer** installe la nouvelle version et rouvre Héon avec les mêmes onglets.

Chaque mise à jour est **signée** : Héon vérifie la signature avant de l’installer et refuse toute version qui ne vient pas du développeur.

## Fonctionnalités

- **Espaces** avec leur couleur, leurs onglets épinglés et leurs dossiers ; **favoris** partagés en haut de la barre latérale ; **onglets du jour** archivés automatiquement après 12 h d’inactivité.
- **Profil séparé** par espace (comptes et cookies à part), **fenêtre de navigation privée** (⇧⌘N) et **espace privé** (⇧⌘P) : rien n’est gardé.
- **Barre de commande** (⌘T) : onglets, historique, actions. **Peek** (⇧ clic sur un lien) : la page s’ouvre par-dessus, sans créer d’onglet. **Split view**.
- **Little Héon** : un lien cliqué dans une autre app s’ouvre dans une petite fenêtre ; **⌘O** l’ouvre dans l’espace actuel. Règles « tel site → tel espace ».
- **Plusieurs onglets à la fois** : ⇧ clic (plage) ou ⌘ clic, puis clic droit (fermer, épingler, déplacer, nouveau dossier…).
- **Bloqueur de publicités et de traqueurs**, désactivable par site (clic droit sur la page).
- **Vitesse des vidéos** (pastille sur chaque vidéo, touches S / D / R), **image dans l’image automatique**.
- **YouTube** sans miniatures ni Shorts (optionnel), **Boosts** : ton propre CSS / JS pour n’importe quel site.
- **Mots de passe** : enregistrement et remplissage, chiffrés dans le trousseau macOS, Touch ID pour les afficher ; import CSV.
- **Extensions Chrome** : bouton « Ajouter à Héon » sur le Chrome Web Store (une partie des extensions seulement).
- **Téléchargements** (⌥⌘L), **PDF**, **impression** (⌘P), **traduction** de page (⌥⌘T).

## Sécurité et vie privée

- HTTPS uniquement, DNS chiffré, liens nettoyés des paramètres de pistage, protection contre l’hameçonnage et les sites malveillants.
- Chaque page tourne isolée (bac à sable Chromium) ; les permissions (caméra, micro, position…) sont demandées site par site.
- Cookies et mots de passe chiffrés sur le disque. Aucune donnée n’est envoyée au développeur : pas de compte, pas de statistiques.
- Tout est réglable dans **Addons et sécurité** (⇧⌘A).

## Raccourcis

| Raccourci | Action |
| --- | --- |
| ⌘T | Barre de commande / nouvel onglet |
| ⌘L | Modifier l’adresse |
| ⌘N / ⇧⌘N | Nouvelle fenêtre / fenêtre de navigation privée |
| ⌘W / ⇧⌘T | Fermer / rouvrir un onglet |
| ⌘D | Épingler / désépingler |
| ⌘S | Afficher / masquer la barre latérale |
| ⌃⇧= | Split view |
| ⌘O | (Little Héon) ouvrir dans l’espace actuel |
| ⇧⌘A | Addons et sécurité |
| ⌥⌘P | Mots de passe |
| ⌥⌘L | Téléchargements |
| ⌥⌘T | Traduire la page |
| ⌘F, ⌘±, ⌘0 | Recherche, zoom |

## Désinstaller

Mettre **Héon** (dans Applications) à la corbeille. Les données restent dans `~/Library/Application Support/Arco` : supprimer ce dossier pour tout effacer.

## Limites connues

- Mac avec puce Apple uniquement (pas de version Intel pour l’instant).
- Pas de Netflix, Disney+ ni autre vidéo protégée.
- Pas de clés d’accès (passkeys) : utiliser le mot de passe (« Essayer une autre méthode »).
- Extensions Chrome : une partie seulement fonctionne.
