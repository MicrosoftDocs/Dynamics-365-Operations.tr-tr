--- 
title: "Satınalma siparişleri için iş şablonunu ayarlama"
description: "Bu yordam, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağına odaklanır."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Satınalma siparişleri için iş şablonunu ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağına odaklanır. İş şablonları, ürünler teslim alma alanından taşınırken bir mobil cihazda ambara yönelik yönergeler kümesini belirler. Bu yordamı, USMF demo verileri şirketinde söz edilen verilerle kullanabilirsiniz. Bu kılavuzu başlatmadan önce bir iş havuzu kodu oluşturun. Bu örnekte Gelen içinde bir iş havuzu kodu kullanılır. Bu yordam ambar yöneticisi için hazırlanmıştır.

1. Ambar yönetimi > Kurulum > İş > İş şablonları öğesine gidin.
2. İş siparişi türü alanında "Satınalma siparişi"ni seçin.

## <a name="create-a-work-template-header"></a>İş şablonu başlığı oluşturma
1. Yeni'ye tıklayın.
2. Sıra numarası alanına bir numara girin.
    * Bu, iş şablonlarının değerlendirileceği sıradır. Gerekirse sırada değişiklik yapabilirsiniz.  
3. İş şablonu alanında bir değer girin.
    * Bu, şablon için benzersiz tanımlayıcıdır.  
4. İş şablonu açıklaması alanında bir değer girin.
    * Geçerli seçeneği, şablon için gereken tüm bilgiler tamamlanana ve sonra Kaydet tıklatılana kadar işaretlenmez.  
    * Satınalma siparişi türünün iş emri otomatik olarak işlenemez, bu nedenle Otomatik olarak işleme koy seçeneğini Hayır olarak bırakın.  
5. İş havuzu kodu alanında bir değer girin.
    * İş havuzu kodları, işi gruplar halinde düzenlemenizi sağlar. Burada belirlediğiniz değer, bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olacaktır.  
6. İş önceliği alanında '1' değerini girin.
    * Bu, işin önemini gösterir ve burada belirlediğiniz değer bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olur.  
7. Kaydet'e tıklayın.
    * Sorguyu Düzenle düğmesi kullanılabilir olmadan önce iş şablonu başlığını kaydetmeniz gerekir.  

## <a name="set-up-the-query-for-the-work-template"></a>İş şablonu sorgusunu ayarlama
1. Sorguyu düzenle'ye tıklayın.
    * Şablonun yalnızca belirli bir ambarın içinde kullanılabileceği şekilde bir sınırlama ayarlanır.  
2. Ekle öğesini tıklatın.
3. Listede, seçili satırı işaretleyin.
4. Alan alanında 'ambar' değerini girin.
5. Ölçütler alanına bir değer yazın.
6. Tamam'a tıklayın.
7. Evet'i tıklatın.

## <a name="set-work-template-details"></a>İş şablonu ayrıntılarını ayarlama
1. Yeni'ye tıklayın.
2. İş türü alanında 'Malzeme çekme öğesini seçin.
3. İş sınıfı kodu alanında 'satınalma' değerini girin.
    * Burada ayarladığınız çalışma sınıfı, bu şablon kullanılarak oluşturulan Malzeme çekme türündeki tüm iş satırlarında varsayılan olacaktır. İş sınıfı, iş siparişi satırlarından değiştirilemez. İş sınıfları, ambar çalışanı tarafından bir mobil cihazda işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.  
4. Yeni'ye tıklayın.
5. İş türü alanında, 'Yerine koyma'yı seçin.
6. İş sınıfı kodu alanında bir değer girin.
    * Malzeme çekme ve yerine koyma yönergeleri bir kümedir. Her bir malzeme çekme/yerine koyma çifti aynı iş sınıfında olmalıdır. Malzeme çekme yönergesi için sağladığınız aynı iş sınıfını kullanın.  
7. Kaydet'e tıklayın.
    * Geçerli onay kutusunun işaretli olduğundan emin olun.  


