---
title: Bir düzeltilmiş tahmini onayla
description: Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez. Bu makale bir tahminin yetkilendirildiği dönemi nasıl belirtebileceğinizi açıklar. Ayrıca, özel şirketler ve tahmin modelleri için tahmini nasıl yetkilendirebileceğinizi açıklar.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1db181913be8ecb4940eba2321d56cfb67f9e9d112495ddbb3e978abe813d918
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779218"
---
# <a name="authorize-an-adjusted-forecast"></a>Bir düzeltilmiş tahmini onayla

[!include [banner](../includes/banner.md)]

Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez. Bu makale bir tahminin yetkilendirildiği dönemi nasıl belirtebileceğinizi açıklar. Ayrıca, özel şirketler ve tahmin modelleri için tahmini nasıl yetkilendirebileceğinizi açıklar.

Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez. Tahminin yetkilendirildiği dönemin başlangıç ve bitiş tarihlerini belirtebilirsiniz. Bu işlev, belli aralıkları dondurmanızı sağlar. 

Belirttiğiniz başlangıç ve bitiş tarihleri, tahminin oluşturulduğu demetin başlangıç ve bitiş tarihlerine karşılık gelmek zorundadır. Sistem bu kısıtlamayı zorlar ve tarihleri ayarlama gerekliyse otomatik olarak ayarlar. 

**Yetkilendirme** sayfasının **Ayrıntılar** öğesinde, en son oluşturulan tahmin hakkındaki ayrıntıları görüntüleyebilirsiniz. 

Kullanılacak tahmini yetkilendirecek şirketleri ve tahmin modellerini seçebilirsiniz Varsayılan olarak, kılavuz tahmini talebin oluşturulduğu tüm şirketleri içerir. Her şirket için, ana planlama parametrelerinde ayarlanan geçerli tahmin planına karşılık gelen tahmin modeli önceden doldurulur. Ancak, bu tahmin modelini o şirkete ait olan herhangi bir tahmin modeli ile değiştirebilirsiniz. Seçili bir şirket için hiçbir tahmini talep verisi oluşturulmadıysa, içe aktarma sırasında bir uyarı iletisi alırsınız. 

**Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusunun nasıl çalıştığını anlamanız çok önemlidir. İstatistik temel tahminde manüel ayarlamalar yaptıysanız, bu onay kutusundaki işaretler kaldırılmış olsa bile ayarlanan değerleri kullanım için yetkilendirilir. Bununla birlikte, değişiklikler yetkilendirmeden sonra kaldırılır. Bu nedenle, bir daha bir tahmin oluşturulduğunda, bu tahmin sadece istatistiksel bir tahmin olur ve **Manüel ayarlamaları talep tahminine aktar** öğesi seçilse bile manüel geçersiz kılmalar olmaz. Bu nedenle, tüm manüel değişiklikleri tutmanıza veya kaldırmanıza izin veren bir mekanizma olan **Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusunu düşünebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)

[Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]