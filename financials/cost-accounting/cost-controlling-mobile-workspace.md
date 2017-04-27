---
title: "Microsoft Dynamics 365 for Operations uygulaması için maliyet yönetimi mobil çalışma alanı"
description: "Maliyet kontrolü mobil çalışma alanı ile, maliyet merkezi yöneticileri, maliyet merkezi performansını her zaman ve her yerde görebilirler."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations uygulaması için maliyet yönetimi mobil çalışma alanı

Maliyet kontrolü mobil çalışma alanı ile, maliyet merkezi yöneticileri, maliyet merkezi performansını her zaman ve her yerde görebilirler. 

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                         | Açıklama                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Dynamics 365 for Operations mobil platformu hakkında bilgi alın | [Dynamics 365 for Operations mobil platformu](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Microsoft Dynamics 365 for Operations sürüm 1611 ve Microsoft Dynamics for Operations platform güncelleştirmesi 3 (Kasım 2016) güncelleştirmelerine sahip bir ortam kullandığınıza emin olun. |
| Düzeltme KB 3215650                                                    | Microsoft Dynamics 365 for Operations içerisinde sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.                                                                       |
| Yüklü uygulama işlemleri için Dynamics 365 sahip mobil aygıt | Dynamics 365 işlemleri uygulama için mobil app deponuzdan indirin.                                                                                                      |

## <a name="introduction"></a>Giriş
Maliyet denetleme mobil çalışma alanı, maliyet merkezlerinin mevcut performansı hakkında anında bilgiyi, ffili maliyetleri, bütçelendirilmiş maliyete kıyaslayarak sağlar. Tekil maliyet öğelerinin durumlarının detayına inebilirsiniz.

### <a name="example"></a>Örnek

Bir personel, uluslararası bir konferansa davet alır. Kuruluş, seyahat masrafların tümünü karşılamak zorunda kalır. Personel, yöneticisi kendi konferansa katılıp katılamayacağını sorar. Yönetici, personelin konferansa katılması için bütçeye sahip olup olmadığını görmek için cep telefonunda Maliyet denetimi mobil çalışma alanını hızla açar.

### <a name="data-security"></a>Veri güvenliği

Maliyet denetimi çalışma alanındaki veriler, kullanıcı kimlik bilgileriyle güvenlik altına alınır. Bir maliyet merkezi yöneticisinin yalnızca kendi maliyet merkezi verilerini görmesine izin verilir. Erişim düzeyi güvenliği maliyet muhasebesi modülünde yönetilir. Maliyet muhasebecileri, maliyet muhasebesi modülünde maliyet denetimi mobil çalışma alanı yapılandırmasını tanımlar. Çalışma alanı Microsoft Dynamics 365 for Operations'a yayımlandıktan sonra, Dynamics 365 for Operations mobil uygulamasında kullanılabilir. Bu, kuruluşunuzdaki tüm maliyet merkezi yöneticilerinin aynı biçimdeki veriye bakabilmelerini sağlar.

### <a name="actions-views-and-links"></a>Eylemler, görünümler ve bağlantılar

Dynamics 365 for Operations uygulaması için maliyet denetleme mobil çalışma alanı, aşağıdaki eylem, görünüm ve bağlantıları sağlar:

-   Eylemler 
    -   Bir düzen seçmek için **Yapılandırma**yı seçin.
    -   Veriyi filtrelemek istediğini maliyet merkezlerini seçmek için **Maliyet nesneleri**ni seçin. **Not:** Bu liste, Maliyet muhasebesi modülünde sağlanmış olan erişime göre görüntülenir.

<!-- -->

-   **Eylemler** altında neyin seçildiğine ve Maliyet muhasebesi modülünde ne yapılandırıldığına bağlı olarak , aşağıdaki bilgiyi Kartlarda görüntüleyebilirsiniz. Tutarın aynı biçimde görüntülendiğini dikkate alın: Fiili, Bütçelendirilmiş, Fark ve Fark %'si. 
    -   Fiili - Bütçe (geçerli dönem) karşılaştırması
    -   Fiili - Revize edilmiş bütçe (geçerli dönem) karşılaştırması
    -   Fiili - Bütçe (önceki dönem) karşılaştırması
    -   Fiili - Revize edilmiş bütçe (önceki dönem) karşılaştırması
    -   fiili - Bütçe (günümüze kadar yıl) karşılaştırması
    -   Fiili - Revize edilmiş bütçe (günümüze kadar yıl) karşılaştırması

<!-- -->

-   Bağlantılar
    -   Geçerli dönem için ayrıntılar.
    -   Önceki dönem için ayrıntılar.
    -   Yıl başından bu güne için ayrıntılar.

Bağlantılardan birini seçtiğinizde, maliyeti öğesi başına bir Kart görüntülenir. Kartlardaki tutar, aşağıdaki biçimde gösterilir: Fiili, Bütçe, Bütçe farkı, Bütçe farkı %'si, Revize edilmiş bütçe, Revize edilmiş farkı ve Revize edilmiş farkı %'si.  [![maliyet-kontrolu](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Başlayın
Mobil cihazınızda maliyet denetimi mobil uygulamasını kullanmaya başlamak için aşağıdaki adımları izleyin.

1.  Mobil uygulama mağazanızda, Microsoft Dynamics 365 for Operations uygulamasını indirin ve kurun.
2.  Cihazınızda uygulamayı başlatın.
3.  Dynamics 365 URL'nizi girin.
4.  Oturum açılacak şirketi girin. Örneğin **USMF** yazın.
5.  İlk defa oturum açtığınızda, Microsoft Dynamics 365 for Operations hesabınızın kullanıcı adı ve parolasını girmeniz için uyarılırsınız. Kimlik bilgilerinizi girin. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz.

Çalışma alanları, mobil app üzerinde görüntülemek için önce istediğiniz çalışma işlemlerini Dynamics 365 for Operations uygulaması için yayımlamanız gerekir.

1.  Dynamics 365 for Operations'ı başlatın.
2.  **Sistem yönetimi** &gt; **Kurulum** &gt; **sistem parametreleri**ne gidin.
3.  **Mobil uygulamayı yönet** seçeneğini işaretleyin.
4.  Mobil platforma yayımlamak için **Maliyet denetleme** çalışma alanını seçin.
5.  **Çalışma alanını yayımla** seçeneğini işaretleyin.
6.  Yayımlanmış çalışma alanlarını görmek için cihazınızı yenileyin.

## <a name="view-the-performance-of-your-cost-center"></a>Maliyet merkezinizin performansını görün
1.  Mobil cihazınızda **Maliyet denetleme** çalışma alanını seçin.
2.  **Maliyet nesnesi denetleme** seçeneğini işaretleyin.
3.  **Eylemler** seçeneğini tıklatın.
4.  **Yapılandırma seç**'i tıklatarak bir maliyet denetleme biçimi seçin.
5.  **Bitti**'yi tıklatın.
6.  **Eylemler** seçeneğini tıklatın.
7.  **Maliyet nesnesi seç**'i tıklatarak erişimizin olduğu maliyet merkezlerini seçin.
8.  **Bitti**'yi tıklatın.
9.  Maliyet merkezinizin toplam performansını görün.
10. **Geçerli dönem için ayrıntılar** üzerine tıklayın.
11. Bireysel maliyet öğelerinin performansını görün.
12. Belirli maliyet öğeleri için de arama yapabilirsiniz.



