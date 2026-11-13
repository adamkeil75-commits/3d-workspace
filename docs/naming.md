# Pojmenování a verzování

## Základní pravidla

- Názvy projektů a pracovních souborů piš malými písmeny bez diakritiky a mezer.
- Slova odděluj podtržítkem.
- Používej písmena a–z, číslice a podtržítko; tečku použij před příponou.
- Dokumentační soubory `README.md` a technické soubory jako `.gitignore` jsou výjimkou.
- Rozměr doplň, pokud odlišuje variantu: `50mm`, `10mm`.
- Verze čísluj třemi číslicemi od `v001`.
- Název projektu po zahájení práce neměň bez aktualizace odkazů a cest.

Základní vzor: `projekt_cast_varianta_v001.pripona`. Nepotřebné části vynech.

| Účel | Příklad |
|---|---|
| Zdrojová scéna | `ranger_50mm_v003.blend` |
| CAD zdroj | `travertin_sklo_10mm_v002.3dm` |
| Celkový export | `ranger_50mm_v003.glb` |
| Samostatná část pro tisk | `ranger_50mm_luk_v003.stl` |
| Náhled | `ranger_50mm_v003_detail_luku.png` |
| Textura | `travertin_basecolor.png` |
| Další materiálové mapy | `travertin_normal.png`, `travertin_roughness.png` |

## Význam verze

Číslo verze propojuje zdroj, exporty a náhledy jednoho stavu modelu. Exporty z `ranger_50mm_v003.blend` tedy nesou `v003`.

Novou verzi vytvoř při významné změně geometrie, materiálů nebo exportního nastavení, která mění předávaný výsledek. Běžné rozpracované ukládání může probíhat v rámci stejné verze; historii změn eviduje Git.

Nepoužívej označení `final_oprava_nove2`. Aktuální doporučený soubor uveď v README projektu jeho přesným názvem a relativním odkazem.

Textury sdílené mezi verzemi mohou mít stabilní názvy. Pokud se jejich obsah mezi předávanými verzemi liší, odděl je verzovanou podsložkou, například `textures/v003/`, a uprav odkazy ve scéně.

## OBJ balíčky

Pro každý předávaný OBJ použij vlastní podsložku, například `exports/obj/ranger_50mm_v003/`. Ulož do ní OBJ, odpovídající MTL a všechny odkazované textury. Ověř funkčnost relativních cest.
