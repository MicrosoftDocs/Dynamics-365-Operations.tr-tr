---
title: "Yalın üretim için Kanban iş planlama"
description: "Bu makale, kanban iş planlamaları üzerinde görsel denetim sağlamak ve kanban işlerini planlamak için çeşitli yöntemler hakkında bilgi sağlar."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 27db57170ccc23c2ea18a49c1a3e5950c870fa13
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Yalın üretim için Kanban iş planlama

[!include[banner](../includes/banner.md)]


Bu makale, kanban iş planlamaları üzerinde görsel denetim sağlamak ve kanban işlerini planlamak için çeşitli yöntemler hakkında bilgi sağlar.  

**Kanban iş planlama çizelgeleme** sayfası yalın üretim iş hücreleri zamanlamaları üzerinde görsel denetim sağlar. Bu, tüm kanban işlerin özetini verir ve birden çok filtre olanakları sağlar. Bu sayfadan kanban yapılandırma ve yürütme ilgili diğer sayfalara taşıyabilirsiniz.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Kanban işleri otomatik zamanlama
**Otomatik planlama miktarı** parametresini kuralında ayarladıysanız, planlama otomatik olarak tetiklenebilir. **Otomatik planlama miktarını** **1** olarak ayarlarsanız, her kanban işi oluşturulduğunda planlanır. Sonuç bir dizi ilk çekene ilk hizmet işlemidir. **Otomatik planlama miktarı**'nı 1'den büyük bir değere ayarlarsanız, kanban işler planlanmadan önce gruplandırılır. 

Bu kavram kanban boyutları gerçek ekonomik toplu boyutlarına azaltılmasını sağlar. Örneğin, belirli bir madde (veya madde ailesi için) ekonomik toplu iş boyutu 30'dur. Ürün miktarı 30 kullanan kanbanlar oluşturmak yerine, kanban kuralını, bir 10 olan bir ürün miktarı ve **Otomatik planlama miktarı** **3** olacak şekilde yapılandırabilirsiniz. Otomatik planlama sadece üç planlanmamış iş varken iş hücresi için kanban işleri planlasa da, yürütme bekleyen iki planlanmamış iş olduğu planlayıcıya ve atölye gözetmenine tamamen saydamdır. Planlayıcı veya Atölye Yöneticisi daha sonra bu iki işleri el ile planlayarak veya ek kanban oluşturarak üretime alabilir.

## <a name="manual-scheduling"></a>El ile yapılan planlama
El ile planlama için Microsoft Dynamics AX 2012 kanban zamanlama tablosu kanban kullanılmaya başladı. El ile planlama, otomatik zamanlama ile birleştirilebilir. Kanban zamanlama tablosu işleri planlamanızı ve planları kaldırmanız, sırayla taşımanızı veya dönem dönem taşımanızı sağlar. İşler **otomatik planlama** değeri **0**'dan fazla olduğu kanban kuralının el ile planlanmamış olduğu kanban kuralına dayanır. Ancak sonraki otomatik planlama olay gerçekleştiğinde bu işler yeniden planlanır (Yeni kanban oluşturulduğunda). El ile zamanlama için aşağıdaki seçenekler kullanılabilir:

-   **Zamanlama** seçilen projelerin son tarihlerine göre zamanlar. (Bu seçenek, otomatik planlamaya benzer.)
-   **Başlangıç tarihinden ileriye zaman planlaması yapın** vade tarihlerine göre seçilen işleri zamanlamaya çalışır, ancak sonucu belirtilen en erken başlangıç tarihi kullanarak zorlar.
-   **Geriye doğru** seçili zamanlanmış işleri sırayla dönem içinde geriye taşır.
-   **İleriye doğru** seçili zamanlanmış işleri sırayla dönem içinde ileriye taşır.
-   **Önceki dönem** seçili zamanlanmış işleri önceki dönem başına veya sonuna taşır.
-   **Sonraki dönem** seçili zamanlanmış işleri sonraki dönem başına veya sonuna taşır.
-   **Plan** &gt; **iş durumunu geri al** , zamanlanmış bir işi zamanlamayı kaldırma sağlar.

## <a name="lean-scheduling-groups"></a>Yalın planlama grupları
Her renk yalın bir zamanlama grubunun temsil eder. Yalın zamanlama grupları serbestçe genel gruplar veya tek çalışma hücreye ait grupları olarak tanımlanabilir. Maddeleri ve boyutları serbestçe zamanlama gruplara atanabilir. Örneğin, bir boyama hücresinde ürünün renk zamanlama grubunun temsil edebilir. Belirli araç kullanımı gereksinimleri tarafından yönetilen iş, öğeler aracı gereksinime göre gruplandırılmış ve ambalaj iş hücre öğeleri ambalaj şablona göre gruplayabilirsiniz. Yalın zamanlama grupları renk kullanımı isteğe bağlıdır, ancak önerilir. Planın durumuna görünürlük sağlar. Örneğin, hangi gün hangi renklerin üretildiğini görmek çok kolaydır ve bu işin nasıl optimize edilebileceğini bir bakışta anlayabilirsiniz.

## <a name="work-cell-capacity-and-period-capacity"></a>İş hücresi kapasitesi ve dönem kapasitesi
Yalın iş hücre kapasitesi her zaman eşzamanlı kapasitedir. Diğer bir deyişle, birden fazla işi iş hücrede aynı anda etkin olabilir. Kapasite iki modda izlenebilir: işlem hacmi ve saat.

### <a name="throughput"></a>İş çıkarma yeteneği

İş hücre kapasitesi ortalama verimi miktarı bir başvuru dönemi (standart iş günü, haftası veya ayı) tarafından tanımlanır. Gerçek kapasite her gün veya hafta sonra iş hücreye atanan takvimin çalışma zamanlarına dayanarak hesaplanır. İş tarafından yüklenen kapasite iş hücresinde madde verimi oranı tarafından ayarlanan iş miktarıdır.

### <a name="hours"></a>Saat

Gün veya hafta olarak kullanılabilir kapasite iş hücresine atanan takvime göre tanımlanır. İş tarafından yüklenen kapasite iş hücresinde madde verimi oranı ve miktar (varsayılan faaliyet miktarı karşı gerçek iş miktarı) tarafından ayarlanan faaliyetin döngü zamanıdır.

#### <a name="period-capacity-factbox"></a>Dönem kapasitesi bilgi kutusu

**Kanban iş planlama çizelgeleme** listesi sayfası seçili iş hücre için kullanılabilir ve kitap haline getirilmiş dönem kapasite gösteren bir bilgi içerir. Üretim akışı modeli seçili zamanlama periyotlara bağlı olarak gün veya hafta dönemleri görüntüleyin.

<a name="see-also"></a>Ayrıca bkz.
--------




