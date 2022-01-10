---
title: Ayrılmış Dual-write Application Orchestration paketi
description: Dual-write Application Orchestration paketi artık tek bir paket değildir ancak daha küçük paketlere ayrılmıştır. Bu konuda, her bir paketin içerdiği çözümler ve eşlemeler ve paketin diğer paketlere bağımlılığı açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3fe1b7707df72927fba78ee9659502cc62471799
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924878"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Ayrılmış Dual-write Application Orchestration paketi

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Daha önce, Dual-write Application Orchestration paketi aşağıdaki çözümleri içeren tek bir paketti:

- Dynamics 365 Notes
- Dynamics 365 Finance and Operations Common Anchor
- Dynamics 365 Finance and Operations Çift Yazma Varlık Eşlemeleri
- Dynamics 365 Varlık Yönetimi Uygulaması
- Dynamics 365 Varlık Yönetimi
- HCM Ortak
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations Common
- Dynamics 365 Company
- Döviz Kurları
- Field Service Common

Tek bir paket olması nedeniyle bu paket, müşteriler için "hep veya hiç" durumu oluşturmuştur. Ancak Microsoft artık bu paketi daha küçük paketlere ayırmıştır. Böylece müşteri, yalnızca gereksinim duyduğu çözümlerin paketlerini seçebilir. Örneğin, Microsoft Dynamics 365 Supply Chain Management müşterisiyseniz ve Dynamics 365 Human Resources, notlar ve varlık yönetimi ile tümleştirmeye gereksinim duymuyorsanız bu çözümleri yüklü çözümlerden hariç tutabilirsiniz. Temeldeki çözüm adları, yayıncı ve eşleme sürümleri aynı kaldığından bu değişiklik hataya neden olmaz. Mevcut yüklemeler yükseltilir.

![Ayrılmış paket.](media/separated-package-1.png)

Bu konuda, her bir paketin içerdiği çözümler ve eşlemeler ve paketin diğer paketlere bağımlılığı açıklanmaktadır.

## <a name="dual-write-application-core"></a>Dual-write Application Core

Dual-write Application Core paketi, kullanıcıların herhangi bir müşteri etkileşimi uygulaması olmadan çift yazmayı yüklemelerine ve yapılandırmalara olanak sağlar. Paket aşağıdaki beş çözümü içerir.

| Benzersiz ad                           | Görünen ad                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Common |
| CurrencyExchangeRates                 | Döviz Kurları                    |
| msdyn_DualWriteAppCoreMaps            | Çift yazma uygulamaları çekirdek varlık eşlemeleri   |
| msdyn_DualWriteAppCoreAnchor          | Çift yazma uygulamaları çekirdek sabit noktası        |

Bu pakette aşağıdaki eşlemeler mevcuttur.

| Finance and Operations uygulamaları     | Müşteri etkileşimi uygulamaları                    |
|---------------------------------|---------------------------------------------|
| Faaliyet birimi                  | msdyn_internalorganizations                 |
| Kuruluş hiyerarşisi          | msdyn_internalorganizationhierarchies       |
| Tüzel kişilikler                  | msdyn_internalorganizations                 |
| Tüzel kişilikler                  | cdm_companies                               |
| Kuruluş hiyerarşisi amaçları | msdyn_internalorganizationhierarchypurposes |
| Döviz kuru para birimi çifti     | msdyn_currencyexchangeratepairs             |
| Ad ekleri                    | msdyn_nameaffixes                           |
| Döviz kuru türü              | msdyn_exchangeratetypes                     |
| CDS Döviz Kurları              | msdyn_currencyexchangerates                 |
| Kuruluş hiyerarşisi türü     | msdyn_internalorganizationhierarchytypes    |
| Para birimleri                      | transactioncurrencies                       |
| Karma gerçeklik kılavuzları varlığı     | msmrw_guides                                |

**Bağımlılık bilgileri**

Dual-write Application Core paketinin diğer paketlere bağımlılığı yoktur.

## <a name="dual-write-human-resources"></a>Dual-write Human Resources

Dual-write Human Resources paketi, Human Resources verilerini eşitlemek için gereken çözümleri ve eşlemeleri içerir. Paket aşağıdaki üç çözümü içerir.

| Benzersiz ad                | Görünen ad                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM Ortak                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources varlık eşlemeleri |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources sabit noktası      |

