# 📸 Photo-PDF - Generator PDF ze zdjęć z opisami

Aplikacja webowa umożliwiająca łatwe tworzenie dokumentów PDF z kolekcji zdjęć wraz z ich opisami. Idealna do tworzenia raportów fotograficznych, dokumentacji wizualnej, albumów czy prezentacji.

## ✨ Funkcje

### 🖼️ Podstawowe funkcje
- **Drag & Drop** - przeciągnij zdjęcia bezpośrednio do aplikacji
- **Wybór plików** - standardowy selector plików dla wygody
- **Podgląd na żywo** - zobacz jak będzie wyglądał twój PDF
- **Opisy zdjęć** - dodaj tekstowe opisy do każdego zdjęcia
- **Eksport do PDF** - wygeneruj profesjonalny dokument PDF

### 🔒 Zabezpieczenia i walidacja
- **Walidacja formatów** - obsługa tylko bezpiecznych formatów obrazów (JPG, PNG, GIF, WebP)
- **Limit rozmiaru plików** - maksymalnie 10 MB na plik
- **Ograniczenie liczby plików** - maksymalnie 50 zdjęć na dokument
- **Sanitizacja nazw plików** - bezpieczne przetwarzanie nazw
- **Obsługa błędów** - szczegółowe komunikaty o problemach

### ⚡ Optymalizacja i wydajność
- **Kompresja obrazów** - automatyczne zmniejszanie rozmiaru dla lepszej wydajności
- **Responsive design** - działa na wszystkich urządzeniach
- **Zarządzanie pamięcią** - efektywne przetwarzanie dużych plików
- **Pasek postępu** - wizualna informacja o stanie przetwarzania
- **Ładowanie asynchroniczne** - nie blokuje interfejsu użytkownika

## 🚀 Jak używać

### 1. Dodawanie zdjęć
- **Metoda 1**: Przeciągnij pliki na strefę drop (oznaczoną ramką)
- **Metoda 2**: Kliknij w strefę drop i wybierz pliki z dysku

### 2. Dodawanie opisów
- Kliknij w pole tekstowe pod każdym zdjęciem
- Wpisz opis (maksymalnie 500 znaków)
- Licznik znaków pomoże kontrolować długość

### 3. Zarządzanie zdjęciami
- **Usuwanie**: Kliknij przycisk ❌ w prawym górnym rogu zdjęcia
- **Zmiana kolejności**: Zdjęcia w PDF będą w takiej kolejności jak na podglądzie
- **Czyszczenie wszystkich**: Użyj przycisku "Wyczyść wszystko"

### 4. Generowanie PDF
- Kliknij przycisk "Generuj PDF"
- Poczekaj na zakończenie procesu (widoczny będzie pasek ładowania)
- PDF zostanie automatycznie pobrany

## 🛠️ Specyfikacja techniczna

### Obsługiwane formaty obrazów
- **JPEG/JPG** - najpopularniejszy format zdjęć
- **PNG** - dla obrazów z przezroczystością
- **GIF** - dla prostych animacji
- **WebP** - nowoczesny format Google'a

### Ograniczenia
- **Rozmiar pliku**: maksymalnie 10 MB na obraz
- **Liczba plików**: maksymalnie 50 obrazów w jednym dokumencie
- **Długość opisu**: maksymalnie 500 znaków na opis
- **Rozdzielczość**: obrazy większe niż 1200x1200px są automatycznie skalowane

### Wymagania systemowe
- **Przeglądarka**: Chrome 60+, Firefox 55+, Safari 11+, Edge 79+
- **JavaScript**: musi być włączony
- **Pamięć**: minimum 2GB RAM (zalecane 4GB dla większych projektów)

## 📁 Struktura plików

```
Photo-PDF/
├── index.html          # Główna aplikacja
├── README.md          # Ta dokumentacja
└── .gitignore         # Ignorowane pliki (opcjonalnie)
```

## 🔧 Instalacja i uruchomienie

### Opcja 1: Bezpośrednie uruchomienie
1. Pobierz pliki z repozytorium
2. Otwórz plik `index.html` w przeglądarce
3. Aplikacja jest gotowa do użycia!

### Opcja 2: Serwer lokalny (zalecane dla developmentu)
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (wymagany zainstalowany http-server)
npx http-server

