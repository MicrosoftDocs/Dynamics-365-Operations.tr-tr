---
title: Nakit akışı tahminini etkinleştirme (önizleme)
description: Bu konuda, Mali İçgörüler'de Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222570"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Nakit akışı tahminini etkinleştirme (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Mali İçgörüler'de Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.

> [!NOTE]
> Nakit akışında ödeme tahminlerini kullanmak için [Müşteri ödeme tahminlerini etkinleştirme](enable-cust-paymnt-prediction.md) konusunda anlatılan şekilde Müşteri ödeme tahminleri özelliğini ayarlamanız gerekir.

1. Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın. Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın. (Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Sürüm 10.0.20 veya sonrasını kullanıyorsanız veya bir Service Fabric dağıtımı kullanıyorsanız bu adımı atlayın. Mali içgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır. Özelliği **Özellik yönetimi** çalışma alanında görmüyorsanız veya özelliği açmaya çalışırken sorun yaşıyorsanız <fiap@microsoft.com> adresiyle iletişime geçin.
  
2. **Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:

    1. **Güncelleştirmeleri denetle**'yi seçin.
    2. Aşağıdaki özellikleri açın:

        - Yeni kılavuz denetimi
        - Izgaralarda gruplandırma (önizleme) 
        - Müşteriye ödeme tahminleri (önizleme)
        - Nakit akışı tahminleri (önizleme)

3. **Nakit ve banka yönetimi \> Nakit akışı tahmin kurulumu** bölümüne gidin ve tahminlere eklenmesi gereken likidite hesaplarını ekleyin.

    > [!NOTE]
    > Likidite hesapları ayarlanmamışsa nakit akışı oluşturulamaz.

4. **Nakit ve banka yönetimi \> Kurulum \> Mali İçgörüler (preview) \> Nakit akışı tahminleri (önizleme)** bölümüne gidin ve şu adımları izleyin:

    1. **Nakit akışı tahmini** sekmesinde, **Özelliği etkinleştir**'i seçin.
    2. **Tahmin modeli oluştur** seçeneğini belirleyin.

Nakit akışı tahmini özelliği hakkında daha fazla bilgi için bkz: [Nakit akışı tahmini](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
