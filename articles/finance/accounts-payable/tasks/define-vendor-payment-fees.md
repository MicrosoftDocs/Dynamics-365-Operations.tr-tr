---
title: Satıcı ödeme masraflarını tanımlama
description: Satıcı ödeme masraflarını ayarlayın.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109843"
---
# <a name="define-vendor-payment-fees"></a>Satıcı ödeme masraflarını tanımlama

[!include [banner](../../includes/banner.md)]

Satıcı ödeme masraflarını ayarlayın. Bu görevde USMF demo şirketi kullanılmaktadır.

1. **Borç hesapları > Ödeme kurulumu > Ödeme masrafı**'na gidin.
2. **Yeni**'yi tıklatın.
3. **Ücret kodu** alanına bir değer girin.
    * **Ücret kodu**, bu ücretin ne zaman kullanılacağını açıklar (örneğin "EFT_Ücreti").  
4. **Ad** alanına bir değer yazın.
5. **Ücret açıklaması** alanına bir değer girin.
    * Ücretin ne zaman atanacağı hakkında daha ayrıntılı bilgi vermek için bir açıklama ekleyin.  
6. **Masraf** alanında **Satıcı**'yı veya **Genel muhasebe**'yi seçin.
    * Ücret kuruluşunuza gider olarak yazılacaksa **genel muhasebe** kullanılır. Ücret satıcıya kesilecekse **Satıcı** kullanılır.  
7. Ücretin gider olarak işleneceği bir ana hesap girin.
    * Bu seçenek, yalnızca, **Masraf** seçeneği olarak **Genel muhasebe** belirtildiği zaman kullanılabilir.  
8. Bu ücretin kullanılabileceği günlüğü seçin. 
    * Satıcı ödeme masrafı için, "Satıcıya ödeme" günlüğünü seçersiniz.  
9. **Kaydet**'e tıklayın.
10. **Ödeme masrafı kurulumu**'na tıklayın.
    * Ücretin, seçtiğiniz günlükte ne zaman varsayılan değer alacağını tanımlamak için **Ödeme masrafı kurulumuna** geçin.  
11. **Tablo**'yu, **Grup**'u veya **Tümü**'nü seçin.
    * **Tablo** tek bir banka hesabı seçmek için, **Grup** bir banka grubu seçmek için ve **Tümü** bu ücret kurulumunun tüm banka hesaplarında kullanılması için kullanılır.  
12. Bir banka grubu veya banka hesabı seçin.
    * Aramada, **Grup**'u seçtiyseniz banka grubu, **Tablo**'yu seçtiyseniz banka hesapları gösterilir.  
13. Bu ücretin ne zaman kesileceğini belirlemek için ödeme yöntemini seçin.
14. Seçili ödeme yöntemi için **Ödeme belirtimi**'ni seçin.
    * **Ödeme belirtimi**, elektronik fon transferli ödeme yöntemleriyle birlikte kullanılır.  
15. Ücretin yüzde mi, tutar mı, yoksa aralık mı olacağını belirtin.
16. Ücretin yüzdesini veya tutarını girin.
    * **Ücret** bir yüzde ise, yüzdeyi girin. **Ücret** bir tutarsa, ücretin tutarını girin. **Ücret** bir aralıksa, katmanlı ücretleri tanımlamak için **Aralık** sekmesini kullanın.  
17. **Ücret para birimi** alanında, ücretin kesileceği para birimini seçin.
    * Ücretin para birimi. Ödeme para birimi, ödemenin para birimine göre ücret kuralının ne zaman yürürlüğe gireceğini belirlemek için kullanılır. Örneğin, bankanız avro olarak yapılan ödemeden bir ücret keserken, diğer ödemelerin hiçbirine ücret kesmeyebilir.  
18. **Kaydet**'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
