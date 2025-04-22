Poniżej znajdziesz przykładowy **README.md** (lub inny plik instrukcji), który możesz umieścić w swoim repozytorium na GitHub. Jest on wzorowany na stylu Twoich poprzednich warsztatów i zawiera szczegółowy opis kroków potrzebnych do stworzenia własnego CV jako statycznej aplikacji na **Azure Static Web Apps**, z wykorzystaniem **Visual Studio Code** oraz **GitHub Copilot**.

---

# Warsztaty: Jak stworzyć własne CV i wdrożyć je na Azure Static Web Apps

## Spis treści

1. [Opis warsztatów](#opis-warsztatów)  
2. [Wymagania wstępne](#wymagania-wstępne)  
3. [Przygotowanie środowiska](#przygotowanie-środowiska)  
   - [Visual Studio Code](#visual-studio-code)  
   - [GitHub Copilot](#github-copilot)  
   - [Konto GitHub](#konto-github)  
   - [Konto Azure / Azure for Students](#konto-azure--azure-for-students)  
4. [Struktura repozytorium](#struktura-repozytorium)  
5. [Krok po kroku: Tworzenie projektu CV](#krok-po-kroku-tworzenie-projektu-cv)  
   1. [Utworzenie nowego repozytorium na GitHub](#1-utworzenie-nowego-repozytorium-na-github)  
   2. [Klonowanie repozytorium i otwarcie go w VS Code](#2-klonowanie-repozytorium-i-otwarcie-go-w-vs-code)  
   3. [Inicjalizacja projektu i pierwsze linie kodu za pomocą GitHub Copilot](#3-inicjalizacja-projektu-i-pierwsze-linie-kodu-za-pomocą-github-copilot)  
   4. [Tworzenie prostej strony CV](#4-tworzenie-prostej-strony-cv)  
   5. [Testowanie lokalne aplikacji](#5-testowanie-lokalne-aplikacji)  
   6. [Wdrażanie na Azure Static Web Apps](#6-wdrażanie-na-azure-static-web-apps)  
6. [Rozwiązywanie problemów](#rozwiązywanie-problemów)  
7. [Materiały dodatkowe](#materiały-dodatkowe)  
8. [Autor](#autor)  

---

## Opis warsztatów

W trakcie tych warsztatów pokażemy, jak w ciągu **2 godzin** stworzyć proste, **statyczne CV** przy pomocy **Visual Studio Code** i **GitHub Copilot**, a następnie wdrożyć je za darmo na **Azure Static Web Apps**. Po ukończeniu warsztatów będziesz miał(a) w pełni funkcjonalną stronę-wizytówkę, którą możesz udostępnić w sieci jako swój **życiorys w nowoczesnej formie**.

---

## Wymagania wstępne

Przed rozpoczęciem warsztatów, upewnij się, że posiadasz:

- **Komputer** z systemem Windows / Linux / macOS z dostępem do Internetu.  
- **Podstawową znajomość** HTML, CSS i (opcjonalnie) JavaScript.  
- **Konto GitHub** – zarejestruj się, jeśli jeszcze go nie masz: [https://github.com/](https://github.com/).  
- **Konto w Azure** (istnieje możliwość skorzystania z darmowej wersji [Azure for Students](https://azure.microsoft.com/pl-pl/free/students/), jeśli jesteś studentem).  

---

## Przygotowanie środowiska

### Visual Studio Code

Pobierz i zainstaluj **Visual Studio Code**:  
[https://code.visualstudio.com/](https://code.visualstudio.com/)

### GitHub Copilot

1. Upewnij się, że posiadasz subskrypcję GitHub Copilot (darmowy okres próbny lub plan edukacyjny).  
2. W **Visual Studio Code** zainstaluj rozszerzenie [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot).  
3. Zaloguj się w rozszerzeniu przy użyciu swoich danych z GitHub.

### Konto GitHub

Jeśli nie masz konta GitHub, załóż je tutaj:  
[https://github.com/](https://github.com/)

### Konto Azure / Azure for Students

Zarejestruj się na [Azure Portal](https://portal.azure.com/) lub utwórz konto w programie **Azure for Students**, jeśli jesteś studentem i chcesz skorzystać z darmowych środków.

---

## Struktura repozytorium

Poniżej przykładowa struktura plików, którą możesz stworzyć w trakcie warsztatów:

```
my-cv-azure
│   README.md
│   index.html
│   style.css
│   .github/workflows/azure-static-web-apps.yml
└── assets
    └── images
        └── (tu będą pliki graficzne, np. zdjęcie profilowe)
```

> **Uwaga**: Nazwy plików i folderów można dowolnie modyfikować. Ważne, by zachować plik konfiguracyjny dla GitHub Actions w `.github/workflows` (o czym dokładniej w dalszej części).

---

## Krok po kroku: Tworzenie projektu CV

### 1. Utworzenie nowego repozytorium na GitHub

1. Wejdź na swój profil GitHub i kliknij przycisk **New** (utwórz nowe repozytorium).  
2. Nadaj repozytorium nazwę, np. **my-cv-azure**.  
3. Zaznacz opcję **Public** (repozytorium publiczne).  
4. Zaznacz opcję **Add a README file** (opcjonalnie).  
5. Kliknij **Create repository**.  

### 2. Klonowanie repozytorium i otwarcie go w VS Code

1. W nowo utworzonym repozytorium skopiuj link do klonowania (np. **HTTPS**).  
2. Otwórz **Visual Studio Code** i z poziomu **Command Palette** (Ctrl+Shift+P lub Cmd+Shift+P) wybierz **Git: Clone**.  
3. Wklej skopiowany link i wskaż folder, w którym chcesz przechowywać lokalną kopię projektu.  
4. Otwórz sklonowane repozytorium w VS Code.

### 3. Inicjalizacja projektu i pierwsze linie kodu za pomocą GitHub Copilot

1. Upewnij się, że masz włączone rozszerzenie **GitHub Copilot** w VS Code.  
2. Utwórz plik **index.html** i zacznij pisać podstawowy szablon HTML (lub zacznij od komentarza, który opisuje co chcesz osiągnąć – Copilot zasugeruje kod).  
3. Możesz wykorzystać podpowiedzi Copilot (skrót klawiszowy: `Alt + \` na Windows / Linux lub `Option + \` na macOS) do generowania i uzupełniania kodu.  
4. Dodaj plik **style.css** i połącz go w sekcji `<head>` pliku HTML.  

### 4. Tworzenie prostej strony CV

1. W **index.html** umieść sekcje takie jak **O mnie**, **Umiejętności**, **Doświadczenie**, **Edukacja** i **Kontakt**.  
2. Posłuż się Copilotem, aby automatycznie generować przykładowe bloki kodu HTML/CSS.  
3. (Opcjonalnie) Dodaj interaktywność w JavaScripcie – Copilot może zaproponować funkcje, które wzbogacą Twoje CV (np. animacje, przejścia).  

Przykład minimalnego kodu w `index.html`:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <title>Moje CV</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>Jan Kowalski</h1>
    <p>Programista Front-end / Student Informatyki</p>
  </header>

  <section id="o-mnie">
    <h2>O mnie</h2>
    <p>Jestem studentem Informatyki na AGH, pasjonuję się tworzeniem aplikacji webowych...</p>
  </section>

  <section id="umiejetnosci">
    <h2>Umiejętności</h2>
    <ul>
      <li>HTML, CSS, JavaScript</li>
      <li>React, Angular</li>
      <li>Azure, Docker, Kubernetes</li>
    </ul>
  </section>

  <!-- Dodaj kolejne sekcje... -->

  <footer>
    <p>Kontakt: jan.kowalski@example.com</p>
  </footer>
</body>
</html>
```

### 5. Testowanie lokalne aplikacji

Aby wyświetlić utworzone CV, wystarczy otworzyć plik **index.html** w przeglądarce (dwuklik).  


### 6. Wdrażanie na Azure Static Web Apps

1. Wejdź na [Azure Portal](https://portal.azure.com/) i utwórz nowy zasób **Static Web App**.  
2. Wskaż repozytorium z GitHub, które będzie źródłem plików dla Twojej strony CV.  
3. Wybierz odpowiedni **branch** (np. `main`) oraz ścieżkę do folderu z plikami strony (np. `"/"` jeśli plik `index.html` znajduje się w głównym katalogu).  
4. Azure utworzy automatycznie plik workflow w katalogu `.github/workflows` (np. `azure-static-web-apps-<coś>.yml`), który będzie konfigurował wdrożenie.  
5. Po chwili Twoje CV zostanie zbudowane i wdrożone na wygenerowany adres URL (np. `https://<twoja-app>.azurestaticapps.net`).  

> **Uwaga**: Możesz też ręcznie dodać plik `.github/workflows/azure-static-web-apps.yml`, jeśli preferujesz własną konfigurację.

Przykład minimalnej konfiguracji workflow (dodawanej automatycznie przez Azure):

```yaml
name: Azure Static Web Apps CI/CD

on:
  push:
    branches:
      - main
  pull_request:
    types: [opened, synchronize, reopened, closed]
    branches:
      - main

jobs:
  build_and_deploy_job:
    if: ${{ github.event_name != 'pull_request' || github.event.pull_request.merged == true }}
    runs-on: ubuntu-latest
    name: Build and Deploy
    steps:
      - uses: actions/checkout@v2

      - name: Build And Deploy
        uses: azure/static-web-apps-deploy@v1
        with:
          azure_static_web_apps_api_token: ${{ secrets.AZURE_STATIC_WEB_APPS_API_TOKEN_<UNIKALNE_ID> }}
          repo_token: ${{ secrets.GITHUB_TOKEN }}
          action: "upload"
          folder: "/"
          api_location: "api"
          app_artifact_location: "build"
```

---

## Rozwiązywanie problemów

- **Nie widzę podpowiedzi Copilota w VS Code.**  
  Upewnij się, że rozszerzenie GitHub Copilot jest zainstalowane i aktywne oraz że jesteś zalogowany na GitHub w Visual Studio Code.

- **Azure Static Web Apps rzuca błąd przy wdrażaniu.**  
  Sprawdź, czy wybrana ścieżka w pliku workflow (`folder: "/"`) jest poprawna i zawiera plik `index.html`.  
  Upewnij się, że plik `index.html` znajduje się w głównym katalogu albo wskaż właściwą ścieżkę.

- **Otrzymuję błąd autoryzacji przy deploymencie.**  
  Upewnij się, że w sekcji [**Secrets** w repozytorium GitHub**](https://docs.github.com/en/actions/security-guides/encrypted-secrets) masz ustawiony poprawny `AZURE_STATIC_WEB_APPS_API_TOKEN`.

---

## Materiały dodatkowe

- **Dokumentacja GitHub Copilot**:  
  [https://docs.github.com/en/copilot](https://docs.github.com/en/copilot)
- **Dokumentacja Azure Static Web Apps**:  
  [https://docs.microsoft.com/azure/static-web-apps](https://docs.microsoft.com/azure/static-web-apps)
- **Visual Studio Code** (poradniki i rozszerzenia):  
  [https://code.visualstudio.com/docs](https://code.visualstudio.com/docs)
- **Git i GitHub** (podstawy):  
  [https://docs.github.com/en/get-started](https://docs.github.com/en/get-started)

---

## Autor

Warsztaty prowadzone przez **[Marcin Gastol](https://github.com/marcingastol)**.  
W razie pytań lub problemów zapraszam do kontaktu / otwarcia **Issue** w tym repozytorium.
