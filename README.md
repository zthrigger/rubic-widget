![alt text](https://github.com/Cryptorubic/rubic-frontend/blob/master/src/assets/images/rubic-logo.svg "Rubic — Multichain DeFi platform")

# Rubic Widget


![alt text](https://github.com/Cryptorubic/rubic-widget/blob/master/src/assets/iframe.png "")


## Get started

1. Put this script tag to the `<head>` of your page 
```html
<script type="text/javascript" src="https://widgets.rubic.exchange/iframe/bundle.min.js"></script>
```

2. Put this `div` tag to the place, where the Rubic Widget will be
```html
<div id="rubic-widget-root"></div>
```

3. Put this script tag to the bottom of `<body>`
```html
<script defer type="text/javascript">
    const configuration = {
        from: 'ETH',
        to: 'RBC',
        fromChain: 'ETH',
        toChain: 'ETH',
        amount: 1,
        iframe: 'flex',
        hideSelectionFrom: false,
        hideSelectionTo: true,
        theme: 'dark',
        background: '#28372e'
    }
    rubicWidget.init(configuration);
</script>
```
You can customize the configuration parameters the way you want. Below is a description of the options available.

## Available configuration parameters

| Parameter          | Possible values                                                                                                                                                                                                                                                                                                                                                                                                          | Default                                                                                                                 | Description                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `from`             | Token symbol (e.g. 'ETH', 'RBC') or address (e.g. '0x32Be343B94f860124dC4fEe278FDCBD38C102D88')                                                                                                                                                                                                                                                                                                                          | `ETH`                                                                                                                   | Can be used to specify tokens to trade.                                                                                                                                                                                 |
| `to`               | Token symbol (e.g. 'ETH', 'RBC') or address (e.g. '0x32Be343B94f860124dC4fEe278FDCBD38C102D88')                                                                                                                                                                                                                                                                                                                          | `RBC`                                                                                                                   | Can be used to specify tokens to trade.                                                                                                                                                                                 |
| `fromChain`        | 'ETH', 'BSC', 'POLYGON', 'HARMONY'                                                                                                                                                                                                                                                                                                                                                                                       | `ETH`                                                                                                                   | Can be used to specify chain to trade.                                                                                                                                                                                  |
| `toChain`          | 'ETH', 'BSC', 'POLYGON', 'HARMONY', 'TRON', 'XDAI'                                                                                                                                                                                                                                                                                                                                                                       | `ETH`                                                                                                                   | Can be used to specify chain to trade.                                                                                                                                                                                  |
| `amount`           | Floating point number, e.g. `1.2345`                                                                                                                                                                                                                                                                                                                                                                                     | `1`                                                                                                                     | Can be used to specify base trade amount.                                                                                                                                                                               |
| `iframe`           | 'flex', 'vertical', 'horizontal'                                                                                                                                                                                                                                                                                                                                                                                         | `flex`                                                                                                                  | Can be used to specify widget appearance. flex -- the widget adjusts to the rubic-widget-rootcontainer size: if the width of the container is less than 1180px, then the widget is vertical, otherwise it is horizontal |
| `hideSelectionFrom`| 'true', 'false'                                                                                                                                                                                                                                                                                                                                                                                                          | `false`                                                                                                                 | Allows you to block the selection of tokens on the form. Thus, it will be possible to exchange only the tokens specified in the parameters.                                                                             |
| `hideSelectionTo`  | 'true', 'false'                                                                                                                                                                                                                                                                                                                                                                                                          | `true`                                                                                                                  | Allows you to block the selection of tokens on the form. Thus, it will be possible to exchange only the tokens specified in the parameters.                                                                             |
| `theme`            | 'dark', 'light'                                                                                                                                                                                                                                                                                                                                                                                                          | `dark`                                                                                                                  | Can be used to specify the theme of the visual design.                                                                                                                                                                  |
| `background`       | values of css `background` property, e.g.'#28372e', 'white', 'linear-gradient(45deg, black, #4aa956)'                                                                                                                                                                                                                                                                                                                    | `linear-gradient(45deg, black, #4aa956)` with dark theme, `linear-gradient(45deg, #4aa956 20%, white)` with light theme | Allows you to set the background in widget outside the trade form.                                                                                                                                                      |
| `language`         | 'en', 'es', 'ko', 'ru', 'zh'                                                                                                                                                                                                                                                                                                                                                                                             | `en`                                                                                                                    | Allows you to set widget language.                                                                                                                                                                                      |
| `injectTokens`     | Object whose array properties contain addresses or symbols of tokens that must be added to the list of tokens available for selection (initially, the list contains only a few basic tokens for each blockchain). Available property keys: `eth`, `bsc`, `polygon`, `harmony`  e.g.  ``` {     eth: ['0xd123575d94a7ad9bff3ad037ae9d4d52f41a7518', 'CRV'],     bsc: ['0x2859e4544c4bb03966803b044a93563bd2d0dd4d'] } ``` | `{}`                                                                                                                    | Allows you to add your tokens to the tokens selection list inside widget.                                                                                                                                               |