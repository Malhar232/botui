![logo](logo.svg)

[![Join the community on Spectrum](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/botui) [![npm](https://img.shields.io/npm/v/botui.svg?style=flat-square)](https://www.npmjs.com/package/botui) [![npm](https://img.shields.io/npm/dm/botui.svg?style=flat-square)](https://www.npmjs.com/package/botui) [![newsletter](newsletter.svg)](https://tinyletter.com/moinhq)

> A JavaScript framework to create conversational UIs.


[Main Site](https://botui.org) - [Read Docs](https://docs.botui.org) - [Examples](https://github.com/moinism/botui-examples)

## Showcase 🎇✨

We are listing all the cool projects that people are building with BotUI, [here](https://github.com/botui/botui/blob/master/Showcase.md). See others' and add yours!

### Quick look

![preview](preview.png)

```html
<div class="botui-app-container" id="botui-app">
  <bot-ui></bot-ui>
</div>
```

```javascript
var botui = new BotUI('botui-app') // id of container

botui.message.bot({ // show first message
  delay: 200,
  content: 'hello'
}).then(() => {
  return botui.message.bot({ // second one
    delay: 1000, // wait 1 sec.
    content: 'how are you?'
  })
}).then(() => {
  return botui.action.button({ // let the user perform an action
    delay: 1000,
    action: [
      {
        text: 'Good',
        value: 'good'
      },
      {
        text: 'Really Good',
        value: 'really_good'
      }
    ]
  })
}).then(res => {
  return botui.message.bot({
    delay: 1000,
    content: `You are feeling ${res.text}!`
  })
})
```


## Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
<a href="https://github.com/botui/botui/graphs/contributors"><img src="https://opencollective.com/botui/contributors.svg?width=890&button=false" /></a>


### License

[MIT License](https://github.com/moinism/botui/blob/master/LICENSE) - Copyrights (c) 2017-20 - Moin Uddin
