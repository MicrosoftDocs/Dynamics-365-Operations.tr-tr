---
title: "Maliyet nesnesi denetleyicilerinin erişim haklarını tanımlama"
description: "Bu konu, maliyet nesnesi denetleyicileri için erişim hakları hakkında bilgi sağlar."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6403aabb6b029807b42ab1ccb11756dcb0dda5dc
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a>Bir maliyet nesnesi denetleyicisinin erişim hakları

[!include[banner](../includes/banner.md)]

**Maliyet kontrolü** çalışma alanı, yöneticilerin maliyet nesnelerinin performanslarını görüntüleyebilecekleri merkezi noktadır. Bu çalışma alanı, yöneticilerin Maliyet muhasebesi verisini, maliyet muhasebecisi olmasalar bile kullanmalarına olanak sağlar. Güvenlik nedeniyle, yöneticiler yalnızca sorumlu oldukları belirli maliyet nesnelerinin Maliyet muhasebesi verilerini görmelidirler.

Maliyet muhasebesinde dört benzersiz rol vardır.

| Rol adı               | Lisans      |
|-------------------------|--------------|
| Maliyet muhasebesi yöneticisi | Faaliyet     |
| Maliyet muhasebecisi         | Operations   |
| Maliyet muhasebe memuru   | Operations   |
| Maliyet nesnesi denetleyicisi  | Takım üyeleri |

Bu konu, **Maliyet nesnesi denetleyicisi** rolünü bir yöneticiye atamayı açıklar.

**Maliyet nesnesi denetleyicisi** rolü bir yöneticiye atandığı, yönetici aşağıdaki görevleri yerine getirebilir:

- **Maliyet denetimi** çalışma alanına erişmek (istemci içinde).

    - Ayrıntıya inme deneyimini destekleyen sayfalarda ayrıntıya inme ve erişim sağlama.

- **Maliyet denetimi** çalışma alanına erişmek (mobil uygulamada).

> [!NOTE]
> **Maliyet nesnesi denetçisi** rolü, kullanıcının hangi maliyet nesnesine erişebileceğini ve görünümüne sahip olacağını denetlemez. Satır düzeyi güvenlik, boyut hiyerarşileri ve Erişim listesi hiyerarşisi tarafından sağlanır.

## <a name="grant-access-rights"></a>Erişim haklarını verme
Aşağıdaki örnek, bir boyut hiyerarşisinin nasıl görünebileceğini gösterir.

**Boyut hiyerarşisi ayrıntıları**

| Boyut hiyerarşisi adı | Boyut    | Boyut hiyerarşisi türü adı      | Erişim listesi hiyerarşisi |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizasyon             | Maliyet merkezleri | Boyut sınıflandırması hiyerarşisi | **Evet**               |

Her bir düğüme bir veya birden fazla kullanıcı kimliği eklemek için hiyerarşi tasarımcısındaki **Kullanıcılar** hızlı sekmesini kullanabilirsiniz.

|                                   | Kullanıcılar            | Boyut üyesi aralıkları   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Düğümler**                         | **Kullanıcı Kimliği**      | **Kaynak boyut üyesi** | **Hedef boyut üyesi** |
| Organizasyon                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Yönetici                 | Nisan            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;İK        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Üretim            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Paketleme | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montaj  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Maliyet muhasebesindeki tüm girişleri görebilmeleri için maliyet muhasebecileri, hiyerarşinin en üst düzeyine atanmalıdır.

Erişim listesi hiyerarşisi ve güvenlik ayarları uygulanabilmeden önce, **Maliyet nesnesi boyut üyelerini görüntüleme erişimini etkinleştir** seçeneği, **Maliyet muhasebesi parametreleri** sayfasında **Genel** sekmesi üzerinde **Evet** olarak ayarlanmalıdır (**Maliyet muhasebesi** > **Kurulum** > **Parametreler**).

Erişim listesi hiyerarşisi için ayarlar, aşağıdaki alanlarda gösterilen veriyi denetlemek için kullanılır:

- **Maliyet kontrolü** çalışma alanı (istemci içinde):

    - Sayfalardaki veri ayrıntıya inme için kullanılır

- **Maliyet kontrolü** çalışma alanı (mobil uygulama içinde):

    - Kartlardaki bakiyeler

- Microsoft Power BI:

    - Veri, Power BI görselleştirmeleri içinde gösterilir
    - Microsoft Dynamics 365 for Finance and Operations istemcisinde gömülü veri Power BI görselleştirmeleri

> [!IMPORTANT]
> - Erişim listesi hiyerarşisi Power BI içerisindeki veriyi etkileyebilmeden önce, Power BI içindeki Erişim listesi hiyerarşisi ve satır düzeyi güvenliği eşleştirilmelidir. Daha fazla bilgi için bkz [Maliyet muhasebesi İçerik Paketi için güvenlik kurma](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Bu konu, **Maliyet kontrolü** çalışma alanını kullanmadan önce ayarlanması gereken önkoşulları gösterir.

Ayrıca bkz.

- [Maliyet kontrolü çalışma alanı](cost-control-workspace.md)
- [Boyut hiyerarşisi](dimension-hierarchy.md)
- [Maliyet muhasebesi içerik paketi için güvenliği kurmak](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

