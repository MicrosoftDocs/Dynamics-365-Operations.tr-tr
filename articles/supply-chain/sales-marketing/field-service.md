---
title: "Field Service için Microsoft Dynamics 365 ile tümleştirme"
description: "Bu konu Field Service için Microsoft Dynamics 365 ile tümleştirmeye genel bakış sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: tr-tr
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Field Service için Microsoft Dynamics 365 ile tümleştirme

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations Finance and Operations ile Microsoft Dynamics 365 for Field Service arasında iş süreçlerinin eşitlenmesini sağlar. Tümleştirme senaryoları iş süreçlerinin eşitlenmesine olanak tanımak için genişletilebilir Veri tümleştirici şablonları ve Common Data Service (CDS) kullanılarak yapılandırılır.
Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel iş ihtiyaçlarını karşılamak üzere eşlenebilir. 

Field Service tümleştirmesi, mevcut aday-nakit işlevinin üzerine inşa olur.

![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/field-service-integration.png)

Field Service and Finance ile Operations arasındaki tümleştirmenin birinci aşaması Field Service'taki iş emirlerinin ve sözleşmelerin Finance and Operations'da faturalandırılmasını sağlamaya odaklanır. Desteklenen akış Field Service'da başlar; iş emirlerinden alınan bilgiler Finance and Operations'a satış siparişleri olarak eşitlenir. Finance and Operations'da satış siparişleri fatura belgeleri oluşturmak üzere faturalandırılır. Ayrıca, Field Service sözleşme faturalarındaki bilgiler Finance and Operations'a eşitlenir. Microsoft Dynamics 365 Veri tümleştirici verileri özelleştirilebilir projeleri kullanarak eşitler. Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel gereksinimleri karşılamak üzere eşlenebilir.

Field Service ile Finance and Operations arasındaki tümleştirmenin birinci aşaması aşağıdaki öğelerin eşitlenmesini sağlar:

- [Finance and Operations'taki ürünler ile Field Service'da Ürün Türü bilgisi içeren ürünler](field-service-product.md)
- [Field Service'taki iş emirleri ile Finance and Operations'taki satış siparişleri](field-service-work-order.md)
- [Field Service'taki faturalar ile Finance and Operations'taki serbest metin faturaları](field-service-invoice.md)

Bir iş emrini Field Service ile Finance and Operations arasında nasıl eşitleyeceğinize ilişkin bir örnek görmek için kısa YouTube videosunu izleyin: [İş emrini Microsoft Dynamics 365 Tümleştirmesi ile eşitleme](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations için sistem gereksinimleri
Field Service tümleştirmesi aşağıdaki sürümleri destekler:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) veya üstü

- Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) Nisan 2018'de yayımlanmıştır ve Platform Güncelleştirmesi 15 (7.0.4841.35234) ile birlikte 8.0.30.8020 uygulama derleme numarasına sahiptir. 

## <a name="system-requirements-for-field-service"></a>Field Service için sistem gereksinimleri
Field Service tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 veya üstü

- Dynamics 365 for Field Service sürüm 1612 (9.0.1.733) (DB 9.0.1.733) çevrimiçi veya üstü sürüm.
- Dynamics 365, sürüm 1.15.0.1 veya üstü sürüm için Müşteri Adayından Nakde (P2C) çözümü. Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)'tan indirilebilir.
- Dynamics 365, sürüm 1.0.0.0 veya üstü sürüm için tümleştirme çözümü. Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration)'tan indirilebilir.

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Microsoft Dynamics 365 for Field Service tümleştirmesi, stok ve proje bilgisi dahil

Saha teknisyenlerine, Finance and Operations'tan stok bilgisi hakkında içgörü vermeye odaklı bu ikinci aşamadaki ek işlev, onların stok düzeylerini güncelleştirmelerine ve malzeme aktarmaları yapmalarına olanak tanır. Ek olarak, satılan malların kurulumunu yapan veya hizmet veren şirketleri, daha iyi kontrol ve tam satışa ve projelerle tümleştirmeye daha iyi görünürlük sahibi olacaklardır.

### <a name="functionality-includes-integration-of"></a>İşlev şunların tümleştirmesini içerir:
- Ambar bilgisi
- Eldeki stok bilgileri
- Stok transferleri
- Stok düzeltmeleri
- Dynamics 365 for Field Service iş emirleri ile bağlantılı Dynamics 365 for Finance and Operations projeleri
- Dynamics 365 for Field Service iş emirleri ile bağlantılı Dynamics 365 for Finance and Operations projeleri, bu proje numarasını Dynamics 365 for Finance and Operations satış siparişlerine uygular ve projeden faturalamaya olanak tanır. 

![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Field Service ile Finance and Operations arasındaki tümleştirmenin ikinci aşaması aşağıdaki şablonların eşitlenmesini sağlar:
- Ambarlar (Fin and Ops'tan Field Service'a) - Finance and Operations'tan Field Service'a ambarlar [Gelişmiş Sorgu] 
- Ürün Stoku (Fin and Ops'tan Field Service'a) - Finance and Operations'tan Field Service'a Stok düzeyi bilgisi [Gelişmiş Sorgu] 
- Stok Ayarlama (Field Service'tan Fin and Ops'a) - Stok ayarlama Field Service'tan Finance and Operations'a [Gelişmiş Sorgu] 
- Stok Aktarmaları (Field Service'tan Fin and Ops'a) - Stok aktarmaları Field Service'tan Finance and Operations'a [Gelişmiş Sorgu] 
- Projeler (Fin and Ops'tan Field Service'a) - Finance and Operations'tan Field Service'a proje listesi 
- Proje ile İş Emirleri (Field Service'tan Fin and Ops'a) - Field Service'tan Sales'a iş emirleri Finance and Operations'ta, Proje desteği ile [Gelişmiş Sorgu] 
- Stok birimi ile Field Service Ürünleri (Fin and Ops'tan Sales'a) - Finance and Operations 'Satılabilir serbest bırakılmış ürünler'den Sales 'Ürünleri'ne, Field Service için, Stok birimi dahil 

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations için sistem gereksinimleri
Field Service tümleştirmesi aşağıdaki sürümleri destekler:

- Dynamics 365 for Finance and Operations sürüm 8.1.2 (Aralık 2019) Aralık 2019'de yayımlanmıştır ve Platform Güncelleştirmesi 22 (7.0.5095) ile birlikte 8.1.195 uygulama derleme numarasına sahiptir. 

## <a name="system-requirements-for-field-service"></a>Field Service için sistem gereksinimleri
Field Service tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

- Field Service for Dynamics 365 (sürüm 8.2.0.286) veya daha sonraki bir sürüm, Dynamics 365 9.1.x üzerinde - Kasım 2018'de yayınlanmış
- Dynamics 365, sürüm 1.15.0.1 veya üstü sürüm için Müşteri Adayından Nakde (P2C) çözümü. Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)'tan indirilebilir.
- 'Field Service Tümleştirmesi, Proje ve Stok' çözümü, Dynamics 365, sürüm 2.0.0.0 veya sonraki bir sürüm için. Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2)'tan indirilebilir.

