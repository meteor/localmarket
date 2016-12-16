Local Market
============

Local Market is an open source app powered by Meteor and made by [Percolate Studio](http://percolatestudio.com). In this example app we explore intermediate techniques:

  - Using a sample database to generate lists and items
  - Integrating OAUTH with Meteor's accounts-ui package
  - Cordova integration to use device phone and GPS
  - Mobile UI & UX
  
## Configuring Twitter

By default, Local Market comes configured with credentials for a shared Twitter app. You can also use credentials for your own Twitter application. Here's how:

1. Register your application on Twitter:
  1. Sign in and create your app on [Twitter's App Dashboard](https://apps.twitter.com/apps/new)
  2. Set Callback URL to anything, but don't keep it blank. (Meteor apps use OAuth 1.0a, which doesn't require setting this field)
  3. In the "Settings" tab, enable "Allow this application to be used to Sign in with Twitter"
  4. In the "Permissions" tab, give the app "Read and Write" access.

2. Configure your Twitter credentials in your Meteor app:
  1. Go to the "Keys and Access Tokens" tab.
  2. Create a `settings.json` file that **won't be in source control** with the following contents:

  ```js
  {
    "twitter": {
      "consumerKey": "<Copy value from Consumer Key (API Key)>",
      "secret": "<Consumer Secret (API Secret)>"
    }
  }
  ```

3. Now you can run or deploy your copy of Local Market with the `--settings path/to/settings.json` option.
