# Test praktyczny – React + TypeScript + Vite + Oxlint + GitHub

## Cel testu

Celem testu jest sprawdzenie, czy potrafisz samodzielnie:

- utworzyć publiczne repozytorium na GitHubie,
- przygotować projekt React z wykorzystaniem Vite,
- pracować z TypeScript,
- wybrać template wykorzystujący Oxlint zamiast ESLint,
- pracować z Git i branchami,
- wykonać Pull Request,
- zmergować zmiany do głównej gałęzi repozytorium,
- wysłać gotowy projekt na GitHub.

---

# Zadanie podstawowe – obowiązkowe

## 1. Utwórz repozytorium GitHub

Na swoim koncie GitHub utwórz nowe repozytorium.

Repozytorium musi być:

- publiczne,
- utworzone na Twoim koncie GitHub,
- przeznaczone wyłącznie na ten test.

Nazwa repozytorium może być dowolna, np.:

```text
react-test
```

lub:

```text
animals-react-app
```

### Ważne

Nie forkować repozytorium z instrukcją.

Każdy uczeń tworzy własne repozytorium od zera.

---

## 2. Utwórz aplikację React

Przygotuj nowy projekt wykorzystujący:

- React,
- TypeScript,
- Vite,
- Oxlint.

Podczas tworzenia projektu wybierz odpowiedni template React + TypeScript wykorzystujący **Oxlint zamiast ESLint**.

Nie korzystaj z Create React App.

Celem zadania jest samodzielne utworzenie właściwego projektu.

---

## 3. Sprawdź Oxlint

Po utworzeniu projektu sprawdź, czy dostępny jest skrypt:

```bash
npm run lint
```

Powinien on uruchamiać Oxlint.

W projekcie nie powinien być używany ESLint.

---

## 4. Uruchom aplikację

Sprawdź, czy aplikacja uruchamia się poprawnie przez:

```bash
npm run dev
```

Po uruchomieniu aplikacja powinna działać w przeglądarce.

W zadaniu podstawowym nie musisz tworzyć rozbudowanego interfejsu.

Możesz zostawić prosty widok aplikacji lub lekko go uprościć.

---

## 5. Praca z branchem

Nie wykonuj całej pracy bezpośrednio na głównej gałęzi repozytorium.

Po utworzeniu projektu:

1. upewnij się, że główna gałąź repozytorium to `main` lub `master`,
2. utwórz nowy branch przeznaczony do pracy nad zadaniem,
3. przełącz się na nowo utworzony branch,
4. wykonuj zmiany i commity właśnie na nim,
5. wyślij branch na GitHub.

Nazwa brancha może być dowolna, ale powinna jasno opisywać wykonywane zadanie, np.:

```text
feature/react-setup
```

lub:

```text
feature/animals-list
```

---

## 6. Commity

W trakcie pracy wykonuj commity.

Nie wykonuj całego zadania jako jednego końcowego commita.

Przykładowy podział pracy:

```text
initial project setup
configure project
cleanup application
```

Nazwy commitów mogą być inne.

Ważne, aby historia repozytorium pokazywała przebieg Twojej pracy.

---

## 7. Utwórz Pull Request

Po zakończeniu pracy na swoim branchu:

1. wejdź do swojego repozytorium na GitHubie,
2. utwórz Pull Request z własnego brancha do głównej gałęzi `main` lub `master`,
3. sprawdź zmiany widoczne w Pull Requeście,
4. zmerguj Pull Request do głównej gałęzi.

Po zakończeniu testu kod rozwiązania powinien znajdować się na głównej gałęzi repozytorium.

### Ważne

Częścią zadania jest pokazanie, że potrafisz wykonać podstawowy workflow:

```text
main/master
    ↓
nowy branch
    ↓
commity
    ↓
push
    ↓
Pull Request
    ↓
merge do main/master
```

---

# Zadanie rozszerzone – dodatkowe

Po wykonaniu zadania podstawowego możesz wykonać część rozszerzoną.

## 1. Przygotuj dane o zwierzętach

Przygotuj dane dotyczące **5 różnych zwierząt**.

Dla każdego zwierzęcia potrzebujemy:

- nazwy,
- kontynentu występowania,
- średniej prędkości,
- średniej wagi.

Przykład:

```text
Cheetah
Africa
100 km/h
50 kg
```

Nie musisz korzystać z tego przykładu.

Dane możesz:

- znaleźć samodzielnie w Internecie,
- przygotować samodzielnie,
- poprosić ChatGPT o przygotowanie przykładowych danych.

---

## 2. Zapisz dane w pliku JSON

Dane powinny znajdować się w osobnym pliku.

