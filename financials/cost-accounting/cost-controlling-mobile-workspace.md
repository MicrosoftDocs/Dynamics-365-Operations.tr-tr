---
title: "Kontrol eden mobil çalışma için Microsoft Dynamics 365 işlemleri app için maliyet."
description: "Maliyeti ile mobil çalışma alanında, maliyet merkezi yöneticileri denetleme maliyet merkezi performans her zaman ve her yerde görebilirsiniz."
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

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kontrol eden mobil çalışma için Microsoft Dynamics 365 işlemleri app için maliyet.

Maliyeti ile mobil çalışma alanında, maliyet merkezi yöneticileri denetleme maliyet merkezi performans her zaman ve her yerde görebilirsiniz. 

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                         | Açıklama                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobil platform için işlemleri hakkında Microsoft Dynamics 365 okuyun | [Dynamics 365 işlemleri mobil platformu](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 işlemleri için                                          | 1611 işlemleri sürümü için Microsoft Dynamics 365 olmayan bir ortamda kullanıyorsanız ve Microsoft Dynamics işlemleri platform için 3 (Kasım 2016) güncelleştirme emin olun. |
| Düzeltme KB 3215650                                                    | Microsoft Dynamics 365 işlemleri için sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.                                                                       |
| Yüklü uygulama işlemleri için Dynamics 365 sahip mobil aygıt | Dynamics 365 işlemleri uygulama için mobil app deponuzdan indirin.                                                                                                      |

## <a name="introduction"></a>Giriş
Mobil çalışma alanı denetleme maliyet, fiili maliyetleri bütçelenen maliyetleri karşı karşılaştırarak Geçerli Maliyet merkezleri performansını anlık bir görünümünü sağlar. Bireysel maliyet öğelerinin durumlarını aşağı inebilir.

### <a name="example"></a>Örnek

Bir çalışan uluslararası bir konferansa davet alır. Organizasyon seyahat masrafları karşılamak zorunda kalırsınız. Çalışan Yöneticisi kendi yaptığı konferansa katılın, ister. Yöneticisi kendi cep telefonu mobil çalışma alanını denetleme maliyet bütçe konferansa katılmak çalışana ait olup olmadığını görmek için hızlı bir şekilde açılır.

### <a name="data-security"></a>Veri güvenliği

Çalışma alanını denetleme maliyet verileri tarafından kullanıcı kimlik bilgileri güvenlik altına alınır. Bir maliyet merkezi Yöneticisi yalnızca kendi maliyet merkezi verileri görmek için izin verilir. Maliyet muhasebesi modülünde erişim düzeyi güvenliği yönetilir. Maliyet muhasebesi modülünde mobil çalışma yapılandırması denetleme maliyeti Maliyet muhasebeci tanımlayın. Çalışma işlemleri uygulama için Microsoft Dynamics 365 yayımlandıktan sonra Dynamics 365 mobil uygulama işlemleri için de kullanılabilir. Bu, kuruluşunuzdaki tüm maliyet merkezi yöneticileri aynı formatta veri görünmesini sağlar.

### <a name="actions-views-and-links"></a>Eylemler, görünümler ve bağlantılar

Mobil çalışma alanı için Dynamics 365 işlemleri app için denetleme maliyeti aşağıdaki eylemleri, görünümler ve bağlantılar sağlar:

-   Eylemler 
    -   Seçin **yapılandırmaları** için bir düzen seçin.
    -   Seçin **nesneleri maliyet** filtre veri istediğiniz Maliyet merkezleri çekilecek. **Not:** göre maliyet muhasebesi modülünde erişim listesi görüntülenir.

<!-- -->

-   Altında seçilene dayalı **Eylemler** ve ne Maliyet muhasebesi modülünde yapılandırılır, kartları aşağıdaki bilgileri görüntüleyebilirsiniz. Not tutar aynı biçimde görüntülenir: Gerçek, bütçe, sapma ve varyans %. 
    -   Gerçek vs bütçe (Cari dönem)
    -   Gerçek vs gözden geçirilmiş bütçe (Cari dönem)
    -   Gerçek vs bütçe (önceki dönem)
    -   Gerçek vs gözden geçirilmiş bütçe (önceki dönem)
    -   Gerçek vs bütçe (Yıllık)
    -   Gerçek vs gözden geçirilmiş bütçe (Yıllık)

<!-- -->

-   Bağlantılar
    -   Geçerli dönem için Ayrıntılar.
    -   Ayrıntılar için önceki dönem.
    -   Yıl başından bugüne yazın.

Bağlantılardan birini seçtiğinizde, bir kart başına maliyet öğesi görüntülenir. Kartları tutarı aşağıdaki biçimde görüntülenir: Gerçek, bütçe, bütçe farkı, bütçe varyans %, gözden geçirilmiş bütçe, bütçe farkı gözden geçirilmiş ve gözden geçirilmiş bütçe varyans %.  [![Maliyet kontrol etme](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Başlayın
Maliyet denetimi mobil app mobil aygıtınızda kullanmaya başlamak için aşağıdaki adımları izleyin.

1.  Mobil app store üzerinde karşıdan yükleyip Microsoft Dynamics 365 işlemleri uygulama için.
2.  Aygıtınızda uygulamayı başlatın.
3.  Dynamics 365 URL'nizi girin.
4.  Oturum açmak için şirket girin. Örneğin: **USMF**.
5.  İlk kez, oturum, Microsoft Dynamics 365 işlem hesabı için kullanıcı adı ve parola için uyarılırsınız. Kimlik bilgilerinizi girin. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz.

Çalışma alanları, mobil app üzerinde görüntülemek için önce istediğiniz çalışma işlemleri uygulama için Dynamics 365 yayımlamanız gerekir.

1.  Dynamics 365 işlemleri için başlatın.
2.  Git **Sistem Yönetimi**&gt;**Kurulum**&gt;**sistem parametreleri**.
3.  Seçin **Yönet mobil uygulama**.
4.  Çalışma alanını seçin ** denetleme maliyeti ** mobil platforma yayımlamak için.
5.  Seçin **çalışma yayımlamak**.
6.  Yayımlanmış çalışma öğrenmek için aygıtınızın yenileyin.

## <a name="view-the-performance-of-your-cost-center"></a>Performans, maliyet merkezinin görünümü
1.  Mobil aygıtınızda seçin **denetleme maliyeti** çalışma alanı.
2.  Seçin **nesne denetleme maliyeti**.
3.  ' I **Eylemler**.
4.  ' I **Select configuration** düzenini denetleme maliyeti seçilecek.
5.  Click **Done**.
6.  ' I **Eylemler**.
7.  ' I **maliyet nesnesi seçin** için size erişim verildi maliyet merkezlerini seçin.
8.  Click **Done**.
9.  Genel performans, maliyet merkezinin görüntüleyin.
10. ' I **ayrıntılar geçerli dönem için**.
11. Öğeleri tek tek maliyet performansını görüntüleyin.
12. Ayrıca belirli maliyet öğeler için arama yapabilirsiniz.



