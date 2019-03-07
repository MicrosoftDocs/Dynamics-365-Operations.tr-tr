---
title: Satınalma siparişini yerine koyma için yerleşim yönergesi ayarlama
description: Bu yordam, bir basit konum yönergesini kurmayı göstermektedir.
author: ShylaThompson
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ca4b3c2598a268c065011daff31296521faa918
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "349090"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Satınalma siparişini yerine koyma için yerleşim yönergesi ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir basit konum yönergesini kurmayı göstermektedir. Gösterilen örnek, bir satınalma siparişi için alınan maddelerin yerleştirileceği yeri belirlemekte kullanılacak bir konum yönergesini oluşturmayı anlatmaktadır. Bu görev kılavuzunu belirtilen verilerle yürütmek için demo verileri şirketi USMF'yi kullanabilirsiniz. Ön koşullar: Değerlendirme kodu oluşturmanız gerekir. Bu yordamda yeniden etiketleme olarak adlandırılan bir değerlendirme kodunu kullanıyoruz. Kendi verinizde bir konum yönergesi oluşturuyorsanız, ambar ve maddeleriniz için gelişmiş ambar yönetimini ayarlamış olmanız gerekir.  Bu yordam ambar yöneticisi için hazırlanmıştır.

1. Ambar yönetimi > Kurulum > Konum yönergeleri öğesine gidin.
2. İş siparişi türü alanında "Satınalma siparişi"ni seçin.

## <a name="create-a-location-directive-header"></a>Bir konum yönergesi başlığı oluşturun
1. Yeni'ye tıklayın.
2. Sıra numarası alanına bir numara girin.
    * Bu, konum yönergesinin seçilen iş türü için işleme sırasıdır. Gerekirse sırada da değişiklik yapabilirsiniz.  
3. İsim alanına bir değer yazın.
    * Bu yönerge için benzersiz tanımlayıcıdır.  
4. İş türü alanında, 'Yerine koyma'yı seçin.
    * Yapılacak iş türünü seçin. İş siparişi türü satınalma siparişi ile yönergesi için Koymak desteklenen tek değeridir.  
5. Tesis alanına bir değer yazın.
6. Ambar alanına bir değer yazın.
    * Yönerge kodunu boş bırakın.  Yönergesi kodları için belirli bir yönerge türü yerine bir iş emri satırı bağlamak için kullanılır. Satınalma siparişleri için, İş şablonu belirlenmeden önce son iş sipariş satırının Yerine Koy türünün konum ve yerine çözümlenir. Bu yüzden iş şablonunun son satırını belirli bir yönergeye bağlamak mümkün değildir.   
7. Değerlendirme kodu alanına bir değer girin.
    * Ambar çalışanı bir mobil cihaz kullanarak madde kaydı sırasında belirli bu değeri girerse, konum yönergesi yalnızca kullanılmak üzere değerlendirme kodu konumu yönergesinin kullanımını sınırlar.  
8. Kaydet'e tıklayın.

## <a name="edit-the-query-for-directive"></a>Yönerge için sorguyu düzenleyin
1. Sorguyu düzenle'ye tıklayın.
    * Bu yönerge kullanımı halihazırda belirtilen değerlendirme kodu ile belirttiğiniz ambardaki kayıtlı öğeler için sınırlıdır. Bu sorguyu kullanarak başka sınırlamalar da ekleyebilirsiniz.  
2. Tamam'a tıklayın.

## <a name="add-directive-lines"></a>Yönerge satırları ekleyin
1. Yeni'ye tıklayın.
    * Bu, konum yönergesinin satırlarının seçilen iş türü için işleme sırasıdır. Gerekirse sırada da değişiklik yapabilirsiniz.  
2. Gönderen miktarı alanına bir sayı girin.
    * Bu yönerge satırı için geçerli olan en düşük miktar budur.  
