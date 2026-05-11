# IMMC 2025 — Global Sports League

- **Cel projektu:** zaprojektowanie globalnej ligi sportowej od zera: wybór dyscypliny, wybór klubów, ranking zespołów, terminarz sezonu oraz analiza kosztów, zmęczenia i prawdopodobieństwa wyłonienia zwycięzcy.

- **Główna idea:** stworzyliśmy kompletny, data-driven framework dla Global Sports League, który łączy matematykę, optymalizację, modelowanie probabilistyczne i analizę logistyczną.

- **Praca grupowa:** projekt powstał zespołowo; miałem wpływ na całość paperu i uczestniczyłem w pisaniu każdego fragmentu kodu. Kody, w których mój udział wynosił **99%+**, zostały załączone oddzielnie.

- **Sport Suitability Score (SSS):** autorska metryka do wyboru najlepszego sportu dla globalnej ligi. Łączy popularność, częstotliwość rozgrywania meczów, różnorodność kontynentalną i brak dominacji jednego kraju.

- **Web scraping danych:** używaliśmy narzędzi takich jak **Selenium** i **BeautifulSoup**, żeby automatycznie zbierać oraz przetwarzać dane rankingowe potrzebne do analizy sportów i drużyn.

- **Zmodyfikowany system ELO:** stworzyliśmy własny ranking klubów piłkarskich oparty na wynikach z wielu lig i turniejów. Model uwzględnia siłę ligi oraz wagę rozgrywek międzynarodowych, więc nie jest to zwykłe “sortowanie drużyn”, tylko pełny system oceny jakości zespołów.

- **CP-SAT / OR-Tools:** do wygenerowania poprawnego terminarza użyliśmy constraint programming. Solver znajduje harmonogram spełniający twarde ograniczenia, np. liczba meczów, kolejki, pary drużyn oraz serie dom/wyjazd.

- **Simulated Annealing:** po znalezieniu poprawnego terminarza optymalizowaliśmy go heurystycznie, minimalizując dystans podróży, koszty finansowe, ślad środowiskowy i nierówności między drużynami.

- **Geometria na kuli ziemskiej:** dystanse między klubami liczyliśmy z użyciem odległości po powierzchni Ziemi, a nie prostych odległości na mapie, co lepiej oddaje realną logistykę podróży międzykontynentalnych.

- **Model jet lagu:** godziny meczów wyznaczaliśmy przez modelowanie rytmu dobowego zespołów funkcją cosinus. Dzięki temu terminarz nie tylko działa, ale też próbuje być sprawiedliwy biologicznie dla drużyn z różnych stref czasowych.

- **Model probabilistyczny:** analizowaliśmy, z jakim prawdopodobieństwem liga wyłoni rzeczywiście najlepszą drużynę. W kodzie wykorzystujemy m.in. wartości oczekiwane, wariancje i rozkład normalny z `scipy.stats`.

- **Balanced K-Means (Machine Learning) dla 24 drużyn:** dla rozszerzonej ligi zastosowaliśmy dynamiczne klastrowanie drużyn. Model łączy geografię i siłę sportową, żeby mecze były jednocześnie logistycznie sensowne i sportowo interesujące.

- **Dynamiczne re-clustering:** po kolejnych rundach drużyny są grupowane ponownie na podstawie wyników, co utrzymuje wysoki poziom rywalizacji i pozwala skalować ligę bez niszczenia kalendarza.

- **Stack technologiczny:** Python, Jupyter Notebook, NumPy, SciPy, Matplotlib, Pandas, Selenium, BeautifulSoup, OR-Tools / CP-SAT oraz własne algorytmy optymalizacyjne.

- **Zawartość repo:**
  - `2025003 (1).pdf` — pełny paper z opisem modelu, założeń, wyników i appendixami z kodem.
  - `IMMC_2025_probabilities.ipynb` — osobny notebook z modelem probabilistycznym, w którym mój wkład wynosił 99%+.
