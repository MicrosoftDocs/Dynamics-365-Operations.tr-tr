---
title: "Gerçek ve bütçe karşılaştırması Power BI içeriği"
description: "Bu konu, Gerçek ve bütçe karşılaştırması Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: tr-tr
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Gerçek ve bütçe karşılaştırması Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu, **Gerçek ve bütçe karşılaştırması** Microsoft Power BI içeriğini açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar. 

# <a name="overview"></a>Özet

**Gerçek ve bütçe karşılaştırması** Power BI içeriği, gerçek ve bütçe performansı karşılaştırmasını kuruluşları içinde izlemekten sorumlu kişiler için oluşturulmuştur. **Gerçek ve bütçe karşılaştırması** Power BI içeriği, bütçe farklılıklarınıza görünürlük sağlar. Farkların sebebini daha iyi anlayabilmek için geçerli yıl için bütçeyi hesap kategorisi, bütçe kodu, ana hesap, ana hesap açıklamaları veya mali dönem için analiz edebilirsiniz. 

# <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek
**Fiili - bütçe karşılaştırması** Power BI içeriğindeki raporlar **Genel muhasebe bütçesi ve tahminleri** ile **CFO** çalışma alanlarında gösterilir.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içeriğine dahil olan raporlar
Aşağı tablo, **Gerçek ve bütçe karşılaştırması** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.

| Rapor                      | Ölçümler |
|-----------------------------|---------|
| Giderler - Gerçek ve bütçe karşılaştırması | <ul><li>Bu yılki toplam giderler</li><li>Bu yılki bütçe toplam giderleri</li></ul> |
| Gelirler - Gerçek ve bütçe karşılaştırması  | <ul><li>Bu yılki toplam gelir</li><li>Bu yılki bütçe toplam gelirler</li><ul> |
| Gider                     | <ul><li>Bu yılki toplam giderler</li><li>Bütçeye dayalı gider hedefleri </li><ul> |
| Gelir                     | <ul><li>Bu yılki toplam gelir</li><li>Bütçeye dayalı gelir hedefleri </li><ul> |
| Net gelir                  | <ul><li>Bu yılki net gelir</li><li>Bütçeye dayalı net gelir hedefleri </li><ul> |

## <a name="extending-the-power-bi-content"></a>Power BI içeriğini genişletmek
Microsoft Dynamics Lifecycle Services (LCS) içinde kullanılabilir durumda olan içerik paketlerini kullanarak, Microsoft Dynamics 365'e oturum açmayan kişilere harika analizler sunabilirsiniz. Bu içerik paketlerini diğer raporları veya görsel öğeleri içerecek şekilde değiştirebilir ve içerik paketlerini analiz için Power BI.com kiracınıza yayınlayabilirsiniz. 

**Gerçek ve bütçe karşılaştırması** Power BI içeriğini LCS'deki Paylaşılan varlıklar kitaplığında bulabilirsiniz. İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](power-bi-content-microsoft-partners.md). Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.

# <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

| Varlık                    | İçindekiler |
|---------------------------|----------|
| Genel Muhasebe Etkinlikleri | Genel muhasebe için hareket tutarları |
| Bütçe Etkinlikleri         | Bütçe kaydı için hareket tutarları |
| Ana Hesaplar             | Raporların filtreleneceği ana hesaplar |
| Mali Takvimler          | Raporların filtreleneceği mali takvimler |
| Genel muhasebe defterleri                   | Genel muhasebeler, geçerli genel muhasebe için raporları filtrelemek için kullanılabilir |
| Bütçe Kodları              | Raporların filtreleneceği bütçe kodları |
| Tüzel Kişilikler            | Tüzel kişilikler, geçerli tüzel kişilikler için raporları filtrelemek için kullanılabilir |

