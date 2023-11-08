# toUnicodeVariant

Javascript function to convert a string into different kind of **ⓤⓝⓘⓒⓞⓓⓔ** variants. 

I 💚 Unicode! ```toUnicodeVariant``` is an attempt to utilize unicode in a structured, organized and logical manner. Skip all the confusions and exceptions, you can render unicode just by referring to a pseudo-named subset of "fonts", also called *variants*. 


#### browser
```html
<script src="path/to/toUnicodeVariant.js"></script>
```
#### nodejs
```javascript
const toUnicodeVariant = require('path/to/toUnicodeVariant.js') 
```
#### Usage
```javascript
toUnicodeVariant(string, variant, combinings)
...
toUnicodeVariant('monospace', 'm') //like first row below 
```

|Variant     | Alias | Description                   | Example           |
|:--------- |:-----:|:----------------------------- |:----------------- |
| monospace |   m   | Monospace      | 𝚖𝚘𝚗𝚘𝚜𝚙𝚊𝚌𝚎 |
| bold   |   b   | Bold text                        |𝐛𝐨𝐥𝐝  |
| italic  |  i  | Italic text                       | 𝑖𝑡𝑎𝑙𝑖𝑐  |
| bold italic   |   bi   | bold+italic text   | 𝒃𝒐𝒍𝒅 𝒊𝒕𝒂𝒍𝒊𝒄 |
| script     |   c   | Handwriting style         | 𝓈𝒸𝓇𝒾𝓅𝓉    |
| bold script  |  bc   | Bolder handwriting     | 𝓫𝓸𝓵𝓭 𝓼𝓬𝓻𝓲𝓹𝓽      |
| gothic  |   g   |Gothic (fraktur)            | 𝔤𝔬𝔱𝔥𝔦𝔠      |
| gothic bold  |   bg   | Gothic in bold| 𝖌𝖔𝖙𝖍𝖎𝖈 𝖇𝖔𝖑𝖉        |
| doublestruck |   d   | Outlined text        | 𝕕𝕠𝕦𝕓𝕝𝕖𝕤𝕥𝕣𝕦𝕔𝕜 |
| 𝗌𝖺𝗇𝗌   |  s   | Sans-serif style    | 𝗌𝖺𝗇𝗌 |
| bold 𝗌𝖺𝗇𝗌   |  bs   | Bold sans-serif   | 𝗯𝗼𝗹𝗱 𝘀𝗮𝗻𝘀 |
| italic 𝗌𝖺𝗇𝗌   |  is   | Italic sans-serif  | 𝘪𝘵𝘢𝘭𝘪𝘤 𝘴𝘢𝘯𝘴 |
| bold italic sans  |  bis   | Bold italic sans-serif  | 𝙗𝙤𝙡𝙙 𝙞𝙩𝙖𝙡𝙞𝙘 𝙨𝙖𝙣𝙨 |
| circled  |  o   | Letters within circles   | ⓒⓘⓡⓒⓛⓔⓓ |
| circled negative |  on   | -- negative  | 	🅒🅘🅡🅒🅛🅔🅓 |
| squared  |  q   | Letters within squares   | 🅂🅀🅄🄰🅁🄴🄳 |
| squared negative  |  qn   | -- negative  | 🆂🆀🆄🅰🆁🅴🅳
| paranthesis   |  p   | Letters within paranthesis  | ⒫⒜⒭⒠⒩⒯⒣⒠⒮⒤⒮ |
| fullwidth | w   | Wider monospace font   | ｆｕｌｌｗｉｄｔｈ |
| flags | f | Regional codes | 🇩🇰 🇺 🇳 🇮 🇨 🇴 🇩 🇪 |
| numbers dot | nd  | Numbers with trailing dot   | 🄀⒈⒉⒊⒋⒌⒍⒎⒏⒐ |
| numbers comma | nc   | Numbers with trailing comma   | 🄁🄂🄃🄄🄅🄆🄇🄈🄉🄊|
| number double circled | ndc | Numbers within double circle  | ⓵⓶⓷⓸⓹⓺⓻⓼⓽ |

## underline, strike and other diacritical marks

The unicoded' text can be combined with a broad range of diacritical marks 

```javascript
toUnicodeVariant('gothic', 'g', 'underline') //𝔤̲𝔬̲𝔱̲𝔥̲𝔦̲𝔠̲
```

|Combining | Short | Sample (italic variant) |
|:--------- |:-----:|:----------------------------- |
| strike | s | 𝑎̶𝑏̶𝑐̶𝑑̶𝑒̶𝑓̶𝑔̶
| strike-curly | sc | 𝑎̴𝑏̴𝑐̴𝑑̴𝑒̴𝑓̴𝑔̴
| underline | u | 𝑎̲𝑏̲𝑐̲𝑑̲𝑒̲𝑓̲𝑔̲
| underline-sm | u-sm |	𝑎̠𝑏̠𝑐̠𝑑̠𝑒̠𝑓̠𝑔̠
| underline-curly | uc | 𝑎̰𝑏̰𝑐̰𝑑̰𝑒̰𝑓̰𝑔̰
| underline-double | ud | 𝑎̳𝑏̳𝑐̳𝑑̳𝑒̳𝑓̳𝑔̳
| underline-double-sm | ud-sm | 𝑎͇𝑏͇𝑐͇𝑑͇𝑒͇𝑓͇𝑔͇
| overline | o | 𝑎̅𝑏̅𝑐̅𝑑̅𝑒̅𝑓̅𝑔̅
| overline-curly | oc | 𝑎̃𝑏̃𝑐̃𝑑̃𝑒̃𝑓̃𝑔̃
| overline-sm | o-sm | 𝑎̄𝑏̄𝑐̄𝑑̄𝑒̄𝑓̄𝑔̄
| overline-double | od | 𝑎̿𝑏̿𝑐̿𝑑̿𝑒̿𝑓̿𝑔̿
| slash | sl | 𝑎̸𝑏̸𝑐̸𝑑̸𝑒̸𝑓̸𝑔̸
| plus-below | pb | 	𝑎̟𝑏̟𝑐̟𝑑̟𝑒̟𝑓̟𝑔̟
| cross-above | ca | 𝑎̽𝑏̽𝑐̽𝑑̽𝑒̽𝑓̽𝑔̽
|  𝐍-above |  {a,c,d,e,h,i,m,o,r,u,v,x}-a | 𝑎ͣ 𝑎ͨ 𝑎ͩ 𝑎ͤ 𝑎ͪ 𝑎ͥ 𝑎ͫ 𝑎ͦ 𝑎ͬ 𝑎ͧ 𝑎ͮ 𝑎ͯ 

