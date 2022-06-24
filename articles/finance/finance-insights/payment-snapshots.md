---
title: Anlık görüntülere genel bakış
description: Bu makalede, daha sonra analiz veya gerçek değerlerle karşılaştırma amacıyla nakit akışı tahminini kaydetmenize olanak sağlayan anlık görüntüler özelliği açıklanmaktadır. Nakit akışı tahmini oluşturduğunuzda, bu tahmini bir "anlık görüntü" olarak kaydedebilirsiniz. Bu anlık görüntüleri, tahmine dahil edilen hesapları düzenlemek için kullanabilir veya anlık görüntüdeki tahmini gerçek değerlerle karşılaştırabilirsiniz.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 64f8aa3e932b4f8b6fdc5b239929216a11bfb377
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896506"
---
# <a name="snapshots-overview"></a>Anlık görüntülere genel bakış

[!include [banner](../includes/banner.md)]

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
