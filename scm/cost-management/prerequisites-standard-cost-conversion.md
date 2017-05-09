---
title: "Standart maliyet dönüştürme için önkoşullar"
description: "Bu konuda, standart maliyet dönüştürme yapmadan önce gerçekleştirilecek görevler açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 562572f45dd78fb5655466e20a0c09b125c74d39
ms.lasthandoff: 03/31/2017


---

# <a name="prerequisites-for-a-standard-cost-conversion"></a>Standart maliyet dönüştürme için önkoşullar

[!include[banner](../includes/banner.md)]


Bu konuda, standart maliyet dönüştürme yapmadan önce gerçekleştirilecek görevler açıklanmaktadır. 

Standart bir maliyet dönüştürmesi yapmadan önce, şu adımları izleyin:

1.  Standart maliyetler için bir **madde model grubu** tanımlayın. Standart bir maliyet stok modeli kullanarak bir madde model grubu oluşturmak için Madde model grupları sayfasını kullanın. Standart bir maliyet dönüştürme ayarlarken, dönüştürülen maddelere bu madde model grubunu atarsınız.
2.  Her bir maddeye bir **maliyet grubu** atayın.
    -   Satın alınan bir maddeye atanan maliyet grubu, standart maliyetlerle ilişkili atanan genel muhasebe hesaplarına temel oluşturabilir. Bu, satınalma fiyatı değişikliklerine yönelik atanan genel muhasebe hesaplarını içerebilir. Bir üretim ortamında, satın alınmış bileşenlere atanan maliyet grubu aynı zamanda üretilmiş bir maddenin hesaplanmış maliyetleri için de bir maliyet segmentasyonu sağlamaktadır.
    -   Bir üretilmiş maddeye atanan maliyet grubu, üretim farkları için genel muhasebe hesapları atanması gibi, standart maliyetlerle ilişkili genel muhasebe hesapları atamanın temelini oluşturabilir.

3.  Sabit maliyetlere sahipken, üretilmiş bir maddeye bir **standart sipariş miktarı** atayın. Üretilmiş bir maddeye yönelik standart sipariş emri miktarı, itfalı veya eşit dağıtılmış, sabit maliyetler için muhasebe lot boyutu işlevi görebilir. Bunlar, rota operasyonlarındaki kurulum sürelerini veya bir ürün reçetesindeki sabit bileşen miktarını içerebilir.
4.  Özellikle yeniden değerleme farkı olmak üzere, standart maliyetlerle ilişkili **genel muhasebe hesapları** atayın. **Deftere nakil** sayfasını (**Stok yönetimi** &gt; **Kurulum**) kullanarak standart maliyetlerle ilgili genel muhasebe hesapları atayın. Standart maliyet dönüştürme işleminde bir minimum değer olarak, tüm maddelere ve tüm maliyet gruplarına ait yeniden değerleme farkı hesabını atamanız gerekir. Standart maliyetler için gerekli olacak genel muhasebe hesaplarını tanımlamak üzere **Hesap planı** sayfasını kullanın. Stok nakil kuralları tanımlamadan önce maliyet ilişkilerini (tablolar, gruplar ve tümü için) etkinleştirmek için **Hareket birleşimleri** sayfasını kullanın.
5.  Standart maliyetlerle ilişkili stok parametreleri tanımlayın. Yeniden değerleme fişlerine bir numara serisi atamak için **Stok ve ambar yönetimi parametreleri** sayfasındaki **Numara serileri** sekmesini kullanın. Bir yeniden değerleme günlüğü, standart maliyet dönüştürmesi maddenin stok değerinde bir değişiklik yarattığında üretilir. Standart maliyetle ilişkili iki parametre tanımlamak üzere Maliyet Kontrol parametreleri tanımlamak için (**Stok muhasebesi** sekmesinde) **Stok ve ambar yönetimi parametreleri** sayfasını kullanın.
    -   Genel muhasebe yok veya Alt genel muhasebe'yi seçmek için **Maliyet dökümü** alanını kullanın. Alt genel muhasebe seçimi, aktif maliyet dökümü olarak adlandırılır. Aktif maliyet dökümü, standart maliyet maddeleri için çok düzeyli bir ürün yapısı üzerinde maliyet grubu segmentasyonunun hesaplanması, sürdürülmesi ve görüntülenmesi için çok önemlidir. Maliyet dökümü aktifken, aşağıdakini tek düzeyli, çok düzeyli veya toplam formatta rapor edebilir ve analiz edebilirsiniz:
        1.  Stok
        2.  Süren iş (WIP)
        3.  Maliyet grubuna göre satılan malların maliyeti

        Aktif maliyet dökümü, üretilen bir öğenin maliyetini etkinleştirmeniz halinde, sonucun maddenin maliyet kaydında maliyet grubu segmentinde saklanacağı anlamına gelir. **Maliyet dökümü** alanına hiç değer girmezseniz, standart maliyet maddeleri için maliyet grubu segmenti sürdürülmeyecektir. Yani, üretilen bir maddenin standart maliyeti maliyet grubu segmentasyonu olmadan tek bir tutar gibi hesaplanır ve sürdürülür ve üretilen bileşenlerin maliyet katkıları tek bir tutarda toplanır.
    -   Özetlenmiş veya maliyet grubu başına seçeneğini belirlemek için **Standarttan farklar** alanını kullanın. Maliyet grubu başına seçimi, satınalma fiyatı farklarını ve üretim farklarını maliyet grubuna göre tanımanıza olanak sağlar. Bu ayrıca dört tip üretim farkını (lot boyutu, miktar, fiyat ve değer değiştirme farkları) tanımanıza da olanak sağlar. Özetlenmiş seçimi, farkları maliyet grubuna göre belirleyemeyeceğiniz ve dört üretim farkı tipini belirleyemeyeceğiniz anlamına gelir. Yalnızca özetlenmiş bir üretim farkı görüntüleyebilirsiniz. Standarttan fark ilkesi, maliyet dökümü ilkesinden bağımsızdır. Yani, maliyet grubuna göre üretim farklarının yakalanmaya devam edilebilmesi için maliyet dökümü ilkesi olarak hiçbirini seçebilir ve maliyet grubu başına farklılıkları seçebilirsiniz.






