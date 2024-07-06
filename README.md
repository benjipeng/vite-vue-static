# Vue 3 + Vite

`pnpm` is used as a package mgr.

refer to `.github/workflows/gh-pages.yml`

```yaml
steps:
  - name: Checkout
    uses: actions/checkout@v4
  - uses: pnpm/action-setup@v4
    with:
      version: 8
  - name: Set up Node
    uses: actions/setup-node@v4
    with:
      node-version: 20
      cache: "pnpm"
  - name: Setup pnpm
    run: npm install -g pnpm
  - name: Install dependencies
    run: pnpm install --frozen-lockfile
  - name: Build
    run: pnpm run build
```
