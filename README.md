name: E2E Tests

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  tests:

    runs-on: ubuntu-latest
    steps:
    - name: Get code
    - uses: actions/checkout@v4
    - name: Use Node.js 20
      uses: actions/setup-node@v4
      with:
        node-version: 20

    - name: Setup Python 
    uses: actions/setup-python@v5.1.1
    with:
        python-version: 3.12
