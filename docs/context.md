## Context

### Özel Context kullanımı

``abc`` framework'ünde her istek, ``Context`` nesnesi ile işlenir. Ancak bazen ihtiyaçlar ``Context`` sınıfını geliştirmemizi gerektirebilir.
Mesela bir template engine'i bağlamak için aşağıdaki gibi bir ``Context`` sınıfı türetebilirsiniz.

```ts
class CustomContext extends Context {
    public readonly eta : Eta;

    constructor(ctx: Context){
        super(ctx);

        this.eta = new Eta({ views: "templates" });
    } 
}
```

### Middleware ile Özel Context Kullanımı

``pre`` fonksiyonu, bütün HTTP isteklerinden önce çalıştırılan bir mekanizmadır. Bu sayede türettiğiniz ``CustomContext``'i bütün rotalarda kullanabilirsiniz.

```ts
app.pre((next) =>
  (ctx) => {
    return next(new CustomContext(ctx));
  }
);
```

### Kullanım

Artık ``eta`` template engine'e ``CustomContext`` üzerinden erişebilirsiniz:

```ts
app
  .get("/", (ctx: CustomContext) => {
    ctx.eta....
});
```
