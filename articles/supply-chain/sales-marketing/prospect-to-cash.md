---
title: "Müşteri adayından nakde"
description: "Bu konuda, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ile Microsoft Dynamics 365 for Sales arasındaki Müşteri adayından nakde çözümüne genel bakış sunulmaktadır."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: tr-tr
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Müşteri adayından nakde

[!include[banner](../includes/banner.md)]

Müşteri adayından nakde çözümü, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ile Microsoft Dynamics 365 for Sales arasında doğrudan eşitleme yapılmasını sağlar. Veri Tümleştirme özelliğiyle birlikte kullanılan Müşteri adayından nakde şablonları Finance and Operations ile Sales arasında hesaplar, ürünler, satışlar, satış teklifleri, satış siparişleri ve satış faturaları için veri akışı sağlar. Finance and Operations ile Sales arasında veri akışı sağlanırken, Sales'de satış ve pazarlama faaliyetlerini gerçekleştirebilir ve Finance and Operations'da stok yönetimini kullanarak sipariş karşılamaları işleyebilirsiniz.

Geçerli sürümde, Müşteri adayından nakde çözümü aşağıdaki türlerde doğrudan eşitleme sağlar:

- [Hesapları Sales içinde koruma ve onları doğrudan Sales'den Finance and Operations'a eşitleme](accounts-template-mapping-direct.md)
- [Ürünleri Finance and Operations içinde yönetme ve onları doğrudan Sales ile eşitleme](products-template-mapping-direct.md)
- [Sales'teki ilgili kişileri koruma ve onları doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)
- [Satış teklifini doğrudan Sales'den Finance and Operations'a eşitleme](sales-quotation-template-mapping-sales-fin.md)
- [Satış siparişlerini doğrudan Finance and Operations'tan Sales'e eşitleme](sales-order-template-mapping-direct.md)
- [Sales ile Finance and Operations arasında satış siparişlerini doğrudan eşitleme](sales-order-template-mapping-direct-two-ways.md)
- [Satış faturasını doğrudan Finance and Operations'tan Sales'e eşitleme](sales-invoice-template-mapping-direct.md)

Önceki sürümlerde, Müşteri adayından nakde çözümü doğrudan yapılamayan aşağıdaki eşitleme türlerini sağlıyordu:

- [Hesapları Sales içinde yönetin ve onları Finance and Operations ile eşitleyin](accounts-template-mapping.md)
- [İlgili kişileri Sales içinde yönetin ve onları Finance and Operations ile eşitleyin](contacts-template-mapping.md)
- [Ürünleri Finance and Operations içinde yönetin ve onları Sales ile eşitleyin](products-template-mapping.md)
- [Satış tekliflerini Sales içinde oluşturun ve onları Finance and Operations ile eşitleyin](sales-quotation-template-mapping.md)
- [Finance and Operations içinde satış siparişleri oluşturun ve onları Sales ile eşitleyin](sales-order-template-mapping.md)
- [Finance and Operations içinde satış faturaları oluşturun ve onları Sales ile eşitleyin](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations için sistem gereksinimleri

Müşteri adayından nakde çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

### <a name="july-2017"></a>Temmuz 2017 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017), platform güncelleştirmesi 8 ile birlikte (uygulama derlemesi 7.2.11792.56024, platform derlemesi 7.0.4565.16212 ile birlikte)
- Finance and Operations için aşağıdaki düzeltmeler:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Bu düzeltme Veri Tümleştirme özelliğiyle Sales'den Finance and Operations'a satış siparişi eşitlemesine olanak tanır. Başka geliştirmeler de içerir.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Finance and Operations'tan Sales'e satış siparişi satırı eşitlemesine olanak tanır.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Finance and Operations'tan Sales'a satış siparişi eşitlemesine olanak tanır.

    > [!NOTE]
    > Yalnızca KB4045570'i yüklemeniz yeterlidir çünkü yükleme diğer Microsoft Bilgi Bankası (KB) makalelerindeki değişiklikleri içerir.

### <a name="november-2016-version-1611"></a>Kasım 2016 (Sürüm 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Kasım 2016), platform güncelleştirmesi 8 veya üstü ile birlikte

- Finance and Operations için aşağıdaki düzeltmeler:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Microsoft Dynamics 365 for Finance and Operations'dan Sales'a Veri tümleştiriciyle satış siparişi eşitlemesine olanak tanır 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Microsoft Dynamics 365 for Finance and Operations'dan Sales'a Veri tümleştiriciyle satış siparişi başlığı ve satırı eşitlemesine olanak tanır
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Veri varlıkları aracılığıyla müşteri adayından nakde tümleştirmesi için destek gereklidir
    
    > [!NOTE]
    > Düzeltmeleri yükledikten sonra aşağıdaki toplu işi SalesPopulateProspectToCash formundan tetiklemeniz gerekir. Bu form yalnızca bir kez gereksinim duyacağınızdan gizlenmiştir. Bu forma erişmek için ortamda oturum açarken şu ifadeyi tarayıcı adresinize ekleyin: &mi=action:SalesPopulateProspectToCash E.g. https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash Açılan formda Tamam'ı tıklayın.
    Bu, “SalesLine”, “SalesQuotationLine” ve “CustInvoiceTrans” tablolarında benzersiz değerlere sahip yeni bir “LineCreationSequnceNumber” alanı oluşturur ve ürün listesini yeniler. Bu, 7.1'de çalışmak üzere P2C tümleştirmesi için gereklidir


## <a name="system-requirements-for-sales"></a>Sales için sistem gereksinimleri

Müşteri adayından nakde çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

- Microsoft Dynamics 365 for Sales sürüm 1612 (8.2.1.207) (DB 8.2.1.207) çevrimiçi
- Microsoft Dynamics 365 for Sales, sürüm 1.15.0.0 (v15) için müşteri adayından nakde çözümü 

   > [!NOTE]
   >
   > 1.0.0.0 ve 1.0.0.1 sürümlü şablonlar Microsoft Dynamics 365 for Sales, sürüm 1.14.1.0'a yönelik Müşteri adayından nakde çözümümde desteklenir
   >
   > 2.0.0.0 ve 2.1.0.0 sürümlü şablonlar Microsoft Dynamics 365 for Sales, sürüm 1.15.0.0'a yönelik Müşteri adayından nakde çözümünde desteklenir

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümünü yükleyin

1. CustomerSource'dan [Dynamics 365 for Sales için Müşteri adayından nakde çözüm paketi zip dosyasını](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) indirin.
2. Zip dosyasının engellenmemiş olduğundan emin olun Aksi takdirde, çözüm paketini yüklemeye çalışırken şu hata iletisini alırsınız: "İçe aktarma paketi bulunamadı." Zip dosyasındaki engellemeyi kaldırmak için dosyaya sağ tıklayın ve **Özellikler**'i seçin. Sonra **Engellemeyi Kaldır**'ı seçin.
3. Zip dosyasını açın ve **PackageDeployer.exe**'yi çalıştırın.
4. Müşteri adayından nakde çözümünü Sales kurulumunuza yükleyin:

    1. Dağıtım türü olarak **Office 365** seçin.
    2. **Gelişmişi göster**'i seçin.
    3. Hızlı yükleme için bir bölge seçin. **Bilmiyorum**'u seçerseniz, sistem tüm bölgeleri arayacaktır ve yükleme daha uzun sürecektir.
    4. Yükleme haklarına sahip bir yönetici kullanıcı için kullanıcı adı ve parola girin.

