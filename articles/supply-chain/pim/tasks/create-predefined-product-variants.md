--- 
title: "Önceden tanımlanmış ürün çeşitleri oluşturma"
description: "Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır."
author: YuyuScheller
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
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c49d25004b19084276404cf887188e89200afa32
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-predefined-product-variants"></a>Önceden tanımlanmış ürün çeşitleri oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır. Bu yöntemi oluşturmak için kullanılan demo şirketi USMF'dir.


## <a name="create-a-product-master"></a>Ana ürün oluşturma
1. Ürün bilgi yönetimi > Ürünler > Ana ürünler'e git.
2. Yeni'ye tıklayın.
3. Ürün numarası alanında bir değer girin.
    * Bir ürün numarasının el ile girilmesi sadece ürün numarası alanı için hiçbir numarası dizisi ayarlanmamışsa gereklidir. Diğer bir deyişle, alan için bir numara serisi ayarlanmışsa bu adımı atlayın.  
4. Ürün adı alanına bir değer girin.
5. Ürün boyutu grubu alanına bir değer girin veya bir değer seçin.
    * SizeCol (Boyut ve Renk) ürün boyut grubunu seçin.  
6. Tamam'a tıklayın.

## <a name="add-product-dimensions"></a>Ürün boyutları ekleme
1. Ürün boyutları öğesini tıklayın.
    * Bu örnekte ürün boyutlarının nasıl el ile girileceği gösterilmiştir. Ayrıca, kullanmak istediğiniz ürün boyutu değerlerini içeren boyut, renk veya tarz grubunu seçebilirsiniz.  
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Ebat alanına bir değer girin veya seçin.
5. İsim alanına bir değer yazın.
6. Yeni'yi tıklatın.
7. Listede, seçili satırı işaretleyin.
8. Ebat alanına bir değer girin veya seçin.
9. İsim alanına bir değer yazın.
10. Renkler sekmesini tıklatın.
11. Yeni'ye tıklayın.
12. Listede, seçili satırı işaretleyin.
13. Renk alanına bir değer girin veya buradan bir değer seçin.
14. İsim alanına bir değer yazın.
15. Yeni'yi tıklatın.
16. Listede, seçili satırı işaretleyin.
17. Renk alanına bir değer girin veya buradan bir değer seçin.
18. İsim alanına bir değer yazın.
19. Kaydet'e tıklayın.
20. Sayfayı kapatın.

## <a name="generate-product-variants"></a>Ürün seçenekleri oluşturma
1. Ürün çeşitleri öğesini tıklayın.
2. Çeşit önerilerini tıklayın.
3. Tümünü seç'i tıklatın.
    * Bu örnekte tüm olası seçenekler dahil edilmiştir. Bu seçeneklerin oluşturulması için sadece olası ürün boyutu kombinasyonlarının bir alt kümesi kullanılacaksa, bireysel girişleri seçebilirsiniz.  
4. Oluştur'a tıklayın.
    * Ürün boyutu değerlerinin kombinasyonuna dayalı olarak tüm seçenekleriniz için açıklamalar oluşturabilirsiniz. Açıklamalar isteğe bağlıdır.  
5. Kaydet'e tıklayın.


