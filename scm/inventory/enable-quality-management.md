---
title: "Kalite yönetimine genel bakış"
description: "Bu makalede, tedarik zincirinizde ürün kalitesini artırmak için Microsoft Dynamics 365 for Finance and Operations'daki kalite yönetimini nasıl kullanabileceğiniz açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: c2c7a9c82809bd989eb362995dfe8e6d7829e89d
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="quality-management-overview"></a>Kalite yönetimine genel bakış

[!include[banner](../includes/banner.md)]


Bu makalede, tedarik zincirinizde ürün kalitesini artırmak için Microsoft Dynamics 365 for Finance and Operations'daki kalite yönetimini nasıl kullanabileceğiniz açıklanmaktadır.

Kalite Yönetimi, uyumsuz ürünler,, kendi başlangıç noktalarını dikkate almadan işleyecek döngü sürelerini yönetmenize yardımcı olabilir. Tanı türleri düzeltme raporlaması ile bağlantılı olduğundan, Microsoft Dynamics 365 for Finance and Operations sorunları düzeltmek ve oluşmalarını önlemek için görevleri zamanlayabilir.

Uygunsuzluğu yönetmek için daha fazla işlevselliğe ek olarak, Kalite Yönetimi sorun türüne göre sorunları (hatta iç sorunları) izlemek için ve çözümleri kısa vadeli veya uzun vadeli olarak tanımlamak için işlev içerir. Anahtar performans göstergeleri (APG) ile ilgili istatistikler, önceki uygunsuzluk sorunlarının geçmişi ve bunları düzeltmek için kullanılan çözümler hakkında bir anlayış sağlar. Önceki kalite ölçülerinin geçmişteki etkilerini incelemek ve ileride kullanılmaya uygun önlemleri belirlemek için geçmişe dönük verileri kullanabilirsiniz.

Bir kalite ilişkisi ayarladığınızda, Finance and Operations çeşitli iş süreçleri, olaylar ve koşullar için kalite emirleri oluşturabilir. Kalite ilişkisi, belirli bir madde, belirli bir madde grubu veya tüm öğeleri kapsayabilir.

## <a name="examples-of-the-use-of-quality-management"></a>Kalite yönetimi kullanımına örnekler
Kalite Yönetimi esnektir ve tedarik zinciri işlemlerinin belirli düzeylerdeki gereksinimlerini karşılamak için çeşitli şekillerde uygulanabilir. Aşağıdaki örneklerde, bu özelliklerin olası kullanımı gösterilmektedir:

-   Önceden tanımlanmış ölçütlere (belirli bir satıcı satınalma siparişinden, ambar kaydı) dayalı bir kalite kontrol işlemini otomatik olarak başlatın.
-   Onaylanmamış stokun kullanılmasını engellemek için inceleme sırasında stoku bloklayın(Tüm satınalma siparişi miktarlarını engelleme).
-   Madde örneklemeyi kalite ilişkilendirmesinin bir parçası olarak, denetlenmesi gereken geçerli fiziksel stok miktarını tanımlamak için kullanın. Örnekleme miktar veya yüzde tabanlı olabilir. 
-   Kısmi alış irsaliyeleri için kalite emirleri oluşturun. Bir siparişten fiziksel olarak alına miktara bağlı olarak oluşturulan bir kalite emri oluşturmak için **Madde örnekleme** formundaki **Güncelleştirilen miktar başına** onay kutusunu seçmelisiniz. 
-   Minimum, maksimum ve hedef test değerleri içeren test türleri oluşturun ve doğrulama sonuçları önceden tanımlanmış olan niteliğe karşı nicelik sınamaları gerçekleştirin.
-   Kalite Ölçüm toleranslarını kontrol etmek için bir kabul edilebilir kalite düzeyi (AQL) belirtin.
-   Denetleme işlemi için gereken test alanı ve test aletleri gibi kaynakları belirtin.

## <a name="working-with-quality-associations"></a>Kalite ilişkileri ile çalışmak
Kalite ilişkisini kullanan iş süreci, satınalma siparişleri, satış siparişleri veya üretim emirleri gibi çeşitli kaynak belgelere ilişkili olabilir. 

Her kalite bağlantısı kaydı oluşturulan kalite emirlerine geçerli olacak testler kümesini, AQL'yi ve örnek alma planını da tanımlamaktadır. Bir iş sürecindeki her değişim için bir kalite ilişkisi kaydı tanımlamanız gerekir. Örneğin, bir satınalma siparişi ürün alış irsaliyesi güncelleştirildiğinde, kalite emri oluşturacak bir kalite ilişkisi ayarlayabilirsiniz. Yürütme planı kurulumuna bağlı olarak, açık bir kalite emri yok ya da satınalma siparişi faturalama gibi sonraki işlemler, engellenen tetikleyici işlem engellenebilir. 

