---
title: Bütçe tekliflerini etkinleştirme (önizleme)
description: Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995152"
---
# <a name="enable-budget-proposals-preview"></a>Bütçe tekliflerini etkinleştirme (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.

1. Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın. Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın. (Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Microsoft Dynamics 365 Finance dağıtımınız Service Fabric dağıtımıysa bu adımı atlayabilirsiniz. Mali İçgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır. Özelliği, **Özellik yönetimi** çalışma alanında göremiyorsanız veya açmaya çalıştığınızda sorunlarla karşılaşıyorsanız [Mali İçgörüler Uygulaması Önizleme ekibine](mailto:fiap@microsoft.com) e-posta gönderin.

2. **Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:

    1. **Güncelleştirmeleri denetle**'yi seçin.
    2. **Bütçe teklifi**'ni arayın ve bu özelliği etkinleştirin.

3. **Bütçeleme \> Kurulum \> Temel Bütçeleme \> Bütçe teklifi (önizleme)** bölümüne gidin ve **Özelliği etkinleştir**'i seçin.

#### <a name="privacy-notice"></a>Gizlilik bildirimi
Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]