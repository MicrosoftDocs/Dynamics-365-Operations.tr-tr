---
title: Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma
description: Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b0985169f7ffadbf97ed4f237c8ec11120cfc3e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981011"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma

[!include [banner](../../includes/banner.md)]

Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir. Bu işlem emniyet stoku günlüğü kullanılarak yapılır. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev, üretim planlamacısına minimum kapsamı korumasında yardım etmeye yönelik olarak tasarlanmıştır.


## <a name="create-a-new-safety-stock-journal-name"></a>Yeni bir emniyet stoku günlüğü adı oluşturun.
1. **Gezinti bölmesinde** **Master planlama > Kurulum > Emniyet stoku günlüğü adları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanına "Malzeme" yazın.
4. **Açıklama** alanına "Malzeme" yazın.
5. Sayfayı kapatın.

## <a name="create-a-safety-stock-journal"></a>Emniyet stoku günlüğü adı oluştur
1. **Gezinti bölmesinde** **Master planlama > Master planlama > Çalıştır > Emniyet stoku hesaplama**'ya gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin. Örneğin, Malzeme gibi oluşturduğunuz emniyet stoku günlük adını seçin.  
4. **Satırlar oluştur**'a tıklayın.
5. **Başlangıç tarihi** alanına bir tarih girin.  
6. **Bitiş tarihi** alanına bir tarih girin.
7. **Tamam**'a tıklayın. Bu işlem, stok işlemleri olan boyutlar için satırlar oluşturur.  

## <a name="calculate-proposal"></a>Teklifi hesapla
1. **Teklifi hesapla**'ya tıklayın.
2. **Sağlama süresi içinde ortalama stok çıkışını kullan** seçeneğini belirleyin.
3. **Çarpım faktörünü** '10' olarak ayarlayın. Teklifi düzenlemek için Çarpma faktörü kullanılır. Demo verilerde yalnızca birkaç işlem bulunduğundan gerçekçi bir teklif elde etmek için faktörü ayarlamanız gerekir.  
4. **Tamam**'a tıklayın. M0002 ve M0003'ü bulmak için aşağı kaydırın. **Hesaplanan minimum** miktar sütununu görüntüleyin.   

## <a name="update-minimum-quantity"></a>Minimum miktarı güncelleştir
1. **Yeni minimum miktar** alanına bir sayı girin. Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin. Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz. Örneğin, ambar 12'si olan M0002 için bu alana Hesaplanan minimum miktarı girebilirsiniz.  
2. Listede, istenen kaydı bulun ve seçin. Örneğin, ambar 12'si olan M0002'yi seçebilirsiniz.  
3. **Yeni minimum miktar** alanına bir sayı girin. Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin. Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Yeni minimum miktarı gönderin ve sonucu doğrulayın
1. **Naklet**'e tıklayın.
2. **Tamam**'a tıklayın.
3. **Madde numarası** alanındaki bağlantıyı izlemek için tıklayın.
4. **Madde numarası** alanındaki bağlantıyı izlemek için tıklayın.
5. **Eylem Bölmesi**'nde Plan'a tıklayın.
6. **Madde kapsamı**'na tıklayın. **Minimum miktarın**, emniyet stoku günlüğündeki yeni minimum miktar ile güncelleştirildiğine dikkat edin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]