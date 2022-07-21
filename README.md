This application demonstrates an issue where the format for a string field is used
as the type of that field.

When using the python generator using this command

`npx @openapitools/openapi-generator-cli generate -i openapi.yaml -g python -o ./`

the generated client no longer allows a string for that field, even a string containing
a valid integer as was intended by the specification, but instead requires an integer.

Meaning, `PostRequest(100)` works but `PostRequest('100')` throws the exception

`openapi_client.exceptions.ApiTypeError: Invalid type for variable 'param'. Required value type is int and passed type was str at ['param']`
