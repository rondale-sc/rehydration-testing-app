# rehydration-testing-app

This is a test of glimmer-vm's rehydration/serialization in an ember.js application:

The steps to try this out on your own are as follows:

- Link to this tarbal of ember canary:

  ```json
    "ember-source": "https://s3.amazonaws.com/builds.emberjs.com/canary/shas/e0d4b3fba4fd9c5ae6d9c61f18055d99e1989265.tgz",
  ```

- list `ember-cli-fastboot` to your dependencies:

  ```json
  "dependencies": {
    "ember-cli-fastboot": "github:rondale-sc/ember-cli-fastboot#37d1f2176fe5ab1ca96870c9c65012f8a98f1552"
  }
  ```
- start your application with `EXPERIMENTAL_RENDER_MODE_SERIALIZE=true ember s`

View your devtools network panel to ensure you have the glimmer-vm's serialization markings.  And ensure you have no script tags with the ids `fastboot-body-start` or `fastboot-body-end`.
