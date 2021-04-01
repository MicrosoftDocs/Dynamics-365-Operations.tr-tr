---
title: Retail'de saat ve işe devam yönetimi
description: Bu konuda, Dynamics 365 Commerce süre ve işe devam yönetimi için desteklenen senaryolar açıklanmaktadır.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28f4f72cd1272bd4562a58e343e50157143fac2c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254925"
---
# <a name="time-and-attendance-management-in-retail"></a>Retail'de saat ve işe devam yönetimi

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 Commerce süre ve işe devam yönetimi için desteklenen senaryolar açıklanmaktadır.

## <a name="manage-worker-setup-and-scheduling"></a>Çalışan kurulumunu ve planlamasını yönetme

### <a name="initial-configuration"></a>Başlangıç konfigürasyonu

- Yapılandırma sihirbazını çalıştırın.
- Çalışanları zaman kayıt çalışanları olarak kaydedin.

### <a name="plan-worker-schedules"></a>Çalışan zaman cetvelini planlayın

- İş planlayıcısını kullanarak profilleri uygulayın. Daha fazla bilgi için bkz. [İş planlayıcı kullanarak profiller uygulamak](https://technet.microsoft.com/library/aa551234.aspx).

Yapılandırma adımları hakkında daha fazla bilgi için bkz. [Zaman ve katılım ayarlama](https://technet.microsoft.com/library/aa496971.aspx).

### <a name="commerce-specific-configuration"></a>Commerce yapılandırması

- Zaman kayıtlarını geçerli kılmak istediğiniz çalışanlara yönelik olarak, Saat için bir işlevsellik profilini etkinleştirin. **POS işlevsellik profilleri** &gt; **İşlevler** &gt; **POS zaman kayıtları** &gt; **Zaman kayıtlarını etkinleştir** seçeneklerine tıklayın.
- Saat girişleri iznini görüntülemeyi etkinleştirmek için satış noktası (POS) izinleri gruplarını yapılandırın. Bu izinle, bir kullanıcı mağazadaki (rehber yoluyla, ilişkili olduğu başka bir mağazadan) diğer çalışanların saat kayıtlarını görüntüleyebilir. Bu izni bir yönetici görevi için geçerli hale getirebilirsiniz, ancak bir kasiyer görevi için geçerli hale getiremezsiniz. **POS izin grupları** &gt; **Saat girişlerini görüntüle** seçeneklerine tıklayın.

## <a name="register-time"></a>Kayıt saati

### <a name="cashier-and-non-cashier-time-registrations"></a>Kasiyer ve kasiyer dışı çalışan zaman kayıtları

- POS'de:

    - Giriş saati işlemleri:

        - Çekmece işlemi olmayan bir işlem veya Yeni vardiya ile oturum açın.
        - Bir Saat işlemi seçin.
        - İstenen bir işlemi seçin:

            - Giriş saati
            - İş Arası
            - Öğle Yemeği Molası
            - Çıkış saati

        <table>
        <thead>
        <tr>
        <th>Geçerli durum</th>
        <th>Geçerli işlemler</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Giriş saati</td>
        <td>
        <ul>
        <li>İş Arası</li>
        <li>Öğle Yemeği Molası</li>
        <li>Çıkış saati</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>İş Arası</td>
        <td>Giriş saati</td>
        </tr>
        <tr>
        <td>Öğle Yemeği Molası</td>
        <td>Giriş saati</td>
        </tr>
        <tr>
        <td>Çıkış saati</td>
        <td>Giriş saati</td>
        </tr>
        </tbody>
        </table>

        [![Saat Durumları](./media/timeclockstates.png)](./media/timeclockstates.png)

- Onay mesajını görüntüleyin ve geçerli etkinlik saatinin doğru olduğunu doğrulayın.
- Günlük defteri:

    - Saat etkinliğini görüntülemek için **Günlük Defteri** öğesine tıklayın.
    - Farklı zaman pencerelerini seçmek için zaman filtrelerini kullanın.
    - Birden çok mağaza konumunda çalışıyorsanız, zaman kayıtlarınızı zamanı kaydettiğiniz tüm mağazalardan görebilirsiniz. Seçilen bir mağazadan zaman kayıtlarını görüntülemek için mağaza filtresini kullanabilirsiniz.

- Farklı saat dilimleri:

    - Saati farklı bir konumdan görüntülüyorsanız (kasiyer günlük defteri için; veya yönetici senaryosu için **Saat girişlerini görüntüle** seçeneğini kullanarak) ve o konum farklı bir saat dilimindeyse, gördüğünüz zaman kayıtları yerel saat diliminize dönüştürülür. Örneğin, biri Arizona'da diğer Nevada'da olan iki mağazanın yöneticisisiniz. Bir kasiyer saat 9:00'da bir giriş saati kaydediyor Arizona'da. O anda, Nevada'da saat sabah 08:00. Bu nedenle, Nevada mağazasındaysanız ve zaman kaydı kayıtlarına bakarsanız, zaman kaydı sabah 08:00 olarak işaretlenir.

## <a name="view-worker-time-registrations"></a>Çalışan zaman kayıtlarını görüntüleme

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Çalışan zaman kayıtlarını görüntüleyin ve mağazaya ya da etkinlik türüne göre filtreleyin.

POS'de:

- **Saat girişlerini görüntüle** öğesini seçin.
- Sizinle aynı mağazaya atanan tüm çalışanlardan saat kayıt etkinliklerini görürsünüz.
- Zaman kayıtlarını filtrelemek için etkinlik türünü ve mağaza filtrelerini kullanabilirsiniz.

## <a name="process-and-manage-time-registrations"></a>Zaman kayıtlarını işleme ve yönetme

Bir Commerce kullanıcısı, zaman kayıtlarını hesaplamak, onaylamak ve ücret bordrosuna aktarmak için iş akışını takip eder.

### <a name="primary-operations"></a>Birincil işlemler

- Hesapla
- Onayla
- Ücret bordrosuna aktar

### <a name="other-common-operations"></a>Diğer ortak işlemler

- Toplu Çıkış
- Devamsızlığı Kaydet

Zaman ve katılım kayıtlarını ayarlamak hakkında daha fazla bilgi için bkz. [Zaman ve katılım kayıtlarını işleme](https://technet.microsoft.com/library/aa573180.aspx).


[!INCLUDE[footer-include](../includes/footer-banner.md)]