# Øvelse 1 - Kom i gang

I denne delen skal du sette opp nødvendige utviklingsverktøy og utviklingsmiljø.

## 1.1 Oppsett av utviklingsverktøy

### 1.1.1 Node.js

:book: For å sjekke om du allerede har Node.js installert, åpne terminal'en på maskinen din:

- Dersom du bruker Mac / Linux, åpne "Terminal".
- Dersom du bruker Windows, åpne "Cmd", "Powershell" eller "Git Bash".

:book: Når du har åpnet terminalen, skriv inn `node -v`. Dersom du får opp versjonsnummer, har du Node installert. Får du beskjed om ukjent kommando, trenger du å installere Node.

:pencil2: Hvis det er en ukjent kommando, last ned og installer siste LTS (long-term support) versjon fra [nodejs.org](https://nodejs.org/en/).

:exclamation: **Merk:** Hvis du har Node installert med en versjon _lavere_ enn siste LTS-versjon, oppgrader til siste LTS-versjon før du fortsetter.

:bulb: Har du behov for flere Node-versjone på maskinen din, bruk Node Version Manager.

### 1.1.2 Visual Studio Code og YAML-utvidelse

:pencil2: Installer [Visual Studio Code](https://code.visualstudio.com/).

:pencil2: Installer [Red Hat YAML-utvidelsen](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) for Visual Studio Code.

## 1.2 Oppsett av GitHub-konto

:pencil2: Hvis du ikke allerede har en GitHub-konto, følg guiden [Registrer en ny GitHub-konto](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account) på GitHub.com. Det er gratis!

### 1.3 Installere git

:book: Git er et kommandolinjeverktøy for versjonskontroll. Det brukes til å håndtere og spore endringer i kode.

#### Sjekke om Git er installert

:bulb: Dersom du har Git installert, gå videre til neste del.

:pencil2: For å sjekke om du allerede har Git installert, åpne terminal-applikasjonen din.

- Hvis du bruker Mac, se etter et program som heter "Terminal".
- Hvis du bruker Windows, åpne "Ledetekst" eller "Git Bash".

Når du har åpnet terminalen, skriv inn `git version`. Utdataen vil enten vise hvilken versjon av Git som er installert, eller gi beskjed om at git er en ukjent kommando. Hvis det er en ukjent kommando, følg guiden [Installer Git](https://github.com/git-guides/install-git).

#### 1.2.2 Valgfritt - Installer GitHub Desktop

Hvis du er ny til git, anbefales [GitHub Desktop](https://desktop.github.com/) for å gjøre det enklere å jobbe med git. GitHub Desktop installerer også git automatisk.

## 1.2 Kom i gang

:bulb: Øvelsene forutsetter at du har noe erfaring med git. Hvis du er ny til git, vurder å lese følgende guider før du fortsetter:

- Git-oversikt: [Om Git](https://docs.github.com/en/get-started/using-git/about-git) på GitHub Docs
- [Push commits til et remote-repo](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository) på GitHub Docs
- [Hent endringer fra et remote-repo](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository) på GitHub Docs

### Forke git-repositoriet

:book: En fork er en kopi av et repository. Å forke et repository lar deg eksperimentere fritt med endringer uten å påvirke det opprinnelige prosjektet.

:pencil2: Åpne [roten av dette repoet](https://github.com/Aalesund-Techschool/continuous-deployment) og velg _Fork_:
![](./images/forking01.png)

:pencil2: Velg _din_ GitHub-bruker som _eier_ og trykk _Create fork_:
![](./images/forking02.png)

:book: Etter forking skal du nå ha en kopi av repositoryet på _din_ GitHub-konto.

### Klone git-repositoriet

:book: Repositorier på GitHub er eksterne repositories. For å lage en lokal kopi på din datamaskin, _kloner_ du det eksterne repositoryet du nettopp opprettet på kontoen din.

#### Klone med GitHub Desktop

:book: Hvis du har GitHub Desktop installert, kan du bruke det til å klone repositoryet.

:pencil2: Følg denne [instruksjonen](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository?tool=webui).

#### Klone med nettleser og terminal

:book: Hvis du ikke har GitHub Desktop installert, kan du klone repositoryet med nettleser og terminal.

:pencil2: Følg denne [instruksjonen](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository?tool=webui).

### Sette opp lokalt utviklingsmiljø

:book: For å gjøre det enklere har vi lagt ved en enkel eksempel-webapp.

:pencil2: Gå til `code`-mappen i repositoryet i terminalen og kjør følgende kommando for å installere alle prosjektavhengigheter:

```bash
npm install
```

:pencil2: Når alt er installert, åpne repository-mappen i Visual Studio Code.

:book: Her er strukturen til `code`-mappen:

```text
code
├── index.html
├── package-lock.json
├── package.json
├── src
├── node_modules
```

- `index.html` er hovedfilen til appen
- `package-lock.json` brukes av NPM for å holde styr på avhengigheter.
- `package.json` inneholder metadata om appen, noen _scripts_ for bygging og testing, og en oversikt over avhengigheter.
- `src` - inneholder JavaScript-koden til webappen
- `node_modules` - lokale kopi av eksterne pakker/ avhengigheter lastet ned etter at npm install kjøres

:pencil2: Kjør `npm run dev` i terminalen.

:book: Følgende utdata skal vises:

```bash
  VITE v3.2.11  ready in 92 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
```

:pencil2: Åpne [http://localhost:5173](http://localhost:5173) i Chrome.

### :book: 1.3 Appen

I dag handler det om å deploye appen, ikke hvordan den fungerer eller å lage flere funksjoner, men det er verdt en rask titt.

Som navnet tilsier, viser appen nåværende tid og antall sekunder igjen av året:

![](./images/app01.png)


### [Gå til oppgave 2 :arrow_right:](../oppgave-2/README.md)
