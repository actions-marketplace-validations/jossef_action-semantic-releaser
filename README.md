**Need an introduction to Semantic Release?** [check this out](https://blog.greenkeeper.io/introduction-to-semantic-release-33f73b117c8) 

#Semantic Releaser GitHub Action
Simple Usage. No files needed. Language Independent.


### Getting Started
Add this step to your action file

```yaml
- name: Semantic Releaser
  uses: jossef/action-semantic-releaser@v1
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Full example

```yaml
name: CI
on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Semantic Releaser
        uses: jossef/action-semantic-releaser@v1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```