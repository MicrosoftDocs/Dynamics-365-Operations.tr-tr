---
title: "Satış iadeleri"
description: "Bu konu için iade siparişlerini işlemi hakkında bilgi sağlar. Müşteri döndürür ve maliyetlendirme ve eldeki stok miktarları üzerinde etkileri hakkında bilgiler içerir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Satış iadeleri

Bu konu için iade siparişlerini işlemi hakkında bilgi sağlar. Müşteri döndürür ve maliyetlendirme ve eldeki stok miktarları üzerinde etkileri hakkında bilgiler içerir.

Müşteriler öğeler çeşitli nedenlerle geri dönebilirsiniz. Örneğin, bir öğe hatalı olabilir veya müşteri beklentilerini karşılamıyor olabilir. Bir müşteri bir maddeyi iade isteği verdiğinde iade işlemini başlatır. Müşterinin isteği alındığında, iade siparişi Microsoft Dynamics 365 işlemleri için oluşturulur.

## <a name="return-order-process"></a>İade siparişi işlemi
Aşağıdaki resimde, iade siparişi işlemine genel bakış sağlar.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

İade siparişi işlemi iki tür vardır: fiziksel dönmek ve yalnızca alacak.

-   **Fiziksel iade** – fiziksel dönüşü ürünleri iade siparişi yetkilendirir.
-   **Yalnızca kredi** – iade siparişi müşteri iade yetkisi verir, ancak müşteri ürün fiziksel olarak iade gerektirmez.

### <a name="physical-return-order-process"></a>İade siparişi fiziksel işlem

1.  **İade siparişi oluşturun.** Resmi olarak yetkilendirme herhangi bir hasar veya istenmeyen ürün dönmek müşteri için belge. İade siparişi şirket döndürülen ürünleri kabul veya kredi sağlamak için müşteri gerektirmez. İade kabul edilirse, kusurlu Madde iade edilmeden önce gönderilecek bir değiştirilen madde yetki verebilir.
2.  **Ambarda incelemesi için ulaşır.** Bir ilk incelemesi ve iade siparişi belgesine dayalı doğrulamayı tamamlamak. İade siparişi iade edilen maddelerin karantina ek inceleme ve kalite kontrol için de destekler.
3.  **Değerlendirme belirler.** Denetleme işlemi sonlandırma ve döndürülen ürünleri ile ne yapılması gerektiğini karar verin. Bu adımın bir parçası müşteri kredi, ürün iade reddedebilirsiniz veya ürün iadesini kabul, ürünün hurda ve sonra başka bir ürünle müşteriye gönderin olup olmadığını karar verin.
4.  **Sevk irsaliyesi oluşturur.** 3. adımda yaptığınız değerlendirme kararı uygulamak ve sevk irsaliyesi oluşturur. Lojistik işlemleri sonlandırın.
5.  **Bir fatura oluşturun.** İade siparişi kapatın.

### <a name="credit-only-process"></a>Yalnızca işlem alacak

1.  **İade siparişi oluşturun.** Resmi olarak yetkilendirme kusurlu veya istenmeyen ürünler dönmeden bir kredi almak müşteri için belge. **Yalnızca kredi** değerlendirme kodu olmadan fiziksel return müşteri kredi kararı yetkilendirir.
2.  **Bir fatura oluşturun.** Alacak dekontu oluştur ve iade siparişi kapatın.

## <a name="return-material-authorization"></a>İade malzeme yetkilendirme
İade malzeme yetkilendirme (RMA) işleme işlevselliği satış siparişi oluşturur. Bir RMA bir satış siparişi oluşturulur ve başka bir satış siparişi değiştirme Siparişi adlı ilişkili olabilir bir iade siparişi olarak kaydedilir. Hem satış siparişlerine kaynak RMA numarası ile bağlayın.

-   **İade siparişi** – bir RMA kaydetmek için atanan türü olan bir satış siparişi, iade siparişi, oluşturma **emri verdi.** RMA bilgide yaptığınız herhangi bir değişiklik satış siparişi otomatik olarak güncelleştirilir. İade siparişi durumu olana kadar **açık**, satış siparişleri listesinde görünmez. RMA varış ve alış irsaliyesi İade edilen maddelerin işlemek gibi bir değerlendirme yalnızca İade eylemi yetkilendirmek için kullanın (bölümüne bakın **değerlendirme kodları ve değerlendirme eylemleri**). Tüm izleme işlemleri satış siparişindeki işlenmeli.
-   **Değiştirme siparişi** – değiştirme Siparişi müşteriye sevk edilecek zaman RMA ikinci ilişkili satış siparişine dahil edebilirsiniz. Hemen sevk irsaliyesi desteklemek RMA için değiştirme siparişi el ile oluşturabilirsiniz. Alternatif olarak, RMA yerini gösteren bir değerlendirme kodu olan kalemi için varış, inceleme ve giriş tamamlandıktan sonra değiştirme siparişi otomatik olarak oluşturulabilir. Değiştirme siparişi satış siparişiyle ilişkili aynı işlevselliğe sahiptir. Örneğin, onu özel bir ürün değiştirilen madde için yapılandırmak için iade edilen maddeyi onarmak, değiştirilen bir satıcıdan göndermek için satınalma siparişi doğrudan teslim oluştur veya diğer destek amacıyla bir üretim emri oluşturmak için kullanabilirsiniz.

