# TMA Dashboard
## About the application/dashboard


TMA dashboard is a c-panel for (Teach Me Arabic) project for e-learning and eductating arabic language for non-native speakers

---
## How to get up and running.

- clone this repo to your local machine 
- open terminal in the repo dir and run __yarn__ to install dependancies
- after installing all packages run __yarn start__ to start the application on __localhost:3000__
- build the binary optemized version of the app by running yarn build

---
## Filesystem and file architecture.


```
├── public
├── package.json
├── src
│   ├── __ test __
│   ├── app
│   ├── pages
│   ├── 
│   ├── pages
│       ├── auth
│       ├── groups
│       ├── live-classes
│       ├── levels
│       ├── permissions
│       ├── students
│       ├── users
│       ├── settings
│       ├── reports
│       ├── home
│       ├── packages
│       ├── packages
│       ├── profile
│       └── index.ts
│   ├── components
│   ├── shared
│   ├── locales
│   ├── helpers
│   ├── ducks
│   ├── configs
│   ├── assets
│   ├── utile
│   ├── app.test.tsx
│   ├── index.tsx
│   ├── i18n.ts
│   └── env.ts
└── README.md
```

--- 
## Localisation

We use i18next library to provide dashboard users with multi-languages experiance  and let them toggle between languages at any time, for now we use only english and arabic languages.

---
## Configuration And Environment Variables

We have a env.ts file located on the src folder which uses to manage the branch or server environment like __stage__ , __dev__ or __production__, you can access any of these servers by changing env file, and in the configs file we have __API URIs__ management according to the env variable set on the bracnch.

There are three different json files for the several environment each file contain only one server URIs and can be used for accessing the server and only one json file executed at the time.

---
## Handling Forms
 
Using __react-hook-form__ to handle html forms and extract the data out of it and there are custom hooks to manage and reformat the data after extracted by __react-hook-form__.


