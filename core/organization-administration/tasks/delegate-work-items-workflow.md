--- 
title: "İş akışındaki iş öğelerini devretme"
description: "Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 30415b28166d5551f43da04a28b0a5194323f2ab
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="delegate-work-items-in-a-workflow"></a>İş akışındaki iş öğelerini devretme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz. Bu yordam, iş öğelerinizi otomatik olarak bir başka kullanıcıya devretmeniz için sistemi yapılandırmanıza yardımcı olur.



Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="set-up-automatic-delegation"></a>Otomatik temsil ayarlama
1. Ortak > Kurulum > Kullanıcı seçenekleri'ne gidin.
2. İş Akışı sekmesine tıklayın.
    * Temsilci bölümünün genişletilmiş olduğundan emin olun.    Diğer kullanıcılar iş maddelerinize otomatik olarak temsilci olarak atanacak biçimde sistemi yapılandırmak için, hangi iş maddesi türlerine ne zaman temsilci atanacağını belirten temsilci kuralları oluşturmanız gerekir. Temsilci kuralı oluşturmak için aşağıdaki adımları izleyin.  
3. Ekle öğesini tıklatın.
4. Kapsam alanında, bir seçenek belirleyin.
    * Tümü: Size atanmış olan tüm iş maddelerine temsilci seçin.    Modül: Yalnızca belirli bir iş akışı türüyle ilişkili iş maddelerine temsilci atayın. Bu seçeneği belirlerseniz Ad alanında iş akışı türünü seçmeniz gerekir.    İş akışı: Yalnızca belirli bir iş akışıyla ilişkili iş maddelerine temsilci atayın. Bu seçeneği belirlerseniz Ad alanında iş akışını seçmeniz gerekir.  
5. Temsilci alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin.
    * İş maddelerine ne zaman otomatik olarak temsilci atanmasını istediğinizi belirtmek için Başlangıç tarihi/saati ve Bitiş tarihi/saati alanlarını kullanın.  
6. Başlangıç tarihi/saati alanına tarih ve saati girin.
7. Bitiş tarihi/saati alanına tarih ve saati girin.
8. Bu temsilci kuralını etkinleştirmek için Etkin onay kutusunu işaretleyin.
    * Kapsam olarak Modül'ü seçtiyseniz Ad alanında modülü seçmeniz gerekir.    Kapsam olarak İş akışı'nı seçtiyseniz Ad alanında temsilci atamak üzere ilgili iş akışını seçmeniz gerekir.  
9. Yorum alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.


