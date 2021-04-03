---
title: İş akışında koşullu kararları yapılandırma
description: Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a593d4e188f47b73967f0c5468f7d7c3e9f64dc8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567472"
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