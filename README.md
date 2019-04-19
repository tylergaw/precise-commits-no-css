# precise-commits doesn't seem to recognize formatting issues in `css` files

### Issue

[style.css](style.css) has incorrect formatting. `precise-commits` does not correct the formatting.

### Steps

1. Make a change to [style.css](style.css)
2. Stage the change with `git add style.css`
3. Run `yarn precise-commits`

```
# yarn precise-commits
yarn run v1.15.2
$ precise-commits
✔  precise-commits: 1 modified file(s) found
✔  [1/1] Processing file: style.css
ℹ        --> No formatting changes required in: style.css
✔  Formatting complete 🎉
```

### Expectation
I would expect precise-commits to have found and fixed the formatting issues in `style.css`

## Things I tried
I thought maybe it was a prettier config issue so I tried adding:

```
"prettier": {
  "files": "*.css"
}
```

to `package.json`

That didn't get it so I also tried creating a `.prettierrc` and adding:

```
{
  "files": "*.css"
}
```

Neither of those fixed the issue.
