# CloudmersivePhishingapiClient.PhishingDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**phishingDetectEmailAdvancedPost**](PhishingDetectionApi.md#phishingDetectEmailAdvancedPost) | **POST** /phishing/detect/email/advanced | Perform advanced AI phishing detection and classification against input email.  Analyzes input email as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
[**phishingDetectFileAdvancedPost**](PhishingDetectionApi.md#phishingDetectFileAdvancedPost) | **POST** /phishing/detect/file/advanced | Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
[**phishingDetectFilePost**](PhishingDetectionApi.md#phishingDetectFilePost) | **POST** /phishing/detect/file | Perform AI phishing detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.
[**phishingDetectTextStringAdvancedPost**](PhishingDetectionApi.md#phishingDetectTextStringAdvancedPost) | **POST** /phishing/detect/text-string/advanced | Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
[**phishingDetectTextStringPost**](PhishingDetectionApi.md#phishingDetectTextStringPost) | **POST** /phishing/detect/text-string | Perform AI phishing detection against input text string.  Returns a clean/not-clean result with confidence level and optional rationale.
[**phishingDetectUrlAdvancedPost**](PhishingDetectionApi.md#phishingDetectUrlAdvancedPost) | **POST** /phishing/detect/url/advanced | Perform advanced AI phishing detection and classification against an input URL.  Retrieves the URL content, checks for SSRF threats, and analyzes the page with AI deep learning to detect phishing and other unsafe content.  Uses 100-125 API calls.


<a name="phishingDetectEmailAdvancedPost"></a>
# **phishingDetectEmailAdvancedPost**
> PhishingDetectionEmailAdvancedResponse phishingDetectEmailAdvancedPost(opts)

Perform advanced AI phishing detection and classification against input email.  Analyzes input email as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```javascript
var CloudmersivePhishingapiClient = require('cloudmersive-phishingapi-client');
var defaultClient = CloudmersivePhishingapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersivePhishingapiClient.PhishingDetectionApi();

var opts = { 
  'body': new CloudmersivePhishingapiClient.AdvancedEmailDetectionRequest() // AdvancedEmailDetectionRequest | Phishing detection request
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.phishingDetectEmailAdvancedPost(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AdvancedEmailDetectionRequest**](AdvancedEmailDetectionRequest.md)| Phishing detection request | [optional] 

### Return type

[**PhishingDetectionEmailAdvancedResponse**](PhishingDetectionEmailAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

<a name="phishingDetectFileAdvancedPost"></a>
# **phishingDetectFileAdvancedPost**
> PhishingDetectionAdvancedResponse phishingDetectFileAdvancedPost(opts)

Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```javascript
var CloudmersivePhishingapiClient = require('cloudmersive-phishingapi-client');
var defaultClient = CloudmersivePhishingapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersivePhishingapiClient.PhishingDetectionApi();

var opts = { 
  'model': "Advanced", // String | 
  'customPolicyId': "customPolicyId_example", // String | 
  'inputFile': "/path/to/file.txt" // File | 
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.phishingDetectFileAdvancedPost(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **String**|  | [optional] [default to Advanced]
 **customPolicyId** | **String**|  | [optional] 
 **inputFile** | **File**|  | [optional] 

### Return type

[**PhishingDetectionAdvancedResponse**](PhishingDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

<a name="phishingDetectFilePost"></a>
# **phishingDetectFilePost**
> PhishingDetectionResponse phishingDetectFilePost(opts)

Perform AI phishing detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.

### Example
```javascript
var CloudmersivePhishingapiClient = require('cloudmersive-phishingapi-client');
var defaultClient = CloudmersivePhishingapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersivePhishingapiClient.PhishingDetectionApi();

var opts = { 
  'model': "Advanced", // String | Model to use; default setting is Advanced
  'inputFile': "/path/to/file.txt" // File | 
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.phishingDetectFilePost(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **String**| Model to use; default setting is Advanced | [optional] [default to Advanced]
 **inputFile** | **File**|  | [optional] 

### Return type

[**PhishingDetectionResponse**](PhishingDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

<a name="phishingDetectTextStringAdvancedPost"></a>
# **phishingDetectTextStringAdvancedPost**
> PhishingDetectionAdvancedResponse phishingDetectTextStringAdvancedPost(opts)

Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```javascript
var CloudmersivePhishingapiClient = require('cloudmersive-phishingapi-client');
var defaultClient = CloudmersivePhishingapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersivePhishingapiClient.PhishingDetectionApi();

var opts = { 
  'body': new CloudmersivePhishingapiClient.PhishingDetectionAdvancedRequest() // PhishingDetectionAdvancedRequest | Phishing detection request
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.phishingDetectTextStringAdvancedPost(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhishingDetectionAdvancedRequest**](PhishingDetectionAdvancedRequest.md)| Phishing detection request | [optional] 

### Return type

[**PhishingDetectionAdvancedResponse**](PhishingDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

<a name="phishingDetectTextStringPost"></a>
# **phishingDetectTextStringPost**
> PhishingDetectionTextStringResponse phishingDetectTextStringPost(opts)

Perform AI phishing detection against input text string.  Returns a clean/not-clean result with confidence level and optional rationale.

### Example
```javascript
var CloudmersivePhishingapiClient = require('cloudmersive-phishingapi-client');
var defaultClient = CloudmersivePhishingapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersivePhishingapiClient.PhishingDetectionApi();

var opts = { 
  'body': new CloudmersivePhishingapiClient.PhishingDetectionTextStringRequest() // PhishingDetectionTextStringRequest | Phishing detection request
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.phishingDetectTextStringPost(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhishingDetectionTextStringRequest**](PhishingDetectionTextStringRequest.md)| Phishing detection request | [optional] 

### Return type

[**PhishingDetectionTextStringResponse**](PhishingDetectionTextStringResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

<a name="phishingDetectUrlAdvancedPost"></a>
# **phishingDetectUrlAdvancedPost**
> PhishingDetectionUrlAdvancedResponse phishingDetectUrlAdvancedPost(opts)

Perform advanced AI phishing detection and classification against an input URL.  Retrieves the URL content, checks for SSRF threats, and analyzes the page with AI deep learning to detect phishing and other unsafe content.  Uses 100-125 API calls.

### Example
```javascript
var CloudmersivePhishingapiClient = require('cloudmersive-phishingapi-client');
var defaultClient = CloudmersivePhishingapiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersivePhishingapiClient.PhishingDetectionApi();

var opts = { 
  'body': new CloudmersivePhishingapiClient.AdvancedUrlDetectionRequest() // AdvancedUrlDetectionRequest | URL phishing detection request
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.phishingDetectUrlAdvancedPost(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AdvancedUrlDetectionRequest**](AdvancedUrlDetectionRequest.md)| URL phishing detection request | [optional] 

### Return type

[**PhishingDetectionUrlAdvancedResponse**](PhishingDetectionUrlAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

