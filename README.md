# abc
> Web uygulamaları geliştirmek için daha iyi bir Deno framework'ü.

[![tag](https://img.shields.io/github/tag/zhmushan/abc.svg)](https://github.com/zhmushan/abc)
[![Build Status](https://github.com/zhmushan/abc/workflows/ci/badge.svg?branch=master)](https://github.com/zhmushan/abc/actions)
[![license](https://img.shields.io/github/license/zhmushan/abc.svg)](https://github.com/zhmushan/abc)
[![tag](https://img.shields.io/badge/deno->=1.0.0-green.svg)](https://github.com/denoland/deno)
[![tag](https://img.shields.io/badge/std-0.98.0-green.svg)](https://github.com/denoland/deno)

## Merhaba dünya

```ts
import { Application } from "https://deno.land/x/abc@v1.3.3/mod.ts";

const app = new Application();

console.log("http://localhost:8080/");

app
  .get("/", (c) => {
    return "Merhaba, Abc!";
  })
  .start({ port: 8080 });
```
