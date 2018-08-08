---
title: "Master planlama ana sayfası"
description: "Master planlama, şirketlerin şirket hedeflerini karşılamak için gelecekteki hammadde ve kapasite gereksinimini belirlemesine ve planlamasına olanak tanır."
author: ShylaThompson
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ed011fa1c1aa35b4a401d51bffc6af19395577
ms.openlocfilehash: 030579ac73d6333ac4ed55433b9679a58247c088
ms.contentlocale: tr-tr
ms.lasthandoff: 02/13/2018

---

# <a name="master-planning-home-page"></a>Master planlama ana sayfası

[!include [banner](../includes/banner.md)]

Temel olarak master planlama, şirketlerin şirket hedeflerini karşılamak için gelecekteki hammadde ve kapasite gereksinimini belirlemesine ve planlamasına olanak tanır. Master planlama aşağıdakileri değerlendirir: 

-  Şu anda mevcut olan hammaddeler ve kapasiteler nelerdir? 
-  Üretimi tamamlamak için ne kadar hammadde ve kapasite gerekli? Örneğin, üretimi tamamlayabilmek için imal edilmesi, satın alınması, transfer edilmesi veya emniyet stoğu olarak ayrılması gerekenleri değerlendirir.

Master planlama gereksinimleri hesaplamak ve planlanmış siparişler oluşturmak için bilgileri kullanır.

Üç ana planlama işlemi vardır:

-  **Master planlama** - Master planlama net gereksinimleri hesaplar. Geçerli mevcut siparişleri temel alır ve şirketin stok yenilemeyi kısa vadeli olarak ve günlük bazda denetlemesini sağlar. Bunu tanımlamak *Net gereksinimler planlaması* terimi de kullanılır. Daha fazla bilgi için bkz. [Master planlama](master-plans.md). 

-  **Tahmin planlama** - Tahmin planı brüt gereksinimleri hesaplar. Gelecekteki tahminleri (veya tahminleri) temel alır ve şirketlerin malzemeleri ve kapasiteyi uzun vadeli planlamasına olanak tanır. Daha fazla bilgi için bkz. [Tahmin planlama](introduction-demand-forecasting.md). 

-  **Şirketlerarası master planlama** - Şirketlerarası master plan tüzel kişilikler arasındaki net gereksinimleri hesaplar. Talep ve tedariği şirketler arasında yalnızca kısa vadeli, kesin talep ve tedarik olarak değil aynı zamanda uzun vadeli, planlamış (henüz kesinleşmemiş) talep ve tedarik için bağlar. Daha fazla bilgi için bkz. [Şirketlerarası master planlama](https://mbspartner.microsoft.com/AX/CourseOverview/1276)  (e-Öğrenim) (CustomerSource hesabı gerektirir). 

Şirketler plan çıktısını değiştirebilir. Düzeltici, net değişiklik veya her ikisini çalıştırabilir. Düzeltici planlar tüm gereksinimleri güncelleştirirken net değişiklik planları, planı yalnızca son planlamadan bu yana ortaya çıkan yeni madde gereksinimleriyle güncelleştirir.

Master planlama planları genellikle bir hafta ile altı ay arasında olabilecek bir kısa vadeli dönemi içerir. Master planlama modülü, geçerli talebi karşılayacak olan tedarik (malzeme) ve kapasiteyi (kaynaklar) gereksinimlerini belirler (net gereksinimler). Çoğu şirkette, alınacak ürünler için en uzun kümülatif sağlama süresini içerecek şekilde genişletilir.

## <a name="learning-map"></a>Öğrenme haritası

Aşağıdaki öğrenme haritası, Master planlama modülünün çerçevesini oluşturan ana konseptleri ve görevleri gösterir. [Hızlı bağlantılar](#quick-links) bölümündeki bağlantılara tıklayarak modülün nasıl kullanılacağını öğrenin.

[![Master planlama için öğrenim haritası](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Hızlı bağlantılar

|      |   |
|------|---|
|        [Master planlar](master-plans.md)       |     [Kısıtlanmış plan oluşturma](./tasks/constrained-plan.md)  |
| [Ortak ürünler için malzeme planı oluşturma](./tasks/create-material-plan-co-products.md)   |  [Master planlama ve birden çok tesis işlevi](master-plan-multisite-functionality.md)  |
| [Şirketlerarası plan oluşturma](./tasks/create-intercompany-plan.md) | [Talep tahminine genel bakış](introduction-demand-forecasting.md)  | 
|[Azaltma anahtarları](reduction-keys.md)| [Master planlamanın temelleri](https://mbspartner.microsoft.com/AX/CourseOverview/1275) (e-Öğrenim) (CustomerSource hesabı gerektirir)     |
|  [İmalatı işlemek için master planlama](https://mbspartner.microsoft.com/D365E/CourseOverview/1514) (eLearning) (requires CustomerSource account) | [Şirketlerarası master planlama](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (e-Öğrenim) (CustomerSource hesabı gerektirir)|
                                  
## <a name="additional-resources"></a>Ek kaynaklar

### <a name="roadmaps"></a>Yol haritaları
Yayımlanmış ve geliştirilmekte olan yeni özellikleri görmek için [Microsoft Dynamics 365 Yol Haritası](https://roadmap.dynamics.com/) bölümüne gidin.

### <a name="blogs"></a>Bloglar
[Dynamics AX İmalat Ar-Ge Ekibi blogunda](https://blogs.msdn.microsoft.com/axmfg) ve [Dynamics AX'te Tedarik Zinciri Yönetimi Ar-Ge Ekibi blogunda](https://blogs.msdn.microsoft.com/dynamicsaxscm) Master planlama ve diğer çözümler hakkında pek çok fikir, haber ve bilgi bulabilirsiniz.

### <a name="task-guides"></a>Görev kılavuzları
Ek yardıma Finance and Operations içinde görev kılavuzları olarak ulaşılabilir. Görev kılavuzlarına erişmek için herhangi bir sayfada **Yardım** düğmesine tıklayın.

### <a name="webinars"></a>Web seminerleri
[Talep tahmini için Azure makine öğrenimi kullanma](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Teknik konferans kayıtları
-  [Talep tahmini işlevini genişletme](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
-  [Master planlama: Performans sorunlarını gidermek için ipuçları ve püf noktaları](https://youtu.be/7v8BPmEs9Dg)
-  [Yardım edin! MRP yavaş!](https://youtu.be/RLXybx20B5o)




