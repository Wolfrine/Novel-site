# Novel-site

Novel-site is a project for hosting and building the documentation for the NovaSaga project. The goal is to present the story online using a simple static site that will be expanded over time.

## Installation

1. Install [Node.js](https://nodejs.org/).
2. Clone this repository and install dependencies:

```bash
npm install
```

## Running the Site

Start the local development server with:

```bash
npm run dev
```

This will serve the site locally so you can preview changes.

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests. For major changes, please open an issue first to discuss what you would like to change.

## Docusaurus Documentation Site

The `docs-site` directory contains the [Docusaurus](https://docusaurus.io/) site.

### Install dependencies

```bash
cd docs-site
npm install
```

### Start the site

```bash
npm run start
```

This will launch a local development server so you can browse the documentation.

The site navigation includes a link to the [NovaSaga repository](https://github.com/Wolfrine/NovaSaga).

## Firebase Hosting

This repository includes configuration for deploying the documentation site to
Firebase Hosting. The GitHub Actions workflow in `.github/workflows` builds the
`docs-site` directory and deploys it automatically when changes are pushed to
`main`.

1. Create a Firebase project and generate a deployment token:

   ```bash
   firebase login:ci
   ```

2. Add the token as `FIREBASE_TOKEN` in your repository secrets.
3. The workflow will build and deploy the site to Firebase on every push to
   `main`.

The site will be available at `https://novel-site-en.web.app`.

If you need to initialize Firebase in client-side scripts, use the configuration
below:

```javascript
export const firebaseConfig = {
  apiKey: "AIzaSyCedk5VIVtOL7qhLeVlPShuq22CmWUzcZM",
  authDomain: "novel-site-en.firebaseapp.com",
  projectId: "novel-site-en",
  storageBucket: "novel-site-en.firebasestorage.app",
  messagingSenderId: "970614384778",
  appId: "1:970614384778:web:58cc844264bd2dfe11a573",
  measurementId: "G-HYT3FX2Z45",
};
```
