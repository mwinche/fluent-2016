Using npm for other stuff
=========================

[Slides](http://slides.com/seldo/fluent-many-uses-of-npm#/)

npm is:

1. a CLI
2. a registry
3. a website
4. a community

npm, inc. was founded so that npm would work forever.

npm's goal: reduce developer friction

npm is not (very) opinionated

~/.npm-init.js and PromZard can take over control of npm init and let you do pretty much whatever

optional dependency: fallback for windows as an example (won't fail if the optional dependency fails to build)

--save-bundle, bundled dependencies, including in its tarball so it doesn't have to download dependencies

offline installs (global cache), use npm --cache-min 999999 (skips all network, relies completely on cache)

npm publish --access=restricted

npm version major -m "bump to version %s" (%s = name of version)

npm owner (manage access to the package)

npm organizations/team/access (paid features, more fine grained access)

shrinkwrap application but not the modules within the application

npm dedupe, npm prune (can do instead of blowing away node_modules)

npm link is used by npm folks

npm outdated (preview of what npm update would do)

dist tags help remove friction

npm deprecate (warns if anyone tries to install that version)

lifecycle hooks: publish install, uninstall, version, test, stop, start, restart

Tools:
* Less, Sass and CSS
* Babel
* Webpack and Browserify
* standard and eslint
* http://sethvincent.com/css-via-npm
* semantic-release
* npm On-Site (paid enterprise thing, can whitelist what it proxies)
* greenkeeper.io
* Node Security Project (npm install nsp)
* Snyk and BitHound
* Tonic (tonicdev.com)
