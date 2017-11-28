---
title: "Perakende süresi ve işe devam"
description: "Bu konuda, Microsoft Dynamics 365 for Retail'de süre ve işe devam yönetimi için desteklenen senaryolar açıklanmaktadır."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d5672579c1e2d51e4b6494a1e86e3606c09a93a2
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="retail-time-and-attendance"></a>Perakende saati ve işe devam

[!include[banner](includes/banner.md)]


Bu konuda, Microsoft Dynamics 365 for Retail'de süre ve işe devam yönetimi için desteklenen senaryolar açıklanmaktadır. 

<a name="manage-worker-setup-and-scheduling"></a>Çalışan kurulumunu ve planlamasını yönetme
----------------------------------

### <a name="initial-configuration"></a> Başlangıç konfigürasyonu

-   Yapılandırma sihirbazını çalıştırın.
-   Çalışanları zaman kayıt çalışanları olarak kaydedin.

### <a name="plan-worker-schedules"></a>Çalışan zaman cetvelini planlayın

-   İş planlayıcısını kullanarak profilleri uygulayın. Daha fazla bilgi için, bkz. <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Yapılandırma adımları hakkında bilgi için, bkz. <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Perakendeye özel yapılandırma

-   Zaman kayıtlarını geçerli kılmak istediğiniz çalışanlara yönelik olarak, Saat için bir işlevsellik profilini etkinleştirin. **POS işlevsellik profilleri** &gt; **İşlevler** &gt; **POS zaman kayıtları** &gt; **Zaman kayıtlarını etkinleştir** seçeneklerine tıklayın.
-   Saat girişleri iznini görüntülemeyi etkinleştirmek için satış noktası (POS) izinleri gruplarını yapılandırın. Bu izinle, bir kullanıcı mağazadaki (rehber yoluyla, ilişkili olduğu başka bir mağazadan) diğer çalışanların saat kayıtlarını görüntüleyebilir. Bu izni bir yönetici görevi için geçerli hale getirebilirsiniz, ancak bir kasiyer görevi için geçerli hale getiremezsiniz. **POS izin grupları** &gt; **Saat girişlerini görüntüle** seçeneklerine tıklayın.

## <a name="register-time"></a>Kayıt saati
### <a name="cashier-and-non-cashier-time-registrations"></a>Kasiyer ve kasiyer dışı çalışan zaman kayıtları

-   POS'de:
    -   Giriş saati işlemleri:
        -   Çekmece işlemi olmayan bir işlem veya Yeni vardiya ile oturum açın.
        -   Bir Saat işlemi seçin.
        -   İstenen bir işlemi seçin:
            -   Giriş saati
            -   İş Arası
            -   Öğle Yemeği Molası
            -   Çıkış saati

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Geçerli durum</th>
    <th>Geçerli işlemler</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Giriş saati</td>
    <td><ul>
    <li>İş Arası</li>
    <li>Öğle Yemeği Molası</li>
    <li>Çıkış saati</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>İş Arası</td>
    <td>Giriş saati</td>
    </tr>
    <tr class="odd">
    <td>Öğle Yemeği Molası</td>
    <td>Giriş saati</td>
    </tr>
    <tr class="even">
    <td>Çıkış saati</td>
    <td>Giriş saati</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Onay mesajını görüntüleyin ve geçerli etkinlik saatinin doğru olduğunu doğrulayın.
-   Günlük defteri:
    -   Saat etkinliğini görüntülemek için **Günlük Defteri** öğesine tıklayın.
    -   Farklı zaman pencerelerini seçmek için zaman filtrelerini kullanın.
    -   Birden çok mağaza konumunda çalışıyorsanız, zaman kayıtlarınızı zamanı kaydettiğiniz tüm mağazalardan görebilirsiniz. Seçilen bir mağazadan zaman kayıtlarını görüntülemek için mağaza filtresini kullanabilirsiniz.

<!-- -->

-   Farklı saat dilimleri:
    -   Saati farklı bir konumdan görüntülüyorsanız (kasiyer günlük defteri için; veya yönetici senaryosu için **Saat girişlerini görüntüle** seçeneğini kullanarak) ve o konum farklı bir saat dilimindeyse, gördüğünüz zaman kayıtları yerel saat diliminize dönüştürülür. Örneğin, biri Arizona'da diğer Nevada'da olan iki mağazanın yöneticisisiniz. Bir kasiyer saat 9:00'da bir giriş saati kaydediyor Arizona'da. O anda, Nevada'da saat sabah 08:00. Bu nedenle, Nevada mağazasındaysanız ve zaman kaydı kayıtlarına bakarsanız, zaman kaydı sabah 08:00 olarak işaretlenir.

## <a name="view-worker-time-registrations"></a>Çalışan zaman kayıtlarını görüntüleme
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Çalışan zaman kayıtlarını görüntüleyin ve mağazaya ya da etkinlik türüne göre filtreleyin.

POS'de:

-   **Saat girişlerini görüntüle** öğesini seçin.
-   Sizinle aynı mağazaya atanan tüm çalışanlardan saat kayıt etkinliklerini görürsünüz.
-   Zaman kayıtlarını filtrelemek için etkinlik türünü ve mağaza filtrelerini kullanabilirsiniz.

## <a name="process-and-manage-time-registrations"></a>Zaman kayıtlarını işleme ve yönetme
Dynamics 365 for Retail kullanıcısı, zaman kayıtlarını hesaplamak, onaylamak ve ücret bordrosuna aktarmak için iş akışını takip eder.

### <a name="primary-operations"></a>Birincil işlemler

-   Hesapla
-   Onayla
-   Ücret bordrosuna aktar

### <a name="other-common-operations"></a>Diğer ortak işlemler

-   Toplu Çıkış
-   Devamsızlığı Kaydet

Zaman ve işe devam kayıtlarını işleme yolları hakkında daha fazla bilgi için, bkz. <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




