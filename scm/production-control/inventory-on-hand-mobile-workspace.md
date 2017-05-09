---
title: "Microsoft Dynamics 365 for Operations uygulaması için eldeki stok mobil çalışma alanı"
description: "Eldeki stok mobil çalışma alanı, ayrılmış ve kullanılabilir stok hakkında mobil bilgileri her yerde ve her zaman edinebilmenizi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations uygulaması için eldeki stok mobil çalışma alanı

Eldeki stok mobil çalışma alanı, ayrılmış ve kullanılabilir stok hakkında mobil bilgileri her yerde ve her zaman edinebilmenizi sağlar. 

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                         | Açıklama                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Dynamics 365 for Operations mobil platformu hakkında bilgi alın | [Dynamics 365 for Operations mobil platformu](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Microsoft Dynamics 365 for Operations sürüm 1611 ve Microsoft Dynamics for Operations platform güncelleştirmesi 3 (Kasım 2016) güncelleştirmelerine sahip bir ortam |
| Düzeltme KB 3215650                                                    | Microsoft Dynamics 365 for Operations'unuz içerisinde sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.                                       |
| Yüklü uygulama işlemleri için Dynamics 365 sahip mobil aygıt | Dynamics 365 işlemleri uygulama için mobil app deponuzdan indirin.                                                                           |

## <a name="introduction"></a>Giriş
Genellikle, şirketler her gün birden fazla sevkiyata ve birden fazla stok girişine sahiptirler. Bu hareketler eldeki stok durumunu sürekli olarak değiştirir. Eldeki stok mobil çalışma alanı, şirketler arası eldeki stok durumunu görmenizi sağlar, böylece stok verisi hakkında en son bilgileri istediğiniz mobil cihazdan edinebilirsiniz. İster ambarda, satın almada, satışta, üretimde veya yönetimde çalışıyor isterseniz de başka bir role sahip olun, eldeki stok verisine her zaman ve her yerde erişebilirsiniz. Mobil çalışma alanı, tesisler arasındaki eldeki stok hakkında anında görünüm sağlar ve eldeki stoku, mevcut malzeme ayırmalarını ve rezerve edilmemiş eldeki stoku tesisler arasında görmenizi sağlar. Eldeki stoku sorgulamak için madde numaralarını da girebilir, eldeki ürünler ve çeşitleri için filtreli arama da gerçekleştirebilirsiniz. Özellikle, mobil çalışma alanı bu özellikleri sağlar:

-   Ürün numarasına veya ürün adına göre arama yapabilir ve eldeki stok durumlarını görmek için ürünleri bulabilirsiniz.
-   Seçili ürünler için aşağıdaki bilgileri görüntüleyebilirsiniz:
    -   Siteye göre eldeki stok
    -   Ambara başına eldeki stok
    -   Konum başına eldeki stok
    -   Toplu iş başına eldeki stok (toplu iş denetimli ürünler için=
    -   Stok durumuna göre eldeki stok

<!-- -->

-   Ürün eldeki stok aşağıdaki şekillerde gösterilir:
    -   Fiziksel stoka göre (Bu görünüm, toplam tutarı temsil eder.)
    -   Fiziksel ayrılana göre (Bu görünüm ayrılan tutarı temsil eder.)
    -   Kullanılabilir fiziksele göre (Bu görünüm, rezervasyonu olmayan tutarı temsil eder.)

## <a name="get-started"></a>Başlayın
Mobil cihazınızda kullanmaya başlamak için:

1.  Mobil uygulama mağazanızdan, Microsoft Dynamics 365 for Operations uygulamasını indirin ve kurun.
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

## <a name="view-the-onhand-inventory-for-a-product"></a>Bir ürün için eldeki stoku görüntüleyin
1.  Mobil cihazınızda **Eldeki stok** çalışma alanını seçin.
2.  **Bir maddenin eldeki durumunu kontrol et** seçeneğini işaretleyin. Çevrimdışı kullanım için uygulamanıza yüklenmiş ürünlerin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bu sayıyı değiştirebilirsiniz. Daha fazla bilgi için ön okuma el kitabına bakın.
3.  Maddeniz listede değilse, Dynamics 365 for Operations içerisinde bir çevrimiçi arama yapmak için **Daha fazla ara**'yı seçin. Ürün numarası ile arayın veya ürün adına göre aramaya geçin.
4.  Bir ürün seçin. Maddenin bir resmi varsa, resim gösterilir.
5.  Eldeki stok bilgisini görmek için aşağıdaki seçeneklerden birini seçin:
    -   Siteye göre eldekini görüntüle
    -   Ambara göre eldekini görüntüle
    -   Konuma göre eldekini görüntüle
    -   Toplu iş başına eldekini görüntüle (toplu iş denetimli ürünler için=
    -   Stok durumuna göre eldekini görüntüle

    Ürün eldeki stok aşağıdaki şekillerde gösterilir:
    -   Fiziksel stoka göre (Bu görünüm, toplam tutarı temsil eder.)
    -   Fiziksel ayrılana göre (Bu görünüm ayrılan tutarı temsil eder.)
    -   Kullanılabilir fiziksele göre (Bu görünüm, rezervasyonu olmayan kullanılabilir tutarı temsil eder.)




