# Facebook CAPI Tag

This is an unofficial Facebook CAPI tag for the Google Tag Manager Community Template Gallery. Please raise an issue if you find any bugs or have a question!

## Documentation

### Endpoint

The URL of your server-side GTM (or similar solution), which accepts the data and sends it to Facebook.

### Pixel ID

This is the Facebook Pixel ID, which can be found in the Facebook Business Manager.

### Event Name

The event you want to measure with the tag. Facebook uses a set of [standard events](https://developers.facebook.com/docs/facebook-pixel/implementation/conversion-tracking#standard-events).

If the standard events do not suit your needs, you can also use a [custom event name](https://developers.facebook.com/docs/facebook-pixel/implementation/conversion-tracking#custom-events).

### Anonymise IP address

When checked, the `aip` parameter is sent to the server-side solution, which discards the remote IP address and does not send it to Facebook.

### Anonymise user agent

When checked, the `aua` parameter is sent to the server-side solution, which discards the user agent and does not send it to Facebook.

### Object Properties

You can include [object properties](https://developers.facebook.com/docs/facebook-pixel/implementation/conversion-tracking#object-properites) with any event.

#### Object Properties Variable

You can use a variable which returns an `Object` to include object properties. Any other type than `Object` is discarded.

This is helpful when you need to include product data on certain pages, simply return the values you need on the product pages and `undefined` on the rest.

#### Object Properties Table

In addition to a variable, you can also use a table to include object properties.

Note that the object properties table overrides values from the object properties variable, if there are any duplicate keys.

### Optional Parameters

#### Event ID

The *Event ID* is used to deduplicate events sent by Facebook Pixel and the CAPI. [Read more](https://developers.facebook.com/docs/marketing-api/conversions-api/parameters/server-event#event-id).
