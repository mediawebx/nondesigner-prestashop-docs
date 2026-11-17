[← Index](README.md)

# NonDesigner – Frequently asked questions (FAQ) and troubleshooting

Answers to the most common questions about the **NonDesigner** module for PrestaShop (2D graphic designer for personalized products with print-ready SVG files).

## Compatibility and requirements

### Which PrestaShop versions does NonDesigner work with?
From PrestaShop **1.7.6.1** up to **8.x** and **9.x**.

### Which PHP version does NonDesigner need?
PHP **7.2 to 8.5** is supported. The **GD Library, cURL, Zip and SimpleXML** extensions are required.

### Does NonDesigner require a license to activate?
No. Once installed and configured it is immediately operational. [Details](installation.md).

### Does NonDesigner support PrestaShop Multistore?
Yes. Settings, shapes, fonts and design cleanup support native Multistore; with several stores you can have different configurations and font catalogs for each. In Multistore a control prevents viewing or exporting designs of another store ("Access Denied").

### How does NonDesigner handle fonts with regard to GDPR?
The module does not load fonts from external services in real time: it downloads the `.ttf` files to your server and serves them locally. [Details](module-configuration.md#font-management-tab).

## Print files

### Which files does NonDesigner generate for printing?
For every order received it generates a **vector SVG** file and a **1:1 scale PNG**, managed from the Back Office. [How to download them](orders-and-svg-export.md).

### Which program do I use to open NonDesigner SVG files?
**Inkscape** (free), which also lets you export them to other formats compatible with graphics programs.

### How do I avoid white borders after cutting the printed product?
Set the **bleed margin** (usually 2–3 mm per side; ask your print supplier for the value). [Details](product-dimensions.md#1-bleed-margin-per-side-mm).

### Do the designs appear in order confirmation emails?
No. The email shows a text indicating the presence of a personalized design, which can be viewed in the customer account's order history.

## Common problems

### I upload a large image but the system returns an error. How do I fix it?
**Cause:** the file size exceeds the limit allowed by the module or the server.

**Solution:** check the value in *General Configuration → Maximum user image size (MB)*. If it is correct, check the `upload_max_filesize` and `post_max_size` limits in your server's `php.ini` with your hosting provider. [Details](module-configuration.md#2-maximum-user-image-size-mb).

### Product dimensions are read as 0 / 0 in the frontend. How do I fix it?
**Cause:** you are using the "Distinct attributes" or "Paired values" method, but the attribute name/value contains invalid characters or multiple numbers that are not correctly separated.

**Solution:** reread [How to set the print dimensions](product-dimensions.md). For paired values use the letter `x` (e.g. `50x70`) and **no** hyphens (`-`) or slashes (`/`). For distinct attributes each value must contain only one number.

### Automatic cleanup of abandoned carts is not starting. How do I fix it?
**Cause:** the cronjob URL was not configured correctly in the server panel (cPanel/Plesk).

**Solution:** copy the full URL from the *Tools Configuration* tab and make sure the server performs an **HTTP GET** call (e.g. via `wget` or `curl`). [Details](module-configuration.md#4-abandoned-cart-design-cleanup).

### How do I manage price variations (front/back printing, rounded corners, no printing)?
NonDesigner does not change the price: use PrestaShop's Combinations/Variants. [Guide with practical example](pricing-and-variants.md).

### Can I let customers buy the product without personalization?
Yes: leave the "Enable the Add to cart button" option visible and create a "No printing" variant. [How to](pricing-and-variants.md#a-how-do-i-also-sell-the-plain-product-without-printing).

## Support

### How do I contact NonDesigner technical support?
Log in to your **PrestaShop Addons** account, go to **My purchases** and send a message to the module's support ticket. Requests are answered within **24–48 business hours**.

---

*Before installing the module, always back up your files and database, and test it on a test server first.*
