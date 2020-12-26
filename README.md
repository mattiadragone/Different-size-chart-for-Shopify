# Different size chart for Shopify

> Use different size chart for Shopify in product page. Differentiate your size chart for vendor or product.type

## Output
You can see on the live store the [size chart](https://mattia-dragone-test.myshopify.com/collections/all).
![Recordit GIF](https://drive.google.com/uc?export=view&id=1d9CQjQxoeEBAGijZIWNNwB9NOu8bDiOy)

# Indice
- [How to](#how-to)
  - [Create your page](##create-your-page)
  - [Create your product](##create-your-product)
  - [Call the popup](##call-the-popup)
- [Option](#option)

# How to
## Create your page
Use Shopify's pages for create your size chart:
- Go to **Online store** > **Page** > **add page**
- use handle for serve different size chart 
  - structure handle: pages/size-chart-**product.type/product.vendor** 

*Also you can create a general size chart to show when there isn't a specific too > handle pages/size-chart

## Create your product
Use product.vendor or product.type to differenciate your size chart:
- Go to **product** > **add product** 
  - insert your product.type or vendor for match with the pages

## Call the popup
The pages content is inside a popup, you can insert a link for call it
```
{% unless product.has_only_default_variant %}
<span id="szcrt"><a href="#">Size Chart</a></span>
{% endunless %}
```
The condition check if there is a more than one product variant and show the link for opening.

# Option
You can differentiate size chart for:
- product.type
- product.vendor

In **snippets/size-chart.liquid** find
for product type:
```
{% assign differentSizeChart_id = product.type %} 
```
for vendor name: 
```
{% assign differentSizeChart_id = product.vendor %} 
```




