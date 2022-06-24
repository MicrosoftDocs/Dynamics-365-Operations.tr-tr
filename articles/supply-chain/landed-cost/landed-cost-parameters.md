---
title: Varış yeri maliyeti parametreleri kurulumu
description: Bu makalede; deftere nakil, durum güncelleştirmeleri, numara serileri ve davranış için Son teslim alma maliyeti modülünde kullanılan genel bilgilerin ve yapılandırma ayarlarının nasıl ayarlanacağı açıklanmaktadır.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 99dbe17d4e83c2c75d52ca3fd22a1772d8045355
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871992"
---
# <a name="landed-cost-parameters-setup"></a>Varış yeri maliyeti parametreleri kurulumu

[!include [banner](../../includes/banner.md)]

Deftere nakil, durum güncelleştirmeleri, numara serileri ve davranışa yönelik olarak **Varış yeri maliyeti** modülünde kullanılan genel bilgileri ayarlamak ve yapılandırma ayarlarını yapmak için **Varış yeri maliyeti parametreleri** sayfası kullanılır. Parametrelerin kurulumu tüzel kişilikler arasında paylaşılmıştır ve bir yönetici tarafından değiştirilebilir.

## <a name="open-the-landed-cost-parameters-page"></a>Varış yeri maliyeti parametreleri sayfasını açma

Parametrelerle çalışmak için **Varış yeri maliyeti \> Kurulum \> Varış yeri maliyeti parametreleri**'ne gidin ve alanları aşağıdaki alt bölümlerde açıklandığı gibi ayarlayın.

![Varış yeri maliyeti parametreleri sayfası.](media/landed-cost-parameters.png "Varış yeri maliyeti parametreleri sayfası")

## <a name="general-tab"></a>Genel sekmesi

### <a name="general-fasttab"></a>Genel FastTab

Aşağıdaki tabloda, **Varış yeri maliyeti parametreleri** sayfasının **Genel** sekmesindeki **Genel** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Ayar | Tanım |
|---|---|
| Sevkiyat oranını kullan | Sevkiyat ücreti tanımlanmış bir dönem için ayarlanır ve birden fazla para birimi kullanan malların tahmini maliyetleri için kullanılır. Sevkiyat ücreti kullanmak için bu seçeneği *Evet* olarak ayarlayın. |
| Döviz kuru türü | Bir seyahat ve seyahat maliyetlerinde çoklu para birimi hesaplamaları için kullanılan döviz kurlarının varsayılan koleksiyonu. |
| Satın alma siparişi miktarını güncelleştir | Kullanıcı, satın alma siparişi satırındaki miktarı değiştirirse ne olacağını seçin:<ul><li>**Kabul et**: Seyahat miktarı otomatik olarak ayarlanır.</li><li>**Uyarı**: Satır bir seyahate eklenmişse bir uyarı gösterilir ancak seyahat miktarı güncelleştirilir.</li><li>**Hata**: Satır bir seyahate eklenmişse bir hata iletisi gösterilir ve satın alma siparişi güncelleştirilemez. Bu nedenle, sipariş satırı önce seyahatten kaldırılmalıdır.</li></ul> |
| Karton sayısını otomatik olarak güncelleştir | Bu seçenek *Evet* olarak ayarlandığında, tüm kartonlar bir araya getirilir ve seyahat ile konteyner düzeylerinde gösterilir. *Hayır* olarak ayarlandığında, karton sayısı başlangıçta 0 (sıfır) olarak ayarlanır ve gerektiğinde el ile düzenlenebilir. |

### <a name="costing-fasttab"></a>Maliyet hızlı sekmesi

