---
title: "Bir düzeltilmiş tahmini onayla"
description: "Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez. Bu makale bir tahminin yetkilendirildiği dönemi nasıl belirtebileceğinizi açıklar. Ayrıca, özel şirketler ve tahmin modelleri için tahmini nasıl yetkilendirebileceğinizi açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 324f7385e8064eedcf35f0f07bb3b2ef6474f410
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Bir düzeltilmiş tahmini onayla

[!include[banner](../includes/banner.md)]


Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez. Bu makale bir tahminin yetkilendirildiği dönemi nasıl belirtebileceğinizi açıklar. Ayrıca, özel şirketler ve tahmin modelleri için tahmini nasıl yetkilendirebileceğinizi açıklar.

Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez. Tahminin yetkilendirildiği dönemin başlangıç ve bitiş tarihlerini belirtebilirsiniz. Bu işlev, belli aralıkları dondurmanızı sağlar. 

Belirttiğiniz başlangıç ve bitiş tarihleri, tahminin oluşturulduğu demetin başlangıç ve bitiş tarihlerine karşılık gelmek zorundadır. Sistem bu kısıtlamayı zorlar ve tarihleri ayarlama gerekliyse otomatik olarak ayarlar. 

**Yetkilendirme** sayfasının **Ayrıntılar** öğesinde, en son oluşturulan tahmin hakkındaki ayrıntıları görüntüleyebilirsiniz. 

Kullanılacak tahmini yetkilendirecek şirketleri ve tahmin modellerini seçebilirsiniz Varsayılan olarak, kılavuz tahmini talebin oluşturulduğu tüm şirketleri içerir. Her şirket için, ana planlama parametrelerinde ayarlanan geçerli tahmin planına karşılık gelen tahmin modeli önceden doldurulur. Ancak, bu tahmin modelini o şirkete ait olan herhangi bir tahmin modeli ile değiştirebilirsiniz. Seçili bir şirket için hiçbir tahmini talep verisi oluşturulmadıysa, içe aktarma sırasında bir uyarı iletisi alırsınız. 

**Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusunun nasıl çalıştığını anlamanız çok önemlidir. İstatistik temel tahminde manüel ayarlamalar yaptıysanız, bu onay kutusundaki işaretler kaldırılmış olsa bile ayarlanan değerleri kullanım için yetkilendirilir. Bununla birlikte, değişiklikler yetkilendirmeden sonra kaldırılır. Bu nedenle, bir daha bir tahmin oluşturulduğunda, bu tahmin sadece istatistiksel bir tahmin olur ve **Manüel ayarlamaları talep tahminine aktar** öğesi seçilse bile manüel geçersiz kılmalar olmaz. Bu nedenle, tüm manüel değişiklikleri tutmanıza veya kaldırmanıza izin veren bir mekanizma olan **Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusunu düşünebilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)

[Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md)




