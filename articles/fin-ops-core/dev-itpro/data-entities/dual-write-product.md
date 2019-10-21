---
title: Birleştirilmiş ürün deneyimi
description: Bu konu Finance and Operations uygulamaları ile Common Data Service arasında ürün verileri tümleştirmesini açıklar.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249340"
---
# <a name="unified-product-experience"></a>Birleştirilmiş ürün deneyimi

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Bir işletmenin ekosistemi Finance, Supply Chain Management ve Sales gibi Dynamics 365 uygulamalarından oluştuğunda, müşterilerin ürün verilerini kaynak olarak kullanmak için bu uygulamaları kullanmaları doğaldır. Bunun nedeni, bu uygulamaların sofistike fiyatlandırma kavramları ve doğru eldeki stok verileriyle kapsamlı bir ürün altyapısı sağlamasıdır. Ürün verilerinin kaynağı için harici bir Ürün Yaşam Döngüsü Yönetimi (PLM) sistemi kullanan müşteriler, Finance and Operations uygulamalarındaki ürünleri diğer Dynamics 365 uygulamalarına yöneltebilirler. Birleştirilmiş ürün deneyimi, Common Data Service'a tümleşik ürün veri modelini getirir ve böylece Power Platform kullanıcıları dahil tüm uygulama kullanıcıları, Finance and Operations uygulamalarından gelen zengin ürün verilerinden yararlanabilir.

Sales'den genel ürün veri modeli.

![Ürünler için veri modeli Sales](media/dual-write-product-4.jpg)

Finance and Operations uygulamalarından gelen ürün veri modeli.