Combinings can be combined by comma separated string 

```javascript
toUnicodeVariant('The quick brown fox jumps over the lazy dog', 'sans', 'underline, slash') // u, sl
```

 𝖳̸̲𝗁̸̲𝖾̸̲ ̸̲𝗊̸̲𝗎̸̲𝗂̸̲𝖼̸̲𝗄̸̲ ̸̲𝖻̸̲𝗋̸̲𝗈̸̲𝗐̸̲𝗇̸̲ ̸̲𝖿̸̲𝗈̸̲𝗑̸̲ ̸̲𝗃̸̲𝗎̸̲𝗆̸̲𝗉̸̲𝗌̸̲ ̸̲𝗈̸̲𝗏̸̲𝖾̸̲𝗋̸̲ ̸̲𝗍̸̲𝗁̸̲𝖾̸̲ ̸̲𝗅̸̲𝖺̸̲𝗓̸̲𝗒̸̲ ̸̲𝖽̸̲𝗈̸̲𝗀̸̲

<details>
  <summary>🔎 Compatibility table, variants / diacritical marks</summary>
</details>

### Special chars
Language specific special chars like ç, ò or ø are not supported by any unicode "variant", and will almost certainly never be in any future. The *script* and *gothic* fonts are in fact just various kind of mathematical symbols (see references below)  almost certainly not supported by unicode "variants", and will never be in any future. Converting a special char like ```ø``` will at best look odd, probably ruin the entire string (vary on reader / browser). 

But -- by using the base latin character as fallback, and inject a makeover of diacritical marks, we can experimentally try to *mimick* some language specific characters. Adding diacritics fails with the figurative variants, but it works okay with most of the rest. 

<details>
  <summary>Table of supported special chars, from 𝗮̂ to 𝗼̷ </summary>
