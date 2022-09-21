---
title: Sensör Veri Yönetim Bilgileri giriş sayfası
description: Bu makale, Sensör Veri Yönetim Bilgileri'ne genel bir bakış sağlar. Kuruluşlar, üretim katındaki makine ve ekipmanlardan gelen Nesnelerin İnterneti (IoT) sinyallerini temel alarak Microsoft Dynamics 365 Supply Chain Management'ta iş süreçlerini yönlendirmek için bu özelliği kullanabilir.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e4cd8d4d4ffcd10d02fbf26615f12cdd6ccca9e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428446"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensör Veri Yönetim Bilgileri giriş sayfası

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management için Sensör Veri Yönetim Bilgileri, kuruluşların üretim katındaki makine ve ekipmanlardan gelen Nesnelerin İnterneti (IoT) sinyallerini temel alarak Supply Chain Management'ta iş süreçlerini yönlendirmesine olanak tanır. Daha önce Supply Chain Management için kullanılabilen *IoT Yönetim Bilgileri* özelliğinin güncelleştirilmiş, yeniden adlandırılmış bir sürümüdür.

Sensör Veri Yönetim Bilgileri aşağıdaki görevleri gerçekleştirmenize olanak sağlar:

- Supply Chain Management'ta bakım varlığı sayacı değerlerini güncelleştirmek ve tahmine dayalı bakım sunmak için makine ve ekipmanlardan ayrıntılar toplayın.
- Microsoft Dynamics Lifecycle Services'ta (LCS) bileşenleri el ile yüklemek ve yapılandırmak yerine basit bir ekleme sihirbazı kullanarak çözümü ayarlayın.
- Azure bileşenlerini yönetmek için daha fazla esnekliğe sahip olmak istiyorsanız bileşenleri kendi aboneliğinize dağıtın.
- Çözümü Azure bileşenlerinde çalışan iş mantığı olarak yapılandırın, ölçeklendirin ve genişletin. Bu bileşenler artık kendi aboneliğinizde yönetilmektedir. Bu nedenle, benzersiz iş gereksinimlerinizi karşılamak için bunları gerektiği gibi özelleştirebilirsiniz.

## <a name="business-scenarios"></a>İş senaryoları

Sensör Veri Yönetim Bilgileri, her biri sistemdeki belirli bir *senaryoyla* temsil edilen çeşitli işlevsellik türlerini etkinleştirir. Her senaryo, aşağıdaki tabloda ayrıntılı olarak açıklandığı gibi sistemde özel bir yapılandırma seçenekleri kümesi sağlar.

| Senaryo | Açıklama |
|---|---|
| [Varlık kesintisi](sdi-scenario-asset-downtime.md) | Makine çalışmama sürelerini izlemek için sensör verilerini kullanarak makine varlıklarının verimliliğini doğru bir şekilde izleyin. |
| [Varlık bakımı](sdi-scenario-asset-maintenance.md) | Makine varlıkları için kritik kontrol noktalarının sensör okumalarına dayalı bakım planlarını iyileştirerek bakım maliyetini en aza indirin ve varlık ömrünü uzatın. |
| [Makine durumu](sdi-scenario-equipment-downtime.md) | Planlayıcıları makine kesintileri hakkında bilgilendirmek ve olası gecikmeleri azaltmaya yönelik seçenekler sunmak için sensör okumalarını kullanarak çalışma verimliliğinden emin olun. |
| [Ürün kalitesi](sdi-scenario-product-quality.md) | Her bir ürün partisinin nem, sıcaklık veya özel olarak tanımlanmış kalite metrikleri gibi gerçek özellikleri için sensör okumalarını karşılaştırarak ürün partilerinin kalitesinden emin olun. Sistem, sapmalar meydana geldiğinde kullanıcıları bilgilendirecektir. |
| [Üretim gecikmeleri](sdi-scenario-production-delays.md) | Gerçek döngü süresini planlanan döngü süresiyle karşılaştırmak için sensör okumalarını kullanın ve üretim, zamanında yapılmadığında süpervizörleri bilgilendirin. Süpervizörler daha sonra maksimum operasyon verimliliğini sağlamak için gerektiğinde müdahale edebilirler. |

## <a name="architecture"></a>Mimari

Aşağıdaki mimari diyagram, çözüme ve bileşenlerine genel bir bakış sağlar.

![Sensör Veri Yönetim Bilgileri mimari diyagramı.](media/sdi-architecture.png "Sensör Veri Yönetim Bilgileri mimari diyagramı")
