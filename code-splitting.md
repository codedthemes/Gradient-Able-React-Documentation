# Code Splitting

## Code Splitting <a id="code-splitting"></a>

Bundling is great, but as your app grows, your bundle will grow too. Especially if you are including large third-party libraries. You need to keep an eye on the code you are including in your bundle so that you don’t accidentally make it so large that your app takes a long time to load.

To avoid winding up with a large bundle, it’s good to get ahead of the problem and start “splitting” your bundle. [Code-Splitting](https://webpack.js.org/guides/code-splitting/) is a feature supported by bundlers like Webpack and Browserify \(via [factor-bundle](https://github.com/browserify/factor-bundle)\) which can create multiple bundles that can be dynamically loaded at runtime.

## React.lazy

> `React.lazy` and Suspense is not yet available for server-side rendering. If you want to do code-splitting in a server rendered app, we still recommend [React Loadable](https://github.com/thejameskyle/react-loadable). It has a nice [guide for bundle splitting with server-side rendering](https://github.com/thejameskyle/react-loadable#------------server-side-rendering).

The `React.lazy` function lets you render a dynamic import as a regular component.

### Before code splitting:

```javascript
import OtherComponent from './OtherComponent';

function MyComponent() {
  return (
    <div>
      <OtherComponent />
    </div>
  );
}
```

### After code splitting:

```javascript
const OtherComponent = React.lazy(() => import('./OtherComponent'));

function MyComponent() {
  return (
    <div>
      <OtherComponent />
    </div>
  );
}
```

This will automatically load the bundle containing the `OtherComponent` when this component gets rendered.

`React.lazy` takes a function that must call a dynamic `import()`. This must return a `Promise` which resolves to a module with a `default` export containing a React component.

* Reference: [Code Splitting](https://reactjs.org/docs/code-splitting.html)
* For more details : [https://reactjs.org/docs/code-splitting.html](https://reactjs.org/docs/code-splitting.html) 

