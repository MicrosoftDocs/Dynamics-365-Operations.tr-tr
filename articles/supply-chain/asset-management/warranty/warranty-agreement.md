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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439438"
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
