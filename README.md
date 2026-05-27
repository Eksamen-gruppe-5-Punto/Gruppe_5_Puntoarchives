# Teknisk dokumentation – PUNTO ARCHIVES

## Om projektet

Vi har lavet et dynamisk website med Astro, hvor indholdet bliver hentet direkte fra vores egen database i **Supabase**

Sitet består af flere sider, hvor brugeren kan:

- Shoppe blazere eller suits
- Læse om firmet og se inspiration via lookbook
- Holde sig opdateret på events

## Links

- GitHub repository: [indsæt link]
- GitHub Pages: [indsæt link]
- Figma: [indsæt link]
- Trello: [indsæt link]

---

## Projektstruktur

```
project/
├── public/
│   └── styles/
│       └── global.css
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── Button.astro
│   │   ├── Cardrack.astro
│   │   ├── Cartbox.astro
│   │   ├── Features.astro
│   │   ├── Filterbox.astro
│   │   ├── Footer.astro
│   │   ├── Navigation.astro
│   │   ├── Pcard.astro
│   │   └── Psite.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   ├── product/
│   │   │   └── [id].astro
│   │   ├── Aboutlookbook.astro
│   │   ├── Event.astro
│   │   ├── index.astro
│   │   ├── Profile.astro
│   │   └── Shop.astro
│   └── styles/
│       └── global.css
├── .gitignore
├── astro.config.mjs
├── package-lock.json
└── package.json
```

### Filbeskrivelser

#### Sider (`src/pages/`)

- **index.astro** – Hjemmesidens forside, der fungerer som brugernes primære visuelle navigationsvej via billeder og links.
- **Shop.astro** – Oversigtssiden, der henter alle tilgængelige produkter dynamisk fra Supabase-databasen.
- **Product.astro** – Detaljesiden for det enkelte produkt, som viser uddybende informationer, beskrivelse og priser.
- **Aboutlookbook.astro** – Inspirationssiden (Lookbook), hvor brandets identitet og visuelle materiale præsenteres.
- **Event.astro** – Her kan man se kommende brand-events.
- **Profile.astro** - her kan brugeren kunne logge sig ind for at se sine fx gemte ting eller tideligere køb (virker ikke)

## Data og JSON-struktur

Vi henter vores produktdata direkte fra Supabase i JSON-format. Et objekt fra vores database ser således ud:

```json
{
  "id": 1,
  "name": "Beige Corduroy Italian Sport Blazer",
  "brand": "GIORGIO ARMANI",
  "price": 749,
  "description": "Relaxed soft-shoulder fit in warm textured corduroy wool blend.",
  "size": ["52 (L)"],
  "modelSize": "186",
  "image": "https://mpbvcoonbwvxvdnpsfil.supabase.co/storage/v1/object/sign/Punto-Billeder/fyr_i_brun_blazer.jpg?token=eyJraWQiOiJzdG9yYWdlLXVybC1zaWduaW5nLWtleV8zYjUzOWM2Yy01YTFkLTQxNmYtYmRiZC1lNzc3NWJkZjA0NTQiLCJhbGciOiJIUzI1NiJ9.eyJ1cmwiOiJQdW50by1CaWxsZWRlci9meXJfaV9icnVuX2JsYXplci5qcGciLCJpYXQiOjE3NzkzNTk5NTIsImV4cCI6MTgxMDg5NTk1Mn0.A4xgMKxGkhxpbpmfdx2EGXlKRN3SgUSrRQSC84nMpJg",
  "details_img_1": "detail1.jpg",
  "details_img_2": "detail2.jpg",
  "details_img_3": "detail3.jpg"
}
(Resten af billederne er også lange links, har derfor ikke gentaget det)
```

## Felter vi bruger

- **id**
- **price**
- **name**
- **brand**
- **image**
- **description**
- **size**
- **modelSize**
- **details_img_1**
- **details_img_2**
- **details_img_3**

### Eksempler på variabler

### Eksempler på funktioner

### Workflow

I vores gruppe har vi arbejdet ud fra et fastlagt Git-workflow for at undgå konflikter i kildekoden. Vi har konsekvent benyttet branches. Når en funktion har været færdig og testet lokalt, har vi committet og pushed ændringerne til GitHub. For at undgå merge-conflicts har vi siddet sammen, når vi har merget branchen ind i vores primære `main`-branch.

---

### Eksempler på branches

- `look-book`
- `menuchanges`
- `productsite`
- `stylecss`

## Bæredygtighed

Valget af Astro som framework er et bæredygtige tiltag.
Astro adskiller sig fra andre frameworks ved at levere fuldstændig ren HTML til browseren som standard og fjerne alt overflødigt JavaScript (Zero JavaScript by default).

---

## Gruppemedlemmer

- Anton Jepsen
- Ditte Helene Andersen
- Eva Roed Schack
- Isabel Maibom
