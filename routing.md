# Routing

This template routing system based on [react-router](https://reacttraining.com/react-router/) and its package [react-router-dom,](https://reacttraining.com/react-router/web/guides/quick-start) it's also use code splitting for better performance.

{% hint style="info" %}
**How can I add new page with menu item ?**

You can use the below explanation to add/remove menu routs and their menu items.
{% endhint %}

## Configure route

Open `next/src/app/router.js` You will find the below example code. In below code we have show how you can add new page route.

{% code-tabs %}
{% code-tabs-item title="router.js" %}
```javascript
// import external modules
import React, { Component, Suspense, lazy } from "react";
import { BrowserRouter, Switch, Route } from "react-router-dom";
import Spinner from "../components/spinner/spinner";

// import internal(own) modules
import MainLayoutRoute from "../layout/routes/mainLayoutRoute";
import { SpinnerComponent } from "../components/spinner/Spinner";

const Analytic = lazy(() => import("../views/dashboard/analytic"));
const Sales = lazy(() => import("../views/dashboard/sales"));


class Router extends Component {
   render() {
      return (
         <BrowserRouter basename="elite-able">
            <Switch>
               <MainLayoutRoute
                exact
                path="/"
                title="Home"
                name="Analytics Dashboard"
                render={matchprops => (
                  <Suspense fallback={<SpinnerComponent />}>
                    <Analytic {...matchprops} />
                  </Suspense>
                )}
              />
              //Add new page route here
              <MainLayoutRoute
                exact
                path="/sales"
                title="Sales"
                name="Sales Dashboard"
                render={matchprops => (
                  <Suspense fallback={<SpinnerComponent />}>
                    <Sales {...matchprops} />
                  </Suspense>
                )}
              />
            </Switch>
         </BrowserRouter>
      );
   }
}

export default Router;
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Add menu item

To add menu items you can use `elite-able/src/layout/components/sidebar/sidBarMenu/menus.js` file. Below code we have show how you can use new menu item.

You can use `MenuSingle`for single menu item and `MultiMenu` for multiple menu items. You can also add badge to menu by using `badgeText`option and set badge color by using `badgeColor`Option.

{% code-tabs %}
{% code-tabs-item title="menus.js" %}
```javascript
import React, { Component } from "react";
import { NavLink, Link } from "react-router-dom";
import * as Icons from "react-feather";
import MenuHelper from "./sideMenuHelp";
import { Badge } from "./sideMenuHelp";

class Menus extends Component {
  render() {
    return (
      <MenuHelper>
        <MenuHelper.Label labelText="Navigation" />
        //Mulitiple menus
        <MenuHelper.MultiMenu
          name="Dashbord"
          Icon={<Icons.Home size={14} />}
          defaultSelect
        >
          <NavLink exact to="/" activeClassName="active">
            Analytics
          </NavLink>
          <NavLink exact to="/sales" activeClassName="active">
            Sales
          </NavLink>
          <NavLink exact to="/crypto" activeClassName="active">
            Crypto
          </NavLink>
          <NavLink exact to="/project" activeClassName="active">
            Project
          </NavLink>
          <NavLink exact to="/helpdesk" activeClassName="active">
            Helpdesk
            <Badge text="NEW" color="danger" />
          </NavLink>
        </MenuHelper.MultiMenu>
        //Single Menu
        <MenuHelper.MenuSingle path="/app/message" icon={<Icons.MessageCircle size={14} />} text="Message" />
       </MenuHelper>
      );
   }
}

export default Menus;
```
{% endcode-tabs-item %}
{% endcode-tabs %}

