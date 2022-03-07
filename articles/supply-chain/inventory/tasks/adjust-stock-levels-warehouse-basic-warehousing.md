---
title: Ambardaki stok düzeylerini ayarlama (temel ambarlama)
description: Bu yordam, ürünlerin ambardaki stok düzeylerini ayarlamak için bir stok ayarlama günlüğünü oluşturma ve deftere nakletme işlemini size gösterecektir.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02458d588c9925a1f4cb9afeada793dfc55a2071
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573837"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Ambardaki stok düzeylerini ayarlama (temel ambarlama)

[!include [banner](../../includes/banner.md)]

Bu yordam, ürünlerin ambardaki stok düzeylerini ayarlamak için bir stok ayarlama günlüğünü oluşturma ve deftere nakletme işlemini size gösterecektir. Buna başlamadan önce stok düzeltmeleri için ayarlanmış bir stok günlüğü adı olması gerekir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. Bu görevler normalde ambar personeli tarafından yerine getirilir.


## <a name="create-an-inventory-adjustment-journal"></a>Bir stok düzeltme günlüğünü yaratmak
1. Stok yönetimi > Yevmiye defteri girişleri > Öğeler > Stok düzeltmesi öğesine gidin.
2. Yeni'ye tıklayın.
3. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, kullanmak istediğiniz stok ayarlama günlük adını tıklatın.
    * Diğer bazı alanlar, seçtiğiniz stok ayarlama günlük adı kurulumu temel alınarak doldurulur.  
5. Tamam'a tıklayın.

## <a name="create-journal-lines"></a>Yevmiye defteri satırları oluştur
1. Yeni'ye tıklayın.
2. Listede madde numarası alanını işaretleyin.
3. Madde numarası alanında bir maddeyi seçin. Demo verileri şirket USMF'yi kullanıyorsanız, 'D0001' yazın.
4. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, bir tesis seçin.
6. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. Listede bir ambar seçin.
    * Bir öğe için zorunlu boyut olarak konum seçtiyseniz, burada konumu belirtmeniz gerekecektir.  
8. Miktar alanına bir sayı girin.
    * Maliyet fiyatı alanı, stok girişleriyle bağlantılı olarak birim başına maliyeti belirtir. Madde numarası için maliyetin belirtilmemiş olması veya bunu el ile değiştirmek istemeniz durumunda, bunu burada yapabilirsiniz.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Stok düzeltme günlüğünü geçerli kılın ve nakledin
1. Doğrula'ya tıklayın.
2. Tamam'a tıklayın.
3. Deftere Naklet öğesine tıklayın.
    * Bu tür bir günlüğü naklettiğinizde stok girişi veya çıkışı nakledilir, stok düzeyi ve değeri değiştirilir ve genel muhasebe hareketleri oluşturulur.  
4. Tamam'a tıklayın.
5. Formu kapatın.
6. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]