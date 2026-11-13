# 3D Workspace

Pracovní prostor pro 3D modely, Blender scény, přípravu pro tisk, vizualizace a pomocné skripty.

Každý projekt má vlastní složku v `projects/`. Jeho README uvádí zadání, rozměry, použité aplikace, aktuální zdrojovou scénu a stav exportů.

## Projekty

| Projekt | Účel | Stav |
|---|---|---|
| [ranger_50mm](projects/ranger_50mm/README.md) | Figurka rangera pro tisk, cílová výška 50 mm | Připravena struktura; modely dosud nenahrány |

## Orientace

| Cesta | Obsah |
|---|---|
| `projects/<projekt>/source/blender/` | Upravitelné scény .blend |
| `projects/<projekt>/source/cad/` | Zdrojové CAD modely, například .3dm nebo .scad |
| `projects/<projekt>/references/` | Reference, skici a podklady |
| `projects/<projekt>/textures/` | Textury a materiálové mapy |
| `projects/<projekt>/exports/stl/` | Tiskové exporty a jednotlivé díly |
| `projects/<projekt>/exports/obj/` | OBJ společně s MTL a texturami |
| `projects/<projekt>/exports/glb/` | Exporty pro prohlížení a předávání |
| `projects/<projekt>/renders/previews/` | Kontrolní náhledy |
| `projects/<projekt>/renders/final/` | Finální prezentační rendery |
| `projects/<projekt>/scripts/` | Skripty konkrétního projektu |
| `projects/<projekt>/docs/` | Technické poznámky, kontroly a historie změn |
| `scripts/blender/` | Společné nástroje pro Blender |
| `docs/` | Společná dokumentace |

Prázdné složky obsahují soubor `.gitkeep`, aby byly zachovány v Gitu. Jakmile obsahují pracovní soubory, lze `.gitkeep` odstranit.

## Jak začít

1. Pro nový projekt zkopíruj [projects/_template/](projects/_template/README.md) do `projects/<nazev_projektu>/`.
2. Vyplň jeho README a přidej odkaz do seznamu projektů výše.
3. Zdrojové modely ukládej do `source/` a textury připojuj relativními cestami.
4. Při předání nebo významné změně vytvoř novou číslovanou verzi.
5. Zdroj, odpovídající exporty a náhledy označ stejným číslem verze.
6. Zapiš aktuální soubory a skutečně provedené kontroly do README projektu.

## Pravidla a návody

- [Pojmenování souborů a verzování](docs/naming.md)
- [Pracovní postup a kontrola exportů](docs/workflow.md)
- [Šablona nového projektu](projects/_template/README.md)
- [Společné skripty](scripts/README.md)

Do repozitáře patří zdrojové scény, potřebné textury, vybrané exporty a náhledy. Automatické zálohy, dočasné soubory a cache vynechává `.gitignore`.

Před přidáním rozsáhlých binárních dat zvol vhodný způsob jejich ukládání, například Git LFS. V této úvodní struktuře Git LFS není nastaven.
