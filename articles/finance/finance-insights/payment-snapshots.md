---
title: Anlık görüntülere genel bakış
description: Bu konu, daha sonra analiz veya gerçek değerlerle karşılaştırma amacıyla nakit akışı tahminini kaydetmenize olanak sağlayan anlık görüntüler özelliğini açıklar. Nakit akışı tahmini oluşturduğunuzda, bu tahmini bir "anlık görüntü" olarak kaydedebilirsiniz. Bu anlık görüntüleri, tahmine dahil edilen hesapları düzenlemek için kullanabilir veya anlık görüntüdeki tahmini gerçek değerlerle karşılaştırabilirsiniz.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a91300ac17b36d890840e6c0c3104fad5fce68f0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752779"
---
# <a name="snapshots-overview"></a>Anlık görüntülere genel bakış

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

Gerçek mali sonuçları anlık görüntü olarak kaydedilmiş bir tahminle karşılaştırmak için **Gerçek değerlerle karşılaştır**'ı seçin. **Fiili değerlerle karşılaştır** sayfası, gerçek tutarların ve tahminin karşılaştırmasını gösterir. Sayfanın üst kısmındaki grafik, iki anlık görüntü arasındaki çakışan dönemde nakit girişleri, nakit akışları ve banka bakiyelerinin karşılaştırmasını gösterir. Alt bölümdeki ızgara, her likidite tutarı için döneme göre gerçek bakiyelerinin ve tahmini bakiyesinin ayrıntılı karşılaştırmasını gösterir. Izgaradaki **Fark** sütunu, bir dönemdeki gerçek bakiye ile tahmini bakiye arasındaki farkı gösterir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
