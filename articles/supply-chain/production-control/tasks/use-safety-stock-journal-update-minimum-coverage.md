--- 
title: "Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma"
description: "Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d278b20724006ec3b3aa557738e8b130ca2bba15
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir. Bu işlem emniyet stoku günlüğü kullanılarak yapılır. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev, üretim planlamacısına minimum kapsamı korumasında yardım etmeye yönelik olarak tasarlanmıştır.


## <a name="create-a-new-safety-stock-journal-name"></a>Yeni bir emniyet stoku günlüğü adı oluşturun.
1. Emniyet stoku günlük adlarına gidin.
2. Yeni'ye tıklayın.
3. Ad alanına "Malzeme" yazın.
4. Açıklama alanına "Malzeme" yazın.
5. Sayfayı kapatın.

## <a name="create-a-safety-stock-journal"></a>Emniyet stoku günlüğü adı oluştur
1. Emniyet stoku hesaplamaya gidin.
2. Yeni'ye tıklayın.
3. Ad alanına bir değer girin veya buradan bir değer seçin.
    * Örneğin, Malzeme gibi oluşturduğunuz emniyet stoku günlük adını seçin.  
4. Satır oluştur'a tıklayın.
5. Başlangıç tarihi alanına bir tarih girin.
    * Tarihi "02.01.2015" olarak ayarlayın.  
6. Bitiş tarihi alanına bir tarih girin.
    * Tarihi "30.12.2015" olarak ayarlayın.  
7. Tamam'a tıklayın.
    * Bu işlem, stok işlemleri olan boyutlar için satırlar oluşturur.  

## <a name="calculate-proposal"></a>Teklifi hesapla
1. Teklifi hesapla'ya tıklayın.
2. Sağlama süresi içinde ortalama stok çıkışını kullan seçeneğini belirleyin.
3. Çarpım faktörünü 10 olarak ayarlayın.
    * Teklifi düzenlemek için Çarpma faktörü kullanılır. Demo verilerde yalnızca birkaç işlem bulunduğundan gerçekçi bir teklif elde etmek için faktörü ayarlamanız gerekir.  
4. Tamam'a tıklayın.
    * M0002 ve M0003'ü bulmak için aşağı kaydırın. Hesaplanan minimum miktar sütununu görüntüleyin.   

## <a name="update-minimum-quantity"></a>Minimum miktarı güncelleştir
1. Yeni minimum miktar alanına bir sayı girin.
    * Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin. Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz. Örneğin, ambar 12'si olan M0002 için bu alana Hesaplanan minimum miktarı girebilirsiniz.  
2. Listede, istenen kaydı bulun ve seçin.
    * Örneğin, ambar 12'si olan M0002'yi seçebilirsiniz.  
3. Yeni minimum miktar alanına bir sayı girin.
    * Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin. Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Yeni minimum miktarı gönderin ve sonucu doğrulayın
1. Deftere Naklet öğesine tıklayın.
2. Tamam'a tıklayın.
3. Madde numarası alanındaki bağlantıyı izlemek için tıklayın.
4. Madde numarası alanındaki bağlantıyı izlemek için tıklayın.
5. Eylem Bölmesinde, Planla öğesine tıklayın.
6. Madde kapsamı'na tıklayın.
    * Minimum miktarın, emniyet stoku günlüğündeki yeni minimum miktar ile güncelleştirildiğine dikkat edin.  


