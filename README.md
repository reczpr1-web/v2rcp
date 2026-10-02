# ⏱️ System Rejestracji Czasu Pracy — RCP v2
> **Kompleksowy Przewodnik Użytkownika i Instrukcja Obsługi Systemu.**

---

## 📑 Spis treści
1. [Pierwsze kroki: Konfiguracja Wi-Fi (Karta Master)](#1-pierwsze-kroki-konfiguracja-wi-fi-karta-master)
2. [Logowanie do panelu w sieci firmowej](#2-logowanie-do-panelu-w-sieci-firmowej)
3. [Zarządzanie pracownikami (Dodawanie, karty NFC, edycja)](#3-zarządzanie-pracownikami)
4. [Grupy i działy firmy](#4-grupy-i-działy-firmy)
5. [Dostęp do Arkusza Google (Dla kadr i księgowości)](#5-dostęp-do-arkusza-google)
6. [Ewidencja czasu pracy i wydruki (Księgowość)](#6-ewidencja-czasu-pracy-i-wydruki)
7. [Codzienna obsługa czytnika (Dla pracowników)](#7-codzienna-obsługa-czytnika)
8. [Znaczenie diod LED i dźwięków](#8-znaczenie-diod-led-i-dźwięków)
9. [Tryb Offline i kopie zapasowe](#9-tryb-offline-i-kopie-zapasowe)
10. [Pomoc techniczna](#10-pomoc-techniczna)

---

## 1. Pierwsze kroki: Konfiguracja Wi-Fi (Karta Master)

Urządzenie posiada specjalną **Kartę Główną (Master Key)**, która służy do wprowadzania terminala w tryb konfiguracji sieci bez konieczności rozkręcania obudowy czy podłączania kabli.

### Instrukcja połączenia z nową siecią Wi-Fi:

1. **Przyłóż Kartę Master do czytnika.**  
   Terminal zagra melodyjkę, podświetli się na żółto, a na małym ekranie wyświetli się napis **`AP`**.
2. **Połącz się z siecią czytnika:**  
   Na telefonie lub komputerze wejdź w ustawienia Wi-Fi i wybierz sieć:  
   👉 **`RCP Setup`** *(sieć jest otwarta, nie wymaga hasła)*.
3. **Otwórz stronę konfiguracji:**  
   * W większości telefonów na pasku powiadomień pojawi się komunikat: *„Zaloguj się do sieci”* — kliknij go.
   * Jeśli okno nie otworzy się samo, otwórz przeglądarkę internetową i wpisz adres:  
     👉 **`http://rcp.local`** lub **`http://192.168.4.1`**
4. **Wybierz sieć Wi-Fi:**  
   * Kliknij przycisk **„📶 Skonfiguruj sieć Wi-Fi”**.
   * Wybierz swoją sieć firmową z listy, wprowadź hasło i kliknij **„Save”**.
   * Wyświetli się okno z ważnym komunikatem o adresie `rcp.local` oraz 10-sekundowym odliczaniem na przycisku. Po upływie 10 sekund przycisk stanie się zielony i aktywny — kliknij **„Zrozumiałem, połącz z siecią”**.
5. Urządzenie zrestartuje się i połączy z firmowym routerem.

> ℹ️ **Bezpieczeństwo:** Tryb konfiguracji jest w pełni odwracalny. Jeśli w ciągu 3 minut nie wprowadzisz nowej sieci, terminal samoczynnie powróci do normalnej pracy.

---

## 2. Logowanie do panelu w sieci firmowej

Po pomyślnym połączeniu z firmowym Wi-Fi panel zarządzania jest dostępny dla każdego komputera i telefonu podłączonego do tego samego routera:

1. Otwórz przeglądarkę i wpisz:  
   👉 **`http://rcp.local`**
2. *Ważna informacja:* Jeśli firmowy router nie obsługuje nazw mDNS, wejdź w panel routera, sprawdź jaki adres IP przydzielono czytnikowi (np. `192.168.1.150`) i wpisz go bezpośrednio w przeglądarce:  
   👉 **`http://[ADRES_IP_URZĄDZENIA]`**

---

## 3. Zarządzanie pracownikami

W zakładce **👥 Pracownicy** znajduje się pełna lista kadry oraz przypisanych kart zbliżeniowych.

### ➕ Dodawanie nowego pracownika:
1. W prawym górnym rogu kliknij niebieski przycisk **`+ Dodaj pracownika`**.
2. **Krok 1 (Dane osobowe):**
   * **Numer ID:** Unikalny numer pracownika w firmie (np. `1`, `007`, `102`).
   * **Imię i nazwisko:** Np. `Jan Kowalski`.
   * **Indywidualna norma (godz.):** Opcjonalnie (jeśli pracownik ma inny wymiar czasu, np. `4` dla pół etatu. Jeśli puste — pobierana jest norma grupy).
   * **Grupy / Działy:** Wybierz dział pracownika (np. *Magazyn*, *Biuro*).
   * Kliknij **`Dalej →`**.
3. **Krok 2 (Przypisanie karty zbliżeniowej NFC):**
   * **Skanuj kartę:** Terminal na ścianie zaświeci się na niebiesko i przejdzie w tryb odczytu. Wystarczy zbliżyć nową kartę lub brelok do czytnika — numer zostanie automatycznie sczytany i zapisany.
   * **Bez karty:** Jeśli pracownik jeszcze nie otrzymał breloka, kliknij ten przycisk. Kartę będzie można dodać w dowolnym momencie później.

### ✏️ Edycja i usuwanie:
* Kliknij na wiersz pracownika lub przycisk **`✏️ Edytuj`**, aby zmienić nazwisko, wymiar godzin lub przypisać nową kartę (z opcją zachowania starej).
* Aby trwale usunąć pracownika z bazy i pamięci urządzenia, kliknij czerwony krzyżyk **`✕`** (na telefonach: przycisk **`⋮ Opcje`** ➔ **`Usuń pracownika`**).

---

## 4. Grupy i działy firmy

W zakładce **🏷️ Grupy i działy** możesz podzielić załogę na sekcje (np. *Produkcja*, *Biuro*, *Kierowcy*):

1. Kliknij **`+ Nowa grupa`**.
2. Wpisz nazwę działu oraz domyślną dobową normę godzin (np. `8`).
3. Wybierz kolor tła oraz kolor tekstu etykiety dla czytelnej identyfikacji na listach obecności.
4. Kliknij **`Zapisz`**.

Przypisanie grupy pracownikowi automatycznie ustala dla niego czas pracy i pozwala na wygodne filtrowanie raportów.

---

## 5. Dostęp do Arkusza Google

Wszystkie dane trafiają bezpośrednio do zabezpieczonego arkusza kalkulacyjnego online w Google Sheets.

W zakładce **🔐 Dostęp do arkusza**:
* **Bezpośredni podgląd:** Kliknij zielony przycisk **`📗 Otwórz arkusz`**, aby przejść prosto do tabeli w nowej karcie przeglądarki.
* **Nadawanie uprawnień (np. dla Księgowości / Właściciela):**
  1. W polu *„Adres e-mail użytkownika”* wpisz adres Gmail osoby uprawnionej.
  2. Wybierz poziom:
     * **Edytor** — pełne prawo do wprowadzania zmian i korekt.
     * **Przeglądający** — wgląd do raportów tylko do odczytu.
  3. Kliknij **`Przyznaj dostęp`**.
* W tabeli poniżej widzisz listę wszystkich osób mających dostęp z możliwością jego natychmiastowego odebrania przyciskiem **`Odbierz`**.

---

## 6. Ewidencja czasu pracy i wydruki

System automatycznie zlicza godziny, wykrywa spóźnienia oraz nadgodziny:

* **Zakładka 📋 Rejestr obecności:**  
  Widok wszystkich odbić z podziałem na tygodnie. Klikając w dowolny wiersz, kierownik może ręcznie skorygować godziny wejścia/wyjścia lub oznaczyć dzień jako **Urlop wypoczynkowy (UW)** lub **Zwolnienie lekarskie (L4)**.
* **Zakładka 📊 Ewidencja czasu pracy:**  
  Gotowe comiesięczne karty pracy dla każdego pracownika.
* **Wydruk / PDF:**  
  Wybierz pracownika lub zestawienie zbiorcze i kliknij zielony przycisk **`🖨️ Drukuj / PDF`**. Strona automatycznie sformatuje się do czystego dokumentu z polami na **podpis pracownika** oraz **podpis pracodawcy**, gotowego do wpięcia w akta.
* **Eksport CSV:**  
  Przycisk **`⬇️ CSV`** generuje plik zgodny z programami kadrowo-płacowymi (Excel, Optima, Gratyfikant).

---

## 7. Codzienna obsługa czytnika

Dla pracowników rejestracja jest maksymalnie uproszczona:

1. Dotknij lewy panel sensoryczny: **WEJŚCIE (IN)** *(zaświeci się na zielono)*.  
   LUB dotknij prawy panel sensoryczny: **WYJŚCIE (OUT)** *(zaświeci się na czerwono)*.
2. Zbliż kartę lub brelok do czytnika na obudowie.
3. Czytnik wyda dźwięk potwierdzenia, diody błysną i wpis zostanie natychmiast zarejestrowany.

---

## 8. Znaczenie diod LED i dźwięków

| Sygnał świetlny (LED) | Sygnał dźwiękowy | Znaczenie |
| :--- | :--- | :--- |
| **Ciągłe podświetlenie** | Brak | Urządzenie w trybie czuwania, gotowe do pracy. |
| **Podświetlona jedna strona** | Krótki pik | Wybrano Wejście lub Wyjście — przyłóż kartę. |
| **Błysk zielony** | Dźwięk wznoszący | **Pomyślnie zarejestrowano WEJŚCIE**. |
| **Błysk czerwony** | Dźwięk opadający | **Pomyślnie zarejestrowano WYJŚCIE**. |
| **Pulsujący żółty / Ekran: `AP`** | Melodyjka serwisowa | **Aktywny tryb konfiguracji Wi-Fi (Karta Master)**. |
| **Potrójny czerwony błysk** | Niski dźwięk błędu | Karta nieznana, błąd odczytu lub powtórne wejście. |
| **Subtelny czerwony impuls co 2 s** | Brak | **Brak Wi-Fi (Tryb Offline)** — terminal działa lokalnie. |

---

## 9. Tryb Offline i kopie zapasowe

* **Pełna ochrona przed brakiem internetu:**  
  Awaria routera lub brak połączenia nie przerywa pracy terminala. Wszystkie odbicia zapisują się w pamięci wewnętrznej urządzenia. W momencie powrotu sieci Wi-Fi terminal **automatycznie przesyła wszystkie zaległe dane do Arkusza Google**.
* **Kopia zapasowa konfiguracji:**  
  W zakładce **⚙️ Ustawienia** ➔ **Kopia zapasowa** możesz jednym kliknięciem zapisać całą bazę ustawień i grup w chmurze Google lub pobrać plik `.json` na dysk komputera.

---

## 10. Pomoc techniczna

W przypadku pytań dotyczących obsługi, konfiguracji lub serwisu:
System wspiera automatyczne aktualizacje oprogramowania (OTA) przez panel `rcp.local`. Wszelkie pytania i zgłoszenia techniczne prosimy kierować do administratora systemu.
