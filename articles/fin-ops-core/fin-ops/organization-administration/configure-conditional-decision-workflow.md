---
title: İş akışında koşullu kararları yapılandırma
description: Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a880d4be461ea9b2caa61b7d038f9b24486a919
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798893"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>İş akışında koşullu kararları yapılandırma

[!include [banner](../includes/banner.md)]

Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.

Koşullu karar, bir iş akışının iki dala ayrıldığı bir noktadır. Koşullu bir kararı iş akışı düzenleyicisinde yapılandırmak için koşullu karara sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.

## <a name="name-a-decision"></a>Karara ad verme

Koşullu bir karara bir ad vermek için aşağıdaki adımları uygulayın.

1. Sol bölmede **Temel Ayarlar**'a tıklayın.
2. Koşullu karar için **Ad** alanına benzersiz bir ad girin.

## <a name="set-conditions"></a> Koşulları ayarlama

Sistem, gönderilen belgeyi belirli koşulları karşılayıp karşılamadığını belirlemek için değerlendirerek hangi dalın kullanıldığını belirler.

1. Sol bölmede **Temel Ayarlar**'a tıklayın.
2. **Koşul ekle** seçeneğini tıklatın.
3. Koşulu girin.
4. Gerekiyorsa ek koşulları girin.
5. Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için aşağıdaki adımları tamamlayın:

    1. **Sınama iş akışı koşulu** formunu açmak için **Sına**'ya tıklayın.
    2. Formdaki **Koşulu doğrula** alanından bir kayıt seçin.
    3. **Sına**'ya tıklayın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.
    4. **Özellikler** formuna geri dönmek için **Tamam** veya **İptal**'e tıklayın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]