<table><thead><tr><th>#</th><th>mono space</th><th>bold</th><th>italic</th><th> bold italic</th><th>script</th><th>bold script</th><th>gothic</th><th>gothic bold</th><th>double struck</th><th>sans</th><th>bold sans</th><th>italic sans</th><th>bold italic sans</th></tr></thead><tbody><tr><td align="center">ä</td><td align="center">𝚊̈</td><td align="center">𝐚̈</td><td align="center">𝑎̈</td><td align="center">𝚊̈</td><td align="center">𝒶̈</td><td align="center">𝓪̈</td><td align="center">𝔞̈</td><td align="center">𝖆̈</td><td align="center">𝕒̈</td><td align="center">𝖺̈</td><td align="center">𝗮̈</td><td align="center">𝘢̈</td><td align="center">𝙖̈</td></tr><tr><td align="center">â</td><td align="center">𝚊̂</td><td align="center">𝐚̂</td><td align="center">𝑎̂</td><td align="center">𝚊̂</td><td align="center">𝒶̂</td><td align="center">𝓪̂</td><td align="center">𝔞̂</td><td align="center">𝖆̂</td><td align="center">𝕒̂</td><td align="center">𝖺̂</td><td align="center">𝗮̂</td><td align="center">𝘢̂</td><td align="center">𝙖̂</td></tr><tr><td align="center">á</td><td align="center">𝚊́</td><td align="center">𝐚́</td><td align="center">𝑎́</td><td align="center">𝚊́</td><td align="center">𝒶́</td><td align="center">𝓪́</td><td align="center">𝔞́</td><td align="center">𝖆́</td><td align="center">𝕒́</td><td align="center">𝖺́</td><td align="center">𝗮́</td><td align="center">𝘢́</td><td align="center">𝙖́</td></tr><tr><td align="center">å</td><td align="center">𝚊̊</td><td align="center">𝐚̊</td><td align="center">𝑎̊</td><td align="center">𝚊̊</td><td align="center">𝒶̊</td><td align="center">𝓪̊</td><td align="center">𝔞̊</td><td align="center">𝖆̊</td><td align="center">𝕒̊</td><td align="center">𝖺̊</td><td align="center">𝗮̊</td><td align="center">𝘢̊</td><td align="center">𝙖̊</td></tr><tr><td align="center">ă</td><td align="center">𝚊̆</td><td align="center">𝐚̆</td><td align="center">𝑎̆</td><td align="center">𝚊̆</td><td align="center">𝒶̆</td><td align="center">𝓪̆</td><td align="center">𝔞̆</td><td align="center">𝖆̆</td><td align="center">𝕒̆</td><td align="center">𝖺̆</td><td align="center">𝗮̆</td><td align="center">𝘢̆</td><td align="center">𝙖̆</td></tr><tr><td align="center">ǟ</td><td align="center">𝚊̈̄</td><td align="center">𝐚̈̄</td><td align="center">𝑎̈̄</td><td align="center">𝚊̈̄</td><td align="center">𝒶̈̄</td><td align="center">𝓪̈̄</td><td align="center">𝔞̈̄</td><td align="center">𝖆̈̄</td><td align="center">𝕒̈̄</td><td align="center">𝖺̈̄</td><td align="center">𝗮̈̄</td><td align="center">𝘢̈̄</td><td align="center">𝙖̈̄</td></tr><tr><td align="center">ã</td><td align="center">𝚊̃</td><td align="center">𝐚̃</td><td align="center">𝑎̃</td><td align="center">𝚊̃</td><td align="center">𝒶̃</td><td align="center">𝓪̃</td><td align="center">𝔞̃</td><td align="center">𝖆̃</td><td align="center">𝕒̃</td><td align="center">𝖺̃</td><td align="center">𝗮̃</td><td align="center">𝘢̃</td><td align="center">𝙖̃</td></tr><tr><td align="center">ā</td><td align="center">𝚊̄</td><td align="center">𝐚̄</td><td align="center">𝑎̄</td><td align="center">𝚊̄</td><td align="center">𝒶̄</td><td align="center">𝓪̄</td><td align="center">𝔞̄</td><td align="center">𝖆̄</td><td align="center">𝕒̄</td><td align="center">𝖺̄</td><td align="center">𝗮̄</td><td align="center">𝘢̄</td><td align="center">𝙖̄</td></tr><tr><td align="center">ȧ</td><td align="center">𝚊̇</td><td align="center">𝐚̇</td><td align="center">𝑎̇</td><td align="center">𝚊̇</td><td align="center">𝒶̇</td><td align="center">𝓪̇</td><td align="center">𝔞̇</td><td align="center">𝖆̇</td><td align="center">𝕒̇</td><td align="center">𝖺̇</td><td align="center">𝗮̇</td><td align="center">𝘢̇</td><td align="center">𝙖̇</td></tr><tr><td align="center">ȃ</td><td align="center">𝚊̑</td><td align="center">𝐚̑</td><td align="center">𝑎̑</td><td align="center">𝚊̑</td><td align="center">𝒶̑</td><td align="center">𝓪̑</td><td align="center">𝔞̑</td><td align="center">𝖆̑</td><td align="center">𝕒̑</td><td align="center">𝖺̑</td><td align="center">𝗮̑</td><td align="center">𝘢̑</td><td align="center">𝙖̑</td></tr><tr><td align="center">ḅ</td><td align="center">𝚋̣</td><td align="center">𝐛̣</td><td align="center">𝑏̣</td><td align="center">𝚋̣</td><td align="center">𝒷̣</td><td align="center">𝓫̣</td><td align="center">𝔟̣</td><td align="center">𝖇̣</td><td align="center">𝕓̣</td><td align="center">𝖻̣</td><td align="center">𝗯̣</td><td align="center">𝘣̣</td><td align="center">𝙗̣</td></tr><tr><td align="center">č</td><td align="center">𝚌̌</td><td align="center">𝐜̌</td><td align="center">𝑐̌</td><td align="center">𝚌̌</td><td align="center">𝒸̌</td><td align="center">𝓬̌</td><td align="center">𝔠̌</td><td align="center">𝖈̌</td><td align="center">𝕔̌</td><td align="center">𝖼̌</td><td align="center">𝗰̌</td><td align="center">𝘤̌</td><td align="center">𝙘̌</td></tr><tr><td align="center">ć</td><td align="center">𝚌́</td><td align="center">𝐜́</td><td align="center">𝑐́</td><td align="center">𝚌́</td><td align="center">𝒸́</td><td align="center">𝓬́</td><td align="center">𝔠́</td><td align="center">𝖈́</td><td align="center">𝕔́</td><td align="center">𝖼́</td><td align="center">𝗰́</td><td align="center">𝘤́</td><td align="center">𝙘́</td></tr><tr><td align="center">ċ</td><td align="center">𝚌̇</td><td align="center">𝐜̇</td><td align="center">𝑐̇</td><td align="center">𝚌̇</td><td align="center">𝒸̇</td><td align="center">𝓬̇</td><td align="center">𝔠̇</td><td align="center">𝖈̇</td><td align="center">𝕔̇</td><td align="center">𝖼̇</td><td align="center">𝗰̇</td><td align="center">𝘤̇</td><td align="center">𝙘̇</td></tr><tr><td align="center">ḉ</td><td align="center">𝚌̧́</td><td align="center">𝐜̧́</td><td align="center">𝑐̧́</td><td align="center">𝚌̧́</td><td align="center">𝒸̧́</td><td align="center">𝓬̧́</td><td align="center">𝔠̧́</td><td align="center">𝖈̧́</td><td align="center">𝕔̧́</td><td align="center">𝖼̧́</td><td align="center">𝗰̧́</td><td align="center">𝘤̧́</td><td align="center">𝙘̧́</td></tr><tr><td align="center">ç</td><td align="center">𝚌̧</td><td align="center">𝐜̧</td><td align="center">𝑐̧</td><td align="center">𝚌̧</td><td align="center">𝒸̧</td><td align="center">𝓬̧</td><td align="center">𝔠̧</td><td align="center">𝖈̧</td><td align="center">𝕔̧</td><td align="center">𝖼̧</td><td align="center">𝗰̧</td><td align="center">𝘤̧</td><td align="center">𝙘̧</td></tr><tr><td align="center">ċ</td><td align="center">𝚌̇</td><td align="center">𝐜̇</td><td align="center">𝑐̇</td><td align="center">𝚌̇</td><td align="center">𝒸̇</td><td align="center">𝓬̇</td><td align="center">𝔠̇</td><td align="center">𝖈̇</td><td align="center">𝕔̇</td><td align="center">𝖼̇</td><td align="center">𝗰̇</td><td align="center">𝘤̇</td><td align="center">𝙘̇</td></tr><tr><td align="center">ĉ</td><td align="center">𝚌̂</td><td align="center">𝐜̂</td><td align="center">𝑐̂</td><td align="center">𝚌̂</td><td align="center">𝒸̂</td><td align="center">𝓬̂</td><td align="center">𝔠̂</td><td align="center">𝖈̂</td><td align="center">𝕔̂</td><td align="center">𝖼̂</td><td align="center">𝗰̂</td><td align="center">𝘤̂</td><td align="center">𝙘̂</td></tr><tr><td align="center">è</td><td align="center">𝚎̀</td><td align="center">𝐞̀</td><td align="center">𝑒̀</td><td align="center">𝚎̀</td><td align="center">𝓮̀</td><td align="center">𝓮̀</td><td align="center">𝔢̀</td><td align="center">𝖊̀</td><td align="center">𝕖̀</td><td align="center">𝖾̀</td><td align="center">𝗲̀</td><td align="center">𝘦̀</td><td align="center">𝙚̀</td></tr><tr><td align="center">é</td><td align="center">𝚎́</td><td align="center">𝐞́</td><td align="center">𝑒́</td><td align="center">𝚎́</td><td align="center">𝓮́</td><td align="center">𝓮́</td><td align="center">𝔢́</td><td align="center">𝖊́</td><td align="center">𝕖́</td><td align="center">𝖾́</td><td align="center">𝗲́</td><td align="center">𝘦́</td><td align="center">𝙚́</td></tr><tr><td align="center">ē</td><td align="center">𝚎̄</td><td align="center">𝐞̄</td><td align="center">𝑒̄</td><td align="center">𝚎̄</td><td align="center">𝓮̄</td><td align="center">𝓮̄</td><td align="center">𝔢̄</td><td align="center">𝖊̄</td><td align="center">𝕖̄</td><td align="center">𝖾̄</td><td align="center">𝗲̄</td><td align="center">𝘦̄</td><td align="center">𝙚̄</td></tr><tr><td align="center">ĕ</td><td align="center">𝚎̆</td><td align="center">𝐞̆</td><td align="center">𝑒̆</td><td align="center">𝚎̆</td><td align="center">𝓮̆</td><td align="center">𝓮̆</td><td align="center">𝔢̆</td><td align="center">𝖊̆</td><td align="center">𝕖̆</td><td align="center">𝖾̆</td><td align="center">𝗲̆</td><td align="center">𝘦̆</td><td align="center">𝙚̆</td></tr><tr><td align="center">ë</td><td align="center">𝚎̈</td><td align="center">𝐞̈</td><td align="center">𝑒̈</td><td align="center">𝚎̈</td><td align="center">𝓮̈</td><td align="center">𝓮̈</td><td align="center">𝔢̈</td><td align="center">𝖊̈</td><td align="center">𝕖̈</td><td align="center">𝖾̈</td><td align="center">𝗲̈</td><td align="center">𝘦̈</td><td align="center">𝙚̈</td></tr><tr><td align="center">ě</td><td align="center">𝚎̌</td><td align="center">𝐞̌</td><td align="center">𝑒̌</td><td align="center">𝚎̌</td><td align="center">𝓮̌</td><td align="center">𝓮̌</td><td align="center">𝔢̌</td><td align="center">𝖊̌</td><td align="center">𝕖̌</td><td align="center">𝖾̌</td><td align="center">𝗲̌</td><td align="center">𝘦̌</td><td align="center">𝙚̌</td></tr><tr><td align="center">ê</td><td align="center">𝚎̂</td><td align="center">𝐞̂</td><td align="center">𝑒̂</td><td align="center">𝚎̂</td><td align="center">𝓮̂</td><td align="center">𝓮̂</td><td align="center">𝔢̂</td><td align="center">𝖊̂</td><td align="center">𝕖̂</td><td align="center">𝖾̂</td><td align="center">𝗲̂</td><td align="center">𝘦̂</td><td align="center">𝙚̂</td></tr><tr><td align="center">ę</td><td align="center">𝚎̨</td><td align="center">𝐞̨</td><td align="center">𝑒̨</td><td align="center">𝚎̨</td><td align="center">𝓮̨</td><td align="center">𝓮̨</td><td align="center">𝔢̨</td><td align="center">𝖊̨</td><td align="center">𝕖̨</td><td align="center">𝖾̨</td><td align="center">𝗲̨</td><td align="center">𝘦̨</td><td align="center">𝙚̨</td></tr><tr><td align="center">ȇ</td><td align="center">𝚎̑</td><td align="center">𝐞̑</td><td align="center">𝑒̑</td><td align="center">𝚎̑</td><td align="center">𝓮̑</td><td align="center">𝓮̑</td><td align="center">𝔢̑</td><td align="center">𝖊̑</td><td align="center">𝕖̑</td><td align="center">𝖾̑</td><td align="center">𝗲̑</td><td align="center">𝘦̑</td><td align="center">𝙚̑</td></tr><tr><td align="center">ȅ</td><td align="center">𝚎̏</td><td align="center">𝐞̏</td><td align="center">𝑒̏</td><td align="center">𝚎̏</td><td align="center">𝓮̏</td><td align="center">𝓮̏</td><td align="center">𝔢̏</td><td align="center">𝖊̏</td><td align="center">𝕖̏</td><td align="center">𝖾̏</td><td align="center">𝗲̏</td><td align="center">𝘦̏</td><td align="center">𝙚̏</td></tr><tr><td align="center">ğ</td><td align="center">𝚐̆</td><td align="center">𝐠̆</td><td align="center">𝑔̆</td><td align="center">𝚐̆</td><td align="center">𝓰̆</td><td align="center">𝓰̆</td><td align="center">𝔤̆</td><td align="center">𝖌̆</td><td align="center">𝕘̆</td><td align="center">𝗀̆</td><td align="center">𝗴̆</td><td align="center">𝘨̆</td><td align="center">𝙜̆</td></tr><tr><td align="center">ǧ</td><td align="center">𝚐̌</td><td align="center">𝐠̌</td><td align="center">𝑔̌</td><td align="center">𝚐̌</td><td align="center">𝓰̌</td><td align="center">𝓰̌</td><td align="center">𝔤̌</td><td align="center">𝖌̌</td><td align="center">𝕘̌</td><td align="center">𝗀̌</td><td align="center">𝗴̌</td><td align="center">𝘨̌</td><td align="center">𝙜̌</td></tr><tr><td align="center">ģ</td><td align="center">𝚐̧</td><td align="center">𝐠̧</td><td align="center">𝑔̧</td><td align="center">𝚐̧</td><td align="center">𝓰̧</td><td align="center">𝓰̧</td><td align="center">𝔤̧</td><td align="center">𝖌̧</td><td align="center">𝕘̧</td><td align="center">𝗀̧</td><td align="center">𝗴̧</td><td align="center">𝘨̧</td><td align="center">𝙜̧</td></tr><tr><td align="center">ġ</td><td align="center">𝚐̇</td><td align="center">𝐠̇</td><td align="center">𝑔̇</td><td align="center">𝚐̇</td><td align="center">𝓰̇</td><td align="center">𝓰̇</td><td align="center">𝔤̇</td><td align="center">𝖌̇</td><td align="center">𝕘̇</td><td align="center">𝗀̇</td><td align="center">𝗴̇</td><td align="center">𝘨̇</td><td align="center">𝙜̇</td></tr><tr><td align="center">ḥ</td><td align="center">𝚑̣</td><td align="center">𝐡̣</td><td align="center">ℎ̣</td><td align="center">𝚑̣</td><td align="center">𝒽̣</td><td align="center">𝓱̣</td><td align="center">𝔥̣</td><td align="center">𝖍̣</td><td align="center">𝕙̣</td><td align="center">𝗁̣</td><td align="center">𝗵̣</td><td align="center">𝘩̣</td><td align="center">𝙝̣</td></tr><tr><td align="center">ĩ</td><td align="center">𝚒̃</td><td align="center">𝐢̃</td><td align="center">𝑖̃</td><td align="center">𝚒̃</td><td align="center">𝒾̃</td><td align="center">𝓲̃</td><td align="center">𝔦̃</td><td align="center">𝖎̃</td><td align="center">𝕚̃</td><td align="center">𝗂̃</td><td align="center">𝗶̃</td><td align="center">𝘪̃</td><td align="center">𝙞̃</td></tr><tr><td align="center">î</td><td align="center">𝚒̂</td><td align="center">𝐢̂</td><td align="center">𝑖̂</td><td align="center">𝚒̂</td><td align="center">𝒾̂</td><td align="center">𝓲̂</td><td align="center">𝔦̂</td><td align="center">𝖎̂</td><td align="center">𝕚̂</td><td align="center">𝗂̂</td><td align="center">𝗶̂</td><td align="center">𝘪̂</td><td align="center">𝙞̂</td></tr><tr><td align="center">í</td><td align="center">𝚒́</td><td align="center">𝐢́</td><td align="center">𝑖́</td><td align="center">𝚒́</td><td align="center">𝒾́</td><td align="center">𝓲́</td><td align="center">𝔦́</td><td align="center">𝖎́</td><td align="center">𝕚́</td><td align="center">𝗂́</td><td align="center">𝗶́</td><td align="center">𝘪́</td><td align="center">𝙞́</td></tr><tr><td align="center">ì</td><td align="center">𝚒̀</td><td align="center">𝐢̀</td><td align="center">𝑖̀</td><td align="center">𝚒̀</td><td align="center">𝒾̀</td><td align="center">𝓲̀</td><td align="center">𝔦̀</td><td align="center">𝖎̀</td><td align="center">𝕚̀</td><td align="center">𝗂̀</td><td align="center">𝗶̀</td><td align="center">𝘪̀</td><td align="center">𝙞̀</td></tr><tr><td align="center">ḱ</td><td align="center">𝚔́</td><td align="center">𝐤́</td><td align="center">𝑘́</td><td align="center">𝚔́</td><td align="center">𝓀́</td><td align="center">𝓴́</td><td align="center">𝔨́</td><td align="center">𝖐́</td><td align="center">𝕜́</td><td align="center">𝗄́</td><td align="center">𝗸́</td><td align="center">𝘬́</td><td align="center">𝙠́</td></tr><tr><td align="center">ḳ</td><td align="center">𝚔̣</td><td align="center">𝐤̣</td><td align="center">𝑘̣</td><td align="center">𝚔̣</td><td align="center">𝓀̣</td><td align="center">𝓴̣</td><td align="center">𝔨̣</td><td align="center">𝖐̣</td><td align="center">𝕜̣</td><td align="center">𝗄̣</td><td align="center">𝗸̣</td><td align="center">𝘬̣</td><td align="center">𝙠̣</td></tr><tr><td align="center">ņ</td><td align="center">𝚗̨</td><td align="center">𝐧̨</td><td align="center">𝑛̨</td><td align="center">𝚗̨</td><td align="center">𝓃̨</td><td align="center">𝓷̨</td><td align="center">𝔫̨</td><td align="center">𝖓̨</td><td align="center">𝕟̨</td><td align="center">𝗇̨</td><td align="center">𝗻̨</td><td align="center">𝘯̨</td><td align="center">𝙣̨</td></tr><tr><td align="center">ń</td><td align="center">𝚗́</td><td align="center">𝐧́</td><td align="center">𝑛́</td><td align="center">𝚗́</td><td align="center">𝓃́</td><td align="center">𝓷́</td><td align="center">𝔫́</td><td align="center">𝖓́</td><td align="center">𝕟́</td><td align="center">𝗇́</td><td align="center">𝗻́</td><td align="center">𝘯́</td><td align="center">𝙣́</td></tr><tr><td align="center">ñ</td><td align="center">𝚗</td><td align="center">𝐧</td><td align="center">𝑛</td><td align="center">𝚗</td><td align="center">𝓃</td><td align="center">𝓷</td><td align="center">𝔫</td><td align="center">𝖓</td><td align="center">𝕟</td><td align="center">𝗇</td><td align="center">𝗻</td><td align="center">𝘯</td><td align="center">𝙣</td></tr><tr><td align="center">õ</td><td align="center">𝚘̃</td><td align="center">𝐨̃</td><td align="center">𝑜̃</td><td align="center">𝚘̃</td><td align="center">𝓸̃</td><td align="center">𝓸̃</td><td align="center">𝔬̃</td><td align="center">𝖔̃</td><td align="center">𝕠̃</td><td align="center">𝗈̃</td><td align="center">𝗼̃</td><td align="center">𝘰̃</td><td align="center">𝙤̃</td></tr><tr><td align="center">ö</td><td align="center">𝚘̈</td><td align="center">𝐨̈</td><td align="center">𝑜̈</td><td align="center">𝚘̈</td><td align="center">𝓸̈</td><td align="center">𝓸̈</td><td align="center">𝔬̈</td><td align="center">𝖔̈</td><td align="center">𝕠̈</td><td align="center">𝗈̈</td><td align="center">𝗼̈</td><td align="center">𝘰̈</td><td align="center">𝙤̈</td></tr><tr><td align="center">ō</td><td align="center">𝚘̄</td><td align="center">𝐨̄</td><td align="center">𝑜̄</td><td align="center">𝚘̄</td><td align="center">𝓸̄</td><td align="center">𝓸̄</td><td align="center">𝔬̄</td><td align="center">𝖔̄</td><td align="center">𝕠̄</td><td align="center">𝗈̄</td><td align="center">𝗼̄</td><td align="center">𝘰̄</td><td align="center">𝙤̄</td></tr><tr><td align="center">ô</td><td align="center">𝚘̂</td><td align="center">𝐨̂</td><td align="center">𝑜̂</td><td align="center">𝚘̂</td><td align="center">𝓸̂</td><td align="center">𝓸̂</td><td align="center">𝔬̂</td><td align="center">𝖔̂</td><td align="center">𝕠̂</td><td align="center">𝗈̂</td><td align="center">𝗼̂</td><td align="center">𝘰̂</td><td align="center">𝙤̂</td></tr><tr><td align="center">ó</td><td align="center">𝚘́</td><td align="center">𝐨́</td><td align="center">𝑜́</td><td align="center">𝚘́</td><td align="center">𝓸́</td><td align="center">𝓸́</td><td align="center">𝔬́</td><td align="center">𝖔́</td><td align="center">𝕠́</td><td align="center">𝗈́</td><td align="center">𝗼́</td><td align="center">𝘰́</td><td align="center">𝙤́</td></tr><tr><td align="center">ò</td><td align="center">𝚘̀</td><td align="center">𝐨̀</td><td align="center">𝑜̀</td><td align="center">𝚘̀</td><td align="center">𝓸̀</td><td align="center">𝓸̀</td><td align="center">𝔬̀</td><td align="center">𝖔̀</td><td align="center">𝕠̀</td><td align="center">𝗈̀</td><td align="center">𝗼̀</td><td align="center">𝘰̀</td><td align="center">𝙤̀</td></tr><tr><td align="center">ŕ</td><td align="center">𝚛́</td><td align="center">𝐫́</td><td align="center">𝑟́</td><td align="center">𝚛́</td><td align="center">𝓇́</td><td align="center">𝓻́</td><td align="center">𝔯́</td><td align="center">𝖗́</td><td align="center">𝕣́</td><td align="center">𝗋́</td><td align="center">𝗿́</td><td align="center">𝘳́</td><td align="center">𝙧́</td></tr><tr><td align="center">ş</td><td align="center">𝚜̧</td><td align="center">𝐬̧</td><td align="center">𝑠̧</td><td align="center">𝚜̧</td><td align="center">𝓈̧</td><td align="center">𝓼̧</td><td align="center">𝔰̧</td><td align="center">𝖘̧</td><td align="center">𝕤̧</td><td align="center">𝗌̧</td><td align="center">𝘀̧</td><td align="center">𝘴̧</td><td align="center">𝙨̧</td></tr><tr><td align="center">ș</td><td align="center">𝚜̦</td><td align="center">𝐬̦</td><td align="center">𝑠̦</td><td align="center">𝚜̦</td><td align="center">𝓈̦</td><td align="center">𝓼̦</td><td align="center">𝔰̦</td><td align="center">𝖘̦</td><td align="center">𝕤̦</td><td align="center">𝗌̦</td><td align="center">𝘀̦</td><td align="center">𝘴̦</td><td align="center">𝙨̦</td></tr><tr><td align="center">ṩ</td><td align="center">𝚜̣̇</td><td align="center">𝐬̣̇</td><td align="center">𝑠̣̇</td><td align="center">𝚜̣̇</td><td align="center">𝓈̣̇</td><td align="center">𝓼̣̇</td><td align="center">𝔰̣̇</td><td align="center">𝖘̣̇</td><td align="center">𝕤̣̇</td><td align="center">𝗌̣̇</td><td align="center">𝘀̣̇</td><td align="center">𝘴̣̇</td><td align="center">𝙨̣̇</td></tr><tr><td align="center">š</td><td align="center">𝚜̌</td><td align="center">𝐬̌</td><td align="center">𝑠̌</td><td align="center">𝚜̌</td><td align="center">𝓈̌</td><td align="center">𝓼̌</td><td align="center">𝔰̌</td><td align="center">𝖘̌</td><td align="center">𝕤̌</td><td align="center">𝗌̌</td><td align="center">𝘀̌</td><td align="center">𝘴̌</td><td align="center">𝙨̌</td></tr><tr><td align="center">ś</td><td align="center">𝚜́</td><td align="center">𝐬́</td><td align="center">𝑠́</td><td align="center">𝚜́</td><td align="center">𝓈́</td><td align="center">𝓼́</td><td align="center">𝔰́</td><td align="center">𝖘́</td><td align="center">𝕤́</td><td align="center">𝗌́</td><td align="center">𝘀́</td><td align="center">𝘴́</td><td align="center">𝙨́</td></tr><tr><td align="center">ü</td><td align="center">𝚞̈</td><td align="center">𝐮̈</td><td align="center">𝑢̈</td><td align="center">𝚞̈</td><td align="center">𝓊̈</td><td align="center">𝓾̈</td><td align="center">𝔲̈</td><td align="center">𝖚̈</td><td align="center">𝕦̈</td><td align="center">𝗎̈</td><td align="center">𝘂̈</td><td align="center">𝘶̈</td><td align="center">𝙪̈</td></tr><tr><td align="center">ù</td><td align="center">𝚞̀</td><td align="center">𝐮̀</td><td align="center">𝑢̀</td><td align="center">𝚞̀</td><td align="center">𝓊̀</td><td align="center">𝓾̀</td><td align="center">𝔲̀</td><td align="center">𝖚̀</td><td align="center">𝕦̀</td><td align="center">𝗎̀</td><td align="center">𝘂̀</td><td align="center">𝘶̀</td><td align="center">𝙪̀</td></tr><tr><td align="center">ú</td><td align="center">𝚞́</td><td align="center">𝐮́</td><td align="center">𝑢́</td><td align="center">𝚞́</td><td align="center">𝓊́</td><td align="center">𝓾́</td><td align="center">𝔲́</td><td align="center">𝖚́</td><td align="center">𝕦́</td><td align="center">𝗎́</td><td align="center">𝘂́</td><td align="center">𝘶́</td><td align="center">𝙪́</td></tr><tr><td align="center">û</td><td align="center">𝚞̂</td><td align="center">𝐮̂</td><td align="center">𝑢̂</td><td align="center">𝚞̂</td><td align="center">𝓊̂</td><td align="center">𝓾̂</td><td align="center">𝔲̂</td><td align="center">𝖚̂</td><td align="center">𝕦̂</td><td align="center">𝗎̂</td><td align="center">𝘂̂</td><td align="center">𝘶̂</td><td align="center">𝙪̂</td></tr><tr><td align="center">ŭ</td><td align="center">𝚞̆</td><td align="center">𝐮̆</td><td align="center">𝑢̆</td><td align="center">𝚞̆</td><td align="center">𝓊̆</td><td align="center">𝓾̆</td><td align="center">𝔲̆</td><td align="center">𝖚̆</td><td align="center">𝕦̆</td><td align="center">𝗎̆</td><td align="center">𝘂̆</td><td align="center">𝘶̆</td><td align="center">𝙪̆</td></tr><tr><td align="center">ȕ</td><td align="center">𝚞̏</td><td align="center">𝐮̏</td><td align="center">𝑢̏</td><td align="center">𝚞̏</td><td align="center">𝓊̏</td><td align="center">𝓾̏</td><td align="center">𝔲̏</td><td align="center">𝖚̏</td><td align="center">𝕦̏</td><td align="center">𝗎̏</td><td align="center">𝘂̏</td><td align="center">𝘶̏</td><td align="center">𝙪̏</td></tr><tr><td align="center">ȗ</td><td align="center">𝚞̑</td><td align="center">𝐮̑</td><td align="center">𝑢̑</td><td align="center">𝚞̑</td><td align="center">𝓊̑</td><td align="center">𝓾̑</td><td align="center">𝔲̑</td><td align="center">𝖚̑</td><td align="center">𝕦̑</td><td align="center">𝗎̑</td><td align="center">𝘂̑</td><td align="center">𝘶̑</td><td align="center">𝙪̑</td></tr><tr><td align="center">ů</td><td align="center">𝚞̊</td><td align="center">𝐮̊</td><td align="center">𝑢̊</td><td align="center">𝚞̊</td><td align="center">𝓊̊</td><td align="center">𝓾̊</td><td align="center">𝔲̊</td><td align="center">𝖚̊</td><td align="center">𝕦̊</td><td align="center">𝗎̊</td><td align="center">𝘂̊</td><td align="center">𝘶̊</td><td align="center">𝙪̊</td></tr><tr><td align="center">ū</td><td align="center">𝚞̄</td><td align="center">𝐮̄</td><td align="center">𝑢̄</td><td align="center">𝚞̄</td><td align="center">𝓊̄</td><td align="center">𝓾̄</td><td align="center">𝔲̄</td><td align="center">𝖚̄</td><td align="center">𝕦̄</td><td align="center">𝗎̄</td><td align="center">𝘂̄</td><td align="center">𝘶̄</td><td align="center">𝙪̄</td></tr><tr><td align="center">ẁ</td><td align="center">𝚠̀</td><td align="center">𝐰̀</td><td align="center">𝑤̀</td><td align="center">𝚠̀</td><td align="center">𝓌̀</td><td align="center">𝔀̀</td><td align="center">𝔴̀</td><td align="center">𝖜̀</td><td align="center">𝕨̀</td><td align="center">𝗐̀</td><td align="center">𝘄̀</td><td align="center">𝘸̀</td><td align="center">𝙬̀</td></tr><tr><td align="center">ẃ</td><td align="center">𝚠́</td><td align="center">𝐰́</td><td align="center">𝑤́</td><td align="center">𝚠́</td><td align="center">𝓌́</td><td align="center">𝔀́</td><td align="center">𝔴́</td><td align="center">𝖜́</td><td align="center">𝕨́</td><td align="center">𝗐́</td><td align="center">𝘄́</td><td align="center">𝘸́</td><td align="center">𝙬́</td></tr><tr><td align="center">ø</td><td align="center">𝚘̷</td><td align="center">𝐨̷</td><td align="center">𝑜̷</td><td align="center">𝚘̷</td><td align="center">𝓸̷</td><td align="center">𝓸̷</td><td align="center">𝔬̷</td><td align="center">𝖔̷</td><td align="center">𝕠̷</td><td align="center">𝗈̷</td><td align="center">𝗼̷</td><td align="center">𝘰̷</td><td align="center">𝙤̷</td></tr></tbody></table>
</details>

