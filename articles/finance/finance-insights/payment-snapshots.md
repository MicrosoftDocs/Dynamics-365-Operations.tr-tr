---
title: Anlık görüntülere genel bakış (Önizleme)
description: Bu konu, daha sonra analiz veya gerçek değerlerle karşılaştırma amacıyla nakit akışı tahminini kaydetmenize olanak sağlayan anlık görüntüler özelliğini açıklar. Nakit akışı tahmini oluşturduğunuzda, bu tahmini bir "anlık görüntü" olarak kaydedebilirsiniz. Bu anlık görüntüleri, tahmine dahil edilen hesapları düzenlemek için kullanabilir veya anlık görüntüdeki tahmini gerçek değerlerle karşılaştırabilirsiniz.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a07749533e84cb26ce59b80e4bde12c96eaf0a3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009355"
---
# <a name="snapshots-overview-preview"></a>Anlık görüntülere genel bakış (Önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Anlık görüntüler, kuruluşların belirli bir anda nakit pozisyonlarına ve nakit tahminlerine ilişkin bilgileri düzenlemesine ve kaydetmesine olanak tanır. Anlık görüntüyü gerçek mali değerlerle karşılaştırabilir, farkı inceleyebilir ve zaman içinde nakit akışı tahminlerini iyileştirmek için bu bilgileri kullanabilirsiniz. Anlık görüntüler, özellikle aşağıdaki şekillerde kullanılabilir:

- Zaman içindeki nakit pozisyonunu ve nakit tahminlerini izleyin.
- Anlık görüntünün oluşturulduğu tüzel kişiliklerin alt kümesini göstermek için verileri filtreleyin.
- Sistem tarafından oluşturulan nakit pozisyonunu ve nakit tahminini düzenleyin.
- Nakit akışının iyimser, kötümser ve büyük olasılıkla gerçekleşebilecek görünümlerini dikkate almak için durum analizi yapın.
- Gerçek mali performansı, anlık görüntüde kaydedilen tahminlerle karşılaştırın.

**Nakit akışı tahminleri** çalışma alanındaki **Nakit pozisyonu** sekmesinde veya **Nakit tahmini** sekmesinde **Yeni anlık görüntü**'yü seçerek anlık görüntü oluşturabilirsiniz. Bir anlık görüntü oluşturulduktan sonra, girişler ve çıkışlar düzenlenebilir ve kaydedilebilir. Tüm kaydedilen anlık görüntüler **Anlık görüntüler** sekmesinde bulunabilir. Bir anlık görüntüyü açmak için, adını seçin.

Anlık görüntülerde nakit girişleri ve çıkışları herhangi bir zamanda düzenlenebilir. Bir giriş tutarı veya bir çıkış tutarı düzenlendiğinde, güncelleştirilmiş tutar orijinal bakiyeyi oluşturan likidite hesaplarına eşit olarak dağıtılır. Anlık görüntüyü düzenlemeyi bitirdiğinizde, **Kaydet**'i seçerek yaptığınız değişiklikleri kaydedin.

Birden fazla anlık görüntüyü karşılaştırmak için **Anlık görüntüleri karşılaştır**'ı seçin. Bir seferde iki anlık görüntüyü karşılaştırabilirsiniz. Karşılaştırılacak iki anlık görüntü seçin ve **Tamam**'ı seçin . **Anlık görüntüyü karşılaştır** sayfası seçilen anlık görüntülerin karşılaştırmasını gösterir. Sayfanın üst kısmındaki grafik, iki anlık görüntü arasındaki çakışan dönemde nakit girişleri, nakit akışları ve banka bakiyelerinin karşılaştırmasını gösterir. Alt bölümdeki ızgara, her likidite tutarıyla ilgili olarak iki tahminin ayrıntılı karşılaştırmasını gösterir. Izgaradaki **Fark** sütunu, bir dönemdeki bakiyeler arasındaki farkı gösterir.

Gerçek mali sonuçları anlık görüntü olarak kaydedilmiş bir tahminle karşılaştırmak için **Gerçek değerlerle karşılaştır**'ı seçin. **Anlık görüntüyü karşılaştır** sayfası, gerçek tutarların ve tahminin karşılaştırmasını gösterir. Sayfanın üst kısmındaki grafik, iki anlık görüntü arasındaki çakışan dönemde nakit girişleri, nakit akışları ve banka bakiyelerinin karşılaştırmasını gösterir. Alt bölümdeki ızgara, her likidite tutarı için döneme göre gerçek bakiyelerinin ve tahmini bakiyesinin ayrıntılı karşılaştırmasını gösterir. Izgaradaki **Fark** sütunu, bir dönemdeki gerçek bakiye ile tahmini bakiye arasındaki farkı gösterir.

#### <a name="privacy-notice"></a>Gizlilik bildirimi
Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]