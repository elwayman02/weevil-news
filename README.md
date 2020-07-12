# weevil-news

### Adding an author

In the command line, run the following:

```ember g author author-name```

This creates a new file `author-name.md` in the `authors/` folder.

### Adding an issue

In the command line, run the following:

```ember g tag issue-#```

e.g. "issue-3"

This creates a new file `issue-#.md` in the `tags/` folder.

Then edit the resulting file to change the following fields:

`name` - This should just be the number of the issue, e.g. `3`
`image` - This field will get used for the publication date, e.g. `Sunday, July 12th, 1899`
`imageMeta` - This field will get used for the publication location, e.g. `Valentine, NH`

### Adding an article

In the command line, run the following:

```ember g post "Name of article"```

If you have multiple others, you can specify one with `--author=author-name` in the above command.

This creates a new file `name-of-article.md` in the `content/` folder.

In this file, change the `tag` section from `new` to the Issue you'd like to publish it under (e.g. `issue-3`). 
You can tag an article to appear in multiple issues. 

### Publishing An Issue

It's recommended to prepare an issue as a branch by adding the new issue and all articles to that branch, then making 
a single pull request back into the master branch to release the issue. That way, no one will see any of the in-progress 
work until the issue is ready. You will also be able to see a preview deployment to know how it will look prior to release.

Articles will be sorted in the order they were created, with the most recent listed first. If you want to change the order, 
simply edit the `date` field in each article so that they display in the desired order.

Once changes have been merged to the master branch, they will automatically build and release to the live website.

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/)
* [Yarn](https://yarnpkg.com/)
* [Ember CLI](https://ember-cli.com/)
* [Google Chrome](https://google.com/chrome/)

## Installation

* `git clone <repository-url>` this repository
* `cd weevil-news`
* `yarn install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).
* Visit your tests at [http://localhost:4200/tests](http://localhost:4200/tests).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Linting

* `yarn lint:hbs`
* `yarn lint:js`
* `yarn lint:js --fix`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

### Deploying

Specify what it takes to deploy your app.

## Further Reading / Useful Links

* [ember.js](https://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
