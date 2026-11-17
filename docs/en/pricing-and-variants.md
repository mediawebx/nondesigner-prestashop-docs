[← Index](README.md) · [← Orders and SVG export](orders-and-svg-export.md) · Next page: [FAQ →](faq.md)

# How to manage prices and variants of personalized products with NonDesigner

## Does NonDesigner change the product price?

No. The **NonDesigner** module manages **only the graphic interface** and the visual personalization experience; it **does not directly modify the product's price**.

All price variations (surcharges or discounts for processing options, such as front/back printing, rounded corners or no printing) must be handled through **PrestaShop's native Combinations/Variants**.

## How do I set the price for front/back printing, rounded corners or no printing? (practical example)

### A. How do I also sell the plain product without printing?

To offer both the raw/plain product and the personalized one:

1. Create an attribute group (e.g. **"Printing"**) and include the option **"No printing"** (or "No personalization") among its values.
2. Assign the "No printing" value the **base price** of the unprocessed product.
3. Set the **Enable the "Add to cart" button** option to **Yes** (see [Product configuration](product-configuration.md#what-does-the-enable-the-add-to-cart-button-option-do)).

### B. How do I set surcharges for printing options?

1. Create the values for the printed options (e.g. **"Front Only Printing"**, **"Front and Back Printing"**, **"Rounded Corners"**).
2. In PrestaShop's **Combinations** panel, set the **price impact** (surcharge) for each combination that involves processing.
3. In the product's **NonDesigner** tab, **map the attribute values** to the module's corresponding options (e.g. link "Front and Back Printing" to the designer's Front/Back mode). See [front/back printing](product-configuration.md#how-do-i-set-up-frontback-printing) and [rounded corners](product-configuration.md#how-do-i-set-rounded-corners).

### Result

When the customer chooses the variant on the product page **before opening the designer**, PrestaShop automatically calculates and applies the **correct price in the cart**.

---

Next page: [FAQ →](faq.md)
