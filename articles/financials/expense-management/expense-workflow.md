---
title: "Gider iş akışı"
description: "Bu konu, Gider yönetimindeki gider raporları için bir gözden geçirme işlemini ayarlamak üzere Microsoft Dynamics 365 for Finance and Operations'ta iş akışı sistemini nasıl kullanabileceğinizi açıklar."
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6ee607f723659a5b6ecd655ba4fdfca35a4c582d
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="expense-workflow"></a>Gider iş akışı

[!include [banner](../includes/banner.md)]

Gider yönetimindeki gider raporları için bir gözden geçirme işlemi ayarlamak üzere Microsoft Dynamics 365 for Finance and Operations'ta iş akışı sistemini kullanabilirsiniz. Gider raporlarını kimin onaylayacağını belirlemek için aşağıdaki ölçütleri kullanan bir iş akışı ayarlayabilirsiniz:

- Çalışan raporlama hiyerarşisi ve önceden belirlenmiş onaylama limitleri
- Ara onaylayıcıları ve bir nihai onaylayıcıyı içeren çok düzeyli onay
- Mali boyutlar ve proje sorumluluğu
- Belirli kullanıcılar veya kullanıcı gruplarına atama

İş akışı onayları, seyahat talepleri, nakit avanslar ve katma değer vergisi (KDV) iadesi için onaylar oluşturulabilir.

**Örnek**

Aşağıda bir gider raporuna ilişkin gider yönetimi iş akışı örneği verilmiştir.

1. Bir personel bir gider raporu oluşturur ve kaydeder.
2. Personel gider raporunu onay için gönderir. Onaylayıcı, iş akışı ayarlandığında tanımlanmış kurallara dayanarak tespit edilir.
3. Onaylayıcı, bir gider raporunun onaylamaya hazır olduğunu belirten bir bildirim alır. Onaylayıcı, gider raporunu gözden geçirir ve aşağıdaki koşulların sağlandığını doğrular:

    - Giderler, hiçbir gider ilkesini ihlal etmiyor. Bir gider bir ilkeyi ihlal ediyorsa, onaylayıcı gider raporunun geçerli bir iş gerekçesi içerdiğini doğrular.
    - Elektronik girişler gider raporuna iliştirilir.

4. Onaylayıcı gider raporunu onaylar.
5. Gider raporu, deftere nakledilmesi için Borç hesapları koordinatörüne atanır.
6. Aşağıdaki adımlardan biri, otomatik deftere nakilin yapılandırmış olup olmamasına bağlı olarak gerçekleşir:

    - Otomatik deftere nakil yapılandırılmışsa, gider raporu ödem için işleme alınır ve gider raporunun durumu güncelleştirilir.
    - Otomatik raporlama yapılandırılmamışsa, Borç hesapları koordinatörü, tüm orijinal makbuzların gönderildiğini ve makbuzların, gider raporundaki giderlere karşılık geldiğini doğrular. Gider raporuna girilen tüm vergi kodlarının da doğru olarak doğrulanması gerekir.

Bu gereksinimler doğrulandıktan sonra gider raporu deftere nakledilir.

Gider raporu deftere nakledildikten sonra, gider raporu için ödeme onaylanır ve personele ödeme yapılır.

