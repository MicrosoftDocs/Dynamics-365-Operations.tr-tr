---
title: Stok durdurma oluştur ve sürdür
description: Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12c6e047e15aaab157e6de70f4a09f500af2965f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439564"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Stok durdurma oluştur ve sürdür

[!include [banner](../../includes/banner.md)]

Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir. Yordamı demo veri şirketi USMF kullanarak, gösterilen örnek değerlerle çalıştırabilirsiniz. Bu yordama başlamadan önce eldeki fiziksel stoka sahip bir öğe olması gerekir.


## <a name="create-an-inventory-blocking"></a>Stok durdurma oluşturun
1. **Gezinti panosu**'nda, **Modüller > Stok yönetimi > Periyodik görevler > Stok durdurma**'ya gidin.
2. **Yeni**'ye tıklayın.
3. **Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede kullanmak istediğiniz maddeyi seçin. Bir madde numarası ile engellemek istediğiniz eldeki fiziksel stoku seçin. USMF kullanıyorsanız, M9201 öğesini seçebilirsiniz.  
5. **Miktar** alanına bir sayı girin. Madde M9201 kullanıyorsanız, 200'den az seçmeniz gerekir.
6. **Stok boyutları** hızlı sekmesini genişletin.
7. **Ambar** alanında, açılır menü düğmesine tıklayarak aramayı açın.
8. Listede, istenen kaydı bulun ve seçin. Madde M9201 kullanıyorsanız, ambar 51'i seçebilirsiniz.  
9. **Kaydet**'e tıklayın.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Stok durdurma koşullarını güncelleştirin
1. **Genel** hızlı sekmesinde, **Miktar** alanına bir numara girin. Stok Miktar alanını, engelleyecek miktarı yansıtacak şekilde güncelleştirin.  
2. **Beklenen tarih** alanında bir tarih girin. Engellenen stokun rezervasyon için ne zaman kullanılabilir hale geleceğini belirtmek için, tarih atamak isteyebilirsiniz. Stok durdurma için Beklenen girişler seçeneği, bir durdurmayı el ile oluşturduğunuzda varsayılan olduğu şekilde, işaretliyse, bu tarih beklenen hareket üzerinde belirir.  
3. **Kaydet**'e tıklayın.

## <a name="remove-the-inventory-blocking"></a>Stok durdurmayı kaldırın
1. **Eylem Bölmesi**'nde, **Sil** öğesine tıklayın.
2. **Evet** seçeneğini tıklatın.
3. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]