Bu pakette aşağıdaki eşlemeler mevcuttur.

| Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları         |
|-----------------------------|----------------------------------|
| Etnik kökenler              | cdm_ethnicorigins                |
| Maaş iş işlevi   | cdm_jobfunctions                 |
| Pozisyonlar V2                | cdm_jobpositions                 |
| İşler                        | cdm_jobs                         |
| Maaş iş türü       | cdm_jobtypes                     |
| Dil kodları              | cdm_languages                    |
| Pozisyon türü               | cdm_positiontypes                |
| Pozisyon çalışan atamaları | cdm_positionworkerassignmentmaps |
| Gazilik durumu              | cdm_veteranstatuses              |
| Çalışan                      | cdm_workers                      |
| Şirket başına istihdam      | cdm_employments                  |

**Bağımlılık bilgileri**

Dual-write Human Resources paketi, Dual-write Application Core paketine bağlıdır. Bu nedenle, Dual-write Human Resources paketini yüklemeden önce Dual-write Application Core paketini yüklemeniz gerekir.

## <a name="dual-write-supply-chain"></a>Dual-write Supply Chain

Dual-write Supply Chain paketi, Supply Chain Management verilerini eşitlemek için gereken çözümleri ve eşlemeleri içerir. Paket aşağıdaki üç çözümü içerir.

| Benzersiz ad                                | Görünen ad                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management genişletilmiş varlık eşlemeleri |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management genişletilmiş sabit noktası      |

Bu pakette aşağıdaki eşlemeler mevcuttur.

| Finance and Operations uygulamaları                 | Müşteri etkileşimi uygulamaları                      |
|---------------------------------------------|-----------------------------------------------|
| Birimler                                       | uoms                                          |
| CDS satış siparişi başlıkları                     | salesorders                                   |
| CDS satış siparişi satırları                       | salesorderdetails                             |
| CDS satış teklifi başlığı                  | teklifler                                        |
| CDS satış teklifi satırları                   | quotedetails                                  |
| CDS serbest bırakılan farklı ürünler              | ürünler                                      |
| Ambar bölgeleri                             | msdyn_warehousezones                          |
| Ambar bölge grupları                       | msdyn_warehousezonegroups                     |
| Ambar iş satırları                        | msdyn_warehouseworklines                      |
| Ambar işi başlıkları                      | msdyn_warehouseworkheaders                    |
| Ambarlar                                  | msdyn_warehouses                              |
| Stok koridoru                             | msdyn_warehouseaisles                         |
| Birim dönüştürmeleri                            | msdyn_unitofmeasureconversions                |
| Teslimat koşulları                           | msdyn_termsofdeliveries                       |
| Teslimat şekilleri                           | msdyn_shipvias                                |
| Ana ürün stilleri                       | msdyn_sharedproductstyles                     |
| Satış faturası satırları V2                      | invoicedetails                                |
| Satış faturası başlıkları V2                    | faturalar                                      |
| Ana ürün boyutları                        | msdyn_sharedproductsizes                      |
| Serbest bırakılan ürünler V2                        | msdyn_sharedproductdetails                    |
| Ana ürün konfigürasyonları               | msdyn_sharedproductconfigurations             |
| Ana ürün renkleri                       | msdyn_sharedproductcolors                     |
| Satış siparişi kaynak kodları                    | msdyn_salesorderorigins                       |
| Ürün girişi başlığı                      | msdyn_purchaseorderreceipts                   |
| Ürün girişi satırı                        | msdyn_purchaseorderreceiptproducts            |
| Satınalma siparişi başlıkları V2                   | msdyn_purchaseorders                          |
| CDS satın alma sipariş satırı geçici silinen varlığı | msdyn_purchaseorderproducts                   |
| CDS satınalma sipariş satırı varlığı              | msdyn_purchaseorderproducts                   |
| İzleme boyutu grupları                   | msdyn_producttrackingdimensiongroups          |
| Stiller                                      | msdyn_productstyles                           |
| Depolama boyut grupları                    | msdyn_productstoragedimensiongroups           |
| Ürüne özel birim dönüşümleri           | msdyn_productspecificunitofmeasureconversions |
| Ürün varsayılan sipariş ayarları V2           | msdyn_productspecificdefaultordersettings     |
| Boyutlar                                       | msdyn_productsizes                            |
| Ürün boyut grupları                    | msdyn_productdimensiongroups                  |
| Varsayılan sipariş ayarları                      | msdyn_productdefaultordersettings             |
| Yapılandırmalar                              | msdyn_productconfigurations                   |
| Tüm ürünler                                | msdyn_globalproducts                          |
| Renkler                                      | msdyn_productcolors                           |
| Ürün kategori hiyerarşisi rolleri            | msdyn_productcategoryhierarchyroles           |
| Ürün kategori hiyerarşileri                | msdyn_productcategoryhierarchies              |
| Ürün kategorisi atamaları                | msdyn_productcategoryassignments              |
| Ürün kategorileri                          | msdyn_productcategories                       |
| Ambar yerleşimleri                         | msdyn_inventorylocations                      |
| CDS eldeki stok                            | msdyn_inventoryonhandentries                  |
| Ürün kategorileri                          | msdyn_productcategories                       |
| CDS eldeki stok                            | msdyn_inventoryonhandrequests                 |
| Ürün Numarası Tanımlanan Barkod           | msdyn_productbarcodes                         |
| Bağlılık programı kartı                                | msdyn_loyaltycards                            |
| Bağlılık programı ödül puanları                       | msdyn_loyaltyrewardpoints                     |
| Fiyat müşteri grupları                       | msdyn_pricecustomergroups                     |
| Tesisler                                       | msdyn_operationalsites                        |
| CDS satış teklifi satırları                   | quotedetails                                  |
| CDS satış siparişi satırları                       | salesorderdetails                             |

