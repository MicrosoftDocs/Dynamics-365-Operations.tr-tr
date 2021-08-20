---
title: Kalite emirleri oluşturmak için proses otomasyon akışlarını çağırın
description: Bu konu, kalite emirleri örneğini kullanarak iş süreçlerini otomatikleştirmek için Power Automate kullanmak için kaynaklar sağlar.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 00c0753990c06e75fff2f78425f1230c84a01c5085d0c295d1534e508fa29496
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765454"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a>Kalite emirleri oluşturmak için proses otomasyon akışlarını çağırın

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Kuruluşlar, standart iş süreçlerini otomatikleştirmek, personele daha uygun etkileşimler sağlamak ve iş süreçlerini otomatik olarak yönlendirmek için çeşitli veri sinyallerini ve sistemlerini kullanmak için artan bir talebe sahiptir. Robotik süreç otomasyonu (RPA) ve Microsoft Power Automate, işletmeler tekrarlayan süreçleri otomatikleştirmek için kodsuz bir deneyim kullanabilir, böylece verimlilik ve doğruluk kazanabilirler.

Supply Chain Management için indirilebilir otomasyon çözümü şablonu, örnek olarak kalite emirlerini kullanarak iş süreçlerini otomatikleştirmek için Power Automate'in nasıl kullanılabileceğini sunar.

Otomasyon çözüm şablonsunu [buradan](https://aka.ms/D365SCMQualityOrderRPASolution) indirebilirsiniz.

Bu özelliğe ve özelliklerine genel bir bakış için aşağıdaki videoya bakın: [Dynamics 365 Supply Chain Management'ta kalite emirleri oluşturmak için RPA kullanma](https://www.youtube.com/watch?v=LFbzJ6-H89w)

![RPA ile otomasyon seçenekleri.](media/rpa-automation-options.png "RPA ile otomasyon seçenekleri")

Power Automate çözüm şablonu, Supply Chain Management'ta kalite emirlerinin oluşturulmasını otomatikleştiren bir bulut otomasyon akışı ve bir masaüstü otomasyon akışı içerir.

Otomasyon, kullanıcı girişi veya makine sinyalleri (Nesnelerin İnterneti (IoT dahil)) dahil olmak üzere birçok olay ve sinyale yanıt olarak başlatılabilir. *Q-Order* Power Application örneği çözüm şablonuna dahil edilir. Kullanıcının bir madde QR kodunu taramasına, miktar girmesine ve kamera kullanarak resim eklemesine olanak tanır.

Çözüm parametreleri, otomasyonu bir üretim tesisindeki belirli bir kullanım örneği için yapılandırmak üzere dahil edilir.

![Kalite emri oluştur.](media/rpa-create-quality-roder.png "Kalite emri oluştur")

Kalite emri oluşturmayı otomatikleştirmek için örnek çözümü indirme, yükleme ve kullanma hakkında eksiksiz bir adım adım kılavuz için, bkz. [Power Automate Desktop kullanarak robotik süreç otomasyonu ile Dynamics 365 Supply Chain Management'ta kalite emri oluşturmayı otomatikleştirme](/power-automate/desktop-flows/dynamics365-scm-rpa).

