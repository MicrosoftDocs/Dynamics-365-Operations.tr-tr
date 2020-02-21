## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Ürün kategorisi atamaları ve msdyn_productcategoryassignments

Bu şablon, Finance and Operations uygulamaları ve Common Data Service arasında verileri eşitler.

Finance and Operations alanı | Eşleme türü | Diğer Dynamics 365 alanı | Varsayılan değer
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
