# Routing

This template routing system based on [react-router](https://reacttraining.com/react-router/) and its package [react-router-dom,](https://reacttraining.com/react-router/web/guides/quick-start) it's also use code splitting for better performance.

{% hint style="info" %}
**How can I add new page with menu item ?**

You can use the below explanation to add/remove menu routs and their menu items.
{% endhint %}

## Configure route

Open `pangong/src/routse.js` and `pangong/src/routes.js`You will find the below example code. In below code we have show how you can add new page route.

{% code-tabs %}
{% code-tabs-item title="router.js" %}
```javascript
import { lazy } from 'react';

const Analytic = lazy(() => import("./views/dashboard/analytic"))
const Sales = lazy(() => import("./views/dashboard/sales"))
const Crypto = lazy(() => import("./views/dashboard/crypto"))
const Project = lazy(() => import("./views/dashboard/project"))
const HelpDesk = lazy(() => import("./views/dashboard/helpdesk"))
const StatistcWidget = lazy(() => import("./views/widget/statisticWidget"))
...
...
...

const Route = [
  /* Dashboard */
  { exact: true, path: "/dashboard/analyatics", name: "Analytic", component: Analytic },
  { exact: true, path: "/dashboard/sales", name: "Sales", component: Sales },
  ...
  ...
]
export default Route
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Add menu item

To add menu items you can use `pangong/src/menu-items.js` file. Below code we have show how you can use new menu item.

{% code-tabs %}
{% code-tabs-item title="menus.js" %}
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
                            id: 'analytics',
                            title: 'Analytics',
                            type: 'item',
                            url: '/dashboard/analytics'
                        },
                        {
                            id: 'sales',
                            title: 'Sales',
                            type: 'item',
                            url: '/dashboard/sales',
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
{% endcode-tabs-item %}
{% endcode-tabs %}

