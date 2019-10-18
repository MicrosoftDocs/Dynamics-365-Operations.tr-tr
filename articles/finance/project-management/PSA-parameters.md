---
title: Project Service Automation tümleştirme parametreleri
description: Bu konu Microsoft Dynamics 365 for Project Service Automation ile Microsoft Dynamics 365 Finance tümleştirdiğinizde varsayılan verinin nasıl girileceğini açıklar.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7cef5384812e0dcb7d5e084ddd7668a7687a259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175068"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation tümleştirmesi parametreleri

[!include[banner](../includes/banner.md)]

**Project Service Automation tümleştirme parametreleri** sayfasında, varsayılan verinin Dynamics 365 Project Service Automation ile Dynamics 365 Finance tümleştirmesi yaptığınızda nasıl girildiğini yapılandırabilirsiniz. Projelerin Project Service Automation'dan Finance'a başarıyla eşitlenebilmesi için aşağıdaki alanları ayarlamanız gerekir.

> [!NOTE]
> - Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme sürüm 8.0 içinde kullanılabilir.
> - Fiili değerlerin tümleştirmesi sürüm 8.0.1 veya sonrasında kullanılabilir.


| Sekme                    | Alan                | Tanım |
|------------------------|----------------------|-------------|
| Genel                | Varsayılan proje türü | Varsayılan proje türünü seçin. Project Service Automation'dan projeler eşitlenirken tümleştirme şablonuna varsayılan bir değer girmediğinizde bu değer kullanılır. Eşitleme sırasında yeni projelerin **Proje türü** alanı bu değere ayarlanır. Ancak proje sözleşme satırları Project Service Automation'dan eşitlenirken bu değer güncelleştirilebilir. |
|                        | Süre kategorisi        | Varsayılan zaman kategorisini seçin. Saat tahminleri Project Service Automation'dan eşitlenirken bu değer kullanılır. Saat tahminleri ve saat gerçek değerleri Project Service Automation'dan eşitlenirken Finance'taki yeni proje saat tahminlerinin **Kategori** alanı bu değere ayarlanır. |
|                        | Ücret kategorisi         | Varsayılan ücret kategorisini seçin. Ücret gerçek değerleri Project Service Automation'dan eşitlenirken bu değer kullanılır. Ücret gerçek değerleri Project Service Automation'dan eşitlenirken Finance'taki yeni ücret hareketlerinin **Kategori** alanı bu değere ayarlanır. |
| Proje grubu varsayılanları | Proje türü         | Varsayılan proje grubunun ayarlanacağı proje türünü seçebileceğiniz bir satır eklemek için **Yeni**'ye tıklayın. Yapılandırmada belirli bir proje türü yalnızca bir kez seçilebilir. |
|                        | Proje Grubu        | Seçili proje türü için varsayılan proje grubunu seçin. Project Service Automation'dan yeni projeler eşitlenirken tümleştirme şablonunda varsayılan bir değer girmediğinizde **Proje grubu** alanı, proje türünün varsayılan değerine ayarlanır. |
| Faturalama türü varsayılanları  | Faturalama türü         | Varsayılan satır özelliğinin ayarlanacağı faturalama türünü seçebileceğiniz bir satır eklemek için **Yeni**'ye tıklayın. Yapılandırmada belirli bir faturalama türü yalnızca bir kez seçilebilir. |
|                        | Satır özelliği        | Seçili faturalama türü için varsayılan satır özelliğini seçin. Yeni saat tahminleri, yeni gider tahminleri veya yeni gerçek değerler Project Service Automation'dan eşitlenirken **Satır özelliği** alanı faturalama türü için varsayılan değere ayarlanır. |
| İşlev kilitleme  | Uygulanamaz       | Project Service Automation kaynaklı projeler ve sözleşmeler için Finance'ta devre dışı bırakılacak işlevselliği seçin. Örneğin, Finance'ta sözleşme ve proje düzenleme, iş kırılım yapıları oluşturma ve zaman çizelgeleri girme özelliklerini devre dışı bırakmayı seçebilirsiniz. Muhasebeyle ilgili alanlar parametre ayarıyla kullanılamaz yapılsa bile, etkin olmaya devam eder. Varsayılan olarak tüm işlevler etkindir. |
