---
title: "Stok durdurma oluşturma ve güncelleştirme"
description: "Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a>Stok durdurma oluşturma ve güncelleştirme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir. Yordamı demo veri şirketi USMF kullanarak, gösterilen örnek değerlerle çalıştırabilirsiniz. Bu yordama başlamadan önce eldeki fiziksel stoka sahip bir öğe olması gerekir.


## <a name="create-an-inventory-blocking"></a>Stok durdurma oluşturun
1. Stok yönetimi > Periyodik görevler > Stok durdurma öğesine gidin.
2. Yeni'ye tıklayın.
3. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede kullanmak istediğiniz maddeyi seçin.
    * Bir madde numarası ile engellemek istediğiniz eldeki fiziksel stoku seçin. USMF kullanıyorsanız, M9201 öğesini seçebilirsiniz.  
5. Miktar alanına bir sayı girin.
    * Madde M9201 kullanıyorsanız, 200'den az seçmeniz gerekir.  
6. Stok bölümünün genişletilmiş görünümüne geçin.
7. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
8. Listede, istenen kaydı bulun ve seçin.
    * Madde M9201 kullanıyorsanız, ambar 51'i seçebilirsiniz.  
9. Kaydet'e tıklayın.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Stok durdurma koşullarını güncelleştirin
1. Miktar alanına bir sayı girin.
    * Stok Miktar alanını, engelleyecek miktarı yansıtacak şekilde güncelleştirin.  
2. Beklenen tarih alanında bir tarih girin.
    * Engellenen stokun rezervasyon için ne zaman kullanılabilir hale geleceğini belirtmek için, tarih atamak isteyebilirsiniz. Stok durdurma için Beklenen girişler seçeneği, bir durdurmayı el ile oluşturduğunuzda varsayılan olduğu şekilde, işaretliyse, bu tarih beklenen hareket üzerinde belirir.  
3. Kaydet'e tıklayın.

## <a name="remove-the-inventory-blocking"></a>Stok durdurmayı kaldırın
1. Sil'i tıklatın.
2. Evet'i tıklatın.
3. Sayfayı kapatın.

