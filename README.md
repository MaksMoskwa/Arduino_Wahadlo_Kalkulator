# 🧮 Kalkulator Arduino – LCD 16x2 + Klawiatura 4x4

## 📌 Opis projektu

Projekt przedstawia prosty kalkulator zbudowany na platformie **Arduino**, wykorzystujący klawiaturę matrycową 4x4 oraz wyświetlacz LCD 16x2.

Urządzenie umożliwia wykonywanie podstawowych działań matematycznych: dodawania, odejmowania, mnożenia i dzielenia. Użytkownik wprowadza liczby za pomocą klawiatury, a wynik obliczeń wyświetlany jest na ekranie LCD.

Projekt został napisany w języku **C++ z wykorzystaniem środowiska Arduino IDE**.

## ⚙️ Wykorzystane komponenty

- Arduino (np. Arduino Uno)
- Klawiatura matrycowa 4x4
- Wyświetlacz LCD 16x2 z obsługą przez bibliotekę Adafruit
- Przewody połączeniowe
- Płytka stykowa (opcjonalnie)

## 📚 Wykorzystane biblioteki

Projekt korzysta z dwóch bibliotek:

- `Adafruit_LiquidCrystal.h` – odpowiada za komunikację i obsługę wyświetlacza LCD.
- `Keypad.h` – umożliwia odczytywanie przycisków z klawiatury matrycowej 4x4.

## 🎮 Obsługa kalkulatora

Klawiatura została skonfigurowana w następujący sposób:

| Przycisk | Funkcja |
|---|---|
| 0–9 | Wprowadzanie cyfr |
| + | Dodawanie |
| - | Odejmowanie |
| * | Mnożenie |
| / | Dzielenie |
| # | Zatwierdzenie działania i wyświetlenie wyniku |
| C | Wyczyszczenie kalkulatora |

### Przykład użycia

Aby wykonać działanie `12 + 8`:

1. Wciśnij `1`.
2. Wciśnij `2`.
3. Wciśnij `+`.
4. Wciśnij `8`.
5. Wciśnij `#`.
6. Na wyświetlaczu pojawi się wynik `20`.

## 🔌 Konfiguracja pinów Arduino

### Klawiatura 4x4

| Pin Arduino | Funkcja |
|---|---|
| D13 | Wiersz 1 |
| D12 | Wiersz 2 |
| D11 | Wiersz 3 |
| D10 | Wiersz 4 |
| D6 | Kolumna 1 |
| D7 | Kolumna 2 |
| D8 | Kolumna 3 |
| D9 | Kolumna 4 |

### Wyświetlacz LCD

Wyświetlacz jest obsługiwany przez bibliotekę `Adafruit_LiquidCrystal` i skonfigurowany w kodzie jako:

`Adafruit_LiquidCrystal lcd_1(0);`

Adres lub numer połączenia zależy od zastosowanego modułu i jego konfiguracji.

## 🧠 Funkcjonalności programu

- Odczytywanie cyfr z klawiatury 4x4.
- Obsługa czterech podstawowych działań matematycznych.
- Wyświetlanie wprowadzanych liczb na ekranie LCD.
- Automatyczne czyszczenie ekranu przy rozpoczęciu kolejnego obliczenia.
- Zatwierdzanie działania przyciskiem `#`.
- Resetowanie kalkulatora przyciskiem `C`.
- Zabezpieczenie przed dzieleniem przez zero.
- Ograniczenie długości wprowadzanej liczby do 16 znaków.

## 🚀 Uruchomienie projektu

1. Podłącz Arduino do komputera.
2. Otwórz projekt w Arduino IDE.
3. Zainstaluj wymagane biblioteki:
   - Adafruit LiquidCrystal
   - Keypad
4. Podłącz klawiaturę 4x4 oraz wyświetlacz LCD zgodnie z konfiguracją pinów.
5. Wybierz odpowiednią płytkę Arduino i port COM.
6. Wgraj program na mikrokontroler.
7. Po uruchomieniu urządzenie będzie gotowe do wykonywania obliczeń.

## ⚠️ Ograniczenia

- Program obsługuje liczby całkowite.
- Nie obsługuje liczb zmiennoprzecinkowych.
- Jedno działanie może zawierać tylko dwie liczby i jeden operator.
- Wyniki dzielenia są obliczane jako liczby całkowite.
- Maksymalna długość wprowadzanej liczby wynosi 16 znaków.

## 👨‍💻 Technologie

- **Język:** C++
- **Platforma:** Arduino
- **Środowisko:** Arduino IDE
- **Wyświetlacz:** LCD 16x2
- **Interfejs wejściowy:** Klawiatura matrycowa 4x4

## 📄 Licencja

Projekt edukacyjny stworzony w celu nauki programowania mikrokontrolerów Arduino, obsługi urządzeń peryferyjnych oraz wykorzystania języka C++ w praktyce.
