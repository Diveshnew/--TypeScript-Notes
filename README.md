# TypeScript-Learning

## 1.Getting Started

KeyTerms to Remember in this section:
```
Dynamically-typed Languages
IntelliSense
Refactoring
Source maps
Statically-typed Languages
Transpiling
Type safety
```

Programming languages divide into two categories: `statically-typed` and `dynamically-typed.`
In statically-typed languages `(eg C++, C#, Java, etc)`, the type of variables is set at 
`compile-time` and cannot change later.

In dynamically-typed languages `(eg Python, JavaScript, Ruby)`, the type of variables is 
determined at `run-time` and can change later.
TypeScript is essentially `JavaScript with static typing` and some additional features that 
help us write more concise and robust code.

Most IDEs and code editors supporting TypeScript provide incredible `IntelliSense and 
auto-completion`. So we get active hints as we code. A great productivity booster!
By providing type information in our code, we get better `refactoring` support in most 
IDEs and code editors.
`Refactoring` means changing the structure of the code without changing its behavior. 
With TypeScript we can `catch more bugs` at `compile time.`

`Browsers` don’t understand TypeScript code. So we need to use the TypeScript compiler 
to `compile and translate` (or transpile) our TypeScript code into regular JavaScript for 
execution by browsers.

`Source maps` are files that represent the mapping between TypeScript and JavaScript 
code. They’re used for debugging.
We can configure the TypeScript compiler by enabling/disabling various settings in `tsconfig.json`

#

## 2. Fundamentals

Since TypeScript is a `superset` of JavaScript, it includes all the `built-in types` in 
JavaScript `(eg number, string, boolean, object, etc)` as well as additional types `(eg any, 
unknown, never, enum, tuple, etc).`

In TypeScript, we set the type of our variables by `annotating` them.
The `any type` can represent any kind of value. It’s something we should avoid as much 
as possible because it defeats the purpose of using TypeScript in the first place. A 
variable of type `any` can take any kind of value!

`Tuples` are fixed-length arrays where each element has a `specific type`. We often use 
them for representing two or three related values.
`Enums` represent a list of related constants.

## Cheat Sheet

### `Annotation`
```TypeScript
let sales: number = 123_456_789;
let numbers: number[] = [1, 2, 3];
```

### `Tuples`
```TypeScript
let user: [number, string] = [1, 'Divesh'];
```

### `Enums`
```TypeScript
enum Size {Small = 1, Medium, Large };
```

### `Functions`
```TypeScript
function calculateTax(income: number): number {
  return income * .2;
}
```

### `Objects`
```TypeScript
let employee: {
  id: number;
  name: string;
  retire: (date: Date) => void
} = {
  id: 1,
  name: 'Mosh',
  retire: (date: Date) => {},
};
```

## Compiler Options

| Option              | Description                    |
|---------------------|--------------------------------|
| noImplicitAny       | When enabled, the compiler will warn you about variables that are inferred with the any type. You’ll then have to explicitly annotate them with any if you have a reason to  do so.|
| noImplicitReturns   | When enabled, the compiler will check all code paths in a function to ensure they return a value. |
| noUnusedLocals      | When enabled, the compiler will report unused local variables.|
| noUnusedParameters  | When enabled, the compiler will report unused parameters.|
