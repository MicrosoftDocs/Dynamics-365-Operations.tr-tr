---
title: Yalın imalat için görsel planlama
description: Bu makale, üretim planlayıcısının kanban işleri için üretim planını denetlemek ve en iyi duruma getirmek üzere kullanabileceği Kanban zamanlama panosu hakkında bilgiler sağlar.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a743be96867c1f325e6fe01f23355c27cb4d0cc0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875202"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Yalın imalat için görsel planlama

[!include [banner](../includes/banner.md)]

Bu makale, üretim planlayıcısının kanban işleri için üretim planını denetlemek ve en iyi duruma getirmek üzere kullanabileceği Kanban zamanlama panosu hakkında bilgiler sağlar.

Bu makale, üretim planlayıcısının kanban işleri için üretim planını denetlemek ve en iyi duruma getirmek üzere kullanabileceği Kanban zamanlama panosu hakkında bilgiler sağlar.

Kanban zamanlama panosu üretim planlayıcıya üretim planını kanban işleri için denetleme ve en iyi duruma getirme olanağı sunar. Kanban iş akışını şeffaf hale getirir ve üretim planlayıcısına yalın imalat iş hücresi için üretim planını en iyi duruma getiren ve düzenleyen bir araç sunar.

## <a name="visual-scheduling-of-kanban-jobs"></a>Kanban işlerini görsel zamanlama
kanban işi bir veya daha fazla kanban işinden oluşabilir. İki tür kanban işi vardır:

-   İşlem
-   Transfer et

Yalnızca **İşlem** türündeki işleri planlayabilirsiniz. Kanban işi ve faaliyet süresi gibi özellikleri üretim kanban akışında tanımlanır. Üretim kanban akışında kanban işi iş hücresine de atanır. İş hücresinin günlük kapasitesi kaynak grubunda ayarlanan iş hücresi kapasitesine göre hesaplanır. İlgili takvimdeki günlük çalışma süresine göre düzeltilir. Bir kanban işi planlandığında, iş iş hücresinin kapasitesini yükler. Kanban planlama panosu aşağıdaki ana özellikleri sağlar:

-   Yalın iş hücresindeki üretim planının grafik özeti. Bu genel bakış tanımlanan dönemlerdeki planlanan kanban işleme işlerini gösterir.
-   Bir araç planlanmamış kanban işlerini planlamanızı ve daha önce planlanan işleri yeniden planlamanızı sağlar.

## <a name="kanban-schedule-board"></a>Kanban zamanlama panosu
**Kanban planlama panosu** sayfası aşağıda gösterildiği gibi yedi ana öğe içerir. 

![Kanban planlama panosu.](./media/kanban-schedule-board-1024x554.png)
1.  Eylem Bölmesi
2.  Filtre alanları
3.  Planlanmamış işler için düğme
4.  Dönem düğümü
5.  Kanban işi
6.  Kapasite çubuğu
7.  Zaman çizelgesi

### <a name="view-the-time-scale"></a>Zaman çizelgesini görüntüleme

Pano, her biri düğüm olarak temsil edilen (4) dönemlere bölünmüştür. Dönem düğümleri dikey eksende listelenir ve yatay eksen dönem uzunluğunu gösteren bir zaman çizelgesini (7) temsil eder. Bir dönemin uzunluğu bir gün veya bir haftadır. Dönem uzunluğu Kanban planlama panosu (2) için seçilen iş hücresinin yapılandırmasıyla belirlenir. Her dönem düğümü için Kanban planlama panosu planlanan kanban işlerinin dönemi ne kadar doldurduğunu belirtir. Ayrıca dönem için maksimum üretim değeri göstergesi de vardır. Planlanan üretim değeri maksimum üretim değerini aşarsa, dönem aşırı yüklü olarak kabul edilir ve kırmızı bir uyarı simgesi görüntülenir. Planlanan kanban işi planlanmış başlangıç ve bitiş tarihleri (5) olan bir dönemde görüntülenir. İşin uzunluğu faaliyet süresine eşittir. Kanban işleri, faaliyet zamanları iş hücresindeki görev süresini aşarsa dönem içinde çakışıyor olarak görünür.

### <a name="view-job-status"></a>İş durumunu görüntüleme

