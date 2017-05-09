---
title: "Microsoft Dynamics 365 for Operations uygulaması için satış siparişleri mobil çalışma alanı"
description: "Satış siparişleri mobil çalışma alanıyla, satış siparişlerinizin en güncel bilgilerini herhangi bir yer ve zamanda öğrenebilirsiniz."
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

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations uygulaması için satış siparişleri mobil çalışma alanı

Satış siparişleri mobil çalışma alanıyla, satış siparişlerinizin en güncel bilgilerini herhangi bir yer ve zamanda öğrenebilirsiniz. 

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                         | Açıklama                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Dynamics 365 for Operations mobil platformu hakkında bilgi alın | [Dynamics 365 for Operations mobil platformu](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Microsoft Dynamics 365 for Operations sürüm 1611 ve Microsoft Dynamics for Operations platform güncelleştirmesi 3 (Kasım 2016) güncelleştirmelerinin yüklendiği bir ortam kullandığınıza emin olun. |
| Düzeltme KB 3215650                                                    | Microsoft Dynamics 365 for Operations içerisinde sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.                                                                       |
| Yüklü uygulama işlemleri için Dynamics 365 sahip mobil aygıt | Dynamics 365 işlemleri uygulama için mobil app deponuzdan indirin.                                                                                                      |

## <a name="overview"></a>Özet
Bu mobil çalışma alanı Dynamics 365 for Operations uygulamasına erişir ve her bir satış siparişiyle ilgili ayrıntılı bilgileri (sipariş durumu, müşteri iletişim bilgileri ve siparişi alanın iletişim bilgileri gibi) görüntülemenizi sağlar. Mobil çalışma alanı, satış siparişlerinin anlık görünümünü sağlar. Müşteri bazında satış siparişlerini veya tüm satış siparişlerini ya da belirli bir satış siparişiyle ilgili bilgileri görüntüleyebilirsiniz. Mobil çalışma alanı, satış siparişlerini derinlemesine çözümlemenize yardımcı olacak iki görünüm sağlar.

### <a name="view-all-sales-orders"></a>Tüm satış siparişlerini görüntüle

Bu görünüm tüm satış siparişlerini listeler.

-   Görüntülemek istediğiniz satış siparişlerini seçmek için aşağıdaki filtrelerden birini kullanın.
    -   Satış siparişine göre ara
    -   Müşteri hesabına göre ara
    -   Müşteri adına göre ara
    -   Duruma göre ara
    -   Serbest bırakma durumuna göre ara
    -   Oluşturma tarih ve saatine göre ara

<!-- -->

-   Satış siparişlerini seçtikten sonra belirli siparişlerin ayrıntılarını görüntüleyebilirsiniz. Özel olarak şunları görüntüleyebilirsiniz:
    -   Müşteri adı ve adres bilgileri
    -   Talep edilen sevk tarihi ve Teyit edilen sevk tarihi gibi farklı satış siparişi tarihleri
    -   Siparişi alanın iletişim bilgileri
    -   Müşteri iletişim bilgileri
    -   Sipariş satırları
    -   Bir satış siparişinin nasıl ve ne zaman sevk edildiğini gösteren sevkiyatlar

### <a name="view-orders-for-a-customer-"></a>Bir müşterinin siparişlerini görüntüle

Bu görünüm, müşterinin satış siparişlerini listeler.

-   Bir müşterinin siparişlerini görüntülemek için aşağıdaki filtrelerden birini kullanın.
    -   Ada göre ara
    -   Hesaba göre ara

<!-- -->

-   Müşteri seçtikten sonra şunları görüntüleyebilirsiniz:
    -   Müşteri adı ve grubu
    -   Müşteri iletişim bilgileri
    -   Müşteri satış siparişleri ve satış siparişleri hakkındaki ayrıntılar:
        -   Müşteri adı ve adres bilgileri
        -   Farklı satış siparişi tarihleri
        -   Siparişi alanın iletişim bilgileri
        -   Müşteri iletişim bilgileri
        -   Sipariş satırları
        -   Bir satış siparişinin nasıl ve ne zaman sevk edildiğini gösteren sevkiyatlar

## <a name="get-started"></a>Başlayın
Mobil cihazınızda satış siparişleri mobil çalışma alanını kullanmaya başlamak için aşağıdaki adımları izleyin.

1.  Mobil uygulama mağazanızda, Microsoft Dynamics 365 for Operations uygulamasını indirin ve yükleyin.
2.  Cihazınızda uygulamayı başlatın.
3.  Dynamics 365 URL'nizi girin.
4.  Oturum açılacak şirketi girin. Örneğin **USMF** yazın.
5.  İlk defa oturum açtığınızda, Microsoft Dynamics 365 for Operations hesabınızın kullanıcı adı ve parolasını girmeniz için uyarılırsınız. Kimlik bilgilerinizi girin. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz.

Çalışma alanları, mobil app üzerinde görüntülemek için önce istediğiniz çalışma işlemlerini Dynamics 365 for Operations uygulaması için yayımlamanız gerekir.

1.  Dynamics 365 for Operations'ı başlatın.
2.  **Sistem yönetimi** &gt; **Kurulum** &gt; **sistem parametreleri**ne gidin.
3.  **Mobil uygulamayı yönet** seçeneğini işaretleyin.
4.  Mobil platforma yayımlamak için çalışma alanını seçin.
5.  **Çalışma alanını yayımla** seçeneğini işaretleyin.
6.  Yayımlanmış çalışma alanlarını görmek için cihazınızı yenileyin.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Bir müşteriyle ilgili satış siparişleri hakkında bilgileri görüntüle
1.  Mobil cihazınızda **Satış siparişleri** çalışma alanını seçin.
2.  **Bir müşterinin siparişlerini görüntüle**'yi seçin.
3.  İstediğiniz müşteriyi bulmak için **Hesap** veya **Müşteri Adı** bilgilerini kullanın.
4.  Müşteriyi seçin.
5.  **İletişim bilgileri**'ni veya **Satış siparişleri**'ni seçin.
6.  **Satış siparişleri** seçilirse, müşterinin satış siparişlerinin listesi görüntülenir.
7.  **Satış siparişi**'ni seçin.
8.  Buraya, satış siparişi satırlarının, sevk irsaliyeleri, müşteri ilgili kişi bilgileri ve siparişi alanın ilgili kişi bilgileri hakkında bilgi görüntüleyebilirsiniz.




