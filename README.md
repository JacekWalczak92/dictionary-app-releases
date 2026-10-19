# dictionary-app-releases

Gotowe wydania aplikacji **Słownik** na Androida (kod: prywatne repo
[dictionary-app](https://github.com/JacekWalczak92/dictionary-app)).

Najnowsza wersja: [Releases → Latest](https://github.com/JacekWalczak92/dictionary-app-releases/releases/latest).
Wymaga Androida 8.0 lub nowszego.

Od wersji 21 słówka z historii można wysłać do aplikacji webowej
[J-Learner English Lessons](https://github.com/JacekWalczak92/english-lessons)
(karta „Moje słówka”): Historia → Eksportuj → **Wyślij do J-Learner**.

## Jak powstaje release

Kod źródłowy w dictionary-app jest prywatny, dlatego workflow potrzebuje sekretu `SOURCE_TOKEN`:
fine-grained token GitHub z dostępem tylko do repozytorium dictionary-app i uprawnieniem
**Contents: Read-only**.

Actions → **Release APK** → Run workflow, w polu `tag` wpisz np. `v21.0`
(opcjonalnie `source_ref` = gałąź/commit z dictionary-app). Workflow pobiera kod,
buduje APK i publikuje je tutaj z sumą SHA-256.

APK jest podpisywane kluczem z sekretów tego repozytorium: `ANDROID_KEYSTORE_BASE64`,
`ANDROID_KEYSTORE_PASSWORD`, `ANDROID_KEY_ALIAS`, `ANDROID_KEY_PASSWORD`.
Bez nich APK dostaje jednorazowy klucz debug i nie zaktualizuje wcześniejszej instalacji
(trzeba ją wtedy odinstalować — historia słówek w telefonie zniknie, więc najpierw ją wyeksportuj).
