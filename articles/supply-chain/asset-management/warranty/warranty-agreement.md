---
title: Garanti sözleşmeleri
description: Bu makalede Varlık Yönetimi'ndeki satış sözleşmelerini açıklanmaktadır.
author: johanhoffmann
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 32e5ba8bf87d7bcd30e7f1493540317764d347ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864041"
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

![Garanti sayfası.](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]