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
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
  },
};
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list

# Instalaciones

## Crear proyecto: yarn + vite + React + TypeScript

1. Ejecutar: yarn create vite
2. Dar nombre al proyecto
3. Seleccionar: React
4. Seleccionar: TypeScript

## ESLint

1. Comprobar instalaciones por defecto
2. Tener instalada la extensión para ESLint

## Prettier

1. Instalación de Prettier: yarn add --dev --exact prettier
2. Crear archivo de configuración: .prettierrc (JSON)
3. Configurar opciones para sobrescribir los valores por defecto en .prettierrc [Prettier Options](https://prettier.io/docs/en/options)

## ESLint + Prettier (conflictos)

1. Instalar eslint-config-prettier: yarn add --dev eslint-config-prettier
2. Añadir en .eslintrc.cjs extends a: prettier

## Scripts para Prettier

1. En package.json, añadir en la sección scripts el comando de format: "format": "prettier --write ./src"
2. Conveniente ejecutar el formato: yarn format
3. Configurar autoformateo de ESLint en VSCode para que aplique las reglas automáticamente:
   ```json
   "editor.codeActionsOnSave": {
     "source.fixAll.eslint": true
   },
   "editor.formatOnPaste": true,
   "editor.formatOnSave": true,
   "editor.formatOnType": true,
   ```
