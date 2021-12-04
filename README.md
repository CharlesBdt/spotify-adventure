# Spotify Adventure

## Project setup

```sh
yarn install
```

## Compiles and hot-reloads for development

```sh
yarn serve
```

## Compiles and minifies for production

```sh
yarn build
```

## Live demo

Visit [Spotify Adventure](https://spotify-adventure.web.app/)

## Lints and fixes files

To use formatting on VS Code please install these plugins : [Eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) and [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode).\
Follow Prettier extension's instructions to setup "format on save" for ease of use.

```sh
yarn lint
```

For VueJS tooling into VS Code, you can install [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur)

## Spotify Developer

Connect your Spotify account in the [Developer Dashboard](https://developer.spotify.com/dashboard/applications)\
Click to "Create an app"\
When done, click on the created app

Fill your .env.development.local file with this app values :

```sh
VUE_APP_CLIENT_ID=
# Client ID is found on the app homepage

VUE_APP_REDIRECT_URL_AFTER_LOGIN=
# Redirect URL after login can be found under "Edit Settings" > "Redirect URIs"

VUE_APP_SPOTIFY_AUTHORIZE_ENDPOINT=
# Spotify Authorize Endpoint is from the doc with value "https://accounts.spotify.com/authorize"
```

For each new endpoint you want to add, don't forget to add the required scopes into the `store/modules/auth.js` file.

## Firebase Hosting

Create your .env.production.local file for hosting with same content as above.

Then prepare for production [here](#compiles-and-minifies-for-production)

When done, run these commands :

```sh
yarn add -g firebase-tools
firebase login
firebase init
firebase deploy
```

## Naming convention

### Files naming

- Folders : kebab-case or spinal-case, eg : `my-components`
- Pages (used by the router) : kebab-case or spinal-case, eg : `my-components` or `my-component.vue`
- Assets (Pictures, css files, logos, ...) : kebab-case or spinal-case, eg: `my-logo.svg`
- Vue components : PascalCase or UpperCamelCase, eg : `MyComponent.vue`

### Variables and classes naming

- html : kebab-case or spinal-case, eg : `my-html-components`
- css : kebab-case or spinal-case, eg : `my-css-class`
- JS functions and variables : camelCase, eg : `myFunction` or `myVariable`
- Vue components and JS classes : PascalCase or UpperCamelCase, eg : `MyComponent` or `MyClass`
