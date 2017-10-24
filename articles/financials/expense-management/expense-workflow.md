---
title: "Gider iş akışı"
description: "Bu konu, iş akışı sistemini Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da, Gider yönetimindeki gider raporları için bir gözden geçirme işlemini nasıl kullanabileceğinizi açıklar."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c2e01d4da04cd24c2df1690e6e354e1c03cb50d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="expense-workflow"></a>Gider iş akışı

[!include[banner](../includes/banner.md)]

İş akışı sistemini Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da, Gider yönetimindeki gider raporları için bir gözden geçirme işlemi için kullanabilirsiniz. Gider raporlarını kimin onaylayacağını belirlemek için aşağıdaki ölçütleri kullanan bir iş akışı ayarlayabilirsiniz:

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

