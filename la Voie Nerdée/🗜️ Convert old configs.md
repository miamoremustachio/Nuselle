The `FlatCompat` utility helps convert old-style configs into the new flat config format.

1. Install latest version of ESLint:

```bash
npm init @eslint/config@latest
```

2. Install all dependencies:

```bash
npm install --save-dev eslint-config-airbnb-base eslint-plugin-import @eslint/eslintrc
```

3. Edit `eslint.config.mjs`:
![[eslint.config.mjs]]

1. Run ESLint:

```bash
npx eslint .
```




[^1]: Sources:
	[https://chatgpt.com/](https://chatgpt.com/)
	[https://eslint.org/docs/latest/use/getting-started](https://eslint.org/docs/latest/use/getting-started)
	[https://eslint.org/docs/latest/use/configure/migration-guide#migrate-your-config-file](https://eslint.org/docs/latest/use/configure/migration-guide#migrate-your-config-file)
