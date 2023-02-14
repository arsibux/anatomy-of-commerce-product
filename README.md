# Anatomy of Commerce Product
Skeleton of commerce product, product variations and attributes.

## Product
In commerce, product is a reference with common fields { product_name, description, and images } to the product variants {product_id, variation_id} and the attributes[capacity, color]. In commerce, **PRODUCT DISPLAY** display all possible product variants as **OPTIONS**.

![](https://github.com/arsibux/anatomy-of-commerce-product/blob/main/img/product.drawio.png)
## Variations
Variations are physical products with different combination of attribites. Variants are the options of the product for customer to choose. For Example
- **128 RED Device** with its unique [PRODUCT_ID, VARIANT_ID, SKU, PRICE, IMAGES, DESCRIPTION].
- **256 BLUE Device** with its unique [PRODUCT_ID, VARIANT_ID, SKU, PRICE, IMAGES, DESCRIPTION].

## Attributes
Product attributes are the characteristics or properties which differntiate each variant. Color and capacity are attributes for variants. Product attribute has valuse like **color[Red, Blue, Green, Black]** and **capacity[128, 256, 512]**. These values make combinations of variants. In this example, maximum combination of variants would be **12**.
value[VARIANT_ID]

## Display Product
In e-commerce, product display provides all possible variants in such a mechanism 
that a customer can filter and select a variant of his choice.

![](https://github.com/arsibux/anatomy-of-commerce-product/blob/main/img/display.png)

## API Structure for Product Detail
**Product Detail Page** required following APIs to render the all details of selected variant.
- Product 
- Attributes
- Variations
- Images

### Product Title
GET Method with parameter of product ID return return array having id and title of the product.
- Path : api/v1/product/id/title
- Method GET
- Param int {id} //Product Id
- Return array Data[id, title]
   `` ["id":1000, "title":"Product Title"] ``
### Attributes
- Path : api/v1/product/id/attributes
- Method GET
- Param int {id} //Product Id
- Return array Data[name, values[]]
  ```` 
  [{
    "name": "capacity",
      "values": [
        "128 GB",
        "256 GB",
        "520 GB"
     ]
   },
  {
    "name": "color",
    "values": [
      "RED",
      "BLUE",
      "GREEN",
      "BLACK"
    ]
  }]

### Variations
- Path : api/v1/product/id/variations
- Method GET
- Param int {id} //Product Id
- Return array Data[id, title]
  ````
  [{
    "id": 1829,
    "capacity": "128 GB",
    "color": "RED"
  },
  {
    "id": 1831,
    "capacity": "256 GB",
    "color": "RED"
  }]

### Variant
- Path : api/v1/variant/{id}
- Method GET
- Param int {id} //variant Id
- Return array Data[id, title]
  `` ["id":1000, "title":"Product Title"] ``

### Images of Variant
- Path : api/v1/product/id/title
- Method GET
- Param int {id} //Product Id
- Return array Data[id, title]
  `` ["id":1000, "title":"Product Title"] ``

## Product Display Component
- Product Title Component
- Product Attributes Component
    - Capacity
    - Color
- Variant Component

## Resources
- [Drupal Commerce Guide](https://docs.drupalcommerce.org/commerce2/developer-guid)
- [Attributes products and variations drupal commerce ](https://menetray.com/en/blog/attributes-products-and-variations-drupal-commerce)