# sb-react18-repro

This project demonstrates an issue where Storybook shows a loading indicator forever when using React 18.

## Reproduction Steps

1. `yarn install`
2. `yarn storybook`

## How This Repository was Created

1. `npx create-react-app sb-react18-repro --scripts-version 4.0.3`
2. `cd sb-react18-repro`
3. (Optiona) I switched from npm to Yarn 3.
4. `npx sb@next init`
5. Upgrade `@storybook/preset-create-react-app` to 4.1.0.
6. Remove `@storybook/builder-webpack5` and `@storybook/manager-webpack5` and remove the reference to Webpack 5 from `.storybook/main.js`. This makes Storybook use Webpack 4 which is what react-scripts v4 is using.
