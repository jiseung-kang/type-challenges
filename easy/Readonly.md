# [Readonly](https://github.com/type-challenges/type-challenges/blob/main/questions/00007-easy-readonly/README.md)

My Code:

```ts
interface Todo {
  title: string;
  description: string;
}

// 이렇게도 지정할 수 있을까?
// type MyReadonly<T> = Readonly<T>

type MyReadonly<T> = { readonly [Key in keyof T]: T[Key] };

const todo: MyReadonly<Todo> = {
  title: "Hey",
  description: "foobar",
};

todo.title = "Hello"; // Error: cannot reassign a readonly property
todo.description = "barFoo"; // Error: cannot reassign a readonly property
```
