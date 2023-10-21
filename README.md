# JDOM <!-- [![Playwright](https://github.com/jdomjs/jdom/actions/workflows/playwright.yml/badge.svg)](https://github.com/jdomjs/jdom/actions/workflows/playwright.yml) -->

lightweight JavaScript to DOM interface for simple "html as code" web apps

---

-   Use JavaScript to compose HTML
    -   Simple js interface similar to React:
        -   tag(props, children)
    -   _jdom.createElement_ method can be used to compose JSX without react
-   jQuery like "QueryList" selector: _$_

---

### Monorepo

-   This project is setup as a monorepo using npm workspaces
    -   [jdom](https://github.com/jdomjs/jdom/tree/main/workspaces/jdom/README.md) -
        jdom UMD module
    -   [docs](https://github.com/jdomjs/jdom/tree/main/workspaces/docs/README.md) -
        Github Pages: https://jdomjs.github.io

### Local Development

-   **npm i** - install dependencies
-   **npm start** - runs the development server that builds github pages site
-   **npm test** - run node unit tests and playwright integration tests
-   **npm run test:ui** - launch playwright gui
-   **npm build** - make a production build

---

### History

Born sometime around 2012 out of it's author's mildly obsessive passion for
simplicity, efficiency and minimalism, while trying to avoid bloated
dependencies. This tiny library was less than 1 kb and allowed it's developer to
write simple web apps with minimal dependencies. It was originally an AMD module
and used to build a few personal projects, an in-browser code text editor, a
multi-office Polycom video conference control dashboard, and a surf forecasting
website. When React came on the scene, this library was abandoned and replaced
in those projects.

5 years later the Author was working for a company named Vertebrae and needed an
ultra light dom library. At the time Vertebrae was building augmented/virtual
reality ad units and selling them through ad exchanges, things like 360 video
and virtual try on. The web experiences were already heavy and every kilobyte
needed to be squeezed to maintain a profit margin (cost to run ads are directly
tied to bandwidth served). So in 2017 Rob Higgins published his library to NPM,
calling it JDOM.

It was used to build all of vertebrae's ad creatives for companies like King
(candy crush), Saban (power rangers), the LA Chargers, the Jigsaw movie
franchise, the Blair Witch Project etc.. Vertebrae later pivots away from
advertising into e-commerce AR experiences and 3D art production pipelines,
where JDOM is also used. This time the technology is implemented into merchant
e-commerce websites like Moscott, Goodr, Tenth Street Hats, Lucy in the Sky.
Vertebrae was acquired by Snap in July 2021 and continued to support those
e-commerce websites for about 2 years until Oct 2023 Snap decides to discontinue
ARES (Augmented Reality Enterprise Shopping Suite), laying off 170 employees.

Now with a little extra time on his hands, Rob decides to clean up and modernize
this repo by:

-   Adding a Github Actions CI/CD/testing suite
-   Adding Github Pages documentation website
-   NPM workspaces architecture
-   Moved to .mjs file type that allows import/export keywords without a compile
    step, so source files can be imported and used directly.

---

#### Possible future features if I continue to have time:

-   Add typescript definitions
-   Add new optional components:
    -   jdom-fetch - fetch and inject server side HTML
    -   jdom-form - use json to generate a form and all of it's inputs
    -   jdom-bootstrap - components for common bootstrap elements
