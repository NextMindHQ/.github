# NextMindHQ — GitHub Organization Masterplan

**Rola:** audyt organizacji GitHub jako produktu — UX, brand, engineering.
**Zakres:** cała organizacja `NextMindHQ`, nie tylko README.
**Data audytu:** 2026-08-06
**Źródło danych:** live `github.com/NextMindHQ` (stan publiczny) + zawartość repo `.github` na dysku (jeszcze nie wypchnięta na GitHub).

Ważne zastrzeżenie na start: część ustawień (email w profilu, twitter/X, verified domain, widoczność członków) jest dostępna tylko właścicielom organizacji w GitHub Settings i nie da się ich zweryfikować z zewnątrz. Tam gdzie tak jest, oznaczam to jako **"do weryfikacji przez Nico"**.

---

## 1. Aktualny stan

Stan faktyczny, zebrany z publicznej strony organizacji, nie z założeń.

| Element | Stan obecny |
|---|---|
| **Nazwa organizacji** | `NextMindHQ` |
| **Avatar** | Obrazek jest ustawiony (nie domyślny identicon GitHub) — wymaga wizualnej weryfikacji, czy to finalne logo, czy tymczasowy placeholder |
| **Opis organizacji (org description)** | *"Building intelligent products powered by modular AI."* — ustawiony w Settings, widoczny w wynikach wyszukiwania Google, social preview i na stronie org |
| **Lokalizacja** | Germany (publiczna) |
| **Website URL w profilu** | brak |
| **README organizacji** | Zaprojektowany lokalnie (v1.1, hero + tabele + siatka wartości), **jeszcze niewypchnięty** — na żywo strona org nie pokazuje żadnego profilu, tylko listę repo |
| **Banner** | Brak. Istnieje tylko brief projektowy (`assets/banner-placeholder.md`), zero pliku graficznego |
| **Social preview (og:image)** | Domyślnie = avatar organizacji w skali 280px — brak dedykowanego obrazu social preview |
| **Pinned / Popular repositories** | Brak możliwości przypięcia — organizacja ma **jedno repozytorium**: `.github` |
| **Nazwy repozytoriów** | Tylko `.github` — nazewnictwo nie do oceny, bo nie ma jeszcze repo produktowych |
| **Opis repozytorium `.github`** | *"NextMindHQ organization profile"* — generyczny, domyślny, nieatrakcyjny (to pole "About" widoczne na karcie repo, niezależne od README) |
| **Gwiazdki / forki / issues** | 0 / 0 / 0 — oczekiwane na tym etapie |
| **Publiczni członkowie** | Brak — "This organization has no public members" |
| **Discussions** | Wyłączone |
| **Projects** | Puste, brak aktywnych tablic |
| **Community Health Files** | Częściowo: `CONTRIBUTING.md` istnieje lokalnie (niewypchnięty), `SECURITY.md` — brak, `CODE_OF_CONDUCT.md` — brak |
| **SECURITY.md** | Brak |
| **CODEOWNERS** | Brak |
| **Issue Templates** | Brak |
| **Pull Request Templates** | Brak |
| **Verified domain / SSO** | Nieznane — do weryfikacji przez Nico |

**Kluczowa obserwacja, która zmienia priorytety:** opis organizacji w ustawieniach GitHub — *"Building intelligent products powered by modular AI."* — mówi dokładnie to, czego strategia brandowa NextMind chce unikać: pozycjonuje firmę jako *AI company*, nie jako firmę technologiczną, dla której AI jest jednym z narzędzi. To pole jest widoczne **zanim ktokolwiek dotrze do README** — w wynikach Google, w linkach social media, na karcie organizacji. Jest to dziś najbardziej niespójny element całego profilu z resztą pracy wykonanej nad README i PROFILE_PLAN.

---

## 2. Mocne strony

Organizacja jest na wczesnym etapie, ale to, co już istnieje, jest spójne i przemyślane:

Nazwa `NextMindHQ` jest krótka, jednoznaczna i dobrze się skaluje jako handle na innych platformach. README (niewypchnięty, ale gotowy) ma wyraźną hierarchię wizualną i unika typowych błędów early-stage firm — brak fałszywych statystyk, brak listy klientów, brak AI-hype'u. Istnieje już dokument `PROFILE_PLAN.md`, czyli firma myśli o profilu GitHub strategicznie, a nie ad hoc. Fakt, że organizacja ma tylko jedno repo i zero aktywności, jest uczciwym stanem, a nie czymś do maskowania — to bardzo dobra pozycja wyjściowa, bo nie trzeba niczego "odkłamywać".

## 3. Słabe strony

