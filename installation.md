# Installation

This React template is based on [create-react-app](https://github.com/facebook/create-react-app) and has its `README.md` which you can find very useful.

{% hint style="info" %}
You **don’t** need to install or configure tools like Webpack or Babel.  
They are configured and hidden so that you can focus on the code.
{% endhint %}

## To get started follow this steps

1. First of all it's required to Install [Node](https://nodejs.org/en/) and npm / [yarn](https://yarnpkg.com/lang/en/).
2. Open your favorite console application \(Terminal, iTerm, Command Prompt etc.\). Navigate to the `mintone/`folder and **Install packages**  : `npm i,` `npm install` or `yarn install`. This command will install all the required [Node.js ](https://nodejs.org/en/)modules into the `node_modules` directory inside `mintone/`folder. And now, you are ready to run the Mintone for the first time.
3. To run project locally: `npm start` or `yarn start` This command will runs the app in development mode. Open [http://localhost:3000](http://localhost:3000/) to view it in the browser.

   The page will automatically reload if you make changes to the code.

4. Now you can use This React project for your application development, make the necessary changes.
5. To builds the app for production `npm run build` or `yarn build`. It will create the `build/` folder inside  this project directory .It correctly bundles React in production mode and optimizes the build for the best performance. The build is minify and the filenames include the hashes. Your app is ready to be deployed.

{% hint style="success" %}
The project was built assuming it is hosted at the server root folder of domain/platform i.e `http://example.com`.

You can control this with the homepage field in your `package.json`. To deploy build for sub-folder i.e `http://example.com/folder-name/` than `"homepage" : "http://example.com/folder-name/".`

You also need to set base-name `<BrowserRouter basename="folder-name">` in `router.js` file.
{% endhint %}

You can find detailed instructions on using Create React App and many tips in [its documentation](https://facebook.github.io/create-react-app/).

{% hint style="warning" %}
**You’ll need to have Node v12.x.x or later on your local development machine** \(but it’s not required on the server\). You can use [nvm](https://github.com/creationix/nvm#installation) \(macOS/Linux\) or [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) to easily switch Node versions between different projects.
{% endhint %}

