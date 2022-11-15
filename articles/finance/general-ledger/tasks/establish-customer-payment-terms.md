---
title: Müşteri ödeme koşulları oluşturma
description: Bu prosedürde bir nakit iskontosu ve vade tarihi kurulumu tanımlanmaktadır.
author: aprilolson
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b2ae5e63a2efb4bc913efa4d88c65a70133a2d9
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752789"
---
# <a name="establish-customer-payment-terms"></a>Müşteri ödeme koşulları oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedürde bir nakit iskontosu ve vade tarihi kurulumu tanımlanmaktadır. Bu görev kılavuzunda USMF demo şirketi kullanılmaktadır.

1. **Gezinti bölmesi > Modüller > Alacak hesapları > Ödemeler kurulumu > Ödeme günleri**'ne gidin. **Ödeme şartları** için kurulum, **Alacak hesapları** ve **Borç hesapları** için paylaşılır. Bunu modül içinde tanımlarsanız, diğer modülde de kullanılabilir. Bu görev kılavuzu için, **Alacak hesapları** altındaki tüm ödeme şartları ayarlanmıştır.
2. **Yeni**'yi tıklatın. Ödeme şartlarınız haftanın belirli bir gününü (Pazartesi, Salı vb.) veya ayın belirli bir tarihini (5'i, 6'sı vb.) gerektiriyorsa bir ödeme günü oluşturun. 
3. **Ödeme günü** alanına bir kod girin.
4. **Açıklama** alanına, ödeme günü için bir açıklama girin.
5. **Hafta/Ay** alanında ya 'Hafta'yı veya 'Ay'ı seçin. Haftanın bir gününü girmek istiyorsanız (örneğin Pazartesi), Hafta'yı seçin. Ay içinde bir tarih girmek istiyorsanız (örneğin ayın 10'), Ay'ı seçin. Bu örnek için Ay'ı seçin. 
6. **Ayın günü** alanına tarih girin. Tarih bir sayı olarak girilmelidir (örneğin "10"; yani "10'u" değil). 
7. **Kaydet**'e tıklayın.
8. Sayfayı kapatın.
9. **Gezinti bölmesi > Modüller > Alacak hesapları > Ödemeler kurulumu > Ödeme koşulları**'na gidin. 

>[!NOTE] 
>**Ödeme koşulları** **Nakit** olarak belirlenmişse, **Ödeme koşulları** sayfasındaki **Nakit ödeme** alanı **Hayır** olmalıdır.

10. **Yeni**'yi tıklatın. **Ödeme şartları**, vade tarihlerinin nasıl hesaplanacağını tanımlamak için kullanılır. Nakit iskontosu tarihi kurulumu ayrı bir sayfada tanımlanır. 
11. **Ödeme koşulları** alanına bir kod girin.
12. **Açıklama** alanına bir açıklama girin.
13. **TÖ**, **Net**, **Geçerli ay** gibi bir **Ödeme yöntemi** seçin. **Ödeme yöntemi**, vade tarihinin nasıl hesaplanacağını tanımlamak için kullanılır. Örneğin, vade tarihi, fatura tarihinden sonra mutlaka bir dizi ay veya gün sayısıysa **Net** kullanılır. Fatura üzerine ödeme gerekiyorsa **TÖ** kullanılabilir ve böylece vade tarihi hesaplanmaz. Bu görev kılavuzu için **Geçerli ay**'ı seçin.  
14. Hesaplamaya belirli bir hafta günü veya tarih eklendiyse bir **Ödeme tarihi** seçin. Ödeme şartlarınıza bağlı olarak bir tutarı Ay veya Gün olarak girebilirsiniz. Alternatif olarak, **Ödeme yönteminin** sonuna "eklemek" için **Ödeme planını** veya **Ödeme gününü** kullanabilirsiniz. Vade tarihi daima sonraki ayın 10'u olacaksa **Ödeme günü** olarak 10'unu seçin. **Ödeme takvimi** kullanıyorsanız hesaplanan tarih iş günü olmayan bir güne geldiğinde vade tarihinin nasıl belirleneceğini tanımlayabilirsiniz. Başlangıç vade tarihi, takvim günleri kullanılarak hesaplanır. Hesaplanan tarih iş günü olmayan bir güne gelirse hesaplanan vade tarihini bir sonraki veya bir önceki iş gününe ayarlayabilirsiniz.
15. **Kaydet**'e tıklayın.
16. Sayfayı kapatın.
17. **Alacak hesapları > Ödemeler kurulumu > Nakit iskontoları**'na gidin.
18. **Yeni**'ye tıklayın. Bu sayfa, nakit iskontosu tarihinin nasıl hesaplanacağını tanımlamak için kullanılır. 
19. **Nakit iskontosu** alanına bir kod girin.
20. **Açıklama** alanına bir açıklama girin.
21. Katmanlı bir nakit iskontosu varsa, bu yeni nakit iskontosundan sonra ilgili **Sonraki iskonto kodu**'nu seçin.
22. **Günler** alanına nakit iskontosu tarihini hesaplamak için kullanılacak gün sayısını girin. **Net** ilkesi seçilirse, nakit iskontosu tarihini hesaplamak için fatura tarihine gün sayısı eklenecektir.  
23. **İskonto yüzdesi** alanına nakit iskontosunun yüzdesini girin.
24. **Müşteri iskontoları için ana hesap**'ta nakit iskontosunun müşteri faturalarına nakil olacağı ana hesabı girin.
25. **İskonto mahsup hesapları** alanında bir seçenek belirtin. "Fatura satırlarındaki hesaplar"ı seçerseniz, nakit iskontosu, satıcı faturası satırlarındaki aynı kıymet/gider ana hesabına nakledilir. **Satıcı faturaları için ana hesabı kullan** seçeneğini belirlerseniz nakit iskontosu, **Satıcı faturaları için ana hesap**'ta tanımladığınız ana hesaba nakledilir. Bu örnek için **Satıcı faturaları için ana hesabı kullan** seçeneğini belirleyin. 
26. **Satıcı iskontoları için ana hesap** alanında nakit iskontosunun satıcı faturalarına nakil olacağı ana hesabı girin.
27. **Kaydet**'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
