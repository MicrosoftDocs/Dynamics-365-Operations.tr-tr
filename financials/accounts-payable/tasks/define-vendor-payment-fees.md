--- 
title: "Satıcı ödeme masraflarını tanımlama"
description: "Satıcı ödeme masraflarını ayarlayın."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 844badb3b3037df8c4f22be558f01ea3dbf37f9d
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-fees"></a>Satıcı ödeme masraflarını tanımlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Satıcı ödeme masraflarını ayarlayın. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Borç hesapları > Ödeme kurulumu > Ödeme masrafı'na gidin.
2. Yeni'ye tıklayın.
3. Ücret Kodu alanına bir değer girin.
    * Ücret kodu, bu ücretin ne zaman kullanılacağını açıklar (örneğin "EFT_Ücreti").  
4. İsim alanına bir değer yazın.
5. Ücret açıklaması alanına bir değer girin.
    * Ücretin ne zaman atanacağı hakkında daha ayrıntılı bilgi vermek için bir açıklama ekleyin.  
6. Masraf alanında Satıcı'yı veya Genel muhasebe'yi seçin.
    * Ücret kuruluşunuza gider olarak yazılacaksa genel muhasebe kullanılır.  Ücret satıcıya kesilecekse Satıcı kullanılır.  
7. Ücretin gider olarak işleneceği bir ana hesap girin.
    * Bu seçenek, yalnızca, Masraf seçeneği olarak Genel muhasebe belirtildiği zaman kullanılabilir.  
8. Bu ücretin kullanılabileceği günlüğü seçin. 
    * Satıcı ödeme masrafı için, "Satıcıya ödeme" günlüğünü seçersiniz.  
9. Kaydet'e tıklayın.
10. Ödeme masraf kurulumu'na tıklayın.
    * Ücretin, seçtiğiniz günlükte ne zaman varsayılan değer alacağını tanımlamak için Ödeme masrafı kurulumuna geçin.  
11. Tablo'yu, Grup'u veya Tümü'nü seçin.
    * Tablo tek bir banka hesabı seçmek için, Grup bir banka grubu seçmek için ve Tümü, bu ücret kurulumunun tüm banka hesaplarında kullanılması için kullanılır  
12. Bir banka grubu veya banka hesabı seçin.
    * Aramada, Grup'u seçtiyseniz banka grubu, Tablo'yu seçtiyseniz banka hesapları gösterilir.  
13. Bu ücretin ne zaman kesileceğini belirlemek için ödeme yöntemini seçin.
14. Seçili ödeme yöntemi için Ödeme belirtimini seçin.
    * Ödeme belirtimi, elektronik fon transferli ödeme yöntemleriyle birlikte kullanılır.  
15. Ücretin yüzde mi, tutar mı, yoksa aralık mı olacağını belirtin.
16. Ücretin yüzdesini veya tutarını girin.
    * Ücret bir yüzde ise, yüzdeyi girin. Ücret bir tutarsa, ücretin tutarını girin. Ücret bir aralıksa, katmanlı ücretleri tanımlamak için Aralık sekmesini kullanın.  
17. Ücret para birimi alanında, ücretin kesileceği para birimini seçin.
    * Ücretin para birimi. Ödeme para birimi, ödemenin para birimine göre ücret kuralının ne zaman yürürlüğe gireceğini belirlemek için kullanılır. Örneğin, bankanız avro olarak yapılan ödemeden bir ücret keserken, diğer ödemelerin hiçbirine ücret kesmeyebilir.  
18. Kaydet'e tıklayın.


