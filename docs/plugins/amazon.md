# AffiliatePluginAmazon
This plugin for open source [Affiliate package](https://github.com/teamtofu/affiliate) automatically affiliates Amazon URLs based upon locality.

## Affiliate Main Package

Make sure [Affiliate](https://affiliate.js.org/) is already installed.

## Installation

With NPM
```bash
$ npm i -S affiliate-plugin-amazon
```

With Yarn
```bash
$ yarn add affiliate-plugin-amazon
```

With a CDN
```html
<script src="https://unpkg.com/affiliate@latest/dist/affiliate.js"></script>
<script src="https://unpkg.com/affiliate-plugin-amazon@latest/dist/plugin.js"></script>
```

With Bower
```bash
$ bower install -S affiliate-plugin-amazon
```

## What It Can Do

Affiliate can modify the following link into any of the others.
```html
<a href="https://www.amazon.co.jp/dp/B01MRZFBBH">Japan</a>
<a href="https://www.amazon.com/dp/B01MRZFBBH">USA</a>
<a href="https://www.amazon.de/dp/B01MRZFBBH">Germany</a>
<a href="https://www.amazon.co.uk/dp/B01MRZFBBH">UK</a>
```

All links would become (if the user's primary language is Italian):
```html
<a href="https://www.amazon.it/dp/B01MRZFBBH?tag=italian-tag">My Locality</a>
```

Or url modification can be disabled:
```html
<a href="https://www.amazon.co.jp/dp/B01MRZFBBH?tag=jp-tag">Japan</a>
<a href="https://www.amazon.com/dp/B01MRZFBBH?tag=us-tag">USA</a>
<a href="https://www.amazon.de/dp/B01MRZFBBH?tag=de-tag">Germany</a>
<a href="https://www.amazon.co.uk/dp/B01MRZFBBH?tag=gb-tag">UK</a>
```

## Documentation

```js
var Affiliate = require('affiliate'); 
var AffiliatePluginAmazon = require('affiliate-plugin-amazon'); 

var amazonAff = AffiliatePluginAmazon(Affiliate, {
    tags: {
        us: '', // for USA, required
        gb: '', // for UK
        de: '', // for Germany
        fr: '', // for France
        jp: '', // for Japan
        ca: '', // for Canada
        cn: '', // for China
        it: '', // for Italy
        es: '', // for Spain
        in: '', // for India
        br: '', // for Brazil
        mx: '' // for Mexico
    },
    debug: false, // verbose logging into the console, default off
    locale: null, // manually set the country code of the browser, default automatic
    modifyDomain: true // modify domains like amazon.com to amazon.co.uk based on locale, default on
});

// amazonAff is now an Affiliate instance

amazonAff.attach(); // this will start affiliation
```

## License

MIT (C) [Russell Steadman](https://teamtofu.github.io/contact). Learn more in the [LICENSE](https://github.com/teamtofu/affiliate-plugin-amazon/blob/master/LICENSE) file.

## Support Me

Like this project? Buy me a [cup of coffee](https://www.paypal.me/RussellSteadman/3). &#x2615; Here are more of my [projects](https://teamtofu.github.io/).