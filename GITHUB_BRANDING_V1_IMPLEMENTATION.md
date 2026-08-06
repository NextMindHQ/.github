# GitHub Branding v1.0 — Implementation Notes

Companion do `GITHUB_BRANDING_MASTERPLAN.md`. Ten dokument to log wdrożenia v1.0: co zostało zmienione w plikach, jakie ustawienia GitHub wymagają ręcznej akcji, i checklista do odhaczenia.

---

## 1. Zmiany w plikach (ten commit, niewypchnięty)

| Plik | Zmiana |
|---|---|
| `assets/banner.png` | **Nowy.** Finalny banner (1983×793px) skopiowany z załącznika. |
| `profile/README.md` | Sekcja hero (`<h1>NextMind</h1>` + tagline + intro tekstowe) zastąpiona osadzonym bannerem `<img>`. Usunięty duplikat treści — banner już zawiera logo, tagline i 4 filary (Software / Automations / Intelligent Systems / Human First), więc powtarzanie tego samego tekstu pod spodem tworzyło redundancję. Usunięty też pierwszy poziomy separator `---` bezpośrednio pod bannerem — krawędź obrazu sama pełni tę funkcję, dodatkowa linia robiła się zbyt ciężka wizualnie. Reszta sekcji (Building Now, Business AI, How We Build, Contact) — bez zmian strukturalnych, tylko przeniesione bliżej banneru. |
| `assets/banner-placeholder.md` | Status zmieniony z "Not started" na "Shipped in v1.0". Dodana sekcja "Deviations from the original spec" — banner różni się od pierwotnego briefu (zdjęciowe tło zamiast płaskiego, wbudowany tekst i ikony, proporcje 2.5:1 zamiast 2:1). Nieproblematyczne, ale odnotowane na potrzeby ewentualnej rewizji w v2.0. |

Nic innego nie zostało ruszone — `PROFILE_PLAN.md`, `CONTRIBUTING.md`, root `README.md` bez zmian.

---

## 2. Ustawienia GitHub Organization — do zmiany ręcznie

Wszystko poniżej wymaga uprawnień właściciela organizacji i jest dostępne w **github.com/organizations/NextMindHQ/settings**.

| Ustawienie | Gdzie | Wartość do ustawienia | Dlaczego |
|---|---|---|---|
| **Organization Description** | Settings → General → *Organization profile* | `We create technology that makes everyday life easier and gives people more time to do what they enjoy.` | Zatwierdzona wersja. Obecnie ustawione jest *"Building intelligent products powered by modular AI."* — sprzeczne z pozycjonowaniem "technology company, nie AI company". To pole widać w Google, social preview i na karcie organizacji, zanim ktokolwiek dotrze do README. |
| **Repository description (`.github`)** | Repo `.github` → *About* (ikona zębatki przy opisie, prawa kolumna) | Krótkie zdanie spójne z org description, np. `Organization profile & branding for NextMind.` | Obecny opis to domyślne "NextMindHQ organization profile" — nijaki, nieużywający okazji do przekazania czegokolwiek o firmie. |
| **Location** | Settings → General → *Organization profile* | Zostaje `Germany` (już ustawione) | Bez zmian — poprawne i wiarygodne. |
| **Website URL** | Settings → General → *Organization profile* | Zostawić puste do czasu, aż NextMind Website będzie live | Link do "coming soon" wygląda gorzej niż puste pole. Uzupełnić dopiero po starcie strony. |
| **Social preview image** | Settings → General → *Social preview* | Wgrać dedykowany obraz 1280×640px (kadr z `banner.png` lub wersja skrócona) | Domyślnie GitHub używa avatara jako social preview w skali 280px — słabo wygląda przy udostępnianiu linku np. na X czy w Slacku. Osobne pole, niezależne od avatara i od bannera w README. |
| **Avatar** | Settings → General → *Organization profile* → *Upload logo* | Zweryfikować, czy obecny avatar to finalne logo NextMind (mark z bannera, nie cały wordmark) | Wordmark źle się skaluje do 16×16px (favicon). Jeśli obecny avatar to już sama ikona "N" z bannera — zostaje bez zmian. Jeśli to inny placeholder — podmienić. |
| **Pinned repositories** | Strona organizacji → *Customize pins* | Nie dotyczy dziś — brak repo produktowych do przypięcia | Aktywować, gdy powstanie pierwsze repo produktowe (priorytet wg `PROFILE_PLAN.md`: Business AI → Website → OS). |
| **Repository visibility default** | Settings → *Repository defaults* | Verify: nowe repo powinny domyślnie powstawać jako **Private**, publikowane świadomie dopiero gdy gotowe | Zapobiega przypadkowemu upublicznieniu niedokończonego repo. |
| **Member visibility** | Settings → *Member privileges* | Do decyzji Nico — obecnie "This organization has no public members" | Brak publicznych członków jest neutralny na tym etapie; ustawić świadomie, gdy dołączą kolejne osoby. |
| **Email** (kontakt organizacji, jeśli pole istnieje w planie GitHub) | Settings → General | `hello.nextmindhq@gmail.com`, jeśli pole jest dostępne w Twoim planie GitHub | Spójność z kontaktem w README. |
| **Verified domain** | Settings → *Verified domains* | Do rozważenia, gdy istnieje domena `nextmindhq.com` lub podobna | Odblokowuje zieloną plakietkę "Verified" przy organizacji — realny sygnał wiarygodności, ale wymaga posiadanej domeny. Nie blokujące na dziś. |

