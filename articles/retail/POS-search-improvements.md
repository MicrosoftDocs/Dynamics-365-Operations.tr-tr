---
title: Satış noktasında (POS) ürün arama ve müşteri arama
description: Bu konu Microsoft Dynamics 365 for Retail içinde ürün ve müşteri arama özelliğinde yapılmış olan iyileştirmeler hakkında genel bakış sağlar.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 1fa38002377fac24a5f3e25bd5924ecb23fec70a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "313601"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Satış noktasında (POS) ürün arama ve müşteri arama

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) ve Cloud Point of Sale (CPOS), ürünler ve müşteriler için kolay kullanımlı arama işlevi sağlar. Arama çubuğu her zaman MPOS ve CPOS pencerelerinin üstünde olduğundan çalışanlar ürünleri ve müşterileri hızla arayabilir.

Çalışanlar geçerli mağazayla ilişkilendirilmiş ürün çeşitleri ve kataloglardaki ürünleri arayabilir. Ayrıca, çalışanlar şirketteki başka bir mağazayla ilişkilendirilmiş ürün çeşitleri ve kataloglardaki ürünleri arayabilir. Bu nedenle, kasiyerler mağaza sınıflandırması dışındaki ürünleri satabilir ve iade alabilir. Benzer şekilde, çalışanlar geçerli mağaza veya şirketle ilişkili herhangi başka bir mağaza ile ilişkili müşterileri arayabilir. Ek olarak, çalışanlar, üst kuruluştaki başka bir şirketle ilişkilendirilmiş müşterileri arayabilirler.

## <a name="product-search"></a>Ürün arama

Varsayılan olarak, ürün aramaları mağaza ürün çeşitlerinde yapılır. Bu arama türü *yerel ürün arama* olarak bilinir. Ancak, çalışanlar geçerli mağaza ile ilişkilendirilen herhangi bir kataloğa kolayca geçiş yapabilir veya farklı bir mağazada arama yapabilirler. Bu arama türü *uzak ürün arama* olarak bilinir. Kataloğu değiştirmek için sayfanın sol tarafındaki **Kategoriler** düğmesini seçin. Beliren bölmenin üstünde, **Kataloğu değiştir** düğmesini seçin ve sonra taramak için kullanılabilir kataloglardan birini seçin. Sistem ürünleri seçilen katalogda arar.

**Kataloğu değiştir** sayfasında, çalışanlar kolayca herhangi bir mağazayı seçebilir veya tüm mağazalar arasındaki ürünler arasından arama yapabilir.

![Kataloğu değiştirme](./media/Changecatalog.png "Kataloğu değiştirme")
 
Bir yerel ürün arama, aşağıdaki ürün özellikleri içerisinde arar:

- Ürün numarası
- Ürün adı
- Tanım
- Boyutlar
- Barkod
- Arama adı

### <a name="enhancements-to-local-product-searches"></a>Yerel ürün aramasındaki geliştirmeler

Yerel ürün arama deneyimi artık daha kullanıcı dostu. Aşağıdaki geliştirmeler yapılmıştır:

- Ürün ve müşteri açılır menüleri arama çubuğuna eklenmiştir; böylece çalışanlar arama yapmadan önce **Ürün** veya **Müşteri** seçimini yapabilirler. Varsayılan olarak, **Ürün** seçilidir, aşağıdaki şekilde gösterildiği gibi.
- Çoklu anahtar sözcük aramaları için (yani, arama terimleri kullanan aramalar için) perakendeciler aramanın *herhangi bir* arama terimi ile mi eşleşen yoksa yalnızca *tüm* arama terimleriyle mi eşleşen sonuçları dahil edeceğini yapılandırabilir. Bu ayar, POS işlevi profilinde, **Ürün arama** olarak adlandırılan yeni bir grupta kullanılabilir. Varsayılan ayar **Herhangi bir arama terimi ile eşleş**'tir. Bu ayar aynı zamanda önerilen ayardır. **Herhangi bir arama terimiyle eşleştir** ayarı kullanıldığında, tamamen veya kısmen bir veya daha fazla arama sözcüğüne uyan tüm ürünler sonuç olarak döndürülür. Bu sonuçlar, en çok eşleşen anahtar kelimeye sahip ürünlere göre (tam veya kısmi) artan düzende sıralanır.

    **Tüm arama terimleriyle eşleş** ayarı, yalnızca tüm arama terimleriyle (kısmi veya tam) olarak eşleşen ürünleri döndürür. Bu ayar, ürün adları uzunsa ve çalışanlar arama sonuçlarında yalnızca sınırlı ürünleri görmek istiyorlarsa kullanışlıdır. Ancak, bu tür aramanın iki sınırlaması vardır:

    - Arama yalnızca tek tek ürün özellikleri üzerinde yapılır. Örneğin, en az bir ürün özelliğinde, yalnızca tüm aranan kelimeleri içeren ürünler döndürülür.
    - Boyutlar aranmaz.

