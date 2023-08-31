### create repo on github under personal repository
### add Dockerfile to repository
### go to action menu, choose "Publish Docker Container"

### change this configuration
```
on:
  schedule:
    - cron: '45 6 * * *'
  push:
    branches: [ "main" ]
    # Publish semver tags as releases.
    tags: [ 'v*.*.*' ]
  pull_request:
    branches: [ "main" ]
```

### to 

```
on:
  push:
    tags: [ 'v*.*.*' ]
```