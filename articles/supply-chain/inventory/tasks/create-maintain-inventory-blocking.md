---
title: Stok durdurma oluştur ve sürdür
description: Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "322272"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Stok durdurma oluştur ve sürdür

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

