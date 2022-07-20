Problem: Can't import the named export 'ApplicationRef' from non EcmaScript module (only default export is available)
Solution: Update webpack config 
```
const config = {
  mode: 'production', // "production" | "development" | "none"
  resolve: {
    extensions: ['*', '.mjs', '.js', '.json']
  },
  module: {
    rules: [
      {
        test: /\.mjs$/,
        include: /node_modules/,
        type: 'javascript/auto'
      }
    ]
  }
}
```

Taken from: https://stackoverflow.com/a/69343125/2527950
