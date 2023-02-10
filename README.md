# Anatomy of Commerce Product
Skeleton of commerce product, product variations and attributes.

## Product
In commerce, product is a reference with common fields { product_name, description, and images } to the product variants {product_id, variation_id} and the attributes[capacity, color].

![](https://github.com/arsibux/anatomy-of-commerce-product/blob/main/img/product.drawio.png)
## Variations
Variations are physical products with different combination of attribites. Variants are the options of the product for customer to choose. For Example
- `128 RED Device` with its unique [PRODUCT_ID, VARIANT_ID, SKU, PRICE, IMAGES, DESCRIPTION].
- `256 BLUE Device` with its unique [PRODUCT_ID, VARIANT_ID, SKU, PRICE, IMAGES, DESCRIPTION].

## Attributes
Product attributes are the characteristics or properties which differntiate each variant. Color and capacity are attributes for variants. Product attribute has valuse like `color[Red, Blue, Green, Gray]` and `capacity[128, 256, 512]`. These values make combinations of variants. In this example, maximum combination of variants would be `12`.
value[VARIANT_ID,]
## Resources
- [Drupal Commerce Guide](https://docs.drupalcommerce.org/commerce2/developer-guid)
- [Attributes products and variations drupal commerce ](https://menetray.com/en/blog/attributes-products-and-variations-drupal-commerce)
