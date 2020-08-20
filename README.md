# Oracle APEX Slider Pro Plugin

[![APEX Community](https://cdn.rawgit.com/Dani3lSun/apex-github-badges/78c5adbe/badges/apex-community-badge.svg)](https://github.com/Dani3lSun/apex-github-badges) [![APEX Plugin](https://cdn.rawgit.com/Dani3lSun/apex-github-badges/b7e95341/badges/apex-plugin-badge.svg)](https://github.com/Dani3lSun/apex-github-badges)
[![APEX Built with Love](https://cdn.rawgit.com/Dani3lSun/apex-github-badges/7919f913/badges/apex-love-badge.svg)](https://github.com/Dani3lSun/apex-github-badges)

APEX Slider Pro is a powerful slider plugin based on the modular, responsive and touch-enabled jQuery slider. It provides elegant and professionally looking sliders.

- [Oracle APEX Slider Pro](#oracle-apex-slider-pro-plugin)
	- [Preview](#preview)
	- [Install](#install)
	- [Plugin Settings](#plugin-settings)
	- [How to use](#how-to-use)
			- [Sample SQL Query for data source](#sample-sql-query-for-data-source)
	- [Demo Application](#demo-application)
	- [Credits](#credits)
	- [WIP](#wip)
  - [Changelog](#changelog)
  - [License](#license)

## Preview
![](https://github.com/reybis/apex-plugin-slider-pro/blob/master/preview.gif)

## Install
- Import plugin file "reybis_slider_pro.sql" from **dist** directory into your application
- *Optional:* Deploy the JS/CSS files from **src/files** directory on your web server and change the "Plugin File Prefix" to web servers folder path.
- *Optional:* Compile the plugin PL/SQL package in your APEX parsing schema and change the plugin render/ajax function to include the package object name. The package files are located in **src/db** directory.

## Plugin Settings
All the settings are component based. The plugin settings are highly customizable and you can change:

- **Orientation** - Indicates whether the slides will be arranged horizontally or vertically.
_Default value: 'horizontal'_ | _Available value: 'horizontal' and 'vertical'_
- **Width** - Sets the width of the slide. Can be set to a fixed value, like 900 (indicating 900 pixels), or to a percentage value, like '100%'. It's important to note that percentage values need to be specified inside quotes. For fixed values, the quotes are not necessary. Also, please note that, in order to make the slider responsive, it's not necessary to use percentage values. More about this in the description of the 'responsive' property.
_Default value: 500_
- **Height** - Sets the height of the slide. The same rules available for the 'width' property also apply for the 'height' property.
_Default value: 300_
- **Autoplay** - Indicates whether or not autoplay will be enabled.
_Default value: true_	 
- **Arrows** - Indicates whether the arrow buttons will showed.
_Default value: false_ 
- **Buttons** - Indicates whether the buttons will showed.
_Default value: true_
- **Breakpoints** - Sets specific breakpoints which allow changing the look and behavior of the slider when the page resizes. The 'breakpoints' property is assigned an object which contains certain browser window widths and the slider properties that are applied to those specific widths. This is very similar to CSS media queries. However, please note that these custom properties will not be inherited between different breakpoints. The slider's properties will reset to the original values before applying a new set of properties, so if you want a certain property value to persist, you need to set it for each breakpoint.
_Default value: null_
- **Responsive** - Makes the slider responsive. The slider can be responsive even if the 'width' and/or 'height' properties are set to fixed values. In this situation, 'width' and 'height' will act as the maximum width and height of the slides.
_Default value: true_ 	 
- **Custom** - Add custom json properties based on the slider pro plugin (See: https://github.com/bqworks/slider-pro/blob/master/docs/api.md).

## How to use
- New Item based on Slider Pro
- Set the SQL Query for data source
- Choose best fitting settings


#### Sample SQL Query for data source

```language-sql
select 'https://github.com/reybis/apex-plugin-slider-pro/blob/master/src/demo/dominican_republic_01.jpg' image, 
        'Playa El Valle, Dominican Republic' alt from dual union all
select 'https://github.com/reybis/apex-plugin-slider-pro/blob/master/src/demo/dominican_republic_02.jpg' image, 
        'Punta Cana, Dominican Republic' alt from dual union all
select 'https://github.com/reybis/apex-plugin-slider-pro/blob/master/src/demo/dominican_republic_03.jpg' image, 
       'Puente De Cayo Samana, Dominican Republic' alt from dual
```

## Demo Application
https://apex.reybis.com/ords/f?p=APEXPLUGINS

user: demo | pass: demo

## Credits
Slider Pro jQuery plugin by [bqworks](https://github.com/bqworks/slider-pro)

## WIP
All the features of the original jQuery plugin adapted to Oracle APEX.

## Changelog

#### 1.0.0 - Initial Release

## License
MIT