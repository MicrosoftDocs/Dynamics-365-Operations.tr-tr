---
title: Müşteri adayından nakde
description: Bu konu, Dynamics 365 Supply Chain Management ve Dynamics 365 Sales arasında Aday'dan nakite çözümüne genel bakış sağlar.
author: ChristianRytt
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: bb928a14d231bef1255612194ec9fdeb9be8f611d26aa4dfbf3efaec8a8d3e9f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726693"
---
# <a name="prospect-to-cash"></a>Aday müşteriden nakde

[!include [banner](../includes/banner.md)]

Aday'dan nakite çözümü, Dynamics 365 Supply Chain Management ve Dynamics 365 Sales arasında doğrudan eşitleme sağlar. Veri tümleştirme özelliğiyle birlikte kullanılan Müşteri adayından nakde şablonları hesaplar, ürünler, satışlar, satış teklifleri, satış siparişleri ve satış faturaları için veri akışı sağlar. Veri akışı sağlanırken, Sales'de satış ve pazarlama faaliyetlerini gerçekleştirebilir ve Supply Chain Management'da stok yönetimini kullanarak sipariş karşılamaları işleyebilirsiniz. 

Aday'dan nakite tümleştirmesi hakkında daha fazla bilgi için kısa YouTube videosu'nu izleyin [Aday'dan nakite tümleştirme](https://www.youtube.com/watch?v=AVV9x5x-XCg).

Geçerli sürümde, Müşteri adayından nakde çözümü aşağıdaki türlerde doğrudan eşitleme sağlar:

- [Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme](accounts-template-mapping-direct.md)
- [Supply Chain Management'daki ürünleri doğrudan Sales'deki ürünlerle eşitleme](products-template-mapping-direct.md)
- [Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)
- [Satış teklifi başlıklarını ve satırlarını Sales'ten Supply Chain Management'a doğrudan eşitleme](sales-quotation-template-mapping-sales-fin.md)
- [Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme](sales-order-template-mapping-direct-two-ways.md)
- [Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management için sistem gereksinimleri
Müşteri adayından nakde tümleştirmesi aşağıdaki sürümlerde desteklenir:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (Aralık 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (Aralık 2017) - Uygulama yapısı 7.3.11971.56116 Platform Güncelleştirmesi 12 ile (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) - platform güncelleştirmesi 8 ile (uygulama yapısı 7.2.11792.56024, platform yapısı 7.0.4565.16212 ile).
- Aşağıdaki düzeltmeler gereklidir:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Bu düzeltme Veri Tümleştirme özelliğiyle Sales'den Supply Chain Management'a satış siparişi eşitlemesine olanak tanır. Başka geliştirmeler de içerir.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Sales'den Supply Chain Management'dan Sales'a satış siparişi satırı eşitlemesine olanak tanır.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Supply Chain Management'dan Sales'a satış siparişi eşitlemesine olanak tanır.

    > [!NOTE]
    > Yalnızca KB4045570 düzeltmesini yüklemeniz yeterlidir çünkü yükleme diğer düzeltmelerdeki değişiklikleri içerir. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations sürüm 1611 (Kasım 2016)

- Dynamics 365 for Finance and Operations sürüm 1611 (Kasım 2016)  platform güncelleştirmesi 8 veya daha yüksek ile

- Aşağıdaki düzeltmeler gereklidir:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Supply Chain Management'dan Sales'a Veri tümleştiriciyle satış siparişi eşitlemesine olanak tanır. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Supply Chain Management'dan Sales'a Veri tümleştiriciyle satış siparişi başlık ve satır eşitlemesine olanak tanır.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Veri varlıkları aracılığıyla müşteri adayından nakde tümleştirmesi için destek gereklidir.
    
    > [!NOTE]
    > Düzeltmeleri yükledikten sonra aşağıdaki toplu işi **SalesPopulateProspectToCash** formundan tetiklemeniz gerekir. Bu form yalnızca bir kez gereksinim duyacağınızdan gizlenmiştir. Forma erişmek için ortamda oturum açın ve şu ifadeyi tarayıcı adresinizdeki URL'ye ekleyin: *&mi=action:SalesPopulateProspectToCash*, örneğin `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Form açıldığında Tamam'a tıklayın. Bu, **SalesLine**, **SalesQuotationLine** ve **CustInvoiceTrans** tablolarında benzersiz değerlere sahip yeni bir **LineCreationSequnceNumber** alanı oluşturur ve ürün listesi yenilenir. Müşteri adayından nakde tümleştirmesinin çalışması için gereklidir.


## <a name="system-requirements-for-sales"></a>Sales için sistem gereksinimleri

Müşteri adayından nakde çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

- Dynamics 365 Sales sürüm 1612 (8.2.1.207) (DB 8.2.1.207) çevrimiçi veya sonraki bir sürüm.
- Dynamics 365 Sales, sürüm 1.15.0.0 veya üstü sürüm için Müşteri Adayından nakde çözümü. Çözüm AppSource'tan indirilebilir. [Download Dynamics 365, Aday Müşteriden Nakde](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]