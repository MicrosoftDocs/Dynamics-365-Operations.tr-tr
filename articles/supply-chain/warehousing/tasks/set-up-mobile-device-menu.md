---
title: Satınalma siparişi iş türünü tamamlamak için bir mobil cihaz menü öğesi ayarlama
description: Bu konu bir Mobil cihaz menü öğesinin nasıl kurulacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 905094ae4e76fadbebea1892ec20427f32e3e71d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216839"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Satınalma siparişi iş türünü tamamlamak için bir mobil cihaz menü öğesi ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu bir Mobil cihaz menü öğesinin nasıl kurulacağını gösterir. Bu örnekte, menü öğesi Satın alma siparişi türünde işi yapan için kullanılır. Menü öğesiyle ilişkili iş sınıfı, hangi işin geçerli olduğunu belirler. Bu kılavuzu USMF demo şirketinde kullanabilirsiniz. Bu yordam genel olarak bir depo yöneticisi tarafından yerine getirilir.


## <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma
1. **Mobil cihaz menüsü öğelerine** arama çubuğuna girerek gidin.
2. **Yeni**'yi seçin.
3. **Menü öğesi adı** alanına bir değer girin. Özgün bir değer girin. Örneğin, `POMove` yazabilirsiniz. Değeri unutmayın, daha sonra ihtiyacınız olacak.  
4. **Başlık** alanına bir değer yazın. Bu, mobil cihazda görüntülenen başlıktır. Örneğin, `PO Move` yazabilirsiniz.  
5. **Mod** alanında, **İş**'i seçin.
6. **Mevcut işi kullan** alanında **Evet**'i seçin.
    - Bu mobil cihaz menü öğesi varolan işi gerçekleştirmek için kullanılır. Bu nedenle, bu değeri **Evet** olarak ayarlamanız gerekir.  
    - **Stok durumunu görüntüle** alanı eldeki stoğun stok durumunun mobil cihazda ambar çalışanına görüntülenip görüntülenmeyeceğini belirler.  
7. **Yöneten** alanında **Sistem gruplandırma** öğesini seçin. **Yöneten** alanında bir seçim yaptığınızda, bu sayfadaki **Genel** bölümünde ek alanlar belirir. Beliren alanlar yaptığınız seçime bağlıdır. **Sistem gruplaması** seçtiğinizde iki yeni alan eklenir. Bunlar aşağıda açıklanmıştır.  
8. **Sistem gruplama** alanında **WorkPoolId** öğesini seçin. Ambar çalışanları bu menü öğesini açtıklarında bir İş havuzu kodunu taramaları istenir. Bu İş havuzu koduna sahip tüm iş emirleri ve bu menü öğesine eklenen iş sınıflarından birinin bulunduğu açık iş emri satırları kullanıcıya gönderilir.  
9. **Sistem gruplandırma etiketi** alanında bir değer girin. Bu, mobil cihazda kullanıcıya görüntülenen metindir. Örneğin, **İş havuzu** yazabilirsiniz.  
10. **Yerine koyma sırasında plakayı geçersiz kıl** için **Evet**'i seçin. Bu seçenek maddeler plaka denetimli bir yerleşime bırakıldığında ambar çalışanlarının hedef plakayı geçersiz kılmalarına olanak tanır.  
11. **Grup yerine koyma** alanında **Evet**'i seçin.
    - İş emrindeki tüm Yerine koyma satırları aynı yerleşimi paylaşıyorsa kullanıcı tüm satırlar için birleştirilmiş tek bir Yerine koy yönergesi alır. 
    - Denetim şablonu kodu: İş denetimi şablonu bir menü öğesinin iş sürecinin başka bir işlem gerçekleştirebilmek üzere kesilip kesilmeyeceğini belirtmenize olanak tanır. Örneğin, bu menü öğesi gelen iş içinse, denetim şablonu çalışanın sıcaklığı denetlemesini gerektirebilir. Sürecin kesintiye uğradığı nokta denetim şablonunda belirtilir ve örneğin, iş başladığında veya tamamlandığında veya durumu değiştiğinde.  
12. **İş sınıfları** bölümünü genişletin.
13. **Yeni**'yi seçin.
14. **İş sınıfı kodu** alanında `Purchase` değerini girin. İş havuzu menü öğesinin kullanılabileceği işi kısıtlar. Bu durumda, Satınalma iş sınıfı koduna sahip iş emri satırlarını açmak için kullanılır.  
15. **Kaydet**'i seçin.

## <a name="set-up-work-confirmation"></a>İş onayı kurulumu
1. **İş onayı kurulumu** seçin.
2. **İş türü** alanında **Malzeme çekme** öğesini seçin.
3. **Otomatik onayla** onay kutusunu işaretleyin. Çekme iş türüne sahip çalışma yönergesi otomatik olarak onaylanır. Bu yönerge kullanıcıya sunulmaz.  
4. **Yeni**'yi seçin.
5. **İş türü** alanında, 'Yerine koyma'yı seçin.
6. **Konum onayı onay kutusunu** işaretleyin. Madde bırakıldığında ambar çalışanından yerleşim için bir onay taraması gerçekleştirmesi istenir.  
7. **Kaydet**'i seçin.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Mobil cihaz menüsüne menü öğesi ekleme
1. **Mobil cihaz** menüsü arama çubuğuna girerek gidin.
2. **Düzenle** öğesini seçin.
3. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **İsim** alanı üzerinde **gelen** değerini girerek filtreleme yapın. Gelen menü öğeleri için kullandığınız menüyü bulmak istiyorsunuz. USMF'de bu **Gelen** olarak adlandırılır.  
4. Ağaçta, **bir değer** seçin.
5. Sağ tarafı gösteren oku seçin.
6. **Kaydet**'i seçin.
7. Sayfayı kapatın.
