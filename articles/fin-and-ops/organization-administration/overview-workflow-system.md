---
title: "İş akışı sistemi"
description: "Bu konuda, Financa and Operations'daki iş akışı sistemi açıklanmaktadır."
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 770796b42e79ad616b469e1dbf5149789bff0788
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="workflow-system"></a>İş akışı sistemi

[!include [banner](../includes/banner.md)]

Bu konuda, Financa and Operations'daki iş akışı sistemi açıklanmaktadır.

## <a name="what-is-workflow"></a>İş akışı nedir?

*İş akışı* terimi, biri sistem olarak ve diğeri iş süreci olarak iki şekilde tanımlanabilir.

### <a name="workflow-is-a-system"></a>İş akışı bir sistemdir

İş akışı, Finance and Operations ile yüklenen ve Uygulama Nesne Sunucusu (AOS) üzerinde çalışan bir sistemdir. İş akışı sistemi, bağımsız iş akışları veya iş süreçleri oluşturmak için kullanabileceğiniz işlevselliği sağlar.

### <a name="workflow-is-a-business-process"></a>İş akışı bir iş sürecidir

İş akışı, bir iş sürecini temsil eder. Bir görevin kimin tarafından tamamlanacağını, bir kararın kimin tarafından verileceğini veya bir belgenin kimin tarafından onaylanacağını göstererek bir belgenin sistem üzerinde nasıl aktığını veya taşındığını tanımlar. Örneğin, aşağıdaki görselde gider raporları için bir iş akışı gösterilmiştir.

![Kullanıcılara atanan öğelerle birlikte iş akışı](./media/workflow_user.gif)

Bu iş akışını daha iyi anlamak için Haluk'un 7.000 ABD Doları tutarında bir gider raporu teslim ettiğini düşünün. Bu senaryoda, Barış'ın mutlaka Haluk'un kendisine yönlendirdiği makbuzları gözden geçirmesi gerekir. Ardından Atilla ve Sibel'in gider raporunu onaylaması gerekir. Şimdi ise Sam'in 11,000 TL tutarında bir gider raporu teslim ettiğini varsayın. Bu senaryoda, Barış'ın makbuzları gözden geçirmesi ve Atilla, Sibel ve Ayla'nın gider raporunu onaylaması gerekir.

## <a name="benefits-of-using-the-workflow-system"></a> İş akışı sistemini kullanmanın yararları

İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:

- **Tutarlı süreçler** – Satın alma talepleri ve gider raporları gibi belirli belgelerin nasıl işlendiğini tanımlayabilirsiniz. İş akışı sistemini kullanarak, belgelerin tutarlı ve verimli şekilde işlenmesini ve onaylanmasını sağlayabilirsiniz.
- **Süreç görünürlüğü** – İş akışı örneklerinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz. Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.
- **Merkezi iş listesi** – Kullanıcılar, İş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir.


## <a name="workflow-content"></a>İş akışı içeriği

+ [İş akışı mimarisi](workflow-system-architecture.md)
+ [İş akışı öğeleri](workflow-elements.md)
+ [İş akışı eylemleri](workflow-actions.md)
+ [İş akışı oluşturma](create-workflow.md)
+ [İş akışı özelliklerini yapılandırma](configure-workflow-properties.md)
+ [Bir görev akışında el ile yapılan görevi yapılandır](configure-manual-task-workflow.md)
+ [Bir görev akışında otomatikleştirilmiş görev yapılandır](configure-automated-task-workflow.md)
+ [Bir onay işlemini bir iş akışında yapılandır](configure-approval-process-workflow.md)
+ [Bir onay adımını bir iş akışında yapılandır](configure-approval-step-workflow.md)
+ [Bir iş akışında bir el ile kararı yapılandırma](configure-manual-decision-workflow.md)
+ [Bir iş akışında koşullu bir kararı yapılandırma](configure-conditional-decision-workflow.md)
+ [Bir iş akışında bir paralel etkinlik yapılandırma](configure-parallel-activity-workflow.md)
+ [Paralel dalı iş akışında yapılandırma](configure-parallel-branch-workflow.md)
+ [Satır maddesi iş akışını yapılandırma](configure-line-item-workflow.md)

