# React Component Library

A set of isolated, reusable components built with React and TypeScript.

## Quick Start

```
git clone https://github.com/mcopper1226/react-storybook-starter.git my-components
cd my-components
yarn
yarn start
```

## Building the Package

To generate a build, simply run `yarn build`.

## About the Project

This is a vanilla React application with very minimal configuration. Code is linted and formatted. Checked in code should be formatted, but this is not enforced programatically. To format, simply run `yarn prettier:fix`.

### Storybook

To view components, run `yarn storybook`. Story setup can be found in the individual component directories with the `*.stories.tsx` extension. Note: these files are not included in the dist output.

### Styles (Modules and Global)

The project uses a mix of global SCSS and SCSS modules that are scoped to individual components. This approach helps guard against inadvertent naming collisions and keeps things tidier.

To use a global class:

- `<div className='container'>`
- Global styles should live in the styles directory and must be imported through the `base.scss` entry point.

To use a module:

- Create a file that follows the convention: `[name].module.scss` (ideally placed inside of the component directory, but it doesn't have to be)
- Import this module at the top of your component file: import styles from [name].module.scss
- Use the styles reference in all of your class: `<div className={styles.fancy}>Fancy Text</div>`
- Note: if your class name includes a hyphen character, you will need to use bracket notation: `<div className={styles['fancy--alternate']}>Alternate Fancy Text</div>`