- Perakendeciler şimdi ürün aramayı, kullanıcılar ürün adlarını yazarken arama sonuçlarını gösterecek şekilde yapılandırabilir. Bu işlev için yeni bir ayar, POS işlevi profilinde, **Ürün arama** olarak adlandırılan bir grupta kullanılabilir. Bu ayarın adı **Yazarken arama önerilerini göster**'dir. Bu işlev, çalışanların aradıkları ürünü hızlıca bulmalarına yardımcı olabilir çünkü tam adını yazmalarına gerek kalmaz.
- Ürün arama algoritması şimdi ayrıca aranan terimleri ürünün **Arama adı** özelliğinde de arar.

    ![Ürün önerileri](./media/Productsuggestions.png "Ürün önerileri")

## <a name="customer-search"></a>Müşteri arama

Müşteri arama, çeşitli amaçlarla müşterileri bulmak için kullanılır. Örneğin, kasiyer bir müşterinin istek listesini veya satın alma geçmişini görüntülemek veya müşteriyi bir harekete eklemek isteyebilir. Çoklu anahtar sözcük aramalarında, müşteri arama algoritması aranan sözcüklerden herhangi biriyle eşleşen tüm müşterileri döndürür. Ancak, daha fazla anahtar kelime ile eşleşen müşteriler sonuçların üst kısmında görüntülenir. Bu davranış, diğer arama motorlarının sonuçları gösterme şekline benzer. Önce aranan terimlerin en fazlası ile eşleşen sonucu gösterirler ve sonra arama sözcükleri ile kısmen eşleşen sonuçları gösterirler. Bu davranış, aramalarında birden fazla anahtar sözcük kullandıkları, ancak sözcüklerden birinin yazım hatası içerdiği durumlarda kasiyerlere yardımcı olur.

Varsayılan olarak, müşteri arama mağazayla ilişkilendirilmiş olan müşteri adres defterleri üzerinden yapılır. Bu arama türü *yerel müşteri arama* olarak bilinir. Bununla birlikte, çalışanlar müşteriler için genel arama da yapabilir. Başka bir deyişle, şirketin mağazaları ve tüm diğer tüzel kişiler arasında arama yapabilirler. Bu arama türü *uzak müşteri arama* olarak bilinir.

Genel olarak aramak için, çalışanlar sayfanın altında bulunan **Sonuçları filtrele** düğmesini seçebilir ve sonra **Tüm mağazaları ara** seçeneğini, aşağıdaki şekilde gösterildiği gibi işaretleyebilir. Bu durumda, yalnızca müşteriler döndürülmez. Merkezdeki herhangi bir adres defterinin parçası olan tüm taraflar da döndürülür. Bu taraflar arasında çalışanlar, satıcılar, ilgili kişiler ve rakipler de vardır.

> [!NOTE]
> Bir uzak müşteri aramasının sonuç döndürmesi için en az dört karakter girilmesi gerekir.