**Bağımlılık bilgileri**

Dual-write Supply Chain paketi aşağıdaki üç pakete bağlıdır. Bu nedenle, Dual-write Supply Chain paketini yüklemeden önce bu paketleri yüklemeniz gerekir.

- Dual-write Application Core paketi
- Dual-write Finance paketi
- Dual-write Human Resources paketi

## <a name="dual-write-finance"></a>Dual-write Finance

Dual-write Finance paketi, Dynamics 365 Finance verilerini eşitlemek için gereken çözümleri ve eşlemeleri içerir. Paket aşağıdaki dört çözümü içerir.

| Benzersiz ad                            | Görünen ad                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance extended varlık eşlemeleri |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance extended sabit noktası      |

Bu pakette aşağıdaki eşlemeler mevcuttur.

| Finance and Operations uygulamaları             | Müşteri etkileşimi uygulamaları        |
|-----------------------------------------|---------------------------------|
| Stopaj vergisi grupları                  | msdyn_withholdingtaxgroups      |
| CDS Contacts V2 (Müşteri)              | ilgili kişiler                        |
| CDS Contacts V2 (Satıcı)                | ilgili kişiler                        |
| Müşteriler V3                            | ilgili kişiler                        |
| Stopaj vergisi kodları                   | msdyn_withholdingtaxcodes       |
| Satıcılar V2                              | msdyn_vendors                   |
| Satıcı ödeme yöntemi                   | msdyn_vendorpaymentmethods      |
| Satıcı grupları                           | msdyn_vendorgroups              |
| Hesap planı                       | msdyn_chartofaccountses         |
| Satış vergisi genel muhasebe deftere nakil grupları V2      | msdyn_taxpostinggroups          |
| Madde satış vergisi grubu                    | msdyn_taxitemgroups             |
| Satış vergisi grupları                        | msdyn_taxgroups                 |
| Satış vergisi muafiyet kodu varlığı CDS        | msdyn_taxexemptcodes            |
| Müşteri grupları                         | msdyn_customergroups            |
| Müşteri ödeme yöntemi                 | msdyn_customerpaymentmethods    |
| Mali boyutlar                    | msdyn_dimensionattributes       |
| Satış vergisi makamları                   | msdyn_taxauthorities            |
| Mali boyut biçimi              | msdyn_financialdimensionformats |
| Mali takvim dönemi                  | msdyn_fiscalcalendarperiods     |
| Mali takvim tümleştirme varlığı      | msdyn_fiscalcalendars           |
| Mali takvim yılı tümleştirme varlığı | msdyn_fiscalcalendaryears       |
| Ödeme koşulları                        | msdyn_paymentterms              |
| Ödeme planı                        | msdyn_paymentschedules          |
| Ödeme planı satırları                  | msdyn_paymentschedulelines      |
| Ödeme günleri CDS                        | msdyn_paymentdays               |
| Ödeme günü satırları CDS V2                | msdyn_paymentdaylines           |
| Ana hesap                            | msdyn_mainaccounts              |
| Ana hesap kategorileri                 | msdyn_mainaccountcategories     |
| Genel muhasebe                                  | msdyn_ledgers                   |
| Müşteriler V3                            | hesaplar                        |

