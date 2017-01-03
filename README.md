sweet-alert-rails-confirm-bootstrap
=========================

A Rails confirm replacement with SweetAlert modified for compatibility with [bootstrap-sweetalert](https://lipis.github.io/bootstrap-sweetalert)

Depends on https://lipis.github.io/bootstrap-sweetalert/

Install Bootstrap Sweetalert via Bower:
```
bower install bootstrap-sweetalert
```
    
Or via Rails-Assets:
``` ruby
gem 'rails-assets-bootstrap-sweetalert', source: 'https://rails-assets.org'
```

## Requirements
Rails >= 3.1

## Usage

Add it to your Gemfile:
```ruby
gem 'sweet-alert-confirm'
```

Add the following to application.js:

```javascript
//= require bootstrap-sweetalert
//= require sweet-alert-confirm
```
Add the following to application.scss:

```scss
/*
@import "bootstrap-sweetalert";
 */
```

### Custom options


You can pass options in `data:`
```Ruby
 data: {
  confirm: 'Are you ready?'
  :'confirm-button-text' => 'Im ready',
  :'cancel-button-text' => 'No way',
  :'confirm-button-color' => '#66CD00',
  :'sweet-alert-type' => 'info',
  text: 'This is a subtitle',
  :'image-url' => '/pic.png'
}
```

![Custom confirm](https://cloud.githubusercontent.com/assets/5833678/4653700/14389916-54b0-11e4-9850-14ee970e9345.png)

Default options that will be used application wide so it is not nessecary to set the option on each link. Put this object inside your app to override default options with `sweetAlertConfirmConfig` object.

```Javascript
var sweetAlertConfirmConfig = {
  title: 'Are you sure?',
  type: 'warning',
  showCancelButton: true,
  confirmButtonClass: 'btn-danger',
  confirmButtonText: 'Ok'
};
```

### Before Callback

A callback that will be runned before alert is shown. Returning `false` will display the alert and `true` will _not_ display it.

`data-saBeforeFunction='myFunction'`

## Contribute

Fork the repo & pull request you fix/feature

append `RAILS_VERSION=4.1.2` or whichever you target before your `bundle` command ex: `RAILS_VERSION=4.1.2 bundle install`

please add/modify test examples on fix or features
