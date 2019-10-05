# File Structure

## Project structure

Under the `flat-able/`folder you will find the project folder structure.

```text
flat-able/
├── .gitignore
├── package.json            -> Package json file.
├── README.md               -> Creat react app Readme file
├── server.js
├── public/
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
└── src/
    ├── App/
    |    ├── components     -> Template custom components
    |    ├── layout         -> Layout components & routers
    |    ├── index.js 
    ├── assets/
    |    ├── images/
    |    ├── scss/          -> Template SCSS files, check folder structure below        
    ├── Demo/               -> View files for all pages
    ├── containers/         -> Data fetching and then renders its corresponding sub-component
    ├── hoc/
    ├── store/              -> Redux App actions, reducers, storeConfig & types  
    ├── config.js           -> Config. file to change layouts & menu color, width, image etc...
    ├── index.js            -> Application root js file
    ├── index.scss          -> Application main scss file
    ├── menu-item.js        -> Allication menu data
    ├── route.js            -> Add routers for pages
    ├── routes.js            -> Add routers for auth pages
    └── serviceWorker.js
```

## SCSS structure

Under the `flat-able/src/assets/scss/`folder you will find the following folder structure.

```text
SCSS/
├── ng-module/             -> Third party plugins customisation scss
├── settings/              -> Template variable scss folder
├── theme/                 -> Layout and React views specific scss files
├── layout-dark.scss       -> Application dark file
├── layout-rtl.scss        -> Application RTL file
├── style.scss             -> Application main file
```