Aşağıdaki tabloda, **Varış yeri maliyeti parametreleri** sayfasının **Genel** sekmesindeki **Maliyetlendirme** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Ayar | Tanım |
|---|---|
| Deftere nakil belirtimi | Genel muhasebedeki değer ayarlamasını seçin:<ul><li>**Toplam**: Toplam rakam genel muhasebeye nakledilir.</li><li>**Madde grubu**: Ayarlama madde grubu başına belirtilir.</li><li>**Madde numarası**: Ayarlama madde başına belirtilir. Bu değer en fazla ayrıntıyı sağlar.</li></ul> |
| Sıfır maliyete izin ver | Kullanıcı, beklenen seyahat maliyeti için bir değer içermeyen bir seyahat faturası veya satın alma siparişinin maliyet tahminini deftere nakletmeye çalışırsa hata göstermek için bu seçeneği *Hayır* olarak ayarlayın. Hata iletisi, 0 (sıfır) maliyetinin tahsis edilemediğini ve fatura deftere naklinin başarısız olacağını belirtir. Bu durumda, kullanıcı tahmini el ile güncelleştirebilir (veya otomatik maliyeti yeniden yapılandırabilir) ve ardından güncelleştirilmiş değeri çekebilir ya da geçerli değilse maliyeti silebilir.<p>Seyahat maliyetinin boş olmasına izin vermek için bu seçeneği *Evet* olarak ayarlayın. Bu durumda maliyet alanına göre 0 (sıfır) fiyat tahsis edilecektir. Daha sonra bir satıcı maliyet faturası, seyahat alındığında sıfır fiyat maliyetine göre işlenebilir.</p><p>Sıfır fiyat maliyetinin görünmesini önlemek için otomatik maliyet kaydındaki tahmini yapılandırmanızı öneririz. Bu tahmin tam olarak doğru olmasa da varsayılan sıfır maliyetten daha doğru olmalıdır.</p> |
| Düzeltme deftere nakil tarihi | Borç hesapları seyahat maliyeti faturasını deftere naklettiğinizde, kapatmalar tablosu (stok ayarlamaları) da güncelleştirilir. Fatura günlüğündeyken **Seyahat maliyetlerini seçin** sayfasında varsayılan olarak ayarlanan tarihi seçin:<ul><li>**Hareket tarihi**: Günlüğün tarihini (deftere nakil tarihi) kullanın.</li><li>**Satın alma siparişi fatura tarihi**: Stok (satınalma siparişi) faturasının mali deftere nakil tarihini kullanın.</li><li>**Seçili tarih**: Kullanıcı bir deftere nakil tarihi belirtebilir. Tarih boş bırakılırsa ve maliyet faturası deftere nakledildiğinde hala boşsa kullanıcı bir hata alır.</li></ul> |
| Satın alma faturası fişini kullan | Bu seçenek *Evet* olarak ayarlandığında, maliyet tahakkuku hareketleri satın alma faturası için kullanılan fiş numarasını kullanır. *Hayır* olarak ayarlandığında sistem, **Varış yeri maliyeti parametreleri** sayfasının **Numara serileri** sekmesinde ayarlanan **Maliyet tahakkuk fişi** numara serisi için bir sonraki kullanılabilir numarayı kullanır.<p>Bu seçenek yalnızca **Borç hesapları parametreleri** sayfasındaki **Fatura** sekmesinde **Genel muhasebedeki gider hesabına naklet** seçeneği *Evet* olarak ayarlandığında etkili olur.</p> |
| Kliring hesabına el ile deftere nakli engelle | Satıcı fatura günlüğünün Eylem Bölmesinde **İşlevler \> Yolculuk maliyetlerini seç**'i seçerek hareketin bir seyahate bağlanmadığı durumlarda kliring hesabına deftere nakil yapılmasını önlemek için bu seçeneği *Evet* olarak ayarlayın. Seyahat ve kliring hesabının doğru şekilde kapatılabilmesi için bu seçeneği *Evet* olarak ayarlamanızı öneririz. |
| Maliyet türü masraf tahakkuk hesabını kullan | Bu seçenek *Evet* olarak ayarlandığında, **Maliyet türü kodları** sayfasındaki ilgili maliyet türü kodu için yapılandırılan masraf tahakkuku hesabı, maliyetleri gider olarak tahakkuk etmek için kullanılır.<p>Bu seçenek yalnızca **Borç hesapları parametreleri** sayfasındaki **Fatura** sekmesinde **Genel muhasebedeki gider hesabına naklet** seçeneği *Evet* olarak ayarlandığında etkili olur. |
| Düzeltmeleri fark olarak naklet | Bu seçenek *Evet* olarak ayarlandığında, standart işlevsellik geçersiz kılınır ve tahmini maliyetler ile fiili maliyetler arasındaki farklarla ilişkili stok düzeltme hareketleri bir fark hesabına nakledilmeye zorlanır.<p>Bu seçenek *Hayır* olarak ayarlandığında, farklarla ilişkili stok düzeltme hareketleri, maliyetlendirme yönteminin ve maliyet türü kodunun yapılandırmasına göre işlenir. Standart maliyet için farklar fark hesabına nakledilmeye devam eder. Hareketli ortalama (WMA) için farklar fark hesabına veya stoka nakledilir.</p><p>Bu seçenek yalnızca **Borç hesapları parametreleri** sayfasındaki **Fatura** sekmesinde **Genel muhasebedeki gider hesabına naklet** seçeneği *Evet* olarak ayarlandığında etkili olur.</p> |

