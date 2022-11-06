
<div id="top"></div>
<br />
<div align="center"> 
  <a href="https://salla.dev"> 
    <img src="https://salla.dev/wp-content/themes/salla-portal/dist/img/salla-logo.png" alt="Logo" width="80" height="80"> 
  </a>
  <h1 align="center">Twilight i18n</h1>
  <p align="center">
Developing your <a href="https://docs.salla.dev/docs/twilight-themes-documentation">Twilight Theme</a>   to support multiple languages is known as internationalization, or i18n (18 letters separate the i and n). Twilight i18n provides you with access to translations that are already made for your Twilight Theme. 
    <br />
    <a href="https://salla.dev/"><strong>Explore our blogs »</strong></a>
    <br />
    <a href="https://github.com/SallaApp/twilight-i18n/issues/new">Report Bug</a> · 
    <a href="https://github.com/SallaApp/twilight-i18n/discussions/new">Request Feature</a> . <a href="https://t.me/salladev">&lt;/Salla Developers&gt;</a> . <a href="https://docs.salla.dev/docs/twilight-themes-documentation">Official Documentation</a> 
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details open>
  <summary>Table of Contents</summary>
<ol>
<li><a  href="#overview">Overview</a></li>
<li><a  href="#usage">Usage</a>
<ul>
<li><a  href="#upload">Download</a></li>
<li><a  href="#download">Upload</a></li>
<li><a  href="#translation-retrieval">Translation retrieval</a></li>
</ul>
</li>

<li><a  href="#support">Support</a></li>
<li><a  href="#contributing">Contributing</a></li>
<li><a  href="#credits">Credits</a></li>
<li><a  href="#license">License</a></li>
</ol>
</details>

<br>

## Overview
The internationalization feature of Twilight Themes makes it easy to pull out strings in other languages, because it involves separating the texts from the code. This makes it easy for Salla theme developers to support multiple languages. The internationalization files, which are JSON based files, are located in the locales directory [`src/locales/`](https://github.com/SallaApp/theme-raed/tree/master/src/locales) and are used to define translation strings. This directory contains a JSON file for each language supported by the Twilight Theme. For applications with a large number of translatable strings, this strategy is recommended.

Following is the location of the internationalization files within a Twilight Theme:

```sh
...
└── src 
    ├── locales
      ├── ar.json
      ├── en.json
      .....
...
```
 
## Usage 
The developer can simply use this [Twilight i18n](https://github.com/SallaApp/twilight-i18n/tree/master/locales) to extend or update the given translation comes with the Twilight default theme.

### Download
By browsing the folder [Twilight i18n](https://github.com/SallaApp/twilight-i18n/tree/master/locales), the developer may download the language translations that he wants to support in his theme. 

### Upload 
For any Twilight Theme, the  internationalization files are located in the locales directory [`src/locales/`](https://github.com/SallaApp/theme-raed/tree/master/src/locales), so simply the developer can upload to the path the translation file of the language he is supporting.

> The developer has the option to add more text to his translation files, as well as update and give translation. This better supports his own special needs.

### Translation retrieval
For retrieving the translation strings, the developer can simply use the default helper [trans()](https://salla.stoplight.io/docs/twilight-themes-documentation/afad4e4ff0cda-twilight-flavoured-twig#trans) function. This helper translates the passed key to the current store language. Retrieving the translation can be done in deafferent ways:

- Simple key: 
```js
<!-- simple key -->
<span>{{ trans('common.remember_my_choice') }}</span>
```

- Key with variable:
```js
<!-- key with variable -->
<span>{{ trans('blocks.header.cart', ['word' => 'Products']) }}</span>
```
- Key with enforced locale/language:
```js
<!-- key with enforced locale/language -->
<!-- this will always print the result of key in English even if the store has different default language -->
<span>{{ trans('common.titles.orders', [], en) }}</span>
```

<p align="right">(<a href="#top">back to top</a>)</p>

## Support

The team is always here to help you. Happen to face an issue? Want to report a bug? You can submit one here on Github using the [Issue Tracker](https://github.com/SallaApp/theme-raed/issues/new). If you still have any questions, please contact us via the [Telegram Bot](https://t.me/SallaSupportBot) or join in the Global Developer Community on [Telegram](https://t.me/salladev).

<p align="right">(<a href="#top">back to top</a>)</p>

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create.
Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request.
You can also simply open an issue with the tag "enhancement". Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

## Credits
- [Salla](https://github.com/sallaApp)
- [All Contributors](../../contributors)
<p align="right">(<a href="#top">back to top</a>)</p>

## License
The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
<p align="right">(<a href="#top">back to top</a>)</p>
