# SupportKit Javascript SDK

### 1. Installation
* ```npm install```
* ```sudo npm install -g grunt```
* ```grunt --help``` to see the list of available tasks

### 2. Essential Grunt Tasks

* ```grunt build``` dumps a plain and a minified file from all files in the folder ```src``` into the folder ```dist```.
* ```grunt clean``` removes all files in the folder ```dist```.
* ```grunt test``` runs karma tests

SupportKit.init('abcdefghijxlmnop', {
    id: 'abcd1234',
    givenName: 'Andrew',
    surname: 'Lavers'
}, function(user) {
    <-- user.id
    user.sendMessage('Hello');
});

// Set an appUserId cookie?

### 3. Deployment

Create the file `grunt-aws.json`:

```
{
    "key": "...",
    "secret": "...",
    "bucket": "..."
}
```

Then

```
grunt deploy
```

### 4. Publishing

* Create environment variables GITHUB_USERNAME and GITHUB_PASSWORD with credentials that have access to the github repo
* Ensure you have the branch master checked out and up to date with NO WORKING DIRECTORY CHANGES (don't worry, I won't let you publish even if you mess up)
* Ensure you have release notes created in the folder release_notes
* Run the following task

```grunt publish:(major | minor | patch | x.y.z)```

## Web References

### Thanks

Project was generated from https://github.com/monbro/generator-javascript-sdk-boilerplate

### Tutorials to build a SDK

* http://msdn.microsoft.com/en-us/library/jj820239.aspx

### How others do it:

* https://github.com/apigee/apigee-javascript-sdk/blob/master/apigee.js
* https://github.com/stackmob/stackmob-js-sdk/blob/master/stackmob.js
* https://github.com/gilt/gilt-js-sdk/blob/master/gilt-js-api.js
* https://github.com/BuddyPlatform/Buddy-JS-SDK/blob/master/buddy.js
* https://github.com/EdmundsAPI/sdk-javascript/blob/master/edmunds.api.sdk.js
* https://github.com/justintv/twitch-js-sdk/blob/master/twitch.js
* https://github.com/aws/aws-sdk-js/blob/master/dist/aws-sdk.js
* https://github.com/Instagram/instagram-javascript-sdk/blob/master/ig.js
* https://github.com/splunk/splunk-sdk-javascript/blob/master/client/splunk.js

### Final usage examples

* https://keen.io/docs/clients/javascript/usage-guide/ with https://dc8na2hxrj29i.cloudfront.net/code/keen-2.1.0-min.js
* https://developers.facebook.com/docs/javascript/quickstart/v2.0 with https://connect.facebook.net/en_US/sdk.js
* https://parse.com/docs/js_guide with www.parsecdn.com/js/parse-1.2.18.min.js

### Helpful sites

* http://blog.ponyfoo.com/2014/01/27/my-first-gulp-adventure
* http://regex101.com/
