---
title: Satır maddesi iş akışlarını yapılandırma
description: Bu konu, bir satır maddesi iş akışı öğesinin nasıl yapılandırılacağını açıklar.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a72719c9fd03f73b69b558fc0f08eed91ea94ee1
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694371"
---
# <a name="configure-line-item-workflows"></a>Satır maddesi iş akışlarını yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu, bir satır maddesi iş akışı öğesinin nasıl yapılandırılacağını açıklar.

Satır maddesi iş akışı öğesi yapılandırmak için öğeye sağ tıklayın ve ardından **Özellikler** sayfasını açmak için **Özellikler**'e tıklayın. Ardından satır maddesi iş akışı öğesinin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.

## <a name="name-the-line-item-workflow-element"></a>Satır maddesi iş akışı öğesini adlandırın

Satır maddesi iş akışı öğesi için bir ad girmek için bu adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'a tıklayın.
2. **Ad** alanında satır maddesi iş akışı öğesi için benzersiz bir ad girin.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Aynı iş akışının tüm satır maddelerini işlemek için kullanılıp kullanılmayacağını belirtin

Aynı iş akışının bir belgedeki tüm satır maddelerini işlemek için kullanılıp kullanılmayacağını belirtmek için aşağıdaki adımları izleyin.

1. Sol bölmede **Temel Ayarlar**'a tıklayın.
2. Belgedeki tüm satır maddelerini aynı iş akışının işlemesi gerekiyorsa **Tüm satır maddeleri için tek bir iş akışı çağır**'a tıklayın. Ardından satır maddelerini işlemek için kullanılacak iş akışını seçin.
3. Belirli bir koşul kümesini karşılayan satır maddelerini belirli bir iş akışının işlemesi gerekiyorsa **Her satır maddesi için bir iş akışı çağır**'a tıklayın. Ardından koşul kümesini tanımlamak için bu adımları izleyin:

    1. **Ekle** öğesine tıklayın.
    2. Tablodaki koşulu seçin.
    3. **Koşul adı** sekmesinde tanımlamakta olduğunuz koşul kümesi için bir ad girin.
    4. Koşulu girmek için **Koşul ekle**'ye tıklayın.
    5. Varsa, gerekli ek koşulları girin.
    6. Girdiğiniz koşul kümesinin doğru biçimde yapılandırıldığını doğrulamak için, **Sına**'ya tıklayın. **Sınama iş akışı koşulu** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin ve ardından **Sına**'ya tıklayın. Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir. **Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.

    **İş akışı** sekmesinde tanımladığınız koşul kümesini karşılayan satır maddelerini işlemek için kullanılacak iş akışını seçin.
