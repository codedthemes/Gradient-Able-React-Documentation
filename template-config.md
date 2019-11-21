# Template Config

{% hint style="info" %}
You can edit this file at **`[ ../src/config.ts ]`**
{% endhint %}

| **Option** | **Default** | **Data Type** | **Description** |
| :--- | :--- | :--- | :--- |
| **layout** | vertical | String | `vertical`, `horizontal` |
| **collapseMenu** | false | Boolean | `true`, `false` |
| **layoutType** | menu-dark | String | `menu-dark`, `menu-light`, `dark` |
| **headerBackColor** | header-default | String | `default-header`,`header-blue`, `header-red`, `header-purple`, `header-info`,  `header-green`,`header-dark` |
| **fullWidthLayout** | false | Boolean | `true`, `false` |
| **navFixedLayout** | true | Boolean | `true`, `false` |
| **headerFixedLayout** | true | Boolean | `true`, `false` |

{% tabs %}
{% tab title="config.js" %}
```javascript
export default {
    defaultPath: '/dashboard/analytics',
    basename: '/gradient-able/react/default', // only at build time to set, like ///gradient-able/react/default
    layout: 'vertical', // vertical, horizontal
    collapseMenu: false, // mini-menu
    layoutType: 'menu-light', // menu-dark, menu-light
    headerBackColor: '', // header-blue, header-red, header-purple, header-info, header-dark
    fullWidthLayout: false,
    navFixedLayout: true,
    headerFixedLayout: true
};
```
{% endtab %}
{% endtabs %}

