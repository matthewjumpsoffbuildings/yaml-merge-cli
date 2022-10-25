# yaml-merge-cli

### Fork of [merge-yaml-cli](https://www.npmjs.com/package/merge-yaml-cli)

Forked to update dependencies by [@vuk](https://github.com/vuk/merge-yaml-cli), renamed to `yaml-merge-cli` to deploy to npm

Merges YAML files together using [glob](https://www.npmjs.com/package/glob) patterns to specify input files, with a CLI to
write out the result as a file.

#### Global Usage

```shell
npm i -g yaml-merge-cli
merge-yaml -i example.yaml includes/*.yml -o merged.yml
```

#### Npx Usage

```shell
npm i -D yaml-merge-cli
npx merge-yaml -i example.yaml includes/*.yml -o merged.yml
```

#### Node.js API

```
const mergeYaml = require('merge-yaml-cli')

mergeYaml.on('files', console.log('Files found: ', files))

const result = mergeYaml.merge(['example.yml', 'includes/*.yml'])
```

#### Tests

The repo contains one simple test case. `tests/base.yml` is merged with `includes/*.yml` and the output is compared with `expected.yml`.

The test can be run with `yarn test` or `npm test` but requires Docker and Docker Compose to be installed.
