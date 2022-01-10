# Personal ESLint Config

Feel free to use this in your projects, or fork and modify if you want to adopt the same style I use.

## Steps

### 1. Install this module

**npm**:

```sh
npm i --save-dev aarongodin/eslint-config#main
```

**yarn**:
```sh
yarn add --dev aarongodin/eslint-config#main
```

> This module is not published on NPM, and as such will be installed from this GitHub repo.

### 2. Create an `.eslintrc.js` file

> Note: remove or change the `ignorePatterns` based on your requirements.

```sh
cat << EOF > .eslintrc.js
module.exports = {
  extends: "@aarongodin",
  ignorePatterns: ["dist", "__snapshots__/**"],
}
EOF
```

### 3. Use Prettier

Modify `package.json` to add the following property:

```json
{
  "prettier": "@aarongodin/eslint-config/prettier.json"
}
```

### 4. Run ESLint

You may need to restart your editor for the eslint configuration to be used. This is a common script I use for linting a project which can be added to the `scripts` definition in `package.json`:

```json
{
  "scripts": {
    "lint": "eslint . --env node --ext .ts --ext .js"
  }
}
```

## Making your own

If you want to convert this into your own personal style, first Fork the repository through GitHub (or simply clone this repo to push somewhere else). After you clone the repository, follow these steps:

1. Change the `name` of the package in `package.json`. I recommend using your GitHub username as the namespace (characters after the `@` symbol).
2. Find and replace references to my username (`aarongodin`) with your own username.
3. Push changes to your remote, and follow your own Readme! If you have pushed the repo to a location other than GitHub, additional steps will be required to install from the location of that git repository. Refer to the npm docs on how to specify a git repository.