**Not:** Açık kalite emirleri olduğunda, stok miktarlarının çıkarılması otomatik olarak engellenir. **Madde örnekleri** sayfasında bulunan **Tam engelleme** ayarına bağlı olarak, miktar kalite emrindeki miktardır ya da kaynak belge satırındaki miktardır. 

Bir iş süreci için, kalite ilişkisi kaydı, kalite emrinin oluşturulduğu olay ve koşulları tanımlar. Koşullar bir siteye veya bir tüzel kişiliğe özel olabilir. Bozucu testler içeren bir kalite emri yalnızca olay için eldeki stok bulunması durumunda oluşturulabilir. 

Aşağıdaki örnekler, her iş sürecindeki değişiklikler için bir kalite bağlantısını tanımlamayı açıklar. Her örnek için, aşağıdaki tablo kalite ilişki kaydındaki olayları ve durumları özetler.

<table>
<tbody>
<tr>
<th>Referans türü</th>
<th>Olay türü</th>
<th>Yürütme</th>
<th>Olay durdurma</th>
<th>Belge başvurusu</th>
</tr>
<tr>
<td>Stok</td>
<td>Geçerli değil</td>
<td>Geçerli değil</td>
<td>Yok</td>
<td>Tümü</td>
</tr>
<tr>
<td rowspan="7">Satışlar</td>
<td rowspan="4">Malzeme çekme işlemi planlandı</td>
<td rowspan="4">Önce</td>
<td>Yok</td>
<td rowspan="22">Belirli Kimlik, Grup veya Yalnızca tümü</td>
</tr>
<tr>
<td>Malzeme çekme işlemi</td>
</tr>
<tr>
<td>Sevk irsaliyesi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="3">Sevk irsaliyesi</td>
<td rowspan="3">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Sevk irsaliyesi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="15">Satınalma</td>
<td rowspan="7">Giriş listesi</td>
<td rowspan="4">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Giriş listesi</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="3">Sonra</td>
<td>Yok</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="3">Kayıt</td>
<td rowspan="3">Geçerli değil</td>
<td>Yok</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="5">Ürün girişi</td>
<td rowspan="3">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="2">Sonra</td>
<td>Yok</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="8">Üretim</td>
<td rowspan="3">Kayıt</td>
<td rowspan="3">Geçerli değil</td>
<td>Yok</td>
<td rowspan="12">Tümü</td>
</tr>
<tr>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="5">Tamamlandı bildirimi</td>
<td rowspan="3">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="2">Sonra</td>
<td>Yok</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="4">Karantina</td>
<td rowspan="3">Tamamlandı bildirimi</td>
<td rowspan="2">Önce</td>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td>Sonra</td>
<td>Bitir</td>
</tr>
<tr>
<td>Bitir</td>
<td>Önce</td>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="3">Rota operasyonu</td>
<td rowspan="3">Tamamlandı bildirimi</td>
<td rowspan="2">Önce</td>
<td>Yok</td>
<td rowspan="3">Belirli Kimlik, Grup veya Tümü ve Kaynağa özel, Grup veya Tümü</td>
</tr>
<tr>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Sonra</td>
<td>Yok</td>
</tr>
<tr>
<td rowspan="3">Ortak ürün üretimi</td>
<td>Kayıt</td>
<td>Geçerli değil</td>
<td rowspan="3">Yok</td>
<td rowspan="3">Tümü</td>
</tr>
<tr>
<td rowspan="2">Tamamlandı bildirimi</td>
<td>Önce</td>
</tr>
<tr>
<td>Sonra</td>
</tr>
</tbody>
</table>