Przykładowa struktura:

```text
src/
  data/
    animals.json
```

Plik powinien zawierać tablicę obiektów.

Przykład pojedynczego obiektu:

```json
{
  "name": "Cheetah",
  "continent": "Africa",
  "averageSpeed": 100,
  "weight": 50
}
```

W pliku powinno znajdować się 5 zwierząt.

---

## 3. Utwórz typ TypeScript

Przygotuj własny typ TypeScript opisujący pojedyncze zwierzę.

Może znajdować się np. w:

```text
src/
  types/
    Animal.ts
```

Typ powinien opisywać następujące właściwości:

```text
name
continent
averageSpeed
weight
```

Dobierz odpowiednie typy danych.

---

## 4. Wyświetl listę zwierząt

Zaimportuj dane z pliku JSON do aplikacji React.

Następnie wyrenderuj wszystkie zwierzęta automatycznie na podstawie tablicy danych.

Do renderowania wykorzystaj:

```javascript
.map()
```

Nie twórz ręcznie pięciu osobnych elementów.

### Niepoprawne podejście

```jsx
<div>Lion</div>
<div>Cheetah</div>
<div>Elephant</div>
<div>Wolf</div>
<div>Horse</div>
```

### Oczekiwane podejście

Aplikacja powinna:

1. pobrać dane z przygotowanej tablicy,
2. przejść po niej przy pomocy `.map()`,
3. wyrenderować element dla każdego zwierzęcia.

Każde zwierzę powinno wyświetlać:

- nazwę,
- kontynent występowania,
- średnią prędkość w `km/h`,
- średnią wagę w `kg`.

Sposób prezentacji danych jest dowolny.

Może to być:

- lista,
- tabela,
- karty.

Wygląd aplikacji nie jest najważniejszą częścią zadania.

---

# Przykładowa struktura projektu

Projekt może wyglądać np. tak:

```text
src/
├── data/
│   └── animals.json
│
├── types/
│   └── Animal.ts
│
├── App.tsx
├── main.tsx
└── index.css
```

Nie musisz odwzorowywać tej struktury dokładnie.

Możesz również stworzyć dodatkowe komponenty.

---

# Przed oddaniem sprawdź

## Zadanie podstawowe

Upewnij się, że:

- repozytorium GitHub jest publiczne,
- repozytorium znajduje się na Twoim koncie,
- projekt wykorzystuje React,
- projekt wykorzystuje TypeScript,
- projekt został utworzony przy pomocy Vite,
- projekt wykorzystuje Oxlint,
- projekt nie wykorzystuje ESLint,
- `npm run dev` działa poprawnie,
- `npm run lint` działa poprawnie,
- pracowałeś na osobnym branchu,
- wykonałeś kilka sensownych commitów,
- branch został wysłany na GitHub,
- utworzyłeś Pull Request,
- Pull Request został zmergowany do `main` lub `master`,
- końcowy kod znajduje się na głównej gałęzi repozytorium.

## Zadanie rozszerzone

Dodatkowo sprawdź, czy:

- istnieje lista 5 zwierząt,
- dane znajdują się w osobnym pliku JSON lub tsx / jsx,
- utworzony został typ TypeScript,
- dane są renderowane automatycznie,
- wykorzystano `.map()`,
- każde zwierzę posiada nazwę,
- każde zwierzę posiada kontynent występowania,
- każde zwierzę posiada średnią prędkość,
- każde zwierzę posiada średnią wagę.

---

# Oddanie testu

Po zakończeniu pracy wyślij wiadomość e-mail na adres:

**[bartosz.ciach@technischools.com](mailto\:bartosz.ciach@technischools.com)**

W wiadomości podaj:

```text
Imię i nazwisko:
Nazwa konta GitHub:
Link do repozytorium:
```

Przykład:

```text
Jan Kowalski
GitHub: jkowalski123
Repozytorium: https://github.com/jkowalski123/react-test
```

Przed wysłaniem wiadomości upewnij się, że repozytorium jest ustawione jako **PUBLIC**.

---

# Na co zwracana będzie uwaga

Podczas sprawdzania testu liczy się nie tylko efekt końcowy.

Zwracana będzie również uwaga na:

- poprawną konfigurację projektu,
- strukturę plików,
- wykorzystanie TypeScript,
- poprawne użycie Oxlint,
- sposób pracy z Gitem,
- pracę na osobnym branchu,
- historię commitów,
- poprawne utworzenie Pull Requesta,
- poprawne wykonanie merge do głównej gałęzi,
- czytelność kodu,
- unikanie powtarzania kodu,
- poprawne renderowanie danych.

Powodzenia!
