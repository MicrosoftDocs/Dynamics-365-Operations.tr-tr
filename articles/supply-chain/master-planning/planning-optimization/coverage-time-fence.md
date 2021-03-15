---
title: Kapsam zaman dilimleri
description: Bu konuda, Planlamayı En İyi Duruma Getirme'yi kullanırken kapsam zaman dilimlerinin nasıl ayarlanacağı açıklanmaktadır. Kapsam zaman dilimi, planlama ufkunuzu ve sınırınızı belirtir.
author: ChristianRytt
manager: tfehr
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f970d7aa9f758d3bc35b7a1b9d1e43be928fd250
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033236"
---
# <a name="coverage-time-fences"></a>Kapsam zaman dilimleri

Bu konuda, Planlamayı En İyi Duruma Getirme'yi kullanırken *kapsam zaman dilimlerinin* nasıl ayarlanacağı açıklanmaktadır. Planlayıcılar, planlama ufkunu (gün olarak karşılama zaman dilimi) tanımlayabilir ve bu dönemin dışında kalan tedariki ve talebi hariç tutabilir. Bu sayede, kapsam zaman dilimleri, aylarca tepki vermenizi gerektirmeyen tedarik önerilerinin neden olduğu "gürültü"nün önlenmesine yardımcı olur. Örnekler arasında, gelecek yılın tahmini ve normal sağlama süresinin dışında verilen müşteri siparişleri yer alır.

Kapsam zaman dilimi, bugünün tarihinden (veya planlama çalıştırmasını yaptığınız tarihten) sonra tedarik ve talebin hariç tutulduğu gün sayısıdır. Gecikmeleri önlemek için kapsam zaman diliminin, toplam sağlama süresinden uzun olduğundan emin olmalısınız. Varsayılan sistem değeri 100 gündür.

Aşağıdaki düzeylerin her biri için bir kapsam zaman dilimi belirtebilirsiniz:

- **Kapsam grubu**: Her kapsam grubu için varsayılan bir kapsam zaman dilimi ayarlayabilirsiniz.
- **Madde kapsamı**: Bir maddeye atanan kapsam grubundan devralınmış kapsam zaman dilimini geçersiz kılabilirsiniz.
- **Master plan**: Kapsam grubundan ve madde kapsamı ayarlarından devralınmış kapsam zaman dilimlerini geçersiz kılabilirsiniz.

Aşağıdaki bölümlerde, her düzeyde bir kapsam grubunun nasıl belirtileceği açıklanmaktadır.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Kapsam grubu için kapsam zaman dilimi ayarlama

Kapsam grubu için bir kapsam zaman dilimi belirttiğinizde, bu ayar söz konusu gruba ait olan tüm maddelere (ürünler) uygulanır. Ancak, belirli maddeler veya belirli master planlar için ayarı geçersiz kılabilirsiniz.

Kapsam grubuyla ilgili bir kapsam zaman dilimi belirtmek için, aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Kapsam \> Kapsam grupları**'na gidin.
1. Listeden mevcut bir kapsam grubu seçin veya yeni bir kapsam grubu oluşturun.
1. **Genel** hızlı sekmesinde, **Kapsam zaman dilimi (gün)** alanını kapsam grubu için kapsam zaman dilimi olarak kullanmak istediğiniz gün sayısına ayarlayın.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Belirli bir madde için kapsam zaman dilimi ayarlama

Her madde (ürün) bir kapsam grubuna aittir. Bir maddeye özel bir kapsam grubu atanmamışsa, varsayılan bir kapsam grubu uygulanır. Her madde, kapsam grubundan bir kapsam zaman dilimini devralır. Ancak, bu zaman dilimini, gerektiğinde belirli maddeler için geçersiz kılabilirsiniz.