![Finance and Operations'ta ürünler için veri modeli](media/dual-write-products-5.jpg)

Bu iki ürün veri modeli aşağıda gösterildiği Common Data Service'ta tümleştirilmiştir.

![Dynamics 365 uygulamalarındaki ürünler için veri modeli](media/dual-write-products-6.jpg)

Ürünler için varlık çift yazma eşlemeleri, verilerin yalnızca tek yönlü akışını sağlamak için tasarlanmıştır ve Finance and Operations uygulamalarından Common Data Service'a gerçek zamanlıya yakın deneyim sunar. Ancak, ürün altyapısı gerektiğinde çift yönlü hale getirilebilecek şekilde açık yapıldı. Microsoft bu yaklaşımı önermemesine karşın müşteriler riskler kendi sorumluluklarında olacak şekilde bunu özelleştirebilir.

## <a name="templates"></a>Şablonlar

Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir. Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için varlık haritaları koleksiyonu oluşturulur.

Finance and Operations | Diğer Dynamics 365 uygulamaları
-----------------------|--------------------------------
Serbest bırakılan ürünler V2 | msdyn\_sharedproductdetails
CDS serbest bırakılan farklı ürünler | Ürün
Ürün numarası tanımlanan barkod | msdyn\_productbarcodes
Varsayılan sipariş ayarları | msdyn\_productdefaultordersettings
Ürüne özel varsayılan sipariş ayarları | msdyn_productspecificdefaultordersettings
Ürün boyut grupları | msdyn\_productdimensiongroups
Depolama boyut grupları | msdyn\_productstoragedimensiongroups
İzleme boyutu grupları | msdyn\_producttrackingdimensiongroups
Renkler | msdyn\_productcolors
Boyutlar | msdyn\_productsizes
Stiller | msdyn\_productsytles
Yapılandırmalar | msdyn\_productconfigurations
Ana ürün renkleri | msdyn_sharedproductcolors
Ana ürün boyutları | msdyn_sharedproductsizes
Ana ürün stilleri | msdyn_sharedproductstyles
Ana ürün konfigürasyonları | msdyn_sharedproductconfigurations
Tüm ürünler | msdyn_globalproducts
Birim | uoms
Birim dönüştürmeleri | msdyn_ unitofmeasureconversions
Ürüne özel ölçü birimi dönüşümü | msdyn_productspecificunitofmeasureconversion
Siteler | msdyn\_operationalsites
Ambarlar | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>Ürünlerin tümleştirilmesi

Bu modelde, ürün Common Data Service'taki iki varlığın birleşimiyle gösterilir: **Ürün** ve **msdyn\_sharedproductdetails**. İlk varlık bir ürünün tanımını (ürünün benzersiz tanımlayıcısı, ürün adı ve açıklaması) içerirken, ikinci varlık ürün düzeyinde depolanan alanları içerir. Bu iki varlığın birleşimi, ürünü stok tutma birimi (SKU) kavramına göre tanımlamak için kullanılır. Serbest bırakılan her ürünün bilgileri belirtilen varlıklarda (Ürün ve Paylaşılan Ürün Ayrıntıları) olacaktır. Tüm ürünleri izlemek için (serbest bırakılmış ve serbest bırakılmamış) **Genel ürünler** varlığı kullanılır. 

Ürün bir SKU olarak temsil edildiği için farklı ürünler, ana ürünler ve ürün çeşitleri kavramları Common Data Service'ta aşağıdaki şekilde yakalanabilir:

- **Alt tür ürününe sahip ürünler**, kendileri tarafından tanımlanan ürünlerdir. Bunlar için boyut tanımlanması gerekmez. Belirli bir defter örnek olarak verilebilir. Bu ürünler için **Ürün** varlığında bir kayıt ve **msdyn\_sharedproductdetails** varlığında bir kayıt oluşturulur. Ürün ailesi kaydı oluşturulmaz.
- **Ana ürünler**, iş süreçlerindeki davranışı belirleyen tanımı ve kuralları içeren genel ürünler olarak kullanılır. Bu tanımlara dayalı olarak, ürün çeşitleri olarak bilinen farklı ürünler oluşturulabilir. Örneğin, Tişört ana üründür ve Renk ve Beden boyutlarına sahip olabilir. Bu boyutların farklı birleşimlerine sahip çeşitler serbest bırakılabilir: small beden mavi tişört veya medium beden yeşil tişört gibi. Tümleştirmede, ürün tablosunda her çeşit için bir kayıt oluşturulur. Bu kayıt farklı boyutlar gibi ürün çeşidine özgü bilgileri içerir. Ürünle ilgili genel bilgiler **msdyn\_sharedproductdetails** varlığında depolanır. (Bu genel bilgi ana üründe tutulur.) Ek olarak, her ana ürün için bir ürün ailesi kaydı oluşturulur. Ana ürün bilgileri, serbest bırakılan ana ürün oluşturulduğunda Common Data Service'la eşitlenir (çeşitler serbest bırakılmadan önce).
- **Ayrı ürünler** tüm ürün alt tür ürünleri ve tüm ürün çeşitlerini ifade eder. 

![Ürünler için veri modeli](media/dual-write-product.png)

Çift yazma işlevi etkin olduğunda, Finance and Operations'taki uygulamalar **Taslak** durumunda diğer Dynamics 365 uygulamalarında eşitlenir. Aynı para birimiyle ilk fiyat listesine eklenir. Başka bir deyişle, Dynamics 365 uygulamasında, Finance and Operations uygulamasında ürünün serbest bırakıldığı tüzel kişiliğin para birimiyle eşleşen ilk fiyat listesine eklenir. 

Örneğin satış siparişi tekliflerinde doğrudan kullanmak amacıyla **Etkin** durumdaki ürünü eşitlemek için, şu ayarın seçilmesi gerekir: **Sistem> Yönetim > Sistem yönetimi > Sistem ayarları > Satış** altından **Ürünleri etkin durumda oluştur = evet** seçeneğini belirleyin. 

### <a name="cds-released-distinct-products-to-product"></a>CDS'de Ürüne serbest bırakılan ayrı ürünler

**Ürün** varlığı, ürünü tanımlayan alanları içerir. Bağımsız ürünleri (alt tür ürünü olan ürünler) ve ürün çeşitlerini içerir. Aşağıdaki tablo eşlemeleri göstermektedir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | ad
PRODUCTDESCRIPTION | >> | açıklama
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | fiyat
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>msdyn\_sharedproductdetails öğesine serbest bırakılan ürünler V2

**msdyn\_sharedproductdetails** varlığı, Finance and Operations uygulamalarından ürünü tanımlayan ve ürünün finansal ve yönetim bilgilerini içeren alanlar içerir. Aşağıdaki tablo eşlemeleri göstermektedir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>msdyn_global ürünlerine tüm ürünler

Tüm ürünler varlığı, hem yayınlanmış ürünler hem de serbest bırakılmamış ürünler olmak üzere Finance and Operations uygulamalarındaki tüm ürünleri içerir. Bu ürünler Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir:

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>Ürün boyutları 

Ürün boyutları, ürün çeşidini tanımlamaya hizmet eden özelliklerdir. Dört ürün boyutu (Renk, Boyut, Stil ve Yapılandırma) ürün çeşitlerini tanımlamak amacıyla Common Data Service'a eşlenir. Aşağıdaki resimde Renk ürün boyutu için veri modeli gösterilmektedir. Aynı model Boyutlara, Stillere ve Yapılandırmalara da uygulanır. 

![Ürünler için veri modeli](media/dual-write-product-2.PNG)

### <a name="colors"></a>Renkler

Olası renkler Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>Boyutlar

Olası boyutlar Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>Stiller

Olası stiller Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>Yapılandırmalar

Olası yapılandırmalar Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
CONFIGURATIONID | \>\> | msdyn\_name

Ürünün farklı ürün boyutları (örneğin, ürün boyutu olarak Boyut ve Renk boyutu bulunan bir ana ürün) olduğunda, her ayrı ürün (her bir ürün çeşidi) bu ürün boyutlarının bir birleşimi olarak tanımlanır. Örneğin, ürün numarası B0001 extra small beden siyah tişört ve ürün numarası B0002 small beden siyah tişörttür. Bu durumda, ürün boyutlarının varolan birleşimleri tanımlanmıştır. Örneğin, önceki örnekteki Tişört extra small ve siyah, small ve siyah, medium ve siyah veya large ve siyah olabilir, ancak extra large ve siyah olamaz. Başka bir deyişle, bir ana ürünün alabileceği ürün boyutları belirtilir ve ürün çeşitleri bu değerlere dayalı olarak serbest bırakılabilir.

Bir ana ürünün alabileceği ürün boyutlarını izlemek için, aşağıdaki varlıklar oluşturulur ve her ürün boyutu için Common Data Service'ta eşlenir. Daha fazla bilgi için bkz. [Ürün bilgilerine genel bakış](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

### <a name="shared-product-color"></a>Paylaşılan ürün rengi

**Paylaşılan ürün rengi** varlığı, belirli bir ana ürünün sahip olabileceği renkleri gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Common Data Service'a taşınır. Aşağıdaki tablo eşlemeleri göstermektedir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>Paylaşılan ürün boyutu

**Paylaşılan ürün boyutu** varlığı, belirli bir ana ürünün sahip olabileceği boyutları gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Common Data Service'a taşınır. Aşağıdaki tablo eşlemeleri göstermektedir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>Paylaşılan ürün stili

**Paylaşılan ürün stili** varlığı, belirli bir ana ürünün sahip olabileceği stilleri gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Common Data Service'a taşınır. Aşağıdaki tablo eşlemeleri göstermektedir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>Paylaşılan ürün yapılandırması

**Paylaşılan ürün yapılandırması** varlığı, belirli bir ana ürünün sahip olabileceği yapılandırmaları gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Common Data Service'a taşınır. Aşağıdaki tablo eşlemeleri göstermektedir.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>Ürün numarası tanımlayıcısı barkodlar

Ürün barkodları, ürünleri benzersiz olarak tanımlamak için kullanılır. Aşağıdaki eşlemeler bu ürün barkodlarının Common Data Service'te kullanılabilir olmasını sağlamak için kullanılır.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARKOD | \> | msdyn\_name
BARKOD | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Varsayılan sipariş ayarları ve ürüne özgü varsayılan sipariş ayarları

Varsayılan sipariş ayarları maddelerin bulunduğu veya depolandığı tesisi ve ambarı, ticari veya stok yönetimi için kullanılacak minimum, maksimum, birden fazla ve standart miktarları, sağlama sürelerini, durdurma bayrağını ve sipariş taahhüt hesabını tanımlar. Bu bilgiler varsayılan sipariş ayarları ve ürüne özgü varsayılan sipariş ayarları varlığı kullanılarak CDS'de kullanılabilir olacaktır. [Varsayılan sipariş ayarları sayfasında](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings) işlev hakkında daha fazla bilgi bulabilirsiniz.

### <a name="default-order-settings"></a>Varsayılan sipariş ayarları

Aşağıdaki eşlemeler varsayılan sipariş ayarlarının Common Data Service'te kullanılabilir olmasını sağlamak için kullanılır.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>Ürüne özel varsayılan sipariş ayarları

Aşağıdaki eşlemeler ürüne özel varsayılan sipariş ayarlarının Common Data Service'te kullanılabilir olmasını sağlamak için kullanılır.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Ölçü birimi ve ölçü birimi dönüşümleri

Ölçü birimleri ve ilgili dönüştürmeleri, şemada gösterilen veri modeline uygun olarak Common Data Service'ta kullanılabilir olacaktır.

![Ürünler için veri modeli](media/dual-write-product-3.PNG)

Ölçü birimi kavramı, Finance and Operations uygulamaları ile diğer Dynamics 365 uygulamaları arasında entegre edilmiştir. Finance and Operations uygulamasındaki her birim sınıfı için Dynamics 365 uygulamasında bu birim sınıfına air birimleri içeren bir birim grubu oluşturulur. Her birim grubu için varsayılan bir temel birim de oluşturulur. 

### <a name="unit-of-measure"></a>Ölçü birimi

Aşağıdaki eşlemeler, Finance and Operations uygulamalarındaki ölçü birimlerinin Common Data Service'te kullanılabilir olması sağlamak için kullanılır.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | ad
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>Ölçü birimi dönüşümleri

Aşağıdaki eşlemeler, Finance and Operations uygulamalarındaki ölçü birimi dönüşümlerinin Common Data Service'te kullanılabilir olması sağlamak için kullanılır.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PAYDA | = | msdyn_denominator
PAY | = | msdyn_numerator
KATSAYI | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
YUVARLAMA | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol

### <a name="product-specific-unit-of-measure-conversions"></a>Ürüne özel ölçü birimi dönüşümleri

Aşağıdaki eşlemeler, Finance and Operations uygulamalarındaki ürüne özel ölçü birimi dönüşümlerinin Common Data Service'te kullanılabilir olması sağlamak için kullanılır.

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
PAYDA | = | msdyn_denominator
PAY | = | msdyn_numerator
KATSAYI | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
YUVARLAMA | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Ürün ilkeleri: boyut, izleme ve depolama grupları

Ürün ilkeleri, ürünleri ve özelliklerini stokta tanımlamak için kullanılan ilke kümeleridir. Ürün boyut grubu, ürün izleme boyut grubu ve depolama boyutu grubu ürün ilkesi olarak bulunabilir. 

### <a name="product-dimension-group"></a>Ürün boyut grubu

Ürünü hangi ürün boyutlarının tanımlayacağı tanımlayan ürün boyutu. Olası dört ürün boyutu grubu bulunur: yapılandırma, renk, boyut ve stil. Ürün boyutu grupları Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir. 

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>Ürün izleme boyutu grupları

Ürün izleme boyutu grubu, ürünü stokta izlemek için kullanılan yöntemi temsil eder. Bunlar Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir: 

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>Ürünler depolama boyutu grubu

Ürün depolama boyutu grubu, ürünün ambarda yerleşimini tanımlamak için kullanılan yöntemi temsil eder. Bunlar Common Data Service'te aşağıdaki eşlemeler aracılığıyla kullanılabilir: 

Kaynak alanı | Eşleme türü | Hedef alan
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation

