---
title: Satıcı ödeme koşullarını tanımlama
description: Bu konu, satıcı faturaları için ödeme koşullarının nasıl ayarlanacağını açıklar.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b69b505996b5536088578885c11a7e8c27f4975
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971865"
---
# <a name="define-vendor-payment-terms"></a>Satıcı ödeme koşullarını tanımlama

[!include [banner](../../includes/banner.md)]

Bu konu, satıcı faturaları için ödeme koşullarının nasıl ayarlanacağını açıklar. Bu görevde USMF demo şirketi kullanılmaktadır.

1. **Gezinti bölmesi > Modüller > Ödeme tutarı > Ödeme kurulumu > Ödeme şartları**'na gidin.
2. **Yeni**'yi seçin. Ödeme şartları sayfası, vade tarihinin nasıl hesaplanacağını tanımlamak için kullanılır. Sayfa, nakit iskontosu tarihinin nasıl hesaplanacağını tanımlamak için kullanılmaz.  
3. **Ödeme şartları** alanına bir değer girin.
4. **Tanım alanına** bir değer girin.
5. **Günler** alanına bir sayı girin. Buraya girilen sayı; vade tarihine veya Ödeme yöntemi sayfasında tanımlanan dönem sonuna ekleme yapmak için kullanılır. Örneğin, **Net**'i seçerseniz sayı vade tarihine eklenir. **Geçerli ay**'ı seçerseniz sayı, geçerli ayın son gününe eklenerek vade tarihi hesaplanır.  
6. **Kaydet**'i seçin.
7. Sayfayı kapatın.
8. **Borç hesapları > Ödeme kurulumu > Nakit iskontoları**'na gidin.
9. **Yeni**'yi seçin.
10. **Nakit iskontosu** alanına bir kod girin.
11. **Tanım** alanına bir değer girin.
12. Satıcı katmanlı bir iskonto teklif ederse, geçerli nakit iskontosunun süresi dolduktan sonraki nakit iskontosunu seçin.
13. Sayfayı kapatın.
14. **Günler** alanına bir sayı girin. **Gün** alanına girilen değer, **Net/Geçerli** alanındaki seçime bağlı olarak, Nakit iskontosu tarihini hesaplamak için kullanılır. **Net** seçildiyse nakit iskontosu tarihini belirlemek için fatura tarihine bu değer eklenecektir. **Geçerli ay** seçildiyse nakit iskontosu tarihini belirlemek için geçerli ayın sonuna bu değer eklenecektir.  
15. **İskonto** alanına nakit iskontosunun yüzdesini girin. 
16. Müşteri faturaları için nakit iskontosunun nakledileceği ana hesabı girin ve sonra nakit iskontosunun satıcı faturaları için nakledileceği ana hesabı girin. **İskonto mahsup hesapları** ayarı **Satıcı iskontosu için ana hesabı kullan** ayarlanırsa Ana hesap kullanılır. Seçenek **Fatura satırlarındaki hesaplar** olarak ayarlanırsa nakit iskontosu, fatura satırlarındaki kıymet/gider hesaplarına nakledilir.  
17. **Kaydet**'i seçin.

