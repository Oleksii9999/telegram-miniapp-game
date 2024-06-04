# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default {
  // other rules...
  parserOptions: {
    ecmaVersion: "latest",
    sourceType: "module",
    project: ["./tsconfig.json", "./tsconfig.node.json"],
    tsconfigRootDir: __dirname,
  },
};
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list

## Setup ngrok

1. Install ngrok globally

```bash
brew install ngrok/ngrok/ngrok
```

2. Create an account on ngrok and get the authtoken

```bash
ngrok config add-authtoken <your_auth_token>
```

3. Start ngrok

```bash
ngrok http --domain=[DOMAIN] https://localhost:5173/

```

## TODO

- [ ] Get profile picture, if not present then show Initials
- [ ] Load game once on /game route. Handle initialization correcty
- [ ] Implement sprites, add 2-3 objects with different appear, removal animation
- [ ] Game starts slower going faster
- [ ] It should have limited amount of falling objects and they should not be that concentrated and spread within the timeframe of 15 seconds
- [ ] Create success and failure screen
- [ ] Handle callback when game is over
- [ ] Create a menu fixed to bottom with items "Home" and "Invite Friends". One should go to home page and the other should go to the invite friends page.
- [ ] Create invite friends page.
