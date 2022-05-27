---
title: Nakit akışı tahminini etkinleştirme
description: Bu konuda, Mali İçgörüler'de Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8dba56af53090d5d78632da4d414143b136f8a8d
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713768"
---
# <a name="enable-cash-flow-forecasting"></a>Nakit akışı tahminini etkinleştirme

[!include [banner](../includes/banner.md)]

Bu konuda, Finance Insights'da Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.

> [!NOTE]
> Nakit akışında ödeme tahminlerini kullanmak için [Müşteri ödeme tahminlerini etkinleştirme](enable-cust-paymnt-prediction.md) konusunda anlatılan şekilde Müşteri ödeme tahminleri özelliğini ayarlamanız gerekir.
  
1. **Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:

    1. **Güncelleştirmeleri denetle**'yi seçin.
    2. **Tümü** sekmesinde, **Nakit akışı tahminlerini** arayın. Bu özelliği bulamazsanız **(Önizleme) Nakit akışı tahminleri**'ni arayın. 
    3. Özelliği etkinleştirin.

2. **Nakit ve banka yönetimi \> Nakit akışı tahmin kurulumu** bölümüne gidin ve tahminlere eklenmesi gereken likidite hesaplarını ekleyin. Ayrıca, **Alacak hesapları** ve **Borç hesapları** sekmelerindeki ödemeler için likidite hesabı da ayarlayın. Nakit akışı tahminini yeniden hesaplatın unutmayın.

    > [!NOTE]
    > Likidite hesapları ayarlanmamışsa nakit akışı oluşturulamaz.
    >
    > Nakit akışı tahminlerini ayarlamak hakkında daha fazla bilgi için bkz: [Nakit akışı tahmini](../cash-bank-management/cash-flow-forecasting.md).

3. **Nakit ve banka yönetimi \> Kurulum \> Mali İçgörüler (preview) \> Nakit akışı tahminleri (önizleme)** bölümüne gidin ve şu adımları izleyin:

    1. **Nakit akışı tahmini** sekmesinde, **Özelliği etkinleştir**'i seçin.
    2. **Tahmin modeli oluştur** seçeneğini belirleyin.

> [!NOTE]
> **Nakit akışı tahmini** modeli eğitimi, bir yıldan fazla süren ve 100 veya daha fazla hareket içeren veriler gerektirir. 1.000'den fazla hareket içeren en az iki yıllık veriniz olmasını öneririz.

Nakit akışı tahmini özelliği hakkında daha fazla bilgi için bkz: [Nakit akışı tahmini](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
