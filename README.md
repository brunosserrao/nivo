<img alt="nivo" src="https://raw.githubusercontent.com/plouc/nivo/master/nivo.png" width="150" height="42" />

[![License][license-image]][license-url]
[![Travis CI][travis-image]][travis-url]
[![NPM version][npm-image]][npm-url]
[![Dependencies][gemnasium-image]][gemnasium-url]

- [Layouts](#layouts)
    - [Pie](#pie)
        - [Pie Legends](#pie-legends)
    - [Stack](#stack)
- [Colors](#colors)

## Layouts

### Pie

Use [d3 Pie layout](https://github.com/mbostock/d3/wiki/Pie-Layout).

#### Pie Legends

##### PieColumnLegends

<img alt="PieColumnLegends" src="https://raw.githubusercontent.com/plouc/nivo/master/doc/nivo-pie-legends-column.png" width="80" height="80" />

```javascript
import { Chart, Pie, PieColumnLegends } from 'nivo';

// ...

React.render((
    <Chart>
        <Pie data={data}>
            <PieColumnLegends />
        </Pie>
    </Chart>
), document.getElementById('pie'));
```

###### properties

key                  | required | default     | description
---------------------|----------|-------------|----------------------------
**labelFn**          | no       | `undefined` |
**radiusOffset**     | yes      | `16`        |
**horizontalOffset** | yes      | `30`        |
**textOffset**       | yes      | `10`        |
**lineColor**        | yes      | `'none'`    | see [colors](#colors)
**textColor**        | yes      | `'none'`    | see [colors](#colors)



##### PieRadialLegends

<img alt="PieRadialLegends" src="https://raw.githubusercontent.com/plouc/nivo/master/doc/nivo-pie-legends-radial.png" width="80" height="80" />

```javascript
import { Chart, Pie, PieRadialLegends } from 'nivo';

// ...

React.render((
    <Chart>
        <Pie data={data}>
            <PieRadialLegends />
        </Pie>
    </Chart>
), document.getElementById('pie'));
```

##### PieSliceLegends

<img alt="PieSliceLegends" src="https://raw.githubusercontent.com/plouc/nivo/master/doc/nivo-pie-legends-slice.png" width="80" height="80" />

```javascript
import { Chart, Pie, PieSliceLegends } from 'nivo';

// ...

React.render((
    <Chart>
        <Pie data={data}>
            <PieSliceLegends />
        </Pie>
    </Chart>
), document.getElementById('pie'));
```

##### Combining Pie legends

```javascript
import { Chart, Pie, PieColumnLegends, PieSliceLegends } from 'nivo';

// ...

React.render((
    <Chart>
        <Pie data={data}>
            <PieColumnLegends />
            <PieSliceLegends />
        </Pie>
    </Chart>
), document.getElementById('pie'));
```

### Stack

Use [d3 Stack layout](https://github.com/mbostock/d3/wiki/Stack-Layout)

## Colors

Beside highlighting data insights, your dataviz should be pretty, right ?
**nivo** provides an easy way to deal with colors, very useful when dealing with nested components.

A lot of components have a `*Color` property, but what can we pass to it ?

- `none` will do nothing, it's often the default, it's useful if you manage chart styles via external **css**
- `inherit` will use color from parent context/component
- `inherit:darker(.5)` will use parent context/component color, and apply [`darker`](https://github.com/mbostock/d3/wiki/Colors#rgb_darker) function on it with an amount of `.5`
- `inherit:brighter(1)` will use parent context/component color, and apply [`brighter`](https://github.com/mbostock/d3/wiki/Colors#rgb_brighter) function on it with an amount of `1`

[license-image]: https://img.shields.io/github/license/plouc/nivo.svg?style=flat-square
[license-url]: https://github.com/plouc/nivo/blob/master/LICENSE.md
[npm-image]: https://img.shields.io/npm/v/nivo.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/nivo
[travis-image]: https://img.shields.io/travis/plouc/nivo.svg?style=flat-square
[travis-url]: https://travis-ci.org/plouc/nivo
[gemnasium-image]: https://img.shields.io/gemnasium/plouc/nivo.svg?style=flat-square
[gemnasium-url]: https://gemnasium.com/plouc/nivo
