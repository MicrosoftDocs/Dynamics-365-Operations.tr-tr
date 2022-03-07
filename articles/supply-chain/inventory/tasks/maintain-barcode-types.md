---
title: Barkod türlerini yönetme
description: Bu yordam, malzeme çekme listesi raporunun bir parçası olarak da kullanılabilen yeni bir barkod açıklamasının nasıl ayarlanacağını gösterir.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571125"
---
# <a name="maintain-bar-code-types"></a>Barkod türlerini yönetme

[!include [banner](../../includes/banner.md)]

Bu yordam, malzeme çekme listesi raporunun bir parçası olarak da kullanılabilen yeni bir barkod açıklamasının nasıl ayarlanacağını gösterir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. USMF kullanıyorsanız, gösterilen örnek değerleri kullanabilirsiniz. Bu görevler genellikle ambar Yöneticisi tarafından yerine getirilir.

1. **Barkodlar**'a gidin.
1. **Yeni**'yi seçin.
1. **Barkod ayarı** alanında, bir değer girin.
1. **Tanım** alanına bir değer girin.
1. **Barkod türü** alanında, bir seçenek belirleyin.
    * USMF kullanıyorsanız, 'Code 39' öğesini seçebilirsiniz.
1. **Maske Kodu** alanında, barkod maskesi kimliğini belirtin. Barkod maskeleri, barkod oluşturmak ve satış noktası (POS) sistemine taranan barkodları hızla tanımlamak için kullanılır. Ayrıntılar için bkz. [Barkod maskelerini ayarlama](../../../commerce/set-up-bar-code-masks.md).
1. **Boyut** alanında, bir sayı girin.
1. **Maksimum uzunluk** alanında, bir sayı girin.
1. **Kaydet**'i seçin.
1. Sayfayı kapatın.
1. **Stok ve ambar yönetim parametreleri**'ne gidin.
1. **Barkod ayarı** alanında, bir değer girin veya bir değer seçin.
    * Daha önce oluşturduğunuz barkod ayarını seçin ancak barkod biçiminin işlemde kullanılan kayıt türü için benzersiz tanımlayıcı biçimiyle eşleşmesi gerektiğini unutmayın. Örneğin, malzeme çekme rotalarının barkod biçimi genellikle bir numara sırası olan malzeme çekme rotası başvuru biçimiyle eşleşmelidir.  
1. **Kaydet**'i seçin.
1. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
