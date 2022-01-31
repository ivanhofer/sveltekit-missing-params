# sveltekit missing params if route contains errors

1. start dev server
   ```bash
	npm run dev
	```
2. open `http://localhost:3000/test/works` in your browser\
   You should see that `[slug]` is set to `'test'`
3. open `http://localhost:3000/test/has-error` in your browser\
   This route contains an error and `[slug]` is `undefined`
