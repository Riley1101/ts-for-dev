---
sidebar_position: 2
---

# Benefits of Typescript

As I mentioned earlier, Typescript is a super set of Javascript. It means that all the Javascript code is valid Typescript code. The benefit here is you can just learn incrementally as you go.

## Typescript configs

Let's go a head and try run the code below in our project.

```ts title='index.ts'
/**
 * Add two numbers
 * @param a first number
 * @param b second
 */
export async function addNumbers(a: number, b: number) {
  await timeout(500);
  return a + b;
}
```
