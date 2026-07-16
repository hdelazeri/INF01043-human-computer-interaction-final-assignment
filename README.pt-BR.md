# Despensa

[English](README.md)

Aplicativo móvel para gerenciar a despensa doméstica. Desenvolvido como trabalho da disciplina **INF01043 — Interação Homem-Computador** do curso de Ciência da Computação da [UFRGS](https://www.ufrgs.br/) (Universidade Federal do Rio Grande do Sul).

## Funcionalidades

- Listar os produtos da despensa
- Adicionar itens manualmente (código de barras, nome, quantidade)
- Importar itens ao escanear o QR Code da nota fiscal eletrônica (NFC-e / SEFAZ-RS)
- Revisar os produtos lidos e escolher quais salvar
- Retirar uma unidade ou remover o produto por completo
- Persistir o inventário localmente com AsyncStorage

## Tecnologias

- [Expo](https://expo.dev/) (~44) / React Native
- TypeScript
- React Navigation (native stack)
- Formik + Yup (formulário de produto manual)
- `expo-barcode-scanner` (QR Code da nota fiscal)
- Cheerio + Axios (leitura dos produtos da NFC-e na SEFAZ-RS)
- AsyncStorage (persistência local)

## Como executar

### Pré-requisitos

- Node.js
- npm
- Expo Go no celular, ou emulador iOS/Android

### Instalação e execução

```bash
npm install
npm start
```

Em seguida, pressione `i` para iOS, `a` para Android, ou escaneie o QR Code com o Expo Go.

Outros scripts:

```bash
npm run ios
npm run android
npm run web
```

## Estrutura do projeto

```
App.tsx                 # Navegação e providers
src/
  Home/                 # Lista da despensa
  Details/              # Detalhe do produto / retirada de unidades
  AddProducts/          # Scanner de QR Code da NFC-e
  AddProductsList/      # Confirmação dos itens lidos
  NewProductForm/       # Formulário de adição manual
  contexts/             # ProductsContext + AsyncStorage
  helper.ts             # Parsing e scraping da NFC-e
```

## Contexto acadêmico

Este aplicativo foi desenvolvido para a disciplina **INF01043 — Interação Homem-Computador** do Instituto de Informática (INF) da UFRGS, com foco em design de interação e usabilidade no gerenciamento cotidiano da despensa.
