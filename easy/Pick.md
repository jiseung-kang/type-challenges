# [Pick](https://github.com/type-challenges/type-challenges/blob/main/questions/00004-easy-pick/README.md)

My Code:

```ts
type MyPick<T, K extends keyof T> = { [Key in K]:T[Key] }
```
