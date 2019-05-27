---
title: Müşteri ödeme masrafları oluşturma
description: Müşteri ödemeleri için ödeme masrafları oluşturun.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5acb202d46ef39376a01ca592f60926786d11186
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572986"
---
# <a name="establish-customer-payment-fees"></a>Müşteri ödeme masrafları oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Müşteri ödemeleri için ödeme masrafları oluşturun.

Bu görevde USMF demo şirketi kullanılmaktadır.

1. Alacak hesapları > Ödemeler kurulumu > Ödeme masrafı'na gidin.
2. Yeni'ye tıklayın.
3. Ücret Kodu alanına bir ücret kodu girin.
    * Ödeme günlüklerinde görüntülenen ücret kodu, yazılan ücretin ne ücreti olduğunu anlaşılır kılar.  
4. Ad alanına bir ücret adı girin.
5. Ücret açıklaması alanına ücret için bir açıklama girin.
6. Ücretin Müşteriye mi, yoksa bir Genel muhasebe hesabına mı çıkarılacağını seçin.
    * Ücret müşteriye yazılacaksa, Müşteri'yi seçin. Ücret kuruluşunuza gider olarak yazılacaksa, Genel muhasebe'yi seçin. Bu görev için Müşteri'yi seçin.  
7. Bu ödeme masrafının kullanılabileceği günlük türünü seçin.
    * Bu ücretler müşteri ödemeleri için kullanılıyorsa, günlük türü büyük olasılıkla Müşteri ödemesi olacaktır.  
8. Kaydet'e tıklayın.
9. Ödeme masraf kurulumu'na tıklayın.
    * Ödeme masrafı kurulumu, ödeme ücreti yazılırken kullanılacak ölçütleri tanımlamak için kullanılır.  Örneğin, banka hesabı USMF OPER ve ödeme yöntemi çek olduğu zaman ücretin hesaplanacağını belirtebilirsiniz.  
10. Bu ücret için kullanılabilecek banka hesaplarını tanımlamak için Tablo'yu, Grup'u veya Tümü'nü seçin.
    * Tümü'nü seçerseniz, bu ücret tüm banka hesaplarına yatırılabilir.  Tablo'yu seçerseniz, yalnızca seçtiğiniz banka hesabı bu ücret için kullanılabilir. Grup'u seçerseniz, bu ücret için yalnızca seçili banka grubundaki banka hesapları kullanılabilir.  
11. Bir banka grubu veya banka hesabı seçin.
    * Tablo'yu seçtiyseniz, aramada banka hesapları görüntülenir. Grup'u seçtiyseniz, aramada banka grupları görüntülenir.  
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. Bu ücretin atanacağı Ödeme yöntemini seçin.
    * Örneğin, ödemeleri elektronik ödeme yerine çekle gönderen müşterilerinize bir ücret ödetebilirsiniz.  
14. Listede, istenen kaydı bulun ve seçin.
15. Uygunsa, ödeme para birimi girin.
    * Ödeme para birimi, ücret alınıp alınmayacağını belirlemede ek bir ölçüt olarak kullanılır.  Örneğin, bankanız normalde avro para birimiyle işlem yaptığı için, ABD doları para birimiyle alınan ödemeler için ek bir ücret talep edebilir.  
16. Ücretin yüzde mi, tutar mı, yoksa aralık mı olacağını belirtin.
17. Ücretin yüzdesini veya tutarını girin.
    * Yüzde/Tutar alanı Yüzde'yse, buraya girilen değer bir yüzde olacaktır. Yüzde/Tutar alanı Tutar'sa, buraya girdiğiniz değer bir tutar olacaktır. Yüzde/Tutar alanı Aralık'sa, katmanları tanımlamak için Aralık sekmesini kullanın.  
18. Ücret para birimi alanında Ücretin para birimini seçin.
    * Bu, ücretin oluşturulacağı para birimidir.  
19. Kaydet'e tıklayın.