### <a name="validation-fasttab"></a>Doğrulama hızlı sekmesi

Aşağıdaki tabloda, **Varış yeri maliyeti parametreleri** sayfasının **Genel** sekmesindeki **Doğrulama** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Ayar | Tanım |
|---|---|
| Çoklu maliyet faturaları | Aynı sair gider için bir seyahate, folyoya veya konteynere birden fazla fatura işlenirse nelerin gerçekleşeceğini seçin.<ul><li>**Kabul et**: Sistem birden fazla maliyet faturasına izin vermelidir.</li><li>**Uyarı**: Bir uyarı gösterilir.</li><li>**Hata**: Bir hata iletisi gösterilir.</li></ul> |
| Her folyo için birden fazla satıcı | Bir folyoya birden fazla satıcının satın alma siparişi eklenirse nelerin gerçekleşeceğini seçin.<ul><li>**Kabul et**: Sistem eyleme izin vermelidir.</li><li>**Uyarı**: Bir uyarı gösterilir ancak eylem yine de gerçekleştirilebilir.</li><li>**Hata**: Bir hata iletisi gösterilir ve eylem engellenir.</li></ul><p>Gümrük müşaviriniz veya yerel yasalarınız bu alan için belirli bir değeri zorunlu kılabilir.</p> |
| Çoklu teslimat modu toleransı | Seyahatten farklı bir teslimat şekli kullanan bir satın alma siparişindeki mallar bu yolculuğa eklenirse nelerin gerçekleşeceğini seçin.<ul><li>**Kabul et**: Sistem eyleme izin vermelidir.</li><li>**Uyarı**: Bir uyarı gösterilir ancak eylem yine de gerçekleştirilebilir.</li><li>**Hata**: Bir hata iletisi gösterilir ve eylem engellenir.</li></ul> |
| Çoklu ambar toleransı | Bir seyahat farklı ambarlara teslim edilmesi gereken birkaç sipariş satırı içeriyorsa ne olacağını seçin. Bu sipariş satırları bir veya daha fazla satın alma siparişine yayılmış olabilir.<ul><li>**Kabul et**: Sistem eyleme izin vermelidir.</li><li>**Uyarı**: Bir uyarı gösterilir.</li><li>**Hata**: Bir hata iletisi gösterilir.</li></ul> |
| Hacim eksik | Kullanıcı bir seyahate hacimsiz bir madde eklerse nelerin gerçekleşeceğini seçin.<ul><li>**Kabul et**: Sistem maddeyi kabul etmelidir.</li><li>**Uyarı**: Bir uyarı gösterilir.</li><li>**Hata**: Bir hata iletisi gösterilir.</li></ul><p>Hacimler maliyetleri hesaplamak ve onaylamak için kullanılıyorsa *Uyarı* veya *Hata*'yı seçmenizi öneririz.</p> |
| Seyahat maliyeti olmayan hizmet sağlayıcı | Kullanıcı bir yolculuğa bağlanmamış bir hizmet sağlayıcısının faturasını işlemeye çalışırsa nelerin gerçekleşeceğini seçin. <ul><li>**Kabul et**: Sistem eyleme izin vermelidir.</li><li>**Uyarı**: Bir uyarı gösterilir.</li><li>**Hata**: Bir hata iletisi gösterilir.</li></ul><p>*Uyarı* seçeneğini belirlemenizi öneririz.</p> |

### <a name="defaults-fasttab"></a>Varsayılanlar hızlı sekmesi

