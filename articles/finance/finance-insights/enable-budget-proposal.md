---
title: Bütçe tekliflerini etkinleştirme (önizleme)
description: Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: cc7b06ee40553a254a939babc30e6f5c99f85507c1a3db4e916f480560cf8835
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768951"
---
# <a name="enable-budget-proposals-preview"></a>Bütçe tekliflerini etkinleştirme (önizleme)

[!include [banner](../includes/banner.md)]

Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.

1. Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın. Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın. (Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Sürüm 10.0.20 veya sonrasını kullanıyorsanız veya bir Service Fabric dağıtımı kullanıyorsanız bu adımı atlayın. Mali içgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır. Özelliği **Özellik yönetimi** çalışma alanında görmüyorsanız veya özelliği açmaya çalışırken sorun yaşıyorsanız <fiap@microsoft.com> adresiyle iletişime geçin.

2. **Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:

    1. **Güncelleştirmeleri denetle**'yi seçin.
    2. **Bütçe teklifi**'ni arayın ve bu özelliği etkinleştirin.

3. **Bütçeleme \> Kurulum \> Temel Bütçeleme \> Bütçe teklifi (önizleme)** bölümüne gidin ve **Özelliği etkinleştir**'i seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