Największy problem to rozjazd między tym, co zaprojektowane lokalnie, a tym, co widać na żywo — cała dotychczasowa praca nad README jest niewidoczna dla świata, dopóki nie zostanie wypchnięta. Opis organizacji w Settings koliduje z pozycjonowaniem "nie jesteśmy AI company". Brak bannera i dedykowanego social preview oznacza, że każdy link do organizacji (Slack, X, LinkedIn) pokazuje samo logo na pustym tle zamiast zaprojektowanej karty. Opis repo `.github` to niewykorzystane pole — "NextMindHQ organization profile" nie mówi nic o firmie. Zerowa obecność community health files (SECURITY, CODEOWNERS, templates) nie jest jeszcze problemem wizerunkowym przy jednym repo, ale stanie się nim w chwili, gdy pojawi się pierwsze repo produktowe i ktoś spróbuje zgłosić issue albo lukę bezpieczeństwa bez żadnego szablonu.

## 4. Co warto poprawić — macierz audytu

| Element | Wpływ na wizerunek | Trudność | Priorytet | Rekomendacja |
|---|---|---|---|---|
| Opis organizacji (Settings) | Bardzo wysoki | Bardzo niska | **P0** | Zmienić na krótki opis zgodny z pozycjonowaniem, np. *"Technology company building software, automations, and AI-driven systems."* — jedno zdanie, bez "AI-powered" jako głównej ramy |
| Wypchnięcie README organizacji | Bardzo wysoki | Bardzo niska | **P0** | README już istnieje i jest gotowe — dziś nie generuje żadnej wartości, bo jest tylko na dysku |
| Opis repo `.github` (pole About) | Średni | Bardzo niska | **P0** | Zmienić z domyślnego tekstu na jedno zdanie o firmie, spójne z org description |
| Avatar | Wysoki | Średnia (zależna od designu) | **P1** | Zweryfikować czy obecny plik to finalne logo; jeśli nie — zaprojektować wg specyfikacji z `PROFILE_PLAN.md` (mark, nie wordmark, czytelny w 16px) |
| Banner / social preview | Wysoki | Średnia | **P1** | Zaprojektować wg briefu w `assets/banner-placeholder.md`; ustawić dedykowany social preview w Settings (osobne pole od avatara) |
| Website URL w profilu org | Średni | Bardzo niska (gdy strona istnieje) | **P1** (blokowane przez NextMind Website) | Uzupełnić, gdy tylko domena/strona będzie live — puste pole dziś jest lepsze niż link do "coming soon" |
| SECURITY.md | Niski dziś / wysoki po pierwszym publicznym repo produktowym | Niska | **P2** | Dodać przed upublicznieniem pierwszego repo z realnym kodem |
| CODEOWNERS | Niski dziś | Niska | **P2** | Dodać, gdy pojawi się więcej niż jeden kontrybutor w repo |
| Issue Templates | Niski dziś | Niska | **P2** | Dodać razem z pierwszym publicznym repo produktowym |
| Pull Request Template | Niski dziś | Niska | **P2** | Jak wyżej |
| CONTRIBUTING.md (org-wide) | Niski dziś | Zrobione lokalnie | **P2** | Wypchnąć razem z resztą — już istnieje, czeka na push |
| Discussions | Niski dziś | Bardzo niska (checkbox) | **P3** | Włączyć dopiero, gdy będzie realna społeczność (NextMind Community) — pusta zakładka Discussions szkodzi bardziej niż jej brak |
| Projects | Niski dziś | Bardzo niska | **P3** | Włączyć tylko jeśli roadmapa ma być publiczna — nie ma dziś takiej potrzeby |
| Pinned repositories | Zerowy dziś (brak repo do przypięcia) | Bardzo niska | **P3** | Zaplanowane w `PROFILE_PLAN.md`; aktywować, gdy powstaną pierwsze repo produktowe |
| Nazewnictwo repozytoriów | Zerowy dziś | — | **P3** | Ustalić konwencję (np. `nextmind-business-ai`, `nextmind-os`, `nextmind-website`) zanim powstanie pierwsze publiczne repo, żeby uniknąć późniejszego przenoszenia/przemianowywania |
| Verified domain / e-mail w profilu | Nieznany | Niska | **P2** | Do weryfikacji przez Nico w Settings → sprawdzić czy `hello.nextmindhq@gmail.com` czy docelowa domena firmowa |

---

## 5. Priorytety

**P0 — zrobić natychmiast, koszt bliski zeru, wpływ natychmiastowy.**
Zmiana opisu organizacji w Settings, wypchnięcie już gotowego README, zmiana opisu repo `.github`. Te trzy rzeczy można wykonać w mniej niż 10 minut i już dziś zamykają największy rozjazd między tym, co zaprojektowane, a tym, co publiczne.

**P1 — zrobić w ciągu najbliższych tygodni, wymaga pracy projektowej.**
Avatar (weryfikacja/redesign), banner + social preview. To jedyne elementy wymagające realnej pracy graficznej, a nie tylko decyzji tekstowej.

