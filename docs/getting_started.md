## Merhaba dünya

``server.ts`` adında bir dosya oluşturun.

```ts
import { Application } from "https://deno.land/x/abc@v1.3.3/mod.ts";

const app = new Application();

app
  .get("/hello", (c) => {
    return "Merhaba, Abc!";
  })
  .start({ port: 8080 });
```

Sunucuyu başlatmak için:

```sh
$ deno run --allow-net server.ts
```
