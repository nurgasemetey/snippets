###  Cannot find name 'expect jest


 [Cannot find name 'expect' · Issue #1068 · kulshekhar/ts-jest](https://github.com/kulshekhar/ts-jest/issues/1068 "Cannot find name 'expect' · Issue #1068 · kulshekhar/ts-jest")




```json
Have you guys ever add a jest type in types section in the tsconfig.json:

{
  "compilerOptions": {
    // ...
    "types": ["node", "jest"],
    // ...
  }
}
First you need to intall jest types by yarn add @types/jest -D.
```

