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
[Easing Graphs / D3 / Observable](https://observablehq.com/@d3/easing)*  
[Easing Animations / D3 / Observable](https://observablehq.com/@d3/easing-animations)*  

\*Note that [D3](https://github.com/d3/d3-ease) has a slightly different API