Aşağıdaki tabloda, **Varış yeri maliyeti parametreleri** sayfasının **Genel** sekmesindeki **Varsayılanlar** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Ayar | Tanım |
|---|---|
| Günlük adı | *Varış günlüğü oluştur* işlevinin kullanması gereken varsayılan günlüğü seçin. |
| Seyahat durumu | Kullanıcıların sistemde bunun için kiralık bir sevkiyat konteyneri ayarlaması için bir seyahatin sahip olması gereken durumu seçin. Bu eylem genellikle mallar transitte veya giriş/çıkış noktasında olduğunda gerçekleşir. |
| Yolculuk şablonu | Yeni kiralık sevkiyat konteynerleri için kullanılacak varsayılan yolculuk şablonunu seçin. Genellikle kiralama maliyetlerini içeren bir yolculuk şablonu seçersiniz. |
| Hareket | Bir teslimatın fazla/eksik miktarı tanımlanan tolerans dahilindeyse bir taşıma günlüğü otomatik olarak işlenir. Kullanılacak varsayılan taşıma günlüğünü seçin. Seçili taşıma günlüğü adı **Mahsup hesap** alanının bir değeri olmalıdır. |
| Transfer | Eksik teslimat işlendiğinde, kısa giriş miktarı eksik teslimat ambarı için transfer edilir. Kullanılacak varsayılan transfer günlüğünü seçin. |
| Seyahat dışındaki satın alma siparişlerini devre dışı bırak | Bir yolculuğa bağlı olmayan satın alma siparişleri için Varış yeri maliyeti fazla/eksik teslimat işlevini kapatın. |
| Transitteki mallar dışındaki satın alma siparişlerini devre dışı bırak | Transitteki mallar işlevselliğini kullanmayan satın alma siparişleri için Varış yeri maliyeti fazla/eksik teslimat işlevini kapatın. |
| Giriş mehil süresinde transitteki mallar | Bir sevkiyat konteynerinin, fazla ek girişlerin ilgili sevkiyat konteyneri için tamamlanabileceği ilk girişinden sonraki gün sayısını belirtin. |

## <a name="status-updates-tab"></a>Durum güncelleştirmeleri sekmesi

Sistem, her yolculuğun durumunu belirtmek için durum değerlerini kullanır. Seyahat durumu değerleri, seyahat izleme veya periyodik toplu işler aracılığıyla seyahatlere otomatik olarak uygulanabilir. Alternatif olarak seyahati açıp Eylem Bölmesinin **Yönet** sekmesindeki **Seyahat güncelleştirme** grubunda bir durum seçerek bunları el ile uygulayabilirsiniz. 

Dilediğiniz sayıda seyahat durumu değeri oluşturabilirsiniz. Ancak bunlardan dördü, **Varış yeri maliyeti parametreleri** sayfasının **Durum güncelleştirmeleri** sekmesinde özel bir amaç için kullanılmış olarak tanımlanmalıdır. Aşağıdaki tabloda, orada kullanılabilecek alanlar açıklanmıştır.

| Ayar | Tanım |
|---|---|
| Maliyetlendirildi | Bir seyahatin tamamlandığını tanımlayan seyahat durumunu seçin. |
| Transitte | Bir seyahatin transitte olduğunu tanımlayan seyahat durumunu seçin. |
| Maliyetlendirmeye hazır | Bir seyahatin maliyetlendirmeye hazır olduğunu tanımlayan seyahat durumunu seçin. Bu durum, **Seyahat maliyetindeki alacak** alanının *Satıcı* olarak ayarlandığı tüm stok satın alma faturaları ve seyahat için seyahat maliyeti faturaları işlendiğinde kullanılır. Maliyetlendirilen işlemde başarısız olan seyahatler, *Maliyetlendirilmeye hazır* durumuna sahip olacaktır.|
| Önceden maliyetlendirilmiş | Bir yolculuğun önceden maliyetlendirildiğini tanımlayan yolculuk durumunu seçin. Bu durum, maliyetlendikten sonra bir yolculuğa yeni bir maliyet hareketi eklendiğinde kullanılır. İkinci bir navlun faturası veya beklenmeyen bir demuraj ücreti alındığında, daha önce maliyetlendirilen bir yolculuğa yeni maliyet hareketleri eklenebilir. Bu durum, maliyetli bir seyahate yeni bir seyahat maliyeti eklendiğinde otomatik olarak uygulanır. |

## <a name="voyage-creator-tab"></a>Seyahat oluşturucu sekmesi

Aşağıdaki tabloda, **Varış yeri maliyeti parametreleri** sayfasının **Seyahat oluşturucu** sekmesindeki bölümler açıklanmaktadır.

| Bölüm | Tanım |
|---|---|
| Toleranslar | **Dış hacim toleransı** ve **Dış ağırlık toleransı** alanları, malların fazla hacimli ve fazla ağır olarak kabul edildiği eşikleri tanımlar. Bir kullanıcı **Seyahat düzenleyicisi** sayfasına mal eklediğinde, birim veya ağırlık burada ayarladığınız değeri aşarsa sistem bir uyarı gösterir. Her alanın değeri, ilgili sevkiyat konteyneri türü için ayarlanan maksimum hacim veya ağırlığın yüzdesi olarak ifade edilir. Değerin maksimum hacim veya ağırlığın yüzde 5 ila 10'u arasında olmasını öneririz. |
| Folyo oluşturma ayarı | Sistem, seyahat oluşturma işlemi sırasında birden fazla folyo oluşturabilir. Yeni bir folyonun ne zaman oluşturulacağını tanımlamak için bu bölümü kullanın. Bu bölümdeki her satır için sistem belirtilen tabloyu ve alanı denetler ve her benzersiz alan değeri için bir folyo oluşturur. |

