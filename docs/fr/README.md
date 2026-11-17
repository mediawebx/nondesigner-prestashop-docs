# NonDesigner – Guide de l'utilisateur et manuel de configuration (français)

**NonDesigner** est un **module PrestaShop** qui ajoute à la fiche produit un **designer graphique 2D** (éditeur / customizer de produits). Les clients ajoutent des textes, images, formes, polices et codes QR pour personnaliser les produits en ligne, et pour chaque commande le module génère automatiquement des **fichiers prêts à imprimer : SVG vectoriel et PNG à l'échelle 1:1**, gérables directement depuis le back office de PrestaShop.

- Site officiel : [nondesigner.com/fr/](https://www.nondesigner.com/fr/)
- Démo en ligne : [nondesigner.com/demonondesigner/fr/](https://www.nondesigner.com/demonondesigner/fr/)
- Acheter sur PrestaShop Addons : [NonDesigner - Designer graphique 2D pour produits personnalisés](https://addons.prestashop.com/fr/declinaisons-de-produits/99215-nondesigner-designer-graphique-2d-pour-produits-personnalises.html)
- Développeur : [Media Web](https://www.mediaweb-x.com/)

🌐 **Langues :** Français (ce guide) · [toutes les langues](../../README.md)

## Fonctionnalités principales

- Designer graphique 2D dans la fiche produit, avec des panneaux activables un à un : texte, images, formes, calques, code QR, filtres photo, effets d'image.
- Génération automatique de fichiers **SVG vectoriels prêts à imprimer** et **PNG 1:1** pour chaque commande reçue.
- Impression **recto/verso** (recto uniquement, recto/verso identique, recto/verso différent).
- **Trois méthodes de calcul de taille** de la zone d'impression : dimensions fixes, attributs distincts (largeur/hauteur) ou valeurs associées (L x H).
- **Marge de fond perdu** configurable pour éviter les marges blanches après la découpe.
- Formes de produit rectangulaires ou rondes, avec angles carrés ou arrondis.
- Polices installées **localement sur votre propre serveur** (aucun chargement externe en temps réel).
- Prise en charge native du **Multiboutique** de PrestaShop.
- Nettoyage automatique (Cron) ou manuel des designs des paniers abandonnés.
- Aucune activation de licence requise.

## Configuration requise en bref

| Exigence | Valeur |
|---|---|
| Versions de PrestaShop compatibles | de 1.7.6.1 à 8.x et 9.x |
| Versions de PHP prises en charge | de PHP 7.2 à PHP 8.5 |
| Extensions PHP requises | GD Library, cURL, Zip, SimpleXML |
| Directives PHP recommandées | `upload_max_filesize` ≥ 10M, `post_max_size` ≥ 10M |

Détails : [Configuration requise et installation](installation.md).

## Sommaire

1. [Comment installer le module NonDesigner sur PrestaShop](installation.md) – configuration requise, compatibilité, installation.
2. [Comment configurer le module NonDesigner (paramètres globaux)](configuration-module.md) – onglets Général, Gestion des formes, Gestion des polices, Configuration des outils, nettoyage des paniers abandonnés.
3. [Comment configurer le designer sur un produit](configuration-produit.md) – activation, impression recto/verso, forme du produit, modèle PDF, application en masse à une catégorie.
4. [Comment définir les dimensions d'impression du produit](dimensions-produit.md) – marge de fond perdu et les trois méthodes de calcul de taille, formats acceptés et erreurs fréquentes.
5. [Comment gérer les commandes et télécharger les fichiers SVG prêts à imprimer](commandes-et-export-svg.md) – design dans le back office, export SVG et JSON, sécurité.
6. [Comment gérer les prix et les déclinaisons des produits personnalisés](prix-et-declinaisons.md) – majorations pour le recto/verso, les angles arrondis, produit sans impression.
7. [Questions fréquentes (FAQ) et dépannage](faq.md).

## Assistance

Connectez-vous à votre compte **PrestaShop Addons**, accédez à **Mes achats** et envoyez un message via le ticket d'assistance du module. Les demandes reçoivent une réponse sous 24 à 48 heures ouvrables.

## Avertissement

Avant d'installer le module, effectuez une sauvegarde des fichiers de votre serveur et de votre base de données et, si possible, testez d'abord l'installation sur un serveur de test.

---

*NonDesigner est développé et distribué par Media Web.*
