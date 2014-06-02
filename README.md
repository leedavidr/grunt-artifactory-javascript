grunt-artifactory-javascript
============================

Use your private artifactory to host javascript dependencies

1. Define dependencies in a file (e.g. dependencies-js-local.json)
```
{
  "repository": {
    url: 'https://artifactory.yourcompany.com',
    repository: 'js-local',
    username: 'test',
    password: 'test'
  },
  "dependencies": {
    "com.yourcompany.js:angular": "0.0.0",
    "com.yourcompany.js:custom": "0.1.0"
  }
}
```

2. Define task in package.json
```
  ...

  "artifactoryJavascript": {
    files: ['dependencies-js-local.json', 'dependencies-js.json']
  }

  ...
```

Forked from https://github.com/leedavidr/grunt-artifactory which is forked from https://github.com/RallySoftware/grunt-nexus-artifact
