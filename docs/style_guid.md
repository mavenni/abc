# Abc Sitil Rehberi
## Adlandırma

- Tür isimleri için PascalCase kullanın.
- Enum değerleri için PascalCase kullanın.
- Global değişkenler için PascalCase kullanın.
- Fonksiyon isimleri için camelCase kullanın.
- Özellik isimleri ve mahallî (yerel) değişkenler için camelCase kullanın.

```ts
// Kötü
export type myType = string;

// İyi
export type MyType = string;
```
```ts
// Kötü
enum Color {
  RED,
  BLACK,
}

// İyi
enum Color {
  Red,
  Black,
}
```

```ts
// Kötü
export function notFoundHandler(_?: Context): never {
  throw new Error();
}

// İyi
export function NotFoundHandler(_?: Context): never {
  throw new Error();
}
```

```ts
// Kötü
export function NotFoundHandler(flag: boolean): void | never {
  if (flag) {
    throw new Error();
  }
}

// İyi
export function notFoundHandler(flag: boolean): void | never {
  if (flag) {
    throw new Error();
  }
}
```

```ts
// Kötü
const GLOBAL_CONFIG = {};

// İyi
const GlobalConfig = {};
```

## `null` & `undefined`
- Her zaman `undefined` kullanın.
