<!--
author:   André Dietrich & Sebastian Zug
email:    LiaScript@web.de
version:  0.0.2
language: en
narrator: US English Female
-->

# Todo-List

- [ ] Basic Implementation & PWA (Reader)
- [ ] Mutlimedia Extensions
- [ ] Tables
- [ ] Animations & TTS output & Presentation Styles
- [ ] ASCII-art
- [ ] Scripting & Code
- [ ] Macros & Libraries

## Implementation

https://github.com/liascript/liascript

## Multimedia Extensions

[LiaScript](https://LiaScript.github.io)

[Annunciation of the brith of Christ](https://upload.wikimedia.org/wikipedia/commons/5/51/Leonardo_da_Vinci_Annunciation.jpg "*Annunciation c. 1472–1476*: is thought to be Leonardo's earliest complete work")

[VIVALDI-BACH; Concerto in D Major 1. Allegro](https://upload.wikimedia.org/wikipedia/commons/3/3f/VIVALDI-BACH%3B_Concerto_in_D_Major_1._Allegro%2C_BWV._972.ogg)

[LiaScript Multimedia Basics](https://www.youtube.com/watch?v=bICfKRyKTwE)

[Animal cell](https://sketchfab.com/3d-models/animal-cell-downloadable-ddc40bb0900544959f02d3ff83c32615)

[Circuit simulation](https://www.falstad.com/circuit/circuitjs.html?startCircuit=majority.txt)


## Tables


| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |             02 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |


                           {{1-2}}
<!--
data-title="Government expenditure on education"
data-xlabel="year"
data-ylabel="% of GDP"
-->
| Year | Finland |     USA | Germany |   China |
| ---- | -------:| -------:| -------:| -------:|
| 1995 | 6.80942 |         | 4.42079 | 1.84192 |
| 1996 | 6.86052 |         | 4.48319 | 1.85338 |
| 1997 |         |         |         |         |
| 1998 |         |         | 4.45345 | 1.84432 |
| 1999 | 5.86960 |         |         | 1.88803 |
| 2000 | 5.71687 |         |         |         |
| 2001 | 5.84797 |         |         |         |
| 2002 | 6.02477 |         |         |         |
| 2003 | 6.17476 |         |         |         |
| 2004 | 6.16849 |         |         |         |
| 2005 | 6.03605 |         |         |         |
| 2006 | 5.93809 |         | 4.27930 |         |
| 2007 | 5.68608 |         | 4.34302 |         |
| 2008 | 5.84676 |         | 4.40954 |         |
| 2009 | 6.48517 |         | 4.88047 |         |
| 2010 | 6.54070 | 5.42001 | 4.91368 |         |
| 2011 | 6.48200 | 5.22389 | 4.80779 |         |
| 2012 | 7.19254 | 5.19485 | 4.93331 |         |
| 2013 | 7.15848 | 4.94378 | 4.93496 |         |
| 2014 | 7.15155 | 4.98948 | 4.93112 |         |

### Animations & TTS output & Presentation Styles

            --{{0}}--
Animations or effects are always associated with two curly braces. They can be either inline, as demonstrated below:

             {{0-2}}
<!-- data-transpose -->
| Music-Style {0-1}{1994} {1}{2014} |      Student rating |
|:--------------------------------- | -------------------:|
| Classic                           |   {0-1}{50} {1}{20} |
| Country                           |   {0-1}{50} {1}{30} |
| Reggae                            |                 100 |
| Hip-Hop                           | {0-1}{200} {1}{220} |
| Hard-Rock                         | {0-1}{350} {1}{400} |
| Samba                             | {0-1}{250} {1}{230} |

               --{{2}}--
Or you can use it to make entire markdown-blocks appear or dissappear.

                {{2-3}}
* important
* ~~**very important**~~
* Not ^~important at all~^
* ;-) --> $ f(a,b,c) = \frac{(a^2+b^2+c^2)}{22}^3 $


          --{{3 Russian Female}}--
Первоначально создан в 2004 году Джоном Грубером (англ. John Gruber) и Аароном
Шварцем. Многие идеи языка были позаимствованы из существующих соглашений по
разметке текста в электронных письмах...

## ASCII-art

Use ASCII-Art to draw diagrams:

                                    Multiline
    1.9 |    DOTS
        |                 ***
      y |               *     *
      - | r r r r r r r*r r r r*r r r r r r r
      a |             *         *
      x |            *           *
      i | B B B B B * B B B B B B * B B B B B
      s |         *                 *
        | *  * *                       * *  *
     -1 +------------------------------------
        0              x-axis               1


  {{1}}
<!-- style="display: block; margin-left: auto; margin-right: auto; max-width: 315px;" -->
````````````
                           .--->  F
  A       B     C   D     /
  *-------*-----*---*----*----->  E
           \            ^ \
            v          /   '--->  G
             B --> C -'
````````````

{{2}} Quizzes???


## Scripting & Code



### Simple

The sum of
<script output="a" default="1" input="range">@input</script>
and
<script output="b" default="1" input="number">@input</script>
is
<script>@input(`a`) + @input(`b`)</script>.

### Not so simple

The first value defines some kind of range:
<script input="range" value="2" output="range">@input</script>
, while the second can be interpreted as range
<script input="range" value="50" output="amplitude">@input</script>.
You can double-click on any gray element to inspect and edit its javascript code.


<script run-once style="display: inline-block; width: 100%">
function func(x) {
    x /= 10;
    return Math.sin(x) * Math.cos(x * @input(`range`) + 1) * Math.sin(x * 3 + 2) * @input(`amplitude`);
}

function generateData() {
    let data = [];
    for (let i = -200; i <= 200; i += 0.1) {
        data.push([i, func(i)]);
    }
    return data;
}

let option = {
    animation: false,
    grid: {
        top: 40,
        left: 50,
        right: 40,
        bottom: 50
    },
    xAxis: {
        name: 'x',
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    yAxis: {
        name: 'y',
        min: -100,
        max: 100,
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    dataZoom: [{
        show: true,
        type: 'inside',
        filterMode: 'none',
        xAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }, {
        show: true,
        type: 'inside',
        filterMode: 'none',
        yAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }],
    series: [
        {
            type: 'line',
            showSymbol: false,
            clip: true,
            data: generateData()
        }
    ]
}

"HTML: <lia-chart option='" + JSON.stringify(option) + "'></lia-chart>"

</script>


### Macros & Libraries

<script input="range" value="0" default="0">
`The square of ${@input} is ${@input * @input}`
</script>

https://github.com/LiaTemplates

### Preview-lia

[preview-lia](https://liamd.informatik.tu-freiberg.de//7lxt5X-YW/download)

Preview GitHub-Projects on your own Website:

https://aizac.herokuapp.com/markdown-just-got-a-new-preview-tag/
