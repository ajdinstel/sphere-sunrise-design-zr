# SPHERE.IO Sunrise design

![SPHERE.IO icon](https://admin.sphere.io/assets/imag-zres/sphere_logo_rgb_long.png)

[![Build Status](https://travis-ci.org/ajdinstel/sphere-sunrise-design-zr.png?branch=master)](https://travis-ci.org/ajdinstel/sphere-sunrise-design-zr) [![Stories in Ready](https://badge.waffle.io/ajdinstel/sphere-sunrise-design-zr.png?label=ready&title=Ready)](https://waffle.io/ajdinstel/sphere-sunrise-design-zr)

###Demo
- [Home](http://ajdinstel.github.io/sphere-sunrise-design-zr/home.html)
- [Product Overview](http://ajdinstel.github.io/sphere-sunrise-design-zr/pop.html)
- [Product Detail](http://ajdinstel.github.io/sphere-sunrise-design-zr/pdp.html)
- [Cart Detail](http://ajdinstel.github.io/sphere-sunrise-design-zr/cart.html)
- [Checkout Sign In (1/5)](http://ajdinstel.github.io/sphere-sunrise-design-zr/checkout-signin.html)
- [Checkout Shipping (2/5)](http://ajdinstel.github.io/sphere-sunrise-design-zr/checkout-shipping.html)
- [Checkout Payment (3/5)](http://ajdinstel.github.io/sphere-sunrise-design-zr/checkout-payment.html)
- [Checkout Confirmation (4/5)](http://ajdinstel.github.io/sphere-sunrise-design-zr/checkout-confirmation.html)
- [Checkout Thank You (5/5)](http://ajdinstel.github.io/sphere-sunrise-design-zr/checkout-thankyou.html)
- [My Account: Personal Details](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-personal-details.html)
- [My Account: Address Book](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-address-book.html)
- [My Account: Payment Details](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-payment-details.html)
- [My Account: My Orders](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-my-orders.html)
- [My Account: My Orders - Single Order](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-my-orders-order.html)
- [My Account: Returns / Exchange](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-returns-exchange.html)
- [My Account: Returns / Exchange - Single Return](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-returns-exchange-order.html)
- [My Account: Wishlist](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-wishlist.html)
- [My Account: Login](http://ajdinstel.github.io/sphere-sunrise-design-zr/my-account-login.html)
- [Confirmation Email](http://ajdinstel.github.io/sphere-sunrise-design-zr/confirmation-email.html)
- [Dispatch Email](http://ajdinstel.github.io/sphere-sunrise-design-zr/dispatch-email.html)
- [No Search Result](http://ajdinstel.github.io/sphere-sunrise-design-zr/no-search-result.html)
- [Mix & Match](http://ajdinstel.github.io/sphere-sunrise-design-zr/mix-match.html)



###Installation

- Install [Node.js](https://nodejs.org/) and [NPM](https://www.npmjs.com/)
- Install [Sass](http://sass-lang.com/install)
- Install [Grunt](http://gruntjs.com/getting-started)
- Run `npm install` in the project root to install the project dependencies.

###Usage

#####Useful commands

`grunt` to build the generated site and watch for changes

`grunt build` to build the generated site

`grunt publish` to publish the generated site to GitHub Pages (requires $GH_TOKEN)

`grunt release-[patch|minor|major]` to release the current version to the Maven Bintray repository and prepare a new version (requires commercetools-bintray repository ID in Maven's settings.xml)

`grunt clean build maven:install` to install to local maven repository (~/.m2/repository/io/sphere/sphere-sunrise-design-zr)

Notice you can always add `--verbose` and/or `--debug` to any command in order to obtain more information.

#####Generated site

Once the project is built, the generated site is located in the `output/` folder.

#####Executed tasks

`grunt clean`
  - Removes the `output/` folder with the generate site

`grunt copy`
  - Copy any CSS file in `input/assets/css/` to `output/assets/css/`
  - Copy any JS file in `input/assets/js/` to `output/assets/js/`
  - Copy any file in `input/assets/img/` to `output/assets/img/`
  - Copy any file in `input/assets/font/` to `output/assets/font/`
  - Copy any Handlebars template in `input/templates/` to `output/templates/` (it flattens any directory)
  - Copy any HTML file in `input/` to `output/` (be careful not to use the same name as a Handlebars template or it will be overwritten)


`grunt coffee`
  - Compile and concatenate any Coffeescript file inside `input/assets/js/` into `output/assets/js/coffee.js`


`grunt sass`
  - Processes `input/assets/css/main.scss` into `output/assets/css/main.min.css`

`grunt postcss`
  - Adds vendor-prefixed CSS properties to `output/assets/css/main.min.css`

`grunt compile-handlebars`
  - Generates HTML files from the Handlebars templates and JSON data defined in `input/templates/` and the partial templates defined in `input/templates/partials/` into `output/`
