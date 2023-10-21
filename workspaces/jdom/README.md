# JDOM <!-- [![Playwright](https://github.com/jdomjs/jdom/actions/workflows/playwright.yml/badge.svg)](https://github.com/jdomjs/jdom/actions/workflows/playwright.yml) -->

### Installation

```
npm install --save jdom

```

### Import

```
import { $, domFactory, svgFactory, style } from 'jdom';
```

---

### Compose DOM Example

##### example:

```
const {div, script, span} = domFactory;
const myDiv = div({
     parent: document.body
     id: 'myDiv',
     style: {
         color: 'red'
     },
     dataset: {
         foo: 'bar'
     },
     children: [
         'injecting script',
         script({src: 'http://some.url'}),
         'done'
     ],
     click: () => {
         alert('now');
     }
 });
 span({parent: myDiv, children: ['SomeText!!!!']});
```

---

### Compose SVG Example

##### example:

```
 const {svg, rect, circle} = svgFactory;

 svg({
     id: 'mySVG',
     width: 200,
     height: 200,
     viewBox: '0 0 200 200',
     children: [
         rect({
             fill : 'red',
             x:5,
             y:5,
             width: 190,
             height: 190
         }),
         circle({
             fill: 'yellow',
             cx: 100,
             cy:100,
             r:80
         })
     ],
     parent: document.body
 });
```

---

### style (**elem**: _HTMLElement_, **props**: _object_)

_update element style_

##### example:

```
 const a = document.getElementById('aDiv');
 style(a, {
     color: 'green',
     backgroundColor: 'red'
 })
```

---

### QueryList(\$) (**selector**: _string_)

##### example:

```
 const $a = $('#aDiv');
```

#### Querylist Event Methods

-   on
-   once
-   off
-   dispatch

##### example:

```
 $a.on('click', () => {
    console.log('clicked');
 });
 $a.dispatch('click');
```

#### Querylist Style Methods

-   style

##### example:

```
 $a.style({
     color: 'green',
     backgroundColor: 'red'
 });
```

#### Querylist Array Prototype Methods

-   filter
-   forEach
-   map
-   pop
-   push
-   shift
-   slice
-   some
-   splice
-   unshift

##### example:

```
const $allForms = $('form');
$allForms.forEach(form => { console.log(form); });
```