<br>
All capital letters are turned into their latin root. Diacritical marks looks silly on most of them. Only in rare cases mimicking a capital letter ends up in a readable entity.

```javascript
toUnicodeVariant('üničode', 'bold italic') //𝒖̈𝒏𝒊𝒄̌𝒐𝒅𝒆
toUnicodeVariant('ÜNIĈODE', 'bold italic') //𝑼𝑵𝑰𝑪𝑶𝑫𝑬
```
## Compatibility tables
<details>
  <summary>Support of numbers, special chars, small letters and diacritics in general</summary>
<table><thead><tr><th></th><th>Numbers</th><th>Small letters</th><th>Special chars</th><th>Diacritics</th></tr></thead><tbody><tr><td>monospace</td><td align="center">𝟶</td><td align="center">𝚊</td><td align="center">𝚌̧</td><td align="center">𝚌̶̧</td></tr><tr><td>bold</td><td align="center">𝟎</td><td align="center">𝐚</td><td align="center">𝐜̧</td><td align="center">𝐜̶̧</td></tr><tr><td>italic</td><td align="center">-</td><td align="center">𝑎</td><td align="center">𝑐̧</td><td align="center">𝑐̶̧</td></tr><tr><td>bold italic</td><td align="center">-</td><td align="center">𝒂</td><td align="center">𝒄̧</td><td align="center">𝒄̶̧</td></tr><tr><td>script</td><td align="center">-</td><td align="center">𝒶</td><td align="center">𝒸̧</td><td align="center">𝒸̶̧</td></tr><tr><td>bold script</td><td align="center">-</td><td align="center">𝓪</td><td align="center">𝓬̧</td><td align="center">𝓬̶̧</td></tr><tr><td>gothic</td><td align="center">-</td><td align="center">𝔞</td><td align="center">𝔠̧</td><td align="center">𝔠̶̧</td></tr><tr><td>gothic bold</td><td align="center">-</td><td align="center">𝖆</td><td align="center">𝖈̧</td><td align="center">𝖈̶̧</td></tr><tr><td>doublestruck</td><td align="center">𝟘</td><td align="center">𝕒</td><td align="center">𝕔̧</td><td align="center">𝕔̶̧</td></tr><tr><td>sans</td><td align="center">𝟢</td><td align="center">𝖺</td><td align="center">𝖼̧</td><td align="center">𝖼̶̧</td></tr><tr><td>bold sans</td><td align="center">𝟬</td><td align="center">𝗮</td><td align="center">𝗰̧</td><td align="center">𝗰̶̧</td></tr><tr><td>italic sans</td><td align="center">-</td><td align="center">𝘢</td><td align="center">𝘤̧</td><td align="center">𝘤̶̧</td></tr><tr><td>bold italic sans</td><td align="center">-</td><td align="center">𝙖</td><td align="center">𝙘̧</td><td align="center">𝙘̶̧</td></tr><tr><td>parenthesis</td><td align="center">𝟶</td><td align="center">⒜</td><td align="center">-</td><td align="center">-</td></tr><tr><td>squared</td><td align="center">-</td><td align="center"> - </td><td align="center">-</td><td align="center">-</td></tr><tr><td>squared negative</td><td align="center">-</td><td align="center"> - </td><td align="center">-</td><td align="center">-</td></tr><tr><td>circled</td><td align="center">⓪</td><td align="center">ⓐ</td><td align="center">-</td><td align="center">-</td></tr><tr><td>circled negative</td><td align="center">⓿</td><td align="center"> - </td><td align="center">-</td><td align="center">-</td></tr><tr><td>fullwidth</td><td align="center">０</td><td align="center">ａ</td><td align="center">-</td><td align="center">-</td></tr><tr><td>flags</td><td align="center">𝟶</td><td align="center"> - </td><td align="center">-</td><td align="center">-</td></tr><tr><td>numbers dot</td><td align="center">🄀</td><td align="center"> - </td><td align="center">-</td><td align="center">-</td></tr><tr><td>numbers comma</td><td align="center">🄁</td><td align="center"> - </td><td align="center">-</td><td align="center">-</td></tr><tr><td>numbers double circled</td><td align="center">𝟶</td><td align="center"> - </td><td align="center">-</td><td align="center">-</td></tr></tbody></table>
</details>

