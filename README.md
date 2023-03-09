```
yarn add react-native-reanimated react-native-splash-screen react-native-gesture-handler react-hook-form @react-navigation/bottom-tabs @react-navigation/native @react-navigation/native-stack react-native-orientation-locker react-native-safe-area-context react-native-screens react-native-vector-icons react-native-spinkit
```

```
yarn add -D babel-plugin-module-resolver eslint-plugin-import eslint-plugin-react eslint-plugin-react-hooks prettier eslint react-native-dotenv @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-plugin-react eslint-plugin-react-hooks react-native-vector-icons @types/react-native-vector-icons
```

### EsLint config

```json
{
  "root": true,
  "extends": ["@react-native-community", "prettier"],
  "plugins": ["react", "react-hooks", "import"],
  "overrides": [
    {
      "files": ["*.ts", "*.tsx", "*.js", "*.jsx"],
      "rules": {
        "no-param-reassign": 0,
        "import/order": [
          "error",
          {
            "groups": ["builtin", "external", "internal", "sibling"],
            "pathGroups": [
              {
                "pattern": "react",
                "group": "builtin",
                "position": "before"
              },
              {
                "pattern": "src/**",
                "group": "external",
                "position": "after"
              }
            ],
            "pathGroupsExcludedImportTypes": ["react"],
            "newlines-between": "always",
            "alphabetize": {
              "order": "asc",
              "caseInsensitive": true
            }
          }
        ],
        "sort-imports": [
          "error",
          {
            "ignoreDeclarationSort": true
          }
        ],
        "import/no-default-export": 0,
        "react-native/no-unused-styles": 0,
        "react-native/no-inline-styles": 2,
        "react-native/no-color-literals": 2,
        "import/prefer-default-export": 0
      }
    }
  ],
  "rules": {
    "global-require": 0,
    "no-param-reassign": [
      2,
      {"props": true, "ignorePropertyModificationsForRegex": ["^acc"]}
    ],
    "react-hooks/rules-of-hooks": 1,
    "react-hooks/exhaustive-deps": 0,
    "react/function-component-definition": [
      1,
      {"namedComponents": "function-declaration"}
    ],
    "@typescript-eslint/no-unused-vars": "error",
    "import/prefer-default-export": 1
  }
}
```

### Prettier config

```json
{
  "arrowParens": "avoid",
  "bracketSameLine": true,
  "bracketSpacing": false,
  "singleQuote": true,
  "trailingComma": "all",
}
```

### 

```js
{
  <...>,
  "compilerOptions": {
    "baseUrl": ".",
    "paths" : {
      "src/*": ["src/*"]
    },
    /* Completeness */
    "skipLibCheck": true
  }
}
```
