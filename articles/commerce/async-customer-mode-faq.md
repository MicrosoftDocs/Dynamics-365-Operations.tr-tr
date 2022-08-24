---
title: Zaman uyumsuz müşteri oluşturma modu hakkında SSS
description: Bu makalede, Microsoft Dynamics 365 Commerce'te zaman uyumsuz müşteri oluşturma modu hakkında sık sorulan soruların yanıtları verilmektedir.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229882"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Zaman uyumsuz müşteri oluşturma modu hakkında SSS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

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

1. **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** ve **RETAILASYNCCUSTOMERATTRIBUTEV2** tablolarında depolanan zaman uyumsuz müşteri verilerinin Commerce headquarters'da bulunduğundan emin olmak için Commerce headquarters'da CDX P-job öğesini çalıştırın.
1. Commerce Headquarters'da **Müşterileri ve kanal isteklerini eşitle** toplu işini çalıştırın. Toplu işin başarılı bir şekilde yürütülmesi tamamlandıktan sonra, önceden sözü edilen tablolardan başarıyla işlenmiş olan tüm kayıtlarda **OnlineOperationCompleted** alanı **1** olarak ayarlanır.
