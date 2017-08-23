--- 
title: "Sabit kıymeti transfer etme"
description: "Bu görev kılavuzu, bir mali boyut kümesinden alınan sabit kıymet defterine ait mali bilgileri yeni bir mali boyut kümesine transfer eder."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ebde1e8bd8a87b44dd77b9050d05d6c2f4774ef2
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-a-fixed-asset"></a>Sabit kıymeti transfer etme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu, bir mali boyut kümesinden alınan sabit kıymet defterine ait mali bilgileri yeni bir mali boyut kümesine transfer eder.  Kılavuzda Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.

1. Sabit kıymetler > Sabit kıymetler > Sabit kıymetler menüsüne gidin.
2. Listede, transfer edilecek sabit kıymeti bulup seçin.
3. Eylem Bölmesinde, Sabit kıymet'e tıklayın.
4. Sabit kıymetleri transfer et'e tıklayın.
5. Transfer tarihi alanına bir tarih girin.
6. Transferi açıklayan yorumları girin.
    * Bu liste, sabit kıymet için tüm defterleri gösterir.  
7. Yeni bir mali boyut kümesine transfer etmek istediğiniz defterleri işaretleyin.
    * Bu liste, seçili defter için mevcut mali boyut değerlerini gösterir.  
    * Seçili sabit kıymet defteri için güncelleştirmek istediğiniz mali boyutu seçin.  
8. Mali boyut alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Diğer mali boyut değerlerini Uygun olarak ayarlayın.  
    * Bir transfer yapıldığında bir değer girilmesine veya boş bırakılmasına bağlı olarak tüm mali boyut değerleri değişir. Örneğin, BusinessUnit için bir değer girdiyseniz ve CostCenter ve Department mali boyutlarını boş bıraktığınız zaman. Hesap yapınız CostCenter ve Department için boş değerlere izin veriyorsa, transfer sonucunda her değer modeli BusinessUnit için yeni değer, CostCenter ve Department için boş değer alır.  
9. Güncelleştir'i tıklatın.
    * Transfer tamamlamadan önce değişiklikleri önizleme fırsatınız olacaktır.  
    * Sabit kıymet defterlerini transfer etmeden önce sonuçları gözden geçirin.  
10. Transfer et seçeneğini tıklatın.


