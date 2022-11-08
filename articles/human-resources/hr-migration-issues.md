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
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733484"
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

## <a name="licensing"></a>Lisans

Dynamics 365 Human Resources için aşağıdaki alanlarda lisansla ilgili herhangi bir değişiklik yoktur: 

- **Minimum lisans satın alma gereksinimi sayısı**
- **Üretim ortamı ve korumalı alan ortamı lisansları** – Mevcut bir bağımsız Human Resources kaynağınız bir adet üretim ortamı ve bir adet korumalı alan ortamı sağlıyorsa finans ve operasyonlar altyapısında da aynı sayıda lisansa sahip olursunuz.
- **Ek korumalı alan lisansları** – Bağımsız Human Resources uygulaması için ek korumalı alan lisansları satın aldıysanız korumalı alan ortamları için finans ve operasyonlar altyapısında aynı sayıda lisansları kullanılabilir. 
