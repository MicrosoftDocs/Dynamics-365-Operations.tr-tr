---
title: İş akışındaki iş öğelerini devretme
description: Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515776"
---
# <a name="delegate-work-items-in-a-workflow"></a>İş akışındaki iş öğelerini devretme

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Bir iş öğesini el ile devredin

Bir tekil iş öğesini devretmek için **Devret** seçeneğini **İş akışı** menüsünde seçin ve daha sonra devredilecek kullanıcıyı bir yorum ile seçin. Bu, iş öğesini tamamlayabilmeleri için bu kullanıcıya yeniden atayacaktır.

## <a name="manually-delegate-multiple-work-items"></a>Çoklu iş öğelerini el ile devret

**Bana atanan iş öğeleri** sayfasından birlikte birden fazla iş öğesine temsilci atanmış olabilir. Aşağıdaki iş akışı türleri toplu temsilci seçme için uygun: Satınalma Sözleşmesi onay iş akışı, satınalma siparişi iş akışı, satınalma talebi gözden geçirme ve satıcı faturası iş akışı. **Çoklu iş öğeleri temsilcisi** özelliği varsayılan olarak devre dışıdır ve **çalışma alanları > özellik yönetimi** etkinleştirilebilir. Bu özelliği etkinleştirme konusunda yardım için sistem yöneticinize başvurun.
1.  **Ortak > Ortak > Çalışma öğeleri > Bana atanan iş öğeleri**'ne gidin.
2.  Temsilci seçilecek iş öğelerini seçin.
3.  **Çalışma öğeleri devret** menüsüne tıklatın.
4.  **Kullanıcı** alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin.
5.  **Yorum** alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.
6.  Çalışma öğesi temsilcisini tamamlamak için **iş maddelerini devret** düğmesini tıklatın.

## <a name="automatically-delegate-work-items"></a>Otomatik olarak iş öğelerini devret

Bir süreliğine ofis dışında olmayı veya başka sebeple iş öğeleri üzerinde çalışamamayı planlıyorsanız, yeni iş öğelerini diğer kullanıcılara **Kullanıcı seçenekleri** sayfasını kullanarak otomatik olarak devredebilirsiniz.

### <a name="set-up-automatic-delegation"></a>Otomatik temsil ayarlama
1. **Ortak > Kurulum > Kullanıcı** seçenekleri'ne gidin.
2. **İş akışı** sekmesine tıklayın. Temsilci bölümünün genişletilmiş olduğundan emin olun. Diğer kullanıcılar iş maddelerinize otomatik olarak temsilci olarak atanacak biçimde sistemi yapılandırmak için, hangi iş maddesi türlerine ne zaman temsilci atanacağını belirten temsilci kuralları oluşturmanız gerekir. Temsilci kuralı oluşturmak için aşağıdaki adımları izleyin.  
3. **Ekle** öğesine tıklayın.
4. **Kapsam** alanında, bir seçenek belirleyin.
    - Tümü: Size atanmış olan tüm iş maddelerine temsilci seçin.
    - Modül: Yalnızca belirli bir iş akışı türüyle ilişkili iş maddelerine temsilci atayın. Bu seçeneği belirlerseniz Ad alanında iş akışı türünü seçmeniz gerekir.
    - İş akışı: Yalnızca belirli bir iş akışıyla ilişkili iş maddelerine temsilci atayın. Bu seçeneği belirlerseniz Ad alanında iş akışını seçmeniz gerekir.  
5. **Temsilci** alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin. İş maddelerine ne zaman otomatik olarak temsilci atanmasını istediğinizi belirtmek için Başlangıç tarihi/saati ve Bitiş tarihi/saati alanlarını kullanın.  
6. **Başlangıç tarihi/saati** alanına tarih ve saati girin.
7. **Bitiş tarihi/saati** alanına tarih ve saati girin.
8. Bu temsilci kuralını etkinleştirmek için **Etkin** onay kutusunu işaretleyin. Kapsam olarak **Modül**'ü seçtiyseniz Ad alanında modülü seçmeniz gerekir. Kapsam olarak **İş akışı**'nı seçtiyseniz Ad alanında temsilci atamak üzere ilgili iş akışını seçmeniz gerekir.  
9. **Yorum** alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.

