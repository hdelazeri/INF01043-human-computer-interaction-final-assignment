# Despensa

[Português](README.pt-BR.md)

Mobile pantry manager for household grocery inventory. Built as a coursework project for **INF01043 — Interação Homem-Computador** (Human–Computer Interaction) in the Computer Science program at [UFRGS](https://www.ufrgs.br/) (Universidade Federal do Rio Grande do Sul).

## Features

- Browse products currently in the pantry
- Add items manually (barcode, name, quantity)
- Import items by scanning the QR code on a Brazilian electronic receipt (NFC-e / SEFAZ-RS)
- Review scanned items and choose which ones to keep
- Remove one unit or delete a product entirely
- Persist inventory locally with AsyncStorage

## Tech stack

- [Expo](https://expo.dev/) (~44) / React Native
- TypeScript
- React Navigation (native stack)
- Formik + Yup (manual product form)
- `expo-barcode-scanner` (receipt QR codes)
- Cheerio + Axios (parse NFC-e product list from SEFAZ-RS)
- AsyncStorage (local persistence)

## Getting started

### Prerequisites

- Node.js
- npm
- Expo Go on a device, or an iOS/Android emulator

### Install and run

```bash
npm install
npm start
```

Then press `i` for iOS, `a` for Android, or scan the QR code with Expo Go.

Other scripts:

```bash
npm run ios
npm run android
npm run web
```

## Project structure

```
App.tsx                 # Navigation and providers
src/
  Home/                 # Pantry list
  Details/              # Product detail / remove units
  AddProducts/          # QR scanner for NFC-e receipts
  AddProductsList/      # Confirm items from a scanned receipt
  NewProductForm/       # Manual add form
  contexts/             # ProductsContext + AsyncStorage
  helper.ts             # NFC-e URL parsing and scraping
```

## Course context

This app was developed for **INF01043 — Interação Homem-Computador** at the Institute of Informatics (INF), UFRGS, focusing on interaction design and usability for everyday grocery/pantry management.
