>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# Errors

The Tiltify API uses HTTP status codes to indicate if a problem has occured
with a request. All responses will contain the HTTP status code, as well as
at least one method of describing the error that occured.

The singular `error` key appears when one thing went wrong with a request. This
will usually appear with authorization errors or not found errors. All of these
error objects have a title and detail keys.

The plural `errors` key appears when submitting a model, with mappings to the
validation errors with each field. You will not see this unless submitting a
POST or PATCH request to the API.

```js
{
  // This is the HTTP status code that is also sent with the request
  "meta": {
    "status": 403,
  },

  // An object describing the error that occurred.
  "error": {
    "title": "Not Authorized",
    "detail": "Sorry, you are not authorized to view this resource."
  },

  // An object pointing to fields that are incorrect in a submitted model
  "errors": {
    "campaign": {
      "name": "name cannot be blank"
    }
  }
}
```

---

## Types of Errors

##### 400 - Bad Request
This error describes when the request could not be fulfilled. This often
happens because of a missing request parameter.

##### 401 - Not Authorized
This error describes when the user needs to be authorized before accessing this
resource.

##### 403 - Forbidden
This error describes when the user accessing a resource does not have
permission to do so.

##### 404 - Not Found
This error describes when a given resource cannot be found. The ID or slug
given is most likely incorrect or has changed. For this reason, we recommend
using the ID if you have access to it.

##### 422 - Unprocessable Entity
This error describes when submitted params are invalid.

##### 500+ - Internal Server Error
This error describes when a something bad happened on our end. You should
rarely see these. We'll do our best to fix them, but feel free to bug our CM.
