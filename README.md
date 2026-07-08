# Cat Ideal Weight Core

[![CI](https://github.com/xiongxingzhe/cat-ideal-weight-core/actions/workflows/ci.yml/badge.svg)](https://github.com/xiongxingzhe/cat-ideal-weight-core/actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Utilities for comparing current cat weight against a target range in kilograms.

Built by [pawsandpounds.com](https://pawsandpounds.com).

## Installation

```bash
npm install cat-ideal-weight-core
```

## Quick Start

```ts
import { compareToIdealKg } from "cat-ideal-weight-core"

const range = { minKg: 3.5, maxKg: 4.5 }

compareToIdealKg(3.1, range) // "below"
compareToIdealKg(4.0, range) // "within"
compareToIdealKg(5.2, range) // "above"
```

## API

### `compareToIdealKg(currentKg: number, range: { minKg: number; maxKg: number }): "below" | "within" | "above"`

- `below` if `currentKg < minKg`
- `within` if in range
- `above` if `currentKg > maxKg`

Throws if `currentKg <= 0`.

## License

MIT
