---
title: Satıcı ödeme koşullarını tanımlama
description: Bu makalede, satıcı faturaları için ödeme koşullarının nasıl ayarlanacağı açıklanmaktadır.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a676856ed43bf1b78684eac0682e0fdef9c84083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906485"
---
# <a name="define-vendor-payment-terms"></a>Satıcı ödeme koşullarını tanımlama

[!include [banner](../../includes/banner.md)]

Bu makalede, satıcı faturaları için ödeme koşullarının nasıl ayarlanacağı açıklanmaktadır. Bu görevde USMF demo şirketi kullanılmaktadır.

1. **Gezinti bölmesi > Modüller > Ödeme tutarı > Ödeme kurulumu > Ödeme şartları**'na gidin.
2. **Yeni**'yi seçin. **Ödeme şartları** sayfası, vade tarihinin nasıl hesaplanacağını tanımlamak için kullanılır. Sayfa, nakit iskontosu tarihinin nasıl hesaplanacağını tanımlamak için kullanılmaz.  
3. **Ödeme şartları** alanına bir değer girin.
4. **Tanım alanına** bir değer girin.
5. **Günler** alanına bir sayı girin. Buraya girilen sayı; vade tarihine veya **Ödeme yöntemi** sayfasında tanımlanan dönem sonuna ekleme yapmak için kullanılır. Örneğin, **Net**'i seçerseniz sayı vade tarihine eklenir. **Geçerli ay**'ı seçerseniz sayı, geçerli ayın son gününe eklenerek vade tarihi hesaplanır.  
6. **Kaydet**'i seçin.
7. Sayfayı kapatın.
8. **Borç hesapları > Ödeme kurulumu > Nakit iskontoları**'na gidin.
9. **Yeni**'yi seçin.
10. **Nakit iskontosu** alanına bir kod girin.
11. **Tanım** alanına bir değer girin.
12. Satıcı katmanlı bir iskonto teklif ederse, geçerli nakit iskontosunun süresi dolduktan sonraki nakit iskontosunu seçin.
13. Sayfayı kapatın.
14. **Günler** alanına bir sayı girin. **Gün** alanına girilen değer, **Net/Geçerli** alanındaki seçime bağlı olarak, **Nakit iskontosu** tarihini hesaplamak için kullanılır. **Net** seçildiyse nakit iskontosu tarihini belirlemek için fatura tarihine bu değer eklenecektir. **Geçerli ay** seçildiyse nakit iskontosu tarihini belirlemek için geçerli ayın sonuna bu değer eklenecektir.  
15. **İskonto** alanına nakit iskontosunun yüzdesini girin. 
16. Müşteri faturaları için nakit iskontosunun nakledileceği ana hesabı girin ve sonra nakit iskontosunun satıcı faturaları için nakledileceği ana hesabı girin. **İskonto mahsup hesapları** ayarı **Satıcı iskontosu için ana hesabı kullan** ayarlanırsa Ana hesap kullanılır. Seçenek **Fatura satırlarındaki hesaplar** olarak ayarlanırsa nakit iskontosu, fatura satırlarındaki kıymet/gider hesaplarına nakledilir.  
17. **Kaydet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
