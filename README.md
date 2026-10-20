# KOReader (mkulik) — repozytorium KPM

Repozytorium [KPM](https://github.com/KindleModding/KPM) z paczką zmodyfikowanego
KOReadera dla Kindle.

## Wymagania

- Kindle z KPM,
- platforma `kindlepw2` (Kindle Paperwhite 2 i nowsze, w tym Kindle Basic 4 / 10. generacji).

## Instalacja

Najpierw usuń oficjalny pakiet KOReadera z KPM, jeśli jest zainstalowany:

```text
;kpm uninstall koreader
```

Dodaj to repozytorium:

```text
;kpm add-repo https://raw.githubusercontent.com/michalkulik/kpm-koreader/main/manifest.json
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

Wydanie: [`v2026.26`](https://github.com/michalkulik/koreader/releases/tag/v2026.26)

Plik: `koreader-mkulik_2026.26.0_kindlepw2.kpkg`
