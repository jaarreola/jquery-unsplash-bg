# jquery-unsplash-bg

jQuery plugin to change a full background image from Unsplash

## Installation
```
npm install jquery-unsplash-bg
```

## Load
```html
<script src="/node_modules/jquery/dist/jquery.js"></script>
<script src="/node_modules/jquery-unsplash-bg/dist/index.js"></script>
```

## Usage
Create a container where you want to set a full background image(`div`, `section`, `article`, etc.)
```html
<div id="full-bg-random"></div>
```

Before using the Unsplash API, you need to [register as a developer](https://unsplash.com/developers).
You must put the **CLIENT_ID** in order to be enable to get photos from Unsplash API.

```js
window.unsplashBg.setup(clientId);
```

Call the plugin:
```js
$(document).ready(function(){
  window.unsplashBg.setup(clientId);

  // get random photo
  $('#full-bg-random').unsplashBg({
    backgroundColor: 'red'
  });

});
```

### Options
By default the plugin use some values:
```js
{
  height: '100vh',
  width: '100%',
  minHeight: '800px',
  backgroundSize: 'cover',
  backgroundPosition: 'center',
  backgroundColor: 'black'
}
```

You can override them:
```js
$('#full-bg-random').unsplashBg({
  minHeight: '900px',
  backgroundSize: 'contain'
});
```

In case that endpoint of Unsplash responses with errors, you can set an image(this only is visible when Unsplash endpoint fails):
```js
$('#full-bg-random').unsplashBg({
  backgroundImage: 'path/image.jpg'
});
```

## Testing
This will build scripts, run tests and generate a code coverage report. Anything less than 100% coverage will throw an error.
```javascript
npm test
```

## Contributing
* ⇄ Pull requests and ★ Stars are always welcome.
* For bugs and feature requests, please create an issue.
* Pull requests must be accompanied by passing automated tests (`npm test`).

[MIT License]: https://github.com/jaarreola/jquery-unsplash-bg/blob/master/LICENSE