**P2 — zrobić przed lub w momencie upublicznienia pierwszego repo produktowego.**
SECURITY.md, CODEOWNERS, Issue/PR templates, CONTRIBUTING.md (push), weryfikacja domeny/e-maila. Żadne z nich nie ma dziś realnego adresata (jedno repo, zero kontrybutorów zewnętrznych), ale przygotowanie ich wcześniej kosztuje mniej niż nadrabianie pod presją, gdy pojawi się pierwszy zewnętrzny issue.

**P3 — odłożyć do momentu, gdy będzie realny popyt.**
Discussions, Projects, pinned repos, nazewnictwo repo. Włączenie tych funkcji bez realnej treści za nimi (pusty Discussions, brak repo do przypięcia) obniża wiarygodność bardziej niż ich brak — pusta funkcja czyta się jako porzucony projekt, nie jako firma "w budowie".

---

## 6. Roadmapa GitHub v1.0 — Fundament (dziś / ten tydzień)

Cel: zamknąć rozjazd między tym, co zaprojektowane, a tym, co publiczne. Zero nowych funkcji — tylko uspójnienie tego, co już istnieje.

1. Zmienić opis organizacji w Settings na zdanie zgodne z pozycjonowaniem "technology company".
2. Wypchnąć `profile/README.md` (v1.1) na `main` — dziś jest gotowe i czeka.
3. Zmienić opis repo `.github` (pole About) z domyślnego tekstu na jedno zdanie o firmie.
4. Wypchnąć `CONTRIBUTING.md` razem z resztą.
5. Zweryfikować avatar wizualnie — jeśli to nie finalne logo, oznaczyć jako zadanie do v1.5.

Efekt: organizacja publicznie pokazuje dokładnie to, co już zaprojektowano lokalnie. Zero nowego designu, tylko synchronizacja.

## 7. Roadmapa GitHub v2.0 — Wizerunek (przed lub wraz z pierwszym publicznym repo produktowym)

Cel: dodać warstwę wizualną i przygotować organizację na pierwszych zewnętrznych odwiedzających spoza kręgu, który już zna firmę.

1. Zaprojektować i wgrać banner + finalny avatar wg specyfikacji z `PROFILE_PLAN.md`.
2. Ustawić dedykowany social preview (osobne pole w Settings, nie sam avatar).
3. Ustalić i wdrożyć konwencję nazewnictwa repozytoriów produktowych.
4. Dodać `SECURITY.md`, `CODEOWNERS`, szablony Issue i Pull Request — aktywne od dnia, w którym pierwsze repo produktowe staje się publiczne.
5. Przypiąć pierwsze repozytoria (priorytet wg `PROFILE_PLAN.md`: Business AI → Website → OS).
6. Uzupełnić website URL w profilu organizacji, gdy strona będzie live.

Efekt: organizacja wygląda i zachowuje się jak firma gotowa na zewnętrznych kontrybutorów i obserwatorów, nawet jeśli jeszcze nimi nie zarządza aktywnie.

## 8. Roadmapa GitHub v3.0 — Ekosystem (gdy pojawi się realna społeczność i skala)

Cel: włączyć funkcje, które mają sens tylko przy realnym ruchu i wielu repozytoriach — nie wcześniej.

1. Włączyć Discussions, powiązane z uruchomieniem NextMind Community.
2. Włączyć Projects, jeśli roadmapa produktowa ma być częściowo publiczna.
3. Rozbudować `CONTRIBUTING.md` o pełny proces (branching, review, testy) zamiast obecnej wersji-zapowiedzi.
4. Rozważyć `CODE_OF_CONDUCT.md`, jeśli Discussions/Community generują realny ruch zewnętrzny.
5. Rozważyć program dla zewnętrznych kontrybutorów (dobre pierwsze issues, oznaczenia `good first issue`), jeśli którykolwiek projekt zostanie faktycznie otwarty na kontrybucje spoza zespołu.
6. Regularny przegląd pinned repos — aktualizować w miarę jak zmienia się to, co firma chce eksponować jako flagowe.

Efekt: GitHub przestaje być tylko wizytówką, a zaczyna działać jak platforma społeczności i otwartego ekosystemu wokół NextMind — ale dopiero wtedy, gdy jest do tego realny powód.

---

## Podsumowanie dla Nico

Największa dźwignia jest dziś w rzeczach, które nic nie kosztują: trzy zmiany z sekcji P0 (opis organizacji, push README, opis repo) można zrobić w kwadrans i natychmiast zamykają najpoważniejszą niespójność — organizacja publicznie przedstawia się jako "AI-powered products", podczas gdy cała reszta strategii mówi "technology company, AI to jedno z narzędzi". Wszystko inne (banner, avatar, community files) to praca, którą warto zaplanować, ale która nie pali się tak jak to jedno zdanie w Settings.
