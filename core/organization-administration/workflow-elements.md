---
title: "İş akışı öğeleri"
description: "Bu makalede, bir iş akışını oluşturan çeşitli öğeler açıklanmaktadır."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 05a35e91d3e502309c42c85960b5b1e2025f0e6e
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="workflow-elements"></a>İş akışı öğeleri

[!include[banner](../includes/banner.md)]


Bu makalede, bir iş akışını oluşturan çeşitli öğeler açıklanmaktadır.

İş akışı öğelerden oluşur. Aşağıdaki bölümlerde her bir öğe türü tanımlanmıştır.

## <a name="tasks"></a>Görevler
*Görev*, gerçekleştirilmesi gereken bir iş birimidir. İş akışına iki tür görev eklenebilir: manuel görevler ve otomatik görevler.

### <a name="manual-task"></a>Manuel görev

*Manuel görev*, kullanıcı tarafından gerçekleştirilmesi gereken bir iş birimidir. Örneğin, bir gider raporu iş akışı, atanan kullanıcının aşağıdaki eylemleri tamamlamasını gerektiren manuel görevler içerebilir:

-   Bir gider raporu ile birlikte gönderilen girişleri incelemek.
-   Bir personel müdürünü aramak.

### <a name="automated-task"></a>Otomatik görev

*Otomatik görev*, sistem tarafından gerçekleştirilmesi gereken bir iş birimidir. İnsan etkileşimi gerekli değildir. Örneğin, bir satış emri iş akışı, sistemin aşağıdaki eylemleri tamamlamasını gerektiren otomatik görevler içerebilir:

-   Bir kredi denetimi gerçekleştirmek.
-   Bir kayıt yoksa müşteri için bir müşteri kaydı oluşturmak.

## <a name="approval-processes"></a>Onay işlemleri
*Onay işlemi*, ayrı adımlardan oluşan bir işlemdir. Her onay adımında, kullanıcı aşağıdaki eylemleri gerçekleştirebilir:

-   Belgeyi onaylama.
-   Belgeyi reddetme.
-   Belgede değişiklik talep etme.
-   Belgeyi onay için başka bir kullanıcıya atama.

## <a name="lineitem-workflow-elements"></a>Satır maddesi iş akışı öğeleri
Belgeleri veya bir belgedeki satır maddelerini işlemek için bir iş akışı oluşturulabilir. Örneğin, zaman çizelgeleri için onay iş akışı hazırladınız. (Biz bu iş akışına *belge iş akışı* diyeceğiz.) Bu belge iş akışına bir *satır öğesi iş akışı* öğesi ekleyebilirsiniz. Satır maddesi öğesi çalıştırıldığında, belgedeki her satır maddesi işlenmek üzere gönderilir. Tüm satır maddelerinin aynı satır maddesi iş akışı tarafından işlenmesini isteyebilirsiniz veya her bir satır maddesinin farklı bir satır maddesi iş akışı tarafından işlenmesini isteyebilirsiniz. Bir işçinin aşağıdaki şekle benzer bir zaman çizelgesi gönderdiğini düşünün. ![Satır maddeli iş akışı](./media/workflow_lineitemworkflow.gif) Bu senaryoda, aşağıdaki satır maddesi iş akışlarını oluşturmak isteyebilirsiniz:

-   **Satır maddesi iş akışı 1** – Bu iş akışı proje kodunun 1111 olduğu satır maddelerini işlemek için kullanılır.
-   **Satır maddesi iş akışı 2** – Bu iş akışı proje kodunun 2222 olduğu satır maddelerini işlemek için kullanılır.
-   **Satır maddesi iş akışı 3** – Bu iş akışı proje kodunun 3333 olduğu satır maddelerini işlemek için kullanılır.

## <a name="flowcontrol-elements"></a>Akış kontrolü öğeleri
Aşağıdaki öğeler, alternatif dalları veya aynı anda çalışan dalları olan iş akışları tasarlamanıza imkan verir.

### <a name="manual-decision"></a>El ile karar

*Manuel karar*, bir iş akışının iki dala ayrıldığı bir noktadır. Bir kullanıcı bir karar almalıdır ve bu karar gönderilen belgeyi işlemek için hangi dalın kullanılacağını belirler.

### <a name="conditional-decision"></a>Koşullu karar

*Koşullu karar* da bir iş akışının iki dala ayrıldığı bir noktadır. Ancak, gönderilen belgeyi işlemek için hangi dalın kullanılacağına sistem karar verir. Bu kararı vermek için, sistem belgeyi değerlendirerek belirtilen koşulları karşılayıp karşılamadığını belirler.

### <a name="parallel-activity"></a>Paralel faaliyet

*Paralel etkinlik*, aynı anda çalışan iki veya daha fazla iş akışı dalı içeren bir iş akışı öğesidir.

### <a name="subworkflow"></a>Alt iş akışı

*Alt iş akışı*, başka bir iş akışının bağlamında çalışan bir iş akışıdır



