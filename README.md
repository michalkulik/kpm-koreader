# KOReader (mkulik) — repozytorium KPM

Repozytorium [KPM](https://github.com/KindleModding/KPM) z paczką zmodyfikowanego
KOReadera dla Kindle.

## Wymagania

- Kindle z KPM,
- platforma `kindlehf` (Kindle z firmware >= 5.16.3, w tym Kindle 10 / KT4) albo `kindlepw2` (starsze Kindle).

## Instalacja

**Uwaga:** `;kpm add-repo https://...` z paska wyszukiwania Kindla nie zadziała.
Kindle `scriptExecutor` odrzuca argumenty zawierające `:` i `.`, więc polecenie
nigdy nie trafia do KPM. Dotyczy to każdego URL-a, także oficjalnego.

Użyj **kterm** albo skryptu (scriptletu) w `/mnt/us/documents/`:

```sh
/var/local/kmc/bin/kpm add-repo https://shelf.mkulik.eu/kpm/manifest.json
/var/local/kmc/bin/kpm update
```

Po dodaniu repo zwykłe polecenia bez URL działają z paska wyszukiwania:

```text
;kpm install koreader-mkulik
```


Główny adres repozytorium (hostowany razem z serwerem półki):

```text
https://shelf.mkulik.eu/kpm/manifest.json
```

Alternatywnie (GitHub Pages):

```text
https://michalkulik.github.io/kpm-koreader/manifest.json
```


Najpierw usuń oficjalny pakiet KOReadera z KPM, jeśli jest zainstalowany:

```text
;kpm uninstall koreader
```

Dodaj to repozytorium:

```text
;kpm add-repo https://shelf.mkulik.eu/kpm/manifest.json
;kpm update
```

Zainstaluj naszą wersję:

```text
;kpm install koreader-mkulik
```

Po instalacji KOReader uruchamia się z **KUAL** oraz przez skrót
`KOReader-mkulik.sh` w `documents`.

## Aktualizacja

```text
;kpm update
;kpm upgrade
```

albo bezpośrednio:

```text
;kpm install koreader-mkulik
```

Ustawienia KOReadera w `/mnt/us/koreader/settings` są zachowywane przy
aktualizacji.

## Ważne

- Pakiet `koreader-mkulik` instaluje aplikację do `/mnt/us/koreader` — tej samej
  lokalizacji co oficjalny pakiet KPM. Nie instaluj obu jednocześnie.
- Po odinstalowaniu naszej paczki KPM usuwa `/mnt/us/koreader`; zrób backup
  `settings`, jeśli chcesz zachować logowanie do półki.
- To repozytorium jest niezależne od oficjalnego repozytorium KindleModding.

## Paczka

Wydanie: [`v2026.41`](https://github.com/michalkulik/koreader/releases/tag/v2026.41)

Pliki:
- `koreader-mkulik_2026.41.0_kindlehf.kpkg` — Kindle 10 / KT4 i inne z FW >= 5.16.3,
- `koreader-mkulik_2026.41.0_kindlepw2.kpkg` — starsze Kindle.
