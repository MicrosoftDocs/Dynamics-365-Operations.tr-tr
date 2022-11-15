---
title: Dynamics 365 Human Resources altyapı birleştirme bilinen sorunlar
description: Bu makalede, Microsoft Dynamics 365 Human Resources altyapı birleştirme işlemi sırasında oluşabilecek sorunlar listelenmiştir.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752703"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources altyapı birleştirme bilinen sorunlar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Paylaşılan Dataverse ortamları

Çift Yazma çerçevesi, iki adet finans ve operasyonlar uygulama ortamını aynı Dataverse ortama bağlanmasını desteklemez. Aşağıdaki öğelerde paylaşılan bir Dataverse ortamına sahipseniz Dataverse ortamını yinelemeniz veya bölmeniz gerekir:

- Bir finans ve operasyon uygulaması
- Mevcut bir Human Resources ortamı

## <a name="environment-type-requirements"></a>Ortam türü gereksinimleri

Geçiş yapabilmeniz için önce aşağıdaki ortam tipleri gereklidir:

- Herhangi bir korumalı alan bağımsız ortamınız yoksa, geçişi doğrulamak için bir tane oluşturmanız gerekir.
- Çoklu üretim bağımsız ortamlarınız varsa, bunlardan biri geçirilebilir. Diğer ortamları korumalı alan olarak işaretlemek için Microsoft Desteği ile iletişime geçin.

## <a name="teams-integration"></a>Teams tümleştirmesi

Teams'teki mevcut Human Resources uygulaması şu anda Microsoft Power Platform çözümüne taşınıyor. Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](hr-admin-teams-leave-app.md).

