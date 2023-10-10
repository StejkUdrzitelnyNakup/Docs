---
sidebar_position: 1
---

# Shoptet
Pro napojení na Shoptet je potřeba vytvořit XML feed, který bude obsahovat všechny produkty, které chcete zobrazit na Udržitelném nákupu.

## Instalace XML feedu
1. Přihlašte se do administrace vašeho eshopu
2. V levém menu klikněte na **Propojení** a následně na **XML feedy**
3. Nad tabulkou s XML feedy klikněte na tlačítko **PŘIDAT**
4. Do pole **Název** zadejte název feedu, např. **Udržitelný nákup**
5. Do pole **Název souboru** zadejte název souboru, např. **udrzitelny-nakup**
6. Do polí **Hlavička XML**, **Tělo XML**, **Patička XML** vložte kód níže
7. Přepněte se do záložky **Pokročilé**
8. Zaklikněte **Feed je aktivní**
9. Dále zde lze zakázat určité kategorie, které se do feedu nebudou zahrnovat

### Hlavička XML
```xml
<?xml version="1.0" encoding="UTF-8"?>
<SHOP>
```

### Tělo XML
```xml
<SHOPITEM>
    <ITEM_ID>#CODE#</ITEM_ID>
    <EAN>#EAN#</EAN>
    <PRODUCT_NAME>#NAME#</PRODUCT_NAME>
    <DESCRIPTION>#DESCRIPTION#</DESCRIPTION>
    <SHORT_DESCRIPTION>#SHORT_DESCRIPTION__NO_HTML#</SHORT_DESCRIPTION>
    <IMAGE_MAIN>#IMG_URL#</IMAGE_MAIN>
    <IMAGE>#IMG_ALT_URL1#</IMAGE>
    <IMAGE>#IMG_ALT_URL2#</IMAGE>
    <IMAGE>#IMG_ALT_URL3#</IMAGE>
    <IMAGE>#IMG_ALT_URL4#</IMAGE>
    <IMAGE>#IMG_ALT_URL5#</IMAGE>
    <PRICE>#OLD_PRICE_VAT#</PRICE>
    <PRICE_AFTER_SALE>#PRICE_VAT#</PRICE_AFTER_SALE>
    <URL>#URL#</URL>
    <MANUFACTURER>#MANUFACTURER#</MANUFACTURER>
    <CATEGORY>#COMPLETE_PATH_PIPE#</CATEGORY>
</SHOPITEM>
```

### Patička XML
```xml
</SHOP>
```