---
title: "Müşteri adayından nakde"
description: "Bu konu Dynamics 365 for Finance and Operations, Enterprise edition ve Dynamics 365 for Sales arasındaki Müşteri adayından nakde çözümüne bir genel bakış sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: tr-tr
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a>Müşteri adayından nakde  

[!include[banner](../includes/banner.md)]

Müşteri adayından nakde çözümü [Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration)'nü Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ve Dynamics 365 for Sales örnekleri için ORtak Veri Hizmeti (CDS) aracılığıyla kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir. Veri Finance and Operations ve Sales arasında akarken, satış ve pazarlama etkinliklerini Sales içerisinde gerçekleştirebilir ve sipariş tamamlamayı, stok yönetimi ile Finance and Operations içerisinde kullanabilirsiniz. 

Bu çözüm aşağıdaki alanlarda tümleştirme sağlar: 

-   [Hesapları Sales içinde yönetin ve onları Finance and Operations ile eşitleyin](accounts-template-mapping.md)
-   [İlgili kişileri Sales içinde yönetin ve onları Finance and Operations ile eşitleyin](contacts-template-mapping.md)
-   [Ürünleri Finance and Operations içinde yönetin ve onları Sales ile eşitleyin](products-template-mapping.md)
-   [Satış tekliflerini Sales içinde oluşturun ve onları Finance and Operations ile eşitleyin](sales-quotation-template-mapping.md)
-   [Finance and Operations içinde satış siparişleri oluşturun ve onları Sales ile eşitleyin](sales-order-template-mapping.md)
-   [Finance and Operations içinde satış faturaları oluşturun ve onları Sales ile eşitleyin](sales-invoice-template-mapping.md)

Bu çözüm aşağıdaki alanlarda doğrudan eşitleme sağlar:

-   [Hesapları Sales içinde koruma ve onları doğrudan Sales'den Finance and Operations'a eşitleme](accounts-template-mapping-direct.md)
-   [Ürünleri Finance and Operations içinde yönetme ve onları doğrudan Sales ile eşitleme](products-template-mapping-direct.md)
-   [Sales'teki ilgili kişileri koruma ve onları doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)
-   [Sales'deki satış teklifi başlıklarını ve satırlarını doğrudan Finance and Operations'la eşitleme](sales-quotation-template-mapping-sales-fin.md)
-   [Finance and Operations içinde satış siparişleri oluşturma ve onları doğrudan Sales ile eşitleme](sales-order-template-mapping-direct.md)
-  [Sales ile Finance and Operations arasında satış siparişi başlıklarını ve satırlarını doğrudan eşitleme](sales-order-template-mapping-between-sales-fin.md)
-   [Sales ile Finance and Operations arasında satış siparişlerini doğrudan eşitleme](sales-order-template-mapping-direct-two-ways.md)
-   [Finance and Operations içinde satış faturaları oluşturma ve onları doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Dynamics 365 for Finance and Operations, Enterprise sürümü için sistem gereksinimleri

Adam müşteriden nakde çözümünü kullanmak için şunu yüklemeniz gerekir:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017), Platform güncelleştirmesi 8 ile (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)

- Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) için düzeltmeler.
        
    -  [KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - Bu düzeltme Sales ile Finance and Operations arasında Veri Tümleştirme özelliğiyle satış siparişi eşitleme desteği ve çeşitli başka geliştirmeler sağlar.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Bu düzeltme satış siparişi satırları eşitlemesini Finance and Operations'tan Sales'a Veri Tümleştirme özelliğini etkinleştirir.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Bu düzeltme satış siparişi satırları eşitlemesini Finance and Operations'tan Sales'a Veri Tümleştirme özelliğini etkinleştirir.

**Not**: Yalnızca KB4045570 yüklemeniz yeterlidir çünkü yükleme diğer KB'lerdeki değişiklikleri içerir.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Dynamics 365 for Sales için sistem gereksinimleri

Adam müşteriden nakde çözümünü kullanmak için şunu yüklemeniz gerekir:

- Dynamics 365 for Sales sürüm 1612 (8.2.1.207) (DB 8.2.1.207) çevrimiçi.
- Dynamics 365 for Sales için Aday müşteriden nakde çözümü, sürüm 1.14.0.0 (v14) veya sonrası.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümünü yükleyin

- [Dynamics 365 for Sales için Aday müşteriden nakde çözüm paketi zip dosyasını](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSource üzerinden yükleyin.

- Çözüm paketini yüklerken "İçe aktarma paketleri bulunamadı" hata mesajını almamak için zip dosyasının engellenmemiş olduğunda emin olun. Dosyanın engelini kaldırmak için aşağıdakini yapın:

    -  Zip dosyasına sağ tıklatın.
    -  **Özellikler**'i seçin ve sonra **Engeli kaldır**'ı seçin. 

- PackageDeployer.exe'yi çıkartın ve çalıştırın.

- Aday müşteriden Nakde çözümünü Sales kurulumunuzda yükleyin.

    - **Office 365** dağıtım türünü seçin.
    - **Gelişmişi göster**'i seçin.
    - Hızlı yükleme için bir **Bölge** seçin. **Emin değil**'i seçerseniz, sistem tüm bölgeleri arayacaktır ve yüklemesi daha uzun sürecektir.
    - Yükleme için kullanıcı haklarına sahip bir yönetici kullanıcı için **Kullanıcı adı** ve **Parola** girin.

