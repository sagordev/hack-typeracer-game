# Hack play.typeracer.com game 🏎️ 😎
### 🎉🎉 Simple script for hack typeracer game. Just for fun! 🎉🎉

## Paste the code in browser console when the countdown will be started.

```js
var INTERVAL_IN_MILLISECOND = 118; //Change as you wish

var inputField = document.querySelector('.txtInput');
var DOMs = [...document.querySelector('.gameView').getElementsByTagName('span')];
DOMs = DOMs.splice(DOMs.length - 3, 3);
var fullSentence = (DOMs.map(DOM => DOM.textContent)).join('');

[...fullSentence].forEach((character, i) => {
	setTimeout(() => {
		inputField.value = inputField.value + character;
		inputField.dispatchEvent(new Event('keydown'));
	}, i * INTERVAL_IN_MILLISECOND);
})
```
