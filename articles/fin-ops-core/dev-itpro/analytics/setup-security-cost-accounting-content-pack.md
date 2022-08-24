---
title: Maliyet muhasebesi analizi güvenliğini ayarlama Power BI içeriği
description: Bu makalede, Maliyet muhasebesindeki erişim düzeyinde güvenliği, Microsoft Power BI'daki satır düzeyinde güvenliğe nasıl yayabileceğiniz açıklanmaktadır.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267947"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Maliyet muhasebesi analizi güvenliğini ayarlama Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu makalede, Maliyet muhasebesindeki erişim düzeyinde güvenliği, Microsoft Power BI'daki satır düzeyinde güvenliğe nasıl yayabileceğiniz açıklanmaktadır. Bu işlevsellik, kullanıcıların yalnızca erişim izni verilen Power BI verilerini görmelerini garantilemeye yardımcı olur.

## <a name="overview"></a>Genel bakış

**Maliyet muhasebesi analizi** Microsoft Power BI içeriği, kullanıcının erişimini sınırlamak için Power BI'ın satır düzeyinde güvenliğini kullanır. Güvenlik, Maliyet muhasebesi parametrelerinde ayarlanan erişim düzeyinde organizasyon hiyerarşisine dayanır. **Maliyet muhasebesi analizi** Power BI içeriği hakkında daha fazla bilgi edinmek için bkz. [Maliyet muhasebesi Power BI içeriği](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Ayarlar
Erişim düzeyinde güvenliği Power BI'ya yaymak için, Power BI içeriği sahibinin bu adımları izlemesi gerekir.

> [!NOTE]
> **Maliyet muhasebesi analizi** Power BI içeriğini yayımlayan kullanıcı otomatik olarak sahip yapılır. Power BI'da güvenliği yalnızca bir sahip ayarlayabilir. Ayrıca, bir sahip PowerBI.com'a başka kullanıcılar ekleyene kadar **Maliyet muhasebesi analizi** Power BI içeriğindeki verileri sahibi dışında kimse göremez.

1. Tanım dosyasını Power BI'da yayımlayın.
2. PowerBI.com adresinde oturum açın.
3. **Maliyet muhasebesi analizi** Power BI içeriği için veri kümesini bulun.
4. Güvenlik sayfasını açın.

    ![Güvenlik sayfasını açma.](./media/CA-picture-1.png)

5. **Maliyet nesne denetleyicisi** rolü zaten oluşturulmuştur. Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisinin bir parçası olan diğer üyeleri ekleyin.

    ![Üyeleri ekleme.](./media/CA-picture-2.png)

**Maliyet nesnesi denetleyicisi** rolüne eklenen kullanıcılar, Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisindeki tanıma göre yalnızca görmelerine izin verilen verileri görecektir.

> [!NOTE]
> Power BI'dan katıştırılan kutucuklara ve raporlara satır düzeyinde güvenlik uygulanır.

## <a name="updating-security"></a>Güvenliği güncelleştirme
Maliyet muhasebesinde erişim düzeyinde güvenlikte güncelleştirmeler yapıldıysa ve Power BI'ın bu güncelleştirmeleri yansıtmasını istiyorsanız **Maliyet muhasebesi analizi** Power BI içeriğinin tüm varlık deposunu güncelleştirmeniz gerekir. Varlık deposu güncelleştirmesini tamamladıktan sonra PowerBI.com'daki yapıları güncelleştirmeniz gerekir. Bir varlık deposunun nasıl güncelleştirileceği hakkında daha fazla bilgi için bkz. [Varlık deposu ile Power BI tümleştirmesi](power-bi-integration-entity-store.md#update-entity-store). **Maliyet muhasebesi analizi** Power BI içeriğinin sahibi, organizasyon hiyerarşisinde yeni kullanıcılara erişim verildiği zaman da bir varlık deposu güncelleştirmesi yapmalıdır. Ayrıca, sahibin yeni kullanıcıları PowerBI.com'daki **Maliyet nesnesi denetleyicisi** rolüne eklemesi, böylece onlara satır düzeyinde güvenlik uygulanmasını sağlaması gerekir.

## <a name="disabling-security"></a>Güvenliği devre dışı bırakma
Kuruluşunuzun veri erişimini kısıtlamak istediğini varsayalım. Maliyet muhasebesini çalıştırdığınız zaman bazı nedenlerle güvenlik parametreleri devre dışı bırakılıyorsa, sahibin kullanıcıları Power BI'da **Maliyet muhasebesici** rolüne eklemesi gerekir. Güvenliği etkinleştirilmiş durumdan devre dışı duruma değiştirirseniz kullanıcıları **Maliyet nesnesi denetleyicisi** rolünden kaldırmak iyi bir fikirdir. Ve güvenliği yeniden etkinleştirdiğinizde de kullanıcıların eklenmesi de tavsiye edilir. Kullanıcılar her iki role ait olabilir. Birleşik erişim, her iki rolün birleşimidir. **Maliyet muhasebesi analizi** Power BI içeriğinde, birleşik erişimi olan kullanıcılar verilere sınırsız erişebilir. Amacınız sınırlı erişim uygulamaksa, kullanıcıların yalnızca **Maliyet nesnesi denetleyicisi** rolüne atanması gerekir. Bu satır düzeyinde güvenlik güncelleştirmeleri hemen uygulanır. Etkilenen kullanıcıların tarayıcılarını yenilemeleri gerekir.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI'ın satır düzeyinde güvenliği hakkında daha fazla bilgi için bkz. [Power BI'daki modelinizde güvenliği yönetme](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
