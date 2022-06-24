---
title: Gerçek - bütçe Power BI içeriği
description: Bu makalede, Fiili değer ve bütçe karşılaştırması Power BI içeriği açıklanmaktadır. Raporlara nasıl erişileceğini açıklar ve veri modeli hakkında bilgi sağlar.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff57d052b66103ad716ad8d55afb4fcb095d2c02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847296"
---
# <a name="actual-vs-budget-power-bi-content"></a>Gerçek - bütçe Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu makalede, **Fiili değer ve bütçe karşılaştırması** Microsoft Power BI içeriği açıklanmaktadır. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Gerçek ve bütçe** karşılaştırması Power BI içeriği, gerçek ve bütçe performansı karşılaştırmasını kuruluşları içinde izlemekten sorumlu kişiler için oluşturulmuştur. **Gerçek ve bütçe** karşılaştırması Power BI içeriği, bütçe farklılıklarınıza görünürlük sağlar. Farkların sebebini daha iyi anlayabilmek için geçerli yıl için bütçeyi hesap kategorisi, bütçe kodu, ana hesap, ana hesap açıklamaları veya mali dönem için analiz edebilirsiniz.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**Fiili - bütçe** karşılaştırması Power BI içeriğindeki raporlar **Genel muhasebe bütçesi ve tahminleri** ile **CFO** çalışma alanlarında gösterilir.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan raporlar
Aşağı tablo, **Gerçek ve bütçe** karşılaştırması Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.

| Rapor                      | Ölçümler                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Giderler - Gerçek ve bütçe karşılaştırması | <ul><li>Bu yılki toplam giderler</li><li>Bu yılki bütçe toplam giderleri</li></ul>  |
| Gelirler - Gerçek ve bütçe karşılaştırması  | <ul><li>Bu yılki toplam gelir</li><li>Bu yılki bütçe toplam gelirler</li><ul>     |
| Gider                     | <ul><li>Bu yılki toplam giderler</li><li>Bütçeye dayalı gider hedefleri</li><ul> |
| Gelir                     | <ul><li>Bu yılki toplam gelir</li><li>Bütçeye dayalı gelir hedefleri</li><ul>   |
| Net gelir                  | <ul><li>Bu yılki net gelir</li><li>Bütçeye dayalı net gelir hedefleri</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

| Varlık                    | İçindekiler                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Genel Muhasebe Etkinlikleri | Genel muhasebe için hareket tutarları                                       |
| Bütçe Etkinlikleri         | Bütçe kaydı için hareket tutarları                                      |
| Ana Hesaplar             | Raporların filtreleneceği ana hesaplar                                               |
| Mali Takvimler          | Raporların filtreleneceği mali takvimler                                            |
| Genel muhasebe defterleri                   | Genel muhasebeler, geçerli genel muhasebe için raporları filtrelemek için kullanılabilir              |
| Bütçe Kodları              | Raporların filtreleneceği bütçe kodları                                                |
| Tüzel Kişilikler            | Tüzel kişilikler, geçerli tüzel kişilikler için raporları filtrelemek için kullanılabilir |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]