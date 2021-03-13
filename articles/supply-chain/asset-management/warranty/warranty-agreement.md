---
title: Garanti sözleşmeleri
description: Bu konuda Varlık Yönetimi'ndeki satış sözleşmelerini açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021516"
---
# <a name="warranty-agreements"></a>Garanti sözleşmeleri

[!include [banner](../../includes/banner.md)]

 


Kıymet yönetiminde, bir kıymet veya kıymet türüne bağlı olabilecek garanti koşulları ayarlayabilirsiniz. Garanti koşulları belirli bir dönem için oluşturulur. Garanti, tam tedarik veya kısmi tedarik sağlayacak şekilde ayarlanabilir ve saatler, giderler ve öğelerle ilgili şartlar ayarlayabilirsiniz.

İlk adım, ekipmanınız için olan tüm satıcı garanti sözleşmelerini oluşturmaktır. Sonra, kıymet veya kıymet türlerine garanti sözleşmelerini iliştirin. Satıcı garanti sözleşmeleri yalnızca bilgilendirme amaçlı olarak kullanılır. Satıcı garantisi bir kıymet için ayarlanmışsa, kıymet üzerinde garanti tedarik dönemini görebilirsiniz.

## <a name="create-a-warranty-agreement"></a>Garanti sözleşmesi oluşturma

Garanti sözleşmesi, çalışma saatleri, giderler ve maddeler için garantiyi kapsayacak birkaç sözleşme satırı içerebilir.

1. **Kıymet yönetimi** \> **Kurulum** \> **Kıymetler** \> **Garanti**'yi seçin.
2. Bir ürün oluşturmak için **Yeni**'yi seçin.
3. **Garanti** alanına bir garanti kodu girin. 
4. **Ad** alanında, bir açıklama girin.

    **Ayrıntılar** hızlı sekmesinde, **Kıymetler** alanında garanti sözleşmesini kullanan etkin kıymetlerin sayısı gösterilir.

5. **Garanti satırları** hızlı sekmesinde, garanti sözleşmesine dahil edilmesi gereken satırları eklemek için aşağıdaki adımları uygulayın:

    1. Garantiye yeni bir koşul eklemek için **Satır ekle**'yi seçin. Sıralı satır numarası **Satır** alanına otomatik olarak girilir.
    2. **Dönem** alanında, garanti döneminin türünü seçin.
    3. **Aralık** alanına bir sayı girin. Bu alan, garantinin geçerli olması gereken dönem sayısını tanımlar.
    4. **Yüzde** alanına, garanti satırı için karşılama yüzdesini girin. Yüzde, şirketiniz tarafından kapsanan miktarı gösterir.

![Garanti sayfası](media/01-warranty.png)
