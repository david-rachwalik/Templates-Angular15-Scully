# Angular Template (Base)

## Web App ([repo](https://github.com/david-rachwalik/Templates-Angular15-Base))

Template baseline for Angular v15 web application

### Primary Actions Taken

- Reorganized initial file directory structure
  - move `favicon.ico` into the `assets` directory
  - update `angular.json` so "build.options.assets" and "test.options.assets" are just `["src/assets"]` (remove favicon.ico)
  - update `index.html` link from `favicon.ico` to `assets/favicon.ico`
  - move `styles.scss` to `styles/index.scss`
  - update `angular.json` for "build.options.styles" and "test.options.styles"
- update `angular.json` so "projects.\*.schematics.@schematics/angular:component" has `"displayBlock": true`
- update `angular.json` so "projects.\*.architect.build.options" has `"stylePreprocessorOptions": { "includePaths": ["src/styles"] }`

### Project Commands Used

Generate a new Angular application ([tutorial](https://angular.io/tutorial/toh-pt5), [layouts](https://indepth.dev/posts/1235/how-to-reuse-common-layouts-in-angular-using-router-2), [RxJS](https://www.learnrxjs.io))

```bash
ng new <app-name>
```

---

[Default Angular component css display block](https://stackoverflow.com/questions/51032328/angular-component-default-style-css-display-block) (generated components will contain css `:host { display: block; }`)

```json
...
// Set default value in angular.json (Angular v9.1+)
"projectType": "application",
"schematics": {
  "@schematics/angular:component": {
    "displayBlock": true
  }
}
...
```

### Angular Generate Commands Used

Generate a new Angular component

```bash
ng g c <component-name>
```

Generate a new Angular module

```bash
ng g m <module-name>
```
