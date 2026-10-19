# dictionary-app-releases

Gotowe wydania aplikacji **Słownik** na Androida (kod: prywatne repo
[dictionary-app](https://github.com/JacekWalczak92/dictionary-app)).

Najnowsza wersja: [Releases → Latest](https://github.com/JacekWalczak92/dictionary-app-releases/releases/latest).
Wymaga Androida 8.0 lub nowszego.

Od wersji 21 słówka z historii można wysłać do aplikacji webowej
[J-Learner English Lessons](https://github.com/JacekWalczak92/english-lessons)
(karta „Moje słówka”): Historia → Eksportuj → **Wyślij do J-Learner**.

## Jak powstaje release

Release publikuje workflow *Release APK* z prywatnego repozytorium dictionary-app
(push taga `v*` albo ręcznie z Actions). APK jest podpisane stałym kluczem,
a jego odcisk SHA-256 jest w opisie każdego release'u.
