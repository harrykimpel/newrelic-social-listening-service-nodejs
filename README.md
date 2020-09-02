[![Community Project header](https://github.com/newrelic/opensource-website/raw/master/src/images/categories/Experimental.png)](https://opensource.newrelic.com/oss-category/#experimental)

# Social Listening Service ![lint & test](https://github.com/newrelic-experimental/newrelic-social-listening-service-nodejs/workflows/continuous%20integration/badge.svg)

>[Brief description - what is the project and value does it provide? How often should users expect to get releases? How is versioning set up? Where does this project want to go?]

 Social Listening Service is an app that listens to data from social platforms (currently only Twitter is supported) and analyses sentiment of natural language data that it listens to.
 It also automatically sends sentiment data to (your) New Relic account where it can be easily charted.
 In combination with New Relic [Dashboards](https://docs.newrelic.com/docs/query-your-data/explore-query-data/dashboards/introduction-new-relic-one-dashboards) it creates a powerful tool that shows sentiment of your audience in reaction to events that you want to track - like certain words, phrases, hashtags etc.

## Installation

#### Prerequisites 

Before running the app you will need:
 - New Relic [Free Account](https://newrelic.com/signup) (at least free tier account is needed)
    - New Relic [Insert API Key](https://docs.newrelic.com/docs/apis/get-started/intro-apis/types-new-relic-api-keys#event-insert-key)
    - New Relic Metric endpoint url - depending on the region of your New Relic account it will be:
        - `metric-api.newrelic.com` - for US
        - `metric-api.eu.newrelic.com` - for EU
 - Twitter [Developer Account](https://developer.twitter.com/en/apply-for-access)
    - Twitter [Bearer Token](https://developer.twitter.com/en/docs/authentication/oauth-2-0/bearer-tokens)
 
Once the tokens are ready create a `.env` file in the root directory and place all your keys there.
 - see the example of the `.env` file under `examples/.env` or just click [this link](https://github.com/newrelic-experimental/newrelic-social-listening-service-nodejs/blob/main/examples/.env)
 - alternatively you can include all the `env vars` from the example using `process.env` object of your environment of choice

#### Installation and App start

Assuming the repository is cloned and the `.env` file is ready:
 - run `npm install` (or `yarn install`)
 - run the app:
   - `npm run dev:start` or
   - `npm run docker:dev:start` - if you want it to run in a Docker container

 Running the app in production mode:
 - install `pm2` package manager globally on your box or use provided Docker container
 - run `npm install` - to install node modules
 - run `npm run build` - to transpile typescript code to ES6
 - run `npm start` - to start the app using `pm2` package manager module
 - read on how to manage your app with `pm2` [here](https://pm2.keymetrics.io/docs/usage/process-management/)

## Getting Started
>[Simple steps to start working with the software similar to a "Hello World"]

## Usage
>[**Optional** - Include more thorough instructions on how to use the software. This section might not be needed if the Getting Started section is enough. Remove this section if it's not needed.]


## Building

>[**Optional** - Include this section if users will need to follow specific instructions to build the software from source. Be sure to include any third party build dependencies that need to be installed separately. Remove this section if it's not needed.]

## Testing

In order to run test simply run `npm test`
 - it will run `unit` test as well as `integration` tests
 - it will log all the test results to the console
 - it will display test `coverage report` after all tests are run
 - it uses `jest` 
 
`E2E` tests are not included in this version yet.

## Support

New Relic hosts and moderates an online forum where customers can interact with New Relic employees as well as other customers to get help and share best practices. Like all official New Relic open source projects, there's a related Community topic in the New Relic Explorers Hub. You can find this project's topic/threads here:

>Add the url for the support thread here

## Contributing
We encourage your contributions to improve [project name]! Keep in mind when you submit your pull request, you'll need to sign the CLA via the click-through using CLA-Assistant. You only have to sign the CLA one time per project.
If you have any questions, or to execute our corporate CLA, required if your contribution is on behalf of a company,  please drop us an email at opensource@newrelic.com.

## License
[Project Name] is licensed under the [Apache 2.0](http://apache.org/licenses/LICENSE-2.0.txt) License.
>[If applicable: The [project name] also uses source code from third-party libraries. You can find full details on which libraries are used and the terms under which they are licensed in the third-party notices document.]
