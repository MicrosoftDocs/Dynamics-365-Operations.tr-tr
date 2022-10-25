---
title: Zaman uyumsuz müşteri oluşturma modu hakkında SSS
description: Bu makalede, Microsoft Dynamics 365 Commerce'te zaman uyumsuz müşteri oluşturma modu hakkında sık sorulan soruların yanıtları verilmektedir.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690215"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Zaman uyumsuz müşteri oluşturma modu hakkında SSS

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te zaman uyumsuz (asenkron) müşteri oluşturma modu hakkında sık sorulan soruların yanıtları verilmektedir.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>"Zaman uyumsuz modda müşterileri düzenlemeyi etkinleştir" özelliğini neden etkinleştiremiyorum?

**Zaman uyumsuz modda müşterileri düzenlemeyi etkinleştir** özelliğini etkinleştirmeden önce, aşağıdaki özellikleri etkinleştirmeniz gerekir:

- Müşteri siparişleri ve müşteri hareketlerine yönelik performans iyileştirmeleri
- Gelişmiş zaman uyumsuz müşteri oluşturmayı etkinleştirme
- Müşteri adresleri için zaman uyumsuz oluşturmayı etkinleştir

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>"Zaman uyumsuz modda müşterileri düzenlemeyi etkinleştir" özelliği etkinleştirildikten sonra Commerce Headquarters'a yapılan gerçek zamanlı servis çağrılarını niçin hâlâ görüyorum?

Bu sorun, özellik durumunun ve diğer kanal meta verilerinin kanalla eşitlenmesini sağlamak amacıyla Commerce Data Exchange (CDX) işlerinin çalıştırılmadığı durumlarda oluşur. Senaryoyu yeniden denemeden önce, aşağıdaki CDX işlerinin Commerce Headquarters'da çalıştırıldığından emin olun:

- 1110 (Genel yapılandırma)
- 1010 (Müşteriler)
- 1070 (Kanal yapılandırması)

Commerce Scale Unit (CSU) içinde önbelleğe alınan veriler, CDX işleri çalıştırıldıktan sonra Commerce Headquarters'a hemen yansıtılmamış olabilir.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Commerce Headquarters, müşteri oluşturma veya güncelleştirmelerini satış noktasından (POS) veya e-ticaret kanalından neden göstermiyor?

Aşağıdaki eylemlerin burada listelendikleri sırayla yapıldığından emin olun.

1. Zaman uyumsuz müşteri verilerinin **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** ve **RETAILASYNCCUSTOMERATTRIBUTEV2** tablolarında depolandığından emin olmak için Commerce Headquarters'da CDX P-job öğesini çalıştırın.
1. Commerce Headquarters'da **Müşterileri ve kanal isteklerini eşitle** toplu işini çalıştırın. Toplu işin başarılı bir şekilde yürütülmesi tamamlandıktan sonra, önceden sözü edilen tablolardan başarıyla işlenmiş olan tüm kayıtlarda **OnlineOperationCompleted** alanı **1** olarak ayarlanır.

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>Zaman uyumsuz mod işleminde hangi müşteri yönetimi yönetiminin başarısız olduğunu nasıl anlarım ve gerekirse nasıl değişiklik yapabilirim?

Tüm zaman uyumsuz mod işlemlerini ve eşitlenme durumlarını görüntülemek için Commerce Headquarters'da **Ticaret ve Satış \> Müşteriler \> Müşteri eşitleme durumu** bölümüne gidin. Değişiklik yapmak için belirli bir işlemi düzenleyin, alanları güncelleştirin, **Kaydet**'i seçin ve ardından değişiklikleri eşitlemek için **Eşitle** seçeneğini belirleyin.

