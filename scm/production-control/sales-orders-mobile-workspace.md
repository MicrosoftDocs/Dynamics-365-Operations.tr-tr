---
title: "Uygulama işlemleri için Microsoft Dynamics 365 çalışma Mobil Satış siparişleri"
description: "Satış siparişleri mobil çalışma alanıyla, satış siparişlerinizde herhangi bir güncel kalabilir ve herhangi bir zamanda."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Uygulama işlemleri için Microsoft Dynamics 365 çalışma Mobil Satış siparişleri

Satış siparişleri mobil çalışma alanıyla, satış siparişlerinizde herhangi bir güncel kalabilir ve herhangi bir zamanda. 

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                         | Açıklama                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobil platform için işlemleri hakkında Microsoft Dynamics 365 okuyun | [Dynamics 365 işlemleri mobil platformu](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 işlemleri için                                          | 1611 işlemleri sürümü için Microsoft Dynamics 365 olmayan bir ortamda kullanıyorsanız ve Microsoft Dynamics işlemleri platform için 3 (Kasım 2016) güncelleştirme emin olun. |
| Düzeltme KB 3215650                                                    | Microsoft Dynamics 365 işlemleri için sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.                                                                       |
| Yüklü uygulama işlemleri için Dynamics 365 sahip mobil aygıt | Dynamics 365 işlemleri uygulama için mobil app deponuzdan indirin.                                                                                                      |

## <a name="overview"></a>Özet
Bu mobil çalışma işlemleri uygulama için Dynamics 365 erişir ve sipariş durumu, müşteri ilgili kişi bilgileri ve siparişi alanın ilgili kişi bilgileri gibi her satış siparişi hakkındaki ayrıntılı bilgileri görüntülemenize olanak sağlar. Mobil çalışma alanı, satış siparişleri anında bir görünümünü sağlar. Müşteriye göre satış siparişleri görüntüleyin veya tüm satış siparişlerini görüntülemek veya belirli bir satış siparişi hakkındaki bilgileri görüntüleyin. Mobil çalışma derinliği satış siparişlerindeki çözümlemenize yardımcı olacak iki görünüm sağlar.

### <a name="view-all-sales-orders"></a>Tüm satış siparişlerini görüntüleyin.

Bu görünüm tüm satış siparişlerini listeler.

-   Görüntülemek istediğiniz satış siparişleri seçmek için aşağıdaki filtrelerden birini kullanın.
    -   Satış siparişine göre arama
    -   Müşteri hesabına göre arama
    -   Müşteri adına göre arama
    -   Duruma göre arama
    -   Yayın durumuna göre arama
    -   Oluşturulma tarihi ve saati arama ölçütü

<!-- -->

-   Satış siparişleri seçtikten sonra belirli siparişleri ayrıntılarını görüntüleyebilirsiniz. Özellikle, şunları görüntüleyebilirsiniz:
    -   Müşteri adı ve adres bilgileri
    -   Talep edilen sevk tarihi ve teyit edilen sevk tarihi gibi farklı satış sipariş tarihleri
    -   Sipariş alanın ilgili kişi bilgileri
    -   Müşteri ilgili kişi bilgileri
    -   Sipariş satırları
    -   Nasıl ve ne zaman bir satış siparişi sevk edildiği Göster sevk irsaliyeleri

### <a name="view-orders-for-a-customer-"></a>Müşteri ** siparişlerini görüntülemek **

Bu görünüm, müşteri başına satış siparişlerini listeler.

-   Bir müşterinin siparişlerini görüntülemek için aşağıdaki filtrelerden birini kullanın.
    -   Adına göre arama
    -   Hesaba göre arama

<!-- -->

-   Bir müşteri seçin sonra şunları görüntüleyebilirsiniz:
    -   Müşteri adı ve Grup
    -   Müşteri ilgili kişi bilgileri
    -   Müşteri satış siparişleri ve satış siparişleri hakkındaki ayrıntıları:
        -   Müşteri adı ve adres bilgileri
        -   Farklı satış sipariş tarihleri
        -   Sipariş alanın ilgili kişi bilgileri
        -   Müşteri ilgili kişi bilgileri
        -   Sipariş satırları
        -   Nasıl ve ne zaman bir satış sevk edilen siparişler Göster sevk irsaliyeleri

## <a name="get-started"></a>Başlayın
Satış siparişleri mobil çalışma mobil aygıtınızda kullanmaya başlamak için aşağıdaki adımları izleyin.

1.  Mobil app store üzerinde karşıdan yükleyip Microsoft Dynamics 365 işlemleri uygulama için.
2.  Aygıtınızda uygulamayı başlatın.
3.  Dynamics 365 URL'nizi girin.
4.  Oturum açmak için şirket girin. Örneğin: **USMF**.
5.  İlk kez, oturum, Microsoft Dynamics 365 işlem hesabı için kullanıcı adı ve parola için uyarılırsınız. Kimlik bilgilerinizi girin. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz.

Çalışma alanları, mobil app üzerinde görüntülemek için önce istediğiniz çalışma işlemleri uygulama için Dynamics 365 yayımlamanız gerekir.

1.  Dynamics 365 işlemleri için başlatın.
2.  Git **Sistem Yönetimi**&gt;**Kurulum**&gt;**sistem parametreleri**.
3.  Seçin **Yönet mobil uygulama**.
4.  Mobil platform için yayımlamak için çalışma alanını seçin.
5.  Seçin **çalışma yayımlamak**.
6.  Yayımlanmış çalışma öğrenmek için aygıtınızın yenileyin.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Bir müşteri için satış siparişleri hakkındaki bilgileri görüntüleyin
1.  Mobil aygıtınızda seçin **satış siparişleri** çalışma alanı.
2.  Seçin **görüntülemek için bir müşteri siparişleri**.
3.  Kullanım ** hesabı ** veya ** müşteri adı ** bilgi istediğiniz müşteriyi bulun.
4.  Müşteriyi seçin.
5.  Seçin **iletişim bilgileri** veya **satış siparişleri**.
6.  Yoksa **satış siparişleri** ise seçilen, bir müşteri için satış siparişlerinin listesi görüntülenir.
7.  Seçin **satış sipariş**.
8.  Buraya, satış siparişi satırlarının, sevk irsaliyeleri, müşteri ilgili kişi bilgileri ve siparişi alanın ilgili kişi bilgileri hakkında bilgi görüntüleyebilirsiniz.