# Live Server w VS Code
# Zainstaluj rozszerzenie Live Server i kliknij "Go Live"
```

## 🎨 Dostosowywanie

### Zmiana limitów
W pliku `index.html` znajdź sekcję `CONFIG` i dostosuj wartości:

```javascript
const CONFIG = {
  MAX_FILE_SIZE: 10 * 1024 * 1024, // 10MB - rozmiar pliku
  MAX_FILES: 50,                   // Liczba plików
  MAX_IMAGE_WIDTH: 1200,           // Szerokość kompresji
  MAX_IMAGE_HEIGHT: 1200,          // Wysokość kompresji
  COMPRESSION_QUALITY: 0.8         // Jakość kompresji (0.1-1.0)
};
```

### Zmiana stylu
Style CSS znajdują się w sekcji `<style>` w pliku `index.html`. Możesz modyfikować:
- Kolory (zmienne CSS lub bezpośrednio w klasach)
- Rozmiary i odstępy
- Animacje i efekty
- Layout responsywny

## 🐛 Rozwiązywanie problemów

### Częste problemy

**Q: Aplikacja nie ładuje zdjęć**
- A: Sprawdź czy format pliku jest obsługiwany (JPG, PNG, GIF, WebP)
- A: Sprawdź czy plik nie przekracza 10 MB
- A: Sprawdź czy JavaScript jest włączony w przeglądarce

**Q: PDF nie generuje się**
- A: Sprawdź czy masz dodane przynajmniej jedno zdjęcie
- A: Sprawdź połączenie internetowe (potrzebne do załadowania bibliotek)
- A: Spróbuj odświeżyć stronę i spróbować ponownie

**Q: Zdjęcia są rozmazane w PDF**
- A: Zwiększ wartość `MAX_IMAGE_WIDTH` i `MAX_IMAGE_HEIGHT` w konfiguracji
- A: Zwiększ `COMPRESSION_QUALITY` (maksymalnie 1.0)

**Q: Aplikacja działa wolno**
- A: Zmniejsz liczbę zdjęć przetwarzanych jednocześnie
- A: Skompresuj zdjęcia przed dodaniem do aplikacji
- A: Sprawdź dostępną pamięć RAM

### Wsparcie techniczne
W przypadku problemów:
1. Sprawdź konsolę przeglądarki (F12 → Console)
2. Sprawdź czy używasz najnowszej wersji przeglądarki
3. Wyczyść cache przeglądarki
4. Spróbuj w trybie incognito/prywatnym

## 📝 Licencja

Ten projekt jest dostępny na licencji MIT. Możesz go używać, modyfikować i dystrybuować zgodnie z warunkami licencji.

## 🤝 Wkład w rozwój

Zachęcamy do zgłaszania:
- **Błędów** - opisz problem i kroki do reprodukcji
- **Ulepszeń** - propozycje nowych funkcji
- **Optymalizacji** - pomysły na poprawę wydajności

## 📊 Changelog

### v2.0 (Obecna wersja)
- ✅ Dodano zabezpieczenia i walidację plików
- ✅ Implementowano kompresję obrazów
- ✅ Dodano pasek postępu i komunikaty o błędach
- ✅ Ulepszono interfejs użytkownika
- ✅ Dodano obsługę usuwania zdjęć
- ✅ Implementowano responsive design
- ✅ Dodano licznik znaków w opisach
- ✅ Zoptymalizowano generowanie PDF

### v1.0 (Poprzednia wersja)
- Podstawowa funkcjonalność drag & drop
- Generowanie prostych PDF
- Podstawowy interfejs

## 🔗 Użyte technologie

- **HTML5** - struktura aplikacji
- **CSS3** - stylowanie i responsywność
- **Vanilla JavaScript** - logika aplikacji
- **jsPDF** - generowanie dokumentów PDF
- **HTML2Canvas** - konwersja HTML do obrazu (fallback)

---

**👨‍💻 Autor**: Piotr Wojtów  
**🔍 Rewident kodu**: Blazej Ejsmont ze wsparciem Claude AI  
**📅 Data utworzenia**: 2025  
**🔄 Ostatnia aktualizacja**: 2025  
**🌍 Wykonano**: w Polsce z ❤️

*Dziękujemy za korzystanie z Photo-PDF! 📸✨*