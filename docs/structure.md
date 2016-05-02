# Project Structure

``` bash
.
├── build/                      # files for global usage of component
│   └── ...
├── src/
│   ├── index.js                # the component
├── static/                     # default gh-pages content
├── test/                       # unit tests
│   ├── index.js                # test build entry file
│   └── karma.conf.js           # test runner config file
├── .babelrc                    # babel config
├── .eslintrc.js                # eslint config
└── package.json                # build scripts and dependencies
```


### `build/`

### `src/`

### `test/`

Contains unit test related files. See [Unit Testing](unit.md) for more details.

### `package.json`

The NPM package meta file that contains all the build dependencies and [build commands](commands.md).
