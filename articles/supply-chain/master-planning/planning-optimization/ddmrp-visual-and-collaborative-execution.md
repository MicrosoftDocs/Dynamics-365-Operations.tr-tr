---
title: Görsel ve işbirliğine dayalı yürütme
description: Bu makalede, Talep Temelli Malzeme Gereksinimi Planlaması ayırma noktalarınızı, arabellek bölgelerinizi, planlı siparişlerinizi ve geçmişinizi nasıl izleyeceğinizi açıklar.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: ce32a4449da8e85f958f212f2c2dfd2841ca6887
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740836"
---
# <a name="visual-and-collaborative-execution"></a>Görsel ve işbirliğine dayalı yürütme

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Bu makalede, Talep Temelli Malzeme Gereksinimi Planlaması ayırma noktalarınızı, arabellek bölgelerinizi, planlı siparişlerinizi ve geçmişinizi nasıl izleyeceğinizi açıklar.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Seçilen ürün için arabellekleri ve miktarları görsel olarak izleme

Microsoft Dynamics 365 Supply Chain Management'ta, seçilen herhangi bir serbest bırakılan ürün için arabelleklerin, eldeki miktarların ve net akış düzeylerinin zaman içinde nasıl değiştiğini görsel olarak izleyebilirsiniz. Grafikleri açmak ve incelemek için bu adımları izleyin.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Ayırma noktası olarak ayarlanan serbest bırakılmış bir öğeyi seçin. (Daha fazla bilgi için bkz. [Stok konumlandırma](ddmrp-inventory-positioning.md).)
1. Eylem Bölmesi'nin **Plan** sekmesinde **Öğe kapsamı**'nı seçin.
1. **Öğe kapsamı** sayfasında ayırma noktası oluşturan bir öğe kapsam kaydı seçin. (Bu kayıt, ayırma noktaları oluşturmak üzere ayarlanmış bir kapsam grubunun adını gösterir.)
1. **Eldeki** sekmesini seçin. Bu sekme, master planlama her çalıştırıldığında belirli bir süre için kaydedilen eldeki düzeyin değeriyle birlikte eldeki miktarların zaman içinde nasıl değiştiğini gösteren bir grafik içerir. Sekme ayrıca, kaydedilen her eldeki düzeyin aşağıdaki kategorilerden hangisine girdiğini gösteren bir tablo içerir:

    - **Kritik oranda düşük** – Dönem için minimumun yarısından daha az.
    - **Düşük** – Minimumun yarısı ile minimumun yarısı arasında.
    - **Eldeki ortalama** – Minimum ve minimum artı yeşil bölge arasında.
    - **Ortalamadan yüksek** – Ortalamadan yüksek.

    ![Eldeki sekmesindeki geçmiş eldeki seviyeler.](media/ddmrp-on-hand-graph.png "Eldeki sekmesindeki geçmiş eldeki seviyeler")

    > [!NOTE]
    > **Eldeki** sekmesinde kullanılan renkler, **Arabellek değerleri** sekmesinde kullanılan benzer renklerden farklı aralıkları temsil eder.

1. Arabellek değerlerinizin zaman içinde nasıl değiştiğini, eldeki ve net akış seviyeleriyle nasıl karşılaştırıldığını görmek için **Arabellek değerleri** sekmesini seçin.

    ![Arabellek değerleri sekmesinde geçmiş eldeki ve net akış düzeyleri.](media/ddmrp-buffer-values-graph.png "Arabellek değerleri sekmesinde geçmiş eldeki ve net akış düzeyleri")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Tüm ayırma noktaları için durumu ve planlanan siparişleri izleme

**Talep temelli MRP** çalışma alanı, ana performans göstergeleri (KPI'lar) ve ayrılma noktası ürünlerinizin ve ilgili planlı siparişlerin durumuna ilişkin genel bakışlarla birlikte çeşitli araçlar sağlar. Açmak için **Master planlama \> Çalışma alanları \> Talep temelli MRP**'ye gidin.

![Talep temelli MRP çalışma alanı.](media/ddmrp-workspace.png "Talep temelli MRP çalışma alanı")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Ayırma noktalarına ve planlı siparişlere genel bakış edinme

**Talep temelli MRP** çalışma alanına ek olarak Supply Chain Management, DDMRP kurulumunuz, ayırma noktaları ve planlanan siparişler hakkında bilgileri görüntüleyebileceğiniz birkaç sayfa sağlar. Bu sayfalardan bazıları, Eylem Bölmesi'nde arabellekleri yönetmenize, ana planlamayı çalıştırmanıza ve diğer ilgili görünümleri açmanıza olanak tanıyan kullanışlı düğmeler de sağlar.

- Net akış düzeyine göre ayırma noktası durumunu görüntülemek için, **Ana planlama \> Ana planlama \> DDMRP \> Net akışa göre ayırma noktası durumu**'na gidin.
- Eldeki stok düzeyine göre ayırma noktası durumunu görüntülemek için, **Ana planlama \> Ana planlama \> DDMRP \> Eldeki ayırma noktaları durumu**'na gidin.
- Ayırma noktaları için planlı siparişleri görüntülemek üzere **Master planlama \> Master planlama \> DDMRP \> Ayırma noktaları için planlı siparişler**'e gidin.
- Ayrılmış sağlama sürelerini görüntülemek için **Master planlama \> Master planlama \> DDMRP\> Ayrılmış sağlama süresi**'ne gidin.

## <a name="clean-up-decoupling-point-buffer-values"></a>Ayrılma noktası arabellek değerlerini temizleme

Zamanla, sisteminiz devam eden arabellek hesaplamalarıyla ilgili büyük miktarda geçmiş veri oluşturacaktır. Bu geçmiş veriler, veri hacminizin artmasına neden olacak ve sonunda sisteminizin performansını etkileyebilir. Bu nedenle, eski ayırma noktası arabellek değerlerini ara sıra temizlemenizi öneririz.

> [!WARNING]
> Temizleme işi, geçmiş arabellek değeri ayarlarını ve geçmiş eldeki/ağ akışı bilgilerini kaldıracaktır. Geri alınamaz.

Ayırma noktası arabellek değerlerinizi temizlemek için bu adımları izleyin.

1. **Master planlama \> Master planlama \> DDMRP \> Ayırma noktası arabellek değerlerini temizleyin**'e gidin.
1. **Ayırma noktası arabellek değerlerini temizleyin** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **(gün)den eski kayıtları sil** – Tutulacak en genç kayıtların yaşını gün olarak belirtin. Bu değerden daha eski olan tüm ayırma noktası arabellek değeri kayıtları silinecektir.
    - **Master plan** – Bu temizlemeden etkilenmesi gereken ürünleri içeren bir ana plan seçin. Temizleme, bu iletişim kutusunda belirttiğiniz **Filtre** ayarları uygulandıktan sonra plandaki tüm ürünlere uygulanacaktır.

1. Toplu işin çalıştırılması gereken kayıt kümesini sınırlamak için, **Dahil edilecek kayıtlar** hızlı sekmesinde, **Sorgu** iletişim kutusunu açmak için **Filtre**'yi seçin. Bu iletişim kutusu, Supply Chain Management'ta bulunan diğer [arka plan işlerinde](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) çalıştığı gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde, temizliğin nasıl, ne zaman ve ne sıklıkta yapılması gerektiğini belirtin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. Yürütme için yeni işi toplu iş kuyruğuna eklemek için **Tamam**'ı seçin.
