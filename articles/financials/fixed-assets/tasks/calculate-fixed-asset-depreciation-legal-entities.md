---
title: Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama
description: Sabit kıymet amortismanı tüzel kişilikler arasında tek bir adımda çalıştırılabilir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840109"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sabit kıymet amortismanı tüzel kişilikler arasında tek bir adımda çalıştırılabilir. Bu yordam, birden fazla tüzel kişilik için işlemi nasıl ayarlayacağınızı ve çalıştıracağınızı gösterir. Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Şirketler arası amortisman çalıştırma günlüklerini ayarlama
1. Sabit kıymetler > Kurulum > Sabit kıymet parametreleri'ne gidin.
2. Sabit kıymet teklifleri bölümünü genişletin.
3. Ekle öğesini tıklatın.
4. Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.
5. Günlük adı alanına bir değer girin veya seçin.
    * Her tüzel kişilik için Sabit kıymet parametreleri sayfasında günlük kurulumunu yineleyin.  

## <a name="depreciation-run"></a>Amortisman çalıştırma
1. Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin.
2. Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.
    * Günlük adı varsayılan olarak Sabit kıymet parametrelerinden alınacaktır. Burada geçerli tüzel kişilik için değiştirilebilir.  
3. Bitiş tarihi alanına bir tarih girin.
    * Amortisman çalıştırmaya dahil edilecek tüzel kişilikleri seçin.  
    * Yalnızca Sabit kıymet parametreleri sayfasında Sabit kıymet teklifleri için ayarlanan günlükleri bulunan tüzel kişilikler listede görüntülenir.  
4. Günlükleri deftere naklet alanında Evet'i seçin.
    * Filtreleme alanları, bu amortisman çalıştırma için seçilen tüzel kişiliklerle ilgili tüm sabit kıymetleri, grupları ve defterleri içerir.  
    * Toplu işleme seçeneği varsayılan olarak etkindir. Bu seçenek etkinleştirildiğinde, amortisman günlüğü oluşturma ve deftere nakletme arka planda çalışır.  
5. Günlük oluştur'a tıklayın.
6. Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.