---

## 3. Checklista — GitHub Branding v1.0

**Pliki (wykonane, czekają na push)**
☑ Banner zapisany jako `assets/banner.png`
☑ `profile/README.md` zaktualizowany o banner, usunięty zduplikowany hero-tekst
☑ `assets/banner-placeholder.md` oznaczony jako shipped
☐ `git add` / `git commit` / `git push` (celowo pominięte w tej sesji — do wykonania przez Nico lub na wyraźne polecenie)

**Ustawienia GitHub (ręczne, do Nico)**
☐ Organization Description → zmienione na zatwierdzoną wersję
☐ Repository description `.github` → zmienione
☐ Social preview image → wgrany dedykowany obraz
☐ Avatar → zweryfikowany / podmieniony jeśli trzeba
☐ Website URL → uzupełnione (dopiero po starcie strony)
☐ Repository visibility default → zweryfikowane
☐ Member visibility → decyzja podjęta świadomie
☐ Verified domain → rozważone (opcjonalne, zależne od posiadania domeny)

**Weryfikacja końcowa**
☐ Podgląd README na GitHub (po pushu) sprawdzony na desktopie
☐ Podgląd README sprawdzony na telefonie (banner + tabele nie rozjeżdżają się)
☐ Link organizacji sprawdzony jako social preview (np. wklejony w prywatnej wiadomości na Slack/X, podgląd karty)

---

## 4. Audyt końcowy — GitHub Branding v1.0

Ocena stanu **po wdrożeniu plikowym, zakładając że powyższa checklista ustawień zostanie odhaczona** (bo część oceny zależy od kroków ręcznych, których nie mogę wykonać za Nico).

| Kryterium | Ocena (1–10) | Uzasadnienie |
|---|---|---|
| **Branding** | 8/10 | Banner + spójna paleta + jeden ton głosu w całym README. Traci punkty, bo banner (fotograficzny, atmosferyczny) i reszta README (płaski, tekstowy, minimalistyczny) to lekko różne rejestry wizualne — nie sprzeczne, ale nie w 100% jednym stylu. |
| **UX** | 8/10 | Jasna hierarchia, banner prowadzi wzrok, sekcje mają rytm. Brak nawigacji wewnętrznej (spis treści) nie jest problemem przy tej długości, ale przy dalszym wzroście README wróci temat. |
| **Professionalism** | 8/10 | Brak hype'u, brak fałszywych metryk, spójny ton. Obniżone do 8, bo dopóki opis organizacji w Settings nie zostanie zmieniony ręcznie, pierwsze wrażenie (Google, social) wciąż mówi "AI-powered products" — niespójnie z resztą. |
| **Trust** | 6/10 | Najniższa ocena i uczciwie — organizacja ma jedno repo, zero publicznej aktywności, zero community health files. To nie błąd wykonania, to naturalny stan firmy na wczesnym etapie. Rośnie automatycznie wraz z v2.0 (SECURITY, CODEOWNERS, pierwsze repo produktowe). |
| **Developer Experience** | 5/10 | Brak CODEOWNERS, Issue/PR templates, SECURITY.md — dla dewelopera, który chciałby dziś coś zgłosić lub skontrybuować, nie ma jeszcze żadnej ścieżki. Zaplanowane w masterplanie na v2.0, celowo nie wdrażane teraz (brak dziś realnego adresata). |
| **First Impression** | 9/10 | To jest najmocniejszy punkt całego wdrożenia — banner + czysty layout dają dokładnie efekt "to wygląda jak prawdziwa firma technologiczna" już w pierwszych sekundach, zanim ktokolwiek przeczyta jedno zdanie. |

**Średnia: 7.3/10.** Rozjazd między wysokim "First Impression" (9) a niższym "Trust"/"Developer Experience" (6, 5) jest oczekiwany i zdrowy dla tego etapu — profil wygląda lepiej niż to, co za nim stoi, ale nie kłamie: nic nie jest udawane, po prostu jeszcze nie zbudowane. To dokładnie odwrotność problemu, którego chcieliście uniknąć (pusty hype bez treści).

---

## 5. Zostawiamy na GitHub Branding v2.0

Zgodnie z priorytetami z masterplanu, celowo nieruszane w v1.0:

- `SECURITY.md`, `CODEOWNERS`, szablony Issue i Pull Request — aktywować wraz z pierwszym publicznym repo produktowym.
- Dedykowany obraz social preview jako osobny plik (dziś rekomendacja to wgranie kadru z bannera — docelowo warto zaprojektować wersję 1280×640 specjalnie pod to pole, bo proporcje bannera 2.5:1 nie są identyczne z formatem social preview).
- Ewentualna rewizja bannera pod kątem spójności stylu z resztą README (patrz sekcja "Deviations" w `assets/banner-placeholder.md`) — nie pilne, tylko odnotowane.
- Pinned repositories, nazewnictwo repo produktowych, Discussions, Projects — bez zmian względem masterplanu, wciąż P2/P3.
