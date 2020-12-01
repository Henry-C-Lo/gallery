# FEC-LEGO-gallery
[![lego-logo-markdown.jpg](https://i.postimg.cc/SNMWY7nK/lego-logo-markdown.jpg)](https://https://github.com/FEC-LEGO)

---
##### Schema 
```javascript
const galleries = [];
for (let productId = 1; productId <= products; productId += 1) {
  const details = [];

  for (let imgId = 1; imgId <= 13; imgId += 1) {
    const productDescription = faker.commerce.productDescription();
    details.push({
      _id: imgId,
      name: productDescription,
      img_url: `https://lego-product-pictures.s3-us-west-1.amazonaws.com/product${productId}-image${imgId}.jpg`,
    });
  }

  galleries.push({
    pid: productId,
    name: faker.commerce.productName(),
    details,
  });
}
```

##### GET products
  - get: `'/:pid/getGalleries' `
##### Path Parameters
  - `pid` listing pid
##### Success Status Code: `200`
##### Returns: JSON object of a set of gallery

```javascript 
    [
        pid: 'Number',
        name: 'String',
        details: [
            _id: 'Number',
            name: 'String',
            img_url: 'String'
        ]
    ]
```
----
#### Demo
[![Gallery Component Demo](https://j.gifs.com/mOvKNO.gif)](https://www.youtube.com/watch?v=ek1j272iAmc)



