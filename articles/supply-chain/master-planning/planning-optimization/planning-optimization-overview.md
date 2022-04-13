---
title: Planlamayı En İyi Duruma Getirmeye genel bakış
description: Bu konu, Planlamayı En İyi Duruma Getirme işlevine genel bir bakış sağlar.
author: t-benebo
ms.date: 10/31/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 7a44de70eeed4a32af47cd5ab636cac74400a2ac
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469100"
---
# <a name="planning-optimization-overview"></a>Planlamayı En İyi Duruma Getirmeye genel bakış

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi, Dynamics 365 Supply Chain Management dışında gerçekleşecek master planlama hesaplamasını ve ilgili SQL veritabanını etkinleştirir. Planlamayı En İyi Duruma Getirme işleviyle ilişkili kazançlar arasında master planlama çalışmaları sırasında artan performans ve SQL veritabanı üzerinde en az etki vardır. Hızlı planlama çalışmaları, planlayıcıların talep ve parametre değişikliklerine hemen tepki verebileceği şekilde ofis saatlerinde de yapılabilir.

Planlamayı En İyi Duruma Getirmeyi kullanmak için Microsoft Dynamics Lifecycle Services'taki (LCS) projenizden Planlamayı En İyi Duruma Getirme Eklentisi'ni yüklemeniz ve Supply Chain Management'ta Planlamayı En İyi Duruma Getirme işlevini açmanız gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md).

Aşağıdaki resimde, Planlamayı En İyi Duruma Getirmeyi ofis saatlerinde çalıştırmanın avantajı gösterilmektedir.

![Planlamayı En İyi Duruma Getirmeyi ofis saatlerinde çalıştırmanın avantajı.](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Artan performans

Planlamayı En İyi Duruma Getirme, uzun süreli master planları içeren senaryolarda kullanılabilir. Özellikle çok büyük miktarlarda veri içeren çok hızlı hesaplamalar için tasarlanmıştır. Aşırı ölçeklenebilir çok kiracılı bir hizmet olarak oluşturulduğundan birden fazla kurulum, planı hesaplamak için aynı anda birlikte çalışabilir. Ayrıca, planlama hizmeti sisteminizden master planlama yükünü kaldırır ve sunucu yükünü en aza indiren veri akışı ile çalışır.

Planlamayı En İyi Duruma Getirme aşağıdaki hedeflere ulaşmanıza yardımcı olabilir:

- Daha kısa çalışma zamanı üzerinden planlama performansını artırın.
- Master planlama çalışması sırasında diğer süreçler üzerindeki etkiyi azaltın.
- Daha sık planlama çalışmaları yapın. (Günlük çalışmalarla sınırlı değilsiniz.)
- Gelecekteki işletme büyümesinin planlama sistemine aşırı yükleme yapmayacağından emin olun.

## <a name="architecture-and-data-flow"></a>Mimari ve veri akışı

LCS'den Planlamayı En İyi Duruma Getirme Eklentisi yüklendiğinde Planlamayı En İyi Duruma Getirme hizmeti için güvenli bir bağlantı oluşturulur. Hizmet, ilgili Supply Chain Management kurulumu olarak aynı veri merkezi ülkesi veya bölgesinde bulunur. Planlamayı En İyi Duruma Getirme ayarlandıktan sonra master planlama çalıştırıldığında ana veriler ve hareket verileri Supply Chain Management'tan Planlamayı En İyi Duruma Getirme hizmetine gönderilir.

Planlamayı En İyi Duruma Getirme Eklentisi kaldırılırsa Planlamayı En İyi Duruma Getirme hizmetindeki ilgili tüm veriler kaldırılır.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Yeniden oluşturma çalışmaları için üst düzey veri akışı

1. Supply Chain Management istemcisi, Planlamayı En İyi Duruma Getirme hizmetinden bir planlama çalışması istemek için bir sinyal gönderir.
2. Planlamayı En İyi Duruma Getirme, tümleşik bağlayıcı aracılığıyla gerekli verileri ister.
3. SQL veritabanı, bağlayıcı aracılığıyla Planlamayı En İyi Duruma Getirme hizmetine ayar, ana veriler ve hareket verileri hakkında istenen bilgileri gönderir. Bağlayıcı, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasında bilgileri çevirir.
4. Planlamayı En İyi Duruma Getirme hizmeti, planlamayla ilgili verileri bellekte tutar ve gerekli hesaplamaları yapar.
5. Planlama sonucu, bağlayıcı aracılığıyla Supply Chain Management veritabanına gönderilir. Sonuçlar, planlı siparişler ve ilişkilendirme bilgileri gibi bilgiler içerir. Planlamayı En İyi Duruma Getirme hizmeti, planlama çalışmasının tamamlandığını belirletecek şekilde Supply Chain Management'a bir sinyal gönderir. Ayrıca ilgili tüm iletileri ve uyarıları da gönderir.

Aşağıdaki resimde, veri akışı gösterilmektedir.

![Yeniden oluşturma çalışmaları için veri akışı.](media/PlanningOptimization2.png)

## <a name="related-resources"></a>İlgili kaynaklar

[Planlama Optimizasyonunu kullanmaya başlama](get-started.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]