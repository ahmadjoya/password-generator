<!-- prettier-ignore-start -->
<!-- SOMETHING AUTO-GENERATED BY TOOLS - START -->
<br />
<br />

<p align ="center">
  <a href="https://nodei.co/npm/js-generate-password" target="_blank">
    <img src="https://nodei.co/npm/js-generate-password.png" alt="npm Info" />
  </a>
</p>

<p align="center">
  <a href="http://npm.im/js-generate-password" target="_blank">
    <img src="https://img.shields.io/npm/v/js-generate-password.svg" alt="npm Version" />
  </a>
  <a href="http://npm.im/js-generate-password" target="_blank">
    <img src="https://img.shields.io/github/v/release/ahmadjoya/js-generate-password" alt="npm Release Version" />
  </a>
  <a href="http://npm.im/js-generate-password" target="_blank">
    <img src="https://img.shields.io/npm/dm/js-generate-password.svg" alt="npm Downloads" />
  </a>
  <a href="http://npm.im/js-generate-password" target="_blank">
    <img src="https://img.shields.io/npm/l/js-generate-password.svg" alt="npm Package License" />
  </a>
</p>

<p align="center">
  <a href="https://github.com/ahmadjoya/js-generate-password/stargazers" target="_blank">
    <img src="https://img.shields.io/github/stars/ahmadjoya/js-generate-password" alt="github Stars" />
  </a>
  <a href="https://github.com/ahmadjoya/js-generate-password/network/members" target="_blank">
    <img src="https://img.shields.io/github/forks/ahmadjoya/js-generate-password" alt="github Forks" />
  </a>
  <a href="https://github.com/ahmadjoya/js-generate-password/stargazers" target="_blank">
    <img src="https://img.shields.io/github/contributors/ahmadjoya/js-generate-password" alt="github Contributors" />
  </a>
  <a href="https://github.com/ahmadjoya/js-generate-password/issues" target="_blank">
    <img src="https://img.shields.io/github/issues/ahmadjoya/js-generate-password" alt="github Issues" />
  </a>
</p>

<br />

# js-generate-password

js-generate-password is usable for every javascript and typescript based project like react, vue, node, etc. it used to generate passwords that may contain alphabets, number and symbols. The options parameter enables the user to enable or disable the characters that are used to generate random password.

The characters that may be choosen from are

- Lowercase Characters
- Uppercase Characters
- Numbers
- Symbols

The user may also specify the minimum number of character for each type.

## Installation

`npm install js-generate-password`

or

`yarn add js-generate-password`

## Usage

For the password to be generated, **parameters** are able to pass as an optional **options** object.

```javascript
import { GeneratePassword } from "js-generate-password";
const password = GeneratePassword({
  length: 14,
  symbols: true,
});
console.log(password);
```

If no parameter is passed, the default parameter will be taken as :

```javascript
options = {
  length: 10,
  lowercase: true,
  uppercase: true,
  numbers: true,
  symbols: false,
  exclude: "",
  minLengthLowercase: 1,
  minLengthUppercase: 1,
  minLengthNumbers: 1,
  minLengthSymbols: 0,
};
```

### Available options

Any of these can be passed into the options object for each function.

| Name               | Description                                                                                                                                                 | Default Value |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| length             | Integer, length of password.                                                                                                                                | 10            |
| lowercase\*        | Boolean, put lowercase letters in password                                                                                                                  | true          |
| uppercase\*        | Boolean, put uppercase letters in password.                                                                                                                 | true          |
| numbers\*          | Boolean, put numbers in password.                                                                                                                           | true          |
| symbols\*          | Boolean, put symbols in password.                                                                                                                           | false         |
| exclude            | String, characters to be excluded from password.                                                                                                            | ''            |
| minLengthLowercase | only if **lowercase** is set to **true**, minLengthLowercase will create a password that will have minimum number of lower case characters in the password. | 1             |
| minLengthUppercase | only if **uppercase** is set to **true**, minLengthUppercase will create a password that will have minimum number of upper case characters in the password. | 1             |
| minLengthNumbers   | only if **numbers** is set to **true**, minLengthNumbers will create a password that will have minimum number of numbers in the password.                   | 1             |
| minLengthSymbols   | only if **symbols** is set to **true**, minLengthSymbols will create a password that will have minimum number of symbols in the password.                   | 1             |

\*At least one should be true.

## Example

- **No Options passed.**

```javscript
const {GeneratePassword} = require("js-generate-password");
const password = GeneratePassword();
console.log(password);
```

In the above case, no parameter is passed as option. Therefore the default values will be taken - which will have alphabets, both upper and lower case, numbers, and will be of length 10 characters.

```javascript
xDU6izb3PV;
```

- **Length parameter passed.**

```javascript
const password = GeneratePassword({ length: 25 });
console.log(password);
```

The password generated is like this

```javascript
U4c3KpQP5UrbZgTcrqMgFeI3R;
```

- **exclude parameter passed.**

```javascript
options={
      exclude : 'abc567XYZ';
      }
password = GeneratePassword(options);
console.log(password);
```

The generated password wouldn't has none of 'abc567XYZ' characters

```javascript
J9yCfttQNj;
```