## <a name="cost-estimates-tab"></a>Maliyet tahminleri sekmesi

**Varış yeri maliyeti parametreleri** sayfasının **Maliyet tahminleri** sekmesi yalnızca bir alan sağlar: **Varsayılan maliyetlendirme sürümü**. Bu alan yalnızca maliyetlendirme yöntemi *Standart maliyetlendirme* olduğunda geçerlidir. *Madde maliyet fiyatı güncelleştirmesi* periyodik görevi için kullanılacak varsayılan maliyet sürümünü seçin. Yeni bir mali yıl başladığında bu ayarı değiştirmeniz gerekebilir.

## <a name="inventory-dimensions-tab"></a>Stok boyutları sekmesi

Boyutların kullanıldığı her Varış yeri maliyeti sayfasında hangi kullanılabilir stok boyutlarının varsayılan olarak gösterileceğini denetlemek için **Varış yeri maliyeti parametreleri** sayfasının **Stok boyutları** sekmesini kullanırsınız.

Bir boyut seçin ve sonra bu boyutun varsayılan olarak gösterilmesi gereken her sayfa için **Seyahat satırları**, **Transitteki mallar** ve/veya **Maliyet tahminleri** seçeneğini *Evet* olarak ayarlayın. Gerektiğinde diğer boyutlar için bu adımı yineleyin.

Bu sekmedeki ayarlar, tüzel kişilikler arasında belirlenen her sayfa için varsayılan boyutları oluşturur. Ancak belirlenen sayfalardan birinde çalışan kullanıcılar, Eylem Bölmesinde **Stok \> Görüntüleme boyutları**'nı seçerek varsayılan boyutları geçersiz kılabilir.

## <a name="number-sequences-tab"></a>Numara serileri sekmesi

**Varış yeri maliyeti parametreleri** sayfasının **Numara serileri** sekmesi, Varış yeri maliyetinin gerektirdiği ancak tüzel kişilikler arasında paylaşılmayan her referans numara serisinin türünü listeler. Listedeki her referans için bir numara serisi kodu seçin.

> [!NOTE]
> Çok şirketli bir yapılandırmada, her şirket (tüzel kişilik) için farklı numara serileri oluşturulmalıdır.

## <a name="shared-number-sequences-tab"></a>Paylaşılan numara serileri sekmesi

**Varış yeri maliyeti parametreleri** sayfasının **Paylaşılan numara serileri** sekmesi, Varış yeri maliyeti için tüzel kişilikler arasında paylaşılan her referans numara serisi türünü listeler. Şu anda, listede yalnızca bir numara serisi vardır. Bu numara serisi seyahat kimliği için kullanılır.

**Tüm seyahatler** sayfasında, kullanıcılar tüm tüzel kişiliklerdeki tüm seyahatleri görüntüleyebilir. Ancak, bir seyahati düzenlemek ve işlemek için kullanıcıların seçilen kaydın tüzel kişiliğinde olması gerekir.

## <a name="feature-visibility-tab"></a>Özellik görünürlüğü sekmesi

Varış yeri maliyeti, Microsoft Dynamics 365 Supply Chain Management'ta sık kullanılan birkaç sayfaya özellikler (alanlar ve işlevler) ekler. Bu sayfalar satıcı ana verileri, serbest bırakılan ürünler, satın alma siparişleri, transfer emirleri ve ambar kurulumuyla ilgili sayfaları içerir. Varış yeri maliyeti kullanıyorsanız bu özelliklerden yararlanabilmeniz için bunları her yerde görünür hale getirmeniz gerekir. Varış yeri maliyeti kullanmıyorsanız özelliklerin sizi engellememesi için gizleyebilirsiniz.

**Varış yeri maliyeti parametreleri** sayfasının **Özellik görünürlüğü** sekmesinde, Varış yeri maliyeti özelliklerini kullanılabilir oldukları her yerde görünür hale getirmek için **Etkinleştir** seçeneğini *Evet* olarak ayarlayın. Özellikleri Varış yeri maliyeti dışındaki ortak sayfalarda gizlemek için *Hayır* olarak ayarlayın. Ancak seçenek *Hayır* olarak ayarlansa bile, **Varış yeri maliyeti parametreleri** sayfası da dahil olmak üzere modül, erişmek için doğru izinlere sahip kullanıcılar tarafından kullanılabilir olur.
