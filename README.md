# example of issue with shadow

To replicate:

- `npm install`
- `npm run watch`


On my machine I get:

```
> shadow-example@0.0.1 watch
> shadow-cljs watch frontend

shadow-cljs - config: /home/ru/Projects/shadow-example/shadow-cljs.edn
shadow-cljs - HTTP server available at http://localhost:3000
shadow-cljs - server version: 2.11.18 running at http://localhost:9630
shadow-cljs - nREPL server started on port 8777
shadow-cljs - watching build :frontend
[:frontend] Configuring build.
[:frontend] Compiling ...
[:frontend] Build failure:
The required JS dependency "readable-stream/writable.js" is not available, it was required by "node_modules/stream-browserify/index.js".

Dependency Trace:
        shadow_example/core.cljs
        node_modules/bugout/index.js
        node_modules/bs58check/index.js
        node_modules/create-hash/browser.js
        node_modules/cipher-base/index.js
        node_modules/stream-browserify/index.js

Searched for npm packages in:
        /home/ru/Projects/shadow-example/node_modules

See: https://shadow-cljs.github.io/docs/UsersGuide.html#npm-install
```
