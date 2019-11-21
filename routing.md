# Routing

This template routing system based on [react-router](https://reacttraining.com/react-router/) and its package [react-router-dom,](https://reacttraining.com/react-router/web/guides/quick-start) it's also use code splitting for better performance.

{% hint style="info" %}
**How can I add new page with menu item ?**

You can use the below explanation to add/remove menu routs and their menu items.
{% endhint %}

## Configure route

Open `gradient-able/src/routse.js` and `gradient-able/src/routes.js`You will find the below example code. In below code we have show how you can add new page route.

{% tabs %}
{% tab title="router.js" %}
```javascript
import { lazy } from 'react';

const Server = lazy(() => import("./views/dashboard/server"))
const Project = lazy(() => import("./views/dashboard/project/*"))
const Shop = lazy(() => import("./views/dashboard/shop"))
const Analaytics = lazy(() => import("./views/dashboard/analyatics"))
...
...
...

const Route = [
  /* Dashboard */
  { exact: true, path: "/dashboard/server", name: "Server", component: Server },
  { exact: true, path: "/dashboard/analytics", name: "Analaytics", component: Analaytics },
  ...
  ...
]
export default Route
```
{% endtab %}
{% endtabs %}

## Add menu item

To add menu items you can use `gradient-able/src/menu-items.js` file. Below code we have show how you can use new menu item.

{% tabs %}
{% tab title="menus.js" %}
```javascript
export default {
    items: [
        {
            id: 'navigation',
            title: 'Navigation',
            type: 'group',
            icon: 'icon-navigation',
            children: [
                {
                    id: 'dashboard',
                    title: 'Dashboard',
                    type: 'collapse',
                    icon: 'feather icon-home',
                    children: [
                        {
                            id: 'server',
                            title: 'Server',
                            type: 'item',
                            url: '/dashboard/server'
                        },
                        {
                            id: 'shop',
                            title: 'Shop',
                            type: 'item',
                            url: '/dashboard/shop',
                            badge: {
                                title: 'NEW',
                                type: 'badge-danger'
                            }
                        }
                    ]
                },
            ]
        },
        ...
        ...
        ...
        {
            id: 'support',
            title: 'Support',
            type: 'group',
            icon: 'icon-support',
            children: [
                {
                    id: 'menu-level',
                    title: 'Menu Levels',
                    type: 'collapse',
                    icon: 'feather icon-menu',
                    children: [
                        {
                            id: 'menu-level-1.1',
                            title: 'Menu Level 1.1',
                            type: 'item',
                            url: '#!',
                        },
                        {
                            id: 'menu-level-1.2',
                            title: 'Menu Level 2.2',
                            type: 'collapse',
                            children: [
                                {
                                    id: 'menu-level-2.1',
                                    title: 'Menu Level 2.1',
                                    type: 'item',
                                    url: '#',
                                },
                                {
                                    id: 'menu-level-2.2',
                                    title: 'Menu Level 2.2',
                                    type: 'collapse',
                                    children: [
                                        {
                                            id: 'menu-level-3.1',
                                            title: 'Menu Level 3.1',
                                            type: 'item',
                                            url: '#',
                                        },
                                        {
                                            id: 'menu-level-3.2',
                                            title: 'Menu Level 3.2',
                                            type: 'item',
                                            url: '#',
                                        }
                                    ]
                                }
                            ]
                        }
                    ]
                },
                {
                    id: 'disabled-menu',
                    title: 'Disabled Menu',
                    type: 'item',
                    url: '#',
                    classes: 'nav-item disabled',
                    icon: 'feather icon-power'
                },
                {
                    id: 'sample-page',
                    title: 'Sample Page',
                    type: 'item',
                    url: '/sample-page',
                    classes: 'nav-item',
                    icon: 'feather icon-sidebar'
                }
            ]
        }
    ]
}
```
{% endtab %}
{% endtabs %}

