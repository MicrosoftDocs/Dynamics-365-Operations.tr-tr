---
title: "Operasyon planlama çizelgeleme"
description: "Bu konu operasyon planlaması hakkındaki bilgileri sağlar. Operasyon planlama çizelgelemesini zaman içinde üretim süresine dair genel bir tahmin yapmak için kullanabilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 958f5514f4c79b2521d709c6051c2997162d5475
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="operations-scheduling"></a>Operasyon planlama çizelgeleme

[!include[banner](../includes/banner.md)]


Bu konu operasyon planlaması hakkındaki bilgileri sağlar. Operasyon planlama çizelgelemesini zaman içinde üretim süresine dair genel bir tahmin yapmak için kullanabilirsiniz.

Üretimi operasyon düzeyinde ve iş düzeyinde planlayabilirsiniz. İş planlamadan farklı olarak, operasyon planlama üretim rotasının operasyonlarını işlere ayırmaz. Planlamaya geçerli kapasite hakkında bilgiler gibi daha fazla ayrıntı eklemek isterseniz iş planlamayı operasyon planlamadan sonra çalıştırabilirsiniz. Yalnızca iş planlamayı da çalıştırabilirsiniz. İş planlama genellikle atölyedeki tek tek işleri anlık veya kısa bir zaman aralığında planlamak için kullanılır.

## <a name="components-of-operations-scheduling"></a>Operasyon planlamasının bileşenleri
Operasyon planlamasının ana bileşenleri planlama yönü, kaynak kapasitesi ve malzemeye göre üretimdir. Operasyon planlamasını kullanarak aşağıdaki hedeflere ulaşabilirsiniz:

-   Belirli bir tarihten ileriye veya geriye doğru planlama yaparak planlama yöntemini denetleyin.
-   Üretimleri kaynakların kapasitesine göre planlayarak kaynak kullanımını en iyi duruma getirin. Bu yaklaşım alternatif kaynakların kullanılması gereken zamanların belirlenmesine de yardımcı olur.
-   Üretimleri gerekli malzemelerin kullanılabilirliğine göre planlayarak malzeme kullanımını en iyi duruma getirin.
-   Referans üretimleri planlayın ve eşitleyin. Üretim emrinin planlaması değiştirildiğinde referans üretimlerin tarihleri ayarlanır.

Operasyon planlamasını çalıştırabilmek için bir üretim emrinin maliyetini tahmin etmeniz gerekir. Tahmin çalıştırmadıysanız operasyon planlaması başlatılmadan önce otomatik olarak çalıştırılır. Operasyon planında aşağıdaki bilgiler belirtilir:

-   Üretim için planlanan ürün
-   Ürünün yapılandırması
-   Üretimde söz konusu miktarlar
-   Üretimin başlangıç ve bitiş tarihleri
-   Üretim faaliyetlerini gerçekleştiren kaynakların kapasite rezervasyonları

Üretimdeki operasyonların hazırlık süresi, işlem süresi ve çalışma süresi. Operasyon planlamasını çalıştırdıktan sonra, üretim emrinin durumu **Planlandı** olur ve tüm operasyonlar üretim rotası ile belirtilen sırayla planlanır. Ancak yalnızca operasyonun süresi dikkate alınır. Başlangıç saati ve bitiş saati planlanmaz.

## <a name="scheduling-direction-and-date"></a>Yön ve tarihi planlama
Planlama yönü, planlama süreci bakımından temel niteliğindedir. Üretim, zamanlama ve planlama gereksinimlerine bağlı olarak herhangi bir tarihten geriye veya ileriye doğru planlanabilir.

-   **Planlama tarihinden ileriye doğru** – Üretimi olabildiğince erken başlatmak için planlayabilirsiniz. Üretim bugün, yarın veya gelecekteki herhangi bir tarihte başlatılabilir. Üretim mümkün olan en erken tarihte bitecek şekilde ileriye doğru planlanır.
-   **Planlama tarihinden geriye doğru** – Üretimi olabildiğince geç başlatmak için planlayabilirsiniz. Geriye doğru planlama üretimin tamamlanması gereken tarihi temel alır. Planlama bu tarihten, üretimin başlatılıp zamanında tamamlanabileceği, mümkün olan en geç tarih için geriye doğru sayar.

## <a name="resource-scheduling"></a>Kaynak zamanlama
Operasyon planlaması çalıştırdığınızda, üretim rotasındaki tüm operasyonlar, operasyon için belirtilen kaynak için planlanır. Ayrıca her operasyonun süresi üretim rotasında belirtilir. Operasyon için bir kaynak grubu belirtildiyse planlama gruptaki kapasiteyi rezerve eder. Ancak iş planlamadan farklı olarak, operasyon planlama gruptaki belirli kaynakları seçmez. Sınırlı kapasite ile çalışıyorsanız, planlama, üretimin tamamlanması için gereken kaynakların kullanılabilirliğine bağlıdır. Operasyon planlaması üretim rotasında belirtilen operasyonların sırasını izler. Planlama, kaynak gruplarındaki kapasiteyi üretim rotasında tanımlanan işlem sürelerini temel alarak rezerve eder. Söz konusu kaynakların kullanılabilir kapasitesinin toplamı, kaynak grubun kapasitesini belirler. Kaynaklar için zaten var olan kapasite rezervasyonları kullanılamayan kapasite olarak kabul edilir. Üretim için yeterli kullanılabilir kapasite yoksa üretim emirleri gecikebilir ve hatta durdurulabilir. Ayrıca üretime dahil edilen kaynaklardan beklediğiniz verimliliği de belirtebilirsiniz. Verimliliği kaynak üzerinden bir yüzde olarak belirtin. Verimlilik yüzdesi kaynağın iş çıkarma yeteneğini ayarlar. Bu ayarlama, kaynak için ayrılan süreyi etkiler. Kaynağı kullanan operasyonların sağlama süreleri de buna göre ayarlanır.

## <a name="operations-scheduling-and-master-planning"></a>Operasyon planlama ve master planlama
Operasyon planlama master planlamayı da destekler ve malzeme gereksinimi hesaplamalarını belirler. Operasyon planlama aşağıdaki bilgileri hesaba katar:

-   **Bekleme listesine alınan üretimler** – Planlanan, serbest bırakılan veya başlatılan ürünler
-   **Malzeme kullanılabilirliği** – Stok, alt üretimler, tedarikçiler ve satıcılar
-   **Kapasite kullanılabilirliği** – Üretim için gerekli olan kaynaklar

## <a name="cancellations"></a>İptaller
Operasyon planlamasını çalıştırdığınızda, rotanın belirli kısımlarını iptal edebilirsiniz. Bu kısımlar kuyruk süresi, hazırlık süresi, işlem süresi, çakışma süresi ve taşıma süresi olabilir.

## <a name="finite-materials"></a>Sonlu malzemeler
Sınırlı malzemeyle çalışıyorsanız planlama üretim için gerekli olan malzemelerin kullanılabilirliğine de bağlıdır. Üretim için yeterli kullanılabilir bileşen yoksa üretim ertelenebilir. Planlamada üretim için kullanılabilir olması gereken malzemeleri belirterek malzeme kullanımını temel alabilirsiniz. Kaynak kapasitesini ve malzemelerin kullanılabilirliğini en iyi duruma getirdiğinizde, üretim bu sınırlamalara göre hesaplanır. Üretim emri, kapasite ve malzemeler aynı anda ve gerekli miktarlarda kullanılabilir olduğu anda başlatılacak şekilde planlanabilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Operasyon planlama çizelgeleme seçenekleri](operation-scheduling-options.md)



