---
description: Simple article to setup ESLint config in Zoho Desk App.
---

# ESLint Setup

## ESLint setup for Zoho Desk React

Becoming a super hero is a fairly straight forward process:

```
npm i -g eslint@5.0.0 eslint-plugin-css-modules eslint-plugin-react eslint-plugin-react-performance @zohodesk/eslint-plugin-zsecurity
```

{% hint style="info" %}
ESLint 5.0.0 is recommended because future versions requires us to install `eslint` and its `plugins` locally.
{% endhint %}

Download and copy this file to your root directory _\(Where you imported your project in your IDE.\)_  


```text
let logLevel = 'error';

module.exports = {
  env: {
    browser: true,
    commonjs: true,
    es6: true,
    node: true
  },
  parserOptions: {
    ecmaFeatures: {
      jsx: true
    },
    sourceType: 'module'
  },
  settings: {
    react: {
      version: '16.6.0'
    }
  },
  plugins: [
    'react',
    'css-modules',
    '@zohodesk/zsecurity',
    '@zohodesk/react-performance'
  ],
  rules: {
    //General Rules
    '@zohodesk/react-performance/no-ref-mapstatetoprops': [logLevel],
    '@zohodesk/zsecurity/no-unsecure-html': [logLevel],
    '@zohodesk/zsecurity/no-protocol-check': [logLevel],
    'for-direction': [logLevel],
    'no-prototype-builtins': [logLevel],
    'no-template-curly-in-string': [logLevel],
    'array-callback-return': [logLevel],
    curly: [logLevel],
    'default-case': [logLevel],
    'dot-location': [logLevel, 'property'],
    'dot-notation': [logLevel],
    eqeqeq: [logLevel],
    'guard-for-in': [logLevel],
    'no-alert': [logLevel],
    'no-caller': [logLevel],
    'no-div-regex': [logLevel],
    'no-else-return': [logLevel],
    'no-empty-function': [logLevel],
    'no-eq-null': [logLevel],
    'no-eval': [logLevel],
    'no-extend-native': [logLevel],
    'no-extra-bind': [logLevel],
    'no-floating-decimal': [logLevel],
    'no-iterator': [logLevel],
    'no-labels': [logLevel],
    'no-loop-func': [logLevel],
    'no-multi-str': [logLevel],
    'no-new-wrappers': [logLevel],
    'no-param-reassign': [logLevel],
    'no-proto': [logLevel],
    'no-redeclare': [logLevel, { builtinGlobals: true }],
    'no-return-assign': [logLevel],
    'no-script-url': [logLevel],
    'wrap-iife': [logLevel, 'outside'],
    'block-spacing': [logLevel],
    'brace-style': [logLevel],
    camelcase: [logLevel],
    'comma-dangle': [logLevel],
    'comma-spacing': [logLevel],
    'func-call-spacing': [logLevel],
    indent: [logLevel, 2, { ignoredNodes: ['JSXElement'], SwitchCase: 1 }],
    'jsx-quotes': [logLevel, 'prefer-single'],
    'key-spacing': [logLevel],
    'keyword-spacing': [logLevel],
    'lines-between-class-members': [logLevel],
    'no-whitespace-before-property': [logLevel],
    'object-curly-spacing': [logLevel, 'always'],
    'space-before-blocks': [logLevel],
    'switch-colon-spacing': [logLevel],
    'space-in-parens': [logLevel],
    quotes: [logLevel, 'single'],
    semi: [logLevel],
    'semi-spacing': [logLevel],
    'arrow-spacing': [logLevel],
    'arrow-body-style': [logLevel],
    'arrow-parens': [logLevel, 'as-needed'],
    'no-const-assign': [logLevel],
    'no-dupe-class-members': [logLevel],
    'no-this-before-super': [logLevel],
    'no-duplicate-imports': [logLevel, { includeExports: true }],
    'no-var': [logLevel],
    'prefer-destructuring': [logLevel],
    'prefer-arrow-callback': [logLevel],
    'prefer-spread': [logLevel],
    'prefer-template': [logLevel],
    'prefer-rest-params': [logLevel],
    'no-useless-constructor': [logLevel],
    'no-duplicate-imports': [logLevel],
    'array-callback-return': [logLevel],
    'no-use-before-define': [logLevel],
    'no-unused-vars': [
      'error',
      { vars: 'all', args: 'after-used', ignoreRestSiblings: false }
    ],

    //React Rules
    'react/jsx-uses-vars': [logLevel],
    'react/jsx-uses-react': [logLevel],
    'react/default-props-match-prop-types': [logLevel],
    'react/no-redundant-should-component-update': [logLevel],
    'react/no-danger': [logLevel],
    'react/no-this-in-sfc': [logLevel],
    'react/no-will-update-set-state': [logLevel],
    'react/no-unused-state': [logLevel],
    'react/no-will-update-set-state': [logLevel],
    'react/prop-types': [logLevel],
    'react/jsx-closing-bracket-location': [logLevel],
    'react/jsx-equals-spacing': [logLevel],
    'react/jsx-indent': [logLevel, 2],
    'react/jsx-key': [logLevel],
    'react/jsx-pascal-case': [logLevel],
    'react/no-array-index-key': [logLevel],
    'react/no-unused-prop-types': [logLevel],
    'react/forbid-component-props': [0],
    'react/forbid-dom-props': [logLevel],
    'react/jsx-no-bind': [logLevel],
    'react/sort-prop-types': [logLevel],
    'react/jsx-no-duplicate-props': [logLevel],
    'react/no-deprecated': [logLevel],
    'react/no-children-prop': [logLevel],
    'react/no-unused-state': [logLevel],
    'react/default-props-match-prop-types': [logLevel],

    // 'react/require-default-props': [logLevel],
    // 'react/require-optimization': [logLevel],
    // 'react/destructuring-assignment': [logLevel],
    // 'react/no-did-update-set-state': [logLevel],

    // CSS Module Rules
    'css-modules/no-unused-class': [logLevel, { camelCase: true }],
    'css-modules/no-undef-class': [logLevel, { camelCase: 'only' }]
  }
};

```

