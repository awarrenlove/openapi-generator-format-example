# openapi_client.DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**root_post**](DefaultApi.md#root_post) | **POST** / | 


# **root_post**
> root_post(post_request)



### Example


```python
import time
import openapi_client
from openapi_client.api import default_api
from openapi_client.model.post_request import PostRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    post_request = PostRequest(
        param="param_example",
    ) # PostRequest | 

    # example passing only required values which don't have defaults set
    try:
        api_instance.root_post(post_request)
    except openapi_client.ApiException as e:
        print("Exception when calling DefaultApi->root_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **post_request** | [**PostRequest**](PostRequest.md)|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

