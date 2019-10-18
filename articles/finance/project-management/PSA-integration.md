---
title: Project Service Automation'a genel bakış
description: Bu konu Dynamics 365 Project Service Automation ile Dynamics 365 Finance tümleştirme çözümü hakkında bilgi sağlar.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250565"
---
# <a name="project-service-automation-overview"></a>Project Service Automation'a genel bakış

[!include[banner](../includes/banner.md)]

Project Service Automation'tan Finance çözümüne tümleştirme, Veri tümleştirme özelliğini Dynamics 365 Finance ve Dynamics 365 Project Service Automation arasında eşitlemek için Common Data Service aracılığıyla kullanmaktadır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, projeler, proje sözleşmeleri, proje sözleşme satırları, proje sözleşme satırı kilometre taşları, proje görevleri, gider hareketi kategorileri, saat tahminleri ve gider tahminlerinin Project Service Automation'dan Finance'a akışına olanak tanır.

> [!NOTE]
> - Sürüm 7.3.0 kullanıyorsanız KB 4074835'i yüklemeniz gerekir. Yüklemeden sonra sabit fiyatlı projeleri tümleştirebilirsiniz.
> - Sürüm 7.3.0'ı kullanıyorsanız ve masraf hareketlerini Project Service Automation'dan çağırıyorsanız bu masrafları proje faturasına dahil etmek için KB 4345320'yi yüklemeniz gerekir.
> - Sürüm 8.0 kullanıyorsanız, proje görevleri tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlev kilitlemeyi kullanabilirsiniz.
> - Sürüm 8.0.1 kullanıyorsanız, fiili değerleri eşitleyebileceksiniz.

Project Service Automation'ı Finance'la tümleştirebilmeniz için Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir. Daha fazla bilgi için bkz. [Project Service Automation tümleştirme parametreleri](PSA-parameters.md).

Bu tümleştirme çözümü aşağıdaki senaryolarda doğrudan eşitlemeyi etkinleştirir:

- Proje sözleşmelerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.
- Project Service Automation'da projeler oluşturma ve bu projeleri Project Service Automation'dan Finance'a doğrudan eşitleme.
- Proje sözleşme satırları Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.
- Proje sözleşme satırı kilometre taşları Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.
- Proje görevlerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.
- Gider hareketi kategorilerini Finance'ta yönetme ve Finance'tan Project Service Automation'a doğrudan eşitleme.
- Project Service Automation'da proje saat tahminleri oluşturma ve bunları Project Service Automation'dan Finance'a doğrudan eşitleme.
- Project Service Automation'da proje gider tahminleri oluşturma ve bunları Project Service Automation'dan Finance'a doğrudan eşitleme.
- Finance'a nakledilebilmeleri için Project Service Automation'da proje süresi, gider ve ücret gerçek değerleri ile Project Service Automation tümleştirme günlüğünde proje hareketleri oluşturun.

## <a name="data-synchronization"></a>Veri eşitleme

Aşağıdaki şekilde, Project Service Automation ile Finance arasında verilerin tümleştirmenin bir parçası olarak nasıl eşitlendiği gösterilmektedir.

> [!NOTE]
> Şu anda tüm şablonlar kullanımda değil. Şablonlar tamamlandıkça yayınlanacaktır.

[![Project Service Automation ile Finance tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance için sistem gereksinimleri

Project Service Automation'dan Finance'a tümleştirme çözümünü kullanmak için , Enterprise edition 7.3'ü Platform güncelleştirmesi 12 veya daha ileri bir platform güncelleştirmesiyle birlikte yüklemeniz gerekir.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation için sistem gereksinimleri

Project Service Automation'dan Finance'a tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

- Dynamics 365 Project Service Automation sürüm 9.0.0.0 veya üstü
- Dynamics 365 Sales için Aday müşteriden nakde çözümü, sürüm 1.14.0.0 (v14) veya sonrası
- Project Service Automation'tan Finance'a çözümü, Dynamics 365 Project Service Automation sürüm 1.0.0.0 veya sonrası için

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation'dan Finance'a tümleştirme çözümünü Project Service Automation örneğinize yükleme

[Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016)'dan Project Service Automation'dan Finance'a tümleştirme çözümünü indirin ve çözümün içinde verilen yönergeleri izleyin.
