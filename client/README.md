# cloudmersive-phishingapi-client

CloudmersivePhishingapiClient - JavaScript client for cloudmersive-phishingapi-client
Easily and directly scan and block phishing security threats in input.
[Cloudmersive Phishing Detection API](https://cloudmersive.com/phishing-detection-api) provides advanced AI phishing detection capabilities.

- API version: v1
- Package version: 2.0.3


## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install cloudmersive-phishingapi-client --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your cloudmersive-phishingapi-client from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('cloudmersive-phishingapi-client')` in javascript files from the directory you ran the last 
command above from.

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/GIT_USER_ID/GIT_REPO_ID
then install it via:

```shell
    npm install GIT_USER_ID/GIT_REPO_ID --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var CloudmersivePhishingapiClient = require('cloudmersive-phishingapi-client');

var defaultClient = CloudmersivePhishingapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix['Apikey'] = "Token"

var api = new CloudmersivePhishingapiClient.PhishingDetectionApi()

var opts = { 
  'body': new CloudmersivePhishingapiClient.AdvancedEmailDetectionRequest() // {AdvancedEmailDetectionRequest} Phishing detection request
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.phishingDetectEmailAdvancedPost(opts, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CloudmersivePhishingapiClient.PhishingDetectionApi* | [**phishingDetectEmailAdvancedPost**](docs/PhishingDetectionApi.md#phishingDetectEmailAdvancedPost) | **POST** /phishing/detect/email/advanced | Perform advanced AI phishing detection and classification against input email.  Analyzes input email as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
*CloudmersivePhishingapiClient.PhishingDetectionApi* | [**phishingDetectFileAdvancedPost**](docs/PhishingDetectionApi.md#phishingDetectFileAdvancedPost) | **POST** /phishing/detect/file/advanced | Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
*CloudmersivePhishingapiClient.PhishingDetectionApi* | [**phishingDetectFilePost**](docs/PhishingDetectionApi.md#phishingDetectFilePost) | **POST** /phishing/detect/file | Perform AI phishing detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.
*CloudmersivePhishingapiClient.PhishingDetectionApi* | [**phishingDetectTextStringAdvancedPost**](docs/PhishingDetectionApi.md#phishingDetectTextStringAdvancedPost) | **POST** /phishing/detect/text-string/advanced | Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
*CloudmersivePhishingapiClient.PhishingDetectionApi* | [**phishingDetectTextStringPost**](docs/PhishingDetectionApi.md#phishingDetectTextStringPost) | **POST** /phishing/detect/text-string | Perform AI phishing detection against input text string.  Returns a clean/not-clean result with confidence level and optional rationale.
*CloudmersivePhishingapiClient.PhishingDetectionApi* | [**phishingDetectUrlAdvancedPost**](docs/PhishingDetectionApi.md#phishingDetectUrlAdvancedPost) | **POST** /phishing/detect/url/advanced | Perform advanced AI phishing detection and classification against an input URL.  Retrieves the URL content, checks for SSRF threats, and analyzes the page with AI deep learning to detect phishing and other unsafe content.  Uses 100-125 API calls.


## Documentation for Models

 - [CloudmersivePhishingapiClient.AdvancedEmailDetectionRequest](docs/AdvancedEmailDetectionRequest.md)
 - [CloudmersivePhishingapiClient.AdvancedUrlDetectionRequest](docs/AdvancedUrlDetectionRequest.md)
 - [CloudmersivePhishingapiClient.PhishingDetectionAdvancedRequest](docs/PhishingDetectionAdvancedRequest.md)
 - [CloudmersivePhishingapiClient.PhishingDetectionAdvancedResponse](docs/PhishingDetectionAdvancedResponse.md)
 - [CloudmersivePhishingapiClient.PhishingDetectionEmailAdvancedResponse](docs/PhishingDetectionEmailAdvancedResponse.md)
 - [CloudmersivePhishingapiClient.PhishingDetectionResponse](docs/PhishingDetectionResponse.md)
 - [CloudmersivePhishingapiClient.PhishingDetectionTextStringRequest](docs/PhishingDetectionTextStringRequest.md)
 - [CloudmersivePhishingapiClient.PhishingDetectionTextStringResponse](docs/PhishingDetectionTextStringResponse.md)
 - [CloudmersivePhishingapiClient.PhishingDetectionUrlAdvancedResponse](docs/PhishingDetectionUrlAdvancedResponse.md)
 - [CloudmersivePhishingapiClient.UnsafeUrlResult](docs/UnsafeUrlResult.md)


## Documentation for Authorization


### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

