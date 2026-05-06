# dataset-drc14

Prerouted DRC dataset package for tscircuit experiments.

This dataset is intentionally plain JavaScript so it can be installed directly from GitHub.

## Structure

- `index.js` is the package entrypoint.
- `index.d.ts` contains lightweight TypeScript declarations.
- `samples/` contains the JSON samples.
- No transpilation step is used.
- Do not create an `index.ts` file.
- Do not publish this package to npm.

## Adding Samples

Move JSON files into `samples/` using two-digit or three-digit ordered names such as:

```txt
samples/sample001.json
samples/sample002.json
samples/sample003.json
```

Then update `index.js` and `index.d.ts` to export them:

```js
import sample001 from "./samples/sample001.json"
import sample002 from "./samples/sample002.json"
import sample003 from "./samples/sample003.json"

export { sample001, sample002, sample003 }

export const samples = [sample001, sample002, sample003]
export default samples
```

Keep numbering increasing from the last known dataset and use leading zeroes.
