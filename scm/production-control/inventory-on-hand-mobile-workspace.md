---
title: "Stok eldeki mobil çalışma alanı için Microsoft Dynamics 365 işlemleri uygulama için"
description: "Eldeki stok mobil çalışma herhangi bir zamanda ve herhangi bir mobil kavramanız ayrılmış ve kullanılabilen stok kazanmak yardımcı olur."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Stok eldeki mobil çalışma alanı için Microsoft Dynamics 365 işlemleri uygulama için

Eldeki stok mobil çalışma herhangi bir zamanda ve herhangi bir mobil kavramanız ayrılmış ve kullanılabilen stok kazanmak yardımcı olur. 

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                         | Açıklama                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobil platform için işlemleri hakkında Microsoft Dynamics 365 okuyun | [Dynamics 365 işlemleri mobil platformu](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 işlemleri için                                          | Bir Microsoft Dynamics 365 işlemleri için 1611 sürümde ortamı ve işlemleri platform Microsoft Dynamics 3 (Kasım 2016) güncelleştirmesi |
| Düzeltme KB 3215650                                                    | İşlemleri için Microsoft Dynamics 365 sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.                                       |
| Yüklü uygulama işlemleri için Dynamics 365 sahip mobil aygıt | Dynamics 365 işlemleri uygulama için mobil app deponuzdan indirin.                                                                           |

## <a name="introduction"></a>Giriş
Genellikle, şirketlerin birden fazla sevk irsaliyelerini ve birden çok giriş stok her gün vardır. Bu hareketleri sürekli olarak eldeki stok durumunu değiştirin. Böylece son stok verilerini seçeceğiniz mobil aygıttaki kavramanız kazanabilirler stok eldeki mobil çalışma şirketler arası eldeki stok durumunu görmenizi sağlar. Olup, ambar, satın alma, satış, üretim veya yönetim iş veya diğer rollere sahip ne olursa olsun, her zaman ve her yerde eldeki stok verilerini erişebilirsiniz. Mobil çalışma olanakları arasında eldeki durumu anlık bir görünümünü sağlar ve eldeki stok tesisleri, geçerli malzeme rezervasyonlarını ve eldeki stoku rezerve edilmemiş görmenizi sağlar. Sorgu için eldeki stoku madde numaralarını girin ve eldeki ürünler veya türevleri için filtre uygulanmış bir arama yapın. Özellikle, mobil çalışma alanı aşağıdaki özellikleri içerir:

-   Eldeki stok durumunu görüntülemek için ürün numarasını veya ürün adı ürünleri bulmak için arama yapabilirsiniz.
-   Seçili ürünler için aşağıdaki bilgileri görüntüleyebilirsiniz:
    -   Site başına eldeki stok
    -   Ambar başına eldeki stoku
    -   Konum başına eldeki stok
    -   Eldeki stok (ürünler toplu kontrol) için toplu iş başına
    -   Eldeki stoku stok durumu başına

<!-- -->

-   Eldeki stok ürün aşağıdaki şekilde gösterilmiştir:
    -   Göre Fiziki stok (Bu görünümü toplam tutarı gösterir.)
    -   (Bu görünümde rezerve edilmiş miktarını temsil eder.) fiziksel ayrılmış
    -   Kullanılabilir fiziksel (rezervasyon yok olan bu görünümü temsil kullanılabilir tutar.)

## <a name="get-started"></a>Başlayın
Mobil aygıtınızda kullanmaya başlamak için:

1.  Mobil app mağazadan, karşıdan yükleyip Microsoft Dynamics 365 işlemleri uygulama için.
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

## <a name="view-the-onhand-inventory-for-a-product"></a>Bir ürün için eldeki stoku görüntüleyin.
1.  Mobil aygıtınızda seçin **, eldeki stok** çalışma alanı.
2.  Seçin **kontrol eldeki bir madde için**. Uygulamanızı çevrimdışı kullanım için yüklenen ürünlerin listesini görürsünüz. Varsayılan olarak, 50 öğeler yüklenir, ancak bu numarayı değiştirebilirsiniz. Daha fazla bilgi için bkz: önceden okuma el kitabı.
3.  Seçin, öğe listede değilse, **daha fazla arama** işlemleri için Dynamics 365 içinde bir çevrimiçi arama yapmak için. Ürün numarasına göre arama veya ürün adına göre aramak için geçin.
4.  Bir ürün seçin. Öğenin bir resim varsa, resim gösterilir.
5.  Eldeki stok durumunu görüntülemek için aşağıdaki seçeneklerden birini seçin:
    -   Eldeki her sitede görüntüle
    -   Eldeki ambara göre görüntüle
    -   Eldeki konum başına Görünüm
    -   Eldeki miktarı (ürünler toplu kontrol) için toplu iş başına görüntüleme
    -   Eldeki stok durumu başına görüntüleme

    Eldeki stok ürün aşağıdaki şekilde gösterilmiştir:
    -   Göre Fiziki stok (Bu görünümü toplam tutarı gösterir.)
    -   (Bu görünümde rezerve edilmiş miktarını temsil eder.) fiziksel ayrılmış
    -   Kullanılabilir fiziksel (Bu görünümü hiçbir ayırmalar içeren kullanılabilir tutar gösterir.)