## <a name="create-a-return-order"></a>Sipariş iadesi oluşturma
Müşteri arızalı veya istenmeyen bir ürün dönmek için ve/veya alacak kaydedilecek organizasyonunuza başvurduğunda, iade siparişi işlemi başlar. Kuruluşunuzun iade kabul ettikten sonra iade iade siparişi tarafından belgelenmiştir. Bu iade siparişi iade edilen ürünün iç işleme odak noktasını olur. İade siparişi oluşturma yordamı aşağıda gösterilmiştir.  

[![İade siparişi oluşturma yordamını](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>İade siparişi başlığı oluşturun

İade siparişi oluşturduğunuzda, aşağıdaki tabloda bulunan bilgileri dahil edilmelidir.

| Alan              | Açıklama                                              | Yorumlar                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Müşteri hesabı   | Müşteriler tablosunu başvuru                       | Varolan müşteri hesabı sağlamalısınız.                                                                                                                                                                                                                                                                                                  |
| Teslimat adresi   | Madde iade adresi                 | Varsayılan olarak, kuruluşunuzun adres kullanılır. Başlığında belirli bir ambar seçiliyse, teslimat adresini, ambar sevkiyat adresine değiştirilir. Bu adres değiştirebileceğiniz **iade sipariş ayrıntıları** sayfa.                                                                                                  |
| Tesis/ambar     | Site veya iade edilen ürün aldığı ambar | İade siparişi için teslimat adresini sitenin veya ambar teslimat adresine göre belirlenir.                                                                                                                                                                                                                                 |
| RMA numarası         | İade siparişine atanan kimliği              | RMA numarası iade siparişi işlemi boyunca diğer anahtar olarak kullanılır. Atanan RMA numarası ayarlanır RMA numara sırası esas **Accounts receivable parameters** sayfa.                                                                                                                              |
| Bitiş tarihi           | Bir öğe döndürülen son tarihi               | Varsayılan değer olarak geçerli tarih artı geçerlilik süresi hesaplanır. Örneğin, bir dönüş yalnızca zaman iade siparişi oluşturulur ve iade siparişi 1 Mayıs oluşturulduğu tarihten itibaren 90 gün boyunca geçerli alandaki değeri ise, **30 Temmuz**. Üzerinde geçerlilik dönemini ayarlama **Accounts receivable parameters** sayfa. |
| İade neden kodu | Müşterinin ürün iade nedeni          | Neden kodu listesinde, kullanıcı tanımlı neden kodları seçilir. Bu alan her zaman güncelleştirebilirsiniz.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>İade siparişi satırları oluştur

İade üstbilgi tamamladıktan sonra aşağıdaki yöntemlerden birini kullanarak iade satırları oluşturabilirsiniz:

-   El ile madde ayrıntıları, miktar ve dönüş her satır için diğer bilgileri girin.
-   Dönüş hattı kullanarak oluşturduğunuz **satış siparişini bulmak** işlev. İade siparişi oluşturduğunuzda, bu işlev kullanmanızı öneririz. **Satış siparişini bulmak** işlevi dönüş satırında faturalanan satış siparişi satırı için başvuru oluşturur ve madde numarası, miktar, fiyat, iskonto ve satış satırından maliyet değerleri gibi ayrıntılar satırı alır. Başvuru garantilemeye yarar adresindeki ürün şirkete iade edildiğinde, aynı birim maliyette onun değerli, satıldığı. Başvuru siparişleri fatura üzerinde satılan miktar aşan miktarın oluşturulmayacak döndüren doğrular.

**Not:** bir satış siparişine referans dönüş satırları düzeltmeleri veya vergilerindeki, satış olarak işlenir. Daha fazla bilgi için "Genel muhasebeye naklet" bölümünde, bu konunun ilerleyen bölümlerinde bkz.

### <a name="charges"></a>Masraflar

Masrafları ve ücretleri iade siparişi bir veya daha aşağıdaki yöntemlerden birini kullanarak eklenebilir:

-   Ücretleri iade sipariş başlığı, iade siparişi satırında veya her ikisi de el ile ekleyebilirsiniz.
-   Giderler iade siparişi başlığına iade neden kodu bir işlevi otomatik olarak eklenebilir.
-   Giderleri satırı değerlendirme koduna göre iade siparişi satırında otomatik olarak eklenebilir.

Giderler sonra iade neden kodu otomatik olarak eklenir veya değerlendirme kod satırına atanır. Neden kodu daha sonra değiştirilen varolan farkı girişi kaldırılmaz, ancak yeni bir ücretsiz giriş eklenebilir, yeni Sebep koduna göre. Masrafları iade siparişi satırları eklediğinizde, satır veya sipariş değerinin bir yüzdesi olarak hesaplanan masraflar yüzde negatif bir sayı değilse satır veya sipariş satırı negatif olduğunda negatif olur. Negatif bir değer içeren bir gider bir kredi için müşteri temsil eder.

### <a name="return-reason-codes"></a>İade neden kodları

Neden kodlarını döndürür uygulayarak iade desenleri analiz kolaylaştırmak yardımcı olabilir. Neden kodları neden öğeleri döndürmek bir müşterinin istediği hakkında bilgi sağlar. Bazı kuruluşlar, birçok sebep kodları vardır. Bu kuruluş, daha iyi bir genel bakış elde etmek için neden kodu gruplar halinde ve birikmiş bildirdiği için sebep kodları gruplayabilirsiniz.

### <a name="disposition-codes-and-disposition-actions"></a>Değerlendirme kodları ve değerlendirme eylemleri

İade siparişi satırında bir değerlendirme kodu varış kayıt parçası olarak iade siparişi işleminde önemli bir adımı atamadır. Değerlendirme kodu aşağıdaki bilgileri belirler:

-   **Mali etkileri** – müşteri iade edilen maddeler için alacaklandırılacak ve tüm giderleri için iade siparişi satırında eklenmelidir?
-   **İade edilen maddeyi eğilimini** – madde olabilir geri stoka eklenen, hurdaya ayrılması veya müşteriye döndürülmelidir?
-   **İade edilen madde Lojistik** – değiştirilen madde verilen müşteriye?

Nasıl, iade edilen malların elden belirleme yanı sıra, değerlendirme kodu iade satırına uygulanacak ücretleri neden olabilir. İstatistiksel analiz için döndürür gruplandırmak için de kullanılabilir. Değerlendirme kodu iade siparişlerini kurulumunun bir parçası olarak tanımlanır. Ancak, her değerlendirme kodu yerleşik değerlendirme eylemlerden birini başvurması gerekir. Aşağıdaki tablo yerleşik değerlendirme kodları ve eylemlerini listeler. **Önemli:** bir öğe değil döndürülmesi gereken, ancak hala müşteri alacak, Ata **yalnızca kredi** dönüş hattı için değerlendirme kodu.

<table>
<thead>
<tr class="header">
<th>Elden çıkarma kodu</th>
<th>Mali etkileri</th>
<th>Lojistik etkileri</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yalnızca alacaklandır</td>
<td><ul>
<li>Müşteri alacak satış fiyatını eksi herhangi bir ücret veya giderler.</li>
<li>Madde nakledilemez gelen zarar genel muhasebeye nakledilir.</li>
</ul></td>
<td>Madde döndürülmelidir değil. Bu değerlendirme eylem için aşağıdaki durumlarda kullanılır:
<ul>
<li>Taraflar arasında yeterli güven yok.</li>
<li>Kusurlu Mal iade maliyet engelleyici olur.</li>
<li>Maddelerin stoka geri izin verilmez. Diğer koşullar nedeniyle fiziksel bir dönüş gerekli deðildir.</li>
</ul></td>
</tr>
<tr class="even">
<td>Alacak</td>
<td><ul>
<li>Müşteri alacak satış fiyatını eksi herhangi bir ücret veya giderler.</li>
<li>İade edilen madde maliyetine göre stok değeri artar.</li>
</ul></td>
<td>Öğe döndürülür ve stoğa geri eklenir.</td>
</tr>
<tr class="odd">
<td>Değiştir ve alacaklandır</td>
<td><ul>
<li>Müşteri alacak satış fiyatını eksi herhangi bir ücret veya giderler.</li>
<li>İade edilen madde maliyetine göre stok değeri artar.</li>
<li>Bir değişiklik için ayrı bir satış siparişi oluşturulur ve ayrı olarak ele alınır.</li>
</ul></td>
<td>Öğe döndürülür ve stoğa geri eklenir.</td>
</tr>
<tr class="even">
<td>Değiştir ve ıskartaya ayır</td>
<td><ul>
<li>Müşteri alacak kaydedilir, herhangi bir ücret veya ücretleri daha az satış fiyatı.</li>
<li>Madde nakledilemez gelen zarar genel muhasebeye nakledilir.</li>
<li>Bir değişiklik için ayrı bir satış siparişi oluşturulur ve ayrı olarak ele alınır.</li>
</ul></td>
<td>Madde iade ve hurdaya çıkarılır.</td>
</tr>
<tr class="odd">
<td>Müşteriye iade et</td>
<td>Hiçbiri, herhangi bir ücret veya giderler hariç.</td>
<td>Öğe döndürülür ancak incelemesinden sonra müşteriye gönderilir. Bu değerlendirme eylem öğesi kasten zarar görmüş veya garanti hükümsüz kullanılabilir.</td>
</tr>
<tr class="even">
<td>Iskarta</td>
<td><ul>
<li>Müşteri alacak satış fiyatını eksi herhangi bir ücret veya giderler.</li>
<li>Madde nakledilemez gelen zarar genel muhasebeye nakledilir.</li>
</ul></td>
<td>Madde iade veya Hurda.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>İnceleme için ambarda varış
Sevk irsaliyesini deftere naklederek iade edilen maddelerin stoka fiziksel olarak almadan önce maddelerin varış kayıt ve isteğe bağlı bir incelemesi ile gitmeniz gerekir. Aşağıdaki resimde, alma işlemine genel bakış sağlar. İzleyen bölümlerde resimde gösterilen her adımı açıklar.  

[![Alma işlemi](./media/salesreturn03.png)](./media/salesreturn03.png)  

Bu konuda ele alınan olmayan birçok çeşitlemeyi işlemi vardır. Bu farklılıkların bazıları şunlardır:

-   Kullanma **varış genel bakış** varış günlüğü oluşturmak için liste. Bunun yerine, varış günlüğü el ile oluşturun. İade siparişleri olacaktır **satış sipariş** referans olarak.
-   Ambar Yönetimi kullanıyorsanız, Paletli taşımalar oluşturur. Dönüş hattı bir durumu olacaktır **gelen** Paletli taşıma sırasında.
-   İade edilen maddeyi doğrudan iade siparişi satırından gelişini kullanarak kaydetme **kayıt** işlev.

Alma işlemi sırasında döndürür ambar varış genel işlemi ile tümleşiktir. Alma işlemi de ayrı bir inceleme yapmak gerekir iade edilen maddeler için karantina siparişlerinin oluşturulmasını destekler.

### <a name="identify-products-in-the-arrival-overview-list"></a>Varış Genel listedeki ürünleri belirlemek

**Varış genel bakış** tüm planlı gelen Varışlar sayfasında listelenir. **Not:** iade siparişlerini varışları işlenmelidir ayrı ayrı varış hareketlerinin diğer türlerinden. Gelen bir paket tanımladığınız sonra **varış genel bakış** (örneğin, eşlik eden RMA belge kullanarak) sayfasında eylem bölmesinde,'ı **Başlat varış** oluşturmak ve varış eşleşen bir varış günlüğü başlatmak için.

### <a name="edit-the-arrival-journal"></a>Gelen maddeler günlüğü Düzenle

Ayarlayarak **Karantina yönetimi** için seçenek **Evet**, dönüş hattı için bir karantina siparişi oluşturabilirsiniz. Bir satır incelemesi için karantina gönderildiyse, değerlendirme kodu belirtemezsiniz. **Not:** ayarlarsanız **Karantina yönetimi** için seçenek **Evet**, maddenin stok model grubu, **Karantina yönetimi** üzerindeki option **günlük satırlarını** sayfa varış günlüğü satırı için işaretlenir ve değiştirilemez. Karantina satırı gönderirse, uygun karantina ambarına belirtmeniz gerekir. Varış satırı incelemesi için gönderilen değil, ambar varış memuru doğrudan varış günlüğü satırında değerlendirme kodu belirtin ve sonra varış günlüğü nakledin. Aynı değerlendirme kodu iade satırının tamamını miktar atanmaması gereken veya satırın tam miktarı almadı, Satırı Böl gerekir. Bir varış günlüğü satırında böldüğünüzde, dönüş hattı da bölme (**SalesLine**) ve yeni bir lot kodu oluşturun. Varış günlüğü satırının miktarını azaltarak satırını bölebilirsiniz. Günlüğü deftere naklettiğinizde, yeni bir iade satır durumu olan oluşturulur **beklenen** kalan miktar için. ' İ tıklatarak satır bölebilirsiniz **işlevler**&gt;**bölme**.

### <a name="process-the-quarantine-order"></a>Karantina siparişi işlemek

İade edilen ürün inceleme ve karantina ambarında gönderilirse, bir karantina siparişi herhangi bir ek işlem tamamlanır. Karantina gönderilen her varış satırı için bir karantina siparişi oluşturulur. Değerlendirme kodu denetleme işleminin sonucunu gösterir. Yalnızca varış günlüğü bölebilirsiniz gibi bir karantina siparişi bölebilirsiniz. Karantina siparişi böl, İade satırının karşılık gelen bölme neden. Kullanarak değerlendirme kodu girildikten sonra karantina siparişi tamamlamak **son** işlevi veya **tamamlandı bildirimi** işlev. Seçerseniz **tamamlandı bildirimi**, yeni varış belirtilen ambardaki oluşturulur. Kullanarak bu varış sonra işleyebilir **varış genel bakış** sayfa. Varış bir karantina siparişinden kaynaklanıyorsa, inceleme sırasında atanan değerlendirme kodu değiştiremezsiniz. Karantina emri kullanarak tamamlarsanız **son** lot işlevini otomatik olarak kaydedilir. Bazen, bir madde sevkiyat ve departman almakla karantinadan geri gönderilebilir. Örneğin, maddeyi stokta depolanacağı konumu karantina denetçisi anlayamazlar. Bu durumda, ilgili sevk irsaliyesi doğru kaydetmek ve karantina nedeniyle belirtilen değerlendirme kodu üzerinde çalışmak için güncelleştirilmesi gerekir. Dönüş hattı kaydedildiğinde alındı bildirimi müşteriye gönderilir. **İade onayını** raporu iade siparişi belgesine benzer. **İade onayını** rapor günlüğe veya aksi takdirde sistemde kayıtlı değildir ve iade siparişi işlemi zorunlu bir adım değildir.

## <a name="replace-a-product"></a>Bir ürünü Değiştir
Ürün değişimi yönetmek için iki yöntem vardır:

-   **Yenileme siparişi oluşturuldu** – müşteriden iade edilen ürün alınmadan önce bir ürün değiştirin.
-   **Değerlendirme kodu tarafından değiştirme** – otomatik olarak yeni bir değişiklik sipariş satırı oluşturun.

### <a name="up-front-replacement"></a>Yenileme siparişi oluşturuldu

İade edilen madde önce yenileme siparişi oluşturuldu değiştirilen madde müşteriye teslim edilebilir. Madde yedek parça onun yerini almaya kullanılabilir değilse, kaldırılamayan bir makine parçası ise, örneğin, ya da yalnızca müşteri başka bir ürünle olabildiğince çabuk olmasını istiyorsanız bu yöntem yararlıdır. Yenileme siparişi oluşturuldu bağımsız bir satış siparişi sırasıdır. Üstbilgiye ilişkin bilgiler müşteriden başlatılır ve satır bilgileri iade siparişinden başlatılır. Düzenleme, işleme ve değiştirme siparişi iade siparişi bağımsız olarak silin. Değiştirme Siparişi sildiğinizde, siparişi değiştirme siparişi oluşturulmuş bir ileti alırsınız. Eylemli değiştirme işlemi aşağıdaki çizimde gösterilmektedir.  

[![Eylemli değiştirme işlemi](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

İade Siparişi değiştirme siparişi için bir başvuru içerir. Kusurlu Mal döndürülmeden önce eylemli değiştirme siparişi iade siparişi için oluşturulmuşsa, kusurlu mal geri döndükten sonra değişikliği için değerlendirme kodu seçemezsiniz.

### <a name="replacement-by-disposition-code"></a>Değerlendirme kodu olarak değiştirme

Değiştirilen Madde müşteriye sevk ve kullandığınız **Değiştir ve hurda** veya **Değiştir ve kredi** değerlendirme eylem iade siparişi, aşağıdaki çizimde gösterilen işlemi kullanın.  

[![Değerlendirme kodu kullanıldığında değiştirme işlemi](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Değiştirilen Madde kullanarak bağımsız bir satış siparişine, yeni satış siparişi teslim edilecektir. Bu satış siparişi iade siparişi için sevk irsaliyesi oluşturulduğunda oluşturulur. Sipariş başlığı bilgileri başvurulan müşteriden iade siparişi başlığındaki kullanır. Girilen bilgilerden satır bilgilerini toplanan **değiştirilen madde** sayfa. **Değiştirilen madde** sayfa doldurulmuş olmalı "Değiştir" sözcüğüyle başlayan değerlendirme Eylemler sahip satırlar için Ancak, miktar ya da değiştirilen madde kimliği doğrulanmış sınırlı veya. Bu davranış, burada tamamen farklı bir öğe müşterilerin istediği nerede aynı madde Müşterinin istediği durumlarda ancak farklı bir yapılandırma veya boyutu ve servis talepleri de verir. Varsayılan olarak, aynı öğe girilen **değiştirilen madde** sayfa. Ancak, işlev ayarlanmış olması koşuluyla, farklı bir öğeyi seçebilirsiniz. **Not:** düzenleme ve değişiklik satış siparişi oluşturulduktan sonra silin.

## <a name="generate-a-packing-slip"></a>Sevk İrsaliyesi Oluştur
İade edilen maddelerin stoka alınmadan önce ait öğeleri siparişi için sevk irsaliyesini güncelleştirmeniz gerekir. Sadece fatura güncelleştirme işlemini güncelleştirme mali hareketin olduğu gibi sevk irsaliyesi güncelleştirmesi fiziksel envanter kaydı güncelleştirme işlemidir. Diğer bir deyişle, bu işlem, stokta yapılan değişiklikleri kaydeder. İadeler söz konusu olduğunda, değerlendirme eylemine atanan adımları sevk sırasında uygulanır irsaliyesi güncelleştirmesi. Sevk irsaliyesi oluşturduğunuzda aşağıdaki olaylar gerçekleşir:

-   Ambarda, standart işlem fiziksel giriş yapmak için kullanılır. Stok modeli grubu, genel muhasebe nakilleri oluşturulur (**Fiziksel stoğun deftere nakli**) ve Accounts receivable parameters (**sevk irsaliyesini genel muhasebeye naklet**) uygun şekilde ayarlayın.
-   "Iskarta" sözcüğünü içeren bir değerlendirme eylemi ile işaretlenmiş maddeler ıskartaya ve stok zararı genel muhasebeye nakledilir.
-   İle işaretli öğeler **dönüş için müşteri** değerlendirme eylem aldı ve müşteriye teslim. Bu öğeler, stoktaki net etkisi yoktur.
-   Değişiklik satış siparişi oluşturulur. Bu satış siparişi üzerindeki bilgiyi temel alan **değiştirilen madde** sayfa.

Sevk irsaliyesi İade durumuna sahip satırlar için oluşturabileceğiniz **kayıtlı**ve yalnızca dönüş hattı üzerinde tam miktarı. İade siparişi birden fazla satır varsa, **kayıtlı** durumu, diğer satırları silerek bir alt kümesi satırları için sevk irsaliyesi oluşturabilir **İrsaliyeyi Kaydet** sayfa. İade siparişi sevk irsaliyelerini açısından değil, iade siparişi satırları açısından kısmi döndürür tanımlanır. Bu nedenle, iade siparişi satırında gösterilen tam miktarı alır, ancak hiçbir şey iade siparişinin diğer satırlardan aldığınız teslimatı kısmi teslimat değil. Ancak, iade siparişi satırında bir maddenin 10 birim verilmesini gerektirir, ancak yalnızca dört birim almak, teslimat kısmi teslimat olur. Aksi takdirde beklenen tüm iade maddeler ulaşmış olan, sevk irsaliyesi bir kenara bırakmanızı ve ulaşması için iade edilen miktarı geri kalanı için bekleyin. Alternatif olarak, kaydetmek ve kısmi miktar deftere nakledin. Sevk irsaliyeleri deftere nakil işleminin bir parçası, müşterinin sevkiyat belgelerden sevk irsaliyesi referans numarasını içeren sipariş satırları ilişkilendirebilirsiniz. Bu ilişki isteğe bağlıdır ve yalnızca başvuru amaçlıdır. Bu işlem güncelleştirmeleri oluşturmaz. Genel olarak, ambalaj atlayabilirsiniz irsaliyesi işlemi ve faturalama için doğrudan gidin. Bu durumda, faturalama sırasında sevk irsaliyesi oluşturma sırasında yapacağı adımları tamamlanır.

## <a name="generate-an-invoice"></a>Bir fatura oluştur
Ancak **iade siparişi**, iade siparişi, özel Lojistik yönleri işlemek için gereken eylemler ve bilgi sayfasını içeren kullanmanız gerekir **satış siparişi** faturalama işlemini tamamlamak için sayfa. Kuruluşunuzun sonra iade siparişleri ve satış siparişleri aynı anda fatura kesebilirsiniz ve aynı kişi gerektiği gibi faturalama işlemini tamamlayabilirsiniz. İade siparişi görüntülemek için **satış sipariş** sayfasında, ilgili satış siparişi açmak satış siparişi numarası bağlantısını tıklatın. İade siparişi üzerinde bulabilirsiniz **tüm satış siparişleri** sayfa. İade siparişleri olan bir sipariş türüne sahip satış siparişleri **siparişi iade**.

### <a name="credit-correction"></a>Alacak düzeltme

Faturalama işleminin bir parçası olarak, tüm sair giderleri doğru olduğundan emin olun. Genel muhasebe nakilleri düzeltmeleri (Storno) hale gelmesine neden için kullanmayı düşünün **alacak düzeltmesi** üzerindeki option **diğer** sekmesinde **Fatura deftere nakil** sayfa fatura/alacak dekontunu naklettiğinizde. **Not:** varsayılan olarak, **alacak düzeltmesi** seçeneği etkinleştirilirse, **düzeltme olarak alacak dekontu** üzerindeki option **Accounts receivable parameters** sayfası etkinleştirildi. Ancak, Storno değil post döndürür önerilir.

## <a name="create-intercompany-return-orders"></a>Şirketlerarası iade siparişleri oluşturma
Kuruluşunuz içindeki iki şirket arasındaki iade siparişlerini tamamlanabilir. Aşağıdaki senaryoları desteklenir:

-   Şirketlerarası bir ilişkisinde yer alan iki şirket arasındaki basit şirketlerarası döndürür
-   Satış yapan şirketin müşterinin iade siparişi oluşturulduğunda kurulan bir şirketlerarası zinciri
-   Satın alma şirkette bir satıcıya iade siparişi oluşturulduğunda kurulan bir şirketlerarası zinciri
-   Harici bir müşteri şirketlerarası bir ilişkisinde yer alan iki şirket arasındaki doğrudan teslim sevkiyat döndürür

### <a name="setup"></a>Kurulum

Minimum kurulum aşağıdaki çizimde, iki şirket için şirketlerarası bir ilişkisinde katılır ve şirketlerarası ticaret yararlanmak gereklidir.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Aşağıdaki senaryoda, CompBuy şirket satın alma ve CompSell satan şirket. Genellikle, satış yapan şirketin malları satın alan şirkete veya, sevk irsaliyesi senaryolarda doğrudan teslim, ve son müşteriye doğrudan gelir. CompBuy, satıcıya ŞA'de\_CompSell CompSell şirket ile ilişkili şirketlerarası son nokta olarak tanımlanır. Aynı anda, CompSell, müşterinin ŞA\_CompBuy CompBuy şirket ile ilişkili şirketlerarası son nokta olarak tanımlanır. Uygun eylemi ilke ayrıntılarını ve değer eşlemeleri her iki şirkette de tanımlanması gerekir. Doğrudan teslim sevkiyat senaryosunda, satış şirketi de şirketlerarası satış siparişi olan bir şirketlerarası iade siparişi oluşturulur. RMA numarası şirketlerarası iade siparişinin CompSell RMA numara serisinden çekilebilir veya CompBuy orijinal iade siparişine atanan RMA numarası alanından kopyalanabilir. RMA numarası ayarları üzerinde **PurchaseRequisition** CompBuy eylem ilkesi bu eylemleri belirler. RMA numarası eşitlenmişse, iki şirketin aynı numara sırasını kullanırsanız, numara çatışmayı riskini azaltmak planlamalısınız.

### <a name="simple-intercompany-returns"></a>Basit şirketlerarası döndürür

Bu senaryo, aşağıdaki çizimde gösterildiği gibi iki şirket aynı kuruluşta ilgilidir.  

[![Basit şirketlerarası dönüş](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Sipariş zinciri şirket satın alma bir satıcıya iade siparişi oluşturulduğunda veya müşteri iade siparişi satış şirketi oluşturulur kurulabilir. Dynamics 365 işlemleri için diğer şirkette karşılık gelen sipariş oluşturur ve başlığı ve satır bilgileri Satıcı siparişi iade siparişi üzerindeki Müşteri yansıtan dönmek emin olur. Kurulan iade siparişi dahil veya hariç başvuru (**satış siparişini bulmak**) için varolan bir müşteri fatura. Sevk irsaliyelerini ve faturaları iki siparişlerinin ayrı ayrı işlenebilir. Örneğin, müşteri iade siparişi için sevk irsaliyesini oluşturmadan önce satıcıya iade siparişi için sevk irsaliyesini oluşturmak zorunda değilsiniz.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Üç taraflar arasında doğrudan teslim sevkiyat döndürür

Bu senaryo bir önceki satışının ise kurulan **doğrudan teslim** türü tamamlandı ve faturaya karşı ise müşteri etkileşim kurduğu şirkette müşteriyle vardır. Aşağıdaki çizimde, CompBuy şirket daha önce satılan ve ürünleri dış müşteriye Faturalanan. Ürünleri doğrudan şirketten CompSell müşteri şirketlerarası sipariş zinciri yoluyla sevk edildiği.  

[![Üç taraflar arasında doğrudan teslim sevkiyat döndürür](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Dış müşteri ürünleri iade etmek isterse, müşteri şirkete CompBuy (RMA02) iade siparişi oluşturulur. Şirketlerarası zincir oluşturmak için iade siparişi doğrudan teslim için işaretlenmelidir. Kullandığınızda **satış siparişini bulmak** dönmek için müşteri fatura almak için işlevi aşağıdaki belgelerin oluşan bir şirketlerarası sipariş zinciri kuruldu:

-   **Orijinal sipariş iadesi:** RMA02 (CompBuy şirket)
-   **Satınalma siparişi:** PO02 (CompBuy şirket)
-   **İade siparişi şirketlerarası:** RMA\_00032 (şirket CompSell)

Doğrudan teslim Şirketlerarası zincir oluşturulduktan sonra tüm fiziksel işleme ve döner işlenmesini şirketlerarası iade siparişi, RMA bağlamında olmalıdır\_00032 CompSell şirkette. Ürünleri CompBuy şirkette alınamaz. Değerlendirme kodu iade siparişine şirketlerarası atandığında, özgün sırasını uygun faturalandırılmasına izin vermek için özgün iade siparişi ile eşitlenir.

## <a name="post-to-the-ledger"></a>Genel muhasebeye nakil
İade siparişi faturalandığında, oluşturulan genel muhasebe nakilleri birkaç önemli ayarları ve parametreleri etkilenir:

-   **İade maliyet fiyatı** – diğerinden daha stok modelleri için **standart maliyet**, **iade maliyet fiyatı** parametre stoğa geri kabul veya ıskartaya maddenin maliyetini belirler. Doğru bir stok değerlemesi hesaplamak için ayarladığınız önemli olduğunu **iade maliyet fiyatı** parametresi doğru. Kullanırsanız, **satış siparişini bulmak** bir başvuru yapan bir müşteri fatura bir iade siparişi satırı oluşturmak için işlev **iade maliyet fiyatı** değeri satılan madde maliyet fiyatına eşittir. Aksi durumda, maliyet fiyatı değer madde kurulumundan gelir veya el ile girilebilir.
-   **Kredi düzeltme/Storno** – **alacak düzeltmesi** parametresi **Fatura deftere nakil** sayfa pozitif (DR/CR) girişleri veya düzeltme olarak kaydedilmiş, negatif girişler deftere nakilleri olup olmayacağını belirler.

İzleyin örneklerde, iade maliyet fiyatı olarak temsil edilen **fatura maliyet fiyatı**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Örnek 1: İade siparişi Müşteri Fatura başvuru değil

İade siparişi, Müşteri Fatura başvuru değil. İade edilen maddeyi alacak kaydedilir. **Kredi düzeltme** iade siparişi, fatura veya alacak dekontu oluşturulduğunda parametresi seçili değildir.  

[![İade siparişi, müşteri invoic başvuru değil](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Not:** için varsayılan değer olarak kullanılan madde ana fiyat **iade maliyet fiyatı** parametre. Varsayılan fiyat, stok çıkışı anında maliyet fiyatından farklı. Bu nedenle, dolaylı 3 kaybı sonucunda olur. Ayrıca, iade siparişi satış siparişindeki müşteriye verilen iskonto içermez. Bu nedenle, aşırı bir kredi oluşur.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Örnek 2: İade siparişi için kredi düzeltme seçilir

Örnek 2 örnek 1, aynı olan ancak **alacak düzeltmesi** parametre iade siparişi Fatura oluşturulduğunda seçilen.  

[![İade siparişi alacak düzeltmesi seçildiği](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Not:** genel muhasebe nakilleri düzeltme negatif olarak girilir.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Örnek 3: İade siparişi satırında satış siparişi Bul işlevi kullanılarak oluşturulan

Bu örnekte, iade siparişi satırında kullanılarak oluşturulan **satış siparişini bulmak** işlev. **Kredi düzeltme** Fatura oluşturulduğunda, parametre seçili değildir.  

[![Satış siparişi Bul kullanılarak oluşturulan sipariş satırı döndürür](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Not:****indirim** ve **iade maliyet fiyatı** doğru biçimde ayarlanır. Bu nedenle, müşteri fatura tam tersi gerçekleşir.


