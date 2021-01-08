# FUNCTION TEMPLATE

## NAME, INPUT, RETURNS, VARIANT, THROWS

```javascript

/**
 * @typedef {{ someKey: unknown, ... }} SomeType
*/

/**
 * Some description for function
 * @param {string} arg1
 * @returns {}
 * @throws
 * @variant
*/
async function some_name(arg1, arg2): SomeType { return; };

// arg1: { someKey: someValue }
// some_output: any
// arg2: string | Error
```