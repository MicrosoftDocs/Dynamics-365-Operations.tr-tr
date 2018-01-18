---
title: "Ambardaki stoğu sayma"
description: "Bu yordam, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Ambardaki stoğu sayma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar. Yordam, "temel depolama" işlevi içindir ve Stok Yönetimi modülünde yer alır; Ambar Yönetimi modülünde bulunan ambarlama işlevi için geçerli değildir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. Kendi verilerinizi kullanıyorsanız, ürünlerin ve yerleşimlerin ayarlandığından ve sayım günlükleri için bir stok günlüğü adı oluşturduğunuzdan emin olun. Stok sayımı normalde bir ambar çalışanı tarafından gerçekleştirilir.


## <a name="create-an-inventory-counting-journal"></a>Stok sayım günlüğü oluşturma
1. Stok Yönetimi > Günlük girişleri > Ürün sayımı > Sayım'a gidin.
2. Yeni'ye tıklayın.
3. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, kullanmak istediğiniz stok sayım günlüğünün adını tıklatın.
    * Diğer bazı alanlar, seçtiğiniz stok sayımı günlük adı kurulumu temel alınarak doldurulur.  
5. Çalışan alanında, aramayı açmak için açılır menü düğmesini tıklatın.
6. Listede kullanmak istediğiniz çalışanı seçin.
7. Seç'e tıklayın.
8. Tamam'a tıklayın.

## <a name="create-journal-lines"></a>Günlük satırları oluştur
1. Yeni'ye tıklayın.
2. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, istenen kaydı bulun ve seçin.
    * Demo verileri şirket USMF'yi kullanıyorsanız, 'A0001' öğesini seçin.  
4. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
    * Demo verileri şirket USMF'yi kullanıyorsanız, tesis '2' öğesini seçin.  
6. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. Listede, istenen kaydı bulun ve seçin.
    * Demo verileri şirket USMF'yi kullanıyorsanız, ambar '24' öğesini seçin.  
8. Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.
9. Listede, istenen kaydı bulun ve seçin.
    * Demo verileri şirket USMF'yi kullanıyorsanız, yerleşim 'BULK-001' öğesini seçin.  
10. Sayılan alanında bir sayı girin.
    * Eldeki ürün alanında gösterilen sayıdan farklı bir sayım rakamı girerseniz, Miktar alanı uyuşmazlığı gösterecek şekilde güncelleştirilir.  
11. Kaydet'e tıklayın.

## <a name="post-the-inventory-counting-journal"></a>Stok sayım günlüğünü deftere nakletme
1. Deftere Naklet öğesine tıklayın.
    * Bir stok sayım günlüğünü deftere naklettiğinizde, sayım miktarı Eldeki ürün alanında belirtilenden farklıysa deftere bir stok girişi veya sorun nakledilir, stok düzeyi ve değer değiştirilir ve genel muhasebe hareketleri oluşturulur.  
2. Tamam'a tıklayın.

## <a name="view-inventory-transactions"></a>Stok hareketlerini görüntüle
1. Stok'u tıklatın.
2. Hareketler'e tıklayın.
    * Burada, stok sayım günlüğünüzü deftere naklettiğinizde oluşturulacak tüm ilgili hareketleri görebilirsiniz.   

