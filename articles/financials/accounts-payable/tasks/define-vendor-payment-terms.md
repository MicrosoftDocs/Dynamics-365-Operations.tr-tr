--- 
title: "Satıcı ödeme koşullarını tanımlama"
description: "Satıcı faturaları için ödeme koşulları ayarlayın."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbac3b27c25377abff341c4bf259e553c14a4ae8
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-terms"></a>Satıcı ödeme koşullarını tanımlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Satıcı faturaları için ödeme koşulları ayarlayın. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Borç hesapları > Ödeme kurulumu > Ödeme şartları'na gidin.
2. Yeni'ye tıklayın.
    * Ödeme şartları sayfası, vade tarihinin nasıl hesaplanacağını tanımlamak için kullanılır. Sayfa, nakit iskontosu tarihinin nasıl hesaplanacağını tanımlamak için kullanılmaz.  
3. Ödeme şartları alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Gün alanına bir sayı girin.
    * Buraya girilen sayı; vade tarihine veya Ödeme yöntemi sayfasında tanımlanan dönem sonuna ekleme yapmak için kullanılır. Örneğin, Net'i seçerseniz, sayı vade tarihine eklenir. Geçerli ay'ı seçerseniz, sayı, geçerli ayın son gününe eklenerek vade tarihi hesaplanır.  
6. Kaydet'e tıklayın.
7. Sayfayı kapatın.
8. Borç hesapları > Ödeme kurulumu > Nakit iskontoları'na gidin.
9. Yeni'ye tıklayın.
10. Nakit iskontosu alanına bir kod girin.
11. Açıklama alanına bir değer girin.
12. Satıcı katmanlı bir iskonto teklif ederse, geçerli nakit iskontosunun süresi dolduktan sonraki nakit iskontosunu seçin.
13. Sayfayı kapatın.
14. Gün alanına bir sayı girin.
    * Gün alanına girilen değer, Net/Geçerli alanındaki seçime bağlı olarak, Nakit iskontosu tarihini hesaplamak için kullanılır. Net seçildiyse, nakit iskontosu tarihini belirlemek için fatura tarihine bu değer eklenecektir. Geçerli ay seçildiyse, nakit iskontosu tarihini belirlemek için geçerli ayın sonuna bu değer eklenecektir.  
15. İskonto alanına nakit iskontosunun yüzdesini girin. 
16. Müşteri faturaları için nakit iskontosunun nakledileceği ana hesabı girin.
17. Satıcı faturaları için nakit iskontosunun nakledileceği ana hesabı girin.
    * İskonto mahsup hesapları ayarı "Satıcı iskontosu için ana hesabı kullan" yapılırsa, Ana hesap kullanılır.  Seçenek "Fatura satırlarındaki hesaplar" olarak ayarlanırsa, nakit iskontosu, fatura satırlarındaki kıymet/gider hesaplarına nakledilir.  
18. Kaydet'e tıklayın.


