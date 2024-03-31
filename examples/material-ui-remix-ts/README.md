# Material UI - Remix example in TypeScript

## How to use

Download the example [or clone the repo](https://github.com/mui/material-ui):

<!-- #default-branch-switch -->

```bash
curl https://codeload.github.com/mui/material-ui/tar.gz/next | tar -xz --strip=2  material-ui-next/examples/material-ui-remix-ts
cd material-ui-remix-ts
```

Install it and run:

```bash
npm install
npm run dev
```

or:

<!-- #default-branch-switch -->

[![Edit on StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/mui/material-ui/tree/next/examples/material-ui-remix-ts)

[![Edit on CodeSandbox](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/p/sandbox/github/mui/material-ui/tree/next/examples/material-ui-remix-ts)

## The idea behind the example

The project uses [Remix](https://remix.run/), which is a full stack web framework.
It includes `@mui/material` and its peer dependencies, including [Emotion](https://emotion.sh/docs/introduction), the default style engine in Material UI v5.
If you prefer, you can [use styled-components instead](https://next.mui.com/material-ui/integrations/interoperability/#styled-components).

## The most important thing

If you are using vite in Remix 2.0, especially when your package.json specifies ` "type": "module",`, and especially Vite with Single-Page-App (SPA): you must bring in Material components as named imports (e.g. `import { Box } from "@mui/material"`) . This applies to `@mui/system`, and likely other `@mui` packages.
As of v5 in Mar 2024, you cannot use the default import approach offered in MUI examples (e.g. `import Box from "@mui/material/Box"`) anywhere in your Remix codebase. If you do, you can face obscure CommonJS errors which, for MUI, do not seem solvable using the ways [e.g. the Remix SPA readme](https://remix.run/docs/en/main/future/spa-mode#cjsesm-dependency-issues) suggests.

## What's next?

<!-- #default-branch-switch -->

You now have a working example project.
You can head back to the documentation and continue by browsing the [templates](https://next.mui.com/material-ui/getting-started/templates/) section.