Bir kanban işiyle ilgili daha fazla bilgi fare imlecini işin üzerine getirdiğinizde görüntülenen araç ipucunda bulunur. Bir simge işin durumu hakkında bilgi sağlar. Örneğin, bir saat simgesi kanban iş süresinin geçmiş olduğunu gösterir.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Kanban planlama panosunu görüntülemek için renkleri kullanma

Kanban planlama panosunun sağladığı genel görünümü geliştirmek için kanban işlerini birbirinden ayırmak üzere renkleri kullanabilirsiniz. Kanban işi rengi, aynı seride üretilmesi gereken ürünleri toplayabileceğiniz yalın planlama grubunda yapılandırılır. Eylem Bölmesinin **Pano** sekmesindeki **Tema renklerini kullan** düğmesi uygulama tema renkleri ile yalın planlama grubunda yapılandırılan renkler arasında geçiş yapmanızı sağlar. Her dönem için, bir kapasite çubuğu (6) döneme ait ne kadar kullanılabilir saatin kanban işleriyle doldurulduğunu gösterir. Dönem aşırı yüklüyse, kapasite çubuğu daha kalın ve kırmızı renkte gösterilir. Tüm bu işlevler **Kanban planlama panosu** sayfasının üst kısmındaki Eylem Bölmesinde (1) yer alan **Pano** sekmesinde bulunur.

## <a name="plan-unplanned-jobs"></a>Planlanmamış işleri planla
Planlanmamış kanban işlerini **Planlanmamış iş planlama** iletişim kutusundan planlayabilirsiniz. Bu iletişim kutusunu açmak için geçerli planlanmamış iş sayısını gösteren **Planlanmamış işler** düğmesine tıklayın. Alternatif olarak, Eylem Panosundaki **Pano** sekmesinde bulunan **Planlanmamış iş planlama**'yı tıklayın. İletişim kutusu iş hücresi için planlanmamış kanban işlerinin listesini gösterir. Izgaradaki tüm alanları filtrelemek için **Filtre** alanını kullanabilirsiniz. Örneğin, belirli bir ürün için kanban işlerini filtreleyebilirsiniz. Planlamak istediğiniz işlerin listesini filtreledikten sonra, bunları listeden seçin ve **Tamam**'ı tıklayın. İşleri planlamak için otomatik planlama kullanmak üzere **Otomatik planlama** seçeneğini **Evet** olarak ayarlayın. Bu durumda, işler vade tarihlerine göre bir dönem içinde planlanır. İşleri döneme göre de planlayabilirsiniz. **Dönem** alanında bir dönem seçmeniz yeterlidir. Aşağıdaki örnekte **Planlanmamış iş planlama** iletişim kutusu örneği gösterilmektedir. 

![Planlanmamış işleri planla iletişim kutusu.](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Aynı dönem içindeki kanban işleri serisi
Dönem içindeki seçilen bir veya daha fazla işin serisini değiştirebilirsiniz. Bu özellik, dönem içindeki bazı işlere öncelik vermek istediğinizde yararlı olabilir. Alternatif olarak, yürütme işlemini en iyi duruma getirmek için aynı ürün özniteliklerine sahip işler için seri düzenlemek isteyebilirsiniz. Seriyi sürükle ve bırak işlemiyle veya Eylem Bölmesindeki **Pano** sekmesinde bulunan **Geri** ve **İleri** menü öğelerini kullanarak değiştirebilirsiniz. 

## <a name="reassign-kanban-jobs-across-periods"></a>Kanban işlerini dönemler arasında yeniden atama
İşleri bir dönemden başka bir döneme atanabilir. Bu özellik bir dönemin aşırı yüklü olması ve boş kapasitesi olan dönemlerde yükü dengelemek istediğinizde yararlı olabilir. İşleri sürükle ve bırak işlemiyle veya Eylem Bölmesindeki **Pano** sekmesinde bulunan **Sonraki dönem** ve **Önceki dönem** menü öğelerini kullanarak yeniden atayabilirsiniz.

## <a name="open-the-kanban-schedule-board"></a>Kanban planlama panosunu açma
Kanban planlama panosunu aşağıdaki sayfalarda yer alan menü öğesini kullanarak açabilirsiniz:

-   **Üretim alanı** sayfası
-   **Kanban işleri planlaması** sayfası
-   **Üretim akışı görselleştirme** sayfası


## <a name="additional-resources"></a>Ek kaynaklar

[Yalın imalat için kanban iş planlama](lean-manufacturing-kanban-job-scheduling.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]