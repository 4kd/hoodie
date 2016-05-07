# hoodie

> A generic backend with a client API for Offline First applications

[![Build Status](https://travis-ci.org/hoodiehq/hoodie.svg?branch=master)](https://travis-ci.org/hoodiehq/hoodie)
[![Dependency Status](https://david-dm.org/hoodiehq/hoodie.svg)](https://david-dm.org/hoodiehq/hoodie)
[![devDependency Status](https://david-dm.org/hoodiehq/hoodie/dev-status.svg)](https://david-dm.org/hoodiehq/hoodie#info=devDependencies)

<a href="http://hood.ie/animals/#low-profile-dog"><img src="https://avatars1.githubusercontent.com/u/1888826?v=3&s=200"
 alt="The Low-Profile Dog Hoodie Mascot" title="The Low-Profile Dog Hoodie Mascot" align="right" /></a>

Hoodie lets you build apps [without _thinking_ about the backend](http://nobackend.org/)
and makes sure that they work great [independent from connectivity](http://offlinefirst.org/).

This is Hoodie’s main repository. It starts a server and serves the client API.
Read more about [how things work](lib).

A good place to start is our [Tracker App](https://github.com/hoodiehq/hoodie-app-tracker).
You can play around with Hoodie’s APIs in the browser console and see how it
works all together in its [simple HTML & JavaScript code](https://github.com/hoodiehq/hoodie-app-tracker/tree/master/public).

If you have any questions come say hi in our [chat](http://hood.ie/chat/).

## Setup

`npm install --save hoodie`

<!--
  TODO: automate package.json update using postinstall
        https://twitter.com/boennemann/status/726579520661282817
-->
Add this to your `package.json`:

```json
"scripts": {
  "start": "hoodie"
}
```

Now run `npm start` to start your Hoodie app.

## Usage

Run `npm start -- --help` to see all available CLI options.

Options can also be specified as environment variables (prefixed with `hoodie_`) or inside a `.hoodierc` file (json or ini).

option        | default       | description
------------- | ------------- | -------------
loglevel      | `'warn'`      | One of: error, warn, info, verbose, silly
port          | `8080`        | Port-number to run the Hoodie App on
bindAddress   | `'127.0.0.1'` | Address that Hoodie binds to
public        | `'public'`    | path to static assets
inMemory      | `false`       | Whether to start the PouchDB Server in memory
dbUrl         | –             | If provided, uses external CouchDB. URL has to contain credentials.
data          | `'.hoodie'`   | Data path

Hoodie is using the [rc](https://www.npmjs.com/package/rc) module to retrieve
configuration from CLI arguments, environment variables and configuration files.

## Testing

Local setup

```
git clone https://github.com/hoodiehq/hoodie.git
cd hoodie
npm install
```

The `hoodie` test suite is run with `npm test`.
You can [read more about testing Hoodie](test).

You can start hoodie for itself using `npm start`. It will  serve the contents
of the [public folder](public).

## License

[Apache 2.0](LICENSE)
