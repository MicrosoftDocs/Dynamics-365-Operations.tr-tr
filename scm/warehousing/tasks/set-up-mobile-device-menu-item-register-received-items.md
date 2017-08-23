--- 
title: "Alınan maddeleri kaydetmek için bir mobil cihaz menü öğesi ayarlama"
description: "Bu görev, bir mobil cihaz menü öğesinin ayarlanmasına odaklanır."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 642e2b05c9f9a59f6b47a22f3d92f2f6ae245039
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Alınan maddeleri kaydetmek için bir mobil cihaz menü öğesi ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev, bir mobil cihaz menü öğesinin ayarlanmasına odaklanır. Bu menü öğesi, satınalma siparişleri üzerinden sipariş edilen ürünlerin giriş kaydı için kullanılır. 

Bu kılavuzu USMF demo şirketinde kullanabilirsiniz. Bu yordam ambar yöneticisi için hazırlanmıştır.


## <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma
1. Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğeleri seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Menü öğesi adı alanına bir değer girin.
    * Bu, mobil cihaz menü öğesinin benzersiz tanımlayıcısıdır. Örneğin, 'SAS kaydım' yazabilirsiniz.  
4. Başlık alanına bir değer yazın.
    * Bu, mobil cihazdaki kullanıcıda görüntülenen başlıktır. Örneğin, 'SAS kaydı' yazabilirsiniz.  
5. Mod alanında, 'İş' seçin.
    * Bir satınalma siparişi satırı için alınan eldeki miktarın kaydı ürünlerin alandan alınıp stoğa taşınması için iş oluşturur. Ürünler kaydedilene kadar iş oluşturulmaz.  Bu nedenle, Mevcut iş seçeneğini kullan öğesini Hayır olarak bırakın.  
6. Genel bölümünü genişletin veya daraltın.
7. İş oluşturma işlemi alanında, 'Satınalma siparişi ürün teslim alma' öğesini seçin.
    * Bir satınalma siparişi satırı, eldeki stok ambarda kaydedilmeden önce benzersiz bir şekilde tanımlanmalıdır. Bu senaryoda, mobil cihaz satın alma sipariş numarasını ve ürün numarası kaydeder ve böylece sistemin SAS satırını tanımlaması sağlanır. Yerine koyma işi oluşturulur ve malzeme başka bir çalışan tarafından çekilebilir.    Seçtiğiniz iş oluşturma yöntemi, Genel hızlı sekmesinde hangi alanların kullanılabilir olacağını belirler.  
    * Varsayılan verileri kullan seçeneğini belirlerseniz, Varsayılan veri düğmesi etkinleştirilir. Burada, bir çalışanın bu değerlerin mobil cihazlarında görünmesi için günlük işlerinde ihtiyaç duydukları verileri görüntüleyeceği alanları seçebilirsiniz.  
    * Plaka gruplandırma parametresi, alınmakta olan ürüne atanan sıra grubuyla birlikte çalışır. Bir paletten azının veya fazlasının tek bir plakada gruplanması gerekip gerekmediğini veya her bir ürün için ayrı bir plakaya bölünmesi gerekip gerekmediğini belirtebilirsiniz.  
    * Plaka oluştur seçeneğini belirlerseniz, numara sırası temel alınarak benzersiz bir plaka oluşturulur.   
    * İş oluşturulduğunda kullanılacak şablonu seçebilirsiniz. Örneğin, bir satınalma siparişi için bir ürün kaydederseniz, yerine koyma işi iş şablonuna dayalı olarak oluşturulur. Bir iş şablonu seçmezseniz, sistem şablonlar ile ilişkili olan sorgu ölçütlerini temel alan bir şablon atayacaktır.  
    * Mobil cihazda değerlendirme kodu görüntülenirse, çalışanlar ürünlerin durumunu veya kalitesini değerlendirebilir ve uygun kodu seçebilir. Değerlendirme kodundaki kurallar ürünlerin diğer ambar süreçlerinde kullanılıp kullanılamayacağını belirler. Kurallar oluşturulan iş için kullanılacak yerleşim yönergesini de belirler.   
    * Toplu iş değerlendirme kodları seçeneğini belirlerseniz, çalışanlar bir toplu işin durumunu veya kalitesini değerlendirebilir ve uygun değerlendirme kodunu seçebilir.  Toplu iş değerlendirme kodunda belirlenen kurallar toplu işin diğer ambar süreçlerinde kullanılıp kullanılamayacağını belirler.  
    * Etiketleri yazdır seçeneğini belirlerseniz, ürünler alındığında bir plaka etiketi otomatik olarak yazdırılır.  
8. Kaydet'e tıklayın.
9. Sayfayı kapatın.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Mobil cihaz menüsüne menü öğesi ekleme
1. Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğesine gidin.
2. Ad alanında bir 'gelen' değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.
3. Düzenle'yi tıklatın.
4. Ağaçta, 'Kullanılabilir menü ve ürünler ağacında önceden oluşturduğunuz bir menü öğesini seçin' öğesini seçin.
    * Daha önce oluşturduğunuz bir menü öğesini seçin.  
5. Sağ tarafı gösteren oku tıklatın.
6. Kaydet'e tıklayın.
7. Sayfayı kapatın.


