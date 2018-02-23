# rehydration-testing-app

This is a test of glimmer-vm's rehydration/serialization in an ember.js application:

The steps to try this out on your own are as follows:

- download the ember-source tarbal:
  `curl https://github.com/rondale-sc/rehydration-testing-app/raw/master/ember-source-3.2.0-utilize-rehydration-serialization-from-glimmer.tgz -O`
- link that to your ember-source in your application's package.json

  ```json
    "ember-source": "./ember-source-3.2.0-utilize-rehydration-serialization-from-glimmer.tgz",
  ```
- list `ember-cli-fastboot` to your dependencies:

  ```json
  "dependencies": {
    "ember-cli-fastboot": "github:rondale-sc/ember-cli-fastboot#utilize-rehydration-serialization-from-glimmer"
  }
  ```
- start your application with `EXPERIMENTAL_RENDER_MODE_SERIALIZE=true ember s`

View your devtools network panel to ensure you have the glimmer-vm's serialization markings.  And ensure you have no script tags with the ids `fastboot-body-start` or `fastboot-body-end`.
