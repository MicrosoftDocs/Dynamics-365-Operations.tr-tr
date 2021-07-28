---
title: Birleştirilmiş ürün deneyimi
description: Bu konu Finance and Operations uygulamaları ile Dataverse arasında ürün verileri tümleştirmesini açıklar.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 115eaad4f11fc4fb5321f0d8bb9d4f5a9f2f2c7c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358605"
---
# <a name="unified-product-experience"></a>Birleşik ürün deneyimi

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bir işletmenin ekosistemi Finance, Supply Chain Management ve Sales gibi Dynamics 365 uygulamalarından oluştuğunda, işletmeler sıklıkla ürün verilerini kaynak olarak kullanmak için bu uygulamaları kullanır. Bunun nedeni, bu uygulamaların sofistike fiyatlandırma kavramları ve doğru eldeki stok verileriyle kapsamlı bir ürün altyapısı sağlamasıdır. Ürün verilerinin kaynağı için harici bir Ürün Yaşam Döngüsü Yönetimi (PLM) sistemi kullanan işletmeler, Finance and Operations uygulamalarındaki ürünleri diğer Dynamics 365 uygulamalarına yöneltebilirler. Birleştirilmiş ürün deneyimi, Dataverse'e tümleşik ürün veri modelini getirir ve böylece Power Platform kullanıcıları dahil tüm uygulama kullanıcıları, Finance and Operations uygulamalarından gelen zengin ürün verilerinden yararlanabilir.

Sales'den genel ürün veri modeli.

