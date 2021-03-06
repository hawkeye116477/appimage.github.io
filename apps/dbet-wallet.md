---
layout: app

permalink: /dbet-wallet/
description: DBET Wallet

icons:
  - dbet-wallet/icons/512x512/dbet-wallet.png

screenshots:
  - dbet-wallet/screenshot.png

authors:
  - name: decent-bet
    url: https://github.com/decent-bet

links:
  - type: GitHub
    url: decent-bet/platform-wallet
  - type: Download
    url: https://github.com/decent-bet/platform-wallet/releases

desktop:
  Desktop Entry:
    Name: DBET Wallet
    Comment: DBET Wallet
    Exec: AppRun
    Terminal: false
    Type: Application
    Icon: dbet-wallet
    StartupWMClass: DBET Wallet
    X-AppImage-Version: 2.0.0-alpha
    Categories: Finance
    X-AppImage-BuildId: 1BRQ3qTLaQMTyrR5QhPAnnlpOgD
  AppImageHub:
    X-AppImage-Signature: no valid OpenPGP data found. the signature could not be verified.
      Please remember that the signature file (.sig or .asc) should be the first file
      given on the command line.
    X-AppImage-Type: 2
    X-AppImage-Architecture: x86_64

electron:
  license: ISC
  repository: https://github.com/decent-bet/platform-wallet
  version: 2.0.0-alpha
  author:
    name: Decent.bet
    email: support@decent.bet
  private: false
  dependencies:
    "@fortawesome/fontawesome": "^1.1.8"
    "@fortawesome/fontawesome-free-brands": "^5.0.13"
    "@fortawesome/fontawesome-free-solid": "^5.0.13"
    "@fortawesome/fontawesome-svg-core": "^1.2.4"
    "@fortawesome/react-fontawesome": "^0.1.2"
    "@google-cloud/logging-winston": "^0.9.0"
    "@material-ui/core": "^3.0.1"
    "@material-ui/icons": "^3.0.1"
    async: "^2.6.0"
    axios: "^0.18.0"
    bignumber.js: "^7.2.1"
    bip39: "^2.5.0"
    crypto-js: "^3.1.9-1"
    dotenv: "^5.0.1"
    electron-log: "^2.2.17"
    electron-serve: "^0.1.0"
    electron-simple-updater: "^1.2.1"
    electron-updater: "^3.1.2"
    ethereum-address: 0.0.4
    ethereum-units: 0.0.1-b
    ethers: "^2.2.6"
    ethjs-provider-signer: "^0.1.4"
    ethjs-signer: "^0.1.1"
    eventing-bus: "^1.3.3"
    hex2dec: "^1.1.0"
    http2: "^3.3.7"
    material-ui: "^0.20.2"
    moment: "^2.20.1"
    path: "^0.12.7"
    promise: "^8.0.1"
    react: "^16.4.2"
    react-copy-to-clipboard: "^5.0.1"
    react-dom: "^16.4.2"
    react-event-components: "^1.1.0"
    react-fittext: "^1.0.0"
    react-intl: "^2.4.0"
    react-material-ui-keyboard: "^6.2.1"
    react-router-dom: "^4.3.1"
    react-tap-event-plugin: "^3.0.3"
    request: "^2.83.0"
    rxjs: "^6.2.2"
    scrypt: "^6.0.3"
    thor-devkit: "^0.2.4"
    thorify: "^1.0.1"
    web3: 1.0.0-beta.34
    web3-eth-abi: 1.0.0-beta.30
    web3-eth-accounts: 1.0.0-beta.30
    web3-providers-ws: 1.0.0-beta.34
    web3-utils: 1.0.0-beta.30
    winston: "^2.4.4"
  jest:
    collectCoverageFrom:
    - src/**/*.{js,jsx}
    setupFiles:
    - "<rootDir>/config/polyfills.js"
    - "<rootDir>/src/setupTests.js"
    setupTestFrameworkScriptFile: mock-local-storage
    testMatch:
    - "<rootDir>/src/**/__tests__/**/*.js?(x)"
    - "<rootDir>/src/**/?(*.)(spec|test).js?(x)"
    testEnvironment: node
    testURL: http://localhost
    transform:
      "^.+\\.(js|jsx)$": babel-jest
      "^.+\\.css$": "<rootDir>/config/jest/cssTransform.js"
      "^(?!.*\\.(js|jsx|css|json)$)": "<rootDir>/config/jest/fileTransform.js"
    transformIgnorePatterns:
    - "[/\\\\]node_modules[/\\\\].+\\.(js|jsx)$"
    moduleNameMapper:
      "^react-native$": react-native-web
    moduleFileExtensions:
    - web.js
    - js
    - json
    - web.jsx
    - jsx
    - ts
    - tsx
    - node
  main: out/electron.js
  lint-staged:
    "*.{js,json,css,md}":
    - prettier --write
    - git add
---
