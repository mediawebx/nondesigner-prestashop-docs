[← Sommaire](README.md)

# NonDesigner – Questions fréquentes (FAQ) et dépannage

Réponses aux questions les plus courantes sur le module **NonDesigner** pour PrestaShop (designer graphique 2D pour produits personnalisés avec fichiers SVG prêts à imprimer).

## Compatibilité et configuration requise

### Avec quelles versions de PrestaShop NonDesigner fonctionne-t-il ?
De PrestaShop **1.7.6.1** jusqu'aux versions **8.x** et **9.x**.

### Quelle version de PHP faut-il pour NonDesigner ?
Les versions de **PHP 7.2 à 8.5** sont prises en charge. Les extensions **GD Library, cURL, Zip et SimpleXML** sont requises.

### NonDesigner nécessite-t-il l'activation d'une licence ?
Non. Une fois installé et configuré, il est immédiatement opérationnel. [Détails](installation.md).

### NonDesigner prend-il en charge le Multiboutique de PrestaShop ?
Oui. Les paramètres, formes, polices et le nettoyage des designs prennent en charge le Multiboutique natif ; avec plusieurs boutiques, vous pouvez avoir des configurations et des catalogues de polices différents pour chacune. En Multiboutique, un contrôle empêche d'afficher ou d'exporter les designs d'une autre boutique (« Accès refusé »).

### Comment NonDesigner gère-t-il les polices au regard du RGPD ?
Le module ne charge pas les polices depuis des services externes en temps réel : il télécharge les fichiers `.ttf` sur votre serveur et les sert localement. [Détails](configuration-module.md#onglet-gestion-des-polices).

## Fichiers d'impression

### Quels fichiers NonDesigner génère-t-il pour l'impression ?
Pour chaque commande reçue, il génère un fichier **SVG vectoriel** et un **PNG à l'échelle 1:1**, gérés depuis le back office. [Comment les télécharger](commandes-et-export-svg.md).

### Avec quel logiciel ouvrir les fichiers SVG de NonDesigner ?
Avec **Inkscape** (gratuit), qui permet aussi de les exporter vers d'autres formats compatibles avec les logiciels de graphisme.

### Comment éviter les marges blanches après la découpe du produit imprimé ?
Définissez la **marge de fond perdu** (généralement 2-3 mm par côté ; demandez la valeur à votre imprimeur). [Détails](dimensions-produit.md#1-marge-de-fond-perdu-par-côté-mm).

### Les designs apparaissent-ils dans les e-mails de confirmation de commande ?
Non. L'e-mail contient un texte indiquant la présence d'un design personnalisé, consultable dans l'historique des commandes du compte client.

## Problèmes fréquents

### Je télécharge une grande image, mais le système renvoie une erreur. Comment résoudre ce problème ?
**Cause :** la taille du fichier dépasse la limite autorisée par le module ou par le serveur.

**Solution :** vérifiez la valeur définie dans *Configuration Générale → Taille maximale des images utilisateur (Mo)*. Si elle est correcte, vérifiez avec votre hébergeur les limites `upload_max_filesize` et `post_max_size` dans le fichier `php.ini` du serveur. [Détails](configuration-module.md#2-taille-maximale-des-images-utilisateur-mo).

### Les dimensions du produit sont lues comme 0 / 0 dans le frontend. Comment résoudre ce problème ?
**Cause :** vous utilisez la méthode « Attributs distincts » ou « Valeurs associées », mais le nom/valeur de l'attribut contient des caractères non valides ou plusieurs nombres mal séparés.

**Solution :** reportez-vous à [Comment définir les dimensions d'impression](dimensions-produit.md). Pour les valeurs associées, utilisez la lettre `x` (par exemple `50x70`) et **ni** tiret (`-`) **ni** barre oblique (`/`). Pour les attributs distincts, chaque valeur ne doit contenir qu'un seul nombre.

### Le nettoyage automatique des paniers abandonnés ne démarre pas. Comment résoudre ce problème ?
**Cause :** l'URL de la tâche Cron n'a pas été correctement configurée dans le panneau du serveur (cPanel/Plesk).

**Solution :** copiez l'URL complète affichée dans l'onglet *Configuration des outils* et assurez-vous que le serveur effectue un appel **HTTP GET** (par exemple via `wget` ou `curl`). [Détails](configuration-module.md#4-nettoyage-des-designs-des-paniers-abandonnés).

### Comment gérer les différences de prix (recto/verso, angles arrondis, sans impression) ?
NonDesigner ne modifie pas le prix : utilisez les combinaisons/déclinaisons de PrestaShop. [Guide avec exemple pratique](prix-et-declinaisons.md).

### Puis-je permettre l'achat du produit sans personnalisation ?
Oui : laissez visible l'option « Activer le bouton Ajouter au panier » et créez une déclinaison « Sans impression ». [Comment faire](prix-et-declinaisons.md#a-comment-vendre-aussi-le-produit-neutre-sans-impression-).

## Assistance

### Comment contacter l'assistance technique de NonDesigner ?
Connectez-vous à votre compte **PrestaShop Addons**, accédez à **Mes achats** et envoyez un message via le ticket d'assistance du module. Les demandes reçoivent une réponse sous **24 à 48 heures ouvrables**.

---

*Avant d'installer le module, effectuez toujours une sauvegarde de vos fichiers et de votre base de données, et testez-le d'abord sur un serveur de test.*
