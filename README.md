# ip-access-control
Allow, Deny style access control for IP access validation.

## Installation
```bash
# NPM
npm install --save @hyperingenuity/ip-access-control

# Yarn
yarn add @hyperingenuity/ip-access-control
```

## Usage
To create an access control validator for a given scheme:
```javascript
const IPAccessControl = require('@hyperingenuity/ip-access-control');

const accessValidator = new IPAccessControl({
  order: 'deny, allow',
  allow: [ '0.0.0.0/0' ],
  deny: []
});
```
To validate a request IP against the validator:
```javascript
const allowed = accessValidator.check('127.0.0.1'); // Boolean return value
```