3. Alıcı miktarı alanına bir sayı girin.
4. Birim alanına bir değer yazın.
    * Gönderici miktarı ve Alıcı miktarı birim olarak ifade edilir. Bu alanı boş bırakırsanız, maddenin sahip olduğu stok birimi kullanılır.  
5. Konum miktarı alanında, bir seçenek seçin.
    * Hiçbiri veya plaka miktarı: Her plaka üzerine kayıtlı miktar. Birimleştirilmiş miktar: Kayıt edilmiş olan tüm miktar. Kalan miktar: Satınalma siparişi satırından henüz kaydedilecek olan miktar. Beklenen Miktar: Satınalma siparişi satırında belirtilen toplam miktarı.  
6. Birim ile sınırlayın onay kutusunu işaretleyin veya işareti kaldırın.
    * Bu seçeneği seçerseniz ve birim sayfası üzerinde birimi ile sınırla belirtirseniz, yalnızca bu ölçüm birimine sahip maddelerin bir konuma koyabilirsiniz. Örneğin, ölçüm PL (palet) ise, sadece palet öğelerini belirtilen konuma koyabilirsiniz.  
7. Bölünmeye izin ver onay kutusunu işaretleyin veya işaretini kaldırın.
    * Miktarı birden çok konum arasında bölmek için yönergeye olanak sağlar.  
8. Kaydet'e tıklayın.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Yönergesi satırını belirli bir birime kısıtlayın
1. Birime göre kısıtla'ya tıklayın.
    * Bu düğme yalnızca birim ile sınırla onay kutusunu seçtikten Kaydet'e bastığınızda kullanılabilir hale gelir.  
2. Birim alanına bir değer yazın.
3. Sayfayı kapatın.

## <a name="add-a-location-directive-action-line"></a>Konum yönergesi eylem satırı ekleyin
1. Yeni'ye tıklayın.
    * Bu, konum yönergesinin eylem satırlarının seçilen iş türü için işleme sırasıdır. Gerekirse sırada da değişiklik yapabilirsiniz.  
2. İsim alanına bir değer yazın.
    * Bu yönerge eylemi için benzersiz tanımlayıcıdır.  
3. Sabit konum alanında, bir seçenek seçin.
    * Sabit ve sabit olmayan konumlar: Sabit konumda, sorguda belirtilen aralıkta ürünün kendi yanı sıra tüm sabit olmayan konumları geçerlidir.  Yalnızca sabit konumdaki ürün için: Sabit konumlarda ürünü için geçerli ve tüm ürün çeşitleri sabit konumlarda aynı kümeyi paylaşır. Yalnızca sabit ürün çeşitleri için konum: yalnızca her ürün çeşidi için belirtilen sabit konumlar geçerlidir.  
4. Strateji alanında, bir seçenek seçin.
    * Satınalma İş sipariş türleri aşağıdaki stratejileri destekler: Hiçbiri: Madde bulunan ilk konuma yerleştirilir. Birleştirme: Madde benzer öğelerin zaten mevcut olduğu bir konuma yerleştirilir. Boş olan ve hiçbir iş gelmeyen konum: Madde bulunan ilk boş konuma yerleştirilir. Konum ancak hiç fiziksel stoğu yoksa ve gelen iş beklenmiyorsa boş olarak değerlendirilir.  
5. Kaydet'e tıklayın.

## <a name="edit-the-query-for-directive-action-line"></a>Yönerge eylem satırı sorgusunu düzenleyin
1. Sorguyu düzenle'ye tıklayın.
2. Ekle öğesini tıklatın.
3. Konum alanına 'konum profil kimliği' yazın.
    * Bu örnekte, biz konum profil kimliği kullanarak olası yerler sınırlayacağız.  
4. Ölçütler alanına bir değer yazın.
5. Tamam'a tıklayın.
    * Ambarınızdaki tüm olası senaryoları elde edene kadar yönerge satırları ve yönerge eylemleri eklemeye devam edebilirsiniz.  