Bir uzak müşteri aramasında, diğer tüzel varlıklardaki müşteriler için müşteri kimliği gösterilmez, çünkü geçerli şirkette bu müşteriler için bir müşteri kimliği oluşturulmamıştır. Ancak, bir çalışan müşteri ayrıntıları sayfasını açarsa, sistem otomatik olarak bu taraf için bir müşteri kimliği oluşturur ve mağazanın müşteri adres defterini müşteri ile ilişkilendirir. Bu nedenle, müşteri daha sonra yapılan yerel mağaza aramalarında da görünür.

![Genel müşteri arama](./media/Globalcustomersearch.png "Genel müşteri arama")

### <a name="enhancements-to-local-customer-search"></a>Yerel müşteri aramasındaki geliştirmeler

Telefon numarasını temel alan aramalar basitleştirilmiştir. Bu aramalar artık müşteri oluşturulurken eklenmiş olabilecek parantez, tire, boşluk gibi özel karakterleri yok sayar. Bu nedenle, kasiyelerin arama yaparken telefon numarası biçimi hakkında endişelenmesi gerekmez. Ayrıca müşteriler için kısmi bir telefon numarası yazarak da arama yapabilirler. Bir telefon numarası özel karakterler içeriyorsa, özel karakterlerden sonra görünen numaralar için arama yaparak da bulunabilir. Örneğin, bir müşterinin telefon numarası **123-456-7890** olarak girilmişse, bir kasiyer müşteriyi **123**, **456**, **7890** veya **1234567890** arayarak veya telefon numarasının ilk birkaç rakamını girerek arayabilir.

Geleneksel müşteri arama birden çok alanda arama yaptığından zaman alabilir. Bunun yerine, kasiyerler artık adı, e-posta adresi veya telefon numarası gibi tek bir özel özellik için arama yapabilir. Müşteri arama algoritmasının kullandığı özellikler topluca *müşteri arama ölçütü* olarak bilinir. Sistem Yöneticisi bir veya daha fazla ölçütü POS'ta görüntülenecek kısayol olarak kolayca yapılandırabilir. Arama tek bir ölçütle sınırlı olduğundan, yalnızca ilgili arama sonuçları gösterilir ve standart müşteri arama performansına göre çok daha iyi performans elde edilir. Aşağıda POS'taki müşteri arama kısayolları gösterilmektedir.

![Müşteri arama kısayolları](./media/SearchShortcutsPOS.png "Müşteri arama kısayolları")

Arama ölçütlerini kısayol olarak belirlemek için yöneticinin Microsoft Dynamics 365 for Finance and Operations'da **Perakende parametreleri** sayfasını açması ve **POS arama ölçütü**, sekmesinde kısayol olarak gösterilecek tüm ölçütleri seçmesi gerekir.

![Arama kısayollarını yapılandırma](./media/ConfigureShortcutsAX.png "Arama kısayollarını yapılandırma")

> [!NOTE]
> Çok sayıda kısayol eklerseniz, POS arama çubuğundaki açılan menü kalabalık olur ve çalışanın arama deneyimini etkileyebilir. Yalnızca gerektiği kadar kısayol eklemenizi öneririz.

**Görüntüleme sırası** alanı kısayolların POS'ta gösterileceği sırayı belirler. Gösterilen ölçütler müşteri arama algoritmasının müşterileri aramak için kullandığı kullanıma hazır özelliklerdir. Bununla birlikte, iş ortakları arama kısayolu olarak özel özellikleri ekleyebilir. Arama kısayolu olarak özel özellikler eklemek için sistem yöneticisinin müşteri arama ölçütleri için kullanılan genişletilebilir numaralandırmayı (enum) genişletmesi ve ardından iş ortağının özel özelliklerini kısayol olarak işaretlemesi gerekir. İş ortakları kendi özel kısayollarını aramalar için kullanıldığında, sonuçları bulmak için kod yazmaktan sorumludur.

> [!NOTE]
> Enuma eklenen özel bir özellik standart müşteri arama algoritmasını etkilemez. Başka bir deyişle, müşteri arama algoritması özel özellikte arama yapmaz. Kullanıcılar yalnızca o özel özellik kısayol olarak eklenirse veya varsayılan arama algoritması geçersiz kılınırsa aramalar için özel bir özellik kullanabilir.
