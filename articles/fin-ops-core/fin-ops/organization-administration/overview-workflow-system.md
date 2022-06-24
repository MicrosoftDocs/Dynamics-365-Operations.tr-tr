---
title: İş akışı sistemine genel bakış
description: Bu makalede iş akışı sistemi açıklanmaktadır.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13dd4335a8b939a44ea7176a90f660999c32a83a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863202"
---
# <a name="workflow-system-overview"></a>İş akışı sistemine genel bakış

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu makalede iş akışı sistemi açıklanmaktadır.

## <a name="what-is-workflow"></a>İş akışı nedir?

*İş akışı* terimi, biri sistem olarak ve diğeri iş süreci olarak iki şekilde tanımlanabilir.

### <a name="workflow-is-a-system"></a>İş akışı bir sistemdir

İş akışı, Uygulama Nesne Sunucusu (AOS) üzerinde çalışan bir sistemdir. İş akışı sistemi, bağımsız iş akışları veya iş süreçleri oluşturmak için kullanabileceğiniz işlevselliği sağlar.

### <a name="workflow-is-a-business-process"></a>İş akışı bir iş sürecidir

İş akışı, bir iş sürecini temsil eder. Bir görevin kimin tarafından tamamlanacağını, bir kararın kimin tarafından verileceğini veya bir belgenin kimin tarafından onaylanacağını göstererek bir belgenin sistem üzerinde nasıl aktığını veya taşındığını tanımlar. Örneğin, aşağıdaki görselde gider raporları için bir iş akışı gösterilmiştir.

![Kullanıcılara atanan öğelerle birlikte iş akışı.](./media/workflow_user.gif)

Bu iş akışını daha iyi anlamak için Haluk'un 7.000 ABD Doları tutarında bir gider raporu teslim ettiğini düşünün. Bu senaryoda, Barış'ın mutlaka Haluk'un kendisine yönlendirdiği makbuzları gözden geçirmesi gerekir. Ardından Atilla ve Sibel'in gider raporunu onaylaması gerekir. Şimdi ise Sam'in 11,000 TL tutarında bir gider raporu teslim ettiğini varsayın. Bu senaryoda, Barış'ın makbuzları gözden geçirmesi ve Atilla, Sibel ve Ayla'nın gider raporunu onaylaması gerekir.

## <a name="benefits-of-using-the-workflow-system"></a> İş akışı sistemini kullanmanın yararları

İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:

- **Tutarlı süreçler** – Satın alma talepleri ve gider raporları gibi belirli belgelerin nasıl işlendiğini tanımlayabilirsiniz. İş akışı sistemini kullanarak, belgelerin tutarlı ve verimli şekilde işlenmesini ve onaylanmasını sağlayabilirsiniz.
- **Süreç görünürlüğü** – İş akışı örneklerinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz. Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.
- **Merkezi iş listesi** – Kullanıcılar, İş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir.


## <a name="workflow-content"></a>İş akışı içeriği

+ [İş akışı sistemi mimarisi](workflow-system-architecture.md)
+ [İş akışı öğeleri](workflow-elements.md)
+ [İş akışı onay süreçlerindeki eylemler](workflow-actions.md)
+ [İş akışlarına genel bakış](create-workflow.md)
+ [İş akışı özelliklerini yapılandırma](configure-workflow-properties.md)
+ [İş akışında el ile girilen görevleri yapılandırma](configure-manual-task-workflow.md)
+ [İş akışında otomatikleştirilmiş görevleri yapılandırma](configure-automated-task-workflow.md)
+ [İş akışında onay işlemlerini yapılandırma](configure-approval-process-workflow.md)
+ [İş akışında onay adımlarını yapılandırma](configure-approval-step-workflow.md)
+ [İş akışında el ile girilen kararları yapılandırma](configure-manual-decision-workflow.md)
+ [İş akışında koşullu kararları yapılandırma](configure-conditional-decision-workflow.md)
+ [İş akışında paralel etkinlikleri yapılandırma](configure-parallel-activity-workflow.md)
+ [İş akışında paralel dalları yapılandırma](configure-parallel-branch-workflow.md)
+ [Satır maddesi iş akışlarını yapılandırma](configure-line-item-workflow.md)
+ [İş akışıyla ilgili SSS](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]