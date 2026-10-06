# Test praktyczny – React + TypeScript + Git + GitHub

## Cel testu

Celem testu jest sprawdzenie, czy potrafisz samodzielnie:

- utworzyć repozytorium GitHub,
- przygotować projekt React,
- wykorzystać Vite,
- pracować z TypeScript,
- skonfigurować linter,
- wykonywać commity i wysłać kod do repozytorium,
- pracować z danymi i renderować listę elementów w React.

---

# Zadanie podstawowe – obowiązkowe

## 1. Utwórz repozytorium GitHub

Na swoim koncie GitHub utwórz nowe:

**PUBLICZNE repozytorium**

Nazwa repozytorium może być dowolna, np.:

```text
react-test
```

lub

```text
animals-react-app
```

Repozytorium musi być publiczne, abym mógł sprawdzić jego zawartość.

---

## 2. Utwórz aplikację React

Przygotuj nowy projekt wykorzystujący:

- React
- TypeScript
- Vite

Nie korzystaj z Create React App.

Projekt musi dać się uruchomić lokalnie.

---

## 3. Skonfiguruj Oxlint

W projekcie nie chcemy korzystać z ESLint.

Zamiast niego skonfiguruj:

**Oxlint**

Oxlint powinien być zainstalowany jako dependency developerskie projektu.

W `package.json` powinien istnieć skrypt:

```text
lint
```

który uruchamia Oxlint.

Po wykonaniu:

```bash
npm run lint
```

Oxlint powinien sprawdzić kod projektu.

Jeżeli boilerplate Vite utworzył konfigurację ESLint, usuń ją oraz niepotrzebne zależności ESLint.

---

## 4. Uruchom aplikację

Sprawdź, czy:

```bash
npm run dev
```

poprawnie uruchamia aplikację.

Nie musisz tworzyć żadnego specjalnego interfejsu użytkownika w zadaniu podstawowym.

Domyślny widok React może zostać zmodyfikowany lub uproszczony.

---

## 5. Git

Projekt musi zostać zapisany w utworzonym wcześniej repozytorium GitHub.

W repozytorium powinny znajdować się wykonane przez Ciebie commity.

Nie wykonuj całego zadania jako jednego końcowego commita.

Przykładowy podział pracy:

```text
initial React setup
configure oxlint
cleanup project
```

Nazwy commitów mogą być inne.

---

# Zadanie rozszerzone

Po wykonaniu zadania podstawowego możesz wykonać zadanie dodatkowe.

## 1. Przygotuj dane

Przygotuj dane dotyczące **5 różnych zwierząt**.

Dla każdego zwierzęcia potrzebujemy:

```text
nazwa
kontynent występowania
średnia prędkość
średnia waga
```

Przykładowe dane:

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

## 2. Zapisz dane jako JSON

Nie wpisuj pięciu zwierząt bezpośrednio jako pięciu osobnych elementów JSX.

Przygotuj plik z danymi, np.:

```text
src/
  data/
    animals.json
```

Plik powinien zawierać tablicę obiektów.

Przykładowa struktura pojedynczego elementu:

```json
{
  "name": "Cheetah",
  "continent": "Africa",
  "averageSpeed": 100,
  "weight": 50
}
```

W pliku powinno znajdować się **5 zwierząt**.

---

## 3. Utwórz typ

Przygotuj własny typ TypeScript opisujący zwierzę.

Może znajdować się np. w:

```text
src/
  types/
    Animal.ts
```

Typ powinien opisywać wszystkie wymagane właściwości:

```text
name
continent
averageSpeed
weight
```

Dobierz poprawne typy danych.

---

## 4. Wyświetl listę zwierząt

Zaimportuj dane do aplikacji React.

Następnie wyrenderuj wszystkie zwierzęta **automatycznie na podstawie tablicy danych**.

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
<div>Horse</div>
<div>Wolf</div>
```

### Oczekiwane podejście

Aplikacja powinna posiadać tablicę danych, po której iterujesz i na jej podstawie tworzysz elementy interfejsu.

Każde zwierzę powinno wyświetlać:

- nazwę,
- kontynent występowania,
- średnią prędkość w `km/h`,
- średnią wagę w `kg`.

Sposób prezentacji danych jest dowolny.

Może to być np.:

- lista,
- tabela,
- karty.

Wygląd aplikacji nie jest najważniejszą częścią zadania.

---

# Przykładowa struktura projektu

Nie musisz odwzorowywać jej dokładnie, ale projekt może wyglądać np. tak:

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

Możesz również stworzyć dodatkowe komponenty.

---

# Przed oddaniem sprawdź

Projekt powinien spełniać następujące wymagania:

- repozytorium GitHub jest publiczne,
- projekt wykorzystuje React,
- projekt wykorzystuje TypeScript,
- projekt został utworzony z wykorzystaniem Vite,
- projekt uruchamia się przez `npm run dev`,
- projekt wykorzystuje Oxlint zamiast ESLint,
- `npm run lint` działa poprawnie,
- kod znajduje się na GitHubie,
- repozytorium posiada historię commitów.

Dla zadania rozszerzonego dodatkowo:

- istnieje lista 5 zwierząt,
- dane znajdują się w osobnym pliku JSON,
- został utworzony typ TypeScript,
- dane są renderowane automatycznie,
- wykorzystano `.map()`,
- każde zwierzę posiada nazwę, kontynent, prędkość i wagę.

---

# Oddanie testu

Po zakończeniu pracy wyślij wiadomość e-mail na adres:

**bartosz.ciach@technischools.com**

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

Przed wysłaniem wiadomości upewnij się, że repozytorium jest ustawione jako **PUBLICZNE**.

---

# Ważne

Nie liczy się wyłącznie efekt końcowy.

Zwróć uwagę również na:

- strukturę projektu,
- czytelność kodu,
- wykorzystanie TypeScript,
- sposób pracy z Gitem,
- historię commitów,
- poprawne użycie narzędzi,
- unikanie powtarzania kodu.

Powodzenia!
