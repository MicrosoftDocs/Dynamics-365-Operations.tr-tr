---
title: İş akışı SSS
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/01/2019
ms.locfileid: "773237"
---
# <a name="workflow-system"></a>İş akışı sistemi

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Finance and Operations içinde iş akışı sistemi hakkında sıkça sorulan soruları yanıtlar.

## <a name="notifications"></a>Bildirimler

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Bir iş öğesi reddedildiğinde neden birden fazla uyarı alınır?
Bir iş öğesi reddedildiğinde, bu iş maddesi reddedildi olarak tamamlanır. Başka bir iş öğesi oluşturulur ve başlatıcıya atanır. Bu, reddedilen iş öğesi için başlatan bir uyarı olacağı ve ayrı bir uyarının, yeni "değişim talebi" iş öğesine atanan kullanıcıya gönderileceği anlamına gelir. 

Her bir uyarı farklı bir iş öğesi içindir, ancak benzerlik karışıklığa neden olabilir. Gelecekteki bir sürümde bunu iyileştirmenin yollarını arıyoruz.
