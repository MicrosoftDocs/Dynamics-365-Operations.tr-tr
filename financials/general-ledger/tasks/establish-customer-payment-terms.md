--- 
title: "Müşteri ödeme koşulları oluşturma"
description: "Bu prosedürde bir nakit iskontosu ve vade tarihi kurulumu tanımlanmaktadır."
author: aprilolson
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
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c871421254be6b0e9443fdf596932776d64428ae
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-payment-terms"></a>Müşteri ödeme koşulları oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde bir nakit iskontosu ve vade tarihi kurulumu tanımlanmaktadır. Bu görev kılavuzunda USMF demo şirketi kullanılmaktadır.

1. Alacak hesapları > Ödemeler >kurulumu > Ödeme günleri'ne gidin.
    * Ödeme şartları için kurulum, Alacak hesapları ve Borç hesapları için paylaşılır. Bunu modül içinde tanımlarsanız, diğer modülde de kullanılabilir. Bu görev kılavuzu için, tüm ödeme şartlarını Alacak hesapları altına aldım.  
2. Yeni'ye tıklayın.
    * Ödeme şartlarınız haftanın belirli bir gününü (Pazartesi, Salı vb.) veya ayın belirli bir tarihini (5'i, 6'sı vb.) gerektiriyorsa bir ödeme günü oluşturun.  
3. Ödeme günü alanına, ödeme günü alanındaki Ödeme günü için bir kod girin.
4. Açıklama alanına, ödeme günü için bir açıklama girin.
5. Hafta/Ay alanında ya Hafta'yı veya Ay'ı seçin.
    * Haftanın bir gününü girmek istiyorsanız (örneğin Pazartesi), Hafta'yı seçin. Ay içinde bir tarih girmek istiyorsanız (örneğin ayın 10'), Ay'ı seçin. Bu örnek için Ay'ı seçin.  
6. Ayın günü alanına tarih girin.
    * Tarih bir sayı olarak girilmelidir (örneğin "10"; yani "10'u" değil).  
7. Kaydet'e tıklayın.
8. Sayfayı kapatın.
9. Alacak hesapları > Ödemeler kurulumu > Ödeme şartları'na gidin.
10. Yeni'ye tıklayın.
    * Ödeme şartları, vade tarihlerinin nasıl hesaplanacağını tanımlamak için kullanılır. Nakit iskontosu tarihi kurulumu ayrı bir sayfada tanımlanır.  
11. Ödeme şartları alanına, Ödeme şartları için bir kod girin.
12. Açıklama alanına bir açıklama girin.
13. Ödeme yöntemi (örneğin TÖ, Net, Geçerli ay vb.) seçin.
    * Ödeme yöntemi, vade tarihi hesaplamasında başlangıcı tanımlamak için kullanılır.  Örneğin, vade tarihi, fatura tarihinden sonra mutlaka bir dizi ay veya gün sayısıysa Net kullanılır. Fatura üzerine ödeme gerekiyorsa TÖ kullanılabilir ve böylece vade tarihi hesaplanmaz. Bu görev kılavuzu için Geçerli ay'ı seçin.  
14. Hesaplamaya belirli bir hafta günü veya tarih eklendiyse bir Ödeme tarihi seçin.
    * Ödeme şartlarınıza bağlı olarak bir tutarı Ay veya Gün olarak girebilirsiniz. Veya, Ödeme yönteminin sonuna 'eklemek' için Ödeme planını veya Ödeme gününü kullanabilirsiniz. Vade tarihi daima sonraki ayın 10'u olacaksa Ödeme günü olarak 10'unu seçin.  
15. Kaydet'e tıklayın.
16. Sayfayı kapatın.
17. Alacak hesapları > Ödemeler kurulumu > Nakit iskontoları'na gidin.
18. Yeni'ye tıklayın.
    * Bu sayfa, nakit iskontosu tarihinin nasıl hesaplanacağını tanımlamak için kullanılır.  
19. Nakit iskontosu alanına, nakit iskontosu için bir kod girin.
20. Açıklama alanına bir açıklama girin.
21. Katmanlı bir nakit iskontosu varsa, bu yeni nakit iskontosundan sonra ilgili Sonraki iskonto kodunu seçin.
22. Nakit iskontosu tarihini hesaplamak için kullanılacak gün sayısını girin.
    * Net ilkesi seçilirse, nakit iskontosu tarihini hesaplamak için fatura tarihine gün sayısı eklenecektir.  
23. Nakit iskontosunun yüzdesini girin.
24. Müşteri faturaları için nakit iskontosunun nakledileceği ana hesabı girin.
25. İskonto mahsup hesapları alanında bir seçenek belirtin.
    * "Fatura satırlarındaki hesaplar"ı seçerseniz, nakit iskontosu, satıcı faturası satırlarındaki aynı kıymet/gider ana hesabına nakledilir. "Satıcı faturaları için ana hesabı kullan"ı seçerseniz, nakit iskontosu, "Satıcı faturaları için ana hesap"ta tanımladığınız ana hesaba nakledilir. Bu örnek için, "Satıcı faturaları için ana hesabı kullan"ı seçin.  
26. Satıcı faturaları için nakit iskontosunun nakledileceği ana hesabı girin.
27. Kaydet'e tıklayın.


