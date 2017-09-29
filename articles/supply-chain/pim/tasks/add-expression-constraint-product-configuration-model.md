--- 
title: "Ürün yapılandırma modeline bir ifade kısıtlaması ekleme"
description: "Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b8286eba5c799789ebba9a501a5a0b06ccdaabb1
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Ürün yapılandırma modeline bir ifade kısıtlaması ekleme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir. Kullanıcı ön ızgarayı metal olarak seçtiyse bir hoparlöre köşe koruması uygulanması gerektiğini nasıl zorunlu kılacağınızı gösterir. Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.


## <a name="create-an-expression-constraint"></a>Bir ifade kısıtlaması oluşturma
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
    * Bu örnek, son teknoloji hoparlör modeli kullanır.  
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Sınırlamalar bölümünü genişletin.
6. Ekle öğesini tıklatın.
7. Oluştur'a tıklayın.
8. İsim alanına bir değer yazın.

## <a name="enter-expression"></a>İfade girin
1. İfadeyi düzenle'yi tıklatın.
    * Bu aşamada görev kaydında kullanıcı arabiriminin kilidini açarsanız, kısıtlama ifadesi oluşturmak için IntelliSense'i ve simgeler listesini kullanabilirsiniz.  
2. ConstraintBody alanında, 'Implies[FrontGrill=="Metal", CornerProtection] ' değerini girin.
    * Bu ifade mantığı şu anlamdadır: Ön ızgara metalse, köşe koruma seçeneği seçili olmalıdır.  
3. Doğrula'ya tıklayın.
    * Doğrulama işlevi, kısıtlama ifadesini gözden geçirir ve sözdizimi hatalarını denetler.  
4. Kapat’a tıklayın.
5. Tamam'a tıklayın.

