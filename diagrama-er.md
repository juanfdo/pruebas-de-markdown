# Prueba de Diagrama ER incrustado en archivo md

Prueba de Diagrama ER ([mermaid](https://mermaid.js.org/intro/getting-started.html)) incrustado en archivo md ([markdown](https://www.markdownguide.org/))

```mermaid
erDiagram
  Product  {
    Integer id
    String name
    String description
    String barcode
    String unitOfMeasure
    Float purchasePrice
    Float salePrice
    Integer quantityOnHand
  }
  Provider  {
    Integer id
    String name
    String address
    String phone
    String email
  }
  Location  {
    Integer id
    String name
    String address
    Integer capacity
  }
  InventoryMovement  {
    Integer id
    Date date
    String type
    Integer quantity
    Float price
    Float total
    Product product
    Provider provider
    Location location
  }
  Product  ||--o{  InventoryMovement  : places
  Provider  ||--o{  InventoryMovement  : places
  Location  ||--o{  InventoryMovement  : places
```