<details>
  <summary>Variant support of diacritical marks</summary>
</details>

### Limits

* None of the *italic* or *gothic* -style variants supports numbers, 0-9
* None of the figurative variants - *squared*, *circled*, *fullwidth* etc - supports complex diacritics
* However, *fullwidth* supports the entire ASCII-table; besides that, all variants are limited to the az-AZ scope


### *flags* variant, f

```flags``` or ```f``` are a special variant that need to be treated differently. It is based on the unicode *regional indicator symbol*, see https://www.unicode.org/charts/PDF/U1F100.pdf. Using that you'll need to pass a string with whitespace between each character :

```javascript
toUnicodeVariant('U N I C O D E', 'f') //🇺 🇳 🇮 🇨 🇴 🇩 🇪
```
However, if you pass a string that contain a country code, or even the name of some international organization, many readers will render the corresponding flag instead :
```javascript
toUnicodeVariant('DK EU UN', 'flags') //🇩🇰 🇪🇺 🇺🇳
```

### Reset a unicoded' string

Use ```String.normalize()```

See https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/normalize

```javascript
'𝖆𝖇𝖈𝖉𝖊𝖋𝖌𝖍𝖎𝖏𝖐𝖑𝖒𝖓𝖔𝖕𝖖𝖗𝖘𝖙𝖚𝖛𝖜𝖝𝖞𝖟'.normalize('NFKC') //or NFKD
```
returns ```abcdefghijklmnopqrstuvwxyz```


### Test
Browser: `test/browser.html`
Node: `test$ node node.js`

These tests show all variants and their coverage az-AZ-09, along with flag combinations For reference, in Chrome (Ubuntu 20.04, 112.x) variants looks like this :<br><br>
<img src="media/variants-chrome-112.png">

-- or you can review a sample output, [test/result-sample.html.txt](test/result-sample.html.txt). Try it out in different browsers - there are significant difference in coverage. 

### References

https://www.unicode.org/charts/PDF/UFF00.pdf<br>
https://www.unicode.org/charts/PDF/U1F100.pdf<br>
https://www.unicode.org/charts/PDF/U1D400.pdf<br>
https://www.unicode.org/charts/PDF/U2460.pdf<br>
https://www.unicode.org/charts//PDF/Unicode-4.0/U40-0300.pdf


### Playground

For now, visit https://detfrieord.dk/tekst-til-unicode (in danish, sorry)