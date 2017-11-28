---
title: "Bir iş akışında koşullu bir kararı yapılandırma"
description: "Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

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






