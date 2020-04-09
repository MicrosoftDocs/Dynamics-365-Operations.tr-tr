---
title: İş akışı geçmişini görüntüleme
description: Bu konuda işlenmesi ve onaylanması için iş akışı sistemine gönderilen bir belgenin durumunu görüntüleme adımları açıklanmaktadır.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd5b8d9f3fd2edab50b52a8345f254ebc6b31d0a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140410"
---
# <a name="view-workflow-history"></a>İş akışı geçmişini görüntüleme

[!include [banner](../../includes/banner.md)]

Bu konuda işlenmesi ve onaylanması için iş akışı sistemine gönderilen bir belgenin durumunu görüntüleme adımları açıklanmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.

1. **Gezinti bölmesi > Modüller > Ortak > Sorgular > İş akışı > İş akışı geçmişi**'ne gidin.
    - İşlenmek ve onaylanmak üzere iş akışı sistemine gönderilen bir belgenin durumunu görüntülemek için bu formu kullanın.  
    - **Örnek Kodu** belgeyi işleyen veya işlemiş olan iş akışı örneğinin kimlik kodudur.  
    - **Durum**, belgenin iş akışı durumudur.  
    - **İş Akışı Kodu**, belgeyi işleyen veya işlemiş olan iş akışının kimlik kodudur.  
    - **Belge**, belgenin kimlik kodudur.  
    - **Belge türü**, işlenmek üzere gönderilen belgenin türüdür.  
    - **İş akışı**, belgeyi işleyen veya işlemiş olan iş akışının adıdır.  
    - **Sürüm**, belgeyi işleyen veya işlemiş olan iş akışının sürüm numarasıdır.  
    - **Oluşturulma tarihi ve saati**, belgenin gönderildiği tarih ve saattir.  
    - **Geçen süre**, belgenin gönderilmesinden itibaren geçen süredir.  
    - **Sürdür** düğmesi, seçili belge için iş akışı işlemini devam ettirmenizi sağlar.  
    - **Geri çağır** düğmesi, seçili belgenin işlenmemesi için belgeyi geri çağırmanızı sağlar.   
2. Listede, istenen satırdaki bağlantıyı seçin.
    - **İş maddeleri** bölümünün genişletildiğinden emin olun. Bu bölümde, seçili belge ile ilişkili iş maddelerini görüntüleyebilirsiniz. Örneğin, bir görevin tamamlanması veya belgenin onaylanması gerekiyor olabilir.  
    - **Yeniden Ata** düğmesi, bir iş maddesini başka bir kullanıcıya yeniden atayabileceğiniz bir iletişim kutusu açar.  
    - **İzleme ayrıntıları** bölümünün genişletildiğinden emin olun. Bu bölümde, seçili belgenin iş akışı geçmişini görüntüleyebilirsiniz.  

