# Template Config

`elite-able/templateConfig.js` file contain template lyaout customization related settings.

**Template config options:**

| Attribute | Type | Options |
| :--- | :--- | :--- |
| themeLayoutColor | string | layout-light-dark,layout-dark, layout-light |
| headerBg | string | light,blue,red,purple,info,dark |
| settingOptions | boolean | true**/**false |
| themeLayoutBox | boolean | true**/**false |
| sidebarCollapsed | boolean | true**/**false |
| sidebarFixed | boolean | true**/**false |
| headerFixed | boolean | true**/**false |
| sidebarBrandColor | string | dark,blue,red,purple,info |

## Sidebar \(Menu\) config options:

| Attribute | Type | Options |
| :--- | :--- | :--- |
| iconColor | boolean | true/false |
| menuCaption | boolean | true/false |
| captionColor | string | default,dark,blue,red,purple,info |
| dropdownIcon | string | arrow\_single , arrow\_double, plus |
| listIcon | string | curcile, line, check, arrow\_shift, arrow\_double, arrow\_single |
| activeColor | string | light,dark,blue,red,purple,info |
| menuBg | string | default,blue,red,purple,info,dark |
| menuBgGradient | string | default,blue,red,purple,info,dark |
| menuBgPattern | string | default,1,2,3,4,5,6 |
| menuBgImage | string | default,1,2,3,4,5 |

{% code-tabs %}
{% code-tabs-item title="templateConfig.js" %}
```javascript
// Elite able React Template Config File
//------------------------------------

// You can customize the theme with the help of this file

//Template config options
const templateConfig = {
  themeLayoutColor: "layout-light-dark", // Options: layout-light-dark,layout-dark, layout-light - Set layout-dark for dark mode and layout-light for light.
  headerBg: "light", //Options: light,blue,red,purple,info,dark - Set siderbar brand color one
  settingOptions: true, //Options: true,false | set false for hidden settings options
  themeLayoutBox: false, //Options: true,false | set true for box layout
  sidebarCollapsed: false, //Options: true,false | set true for Collapsed sidebar
  sidebarFixed: true, //Options: true,false | set false for static sidebar
  headerFixed: true, //Options: true,false | set false for static Header
  sidebarBrandColor: "dark", //Options: dark,blue,red,purple,info - Set siderbar brand color one
  menuSettings: {
    iconColor: false, //Oprions: true,false | set true for collerd icons
    menuCaption: true, //Oprions: true,false | set false for hidden menu Caption
    captionColor: "default", //Options: default,dark,blue,red,purple,info - Set menu caption color one
    dropdownIcon: "arrow_single", // Options: arrow_single , arrow_double, plus - Set dropdown menu icon one
    listIcon: "curcile", //Options: curcile, line, check, arrow_shift, arrow_double, arrow_single - Set  menu list icon one
    activeColor: "blue", //Options: light,dark,blue,red,purple,info - Set siderbar active color one
    menuBg: "default", //Options: default,blue,red,purple,info,dark - Set siderbar background color one
    menuBgGradient: "default", //Options: default,blue,red,purple,info,dark - Set siderbar background Gradient color one
    menuBgPattern: "default", //Options: default,1,2,3,4,5,6 - Set siderbar background Pattern one
    menuBgImage: "default" //Options: default,1,2,3,4,5 - Set siderbar background image one
  },

  fixedHeader: true // Options: true, false - Set true for fixed Header.
};

export default templateConfig;
```
{% endcode-tabs-item %}
{% endcode-tabs %}

