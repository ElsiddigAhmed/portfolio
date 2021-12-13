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
│   ├── utiles
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

---
## Helpers

In the helpers folder we have many different classes writted to manage, access and update system statuses and so many things on the code like accessing storage and using different type of storage by the system, you can also use api adapters and services classes provided as a helpers.

### here are a list of helpers you can use in the system.

- accessing and managing storage on the system using __storage adapter class__.
- connecting to the api and passing data to remote web services using __service class__.
- change and handle system settings using __system status class__.
- using the the remote proxy and connecting to the apis in one place using __api proxy class__.

---
## Routing And Pages.

using __react-router-dom__ to handle routing on the system and creating several routing components that accept many type of authentication and different roles of users to manage auth and protected routes and provide a smooth access to it.

---
## Components And Shared Code.

we have all shared code, layout and reused components under one folder called components and we put all main pages and screens that have a seperate page url in __pages__ folder, the components like dashboard layout, inputs and lists, popup wrappers and all of that as a reusable elements in the system so they should not depent on a specific page or some other code and they are wildly used in the system.

---
## Data Management.

We use __Redux__ to handle and manage data and system states, so far we need to enhance the data management a bit in free time but we have the controllers working fine and all data changing states are handled by __redux__ , we use thunk middleware as a simple and easy to understand middleware for redux, _we do not save user status on redux states but we temperarly storing them while we fetching data from web services.

---
## Testing

We have testing the main units in the code as a unit test and also the system as a one unit running using integration test, the __ test __ folder contain the unit test for all units on the system that are dependent from other units or code like api proxy and system status and so many things out there.
