---
title: Satıcı ödeme masraflarını tanımlama
description: Satıcı ödeme masraflarını ayarlayın.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 404bd1e22caa8098f114a2dcc67dd420509cce2b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140479"
---
# <a name="define-vendor-payment-fees"></a>Satıcı ödeme masraflarını tanımlama

[!include [banner](../../includes/banner.md)]

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

