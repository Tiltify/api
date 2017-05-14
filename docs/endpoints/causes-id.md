# GET /causes/:id

Retreives a single cause given an identifier.

```js
{
  "id": 35,
  "name": "St. Jude Children's Research Hospital",
  "slug": "stjude",
  "url": "https://stjude.tiltify.com",
  "currency": "USD",
  "about": "* St. Jude Children's Research Hospital is leading the way the\nworld understands, treats and defeats childhood cancer and other\nlife-threatening diseases.  \n* Your support helps ensure that families never receive a bill\nfrom St. Jude for treatment, travel, housing or food -- because all a family\nshould worry about is helping their child live.  \n* St. Jude has helped push the childhood cancer survival rate\nfrom less than 20% when we opened to 80% today. We won't stop until no child\ndies from cancer.",
  "video": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "image": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "avatar": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "logo": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "bannerSrc": "https://asdfasdfasdf.cloudfront.net/1234.jpg",
  "bannerAlt": "some text describing the banner",
  "bannerTitle": "St. Jude Children's Research Hospital",
  "bannerIntro": "Start a fundraising campaign to help us end childhood cancer."
}
```

## Examples

{% method %}
### GET /causes/42
Returns a single cause entity with the ID of 42.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/42
```

{% sample lang="js" %}
```js
try {
  const cause = await Tiltify.Cause.get(42)
  // do something with the cause
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  cause = Tiltify::Cause.get(42)
  # do something with the cause
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.get(42) do
  {:ok, cause} -> # do something with the cause
  {:error, error} -> # handle error
end
```

{% endmethod %}

---

{% method %}
### GET /cause/cause-slug
Returns a single cause entity with a slug of cause-slug.

{% sample lang="curl" %}
```bash
curl https://tiltify.com/api/v3/causes/cause-slug
```

{% sample lang="js" %}
```js
try {
  const cause = await Tiltify.Cause.get('cause-slug')
  // do something with the cause
} catch(error) {
  // handle error
}
```

{% sample lang="ruby" %}
```ruby
begin
  cause = Tiltify::Cause.get('cause-slug')
  # do something with the cause
rescue Exception => error
  # handle error
end
```

{% sample lang="elixir" %}
```elixir
case Tiltify.Cause.get("cause-slug") do
  {:ok, cause} -> # do something with the cause
  {:error, error} -> # handle error
end
```

{% endmethod %}

