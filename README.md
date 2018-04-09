# rehydration-testing-app

This is a test of glimmer-vm's rehydration/serialization in an ember.js application:

The steps to try this out on your own are as follows:

- `ember-cli-fastboot` and `fastboot` need to be pinned to `1.1.4-beta.1`
- Link to this tarbal of ember canary

  ```json
    "fastboot": "^1.1.4-beta.1",
    "ember-cli-fastboot": "^1.1.4-beta.1",
    "ember-source": "https://s3.amazonaws.com/builds.emberjs.com/canary/shas/462c33ff573a271edc4bcd907025e190d327f8a6.tgz",
  ```

- start your application with `EXPERIMENTAL_RENDER_MODE_SERIALIZE=true ember s`


View the page source and you should see `<!--%+b:0%-->` tags which are used by glimmer to denote node trees.
```js
<script type="x/boundary" id="fastboot-body-start"></script><!--%+b:0%--><!--%+b:1%--><!--%+b:2%-->`
...
```

Make sure that you don't have an older version of fastboot in your dependencies.