Aşağıdaki tabloda belirli türde işlemler için kalite emirlerinin nasıl oluşturulabileceği hakkında daha fazla bilgi sağlar.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>İşleme türü</th>
<th>Kalite emirlerinin ne zaman otomatik olarak oluşturulabileceği</th>
<th>Bozucu sınama yapılması gerekirse kalite emirlerinin ne zaman oluşturulabileceği</th>
<th>Koşul bilgisi</th>
<th>El ile oluşturma bilgisi</th>
</tr>
<tr>
<td>Satın alma siparişi</td>
<td>Alınan malzeme için ürün girişi ya da giriş listesi nakledildikten önce veya sonra.</td>
<td>Alınan malzeme için ürün girişi nakledildikten sonra, çünkü malzemenin bozucu test için mevcut olması gerekmektedir.</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir satınalma siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Karantina emri</td>
<td>Karantina siparişi tamamlandı veya sona erdi olarak bildirildikten önce veya sonra.</td>
<td>Yıkıcı testler gerektiren kalite emirleri oluşturulamaz. Karantina siparişi işlevinin, yok edilen malzemenin değerlendirmesini üstleneceği kabul edilir.</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir karantina siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Satış siparişi</td>
<td>Bir zamanlanmış malzeme çekme işlem veya sevk irsaliyesi güncelleştirmesi sevk maddeler için önce</td>
<td>Herhangi bir adımda</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir satış siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Üretim emri</td>
<td>Üretim emri için bitmiş miktar rapor edildikten önce veya sonra</td>
<td>Üretim emri için bitmiş miktar rapor edildikten sonra</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir üretim emrine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Bir rota operasyonuna sahip olan üretim emri</td>
<td>Bir operasyon için bir rapor sona erdikten önce veya sonra</td>
<td>Son operasyon için raporlama üretimi bittikten sonra.</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya operasyon kaynağı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir rota operasyonu gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Stok</td>
<td>Bir kalite emri, transfer emri hareketleri veya bir stok günlüğünde bir hareket için otomatik olarak oluşturulamaz.</td>
<td></td>
<td></td>
<td>Bir kalite emrinin bir maddenin stok miktarı için el ile oluşturulması gerekir. Fiziksel eldeki stok gereklidir.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Kalite yönetim sayfaları
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Sayfa</th>
<th>Açıklama</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kalite ilişkileri</td>
<td>Bu makalenin önceki bölümlerine bakınız.</td>
<td>Bir kalite ilişkisi oluşturulan bir kalite emri için aşağıdaki tüm bilgileri tanımlar:
<ul>
<li>Hareket olayı</li>
<li>Öğeler üzerinde gerçekleştirilmesi gereken test dizileri</li>
<li>Kabul edilebilir kalite düzeyi</li>
<li>Örnekleme planı</li>
</ul>
Kalite emirlerinin otomatik olarak oluşturulmasını gerektiren iş işlemindeki her farklılık için bir kalite eşleştirmesi tanımlamanız gerekmektedir. Örneğin, satınalma siparişleri, karantina siparişleri, satış siparişleri ve üretim emirleri için iş süreçlerinde bir kalite emri oluşturulabilir.</td>
</tr>
<tr class="even">
<td>Testler</td>
<td>Ürünlerinizin kalite belirtimlerini sağlayıp sağlamadığını belirleyen tek tek testler tanımlamak ve görüntülemek için bu sayfayı kullanın. Bir veya daha çok bireysel testleri bir test grubuna atayabilirsiniz. Bu durumda, kabul edilebilir ölçüm değerleri gibi teste özgü bilgileri de belirtirsiniz. Ölçüm değerleri nicel testleri için kullanılır ve nitel testler için test değişkenleri kullanılır.
<ul>
<li>Nicel bir testin bir test tür <strong>tamsayı</strong> veya <strong>kesir</strong>, ve de atanmış bir ölçüsü vardır. Kalite belirtimleri ve test sonuçları sayı olarak ifade edilir.</li>
<li>Kalite testi, <strong>Seçenek</strong> test tipindedir. Kalite testleri, ölçülmekte olan değişken ve onun numaralandırılmış seçenekleri hakkında ek bilgi gerektirirler. Kalite belirtimleri ve test sonuçları bir sonuca göre ifade edilirler.</li>
</ul></td>
<td>Bir üretim şirketi satınalınan malzeme üzerinde, malzeme kalitesi hakkında bir sayısal test ile ambalaj hasarı üzerine bir kalite testi dahil olmak üzere iki test gerçekleştiriyor. Şirket, test değişkenini (hasarlı ambalaj) ve sonuçlarını tanımlamak için ek bilgiler tanımlıyor. Şirket <strong>Test grupları</strong> sayfasını iki testleri bir test grubuna atamak için ve teste özgü bilgileri belirtmek için kullanır. Test grubu, şirketin iki teste ait test sonuçlarını rapor edebilmesi için bir kalite emrine atanır.</td>
</tr>
<tr class="odd">
<td>Test grupları</td>
<td>Test gruplarını ve test grubuna atanmış bireysel testleri ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın. Üst bölme test gruplarını gösterir ve alt bölme seçili bir test grubuna atanan testleri görüntüler. Test grubuna; örnekleme planı, kabul edilebilir kalite düzeyi ve bozucu test gereksinimi gibi birçok ilke atarsınız. Tek bir testi bir test grubuna atadığınızda, sıra, belgeler ve geçerlilik tarihleri gibi ek bilgiler tanımlarsınız. Nicel bir test için tanımladığınız bilgilere kabul edilebilir ölçüm değerleri de dahildir. Nitel bir test için bu bilgilere test değişkeni ve varsayılan sonuç dahildir. Bir kalite emrine atanan test grubu, belirtilen öğe üzerinde gerçekleştirilmesi gereken testlerin varsayılan kümesini tanımlar. Bununla birlikte, kalite emrindeki testleri değiştirebilirsiniz, ekleyebilir veya silebilirsiniz. Test sonuçları, kalite emrindeki her test için rapor edilir.</td>
<td>Bir üretim şirketi, kalite yönergelerindeki her sapma için bir test grubu tanımlıyor. Çeşitli test grupları, örnekleme planları arasındaki farklılıkları, birlikte gerçekleştirilmesi gereken testler kümesini, kabul edilebilir kalite düzeyini ve diğer etkenleri yansıtır. Nicel testleri için, kabul edilebilir ölçüm değerleri için de farklılıklar vardır. Şirket, kalite kurallarını uygulayabilmek için kalite emirlerini otomatik oluşturabilmek için her kurala bir test grubunu <strong>Kalite ilişkilendirmeleri</strong> sayfasından atar ve ayrıca el ile oluşturulan kalite emirlerine de bir test grubu atar.</td>
</tr>
<tr class="even">
<td>Madde kalite grupları</td>
<td>Bir kalite grubuna atanmış maddeleri veya bir maddeye atanmış kalite gruplarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın. Kalite grubu, maddeler için ortak test gereksinimlerini temsil eder. <strong>Test grupları</strong> sayfasındaki test gereksinimlerini tanımladıktan sonra, kalite emirlerini otomatik olarak oluşturmak için kurallar tanımlayabilirsiniz. İşlemi basitleştirmek için, kuralları her bir öğe için tanımlamanız gerekmez. Bunun yerine, <strong>Kalite ilişkileri</strong> sayfasını kullanarak bir kalite grubu için kurallar tanımlarsınız. Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir kalite grubuna ilgili maddeleri atayabilirsiniz. Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir maddeye bir kalite grubuna ilgili maddeye atabilirsiniz.</td>
<td>Üretim şirketi, gelen denetim için aynı test gereksinimlerine sahip çeşitli hammaddeler satın alıyor. Şirket bir kalite grubu tanımlar ve artından hammaddeler ile ilişkilendirilmiş olan madde numaralarını bu gruba atar. Daha sonra aynı sınama gereksinimleri olan yeni bir hammadde türü şirket tarafından satın alınır. Yeni malzeme için yeni test gereksinimleri ayarlamak yerine, şirket yeni malzeme için madde numarasını mevcut kalite grubuna ekler. Aynı üretim şirketi, aynı üretim testi gereksinimlerine sahip maddeler de üretiyor ve ön sevkiyat testleri için aynı gereksinimlere sahip maddeleri sevk ediyor. Şirket iki ek kalite grubu tanımlıyor ve sonra her gruba ilgili madde numaralarını atıyor.</td>
</tr>
<tr class="odd">
<td>Test değişkenleri</td>
<td>Nitel bir test ile ilişkili değişkenleri görüntülemek ve tanımlamak için bu sayfayı kullanın. Her değişken için olası sonuçları gösteren numaralandırılmış seçenekleri tanımlayın. Testleri tanımlamak için <strong>Testler</strong> sayfasını kullanın. Nitel testler için test türünü <strong>Seçenek</strong> olarak ayarlamanız gerekir. <strong>Test grupları</strong> sayfasını kullanarak bir teste bir test değişkeni atayın.</td>
<td>Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor. Bu inceleme testinin birçok değişkeni vardır. Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir. İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</td>
</tr>
<tr class="even">
<td>Test değişkeni sonuçları</td>
<td>Bir kalite testiyle ilişkili bir test değişkenine ait olası test sonuçlarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın. Her sonuç için bir <strong>geçti</strong> veya <strong>başarısız</strong> oldu durumu atarsınız. <strong>Testler</strong> sayfasında tanımlanan her nitel test için bir değişken ve sonuçlarını tanımlamalısınız. (Kalite testleri için, test türü <strong>Testler</strong> sayfasında <strong>Seçenek</strong> olarak ayarlanmıştır.) <strong>Test grupları</strong> sayfasını kullanıp, bir test değişkenini ve varsayılan sonucu bir kişisel kalite testine atayın.</td>
<td>Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor. Bu inceleme testinin birçok değişkeni vardır. Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir. İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor. Her sonuca <strong>geçti</strong> veya <strong>kaldı</strong> durumu atanır. Her değişkene yönelik denetim testi sırasında, denetçi sonuçlardan birini seçerek test sonucunu rapor ediyor.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Ayrıca bkz.
--------

[Kalite yönetimi işlemleri](quality-management-processes.md)

[Uygunsuzluk yönetiminin etkinleştirilmesi](enable-nonconformance-management.md)




