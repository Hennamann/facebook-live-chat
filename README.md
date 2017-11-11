# facebook-live-chat

A module for grabbing live chat comments from a Facebook livestream.

## Example

```js
const Facebook = require('facebook-live-chat');

const fb = new Facebook('FACEBOOK_USER_ID_HERE', 'USER_ACCESS_TOKEN_HERE');

fb.on('ready', () => {
	console.log('ready!');
	fb.listen(1000);
});

fb.on('chat', json => {
	console.log(json.message);
});

fb.on('error', err => {
	console.log(err);
});
```

## Install

```
$ npm install --save facebook-live-chat
```

## License

[MIT](https://github.com/Hennamann/facebook-live-chat/blob/master/LICENSE.md)

## Author

[Ole Henrik Stabell](https://github.com/hennamann)
