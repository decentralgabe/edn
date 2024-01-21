# @transmute/edn-graph

[![CI](https://github.com/transmute-industries/edn-graph/actions/workflows/ci.yml/badge.svg)](https://github.com/transmute-industries/edn-graph/actions/workflows/ci.yml)
![Branches](./badges/coverage-branches.svg)
![Functions](./badges/coverage-functions.svg)
![Lines](./badges/coverage-lines.svg)
![Statements](./badges/coverage-statements.svg)
![Jest coverage](./badges/coverage-jest%20coverage.svg)

<!-- [![NPM](https://nodei.co/npm/@transmute/edn-graph.png?mini=true)](https://npmjs.org/package/@transmute/edn-graph) -->

🚧 Experimental 🔥

<img src="./transmute-banner.png" />

#### [Questions? Contact Transmute](https://transmute.typeform.com/to/RshfIw?typeform-source=edn-graph)

## Usage

```bash
npm i @transmute/edn-graph --save
```

```ts
import * as edn from "@transmute/edn-graph";
const document: edn.EDNCoseSign1 = await edn.parse(
  Buffer.from("D28444A1013822A1044...02E9D91E9B7B59622A3C", "hex")
  // or "18([h'A1013822', {4: h'5 ...
)
const alg = document.signatureAlgorithm();
expect(alg.value).toBe(-35);
expect(alg.comment).toBe("ECDSA with SHA-384");
// use the parsed abstract syntax tree for
// CBOR Extended Diagnostic Notation (EDN)
// to build custom diagnostic renderers
// TODO: https://github.com/transmute-industries/vscode-scitt-preview
```

## Develop

```bash
npm i
npm t
npm run lint
npm run build
```
