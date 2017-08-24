--- 
title: "Tahsilat mektubu sırası oluşturma"
description: "Tahsilat mektubu sırası oluşturmak için bu görev kılavuzunu kullanın."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b050d47910c146b9691e7aae5b4a1a847ce716e
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-collection-letter-sequence"></a>Tahsilat mektubu sırası oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tahsilat mektubu sırası oluşturmak için bu görev kılavuzunu kullanın. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Alacak ve tahsilatlar > Kurulum > Tahsilat mektubu sırasını ayarla'ya gidin.
2. Yeni'ye tıklayın.
3. Tahsilat mektubu sırası alanında, sırayı temsil edecek bir sıra kodu girin. Bir deftere nakil profili ayarladığınız zaman kullanılır.
4. Açıklama alanına bir değer girin.
    * Ödeme şartları isteğe bağlıdır. Buraya bir değer girerseniz, tahsilat mektubu ücreti faturasında, müşteriyle depolanan ödeme şartları yerine bu ödeme şartları kullanılır.  
5. Tahsilat mektubu kodu alanında, göndermek istediğiniz ilk tahsilat mektubunun kodunu seçin.
    * İlk tahsilat mektubu, faturadaki vade tarihine, bu satırdaki Gün alanında mehil süresi için girdiğiniz değere ve bu satıra girdiğiniz diğer bilgilere göre oluşturulur.  
6. Açıklama alanına bir değer girin.
    * Ücretin para birimi, müşteri para biriminin varsayılan değeri olur. Bu para birimi kodu, fatura para biriminden farklı olabilir.  
7. Sırada gönderilecek sonraki tahsilat mektubunu eklemek için Ekle'ye tıklayın
    * Çoğu durumda, ilk tahsilat mektubu yalnızca bir uyarıdır. Gerekirse ücretler ekleyebilirsiniz.  
8. Tahsilat mektubu kodu alanında, sıradaki gönderilecek sonraki tahsilat mektubunu seçin.
9. Tanım alanına bir değer girin.
10. Ana hesap alanında, ücretler için kullanılacak gelir hesabını seçin.
11. Bu tahsilat mektubu deftere nakledilince yansıtılacak ücreti girin.
12. Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Ücret üzerinden satış vergileri hesaplamak gerekiyorsa bir madde satış vergisi grubu seçin.  
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. Tahsilat mektubu gönderilmeden önce gereken minimum vadesi geçmiş bakiyeyi girin.
15. İzin vereceğiniz mehil süresi gün sayısını girin.
    * Bu, bir tahsilat mektubunun oluşturulabileceği son tarihten sonraki gün sayısıdır. Hesaplama için kullanılan vade tarihi, tahsilat mektubunun tahsilat mektubu sırasındaki konumuna bağlıdır:   ⦁    Tahsilat mektubu 1 için mehil süresi, faturadaki vade tarihine karşılık gelir.  ⦁ Tahsilat mektubu 2 ve sonraki tahsilat mektupları için mehil süresi, Alacak hesapları parametreleri sayfasının Tahsilat mektubu kodunu güncelleştir alanındaki seçime bağlı olarak, önceki tahsilat mektubunun deftere nakledildiği veya yazdırıldığı tarihe göre belirlenir.  
16. Sıradaki son tahsilat mektubunu eklemek için Ekle'ye tıklayın.
    * Bir tahsilat mektubu sırası için en fazla beş tahsilat mektubu kodu ekleyebilirsiniz.  
17. Tahsilat mektubu kodu alanında, sıradaki gönderilecek sonraki tahsilat mektubunu seçin.
18. Tanım alanına bir değer girin.
19. Ana hesap alanında istediğiniz değerleri belirtin.
20. Para birimi cinsinden ücret alanına bir sayı girin.
21. Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
22. Listede, seçili satırdaki bağlantıya tıklayın.
23. Minimum vadesi geçmiş bakiye alanına bir sayı girin.
24. Gün alanına bir sayı girin.
25. Müşterinin ek teslimat ve faturalamalarını durdurmak için bu onay kutusunu işaretleyin.
    * Hesap üzerindeki engeli kaldırmak için Müşteriler sayfasındaki Faturalama ve beklemedeki teslimat alanında Hayır seçeneğini belirleyin.  
26. Not hızlı sekmesini genişletin.
27. Seçili tahsilat mektubu kodu için tahsilat mektubunda görünecek metni girin.
    * Not kutusunun yukarısındaki Çeviriler menüsünü kullanarak bu metni birden fazla dile çevirebilirsiniz.  


