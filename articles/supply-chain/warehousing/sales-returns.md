---
title: Satış iadeleri
description: Bu makale için iade siparişlerini işlemi hakkında bilgi sağlar. Müşteri iadeleri ve bu iadelerin maliyetlendirmeye ve eldeki stok miktarlarına etkisi hakkında bilgi içerir.
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnTable, ReturnTableListPagePreviewPane, ReturnTableReferences, SalesReturnExpiredOrdersPart, SalesReturnFindOrderFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e8045ec39b9caf9bf0dc2b2d331419efb54e6d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860420"
---
# <a name="sales-returns"></a>Satış iadeleri

[!include [banner](../includes/banner.md)]

Bu makale için iade siparişlerini işlemi hakkında bilgi sağlar. Müşteri iadeleri ve bu iadelerin maliyetlendirmeye ve eldeki stok miktarlarına etkisi hakkında bilgi içerir.

Müşteriler malları çeşitli nedenlerle iade edebilir. Örneğin, bir mal kusurlu veya müşterinin beklentilerini karşılamamış olabilir. Müşteri, bir malı iade etmek için bir istekte bulunduğu zaman iade işlemi başlar. Müşterinin talebi alınınca bir iade emri oluşturulur.

## <a name="return-order-process"></a>İade emri işlemi
Aşağıdaki şekilde iade emri işleminin genel özeti verilmektedir.  

