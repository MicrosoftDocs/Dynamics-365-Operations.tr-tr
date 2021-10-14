---
title: Alınan maddeleri kaydetmek için bir mobil cihaz menü öğesi ayarlama
description: Bu konu, bir mobil cihaz menü öğesinin ayarlanmasına odaklanır.
author: Mirzaab
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 410a70294e5a417950ed5332ec5fdd7da321a31d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565171"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Alınan maddeleri kaydetmek için bir mobil cihaz menü öğesi ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu, bir mobil cihaz menü öğesinin ayarlanmasına odaklanır. Bu menü öğesi, satınalma siparişleri üzerinden sipariş edilen ürünlerin giriş kaydı için kullanılır. 

Bu kılavuzu USMF demo şirketinde kullanabilirsiniz. Bu yordam ambar yöneticisi için hazırlanmıştır.


## <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma
1. Gezinti bölmesinde, **Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü öğeleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Menü öğesi adı** alanına bir değer girin. Bu, mobil cihaz menü öğesinin benzersiz tanımlayıcısıdır. Örneğin, `My PO registration` yazabilirsiniz.  
4. **Başlık** alanına bir değer yazın. Bu, mobil cihazdaki kullanıcıda görüntülenen başlıktır. Örneğin, `PO registration` yazabilirsiniz.  
5. **Mod** alanında, **İş**'i seçin. Bir satınalma siparişi satırı için alınan eldeki miktarın kaydı ürünlerin alandan alınıp stoğa taşınması için iş oluşturur. Ürünler kaydedilene kadar iş oluşturulmaz. Bu nedenle, **Mevcut işi kullan** seçeneğini **Hayır** olarak bırakın.
6. **Genel** bölümünün **İş oluşturma işlemi** alanında, **Satınalma siparişi ürün teslim alma** öğesini seçin.
    - Bir satınalma siparişi satırı, eldeki stok ambarda kaydedilmeden önce benzersiz bir şekilde tanımlanmalıdır. Bu senaryoda, mobil cihaz satın alma sipariş numarasını ve ürün numarası kaydeder ve böylece sistemin SAS satırını tanımlaması sağlanır. Yerine koyma işi oluşturulur ve malzeme başka bir çalışan tarafından çekilebilir. Seçtiğiniz iş oluşturma yöntemi, **Genel** hızlı sekmesinde hangi alanların kullanılabilir olacağını belirler.  
    - **Varsayılan verileri kullan** seçeneğini belirlerseniz, **Varsayılan veri** düğmesi etkinleştirilir. Burada, bir çalışanın bu değerlerin mobil cihazlarında görünmesi için günlük işlerinde ihtiyaç duydukları verileri görüntüleyeceği alanları seçebilirsiniz.  
    - **Plaka gruplandırma** parametresi, alınmakta olan ürüne atanan sıra grubuyla birlikte çalışır. Bir paletten azının veya fazlasının tek bir plakada gruplanması gerekip gerekmediğini veya her bir ürün için ayrı bir plakaya bölünmesi gerekip gerekmediğini belirtebilirsiniz.  
    - **Plaka oluştur** seçeneğini belirlerseniz, numara sırası temel alınarak benzersiz bir plaka oluşturulur.  
    - İş oluşturulduğunda kullanılacak şablonu seçebilirsiniz. Örneğin, bir satınalma siparişi için bir ürün kaydederseniz, yerine koyma işi iş şablonuna dayalı olarak oluşturulur. Bir iş şablonu seçmezseniz, sistem şablonlar ile ilişkili olan sorgu ölçütlerini temel alan bir şablon atayacaktır.  
    - Mobil cihazda değerlendirme kodu görüntülenirse, çalışanlar ürünlerin durumunu veya kalitesini değerlendirebilir ve uygun kodu seçebilir. Değerlendirme kodundaki kurallar ürünlerin diğer ambar süreçlerinde kullanılıp kullanılamayacağını belirler. Kurallar oluşturulan iş için kullanılacak yerleşim yönergesini de belirler.   
    - **Toplu iş değerlendirme kodları** seçeneğini belirlerseniz, çalışanlar bir toplu işin durumunu veya kalitesini değerlendirebilir ve uygun değerlendirme kodunu seçebilir. Toplu iş değerlendirme kodunda belirlenen kurallar toplu işin diğer ambar süreçlerinde kullanılıp kullanılamayacağını belirler.  
    - **Etiketleri yazdır** seçeneğini belirlerseniz, ürünler alındığında bir plaka etiketi otomatik olarak yazdırılır.  
7. **Kaydet**'i seçin.
8. Sayfayı kapatın.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Mobil cihaz menüsüne menü öğesi ekleme
1. Gezinti bölmesinde, **Modüller > Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menü öğeleri**'ne gidin.
2. **Ad** alanına bir `inbound` değeriyle filtre uygulamak için **Hızlı Filtre**'yi kullanın.
3. **Düzenle** öğesini seçin.
4. Kullanılabilir menüler ve öğeler ağacında önceden oluşturduğunuz bir menü öğesini seçin.
5. Sağ tarafı gösteren oku seçin.
6. **Kaydet**'i seçin.
7. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]