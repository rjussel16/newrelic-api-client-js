# newrelic-api-test-js [![Build Status](https://travis-ci.org/kenahrens/newrelic-api-client-js.svg?branch=master)](https://travis-ci.org/kenahrens/newrelic-api-client-js)
JavaScript library to test connectivity to New Relic API

# How to use
This is just a simple library to test connectivity between NodeJS and New Relic API.

### Initial Setup
Clone the repository and run npm install which should install dependencies into node_modules
```
kahrens@kenbook8u:~/dev/node$ git clone https://github.com/kenahrens/newrelic-api-test-js.git
...
kahrens@kenbook8u:~/dev/node$ cd newrelic-api-test
kahrens@kenbook8u:~/dev/node/newrelic-api-test$ npm install
```

### Environment Variables
Set 4 environment variables to the correct values for your account (verify with [API Keys](https://rpm.newrelic.com/apikeys)))
* NEWRELIC_ACCOUNT_ID - you will also see this in the URL bar
* NEWRELIC_REST_API_KEY - overall REST Key (legacy)
* NEWRELIC_ADMIN_API_KEY - specific Admin user API Key, used for certain API calls
* NEWRELIC_INSIGHTS_QUERY_KEY - there are keys just for Insights in the Manage Data section

### Execute Tests
You can also run the test cases which is a way to double check things are configured properly.
```
kahrens:newrelic-api-client-js kahrens$ npm test

> newrelic-api-test@0.0.1 test /Users/kahrens/Documents/github/newrelic-api-client-js
> ./node_modules/mocha/bin/mocha



  New Relic API Test
    ✓ calls the applications api (293ms)
    ✓ gets a specific application (183ms)
    ✓ gets the metricNames for a specific application (282ms)
    ✓ gets the metricData for a specific application (225ms)
    ✓ gets the hosts for a specific application (212ms)
    ✓ gets the instances for a specific application (210ms)
    ✓ calls the mobile api (212ms)
    ✓ calls the browser api (412ms)
    ✓ calls the keyTransactions api (178ms)
    ✓ calls the servers api (188ms)
    ✓ calls the usages api for apm (193ms)
    ✓ calls the users api (167ms)
    ✓ calls the plugins api (227ms)
    ✓ gets the component for a specific plugin (292ms)

  New Relic Insights API Test
    ✓ calls the query api (272ms)

  New Relic Synthetics API Test
    ✓ calls the synthetics api (673ms)


  16 passing (4s)
```
