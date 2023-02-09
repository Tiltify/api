>### Deprecation Notice
>Api V3 is being deprecated on July 1st, 2023. Please consider updating to V5

>[V5 Api Documentation](https://v5api.tiltify.com/api/public)

-----

# Pagination

We use cursor based pagination for our donations and this information is
embeded in the response under the `links` key. You will find a `prev` and
`next` link that point to the next pages of the paginated response. You may
submit an optional `count` field of up to 100.


|key|description|
|:---|:---|
|**count**| This is the amount of results to return for the page. This number must be between 1 and 100.
|**before** or **after**| This is the id last item on the previous page.

Note that items are paginated in the order in which we use them on our site.
For example donations are paginated by their `completed_at` times, and the ids
may appear out of order because of payment provider webhook response times.

Sometimes you will find that the next page or prev page links are empty
strings, this means there are no more items in that direction at this time. You
can reuse the same request if you are polling the API, and new items will be in
the response if they exist.

```js
{
  // This is the HTTP status code that is also sent with the request
  "meta": {
    "status": 200,
  },

  // An object describing the pagination status of a given response
  "links": {
    "prev": "/api/v3/campaigns/5815/donations?count=10&before=116455",
    "next": "/api/v3/campaigns/5815/donations?count=10&after=310133",
    "self": "/api/v3/campaigns/5815/donations?count=10"
  }
}
```
