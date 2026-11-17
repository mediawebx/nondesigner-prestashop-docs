[← Sommaire](README.md) · [← Commandes et export SVG](commandes-et-export-svg.md) · Page suivante : [FAQ →](faq.md)

# Comment gérer les prix et les déclinaisons des produits personnalisés avec NonDesigner

## NonDesigner modifie-t-il le prix du produit ?

Non. Le module **NonDesigner** gère **exclusivement l'interface graphique** et l'expérience de personnalisation visuelle ; il **ne modifie pas directement le prix** du produit.

Toutes les différences de prix (majorations ou remises pour les options de traitement, comme l'impression recto/verso, les angles arrondis ou l'absence d'impression) doivent être gérées nativement via les **combinaisons/déclinaisons de PrestaShop**.

## Comment définir le prix de l'impression recto/verso, des angles arrondis ou de l'absence d'impression ? (exemple pratique)

### A. Comment vendre aussi le produit neutre sans impression ?

Pour proposer à la fois le produit brut/non imprimé et le produit personnalisé :

1. Créez un groupe d'attributs (par exemple **« Impression »**) et ajoutez parmi ses valeurs l'option **« Sans impression »** (ou « Aucune personnalisation »).
2. Attribuez à la valeur « Sans impression » le **prix de base** du produit non traité.
3. Définissez l'option **Activer le bouton « Ajouter au panier »** sur **Oui** (voir [Configuration du produit](configuration-produit.md#à-quoi-sert-loption--activer-le-bouton-ajouter-au-panier--)).

### B. Comment définir les majorations pour les options d'impression ?

1. Créez les valeurs pour les options d'impression (par exemple **« Impression recto uniquement »**, **« Impression recto-verso »**, **« Angles arrondis »**).
2. Dans le panneau **Déclinaisons** de PrestaShop, définissez l'**impact sur le prix** (majoration) pour chaque combinaison impliquant un traitement.
3. Dans l'onglet **NonDesigner** du produit, **associez les valeurs d'attribut** aux options correspondantes du module (par exemple, liez « Impression recto-verso » au mode recto/verso du designer). Voir [recto/verso](configuration-produit.md#comment-configurer-limpression-rectoverso-) et [angles arrondis](configuration-produit.md#comment-configurer-les-angles-arrondis-).

### Résultat

Lorsque le client sélectionne la déclinaison sur la page produit **avant d'ouvrir le designer**, PrestaShop calcule et applique automatiquement le **prix correct dans le panier**.

---

Page suivante : [FAQ →](faq.md)
