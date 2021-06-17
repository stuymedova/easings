# Easings

## Easing functions

- Back easings: `backInOut`, `backIn`, `backOut`
- Bounce easings: `bounceInOut`, `bounceIn`, `bounceOut`
- Circle easings: `circleInOut`, `circleIn`, `circleOut`
- Elastic easings: `elasticInOut`, `elasticIn`, `elasticOut`
- Exponential easings: `expoInOut`, `expoIn`, `expoOut`
- Linear easings: `linear`
- Sine easings: `sineInOut`, `sineIn`, `sineOut`
- Quadratic easings: `quadInOut`, `quadIn`, `quadOut`
- Quartic easings: `quartInOut`, `quartIn`, `quartOut`
- Quintic easings: `quintInOut`, `quintIn`, `quintOut`

## Usage (example)

```js
import * as easings from 'https://deno.land/x/easings/easings.ts';

for (let t = 0; t <= 1; t += 0.05) {
  const eased = easings.cubicInOut(t);
  const str = repeat('*', eased * 20);
  console.log(str);
}

function repeat(str, num) {
  let result = '';
  num = Math.round(num);
  while (num--) {
    if(num >= 0) result += str;
    else num = 0
  }
  return result;
}
```

Output: 
```

*
*
**
***
*****
*******
**********
*************
***************
*****************
******************
*******************
*******************
********************
********************
********************
```