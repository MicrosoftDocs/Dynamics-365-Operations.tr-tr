---
title: Project Service Automation
description: "Bu çözüm, Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation örnekleri arasında Common Data Service (CDS) üzerinden verileri eşitlemek için Veri Tümleştirme özelliğini kullanır."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Project Service Automation'dan Finance and Operations'a tümleştirme çözümü, Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation örnekleri arasında Common Data Service (CDS) üzerinden verileri eşitlemek için Veri Tümleştirme özelliğini kullanır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, projeler, proje sözleşmeleri, proje sözleşme satırları, proje sözleşme satırı kilometre taşları, proje görevleri, gider hareketi kategorileri, saat tahminleri ve gider tahminlerinin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.

> [!NOTE] 
> Dynamics 365 for Finance and Operations, Enterprise sürüm 7.3.0 kullanıyorsanız KB 4074835'i yüklemeniz gerekir. Bu, sabit fiyatlı projeleri tümleştirmenize olanak sağlar.
>
> Dynamics 365 for Finance and Operations sürüm 8.0 kullanıyorsanız, proje görevleri tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlev kilitlemeyi kullanabilirsiniz.
>
> Dynamics 365 for Finance and Operations sürüm 8.0.1 kullanıyorsanız gerçek değerleri eşitleyebilirsiniz.
>
> Dynamics 365 for Finance and Operations, Enterprise sürümü 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.

Project Service Automation'ı Finance and Operations'la tümleştirebilmeniz için Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir. Daha fazla bilgi için bkz: Project Service Automation tümleştirme parametreleri.

Bu tümleştirme çözümü aşağıdaki senaryolarda doğrudan eşitlemeyi etkinleştirir:

- Proje sözleşmelerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Project Service Automation'da projeler oluşturma ve bu projeleri Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Proje sözleşme satırlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Proje sözleşme satırı kilometre taşlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Proje görevlerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Gider hareketi kategorilerini Finance and Operations'ta yönetme ve Finance and Operations'tan Project Service Automation'a doğrudan eşitleme.
- Project Service Automation'da proje saat tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.
- Project Service Automation'da proje gider tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.

## <a name="data-synchronization"></a>Veri eşitleme
Aşağıdaki şekilde, Project Service Automation ile Finance and Operations arasında verilerin tümleştirmenin bir parçası olarak nasıl eşitlendiği gösterilmektedir.

> [!NOTE]
> Şu anda tüm şablonlar kullanımda değil. Şablonlar tamamlandıkça yayınlanacaktır.

[![Finance and Operations ile Project Service Automation tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations için sistem gereksinimleri

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü 7.3'ü platform güncelleştirmesi 12 veya daha ileri bir platform güncelleştirmesiyle birlikte yüklemeniz gerekir.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation için sistem gereksinimleri

Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

- Microsoft Dynamics 365 for Project Service Automation 9.0.0.0 veya daha ileri bir sürüm.
- Dynamics 365 for Sales için Aday müşteriden nakde çözümü, sürüm 1.14.0.0 (v14) veya sonrası.
- Dynamics 365 for Project Service Automation 1.0.0.0 veya daha ileri bir sürüm için Project Service Automation'dan Finance and Operations'a çözümü.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü Project Service Automation örneğinize yükleme



