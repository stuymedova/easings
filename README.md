# Easings

## Easing functions

- Back easings: `backInOut(t)`, `backIn(t)`, `backOut(t)`
- Bounce easings: `bounceInOut(t)`, `bounceIn(t)`, `bounceOut(t)`
- Circle easings: `circleInOut(t)`, `circleIn(t)`, `circleOut(t)`
- Elastic easings: `elasticInOut(t)`, `elasticIn(t)`, `elasticOut(t)`
- Exponential easings: `expoInOut(t)`, `expoIn(t)`, `expoOut(t)`
- Linear easings: `linear(t)`
- Sine easings: `sineInOut(t)`, `sineIn(t)`, `sineOut(t)`
- Quadratic easings: `quadInOut(t)`, `quadIn(t)`, `quadOut(t)`
- Quartic easings: `quartInOut(t)`, `quartIn(t)`, `quartOut(t)`
- Quintic easings: `quintInOut(t)`, `quintIn(t)`, `quintOut(t)`

## Demo/Usage

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

## More on easing
[Easing Graphs / D3 / Observable](https://observablehq.com/@d3/easing)_  
[Easing Animations / D3 / Observable](https://observablehq.com/@d3/easing-animations)_  

\*Note that D3 has a slightly different API
