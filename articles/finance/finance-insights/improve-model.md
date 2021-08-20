---
title: Tahmin modelini geliştirme (önizleme)
description: Bu konu, tahmin modellerinin performansını artırmak için kullanabileceğiniz özellikleri açıklamaktadır.
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 0bf4dd0f7edc528393af628eb3776c32957c459d3eaa166b0bc54d9318b54916
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768807"
---
# <a name="improve-the-prediction-model-preview"></a>Tahmin modelini geliştirme (önizleme)

[!include [banner](../includes/banner.md)]

Bu konu, tahmin modellerinin performansını artırmak için kullanabileceğiniz özellikleri açıklamaktadır. Modelinizi Microsoft Dynamics 365 Finance'teki **Müşteri ödeme tahminleri** çalışma alanında geliştirmeye başlarsınız. Ardından geliştirme adımları AI Builder'da tamamlanır.

## <a name="select-historical-outcomes"></a>Geçmiş sonuçları seçme

Önce faturalar için üç olası sonucu seçersiniz: **Zamanında**, **Geç** ve **Çok geç**. Üç sonuç da seçilmelidir. Sonuçlardan herhangi birinin seçimini kaldırırsanız eğitim faturalar eğitim işleminde filtrelenerek çıkarılır ve tahminin doğruluğu azalır.

[![Sonuçları onaylama.](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Kuruluşunuz yalnızca iki sonuç gerektiriyorsa **Geç** ve **Çok geç** eşiklerini 0 (sıfır) gün olarak değiştirin. Bu şekilde tahmini etkili bir şekilde ikili duruma daraltabilirsiniz: **Zamanında** veya **Geç**.

## <a name="select-fields"></a>Alanları seçin

Modele dahil edilecek alanları seçerken, bu listenin Azure Data Lake içindeki verilerle eşlenen Microsoft Dataverse tablosundaki tüm kullanılabilir alanlarını içerdiğine dikkat edin. Bu alanlardan bazıları **seçilmemelidir**. Seçilmemesi gereken alanlar üç kategoriden birine girer:

- Alan, Dataverse tablosu için gereklidir ancak veri gölünde alanla ilgili destekleyici veri yoktur.
- Alan bir kimlik olduğundan makine öğrenimi özelliği için bir anlam ifade etmez.
- Alan, tahmin sırasında kullanılamayacak bilgileri temsil eder.

Aşağıdaki bölümlerde, fatura ve müşteri varlıkları için kullanılabilir alanlar gösterilir ve eğitim için **seçilmemesi** gereken alanlar listelenir. Bu alanların her biri için belirtilen kategori, önceki listede yer alan kategorilere başvurur.
 
### <a name="invoice-dataverse-table"></a>Fatura Dataverse tablosu

Aşağıdaki şekilde, fatura tablosu için kullanılabilir alanlar gösterilmektedir.

[![Fatura tablosu için kullanılabilir alanlar.](./media/available-fields.png)](./media/available-fields.png)

Eğitim için aşağıdaki alanlar seçilmemelidir:

- **Fatura Hesabı** (kategori 2)
- **Kapalı** (kategori 3): Bu alan, faturaları eğitim (kapalı) ve tahmin (kapalı değil) için filtrelemek amacıyla kullanılır.
- **Ad** (kategori 1)
- **Kaynak kimliği** (kategori 2)
- **Kaynak kaydı** (kategori 2)
- **Kaynak tablosu** (kategori 2)

### <a name="customer-dataverse-table"></a>Müşteri Dataverse tablosu

Aşağıdaki şekilde, müşteri tablosu için kullanılabilir alanlar gösterilmektedir.

[![Müşteri tablosu için kullanılabilir alanlar.](./media/related-entities.png)](./media/related-entities.png)

Eğitim için aşağıdaki alan seçilmemelidir:

- **Satır benzersiz anahtarı** (Kategori 2)

## <a name="filters"></a>Filtreler

Faturadaki veya müşteri tablolarındaki alanlar için filtre ölçütü ayarlayarak eğitim için kullanılan faturalara filtre uygulayabilirsiniz. Örneğin, bir eşiği yalnızca, toplamın eşit olduğu veya belirli bir tutarı aşan faturaları içerecek şekilde ayarlayabilirsiniz. Alternatif olarak, belirli bir müşteri grubundaki müşterilerle ilişkilendirilmiş faturaları hariç tutabilirsiniz.

Verilerinize filtre uygulama hakkında daha fazla bilgi için bkz. [Tahmin modeli oluşturma](https://docs.microsoft.com/ai-builder/prediction-create-model#filter-your-data).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
