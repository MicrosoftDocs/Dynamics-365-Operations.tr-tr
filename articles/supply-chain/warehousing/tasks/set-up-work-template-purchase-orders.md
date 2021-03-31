---
title: Satın alma siparişleri için iş şablonunu ayarlama
description: Bu konu, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağını açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe0b6f9b966a5ce31af9da74a2038877debd2e7c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215757"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Satın alma siparişleri için iş şablonunu ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağını açıklar. İş şablonları, ürünler teslim alma alanından taşınırken bir mobil cihazda ambara yönelik yönergeler kümesini belirler. Bu yordamı, USMF demo verileri şirketinde söz edilen verilerle kullanabilirsiniz. Bu kılavuzu başlatmadan önce bir iş havuzu kodu oluşturun. Bu örnekte Gelen içinde bir iş havuzu kodu kullanılır. Bu yordam ambar yöneticisi için hazırlanmıştır.

1. Gezinti bölmesinde **Modüller > Ambar yönetimi > Kurulum > İş > İş şablonları**'na gidin.
2. **İş siparişi türü** alanında **Satınalma siparişi**'ni seçin.

## <a name="create-a-work-template-header"></a>İş şablonu başlığı oluşturma
1. **Yeni**'yi seçin.
2. **Sıra numarası** alanına bir numara girin. Bu, iş şablonlarının değerlendirileceği sıradır. Gerekirse sırada değişiklik yapabilirsiniz.  
3. **İş şablonu** alanında bir değer girin. Bu, şablon için benzersiz tanımlayıcıdır.  
4. **İş şablonu açıklaması** alanında bir değer girin.
    - **Geçerli** seçeneği, şablon için gereken tüm bilgiler tamamlanana ve sonra **Kaydet** seçilene kadar işaretlenmez.  
    - **Satınalma siparişi** türünün iş emri otomatik olarak işlenemez, bu nedenle **Otomatik olarak işleme koy** seçenek kümesini **Hayır** olarak bırakın.  
5. **İş havuzu kodu** alanında bir değer girin. İş havuzu kodları, işi gruplar halinde düzenlemenizi sağlar. Burada belirlediğiniz değer, bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olacaktır.  
6. **İş önceliği** alanında `1` değerini girin. Bu, işin önemini gösterir ve burada belirlediğiniz değer bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olur.  
7. **Kaydet**'i seçin. **Sorguyu Düzenle** düğmesi kullanılabilir olmadan önce iş şablonu başlığını kaydetmeniz gerekir.  

## <a name="set-up-the-query-for-the-work-template"></a>İş şablonu sorgusunu ayarlama
1. **Sorguyu düzenle**'yi seçin. Şablonun yalnızca belirli bir ambarın içinde kullanılabileceği şekilde bir sınırlama ayarlanır.  
2. **Ekle**'yi seçin.
3. Yeni satırın **Alan** alanında, `warehouse` yazın.
4. **Ölçütler** alanına bir değer yazın.
5. **Tamam**'ı seçin.
6. **Evet**'i seçin.

## <a name="set-work-template-details"></a>İş şablonu ayrıntılarını ayarlama
1. **Yeni**'yi seçin.
2. **İş türü** alanında **Malzeme çekme** öğesini seçin.
3. **İş sınıfı kodu** alanında `purchase` değerini girin. Burada ayarladığınız çalışma sınıfı, bu şablon kullanılarak oluşturulan Malzeme çekme türündeki tüm iş satırlarında varsayılan olacaktır. İş sınıfı, iş siparişi satırlarından değiştirilemez. İş sınıfları, ambar çalışanı tarafından bir mobil cihazda işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.  
4. **Yeni**'yi seçin.
5. **İş türü** alanında, **Yerine koyma**'yı seçin.
6. **İş sınıfı kodu** alanında bir değer girin. Malzeme çekme ve yerine koyma yönergeleri bir kümedir. Her bir malzeme çekme/yerine koyma çifti aynı iş sınıfında olmalıdır. Malzeme çekme yönergesi için sağladığınız aynı iş sınıfını kullanın.  
7. **Kaydet**'i seçin. **Geçerli** onay kutusunun işaretli olduğundan emin olun.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]