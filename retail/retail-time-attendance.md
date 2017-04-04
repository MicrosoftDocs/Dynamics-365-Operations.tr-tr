---
title: "Perakende süresi ve işe devam"
description: "Bu konu, Microsoft Dynamics 365 işlemleri - perakende için zaman ve katılımcı yönetimi için desteklenen senaryolar açıklanır."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>Perakende süresi ve işe devam

Bu konu, Microsoft Dynamics 365 işlemleri - perakende için zaman ve katılımcı yönetimi için desteklenen senaryolar açıklanır. 

<a name="manage-worker-setup-and-scheduling"></a>Alt yapısı ve zamanlama Yönet
----------------------------------

### <a name="initial-configuration"></a> Başlangıç konfigürasyonu

-   Yapılandırma sihirbazını çalıştırın.
-   Çalışanları zaman kayıt çalışanları olarak kaydedin.

### <a name="plan-worker-schedules"></a>Çalışan zaman cetvelini planlayın

-   İş planlayıcısını kullanarak profilleri uygulayın. Daha fazla bilgi için, bkz. <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Yapılandırma adımları hakkında bilgi için, bkz. <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Perakendeye özel yapılandırma

-   Zaman kayıtlarını geçerli kılmak istediğiniz çalışanlara yönelik olarak, Saat için bir işlevsellik profilini etkinleştirin. ' I **POS işlevsellik profilleri**&gt;**işlevler**&gt;**POS saat kayıtları**&gt;**etkinleştirmek zaman kayıtlarını**.
-   Saat girişleri iznini görüntülemeyi etkinleştirmek için satış noktası (POS) izinleri gruplarını yapılandırın. Bu izinle, bir kullanıcı mağazadaki (rehber yoluyla, ilişkili olduğu başka bir mağazadan) diğer çalışanların saat kayıtlarını görüntüleyebilir. Bu izni bir yönetici görevi için geçerli hale getirebilirsiniz, ancak bir kasiyer görevi için geçerli hale getiremezsiniz. ' I **POS izin grupları**&gt;**zaman saati girişlerini görüntülemek**.

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
    -   Saati farklı bir konumdan görüntülüyorsanız (kasiyer günlük defteri için; veya yönetici senaryosu için **Saat girişlerini görüntüle** seçeneğini kullanarak) ve o konum farklı bir saat dilimindeyse, gördüğünüz zaman kayıtları yerel saat diliminize dönüştürülür. Örneğin, iki mağazalar için bir yönetici, biri Arizona'da ve diğer Nevada'ya olur. Bir kasiyer bir saat-saat 9: 00'da kaydeder Arizona içinde. O anda, Nevada'da saat sabah 08:00. Bu nedenle, Nevada mağazasındaysanız ve zaman kaydı kayıtlarına bakarsanız, zaman kaydı sabah 08:00 olarak işaretlenir.

## <a name="view-worker-time-registrations"></a>Alt saat kayıtları görüntüle
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Çalışan zaman kayıtlarını görüntüleyin ve mağazaya ya da etkinlik türüne göre filtreleyin.

POS'de:

-   **Saat girişlerini görüntüle** öğesini seçin.
-   Sizinle aynı mağazaya atanan tüm çalışanlardan saat kayıt etkinliklerini görürsünüz.
-   Zaman kayıtlarını filtrelemek için etkinlik türünü ve mağaza filtrelerini kullanabilirsiniz.

## <a name="process-and-manage-time-registrations"></a>İşlem ve zaman kayıtlarını yönetme
Dynamics 365 - operasyonlar için perakende kullanıcı saat kayıtlarını transfer için bordro hesaplamak ve onaylamak için iş akışını izler.

### <a name="primary-operations"></a>Birincil işlemler

-   Hesapla
-   Onayla
-   Ücret bordrosuna aktar

### <a name="other-common-operations"></a>Diğer ortak işlemler

-   Toplu Çıkış
-   Devamsızlığı Kaydet

Zaman ve işe devam kayıtlarını işleme yolları hakkında daha fazla bilgi için, bkz. <https://technet.microsoft.com/en-us/library/aa573180.aspx>.


