---
title: Tahsilat mektubu sırası oluşturma
description: Tahsilat mektubu sırası oluşturmak için bu görev kılavuzunu kullanın.
author: mikefalkner
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03f76f6539e8f318b75c8ec8f53020eb7052ec45
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137934"
---
# <a name="create-a-collection-letter-sequence"></a>Tahsilat mektubu sırası oluşturma

[!include [banner](../../includes/banner.md)]

Tahsilat mektubu sırası oluşturmak için bu görev kılavuzunu kullanın. Bu görevde USMF demo şirketi kullanılmaktadır.

1. Gezinti bölmesinde **Modüller > Alacak ve tahsilatlar > Kurulum > Tahsilat mektubu sırasını ayarla**'ya gidin.
2. **Yeni**'ye tıklayın.
3. **Tahsilat mektubu sırası** alanında, sırayı temsil edecek bir sıra kodu girin. Bir deftere nakil profili ayarladığınız zaman kullanılır.
4. **Tanım** alanına bir değer girin.  Ödeme şartları isteğe bağlıdır. Buraya bir değer girerseniz, tahsilat mektubu ücreti faturasında, müşteriyle depolanan ödeme şartları yerine bu ödeme şartları kullanılır.  
5. **Tahsilat mektubu kodu** alanında, göndermek istediğiniz ilk tahsilat mektubunun kodunu seçin. İlk tahsilat mektubu, faturadaki vade tarihine, bu satırdaki Gün alanında mehil süresi için girdiğiniz değere ve bu satıra girdiğiniz diğer bilgilere göre oluşturulur.  
6. **Tanım** alanına bir değer girin. Ücretin para birimi, müşteri para biriminin varsayılan değeri olur. Bu para birimi kodu, fatura para biriminden farklı olabilir.  
7. Sırada gönderilecek sonraki tahsilat mektubunu eklemek için **Ekle**'ye tıklayın. Çoğu durumda, ilk tahsilat mektubu yalnızca bir uyarıdır. Gerekirse ücretler ekleyebilirsiniz.  
8. Tahsilat mektubu kodu alanında, sıradaki gönderilecek sonraki tahsilat mektubunu seçin.
9. **Tanım** alanına bir değer girin.
10. **Ana hesap** alanında, ücretler için kullanılacak gelir hesabını seçin.
11. Bu tahsilat mektubu deftere nakledilince yansıtılacak ücreti girin.
12. **Madde Satış vergisi grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın. Ücret üzerinden satış vergileri hesaplamak gerekiyorsa bir madde satış vergisi grubu seçin.  
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. **Minimum vadesi geçmiş bakiye** alanında tahsilat mektubu gönderilmeden önce gereken minimum vade tarihi bakiyesini girin.
15. **Günler** alanına izin vereceğiniz mehil süresi gün sayısını girin. Bu, bir tahsilat mektubunun oluşturulabileceği son tarihten sonraki gün sayısıdır. Hesaplama için kullanılan vade tarihi, tahsilat mektubunun tahsilat mektubu sırasındaki yerine bağlıdır:
    - Tahsilat mektubu 1'in mehil süresi, faturadaki vade tarihine göre belirlenir.
    - Tahsilat mektubu 2 ve sonraki tahsilat mektupları için mehil süresi, Alacak hesapları parametreleri sayfasının Tahsilat mektubu kodunu güncelleştir alanındaki seçime bağlı olarak, önceki tahsilat mektubunun deftere nakledildiği veya yazdırıldığı tarihe göre belirlenir.  
16. Sıradaki son tahsilat mektubunu eklemek için **Ekle**'ye tıklayın. Bir tahsilat mektubu sırası için en fazla beş tahsilat mektubu kodu ekleyebilirsiniz.  
17. **Tahsilat mektubu kodu** alanında, sıradaki gönderilecek sonraki tahsilat mektubunu seçin.
18. **Tanım** alanına bir değer girin.
19. **Ana hesap** alanında istediğiniz değerleri belirtin.
20. **Para birimi cinsinden ücret**' alanına bir sayı girin.
21. **Madde Satış vergisi grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
22. Listede, seçili satırdaki bağlantıya tıklayın.
23. **Minimum vadesi geçmiş bakiye** alanına bir sayı girin.
24. **Günler** alanına bir sayı girin.
25. Müşterinin ek teslimat ve faturalamalarını durdurmak için **Engelle** onay kutusunu işaretleyin. Hesap üzerindeki engeli kaldırmak için Müşteriler sayfasındaki Faturalama ve beklemedeki teslimat alanında **Hayır** seçeneğini seçin.  
26. **Not** hızlı sekmesini genişletin.
27. Seçili tahsilat mektubu kodu için tahsilat mektubunda görünecek metni girin. Not kutusunun yukarısındaki Çeviriler menüsünü kullanarak bu metni birden fazla dile çevirebilirsiniz.  

