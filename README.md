# Phonebook App

A contact manager built with React and Redux Toolkit. Add, search and delete
contacts; state is synced with a REST backend through async thunks.

**[Live demo](https://YOUR-NEW-URL.vercel.app)**

![Phonebook App screenshot](docs/screenshot.png)

## Features

- Add contacts with form validation (Formik + Yup)
- Filter contacts by name as you type
- Delete contacts
- Server-synced state via Redux Toolkit async thunks (Axios)
- [Loading / error handling: verify and describe, or remove this line]

## Tech stack

| Area | Tools |
|---|---|
| UI | React 19, CSS Modules, react-icons |
| State | Redux Toolkit, React Redux |
| Forms | Formik, Yup |
| HTTP | Axios, MockAPI |
| Tooling | Vite, ESLint |

## Getting started

```bash
git clone https://github.com/Full-Stack-Web-Applications/Phonebook_App.git
cd Phonebook_App
cp .env.example .env     # set VITE_API_URL
npm install
npm run dev
```

Requires Node.js 20.19+ (check the Vite docs for the exact range).
Other scripts: `npm run build`, `npm run preview`, `npm run lint`.

## How it works

`contactsSlice` holds the contact list and talks to the API through async
thunks (fetch, add, delete). `filtersSlice` holds the search term.
`ContactList` derives the visible list from both slices.

## Project structure

```
src/
├── redux/        store, contactsSlice, filtersSlice
└── components/   ContactForm, ContactList, Contacts, SearchBox
```

## Limitations and next steps

- No automated tests yet (planned: Vitest + React Testing Library)
- The demo backend is a public, unauthenticated MockAPI endpoint, so data can
  be changed by any visitor
- [No edit-contact feature: verify]
