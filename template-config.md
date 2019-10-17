# Template Config

{% hint style="info" %}
You can edit this file at **`[ ../src/config.ts ]`**
{% endhint %}

| **Option** | **Default** | **Data Type** | **Description** |
| :--- | :--- | :--- | :--- |
| **layout** | vertical | String | `vertical`, `horizontal` |
| **subLayout** | - | String | `horizontal-2` \(only used for layout is horizontal\) |
| **collapseMenu** | false | Boolean | `true`, `false` |
| **layoutType** | menu-dark | String | `menu-dark`, `menu-light`, `dark` |
| **headerBackColor** | header-default | String | `default-header`,`header-blue`, `header-red`, `header-purple`, `header-info`,  `header-green`,`header-dark` |
| **navBrandColor** | brand-default | String | `brand-default`, `brand-blue`, `brand-red`, `brand-purple`, `brand-info`, `brand-green`, `brand-dark` |
| **rtlLayout** | false | Boolean | `true`, `false` |
| **navFixedLayout** | true | Boolean | `true`, `false` |
| **headerFixedLayout** | true | Boolean | `true`, `false` |
| **boxLayout** | false | Boolean | `true`, `false` |

{% code-tabs %}
{% code-tabs-item title="config.js" %}
```javascript
export default {
    defaultPath: '/dashboard/analytics',
    basename: '/pangong/react/default', // only at build time to set, like //pangong/react/
    layout: 'vertical', // vertical, horizontal
    subLayout: '', // horizontal-2
    collapseMenu: false, // mini-menu
    layoutType: 'menu-dark', // menu-dark, menu-light, dark
    headerBackColor: 'default-header', // default-header, header-blue, header-red, header-purple, header-green header-info, header-dark
    nabBrandColor: 'brand-default', // brand-default, brand-blue, brand-red, brand-purple, brand-green brand-info, brand-dark
    rtlLayout: false,
    navFixedLayout: true,
    headerFixedLayout: true,
    boxLayout: false
};
```
{% endcode-tabs-item %}
{% endcode-tabs %}

