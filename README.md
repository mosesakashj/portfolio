# portfolio

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Build Update Commands for Github Pages
```
(Remove dist directory from git ignore file)

npm run build
git add dist
git commit -m 'adding dist subtree'
git subtree push --prefix dist origin gh-pages
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