![CE'de ürünler için veri modeli.](media/dual-write-product-4.jpg)

Finance and Operations uygulamalarından genel ürün veri modeli.

![Finance and Operations'de ürünler için veri modeli.](media/dual-write-products-5.jpg)

Bu iki ürün veri modeli aşağıda gösterildiği gibi Dataverse'te tümleştirilmiştir.

![Dynamics 365 uygulamalarındaki ürünler için veri modeli.](media/dual-write-products-6.jpg)

Ürünler için çift yazma tablo eşlemeleri, Finance and Operations uygulamalarından Dataverse'e gerçek zamanlıya yakın olarak verilerin yalnızca tek yönlü akışını sağlamak için tasarlanmıştır. Ancak, ürün altyapısı gerektiğinde çift yönlü hale getirilebilecek şekilde açık yapıldı. Microsoft bu yaklaşımı önermemesine karşın kendi sorumluluğunuzda olacak şekilde bunu özelleştirebilirsiniz.

## <a name="templates"></a>Şablonlar

Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir. Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için tablo haritaları koleksiyonu oluşturulur.

Finance and Operations uygulamaları | Diğer Dynamics 365 uygulamaları | Tanım
-----------------------|--------------------------------|---
Serbest bırakılan ürünler V2 | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails** tablosu, Finance and Operations uygulamalarından ürünü tanımlayan ve ürünün mali ve yönetim bilgilerini içeren sütunlar içerir. 
Dataverse serbest bırakılan farklı ürünler | Ürün | **Ürün** tablosu, ürünü tanımlayan sütunları içerir. Bağımsız ürünleri (alt tür ürünü olan ürünler) ve ürün çeşitlerini içerir. Aşağıdaki tablo eşlemeleri göstermektedir.
Ürün numarası tanımlanan barkod | msdyn\_productbarcodes | Ürün barkodları, ürünleri benzersiz olarak tanımlamak için kullanılır.
Varsayılan sipariş ayarları | msdyn\_productdefaultordersettings
Ürüne özel varsayılan sipariş ayarları | msdyn_productdefaultordersettings
Ürün boyut grupları | msdyn\_productdimensiongroups | Ürünü hangi ürün boyutlarının tanımlayacağı tanımlayan ürün boyutu. 
Depolama boyut grupları | msdyn\_productstoragedimensiongroups | Ürün depolama boyutu grubu, ürünün ambarda yerleşimini tanımlamak için kullanılan yöntemi temsil eder.
İzleme boyutu grupları | msdyn\_producttrackingdimensiongroups | Ürün izleme boyutu grubu, ürünü stokta izlemek için kullanılan yöntemi temsil eder.
Renkler | msdyn\_productcolors
Boyutlar | msdyn\_productsizes
Stiller | msdyn\_productsytles
Yapılandırmalar | msdyn\_productconfigurations
Ana ürün renkleri | msdyn_sharedproductcolors | **Paylaşılan ürün rengi** tablosu, belirli bir ana ürünün sahip olabileceği renkleri gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
Ana ürün boyutları | msdyn_sharedproductsizes | **Paylaşılan ürün boyutu** tablosu, belirli bir ana ürünün sahip olabileceği boyutları gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
Ana ürün stilleri | msdyn_sharedproductstyles | **Paylaşılan ürün stili** tablosu, belirli bir ana ürünün sahip olabileceği stilleri gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
Ana ürün yapılandırmaları | msdyn_sharedproductconfigurations | **Paylaşılan ürün yapılandırması** tablosu, belirli bir ana ürünün sahip olabileceği yapılandırmaları gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
Tüm ürünler | msdyn_globalproducts | Tüm ürünler tablosu, hem serbest bırakılmış ürünler hem de serbest bırakılmamış ürünler olmak üzere Finance and Operations uygulamalarındaki tüm ürünleri içerir.
Birim | uoms
Birim dönüştürmeleri | msdyn_ unitofmeasureconversions
Ürüne özel ölçü birimi dönüşümü | msdyn_productspecificunitofmeasureconversion
Ürün kategorileri | msdyn_productcategories | Her bir ürün kategorisi ve bunların yapısı ve özellikleri hakkında bilgiler ürün kategorisi tablosunda bulunur. 
Ürün kategori hiyerarşileri | msdyn_productcategoryhierarhies | Ürünleri kategorize etmek veya gruplamak için ürün hiyerarşilerini kullanabilirsiniz. Kategori hiyerarşileri, Ürün kategorisi hiyerarşisi tablosu kullanılarak Dataverse'te kullanılabilir. 
Ürün kategori hiyerarşisi rolleri | msdyn_productcategoryhierarchies | Ürün hiyerarşileri D365 Finance and Operations'taki farklı roller için kullanılabilir. Her rolde hangi kategorinin kullanıldığını belirtmek için ürün kategorisi rol tablosu kullanılır. 
Ürün kategorisi atamaları | msdyn_productcategoryassignments | Ürünü bir kategoriye atamak için ürün kategorisi atamaları tablosu kullanılabilir.

## <a name="integration-of-products"></a>Ürünlerin tümleştirilmesi

Bu modelde, ürün Dataverse'teki iki tablonun birleşimiyle gösterilir: **Ürün** ve **msdyn\_sharedproductdetails**. İlk tablo bir ürünün tanımını (ürünün benzersiz tanımlayıcısı, ürün adı ve açıklaması) içerirken, ikinci tablo ürün düzeyinde depolanan sütunları içerir. Bu iki tablonun birleşimi, ürünü stok tutma birimi (SKU) kavramına göre tanımlamak için kullanılır. Kullanıma sunulan her ürünün bilgileri belirtilen tablolarda (Ürün ve Paylaşılan Ürün Ayrıntıları) olacaktır. Tüm ürünleri izlemek için (serbest bırakılmış ve serbest bırakılmamış) **Genel ürünler** tablosu kullanılır. 

Ürün bir SKU olarak temsil edildiği için farklı ürünler, ana ürünler ve ürün çeşitleri kavramları Dataverse'ta aşağıdaki şekilde yakalanabilir:

- **Alt tür ürününe sahip ürünler**, kendileri tarafından tanımlanan ürünlerdir. Boyut tanımlanması gerekmez. Belirli bir defter örnek olarak verilebilir. Bu ürünler için **Ürün** tablosunda bir satır ve **msdyn\_sharedproductdetails** tablosunda bir satır oluşturulur. Ürün ailesi satırı oluşturulmaz.
- **Ana ürünler**, iş süreçlerindeki davranışı belirleyen tanımı ve kuralları içeren genel ürünler olarak kullanılır. Bu tanımlara dayalı olarak, ürün çeşitleri olarak bilinen farklı ürünler oluşturulabilir. Örneğin, Tişört ana üründür ve Renk ve Beden boyutlarına sahip olabilir. Bu boyutların farklı birleşimlerine sahip çeşitler serbest bırakılabilir: small beden mavi tişört veya medium beden yeşil tişört gibi. Tümleştirmede, ürün tablosunda her çeşit için bir satır oluşturulur. Bu satır farklı boyutlar gibi ürün çeşidine özgü bilgileri içerir. Ürünle ilgili genel bilgiler **msdyn\_sharedproductdetails** tablosunda depolanır. (Bu genel bilgi ana üründe tutulur.) Ana ürün bilgileri, serbest bırakılan ana ürün oluşturulduğunda Dataverse ile eşitlenir (çeşitler yayımlanmadan önce).
- **Ayrı ürünler** tüm ürün alt tür ürünleri ve tüm ürün çeşitlerini ifade eder. 

![Ürünler için veri modeli.](media/dual-write-product.png)

Çift yazma işlevi etkin olduğunda, Finance and Operations'taki ürünler **Taslak** durumunda diğer Dynamics 365 ürünlerinde eşitlenir. Aynı para birimiyle ilk fiyat listesine eklenir. Başka bir deyişle, Dynamics 365 uygulamasında, Finance and Operations uygulamasında ürünün serbest bırakıldığı tüzel kişiliğin para birimiyle eşleşen ilk fiyat listesine eklenir. Belirtilen para birimi için fiyat listesi yoksa fiyat listesi otomatik olarak oluşturulur ve ürün buna atanır. 

Varsayılan fiyat listesini birimle ilişkilendiren çift yazma eklentilerin geçerli uygulaması, Finance and Operations uygulamasıyla ilgili para birimini arar ve fiyat listesi adının alfabetik sıralamasını kullanarak customer engagement uygulamasındaki ilk fiyat listesini bulur. Belirli bir para birimi için birden fazla fiyat listeniz olduğunda, bu para birimi için varsayılan fiyat listesi ayarlamak istediğinizde, fiyat listesi adını, o para birimine yönelik diğer fiyat listelerinden alfabetik sıraya göre daha önde olan bir adla güncelleştirmeniz gerekir.

Varsayılan olarak, Finance and Operations uygulamalarındaki ürünler **Taslak** durumundaki diğer Dynamics 365 uygulamalarıyla eşitlenir. Örneğin, satış siparişi tekliflerinde doğrudan kullanmak amacıyla **Etkin** durumdaki ürünü eşitlemek için şu ayarın seçilmesi gerekir: **Sistem > Yönetim > Sistem yönetimi > Sistem ayarları > Satış** sekmesi ve **Ürünleri etkin durumda oluştur = evet** seçeneğini belirleyin. 

Ürünler eşitlenirken, Finance and Operations uygulamasındaki **Satış birimi** alanı için bir değer girmeniz gerekir; çünkü bu alan Sales'da zorunlu bir alandır.

Dynamics 365 Sales'den ürün aileleri oluşturma, ürünlerin çift yazma eşitlemesiyle desteklenmez.

Ürün eşitleme işleminin Finance and Operations uygulaması ile Dataverse arasında yapıldığını unutmayın. Bu, ürün tablo sütunlarının değerlerinin Dataverse'te değiştirilebileceği anlamına gelir ancak eşitleme tetiklendiğinde (Finance and Operations uygulamasında bir ürün sütunu değiştirildiğinde) bu işlem, Dataverse'teki değerlerin üzerine yazar. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Ürün boyutları 

Ürün boyutları, ürün çeşidini tanımlamaya hizmet eden özelliklerdir. Dört ürün boyutu (Renk, Boyut, Stil ve Yapılandırma) ürün çeşitlerini tanımlamak amacıyla Dataverse'a eşlenir. Aşağıdaki resimde Renk ürün boyutu için veri modeli gösterilmektedir. Aynı model Boyutlara, Stillere ve Yapılandırmalara da uygulanır. 

![Ürün boyutları için veri modeli.](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Ürünün farklı ürün boyutları (örneğin, ürün boyutu olarak Boyut ve Renk boyutu bulunan bir ana ürün) olduğunda, her ayrı ürün (her bir ürün çeşidi) bu ürün boyutlarının bir birleşimi olarak tanımlanır. Örneğin, ürün numarası B0001 extra small beden siyah tişört ve ürün numarası B0002 small beden siyah tişörttür. Bu durumda, ürün boyutlarının var olan birleşimleri tanımlanmıştır. Örneğin, önceki örnekteki Tişört extra small ve siyah, small ve siyah, medium ve siyah veya large ve siyah olabilir, ancak extra large ve siyah olamaz. Başka bir deyişle, bir ana ürünün alabileceği ürün boyutları belirtilir ve ürün çeşitleri bu değerlere dayalı olarak serbest bırakılabilir.

Bir ana ürünün alabileceği ürün boyutlarını takip etmek için aşağıdaki tablolar oluşturulur ve her ürün boyutu için Dataverse'te eşlenir. Daha fazla bilgi için bkz. [Ürün bilgilerine genel bakış](../../../../supply-chain/pim/product-information.md). 

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Varsayılan sipariş ayarları ve ürüne özgü varsayılan sipariş ayarları

Varsayılan sipariş ayarları maddelerin bulunduğu veya depolandığı tesisi ve ambarı, ticari veya stok yönetimi için kullanılacak minimum, maksimum, birden fazla ve standart miktarları, sağlama sürelerini, durdurma bayrağını ve sipariş taahhüt hesabını tanımlar. Bu bilgiler varsayılan sipariş ayarları ve ürüne özel varsayılan sipariş ayarları varlığı kullanılarak Dataverse'te kullanılabilir. İşlev hakkında daha fazla bilgiye [Varsayılan sipariş ayarları konusu](../../../../supply-chain/production-control/default-order-settings.md)'ndan ulaşabilirsiniz.

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Ölçü birimi ve ölçü birimi dönüşümleri

Ölçü birimleri ve ilgili dönüştürme, şemada gösterilen veri modeline uygun olarak Dataverse'te kullanılabilir.

![Ölçü birimi için veri modeli.](media/dual-write-product-three.png)

Ölçü birimi kavramı, Finance and Operations uygulamaları ile diğer Dynamics 365 uygulamaları arasında entegre edilmiştir. Finance and Operations uygulamasındaki her birim sınıfı için Dynamics 365 uygulamasında bu birim sınıfına ait birimleri içeren bir birim grubu oluşturulur. Her birim grubu için varsayılan bir temel birim de oluşturulur. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Finance and Operations ile Dataverse arasında eşleşen birim verilerinin başlangıç eşitlemesi

### <a name="initial-synchronization-of-units"></a>Birimlerin başlangıç eşitlemesi

Çift yazma etkinleştirildiğinde Finance and Operations uygulamalarından birimler diğer Dynamics 365 uygulamalarına eşitlenir. Finance and Operations uygulamaları ile Dataverse arasında eşitlenen birim gruplarında "Harici olarak korunduklarını" belirten bir bayrak bulunur.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Finance and Operations ve diğer Dynamics 365 uygulamalarındaki birimleri ve birim sınıflarını/gruplarını eşleştirme

Öncelikle, birimin tümleştirme anahtarının msdyn_symbol olduğunu dikkate almak önemlidir. Bu nedenle, bu değer Dataverse'te veya diğer Dynamics 365 uygulamalarında benzersiz olmalıdır. Diğer Dynamics 365 uygulamalarında "Birim grubu kodu" ve "Ad" çifti bir birimin benzersizliğini tanımladığından Finance and Operations uygulamaları ile Dataverse arasında birim verilerini eşleştirirken farklı senaryoları dikkate almanız gerekir.

Finance and Operations uygulamaları ve diğer Dynamics 365 uygulamalarında eşleşen/çakışan birimler için:

+ Diğer Dynamics 365 uygulamalarında **bir birim grubuna ait olan ve Finance and Operations uygulamalarında ilişkili birim sınıfına karşılık gelen birim**. Bu durumda, diğer Dynamics 365 uygulamalarındaki msdyn_symbol sütunu, Finance and Operations uygulamalarındaki birim simgesiyle doldurulmalıdır. Bu nedenle, veriler eşlendiğinde birim grubu diğer Dynamics 365 uygulamalarında "Harici olarak korunan" olarak ayarlanır.
+ **Diğer Dynamics 365 uygulamalarında bir birim grubuna ait olan ve Finance and Operations uygulamalarında ilişkili birim sınıfına karşılık gelmeyen birim (diğer Dynamics 365 uygulamalarındaki birim sınıfı için Finance and Operations uygulamalarında mevcut birim sınıfının olmaması).** Bu durumda, msdyn_symbol alanı rastgele bir dizeyle doldurulmalıdır. Bu değerin diğer Dynamics 365 uygulamalarında benzersiz olması gerektiğini unutmayın.

Diğer Dynamics 365 uygulamalarında bulunmayan Finance and Operations'taki birimler ve birim sınıfları için:

Çift yazmanın parçası olarak Finance and Operations uygulamalarındaki birim grupları ve bunların karşılık gelen birimleri diğer Dynamics 365 uygulamalarında ve Dataverse'te oluşturulup eşitlenir ve birim grubu “Harici olarak korunan” olarak ayarlanır. Ek önyükleme çalışmasına gerek yoktur.

Finance and Operations uygulamalarında bulunmayan diğer Dynamics 365 uygulamalarındaki birimler için:

msdyn_symbol sütunu tüm birimler için doldurulmalıdır. Birimler, her zaman karşılık gelen birim sınıfı için (varsa) Finance and Operations uygulamalarında oluşturulabilir. Birim sınıfı yoksa öncelikle diğer Dynamics 365 uygulamaları birim grubuyla eşleşen birim sınıfı oluşturulmalıdır (numaralandırmayı uzatıyorsanız Finance and Operations uygulamalarında uzantı dışında bir birim sınıfı oluşturamayacağınızı unutmayın). Ardından birimi oluşturabilirsiniz. Birim için Finance and Operations uygulamalarındaki birim sembolünün, birim için diğer Dynamics 365 uygulamalarında daha önce belirtilen msdyn_symbol olması gerektiğini unutmayın.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Ürün ilkeleri: boyut, izleme ve depolama grupları

Ürün ilkeleri, ürünleri ve özelliklerini stokta tanımlamak için kullanılan ilke kümeleridir. Ürün boyut grubu, ürün izleme boyut grubu ve depolama boyutu grubu ürün ilkesi olarak bulunabilir. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Ürün hiyerarşileri

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Ürünler için tümleştirme anahtarı 

Dynamics 365 for Finance and Operations ile Dataverse arasında ürünleri benzersiz şekilde tanımlamak için tümleştirme anahtarları kullanılır. Ürünler için, **(productnumber)** Dataverse'te bir ürünü tanımlayan benzersiz anahtardır. Bu, bir birleşimden oluşur: **(şirket, msdyn_productnumber)**. **Şirket** Finance and Operations'ta tüzel kişiliği ve **msdyn_productnumber** Finance and Operations'ta belirli bir ürünün ürün numarasını belirtir. 

Başka bir Dynamics 365 uygulamaları kullanıcısı için ürün, kullanıcı arabiriminde **msdyn_productnumber** ile tanımlanır (sütun etiketinin **Ürün numarası** olduğunu unutmayın). Ürün formunda, hem şirket hem de msydn_productnumber gösterilir. Ancak bir ürünün benzersiz anahtarı olan (productnumber) sütunu gösterilmez. 

Dataverse üzerinde uygulama oluşturuyorsanız, tümleştirme anahtarı olarak **ProductNumber** (benzersiz ürün kodu) öğesini kullanarak ilgiyi ödemelisiniz. Benzersiz olmadığından **msdyn_productnumber** kullanmayın. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Ürünlerin başlangıç eşitlemesi ve verilerin Dataverse'ten Finance and Operations'a taşınması

### <a name="initial-synchronization-of-products"></a>Ürünlerin başlangıç eşitlemesi 

Çift yazma etkinleştirildiğinde Finance and Operations uygumalarından ürünler Dataverse ve diğer müşteri etkileşimi uygulamalarına eşitlenir. Dataverse ve diğer Dynamics 365 uygulamalarında çift yazma yayınlanmadan önce oluşturulan ürünlerin, Finance and Operations uygulamalarındaki ürün verileriyle güncelleştirilmediğini veya eşleşmediğini unutmayın.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Finance and Operations ve diğer Dynamics 365 uygulamalarındaki ürün verilerini eşleştirme

Finance and Operations'ta, Dataverse'te ve diğer Dynamics 365 uygulamalarında aynı ürünler tutuluyorsa, (çakışan/eşlenen) çift yazma etkinleştirildiğinde Finance and Operations'taki ürünlerin eşitlenmesi gerçekleşir ve Dataverse'te aynı ürün için tekrarlanan satırlar görünür.
Diğer Dynamics 365 uygulamalarında Finance and Operations ile çakışan/eşlenen ürünler varsa önceki durumdan kaçınmak için çift yazmayı etkinleştiren yönetici, ürünlerin eşitlenmesi gerçekleşmeden önce **Şirket** (örnek: "USMF") ve **msdyn_productnumber** (örnek: "1234:Black:S") sütunlarını önyüklemelidir. Başka bir deyişle, Dataverse'te ürünlerdeki bu iki sütunun Finance and Operations'ta ürünün ve ürün numarasının eşleşmesi gerektiği ilgili şirketle doldurulması gerekir. 

Böylece, eşitleme etkinleştirildiğinde ve gerçekleştiğinde Finance and Operations'taki ürünler, Dataverse ve diğer Dynamics 365 uygulamalarındaki eşleşen ürünlerle eşitlenir. Bu hem farklı ürünler hem de ürün çeşitleri için geçerlidir. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Ürün verilerinin diğer Dynamics 365 uygulamalarından Finance and Operations'a taşınması

Diğer Dynamics 365 uygulamalarında Finance and Operations'ta bulunmayan ürünler varsa yönetici bu ürünleri Finance and Operations'ta içe aktarmak için öncelikle **EcoResReleasedProductCreationV2Entity** varlığını kullanabilir. Ardından yukarıda açıklandığı gibi Finance and Operations ve diğer Dynamics 365 uygulamalarındaki ürün verilerini eşleştirebilir. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
