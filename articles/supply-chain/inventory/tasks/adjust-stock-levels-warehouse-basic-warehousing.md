---
title: Ambardaki stok düzeylerini ayarlama (temel ambarlama)
description: Bu yordam, ürünlerin ambardaki stok düzeylerini ayarlamak için bir stok ayarlama günlüğünü oluşturma ve deftere nakletme işlemini size gösterecektir.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9678dffd84e9e4032510811731a67da953b40431
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439569"
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

## <a name="create-journal-lines"></a>Günlük satırları oluştur
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

