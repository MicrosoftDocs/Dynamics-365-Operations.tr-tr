--- 
title: "Ürün yapılandırma modeline hesaplama ekleme"
description: "Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Ürün yapılandırma modeline hesaplama ekleme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir. Beyaz hoparlörler için hoparlör yüksekliğini 10 ve diğer dolaplar için 15 olarak ayarlamak için "If" işlecini kullanarak bir mantıksal ifadeyi nasıl oluşturabileceğinizi gösterir. Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.


## <a name="add-a-calculation"></a>Hesaplama ekleme

## <a name="create-calculation-expression"></a>Hesaplama ifadesi oluşturma
1. İfadeyi düzenle'yi tıklatın.
2. ConstraintBody alanında, 'If[CabinetFinish=="White", 10, 15]' değerini girin.
3. Doğrula'ya tıklayın.
4. Kapat’a tıklayın.
5. Tamam'a tıklayın.


