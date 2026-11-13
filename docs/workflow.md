# Pracovní postup a kontrola exportů

## Založení projektu

1. Zkopíruj obsah `projects/_template/` do nové projektové složky.
2. Uprav README: zadání, cílové rozměry, jednotky, aplikace a stav.
3. Přidej projekt do hlavního README.
4. Vlož potřebné podklady a uveď jejich původ a oprávnění k použití, pokud jsou známé.

## Práce se zdrojem

- Blender scény ukládej do `source/blender/`, CAD zdroje do `source/cad/`.
- Textury ukládej do `textures/` a v Blenderu používej relativní cesty.
- Zaznamenej skutečně použitou verzi Blenderu a potřebné doplňky.
- Rozměry, orientaci os a exportní měřítko eviduj pro každý projekt.
- Cache simulací ukládej do složky `cache/`; tato složka se neukládá do Gitu.
- Samotné modely ani textury nejsou vyloučeny z verzování.

## Export pro tisk

- Ověř cílové rozměry a exportní měřítko opětovným importem nebo v sliceru.
- U STL výslovně zapiš zamýšlené jednotky; soubor STL je sám neuchovává.
- Zkontroluj uzavřenost sítě, normály, nežádoucí průniky a tenké části.
- U rozdělených modelů zkontroluj kompletaci dílů a zaznamenej spojovací tolerance.
- Zaznamenej použitý slicer, tiskárnu a materiál, pokud proběhla tisková zkouška.
- Kontrola exportu a ověření skutečným tiskem jsou dva různé stavy.

## OBJ a GLB

- Zapiš exportní jednotky, orientaci os a podstatná nastavení.
- OBJ předej s odpovídajícím MTL a texturami v samostatné podsložce.
- GLB ověř opětovným importem nebo v cílovém prohlížeči.
- Zkontroluj měřítko, materiály, textury a případné animace.

## Předání verze

1. Ulož zdrojovou scénu s číslem verze.
2. Exporty a náhledy pojmenuj shodným číslem verze.
3. Aktualizuj odkazy na aktuální soubory v README projektu.
4. Zapiš datum, rozsah změny a provedené kontroly do dokumentace projektu.
5. Před commitem projdi seznam přidávaných souborů; vynech dočasná data a přihlašovací údaje.
6. Commit popiš konkrétně, například `ranger: upravit polohu luku ve v003`.

Neoznačuj výsledek jako ověřený, dokud příslušná kontrola skutečně neproběhla.
