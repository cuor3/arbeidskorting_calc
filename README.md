# Arbeidskorting Kalkulator (NL 2021–2026)

Statyczna aplikacja (jeden plik `index.html`) obliczająca okres pracy w dniach (z 360) na podstawie arbeidskorting z jaaropgaave.

## Publikacja na GitHub Pages
1. Utwórz nowe repozytorium na GitHub (np. `arbeidskorting-kalkulator`).
2. Wgraj wszystkie pliki z tego folderu (`index.html`, `.nojekyll`, `README.md`) do gałęzi `main`.
3. Settings → Pages → Source: **Deploy from a branch** → Branch: `main` / `/ (root)` → Save.
4. Po ok. minucie strona będzie pod adresem `https://<użytkownik>.github.io/<repozytorium>/`.

## Logika
- D > P3 → 360 dni
- P2 < D ≤ P3 → MIN(360, AK / V3 × 360)
- D ≤ P2 → MIN(360, AK / V2 × 360)

Parametry roczne znajdują się w obiekcie `PARAMS` w `index.html`. Aby dodać kolejny rok, dopisz nowy wpis i opcję w `<select id="rok">`.
