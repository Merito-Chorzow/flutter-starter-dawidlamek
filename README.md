# Geo Journal (Flutter)

Geo Journal to prosta aplikacja mobilna/webowa stworzona w Flutterze (Dart),
umożliwiająca dodawanie wpisów z opisem oraz zapisem aktualnej lokalizacji GPS.

Projekt został wykonany w ramach zadania zaliczeniowego z Fluttera.

---

## Zakres funkcjonalny

### Natywna funkcja
Aplikacja korzysta z **lokalizacji GPS urządzenia** (`geolocator`):
- użytkownik może pobrać aktualną lokalizację,
- współrzędne zapisywane są razem z wpisem,
- obsłużone są sytuacje braku zgody na lokalizację.

### API
Aplikacja komunikuje się z zewnętrznym API (MockAPI):
- `GET /entries` – pobieranie listy wpisów,
- `POST /entries` – dodawanie nowego wpisu.

---

## Widoki aplikacji

1. **Lista wpisów**
   - lista zapisanych wpisów,
   - informacja o dacie i lokalizacji,
   - obsługa stanu pustego, ładowania i błędów.

2. **Szczegóły wpisu**
   - tytuł,
   - opis,
   - data utworzenia,
   - lokalizacja (jeśli została zapisana).

3. **Dodaj wpis**
   - formularz (tytuł, opis),
   - przycisk „Pobierz lokalizację” (GPS),
   - zapis danych do API.

4. **Ustawienia**
   - przełącznik jasny / ciemny motyw aplikacji.

---

## Nawigacja

- przejście lista → szczegóły (z przekazaniem danych wpisu),
- przejście lista → dodaj wpis,
- przejście lista → ustawienia.

---

## Obsługa stanów UX

- **Ładowanie** – wskaźnik CircularProgressIndicator,
- **Pusty stan** – komunikat przy braku wpisów,
- **Błąd API / brak internetu** – komunikat z możliwością ponowienia,
- **Brak uprawnień lokalizacji** – komunikat informujący użytkownika.

---

## Użyte technologie

- Flutter (Dart)
- HTTP (`http`)
- Lokalizacja GPS (`geolocator`)
- MockAPI (REST API)

---

## Uruchomienie projektu

### Wymagania
- Flutter SDK
- Android Emulator lub przeglądarka (Chrome)
- VS Code lub Android Studio

### Kroki

```bash
flutter pub get
flutter run
