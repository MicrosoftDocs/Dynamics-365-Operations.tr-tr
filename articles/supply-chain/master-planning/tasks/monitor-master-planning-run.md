---
title: Master planlama çalışmasını izleme
description: Bu konu, üretim planlayıcısının bir master planlamanın devam edip etmediğini nasıl görebileceğini açıklar.
author: ChristianRytt
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1438ed6bcec485ff9665ffd9659c938f5cac478
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778143"
---
# <a name="monitor-a-master-planning-run"></a>Master planlama çalışmasını izleme

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Master planlama ilerlemesini görselleştirmek için Gantt şeması kullanma

**Master planlama ilerlemesini görüntüleme** sayfasından, geçmiş master planlama çalışmalarının ayrıntılarını Gantt şeması olarak görüntüleyebilirsiniz. Bu işlev, master planlamanın çeşitli aşamalarında harcanan zamanı anlamanıza yardımcı olabilir. Var olan bir etkin planlama işi için ilerlemeyi izlemek ve tahmini kalan süreyi görüntülemek üzere **Master planlama ilerlemesini görüntüleme** sayfası kullanılabilir.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>Master plan ilerlemesi görselleştirme özelliğini açma ve kullanma

Bu işlevi kullanmak için aşağıdaki adımları izleyin.

1. **Özellik yönetimi** çalışma alanındaki **Yeni** sekmesinde, listeden **Master planlama ilerlemesi görselleştirmesi**'ni seçin. Özellik, **Yeni** sekmesinde görünmüyorsa **Etkileştirilmemiş** ve **Tümü** sekmelerine bakın.
1. **Şimdi etkinleştir**'i seçin. Alternatif olarak, **Planla**'yı seçin ve ardından özelliğin açılmasını istediğiniz zamanı seçin. (Supply Chain Management sürüm 10.0.21 itibariyle, bu özellik varsayılan olarak açıktır.)

**Master planlama ilerlemesini görüntüleme** sayfası hem geçmiş planlama işlerini hem de etkin planlama işlerini görüntüleyebilir. 

Geçmiş planlama işlerini görüntülemek için iki seçenek vardır. 

1. **Master planlama \> Ayar \> Planlar \> Master planlar**'a gidin ve ardından Eylem Bölmesinde **Geçmiş**'i seçin. İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.
1. **Master planlama \> Çalışma alanları \> Master planlama**'ya gidin, Master planlama kutucuğunda **Geçmiş**'e tıklayın. İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.

Etkin planlama işlerini görüntülemek için iki seçenek vardır. 
1. **Master planlama \> Çalışma alanları \> Master planlama**'ya gidin, Eylem Bölmesinde **Bitirilmemiş planlama işlemi**'ni seçin. İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.
1. **Master planlama \> Çalışma alanları \> Master planlama**'ya gidin, Master planlama kutucuğunda **İlerlemeyi görüntüle**'ye tıklayın. İstediğiniz iş seçiliyken **Sorgular**'ı seçin ve ardından **İlerlemeyi görüntüle** seçeneğini belirleyin.

Etkin işleri yalnızca bir planlama işi işlenirken görüntüleyebileceğinizi unutmayın.

### <a name="analyze-a-master-planning-job"></a>Master planlama işini analiz etme

Gantt şemasında, harcanan zamanla ilgili ek ayrıntıları görüntülemek için aşağıdaki planlama süreçlerinin her birini genişletebilirsiniz:

- Başlatılıyor
- Veriler siliniyor ve ekleniyor
- Tedarik planlama
- Gecikmeler
- Eylem iletileri
- Sonlandırma
- Otomatik kesinleştirme

Eylem iletilerini kullanmanın etkisini görmek istiyorsanız Gantt şeması yararlı bir araçtır.

#### <a name="navigation-in-the-gantt-chart"></a>Gantt şemasında gezinme

