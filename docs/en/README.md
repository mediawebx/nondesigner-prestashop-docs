# NonDesigner – User Guide and Configuration Manual (English)

**NonDesigner** is a **PrestaShop module** that adds a **2D graphic designer** (product customizer / editor) to the product page. Customers add text, images, shapes, fonts and QR codes to personalize products online, and for every order the module automatically generates **print-ready files: vector SVG and 1:1 PNG**, managed directly from the PrestaShop Back Office.

- Official website: [nondesigner.com/en/](https://www.nondesigner.com/en/)
- Live demo: [nondesigner.com/demonondesigner/](https://www.nondesigner.com/demonondesigner/)
- Buy on PrestaShop Addons: [NonDesigner – 2D graphic designer for custom products](https://addons.prestashop.com/en/product-variants/99215-nondesigner-2d-graphic-designer-for-personalised-products.html)
- Developer: [Media Web](https://www.mediaweb-x.com/)

🌐 **Languages:** English (this guide) · [all languages](../../README.md)

## Main features

- 2D graphic designer in the product page, with panels you can enable one by one: text, images, shapes, layers, QR code, photo filters, image effects.
- Automatic generation of **print-ready vector SVG** and **1:1 PNG** files for every order received.
- **Front/back printing** (front only, identical front/back, different front/back).
- **Three sizing methods** for the print area: fixed dimensions, distinct attributes (width/height) or paired values (W x H).
- Configurable **bleed margin** to avoid white edges after cutting.
- Rectangular or round product shapes, with square or rounded corners.
- Fonts installed **locally on your own server** (no external real-time font loading).
- Native PrestaShop **Multistore** support.
- Automatic (cron) or manual cleanup of abandoned-cart designs.
- No license activation required.

## System requirements at a glance

| Requirement | Value |
|---|---|
| Compatible PrestaShop versions | 1.7.6.1 up to 8.x and 9.x |
| Supported PHP versions | PHP 7.2 to PHP 8.5 |
| Required PHP extensions | GD Library, cURL, Zip, SimpleXML |
| Recommended PHP directives | `upload_max_filesize` ≥ 10M, `post_max_size` ≥ 10M |

Details: [Requirements and installation](installation.md).

## Table of contents

1. [How to install the NonDesigner module on PrestaShop](installation.md) – system requirements, compatibility, installation.
2. [How to configure the NonDesigner module (global settings)](module-configuration.md) – General, Shape Management, Font Management and Tools Configuration tabs, abandoned-cart cleanup.
3. [How to configure the designer on a single product](product-configuration.md) – enabling, front/back printing, product shape, PDF template, bulk apply to a category.
4. [How to set the print dimensions of a product](product-dimensions.md) – bleed margin and the three sizing methods, accepted formats and common mistakes.
5. [How to manage orders and download print-ready SVG files](orders-and-svg-export.md) – design in the Back Office, SVG and JSON export, security.
6. [How to manage prices and variants of personalized products](pricing-and-variants.md) – surcharges for front/back printing, rounded corners, plain product without printing.
7. [Frequently asked questions (FAQ) and troubleshooting](faq.md).

## Support

Log in to your **PrestaShop Addons** account, go to **My purchases** and send a message to the module's support ticket. Requests are answered within 24–48 business hours.

## Important notice

Before installing the module, back up your server files and database and, if possible, test the installation on a test server first.

---

*NonDesigner is developed and distributed by Media Web.*