Belirli bir maddeyle ilgili bir kapsam zaman dilimi belirtmek için, aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Izgarada bir ürün seçin.
1. Eylem Bölmesindeki **Plan** sekmesinde yer alan **Kapsam** grubunda **Madde kapsamı**'nı seçin.
1. **Madde kapsamı** sayfasındaki **Genel bakış** sekmesinde kapsam zaman dilimini ayarlamak istediğiniz sahanın satırını seçin veya oluşturun.
1. Seçili sahanın ayarlarını açmak için **Genel** sekmesini seçin.
1. **Kapsam grubu ayarlarını geçersiz kıl** onay kutusunu seçin.
1. **Kapsam zaman dilimi (gün)** alanını madde için kapsam zaman dilimi olarak kullanmak istediğiniz gün sayısına ayarlayın.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Master plan için kapsam zaman dilimi ayarlama

Master plan düzeyinde kapsam zaman dilimi belirtebilirsiniz: Bu şekilde, master planlama hesaplamasının bir master plan için kapsadığı gün sayısını tanımlarsınız. Bu ayar, her ilgili madde ve kapsam grubu için tanımlanan tüm kapsam süresi ayarlarını geçersiz kılar.

Belirli bir master plan ile ilgili bir kapsam zaman dilimi belirtmek için, aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Listedeki mevcut master planlardan birini seçin veya yeni bir master plan oluşturun.
1. **Gün cinsinden zaman dilimleri** hızlı sekmesinde, **Kapsam** seçeneğini *Evet* olarak ayarlayın. Ardından, seçeneğin altındaki alanda master plan için kapsam zaman dilimi olarak kullanmak istediğiniz gün sayısını girin.

## <a name="considerations-for-coverage-time-fences"></a>Kapsam zaman dilimleriyle ilgili dikkat edilmesi gereken noktalar

Kapsam zaman dilimleri ayarlanırken, aşağıdaki noktaları göz önünde bulundurun:

- Kapsam zaman dilimleri master planlamaya ait giriş verilerini etkiler. Gecikmeler oluşursa, sonuçta elde edilen planlı siparişlerin tarihi, kapsam zaman diliminin dahil edildiği bugünün tarihinden sonraki bir tarih olabilir.
- Kapsam zaman dilimleri takvim günleri olarak belirtilir. Çalışma günlerini kullanan takvimler zaman dilimi hesaplamasını etkilemez. Örneğin hafta sonları çalışma zamanı takviminde kapalı günler olarak ayarlanmış olsa bile bir hafta her zaman yedi gün kabul edilir.
- Kapsam zaman diliminin dışında kalan tedarik ve talepler için gereksinim hareketleri oluşturulmaz.
- Herhangi bir onaylı tedarik ve talep kapsam zaman diliminin dışında kalırsa altyapıya yüklenmez. Bu nedenle, stok yenileme tetiklenmez ve gecikmeler hesaplanmaz. Bununla birlikte, bu tedarik ve talep sistemden temizlenmemelidir.
- Güvenlik stoku miktarlarındaki (minimum anahtarlardan) değişimler, kapsam zaman diliminin dışında kalmaları durumunda yoksayılır.
- Hesaplanan talep edilen sevk tarihi kapsam zaman diliminin içinde değilse, şirketlerarası talep yok sayılır. Yerleşik master planlama için şirketlerarası talebin kapsam zaman dilimi ile sınırlı olmadığını unutmayın.
- Bütçe tarihi kapsam zaman diliminin içinde değilse talep tahminleri yoksayılır. Yerleşik talep tahminleri için şirketlerarası talebin kapsam zaman dilimi ile sınırlı olmadığını unutmayın.
- Planlamayı En İyi Duruma Getirme saat dilimine duyarlıdır. Tedarik ve talep sahalarındaki saat dilimini ve planlamanın çalıştırıldığı saati dikkate alır. Örneğin, master planlamanın Danimarka'daki bir sahadan 15 Ekim 11:00'da (GMT+1 saat dilimi) tetiklendiğini ve on günlük kapsam zaman diliminin kullanıldığını varsayalım. Bu durumda, Seattle'daki (GMT-8 zaman dilimi)bir sahadan tetiklenen tedarik ve talep, 25 Ekim 02:00'a kadar dahil edilir (= ana planlamanın tetiklenmesinin ardından on 24 saatlik gün sonra eksi dokuz saatlik zaman dilimi farkı). Yerleşik master planlama altyapısının yalnızca zaman diliminin tarihini dikkate aldığını unutmayın. Bu nedenle sonuç farklı olabilir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]