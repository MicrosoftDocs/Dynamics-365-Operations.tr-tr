---
title: Varlık bağımlılığı zinciri (eşitleme sırası)
description: Bu konu, ilk verileri oluşturmak için izlemeniz gereken eşitleme sırasını belirtir.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275499"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Varlık bağımlılığı zinciri (eşitleme sırası)

[!include [banner](../../includes/banner.md)]

Bu konu, **ilk eşitleme** özelliği tarafından sağlanan varlık bağımlılıklarını kullanmıyorsanız, ilk veriyi oluşturmak için izlemeniz gereken eşitleme sırasını belirtir. **ilk eşitlemeyi** kullanmıyorsanız, her varlık eşlemeyi ayrı olarak çalıştırmanız gerekir.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management varlıkları

Supply Chain Management için aşağıdaki varlıklar etkinleştirmeniz gereken sırada listelenmişlerdir.

| Çift-yazma sayfasında eşleme adı | Supply Chain Management'ta varlık meta verisi | Common Data Service İçinde varlık meta veri adı | Notlar |
|---|---|---|---|
| Birimler ... uom                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Birim dönüştürmeleri ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Tüm ürünler ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Ürün boyut grupları ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Depolama boyutu grupları ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| İzleme boyutu grupları ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Renkler ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Boyutlar ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Stiller ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Yapılandırmalar ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Serbest bırakılan ürünler V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service serbest bırakılan ayrı ürünler ... ürünler                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | ürün                                      | |
| Ürün Numarası Tanımlanan Barkod ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Varsayılan sipariş ayarları ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Ürün varsayılan sipariş ayarları V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Ürüne özel birim dönüşümleri ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Siteler ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Ambarlar ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Bkz. [not 1](#scm-notes). |
| Ana ürün renkleri ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Ana ürün boyutları ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Ana ürün stilleri ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Ana ürün yapılandırmaları ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Ürün kategorileri ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Bkz. [not 2](#scm-notes). |
| Ürün kategorisi atamaları ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Ürün kategorisi hiyerarşileri ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Ürün kategorisi hiyerarşi rolleri ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Stok koridoru ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Ambar bölgeleri ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Ambar bölge grupları ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Ambar yerleşimleri ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Bkz. [not 3](#scm-notes). |
| Ambar iş başlıkları ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Ambar iş satırları ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Bkz. [not 4](#scm-notes). |
| Teslimat şekilleri ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Teslimat koşulları ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Satış siparişi kaynak kodları ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service satış siparişi başlıkları ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service satış siparişi satırları ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service satış teklifi başlığı ... teklifler                               | SalesQuotationHeaderCommon Data ServiceEntity          | teklif                                        | |
| Common Data Service satış teklifi satırları ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Satış faturası başlıkları V2 ... faturalar                                               | SalesInvoiceHeaderV2Entity                             | fatura                                      | |
| Satış faturası satırları V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Eşlemeye özel notlar

1. Kendinden bağımlılık nedeniyle, başlangıç eşitlemesini iki kez çalıştırmanız gerekebilir.
2. Varsayılan olarak, üst-alt öğe ilişkisi ("akıllı" sıralama platform tarafından işlenmediği) için ilk eşitleme kapalıdır. Bu nedenle, varolan ürün kategorilerinin el ile eşitlenmeli (örneğin kategori açıklamasını güncelleştirerek) doğru sırada (önce kök kategorisi, sonra alt öğeleri ve alt öğelerinin alt öğeleri). **Ürün bilgi yönetimi \> Kurulum \> Kategoriler ve öznitelikler \> Kategori hiyerarşisi**'ne gidin. **Kategori hiyerarşileri** sayfasında, her bir hiyerarşiyi seçebilir ve içindeki ürün kategorilerini görebilirsiniz.
3. Boş **ItemNumberInLocation** arama alanlarının eşlemesi ve birinci, ikinci ve üçüncü ek ambar bölgeleri ilk eşitlemenin başarısız olmasına neden olacak. Bu nedenle, Bu eşlemeler şimdilik kaldırılır.
4. Boş **CaptureWeight** alanının eşlemesi, ilk eşitlemenin başarısız olmasına neden olur. Bu nedenle, Bu eşleme şimdilik kaldırılır.

### <a name="setup-related-information"></a>Kurulumla ilgili bilgiler

+ Kayıtlar, Dynamics 365'deki model kullanımlı uygulamalardaki **ürünler** varlığı içinde ilk oluşturulduğunda, bunlar **taslak** durumuna sahiptirler. Durumu **etkin** olarak değiştirmek için, model temelli uygulamada **Ayarlar \> Yönetim \> Sistem Ayarları \>Satışlar**'a gidin, **etkin durumda ürün oluştur** seçeneğini **Evet** olarak ayarlayın.
+ Dynamics 365'te veya Common Data Service'de model kullanımlı uygulamalarda **Ürün** varlığı içinde ikili yazmayı etkinleştirmeden önce kayıt oluşturursanız, bu kayıtlar yalnızca **şirket** dahil olmak üzere tüm anahtar Finance and Operations uygulamadaki verilerle eşleşiyorsa güncelleştirilir.
+ **Ürün** varlığının eşitlenmesi tek yönlü, Finance and Operations uygulamalardan to Common Data Service'e  yapılır. Dynamics 365 ' te model kullanımlı uygulamalardaki **ürünler** varlığında eşlenen bir alan güncelleştirildiğinde, Finance and Operations uygulamadan bir sonraki eşitleme sırasında güncelleştirme geçersiz kılınır.

### <a name="known-issues"></a>Bilinen sorunlar

- Bir Finance and Operations uygulamadaki bir birim silindiğinde hata oluşur. Ölçü birimleri Finance and Operations uygulamadan Common Data Service'e eşitlendiğinde belirli bir sınıfın ilk birimi birincil birim olarak oluşturulur ve silme işlemi önleyecektir.

    **Azaltma:** önce Common Data Service'de birimi silin. Böylece, Finance and Operations uygulamasında silinebilir.

- Bir operasyonel site Common Data Service'te silindiğinde hata oluşur. Hata iletisi, "bilgi günlüğü: Uyarı: birincil adres silinemez.; Uyarı: aşağıdaki veri kaynağı için doğrulama başarısız olduğu için, varlık kaydı silinemedi: InventSiteLogisticsLocation (InventSiteLogisticsLocation). " Bu hataya, Finance and Operations uygulamadaki veri varlığındaki bir sorun neden olmaktadır.

    **Azaltıcı etken:** Finance and Operations uygulamasında siteyi silebilirsiniz. İlgili ikili yazma eşlemesi çalışıyorsa, site Common Data Service'te silinir.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance varlıkları

Dynamics 365 Finance için aşağıdaki varlıklar etkinleştirmeniz gereken sırada listelenmişlerdir.

| Çift-yazma sayfasında eşleme adı | Finance İçinde varlık meta veri adı | Common Data Service İçinde varlık meta veri adı | Notlar |
|---|---|---|---|
| Para birimleri ... transactioncurrencies                                            | CurrencyEntity                              | Para Birimi                                   | |
| Döviz kuru türü ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Döviz kuru para birimi çifti ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service Döviz Kurları ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Bkz. [not 1](#fin-notes). |
| Mali takvim tümleştirme varlığı ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Mali takvim yıl tümleştirme varlığı ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Mali takvim dönemi ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Kuruluş hiyerarşisi türü ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Bkz. [not 1](#fin-notes). |
| Kuruluş hiyerarşisi amaçları ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Bkz. [not 1](#fin-notes). |
| Tüzel kişilikler ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Bkz. [not 1](#fin-notes). |
| Tüzel kişilikler ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Faaliyet birimi ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Bkz. [not 1](#fin-notes). |
| Kuruluş hiyerarşisi - yayımlandı ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Bkz. [not 1](#fin-notes). |
| Ad ekleri ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Ödeme günleri Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Ödeme günü satırları Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Ödeme planı ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Ödeme planı satırları ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Ödeme koşulları ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Müşteri ödeme yöntemi ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Satıcı ödeme yöntemi ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Müşteri grupları ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Satıcı grupları ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Satış vergisi grupları ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Madde satış vergisi grubu ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Satış vergisi genel muhasebe deftere nakil grupları V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Satış vergisi muafiyet kodu varlığı Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Satış vergisi makamları ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Satış vergisi kodları ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Bkz. [not 1](#fin-notes). |
| Mali boyut biçimi ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Mali boyutlar ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Stopaj vergisi grupları ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Stopaj vergisi kodları ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Hesap planı ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Genel muhasebe ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Bkz. [not 1](#fin-notes). |
| Ana hesap kategorileri ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Ana hesap ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Müşteriler V3 ... hesaplar                                                       | CustCustomerV3Entity                        | hesap                                    | Bkz. [not 2](#fin-notes). |
| Müşteriler V3 ... ilgili kişiler                                                       | CustCustomerV3Entity                        | iletişim                                    | Bkz. [not 3](#fin-notes). |
| Satıcılar V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Bkz. [not 2](#fin-notes). |
| Common Data Service İlgili Kişileri V2 ... kişiler                                    | smmContactPersonCommon Data ServiceV2Entity | iletişim                                    | Bkz. [not 4](#fin-notes). |
| Common Data Service İlgili Kişileri V2 ... kişiler                                    | smmContactPersonCommon Data ServiceV2Entity | iletişim                                    | Bkz. [not 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Eşlemeye özel notlar

1. Tek yönlü eşitleme Finance and Operations uygulamalarından Common Data Service'e yapılır.
2. Kendinden bağımlılık nedeniyle, başlangıç eşitlemesini birden daha fazla kez çalıştırmanız gerekebilir. Common Data Service'deki **Hesaplar** sayfasını kullanarak bir hesap oluştururken, ilişki türü olarak **Müşteri**'yi seçtiğinizden emin olun. İlk eşitleme sırasında **birincil kişi** alanla ilgili sorunlarla karşılaşırsanız, bu alanı eşleştirmeden kaldırın ve sonra ilk eşitlemeyi yeniden çalıştırın. İlk eşitleme başarılı bir şekilde tamamlandıktan sonra, eşlemeyi durdurun ve **birincil kişi** alanını yeniden ekleyin. Sonra eşlemeyi başlatın, ancak ilk eşitlemeyi atlayın. **Birincil kişi** alanın değeri ilk eşitlemeye dahil edilmeyecektir ve değerleri el ile geçirmeniz gerekir.
3. **Kişi** türünde bir müşteri oluşturmaya çalıştığınızda, Common Data Service' de **ilgili kişiler** sayfasında, **satış yapılabilir** seçeneğini **Evet** olarak ayarladığınızdan emin olun.
4. Bu eşleme, müşteri ilgili kişilerini bağlamak için iki yüze filtre uygulama. Eşleme ayrıntılarını açın, **satışlar.ilgili kişi** varlık adının yanındaki filtre düğmesini (huni sembolü) seçin ve dosya ölçütlerinin **msdyn_contactforvendor eq true and msdyn_sellable eq false** içerdiğinden emin olun.
5. Bu eşleme, satıcı ilgili kişilerini bağlamak için iki yüze filtre uygulama. Eşleme ayrıntılarını açın, **satışlar.ilgili kişi** varlık adının yanındaki filtre düğmesini (huni sembolü) seçin ve filtre ölçütlerinin **msdyn_contactforvendor eq true and msdyn_sellable eq false** içerdiğinden emin olun. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources varlıkları

Dynamics 365 Human Resources için aşağıdaki varlıklar etkinleştirmeniz gereken sırada listelenmişlerdir.

| Çift-yazma sayfasında eşleme adı | İnsan Kaynakları varlık meta veri adı | Common Data Service İçinde varlık meta veri adı | Notlar |
|---|---|---|---|
| cdm_jobfunction - İş İşlevi                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - İş Tipleri                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - İşler                                               |                                   | cdm_jobs                         | |
| cdm_jobs - İş Ayrıntıları                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - Pozisyon Türü                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Temel pozisyon                              | HcmPositionBaseEntity             | cdm_jobposition                  | Bkz. [not 1](#hr-notes). |
| cdm_jobposition - Pozisyon Ayrıntıları                            | HcmPositionDetailEntity           | cdm_jobposition                  | Bkz. [not 1](#hr-notes). |
| cdm_jobposition - Pozisyon Süresi                           | HcmPositionDurationEntity         | cdm_jobposition                  | Bkz. [not 1](#hr-notes). |
| cdm_jobposition - Pozisyon Hiyerarşileri                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Bkz. [not 1](#hr-notes). |
| cdm_veteranstatus - Gazilik Durumu                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - Etnik Kökeni                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Dil Kodu                              |                                   | cdm_languagecode                 | |
| cdm_worker - Çalışan                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - İstihdamlar                                 |                                   | cdm_employments                  | |
| cdm_employments - İstihdam Ayrıntısı                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Pozisyon Çalışan Atamaları | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Bkz. [not 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Eşlemeye özel notlar

1. Bir Common Data Service varlık birçok Finance and Operations uygulama varlığı ile eşlendi.
2. Bu eşlemede kendine ait bir referans var.

## <a name="asset-management-entities"></a>Kıymet Yönetimi varlıkları

Dynamics 365 Supply Chain Management için Varlık Yönetimi aşağıdaki varlıklar etkinleştirmeniz gereken sırada listelenmişlerdir.

| Çift-yazma sayfasında eşleme adı | Kıymet Yönetimi'ne varlık meta verisi | Common Data Service İçinde varlık meta veri adı | Notlar |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Varlık yönetimi varlık yaşam döngüsü durumları               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Varlık yönetimi varlık yaşam döngüsü modelleri               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü modelleri | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü durumları | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Varlık yönetimi varlık türleri                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Varlık yönetimi işlem yapılacak yerleşim türleri            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Varlık yönetimi işlem yapılacak yerleşimler                 | msdyn_functionallocations                | Bkz. [not](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Varlık yönetimi varlıkları                               | msdyn_customerassets                     | Bkz. [not](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Varlık yönetimi üreticiler                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Varlık yönetimi modelleri                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Varlık yönetimi garanti                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Eşlemeye özel notlar

- Kendinden bağımlılık nedeniyle, başlangıç eşitlemesini birden daha fazla kez çalıştırmanız gerekebilir.
