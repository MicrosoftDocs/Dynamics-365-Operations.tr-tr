---
title: "Field Service için Microsoft Dynamics 365 ile tümleştirme"
description: "Bu konu Field Service için Microsoft Dynamics 365 ile tümleştirmeye genel bakış sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
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
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: tr-tr
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Field Service için Microsoft Dynamics 365 ile tümleştirme

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations Finance and Operations ile Microsoft Dynamics 365 for Field Service arasında iş süreçlerinin eşitlenmesini sağlar. Tümleştirme senaryoları iş süreçlerinin eşitlenmesine olanak tanımak için genişletilebilir Veri tümleştirici şablonları ve Common Data Service (CDS) kullanılarak yapılandırılır.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/field-service-integration.png)](./media/field-service-integration.png)

Field Service and Finance ile Operations arasındaki tümleştirmenin birinci aşaması Field Service'taki iş emirlerinin ve sözleşmelerin Finance and Operations'da faturalandırılmasını sağlamaya odaklanır. Desteklenen akış Field Service'da başlar; iş emirlerinden alınan bilgiler Finance and Operations'a satış siparişleri olarak eşitlenir. Finance and Operations'da satış siparişleri fatura belgeleri oluşturmak üzere faturalandırılır. Ayrıca, Field Service sözleşme faturalarındaki bilgiler Finance and Operations'a eşitlenir. Microsoft Dynamics 365 Veri tümleştirici verileri özelleştirilebilir projeleri kullanarak eşitler. Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel gereksinimleri karşılamak üzere eşlenebilir.

Field Service ile Finance and Operations arasındaki tümleştirmenin birinci aşaması aşağıdaki öğelerin eşitlenmesini sağlar:

- [Finance and Operations'taki ürünler ile Field Service'da Ürün Türü bilgisi içeren ürünler](field-service-product.md)
- [Field Service'taki iş emirleri ile Finance and Operations'taki satış siparişleri](field-service-work-order.md)
- [Field Service'taki faturalar ile Finance and Operations'taki serbest metin faturaları](field-service-invoice.md)

Bir iş emrini Field Service ile Finance and Operations arasında nasıl eşitleyeceğinize ilişkin bir örnek görmek için YouTube'daki kısa videoyu izleyin: [Dynamics 365 for Field Service ile Finance and Operations arasında bir iş emrini eşitleme](https://www.youtube.com/watch?v=hAB4TDVMjxU).

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations için sistem gereksinimleri
Field Service tümleştirmesi aşağıdaki sürümleri destekler:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) veya üstü

- Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) Nisan 2018'de yayımlanmıştır ve Platform Güncelleştirmesi 15 (7.0.4841.35234) ile birlikte 8.0.30.8020 uygulama derleme numarasına sahiptir. 

## <a name="system-requirements-for-field-service"></a>Field Service için sistem gereksinimleri
Field Service tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 veya üstü

- Dynamics 365 for Field Service sürüm 1612 (9.0.1.733) (DB 9.0.1.733) çevrimiçi veya üstü sürüm.
- Dynamics 365, sürüm 1.15.0.1 veya üstü sürüm için Müşteri Adayından Nakde (P2C) çözümü. Çözüm [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)'tan indirilebilir.
- Dynamics 365, sürüm 1.0.0.0 veya üstü sürüm için tümleştirme çözümü. Çözüm [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration)'tan indirilebilir.