**Bağımlılık bilgileri**

Dual-write Finance paketi, Dual-write Application Core paketine bağlıdır. Bu nedenle, Dual-write Finance paketini yüklemeden önce Dual-write Application Core paketini yüklemeniz gerekir.

## <a name="dual-write-notes"></a>Dual-write Notes

Dual-write Notes paketi, not veya ek açıklama verilerini eşitlemek için gereken çözümleri ve eşlemeleri içerir. Paket aşağıdaki dört çözümü içerir.

| Benzersiz ad                  | Görünen ad                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 notlar genişletilmiş    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 notlar varlık eşlemeleri |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 notlar sabit noktası      |

Bu pakette aşağıdaki eşlemeler mevcuttur.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Satış siparişi başlığı belge ekleri    | ek açıklamalar         |
| Müşteri ekleri                       | ek açıklamalar         |
| Satıcı belgesi ekleri                | ek açıklamalar         |
| Satın alma siparişi başlığı belge ekleri | ek açıklamalar         |

**Bağımlılık bilgileri**

Dual-write Notes paketi aşağıdaki iki pakete bağlıdır. Bu nedenle, Dual-write Notes paketini yüklemeden önce bu paketleri yüklemeniz gerekir.

- Dual-write Application Core paketi
- Dual-write Finance paketi

## <a name="dual-write-asset-management"></a>Dual-write Asset Management

Dual-write Asset Management paketi, Supply Chain Management veya Dynamics 365 Field Service'ten varlık verilerini eşitlemek için gereken çözümleri ve eşlemeleri içerir. Paket aşağıdaki dört çözümü içerir.

| Benzersiz ad                          | Görünen ad                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 Varlık Yönetimi             |
| Dynamics365AssetManagementApp        | Dynamics365 Varlık Yönetimi Uygulaması          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 Varlık Yönetimi varlık eşlemeleri |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 Varlık Yönetimi sabit noktası      |

Bu pakette aşağıdaki eşlemeler mevcuttur.

| Finance and Operations uygulamaları                           | Müşteri etkileşimi uygulamaları                |
|-------------------------------------------------------|-----------------------------------------|
| Varlık yönetimi garanti                             | msdyn_warranties                        |
| Varlık yönetimi modelleri                               | msdyn_models                            |
| Varlık yönetimi üreticiler                        | msdyn_manufacturers                     |
| Varlık yönetimi işlem yapılacak yerleşim türleri            | msdyn_functionallocationtypes           |
| Varlık yönetimi işlem yapılacak yerleşimler                 | msdyn_functionallocations               |
| Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü durumları | msdyn_functionallocationlifecyclestates |
| Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü modelleri | msdyn_functionallocationlifecyclemodels |
| Varlık yönetimi varlıkları                               | msdyn_customerassets                    |
| Varlık yönetimi varlık türleri                          | msdyn_customerassetcategories           |
| Varlık yönetimi varlık yaşam döngüsü durumları               | msdyn_assetlifecyclestates              |
| Varlık yönetimi varlık yaşam döngüsü modelleri               | msdyn_assetlifecyclemodels              |

**Bağımlılık bilgileri**

Dual-write Asset Management paketi, Dual-write Application Core paketine bağlıdır. Bu nedenle, Dual-write Asset Management paketini yüklemeden önce Dual-write Application Core paketini yüklemeniz gerekir.

## <a name="packages-required-for-project-operations"></a>Project Operations için gerekli paketler
Project Operations aşağıdaki paketlere bağlıdır. Bu nedenle, Project Operations paketini yüklemeden önce bu paketleri yüklemeniz gerekir.

- Dual-write Application Core paketi
- Dual-write Finance paketi
- Dual-write Supply Chain paketi
- Dual-write Asset Management paketi
- Dual-write Human Resources paketi
