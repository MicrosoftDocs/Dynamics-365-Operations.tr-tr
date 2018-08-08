---
title: "Üretim talebine bağlı olarak konsinye stok sahipliğini değiştirme"
description: "Bu yordam üretimde stok için bir talep olduğunda, konsinye stoğun sahibini satıcıdan tüzel kişiliğinize değiştirmeyi gösterir."
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5925f5423d596adc4326dfff4734de2afd80b5a8
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Üretim talebine bağlı olarak konsinye stok sahipliğini değiştirme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam üretimde stok için bir talep olduğunda, konsinye stoğun sahibini satıcıdan tüzel kişiliğinize değiştirmeyi gösterir. Bu sahiplik değişikliği bir stok sahipliği değişiklik günlüğü oluşturup bunu deftere naklederek yapılır. Sahiplik değişikliği günlük satırları el ile veya bu kayıtta gösterildiği gibi, var olan üretim talebine göre oluşturulabilir. Genellikle, bu görevi bir atölye gözetmeni gerçekleştirir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Kendi verilerinizi kullanıyorsanız şu önkoşullara sahip olduğunuzdan emin olun: stok sahibi değişikliği için ayarlanmış bir stok günlüğü adı, fiziksel olarak kaydedilmiş satıcıya ait eldeki maddeler ve malzeme için bir veya daha fazla üretim emri satırı. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="create-an-inventory-ownership-journal"></a>Stok sahipliği günlüğü oluşturma
1. Stok yönetimi > Günlük girişleri > Maddeler > Stok sahipliği değişikliği'ne gidin.
2. Yeni'ye tıklayın.
    * Stok sahipliği değişiklik günlüğü konsinye stoğun sahibini satıcıdan geçerli tüzel kişiliğe değiştirmek için kullanılır. Bu sahiplik değişikliği, satıcının sahibi olduğu eldeki stoğu serbest bırakıp bu stoğu geçerli tüzel kişilik tarafına alarak gerçekleştirilir.  
3. Ad alanına bir değer girin veya buradan bir değer seçin.
    * Yalnızca Sahiplik değişikliği günlük türüne sahip stok günlüğü adlarını seçebilirsiniz.  
4. Tamam'a tıklayın.
5. İşlevler'i tıklatın.
6. Üretim emirlerinden günlük satırları oluştur öğesine tıklayın.
    * Sahipliği değiştirme işlemine hammaddenin tüketimi için talebi olan tüm üretim satırlarını sorgulayarak başlayabilirsiniz.  
7. Eklenecek stok sorunu durumları alanında bir seçenek belirleyin.
    * Bu seçenek, stok hareketlerinin çıkış durumuna göre filtre uygulamanıza olanak tanır. Örneğin, Malzeme çekildi ve Rezerve fiziksel durumlarına sahip stok için günlük satırları oluşturabilirsiniz.  
8. Eklenecek kayıtlar bölümünü genişletin.
    * Bu bölüm daha fazla filtre uygulamanıza olanak tanır. Örneğin, belirli bir hammadde tarihi seçebilirsiniz.  
9. Tamam'a tıklayın.

## <a name="post-the-inventory-ownership-change-journal"></a>Stok sahipliği değişikliği günlüğünü deftere nakletme
1. Deftere Naklet öğesine tıklayın.
    * Günlük deftere nakledildiğinde, satıcıya ait stok bir "Sahiplik değişikliği" referansı kullanılarak yayımlanır. Daha sonra stok satınalma siparişi ürün girişi ile güncelleştirilen bir stok hareket kullanılarak elde olarak alınır. Yalnızca deftere nakledilen günlükle ilgili hareketlerin oluşturulduğuna dikkat edin. Beklenen stok hareketleri oluşturulmaz.  
2. Tamam'a tıklayın.
3. Sayfayı kapatın.

