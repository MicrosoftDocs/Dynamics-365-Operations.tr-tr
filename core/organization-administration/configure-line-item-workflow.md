---
title: "Satır maddesi iş akışı yapılandırma"
description: "Bu konu, bir satır maddesi iş akışı öğesinin nasıl yapılandırılacağını açıklar."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e92895ce9cc87e933c4d1efc7ac74f9db07b2951
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-line-item-workflow"></a>Satır maddesi iş akışı yapılandırma

[!include[banner](../includes/banner.md)]


Bu konu, bir satır maddesi iş akışı öğesinin nasıl yapılandırılacağını açıklar.

Satır maddesi iş akışı öğesi yapılandırmak için öğeye sağ tıklayın ve ardından **Özellikler** sayfasını açmak için **Özellikler**'e tıklayın. Ardından satır maddesi iş akışı öğesinin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-lineitem-workflow-element"></a>Satır maddesi iş akışı öğesini adlandırın
Satır maddesi iş akışı öğesi için bir ad girmek için bu adımları izleyin.

1.  Sol bölmede **Temel Ayarlar**'a tıklayın.
2.  **Ad** alanında satır maddesi iş akışı öğesi için benzersiz bir ad girin.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Aynı iş akışının tüm satır maddelerini işlemek için kullanılıp kullanılmayacağını belirtin
Aynı iş akışının bir belgedeki tüm satır maddelerini işlemek için kullanılıp kullanılmayacağını belirtmek için aşağıdaki adımları izleyin.

1.  Sol bölmede **Temel Ayarlar**'a tıklayın.
2.  Belgedeki tüm satır maddelerini aynı iş akışının işlemesi gerekiyorsa **Tüm satır maddeleri için tek bir iş akışı çağır**'a tıklayın. Ardından satır maddelerini işlemek için kullanılacak iş akışını seçin.
3.  Belirli bir koşul kümesini karşılayan satır maddelerini belirli bir iş akışının işlemesi gerekiyorsa **Her satır maddesi için bir iş akışı çağır**'a tıklayın. Ardından koşul kümesini tanımlamak için bu adımları izleyin:
    1.  **Ekle** öğesine tıklayın.
    2.  Tablodaki koşulu seçin.
    3.  **Koşul adı** sekmesinde tanımlamakta olduğunuz koşul kümesi için bir ad girin.
    4.  Koşulu girmek için **Koşul ekle**'ye tıklayın.
    5.  Varsa, gerekli ek koşulları girin.
    6.  Girdiğiniz koşul kümesinin doğru biçimde yapılandırıldığını doğrulamak için, **Sına**'ya tıklayın. **Sınama iş akışı koşulu** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin ve ardından **Sına**'ya tıklayın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir. **Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.

    **İş akışı** sekmesinde tanımladığınız koşul kümesini karşılayan satır maddelerini işlemek için kullanılacak iş akışını seçin.




