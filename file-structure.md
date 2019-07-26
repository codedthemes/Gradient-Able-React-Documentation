# File Structure

## Project structure

Under the `next/`folder you will find the project folder structure.

```text
next/
├── .gitignore
├── package.json            -> Package json file.
├── README.md               -> Creat react app Readme file
├── server.js
├── public/
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
└── src/
    ├── app/
    |    ├── app.js
    |    ├── router.js      -> Add routers for pages
    ├── assets/
    |    ├── images/
    |    ├── css/
    |    ├── fonts/
    |    ├── scss/          -> Template SCSS files, check folder structure below
    ├── components/         -> Template custom components
    ├── containers/         -> Data fetching and then renders its corresponding sub-component
    ├── layouts/            -> Layout components & routers
    ├── redux/              -> Redux App actions, reducers, storeConfig & types
    ├── utiliy/
    ├── views/              -> View files for all pages
    ├── index.js            -> Application root js file
    ├── index.scss          -> Application main scss file
    ├── registerServiceWorker.js
    └── templateConfig.js   -> Config. file to change layouts & menu color, width, image etc...
```

## SCSS structure

Under the `next/assets/scss/`folder you will find the following folder structure.

```text
SCSS/
├── core/                  -> Template core files
├── layout/                -> Template layouts scss folder
├── mixins/                -> Custom mixins scss folder
├── other/                 -> Third party plugins customisation scss
├── pages/                 -> Template extra pages
├── theme-elements/        -> React views specific scss files
├── _color.scss            -> All color variables
├── _fonts.scss            -> Template font customizer
├── _variable.scss         -> Template variables
├── style.scss             -> Application main file
```

