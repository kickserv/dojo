# Dojo

Dojo is the CSS toolkit that powers Kickserv's front-end design. It's purposefully limited to common components to provide our developers with the most flexibility, and to keep Kickserv uniquely *Kickservy*. It's built with SCSS and available via Bower, so it's easy to include all or part of it within your own project.

[**Read the Dojo documentation**](http://dojo.kickserv.com) to learn more.

_**Heads up!** We love open source, but Dojo is unlikely to add new features that are not used in Kickserv. It's first and foremost our CSS toolkit. We really love to share though, so hopefully that means we're still friends <3._

## Contents

- [Install](#install)
- [Usage](#usage)
- [Documentation](#documentation)
  - [Dependencies](#dependencies)
  - [Running locally](#running-locally)
  - [Publishing](#publishing)
  - [Dojo stats](#dojo-stats)
- [Updating](#updating)
- [Contributing](#contributing)
- [Versioning](#versioning)
- [License](#license)

## Install

### Manually

Download the [latest release](https://github.com/kickserv/dojo/releases/latest) and copy the SCSS files over to your own project. Once your files are in place, jump to the [usage guidelines](#usage) for including Dojo into your own CSS.

### Bower

```
$ bower install dojo-css --save
```

### Things to know

**Hey, Kickservers!** For Kickserv, you'll need to  `cd` into `vendor/assets` and run `bower install` there. Be sure to commit and push all the changes, including the `bower.json` and everything under `bower_components`.

## Usage

Once included, simply `@import` either the master SCSS file, or the individual files as you need them.

```scss
// Example: All of Dojo
@import "dojo-css/scss/dojo";

// Example: Individual files
@import "dojo-css/scss/variables";
@import "dojo-css/scss/mixins";
@import "dojo-css/scss/base";
```

## Documentation

Dojo's documentation is built with Jekyll and published to `http://dojo.kickserv.com` via the `gh-pages` branch.

### Dependencies

You'll need the following installed:

- Latest Jekyll (minimum v2.2.0): `$ gem install jekyll`
- Latest Rouge: `$ gem install rouge`
- Latest Sass: `$ gem install sass`
- Latest Grunt CLI: `$ npm install -g grunt-cli`
- [Node.js and npm](http://nodejs.org/download/)

If you have all those set up, now you can install the dependencies:

```bash
$ npm install
$ npm install autoprefixer-core
$ bower install
```

### Running locally

From the Terminal, start a local Jekyll server:

```bash
$ jekyll serve
```

Open a second Terminal tab to automatically recompile the Sass files, run autoprefixer, and update our [Dojo stats file](#dojo-stats):

```bash
$ grunt watch
```

Alternatively, you can manually run `grunt` and `jekyll serve` when needed.

### Publishing

Use the included Grunt task to generate and publish Dojo's docs to the `gh-pages` branch.

```bash
$ grunt publish
```

This takes the `_site` directory, generates it's own Git repository there, and publishes the contents to the `gh-pages` branch here on Kickserv. Changes are reflected in the hosted docs within a minute or so.

### Dojo stats

When compiling or watching the Sass files, Dojo will automatically generate a `.dojo-stats.md` file. This is tracked in the Git repository to provide us historical and contextual information on the changes we introduce. For example, we'll know when the number of selectors or declarations rises sharply within a single change.

## Updating

Within `bower.json`, update to a new release by changing the version number that follows the `#` in the dependency URL.

```json
{
  "name": "myapp",
  "dependencies": {
    "dojo-css": "x.x.x"
  }
}
```

To pull down the updated package, `cd` into `vendor/assets`, and run `bower install`.

```
$ cd vendor/assets
$ bower install
```

Check in `bower.json` and all changes under `vendor/assets/bower_components`.

## Development

Development of Dojo happens in our primary branch, `master`. For stable versions, see the [releases page](https://github.com/kickserv/dojo/releases). `master` will always be up to date with the latest changes, including those which have yet to be released.

## Versioning

For transparency into our release cycle and in striving to maintain backward compatibility, Dojo is maintained under [the Semantic Versioning guidelines](http://semver.org/). Sometimes we screw up, but we'll adhere to those rules whenever possible.

## License

Created by and copyright Kickserv, Inc. Released under the [MIT license](LICENSE.md).