[![İade emri işlemi.](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

İki tür iade emri işlemi vardır: fiziksel iade ve yalnızca alacak.

-   **Fiziksel iade** – İade emri, ürünlerin fiziksel iadesi için yetki verir.
-   **Yalnızca alacak** – İade emri müşteriye alacak olarak iade için yetki verir ancak müşterinin ürünleri fiziksel olarak iade etmesi gerekmez.

### <a name="physical-return-order-process"></a>Fiziksel iade emri işlemi

1.  **İade emri oluşturun.** Müşterinin kusurlu veya istemediği ürünü iade etmesi için yetkilendirmeyi resmen belgeleyin. İade emri şirketin iade edilen ürünleri kabul etmesini veya müşteriye alacak yazılmasını gerektirmez. İade kabul edilirse, kusurlu mal iade edilmeden önce değiştirme amacıyla bir malın gönderilmesine yetki verebilirsiniz.
2.  **İnceleme için ambara gidin.** İade emri belgesine göre ilk incelemeyi ve doğrulamayı tamamlayın. İade emri, iade edilen malların ek inceleme ve kalite kontrolü için karantinasını da destekler.
3.  **Değerlendirmeyi yapın.** İnceleme işlemini sonlandırın ve iade edilen ürünler için ne yapılması gerektiğine karar verin. Bu adımın bir parçası olarak, müşteriye alacak yazmaya veya ürün iadesini reddetmeye ya da ürün iadesini kabul edip ürünü ıskartaya ayırmaya ve ardından müşteriye yeni bir ürün göndermeye karar verin.
4.  **Sevk irsaliyesi oluşturun.** Bir sevk irsaliyesi oluşturun ve üçüncü adımda yaptığınız değerlendirme kararını uygulayın. Lojistik işlemleri tamamlayın.
5.  **Fatura oluşturun.** İade emrini kapatın.

### <a name="credit-only-process"></a>Yalnızca alacaklandırma işlemi

1.  **İade emri oluşturun.** Müşterinin kusurlu veya istemediği ürünü iade etmeden alacaklandırılma yetkisini resmen belgeleyin. **Yalnızca alacak** değerlendirme koduyla, fiziksel iade olmadan müşteriyi alacaklandırma kararı için yetki verilir.
2.  **Fatura oluşturun.** Alacak dekontu oluşturun ve iade emrini kapatın.

## <a name="return-material-authorization"></a>Malzeme iade yetkisi
Malzeme İade Yetkisi (RMA) işlemi, satış emri işlevine dayanarak yapılır. RMA, bir satış siparişi olarak oluşturulan iade emri olarak kaydedilir ve "değiştirme siparişi" adı verilen başka bir satış siparişiyle ilişkilendirilebilir. Her iki satış siparişi kaynak RMA numarasıyla bağlantılıdır.

-   **İade emri** – Bir RMA kaydettirmek için, atanan türe sahip bir satış siparişi olan bir iade emri oluşturursunuz. **İade edilen sipariş.** RMA bilgilerinde yaptığınız değişiklikler satış siparişinde otomatik olarak güncelleştirilir. İade emrinin durumu **Açık** olana kadar, emir satış siparişleri listesinde görünmez. İade edilen malların varış ve giriş işlemlerini gerçekleştirmek ve yalnızca alacakla değerlendirme eylemine yetki vermek için RMA'yı kullanırsınız (bkz. **Değerlendirme kodları ve değerlendirme eylemleri**). Diğer tüm takip işlemleri satış siparişinde işlenmelidir.
-   **Değiştirme siparişi** – Müşteriye bir değiştirme siparişi gönderilmesi gerektiği zaman RMA'ya ikinci bir ilişkili satış siparişi dahil edilebilir. Hemen sevkiyatı desteklemek için RMA'ya ilişkin değiştirme siparişini el ile oluşturabilirsiniz. Alternatif olarak, değiştirme işlemini gösteren bir değerlendirme kodu olan RMA satır maddesi için varış, inceleme ve giriş işlemleri tamamlandıktan sonra değiştirme siparişi otomatik olarak oluşturulabilir. Değiştirme siparişi bir satış siparişiyle ilişkili işlevselliğin aynısına sahiptir. Örneğin, bunu özel ürünü değiştirme malı olarak yapılandırmak, iade edilen bir malı onarmak üzere bir üretim emri oluşturmak, satıcıdan bir değiştirme malı göndermek için doğrudan teslimat satınalma siparişini oluşturmak veya başka amaçları desteklemek için kullanabilirsiniz.

## <a name="create-a-return-order"></a>Sipariş iadesi oluşturma
Müşteri arızalı veya istemediği bir ürünü iade etmek ve/veya alacak kaydedilmesi için kuruluşunuza başvurduğunda iade siparişi işlemi başlar. Kuruluşunuz iadeyi kabul ettikten sonra iade bir iade emriyle belgelenir. Bu iade emri, iade edilen ürünün dahili işlemlerinin odak noktası olur. İade emri oluşturma prosedürü aşağıda gösterilmektedir.  

[![İade emri oluşturma prosedürü.](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>İade emri başlığı oluşturun

İade emri oluşturduğunuzda, aşağıdaki tabloda bulunan bilgiler dahil edilmelidir.

| Alan              | Açıklama                                              | Yorumlar                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Müşteri hesabı   | Müşteriler tablosuna bir referans                       | Mevcut bir müşteri hesabı belirtmelisiniz.                                                                                                                                                                                                                                                                                                  |
| Teslimat adresi   | Malın iade edileceği adres                 | Varsayılan olarak, kuruluşun adresi kullanılır. Başlıkta belirli bir ambar seçiliyse, teslimat adresi, ambarın teslimat adresi olarak değiştirilir. Bu adresi **İade emri ayrıntıları** sayfasında değiştirebilirsiniz.                                                                                                  |
| Tesis/ambar     | İade edilen ürünü teslim alan tesis veya ambar | İade emri için teslimat adresi, tesisin veya ambarın teslimat adresine göre belirlenir.                                                                                                                                                                                                                                 |
| RMA numarası         | İade emrine atanan kod.              | RMA numarası, iade emri işlemi boyunca bir alternatif anahtar olarak kullanılır. RMA numarası, **Alacak hesapları parametreleri** sayfasında ayarlanan RMA numara serisine göre atanır.                                                                                                                              |
| Bitiş tarihi           | Bir malın iade edilebileceği son tarih               | Varsayılan değer, geçerli tarih artı geçerlilik süresi olarak hesaplanır. Örneğin, bir iade, iade emri oluşturulduktan sonra 90 gün geçerliyse ve iade emri 1 Mayıs'ta oluşturulduysa, alandaki değer **30 Temmuz** olur. Geçerlilik süresi **Alacak hesapları parametreleri** sayfasından ayarlanır. |
| İade neden kodu | Müşterinin ürün iade nedeni          | Neden kodu, kullanıcı tanımlı neden kodları listesinden seçilir. Bu alanı istediğiniz zaman güncelleyebilirsiniz.                                                                                                                                                                                                                                    |
### <a name="create-return-order-lines"></a>İade emri satırlarını oluşturun

İade başlığını tamamladıktan sonra aşağıdaki yöntemlerden birini kullanarak iade satırları oluşturabilirsiniz:

-   Her iade satırı için madde ayrıntılarını, miktarı ve diğer bilgileri el ile girin.
-   **Satış siparişi bul** işlevini kullanarak bir iade satırı oluşturun. İade emri oluştururken bu işlevi kullanmanızı öneririz. **Satış siparişi bul** işlevi, iade satırından, faturalanan satış siparişi satırına referans oluşturur ve madde numarası, miktar, fiyat, iskonto ve maliyet değerleri gibi satır ayrıntılarını satış satırından alır. Referans, ürün şirkete iade edildiğinde, satıldığı birim maliyetiyle değerlendirilmesini garantilemeye yardımcı olur. Referans iade emrindeki miktarın, faturadaki satış miktarını aşmadığını da doğrular.

>[!NOTE] 
>Bir satış siparişine referans bulunan iade satırları, satışa ilişkin düzeltmeler veya ters kayıtlar olarak işlem görür. Daha fazla bilgi için, bu makalede ileride yer alan "Genel muhasebeye nakletme" bölümüne bakın.

### <a name="charges"></a>Masraflar

Ücretler ve masraflar, aşağıdaki yöntemlerden bir veya daha fazlasıyla iade emrine eklenebilir:

-   İade emri başlığına, iade emri satırına veya her ikisine masrafları el ile ekleyebilirsiniz.
-   Masraflar iade emri başlığına iade neden kodunun bir işlevi olarak otomatik eklenebilir.
-   Masraflar iade emri satırına satırın değerlendirme kodunu temel alarak otomatik eklenebilir.

Masraflar, satıra bir iade nedeni kodu veya değerlendirme kodu atandıktan sonra otomatik olarak eklenir. Neden kodu daha sonra değiştirilirse, mevcut masraf girişi kaldırılmaz ancak yeni neden koduna dayalı olarak yeni bir masraf girişi eklenebilir. İade emri satırlarına masraf eklediğiniz zaman, satır veya sipariş değerinin bir yüzdesi olarak hesaplanan masraflar, yüzde de negatif bir sayı değilse, satır veya sipariş negatif olduğunda negatif olur. Negatif değer taşıyan bir masraf, müşteriye yazılan alacağı temsil eder.

### <a name="return-reason-codes"></a>İade neden kodları

İadelere neden kodları uygulayarak iade modellerinin daha kolay analiz edilir hale gelmesine yardımcı olabilirsiniz. Neden kodları müşterinin malı neden iade etmek istediği hakkında bilgi sağlar. Bazı kuruluşların birçok neden kodu vardır. Bu kuruluşlar, daha iyi bir genel bakış elde etmek ve kapsamlı raporlar elde etmek için neden kodlarını neden kodu grupları halinde düzenleyebilir.

### <a name="disposition-codes-and-disposition-actions"></a>Değerlendirme kodları ve değerlendirme eylemleri

İade emri işleminde önemli bir adım, varış kaydının bir parçası olarak iade emri satırına bir değerlendirme kodu atamaktır. Değerlendirme kodu aşağıdaki bilgileri belirler:

-   **Mali etkiler** – Müşteri iade edilen mallar için alacaklandırılacak mı ve iade emri satırına herhangi bir masraf eklenecek mi?
-   **İade edilen malı değerlendirme** – Mal stoka geri mi eklenecek, ıskartaya mı ayrılacak yoksa müşteriye mi iade edilecek?
-   **İade edilen malın lojistiği** – Müşteriye bir değiştirilme malı verilecek mi?

İade edilen malların nasıl değerlendirileceğini belirlemeye ek olarak, değerlendirme kodları iade satırına masrafların uygulanmasını sağlayabilir. Bu kodlar iadeleri istatistiksel analiz amacıyla gruplandırmak için de kullanılabilir. Değerlendirme kodları iade emirleri kurulumunun bir parçası olarak tanımlanır. Ancak, her değerlendirme kodunun yerleşik değerlendirme eylemlerinden birine başvurması gerekir. Aşağıdaki tabloda yerleşik değerlendirme kodlarının ve eylemlerinin listesi verilmektedir. **Önemli:** Bir malın iade edilmemesi gerektiği halde müşteriye alacak yazılması gerekiyorsa, iade satırına **Yalnızca alacak** değerlendirme kodunu atayın.

<table>
<thead>
<tr class="header">
<th>Elden çıkarma kodu</th>
<th>Mali etkiler</th>
<th>Lojistikteki etkileri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yalnızca alacaklandır</td>
<td><ul>
<li>Müşteriye satış fiyatından ücretler veya masraflar düşülerek kalan tutar alacak yazılır.</li>
<li>Malın ıskartaya ayrılmasından kaynaklanan zarar genel muhasebeye nakledilir.</li>
</ul></td>
<td>Bu mal iade edilemez. Bu değerlendirme eylemi aşağıdaki durumlarda kullanılır:
<ul>
<li>Taraflar arasında yeterli güven vardır.</li>
<li>Kusurlu malın iade maliyeti aşırıdır.</li>
<li>Bu malların stoka iadesine izin verilemiyordur. Başka koşullar nedeniyle fiziksel bir iade gerekli değildir.</li>
</ul></td>
</tr>
<tr class="even">
<td>Alacak</td>
<td><ul>
<li>Müşteriye satış fiyatından ücretler veya masraflar düşülerek kalan tutar alacak yazılır.</li>
<li>Stok değeri, iade edilen malın maliyetiyle artar.</li>
</ul></td>
<td>Mal iade edilir ve stoka geri eklenir.</td>
</tr>
<tr class="odd">
<td>Değiştir ve alacaklandır</td>
<td><ul>
<li>Müşteriye satış fiyatından ücretler veya masraflar düşülerek kalan tutar alacak yazılır.</li>
<li>Stok değeri, iade edilen malın maliyetiyle artar.</li>
<li>Bir değişiklik için ayrı bir satış siparişi oluşturulur ve ayrı olarak ele alınır.</li>
</ul></td>
<td>Mal iade edilir ve stoka geri eklenir.</td>
</tr>
<tr class="even">
<td>Değiştir ve ıskartaya ayır</td>
<td><ul>
<li>Müşteriye satış fiyatından ücretler veya masraflar düşülerek kalan tutar alacak yazılır.</li>
<li>Malın ıskartaya ayrılmasından kaynaklanan zarar genel muhasebeye nakledilir.</li>
<li>Bir değişiklik için ayrı bir satış siparişi oluşturulur ve ayrı olarak ele alınır.</li>
</ul></td>
<td>Madde iade edilir ve ıskartaya ayrılır.</td>
</tr>
<tr class="odd">
<td>Müşteriye iade et</td>
<td>Herhangi bir ücret veya masraflar hariç hiçbiri.</td>
<td>Mal iade edilir ancak incelendikten sonra müşteriye geri gönderilir. Bu değerlendirme eylemi, mala kasten zarar verildiği veya garanti geçersiz hale geldiği zaman kullanılabilir.</td>
</tr>
<tr class="even">
<td>Iskarta</td>
<td><ul>
<li>Müşteriye satış fiyatından ücretler veya masraflar düşülerek kalan tutar alacak yazılır.</li>
<li>Malın ıskartaya ayrılmasından kaynaklanan zarar genel muhasebeye nakledilir.</li>
</ul></td>
<td>Mal iade edilir veya ıskartaya ayrılır.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>İnceleme için ambara varış
Sevk irsaliyesini deftere naklederek iade edilen malları stoka fiziksel olarak almadan önce malların varış kayıt ve isteğe bağlı bir incelemeden geçirilmesi gerekir. Aşağıdaki şekilde varış işleminin genel özeti verilmektedir. Şekilde gösterilen her adım ilerideki bölümlerde açıklanmaktadır.  

[![Varış işlemi.](./media/salesreturn03.png)](./media/salesreturn03.png)  

Bu işlemde bu makale kapsamında ele alınmayan çeşitli varyasyonlar vardır. Bu varyasyonlardan birkaçı:

-   Varış günlüğü oluştururken **Varışa genel bakış** listesini kullanmayın. Bunun yerine, Varış günlüğünü el ile oluşturun. İade emirlerinde referans olarak **Satış siparişi** olacaktır.
-   Ambar yönetimi kullanıyorsanız, paletli taşımalar oluşturun. Paletli taşıma sırasında iade satırının durumu **Gelen** olacaktır.
-   İade edilen malın varışını doğrudan iade siparişi satırına **Kayıt** işleviyle kaydedin.

Varış işlemi sırasında iadeler ambar varışları için genel işlemle tümleştirilir. Varış işlemi ayrı bir incelemeye alınması gereken iade mallar için karantina emirlerinin oluşturulmasını da destekler.

### <a name="identify-products-in-the-arrival-overview-list"></a>Varışa genel bakış listesindeki ürünleri belirleme

**Varışa genel bakış** sayfasında tüm planlı gelen varışlar listelenir.

>[!NOTE] 
>İade siparişlerinden gelen varışlar, diğer türlerdeki varış hareketlerinden ayrı işlenmelidir. **Varışa genel bakış** sayfasında bir gelen paketi belirledikten sonra (örneğin, eşlik eden RMA belgesini kullanarak), Eylem bölmesinde **Varışı başlat**'a tıklayarak, varışla eşleşen bir Varış günlüğü oluşturup başlatın.

### <a name="edit-the-arrival-journal"></a>Varış günlüğünü düzenleme

**Karantina yönetimi** seçeneği ayarını **Evet** yaparak, iade satırı için bir karantina emri oluşturabilirsiniz. Bir satır inceleme amacıyla karantinaya gönderildiyse, değerlendirme kodu belirtemezsiniz. 
 
Malın stok modeli grubunda **Karantina yönetimi** seçeneği ayarını **Evet** yaparsanız, **Yevmiye defteri satırları** sayfasındaki **Karantina yönetimi** seçeneği Varış günlüğü satırı için işaretlenir ve değiştirilemez. Satır karantinaya gönderilirse, ilgili karantina ambarını belirtmeniz gerekir. 

Varış satırı incelemeye gönderilmiyorsa, ambar varış memuru değerlendirme kodunu doğrudan Varış günlüğü satırında belirtmeli ve ardından Varış günlüğünü nakletmelidir. Aynı değerlendirme kodu iade satırının tüm miktar atanmayacaksa veya satırın tüm miktarı teslim alınmadıysa satırı bölmeniz gerekir. Bir Varış günlüğü satırını böldüğünüz zaman, iade satırını da (**SatışSatırı**) böler ve yeni bir lot kodu oluşturursunuz. Varış günlüğü satırının miktarını azaltarak satırı bölebilirsiniz. Günlük deftere nakledilince kalan miktar için **Beklenen** durumunda yeni bir iade satırı oluşturulur. Satırı **İşlevler** &gt; **Böl**'e tıklayarak da bölebilirsiniz.

### <a name="process-the-quarantine-order"></a>Karantina emrini işleme

İade edilen ürünler karantina ambarında incelemeye gönderilirse, ek işlemler bir karantina emri dahilinde tamamlanır. Karantinaya gönderilen her varış satırı için bir karantina emri oluşturulur. Değerlendirme kodu inceleme işleminin sonucunu gösterir. 

Karantina emrini tıpkı Varış günlüğünü böldüğünüz gibi bölebilirsiniz. Karantina emrini bölerseniz, iade satırının da karşılık gelen bir bölme işleminden geçirilmesine neden olursunuz. Değerlendirme kodu girildikten sonra **Son** veya **Tamamlandı olarak bildir** işleviyle karantina emrini tamamlayın. **Tamamlandı olarak bildir**'i seçerseniz, ilgili ambarda yeni bir varış oluşturulur. Bunun ardından bu varışı **Varışa genel bakış** sayfasından işleyebilirsiniz. 

Varış bir karantina emrinden kaynaklanıyorsa, inceleme sırasında atanan değerlendirme kodunu değiştiremezsiniz. Karantina emrini **Son** işlevini kullanarak tamamlarsanız lot otomatik olarak kaydedilir. Bazen bir mal karantinadan Sevkiyat ve teslim alma departmanına geri gönderilebilir. Örneğin karantina denetçisi malın stokta nerede depolanacağı bilmiyor olabilir. Bu durumda, karantina nedeniyle belirtilen değerlendirme kodunun doğru bir şekilde kaydedilmesi ve gerekli işlemlerin yapılabilmesi için ilgili sevk irsaliyesinin güncellenmesi gerekir. 

İade satırı kaydedilirken müşteriye alındı onayı gönderilir. **İade onayı** raporu iade emri belgesine benzer. **İade onayı** raporu günlüğe işlenmez ve sisteme başka bir şekilde kaydedilmez ve iade emri işleminde zorunlu bir adım değildir.

## <a name="replace-a-product"></a>Ürünü değiştirme
Ürün değişimini yönetmek için iki yöntem vardır:

-   **Önceden yenileme** – İade edilen ürün müşteriden alınmadan önce bir ürünü değiştirirsiniz.
-   **Değerlendirme koduyla değiştirme** – Otomatik olarak yeni bir değiştirme siparişi satırı oluşturulur.

### <a name="up-front-replacement"></a>Yenileme siparişi oluşturuldu

Önceden yenileme durumunda, mal iade edilmeden önce, değiştirilen mal müşteriye teslim edilebilir. Örneğin, mal, yerine yedek parça koyulmadan çıkarılamayacak bir makine parçasıysa veya müşterinin yenilenen ürünü en kısa sürede almasını istiyorsanız bu yöntem yararlı olur. Önceden yenileme siparişi, bağımsız bir satış siparişidir. Başlık bilgileri müşteriden, satır bilgileri iade emrinden başlatılır. Değiştirme siparişini iade emrinden bağımsız olarak düzenleyebilir, işleyebilir ve silebilirsiniz. Bir değiştirme siparişini değiştirdiğiniz zaman, siparişin bir değiştirme siparişi olarak oluşturulduğu iletisi alırsınız. Önceden değiştirme işlemi aşağıdaki şekilde gösterilmektedir.  

![Önceden değiştirme işlemi.](./media/SalesReturn04.png)

İade emri, değiştirme siparişine başvuru içerir. Kusurlu mal iade edilmeden önce bir önceden değiştirme siparişi oluşturulursa, kusurlu mal iade edildikten sonra, değiştirme için değerlendirme kodu seçemezsiniz.

### <a name="replacement-by-disposition-code"></a>Değerlendirme koduyla değiştirme

Müşteriye bir değiştirme maddesi gönderirseniz ve iade emrinde **Değiştir ve ıskartaya ayır** veya **Değiştir ve alacaklandır** değerlendirme eylemini kullanıyorsanız, aşağıdaki şekilde gösterilen işlemi kullanın.  

![Değerlendirme kodu kullanıldığında değiştirme işlemi.](./media/SalesReturn05.png)

Değiştirilen mal, değiştirme satış siparişi adlı bağımsız bir satış siparişiyle teslim edilir. Bu satış siparişi, iade emri için sevk irsaliyesi hazırlanırken oluşturulur. Sipariş başlığında, iade emri başlığında başvurulan, müşteriden alınmış bilgiler kullanılır. Satır bilgileri, **Yerine koyulacak madde** sayfasına girilen bilgilerden alınır. **Yerine koyulacak madde** sayfası, "değiştir" sözcüğüyle başlayan değerlendirme eylemleri olan satırlar için doldurulmuş olmalıdır. Ancak, değiştirme maddesinin ne miktarı ne de kimliği doğrulanmıştır veya sınırlıdır. Bu davranışa, müşterinin aynı malı farklı bir yapılandırma veya boyutta istediği veya müşterilerin tamamen farklı bir mal istediği durumlarda izin verilir. Varsayılan olarak, **Yerine koyulacak madde** sayfasına aynı mal girilir. Ancak, işlevin ayarlanmış olması koşuluyla, farklı bir mal seçebilirsiniz. 

>[!NOTE] 
>Değiştirme satış siparişini oluşturulduktan sonra silemez ve düzenleyemezsiniz.

## <a name="generate-a-packing-slip"></a>Sevk irsaliyesi oluşturma
İade edilen malların stoka alınabilmesi için, malların ait olduğu siparişin sevk irsaliyesini güncelleştirmeniz gerekir. Fatura güncelleştirme işlemi nasıl mali hareketin güncelleştirilmesi ise, sevk irsaliyesi güncelleştirme işlemi de stok kaydının fiziksel olarak güncelleştirilmesidir. Diğer bir deyişle, bu işlem, stokta yapılan değişiklikleri kaydeder. İadelerde ise, elden çıkarma eylemine atanan adımlar, sevk irsaliyesinin güncelleştirilmesi sırasında uygulanır. Sevk irsaliyesi oluşturduğunuzda aşağıdaki olaylar gerçekleşir:

-   Ambarda fiziksel giriş yapmak için standart işlem kullanılır. Stok modeli grubu (**Fiziksel stokun deftere nakli**) ve Alacak hesapları parametreleri (**Sevk irsaliyesini genel muhasebeye naklet**) uygun şekilde ayarlandıysa genel muhasebe nakilleri oluşturulur.
-   "Iskarta" sözcüğünü içeren bir değerlendirme eylemiyle işaretlenmiş maddeler ıskartaya ayrılır ve genel muhasebeye stok zararı nakledilir.
-   **Müşteriye iade** değerlendirme eylemiyle işaretlenmiş maddelerin girişi yapılır ve müşteriye teslim edilir. Bu maddelerin stokta net etkisi yoktur.
-   Bir değiştirme satış siparişi oluşturulur. Bu satış siparişinde **Yerine koyulacak madde** sayfasındaki bilgiler temel alır.

Sevk irsaliyesini yalnızca iade durumu **Kayıtlı** olan satırlar için ve ancak iade satırındaki tüm miktar için oluşturabilirsiniz. İade siparişinde birden fazla satırın durumu **Kayıtlı** ise, **Sevk irsaliyesini deftere kaydet** sayfasındaki diğer satırları silerek bir satırlar alt kümesi için sevk irsaliyesi oluşturabilirsiniz. 

Kısmi iadeler iade emri sevkiyatlarına göre değil, iade emri satırlarına göre tanımlanır. Bu nedenle, bir iade emri satırındaki tam miktarı alır ancak iade emrindeki diğer satırlardan hiçbir şey almazsanız, teslimat kısmi bir teslimat değildir. Ancak, bir iade emri satırında belirli bir maddeden 10 birimin iade edilmesi isteniyorsa, ancak siz yalnızca 4 birim alırsanız, bu kısmi bir teslimattır. Beklenen maddelerin tümü ulaşmadıysa, sevkiyatı bir kenara bırakıp, iade edilen miktarın geri kalan kısmının ulaşmasını bekleyebilirsiniz. Alternatif olarak, kısmi miktarı kaydedip deftere nakledebilirsiniz. Sevk irsaliyelerini deftere nakletme işleminin bir parçası olarak, müşterinin sevkiyat belgelerindeki sevk irsaliyesi referans numarasını sipariş satırlarıyla ilişkilendirebilirsiniz. Bu ilişkilendirme isteğe bağlıdır ve yalnızca referans amaçlıdır. Bu, herhangi bir hareket güncelleştirmesi oluşturmaz. 

Genel olarak, sevk irsaliyesi işlemini atlayıp doğrudan faturalamaya geçebilirsiniz. Bu durumda, sevk irsaliyesi oluşturma sırasında uygulamış olacağınız adımlar faturalama sırasında tamamlanır.

## <a name="generate-an-invoice"></a>Bir fatura oluştur
**İade emri** sayfasında iade emrinin özel lojistik yönlerini işlemek için gereken bilgi ve eylemler bulunmasına karşın, faturalama işlemini tamamlamak için **Satış siparişi** sayfasını kullanmanız gerekir. Kuruluşunuz bunun ardından iade emirlerini ve satış siparişlerini aynı anda faturalayabilir ve gerekirse faturalama işlemini aynı kişi tamamlayabilir. İade emrini **Satış siparişi** sayfasında görüntülemek için, satış siparişi numarasının bağlantısına tıklayarak ilgili satış siparişini açın. İade emrini **Tüm satış siparişleri** sayfasında da bulabilirsiniz. İade emirleri, sipariş türü **İade edilen sipariş** olan satış siparişleridir.

### <a name="credit-correction"></a>Alacak düzeltme

Faturalama işleminin bir parçası olarak, tüm sair giderleri doğrulayın. Genel muhasebe nakillerinin düzeltmeler (Storno) haline gelmesini sağlamak için, faturayı/alacak dekontunu naklederken **Fatura deftere naklediliyor** sayfasının **Diğer** sekmesindeki **Alacak düzeltme** seçeneğini kullanmayı düşünün.

> [!NOTE]
> Varsayılan olarak, **Alacak düzeltmesi** seçeneği, **Alacak hesapları parametreleri** sayfasındaki **Düzeltme olarak alacak dekontu** seçeneği etkinleştirildiği zaman etkinleştirilir. Ancak, iadeleri Storno'yla nakletmemenizi öneririz.

## <a name="create-intercompany-return-orders"></a>Şirketlerarası iade emirleri oluşturma
İade emirleri kuruluşunuzdaki iki şirket arasında tamamlanabilir. Aşağıdaki senaryolar desteklenir:

-   Şirketlerarası bir ilişki içindeki iki şirket arasındaki basit şirketlerarası iadeler
-   Satış yapan şirkette bir müşteri iade emri oluşturulduğu zaman kurulan bir şirketlerarası zincir
-   Alıcı şirkette bir satıcı iade emri oluşturulduğu zaman kurulan bir şirketlerarası zincir
-   Harici bir müşteri ve şirketlerarası bir ilişki içindeki iki şirket arasında yapılan doğrudan teslim sevkiyat iadeleri

### <a name="setup"></a>Kurulum

Aşağıdaki şekilde, iki şirketin şirketlerarası bir ilişkiye girmesi ve şirketlerarası ticaretten faydalanması için gereken minimum kurulum gösterilmektedir.  

![Minimum kurulum.](./media/SalesReturn06.png)

Aşağıdaki senaryoda, CompBuy şirket alıcı, CompSell ise satıcı şirkettir. Genellikle, satıcı şirket malları alıcı şirkete veya doğrudan teslim sevk senaryolarında doğrudan son müşteriye gönderir. CompBuy'da, satıcı IC\_CompSell, CompSell şirketiyle ilişkili şirketlerarası bir uç nokta olarak tanımlanır. Aynı zamanda, CompSell'de, müşteri IC\_CompBuy, CompBuy şirketiyle ilişkili şirketlerarası bir uç nokta olarak tanımlanır. Uygun eylem ilkesi politikası ayrıntıları ve değer eşlemeleri her iki şirkette de tanımlanmalıdır. Doğrudan teslim sevkiyat senaryosunda, bir şirketlerarası iade emri oluşturulur (bu aynı zamanda bir şirketlerarası satış siparişidir). Şirketlerarası iade emrinin RMA numarası, CompSell'deki RMA numara serisinden alınabilir veya CompBuy'daki orijinal iade emrine atanmış RMA numarasından kopyalanabilir. CompBuy'ın **SatınalmaTalebi** eylem politikasındaki RMA numarası ayarları bu eylemleri belirler. RMA numarası eşitlenmişse, iki şirketin aynı numara sırasını kullanması durumunda numara çakışması riskini azaltma planı yapmanız gerekir.

### <a name="simple-intercompany-returns"></a>Basit şirketlerarası iadeler

Bu senaryo, aşağıdaki şekilde gösterildiği gibi, aynı kuruluştaki iki şirketle ilgilidir.  

![Basit şirketlerarası iade.](./media/SalesReturn07.png)

Alıcı şirkette bir satıcı iade emri veya satıcı şirkette müşteri iade emri oluşturulduğunda sipariş zinciri oluşturulabilir. Diğer şirkette karşılık gelen sipariş oluşturulur ve satıcı iade siparişindeki başlık ve satır bilgilerinin müşteri iade emrindeki ayarları yansıtıp yansıtmadığından emin olur. Oluşan iade emri, mevcut bir müşteri faturasında referansı (**Satış siparişini bul**) dahil edebilir veya hariç tutabilir. İki emrin sevk irsaliyeleri ve faturaları ayrı ayrı işlenebilir. Örneğin, müşteri iade emri için sevk irsaliyesi oluşturmadan önce satıcı iade emri için bir sevkiyat irsaliyesi oluşturmak zorunda kalmazsınız.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Üç taraf arasında doğrudan teslim sevkiyat iadeleri

Bu senaryo, **Doğrudan teslim** türünden bir önceki satışın tamamlanması durumunda ve müşteriyle etkileşime giren şirkette müşteriye yönelik bir fatura mevcutsa oluşturulabilir. Aşağıdaki şekilde, CompBuy şirketi daha önce müşterileri Extern'e ürün satmış ve faturalamıştır. Ürünler CompSell şirketinden müşteriye bir şirketlerarası sipariş zinciri aracılığıyla doğrudan gönderilmiştir.  

![Üç taraf arasında doğrudan teslim sevkiyat iadeleri.](./media/SalesReturn08.png)

Extern adlı müşteri ürünleri iade etmek isterse, CompBuy şirketinde müşteri için bir iade emri (RMA02) oluşturulur. Şirketlerarası zinciri kurmak için, iade emrine doğrudan teslim işareti koyulması gerekir. İade için müşteri faturasını seçerken **Satış siparişini bul** işlevini kullanırsanız, aşağıdaki belgelerden oluşan bir şirketlerarası sipariş zinciri kurulur:

-   **Orijinal iade emri:** RMA02 (CompBuy şirketi)
-   **Satınalma siparişi:** PO02 (CompBuy şirketi)
-   **Şirketlerarası iade emri:** RMA\_00032 (CompSell şirketi)

Doğrudan teslim şirketlerarası zinciri oluşturulduktan sonra iadelerin tüm fiziksel işlemleri şirketlerarası iade emri CompSell şirketindeki RMA\_00032 bağlamında olmalıdır. Ürünler CompBuy şirketinde teslim alınamaz. Şirketlerarası iade emrine bir değerlendirme kodu atandığı zaman, orijinal siparişin doğru faturalanmasını sağlamak için orijinal iade emriyle senkronize edilir.

## <a name="post-to-the-ledger"></a>Genel muhasebeye naklet
İade emri faturalandığında üretilen genel muhasebe nakilleri birkaç önemli ayar ve parametreden etkilenir:

-   **İade maliyet fiyatı** – **Standart maliyet** dışında stok modelleri için, maddenin stoka dönmesinin kabulü veya ıskartaya ayrılması durumunda maddenin maliyetini **İade maliyet fiyatı** parametresi belirler. Doğru bir stok değerlemesi hesaplamak için, **İade maliyet fiyatı** parametresini doğru ayarlamanız önemlidir. Bir müşteri faturasına atıf yapan bir iade emri satırı oluşturmak için **Satış siparişini bul** işlevini kullanırsanız, **İade bedeli fiyatı** değeri, satılan maddenin maliyet fiyatına eşittir. Aksi durumda, maliyet fiyatı değeri madde kurulumundan gelir veya el ile girilebilir.
-   **Alacak düzeltme / Storno** – **Fatura deftere naklediliyor** sayfasındaki **Alacak düzeltme** parametresi, nakillerin pozitif (DR/CR) girişleri olarak mı yoksa düzeltici, negatif girişler olarak mı kaydedileceğini belirler.

Aşağıdaki örneklerde, iade maliyet fiyatı **Fatura maliyet fiyatı** olarak temsil edilir.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Örnek 1: İade emrinde bir müşteri faturasına referans yok

İade emrinde bir müşteri faturasına referans yok. İade edilen madde alacak kaydediliyor. İade emri faturası veya alacak dekontu oluşturulduğu zaman **Alacak düzeltme** parametresi seçilmemiş.  

![İade emri bir müşteri faturasına başvurmuyor.](./media/SalesReturn09.png)  

> [!NOTE]
> **İade maliyet fiyatı** parametresi için varsayılan değer olarak madde master fiyatı kullanılır. Varsayılan fiyat, stok çıkışı anındaki maliyet fiyatından farklıdır. Bu nedenle, etki, 3 birimlik bir kaybın tahakkuk etmesidir. Ayrıca, iade emri, satış siparişinde müşteriye verilen iskontoyu içermez. Bu nedenle, fazla bir alacak oluşur.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Örnek 2: İade emri için alacak düzeltmesi seçiliyor

Örnek 2, örnek 1'le aynı olmakla birlikte, iade emri faturası oluşturulurken **Alacak düzeltmesi** parametresi seçilmiştir.  

![Alacak düzeltmesinin seçildiği iade emri.](./media/SalesReturn10.png)  

>[!NOTE] 
>Genel muhasebe nakilleri negatif düzeltmeler olarak girilir.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Örnek 3: İade emri satırı Satış siparişi bul işlevi kullanılarak oluşturuluyor

Bu örnekte iade emri satırı **Satış siparişi bul** işlevi kullanılarak oluşturuluyor. Fatura oluşturulurken **Alacak düzeltme** parametresi seçilmemiş.  

![Satış siparişi bul işlevi kullanılarak oluşturulan iade emri satırı.](./media/SalesReturn11.png)  

> [!NOTE]
> **İskonto** ve **İade maliyet fiyatı** doğru biçimde ayarlanmıştır. Bu nedenle, müşteri faturasının tam ters kaydı gerçekleşir.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]