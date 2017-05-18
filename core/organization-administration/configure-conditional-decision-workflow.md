---
title: "Bir iş akışında koşullu bir kararı yapılandırma"
description: "Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d3efb6106df7d66ebe9b1a061f9976b8978704b1
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Bir iş akışında koşullu bir kararı yapılandırma

[!include[banner](../includes/banner.md)]


Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.

Koşullu karar, bir iş akışının iki dala ayrıldığı bir noktadır. Koşullu bir kararı iş akışı düzenleyicisinde yapılandırmak için koşullu karara sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.

## <a name="name-a-decision"></a>Karara ad verme
Koşullu bir karara bir ad vermek için aşağıdaki adımları uygulayın.
1.  Sol bölmede **Temel Ayarlar**'a tıklayın.
2.  Koşullu karar için **Ad** alanına benzersiz bir ad girin.

## <a name="set-conditions"></a> Koşulları ayarlama
Sistem, gönderilen belgeyi belirli koşulları karşılayıp karşılamadığını belirlemek için değerlendirerek hangi dalın kullanıldığını belirler.
1.  Sol bölmede **Temel Ayarlar**'a tıklayın.
2.  **Koşul ekle** seçeneğini tıklatın.
3.  Koşulu girin.
4.  Gerekiyorsa ek koşulları girin.
5.  Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için aşağıdaki adımları tamamlayın:
    1.  **Sınama iş akışı koşulu** formunu açmak için **Sına**'ya tıklayın.
    2.  Formdaki **Koşulu doğrula** alanından bir kayıt seçin.
    3.  **Sına**'ya tıklayın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.
    4.  **Özellikler** formuna geri dönmek için **Tamam** veya **İptal**'e tıklayın.