- Seçilen grubu genişletmek ve ayrıntıları göstermek için ağaç görünümünde artı işaretini (**+**) seçin.
- Seçilen grubu daraltmak için ağaç görünümünde eksi işaretini (**–**) seçin.
- Gezinmek için klavyenizi kullanabilirsiniz. Satırlar arasında gezinmek için **Yukarı ok** ve **Aşağı ok** tuşlarını kullanın. Grupları genişletmek ve daraltmak için **Sağ ok** ve **Sol ok** tuşlarını kullanın.
- Gantt şemasındaki tüm düzeyleri açmak veya kapatmak için **Tümünü genişlet** veya **Tümünü daralt**'ı seçin.
- İlgili işleme süresini görüntülemek için bir görevin üzerine gelin. (Görevler, Gantt şemasındaki en düşük düzeydir.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>İşleri karşılaştırmak için ek bir master planlama çalışması görüntüleme

**Ek master planlama çalışması gösterme** alanında bir master planlama işi seçerek Gantt şemasında ek bir master planlama çalışmasını görüntüleyebilir ve iki işi karşılaştırabilirsiniz.

#### <a name="bom-level-display"></a>Ürün reçetesi düzeyinde görüntüleme

Ürün reçetesi (BOM) düzeyleri tedarik planlama, gecikmeler, eylemler ve kesinleştirme için farklı gösterilir.

- **Tedarik planlama**: Ürün reçetesi düzeyleri beklenen şekilde gösterilir. Yukarıdan aşağıya doğru hesaplanırlar.

    **Örnek:** Ürün reçetesi düzeyi 0, 1, 2

- **Gecikmeler**: Ürün reçetesi düzeyleri, tedarik planlama ürün reçetesi seviyeleri -1 ile çarpılarak gösterilir. (Başka bir deyişle, bunların negatif işareti vardır.)

    **Örnek:** Ürün reçetesi düzeyi –2, –1, 0

- **Eylem iletisi**: Ürün reçetesi düzeyleri beklenen şekilde gösterilir. Yukarıdan aşağıya doğru hesaplanırlar.

    **Örnek:** Ürün reçetesi düzeyi 0, 1, 2

- **Otomatik kesinleştirme**: Ürün reçetesi düzeyleri, 999 eksi tedarik planlama ürün reçetesi düzeyi olarak gösterilir.

    **Örnek:** Ürün reçetesi düzeyi 999, 998, 997

Aşağıdaki tablo, davranışı özetlemektedir.

| Gösterilen ürün reçetesi düzeyi | Son madde | Alt bileşen | Hammadde |
|---|---|---|---|
| Tedarik planlama | 0 | 1 | 2 |
| Gecikmeler | 0 | –1 | –2 |
| Eylem iletisi | 0 | 1 | 2 |
| Otomatik kesinleştirme | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>İlerlemeyi görselleştirme

Çalışmakta olan bir master planlama işini görüntülüyorsanız ilerleme, Gantt şemasında renklerle gösterilir. Mavi tema için aşağıdaki renkler geçerlidir. Diğer renk temaları için renkler farklı olacaktır.

- **Lacivert**: Tamamlanmış planlama görevleri.
- **Turuncu**: Şu anda devam eden görev.
- **Açık mavi**: Kalan görevler için tahmin.

Renk, Gantt şemasında yalnızca en düşük düzeyde gösterilir. Master planlama işindeki tüm görevleri görüntülemek için **Tümünü genişlet**'i seçin. Kalan görevlerin tahmini, geçmiş master planlama işlerini temel alır.

## <a name="run-master-planning-and-track-processing-time"></a>Master planlamayı çalıştırma ve işleme süresini izleme

1. Varsayılan panoda **Master planlama**'yı seçin.
1. **Plan** alanına bir değer girin veya bir değer seçin.
1. **Çalıştır**'ı seçin.
1. **İşleme izleme saati** seçeneğini **Evet** olarak ayarlayın.
1. **İş parçacığı sayısı** alanına bir rakam girin.
1. **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.
1. Kılavuzda, **Alan** alanının **Madde numarası** olarak ayarlandığı satırı seçin.
1. **Ölçütler** alanına bir değer girin.
1. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]