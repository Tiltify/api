# Errors

The Tiltify API uses HTTP status codes to indicate if a problem has occured
with a request. An error response will contain the HTTP status code, as well as
at least one method of describing the error that occured.

```js
{

  // This is the HTTP status code that is also sent with the request
  "status": 404,

  // A string describing what is wrong
  "error": "Sorry, you are not authorized to view this resource.",

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

##### 403 - Not Authorized
This error describes when the user accessing a resource does not have
permission to do so.

##### 404 - Not Found
This error describes when a given resource cannot be found. The ID or slug
given is most likely incorrect or has changed. For this reason, we recommend
using the ID if you have access to it.

##### 500+ - Internal Server Error
This error describes when a something bad happened on our end. You should
rarely see these. We'll do our best to fix them, but feel free to bug our CM.
