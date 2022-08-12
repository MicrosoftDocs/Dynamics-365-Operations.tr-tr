---
title: Birleşik ürün deneyimi
description: Bu makale, finans ve operasyon uygulamaları ile Dataverse arasında ürün verileri tümleştirmesini açıklar.
author: t-benebo
ms.date: 06/23/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1546cdaf3c63a7ff9a330ae8609595aaf48fbc48
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111501"
---
# <a name="unified-product-experience"></a>Birleşik ürün deneyimi

[!include [banner](../../includes/banner.md)]



Bir işletmenin ekosistemi Finance, Supply Chain Management ve Sales gibi Dynamics 365 uygulamalarından oluştuğunda, işletmeler sıklıkla ürün verilerini kaynak olarak kullanmak için bu uygulamaları kullanır. Bunun nedeni, bu uygulamaların sofistike fiyatlandırma kavramları ve doğru eldeki stok verileriyle kapsamlı bir ürün altyapısı sağlamasıdır. Ürün verilerinin kaynağı için harici bir Ürün Yaşam Döngüsü Yönetimi (PLM) sistemi kullanan işletmeler, finans ve operasyon uygulamalarındaki ürünleri diğer Dynamics 365 uygulamalarına yöneltebilirler. Birleştirilmiş ürün deneyimi, Dataverse'e tümleşik ürün veri modelini getirir ve böylece Power Platform kullanıcıları dahil tüm uygulama kullanıcıları, finans ve operasyon uygulamalarından gelen zengin ürün verilerinden yararlanabilir.

Sales'den genel ürün veri modeli.

![CE'de ürünler için veri modeli.](media/dual-write-product-4.jpg)

Finans ve operasyon uygulamalarından gelen ürün veri modeli.

![Finans ve operasyon uygulamalarındaki ürünler için veri modeli.](media/dual-write-products-5.jpg)

Bu iki ürün veri modeli aşağıda gösterildiği gibi Dataverse'te tümleştirilmiştir.

![Dynamics 365 uygulamalarındaki ürünler için veri modeli.](media/dual-write-products-6.jpg)

Ürünler için çift yazma tablo eşlemeleri, finans ve operasyon uygulamalarından Dataverse'e neredeyse gerçek zamanlı olarak yalnızca tek yönlü veri akışı sağlamak üzere tasarlanmıştır. Ancak, ürün altyapısı gerektiğinde çift yönlü hale getirilebilecek şekilde açık yapıldı. Microsoft bu yaklaşımı önermemesine karşın kendi sorumluluğunuzda olacak şekilde bunu özelleştirebilirsiniz.

## <a name="templates"></a>Şablonlar

Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir. Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için tablo haritaları koleksiyonu oluşturulur.

Finans ve Operasyon uygulamaları | Diğer Dynamics 365 uygulamaları | Açıklama
-----------------------|--------------------------------|---
[Tüm ürünler](mapping-reference.md#138) | msdyn_globalproducts | Tüm ürünler tablosu, finans ve operasyon uygulamalarında bulunan tüm ürünleri, hem piyasaya sürülen ürünleri hem de piyasaya sürülmeyen ürünleri içerir.
[CDS serbest bırakılan farklı ürünler](mapping-reference.md#213) | Ürün | **Ürün** tablosu, ürünü tanımlayan sütunları içerir. Bağımsız ürünleri (alt tür ürünü olan ürünler) ve ürün çeşitlerini içerir. Aşağıdaki tablo eşlemeleri göstermektedir.
[Renkler](mapping-reference.md#170) | msdyn\_productcolors
[Konfigürasyonlar](mapping-reference.md#171) | msdyn\_productconfigurations
[Varsayılan sipariş ayarları](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Ürün kategorileri](mapping-reference.md#166) | msdyn_productcategories | Her bir ürün kategorisi ve bunların yapısı ve özellikleri hakkında bilgiler ürün kategorisi tablosunda bulunur.
[Ürün kategorisi atamaları](mapping-reference.md#167) | msdyn_productcategoryassignments | Ürünü bir kategoriye atamak için ürün kategorisi atamaları tablosu kullanılabilir.
[Ürün kategori hiyerarşileri](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Ürünleri kategorize etmek veya gruplamak için ürün hiyerarşilerini kullanabilirsiniz. Kategori hiyerarşileri, Ürün kategorisi hiyerarşisi tablosu kullanılarak Dataverse'te kullanılabilir.
[Ürün kategori hiyerarşisi rolleri](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Ürün hiyerarşileri D365 finans ve operasyon uygulamalarındaki farklı roller için kullanılabilir. Her rolde hangi kategorinin kullanıldığını belirtmek için ürün kategorisi rol tablosu kullanılır.
[Ürün varsayılan sipariş ayarları V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Ürün boyut grupları](mapping-reference.md#173) | msdyn\_productdimensiongroups | Ürünü hangi ürün boyutlarının tanımlayacağı tanımlayan ürün boyutu.
[Ana ürün renkleri](mapping-reference.md#187) | msdyn_sharedproductcolors | **Paylaşılan ürün rengi** tablosu, belirli bir ana ürünün sahip olabileceği renkleri gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
[Ana ürün yapılandırmaları](mapping-reference.md#188) | msdyn_sharedproductconfigurations | **Paylaşılan ürün yapılandırması** tablosu, belirli bir ana ürünün sahip olabileceği yapılandırmaları gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
[Ana ürün boyutları](mapping-reference.md#190) | msdyn_sharedproductsizes | **Paylaşılan ürün boyutu** tablosu, belirli bir ana ürünün sahip olabileceği boyutları gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
[Ana ürün stilleri](mapping-reference.md#191) | msdyn_sharedproductstyles | **Paylaşılan ürün stili** tablosu, belirli bir ana ürünün sahip olabileceği stilleri gösterir. Bu kavram, verileri tutarlı tutmak amacıyla Dataverse'a taşınır.
[Ürün Numarası Tanımlanan Barkod](mapping-reference.md#164) | msdyn\_productbarcodes | Ürün barkodları, ürünleri benzersiz olarak tanımlamak için kullanılır.
[Ürüne özel birim dönüşümleri](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Serbest bırakılan ürünler V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails** tablosu, ürünü tanımlayan finans ve operasyon uygulamalarından gelen ve ürünün mali ve yönetim bilgilerini içeren sütunları içerir.
[Boyutlar](mapping-reference.md#174) | msdyn\_productsizes
[Depolama boyut grupları](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Ürün depolama boyutu grubu, ürünün ambarda yerleşimini tanımlamak için kullanılan yöntemi temsil eder.
[Stiller](mapping-reference.md#178) | msdyn\_productstyles
[İzleme boyutu grupları](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Ürün izleme boyutu grubu, ürünü stokta izlemek için kullanılan yöntemi temsil eder.
[Birimler](mapping-reference.md#219) | uoms
[Birim dönüştürmeleri](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Ürünlerin tümleştirilmesi

Bu modelde, ürün Dataverse'teki iki tablonun birleşimiyle gösterilir: **Ürün** ve **msdyn\_sharedproductdetails**. İlk tablo bir ürünün tanımını (ürünün benzersiz tanımlayıcısı, ürün adı ve açıklaması) içerirken, ikinci tablo ürün düzeyinde depolanan sütunları içerir. Bu iki tablonun birleşimi, ürünü stok tutma birimi (SKU) kavramına göre tanımlamak için kullanılır. Kullanıma sunulan her ürünün bilgileri belirtilen tablolarda (Ürün ve Paylaşılan Ürün Ayrıntıları) olacaktır. Tüm ürünleri izlemek için (serbest bırakılmış ve serbest bırakılmamış) **Genel ürünler** tablosu kullanılır.

Ürün bir SKU olarak temsil edildiği için farklı ürünler, ana ürünler ve ürün çeşitleri kavramları Dataverse'ta aşağıdaki şekilde yakalanabilir:

- **Alt tür ürününe sahip ürünler**, kendileri tarafından tanımlanan ürünlerdir. Boyut tanımlanması gerekmez. Belirli bir defter örnek olarak verilebilir. Bu ürünler için **Ürün** tablosunda bir satır ve **msdyn\_sharedproductdetails** tablosunda bir satır oluşturulur. Ürün ailesi satırı oluşturulmaz.
- **Ana ürünler**, iş süreçlerindeki davranışı belirleyen tanımı ve kuralları içeren genel ürünler olarak kullanılır. Bu tanımlara dayalı olarak, ürün çeşitleri olarak bilinen farklı ürünler oluşturulabilir. Örneğin, Tişört ana üründür ve Renk ve Beden boyutlarına sahip olabilir. Bu boyutların farklı birleşimlerine sahip çeşitler serbest bırakılabilir: small beden mavi tişört veya medium beden yeşil tişört gibi. Tümleştirmede, ürün tablosunda her çeşit için bir satır oluşturulur. Bu satır farklı boyutlar gibi ürün çeşidine özgü bilgileri içerir. Ürünle ilgili genel bilgiler **msdyn\_sharedproductdetails** tablosunda depolanır. (Bu genel bilgi ana üründe tutulur.) Ana ürün bilgileri, serbest bırakılan ana ürün oluşturulduğunda Dataverse ile eşitlenir (çeşitler yayımlanmadan önce).
- **Ayrı ürünler** tüm ürün alt tür ürünleri ve tüm ürün çeşitlerini ifade eder.

![Ürünler için veri modeli.](media/dual-write-product.png)

Çift yazma işlevi etkinleştirildiğinde, finans ve operasyon'dan gelen ürünler diğer Dynamics 365 ürünlerinde **Taslak** durumunda eşitlenir. Customer Engagement uygulamasında kullanılan aynı para birimiyle ve fiyat listesi adında alfabetik sıralama kullanılarak ilk fiyat listesine eklenirler. Başka bir deyişle, ürünün bir finans ve operasyon uygulamasında piyasaya sürüldüğü yasal tablonuzun para birimiyle eşleşen bir Dynamics 365 uygulamasında ilk fiyat listesine eklenirler. Belirtilen para birimi için fiyat listesi yoksa fiyat listesi otomatik olarak oluşturulur ve ürün buna atanır.

Varsayılan fiyat listesini birimle ilişkilendiren çift yazma eklentilerinin geçerli uygulaması, finans ve operasyon uygulamasıyla ilişkili para birimini arar ve fiyat listesi adında alfabetik sıralamayı kullanarak müşteri etkileşimi uygulamasında ilk fiyat listesini bulur. Belirli bir para birimi için birden fazla fiyat listeniz olduğunda, bu para birimi için varsayılan fiyat listesi ayarlamak istediğinizde, fiyat listesi adını, o para birimine yönelik diğer fiyat listelerinden alfabetik sıraya göre daha önde olan bir adla güncelleştirmeniz gerekir. Belirtilen para birimi için fiyat listesi yoksa yeni bir tane oluşturulur.

Varsayılan olarak, finans ve operasyon uygulamalarındaki ürünler **Taslak** durumundaki diğer Dynamics 365 uygulamalarıyla eşitlenir. Örneğin, satış siparişi tekliflerinde doğrudan kullanmak amacıyla **Etkin** durumdaki ürünü eşitlemek için şu ayarın seçilmesi gerekir: **Sistem > Yönetim > Sistem yönetimi > Sistem ayarları > Satış** sekmesi ve **Ürünleri etkin durumda oluştur = evet** seçeneğini belirleyin.

Ürünler eşitlendiğinde, Sales'da zorunlu bir alan olduğundan, finans ve operasyon uygulamasındaki **Satış birimi** alanı için bir değer girmeniz gerekir.

Dynamics 365 Sales'den ürün aileleri oluşturma, ürünlerin çift yazma eşitlemesiyle desteklenmez.

Ürünlerin eşitlenmesi finans ve operasyon uygulamasından Dataverse'e doğru gerçekleşir. Bu, ürün tablosu sütunlarının değerlerinin Dataverse'te değiştirilebileceği anlamına gelir ancak eşitleme tetiklendiğinde (bir finans ve operasyon uygulamasında bir ürün sütunu değiştirildiğinde), bu işlem Dataverse uygulamasındaki değerlerin üzerine yazar.

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları |
---|---
[CDS serbest bırakılan farklı ürünler](mapping-reference.md#213) | Ürün |
[Serbest bırakılan ürünler V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Tüm ürünler](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Ürün boyutları

Ürün boyutları, ürün çeşidini tanımlamaya hizmet eden özelliklerdir. Dört ürün boyutu (Renk, Boyut, Stil ve Yapılandırma) ürün çeşitlerini tanımlamak amacıyla Dataverse'a eşlenir. Aşağıdaki resimde Renk ürün boyutu için veri modeli gösterilmektedir. Aynı model Boyutlara, Stillere ve Yapılandırmalara da uygulanır.

![Ürün boyutları için veri modeli.](media/dual-write-product-two.png)

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları |
---|---
[Renkler](mapping-reference.md#170) | msdyn\_productcolors
[Boyutlar](mapping-reference.md#174) | msdyn\_productsizes
[Stiller](mapping-reference.md#178) | msdyn\_productstyles
[Konfigürasyonlar](mapping-reference.md#171) | msdyn\_productconfigurations

Ürünün farklı ürün boyutları (örneğin, ürün boyutu olarak Boyut ve Renk boyutu bulunan bir ana ürün) olduğunda, her ayrı ürün (her bir ürün çeşidi) bu ürün boyutlarının bir birleşimi olarak tanımlanır. Örneğin, ürün numarası B0001 extra small beden siyah tişört ve ürün numarası B0002 small beden siyah tişörttür. Bu durumda, ürün boyutlarının var olan birleşimleri tanımlanmıştır. Örneğin, önceki örnekteki Tişört extra small ve siyah, small ve siyah, medium ve siyah veya large ve siyah olabilir, ancak extra large ve siyah olamaz. Başka bir deyişle, bir ana ürünün alabileceği ürün boyutları belirtilir ve ürün çeşitleri bu değerlere dayalı olarak serbest bırakılabilir.

Bir ana ürünün alabileceği ürün boyutlarını takip etmek için aşağıdaki tablolar oluşturulur ve her ürün boyutu için Dataverse'te eşlenir. Daha fazla bilgi için bkz. [Ürün bilgilerine genel bakış](../../../../supply-chain/pim/product-information.md).

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları |
---|---
[Ana ürün renkleri](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Ana ürün konfigürasyonları](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Ana ürün boyutları](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Ana ürün stilleri](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Ürün Numarası Tanımlanan Barkod](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Varsayılan sipariş ayarları ve ürüne özgü varsayılan sipariş ayarları

Varsayılan sipariş ayarları maddelerin bulunduğu veya depolandığı tesisi ve ambarı, ticari veya stok yönetimi için kullanılacak minimum, maksimum, birden fazla ve standart miktarları, sağlama sürelerini, durdurma bayrağını ve sipariş taahhüt hesabını tanımlar. Bu bilgiler varsayılan sipariş ayarları ve ürüne özel varsayılan sipariş ayarları varlığı kullanılarak Dataverse'te kullanılabilir. İşlev hakkında daha fazla bilgiye [Varsayılan sipariş ayarları makalesinden](../../../../supply-chain/production-control/default-order-settings.md) ulaşabilirsiniz.

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları |
---|---
[Varsayılan sipariş ayarları](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Ürün varsayılan sipariş ayarları V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Ölçü birimi ve ölçü birimi dönüşümleri

Ölçü birimleri ve ilgili dönüştürme, şemada gösterilen veri modeline uygun olarak Dataverse'te kullanılabilir.

![Ölçü birimi için veri modeli.](media/dual-write-product-three.png)

Ölçü birimi kavramı, finans ve operasyon uygulamaları ile diğer Dynamics 365 uygulamaları arasında entegre edilmiştir. Finans ve operasyon uygulamasındaki her birim sınıfı için Dynamics 365 uygulamasında bu birim sınıfına ait birimleri içeren bir birim grubu oluşturulur. Her birim grubu için varsayılan bir temel birim de oluşturulur.

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları |
---|---
[Ürüne özel birim dönüşümleri](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Birimler](mapping-reference.md#219) | uoms
[Birim dönüştürmeleri](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Finans ve operasyon ile Dataverse arasında eşleşen birim verilerinin başlangıç eşitlemesi

### <a name="initial-synchronization-of-units"></a>Birimlerin başlangıç eşitlemesi

Çift yazma etkinleştirildiğinde finans ve operasyon uygulamalarındaki birimler diğer Dynamics 365 uygulamalarına eşitlenir. Dataverse'te finans ve operasyon uygulamalarından eşitlenen birim gruplarının "Harici olarak sağlandığını" belirten bir bayrak kümesi vardır.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Finans ve operasyon ve diğer Dynamics 365 uygulamalarındaki birimleri ve birim sınıflarını/gruplarını eşleştirme

Öncelikle, birimin tümleştirme anahtarının msdyn_symbol olduğunu dikkate almak önemlidir. Bu nedenle, bu değer Dataverse'te veya diğer Dynamics 365 uygulamalarında benzersiz olmalıdır. Diğer Dynamics 365 uygulamalarında, bir birimin benzersizliğini tanımlayan "Birim grup kimliği" ve "Ad" çifti olduğundan, finans ve operasyon uygulamaları ile Dataverse arasında birim verilerini eşleştirmek için farklı senaryoları düşünmeniz gerekir.

Finans ve operasyon uygulamaları ve diğer Dynamics 365 uygulamalarında eşleşen/çakışan birimler için:

+ **Diğer Dynamics 365 uygulamalarında bir birim grubuna ait olan ve finans ve operasyon uygulamalarında ilişkili birim sınıfına karşılık gelen birim**. Bu durumda, diğer Dynamics 365 uygulamalarında msdyn_symbol sütun, finans ve operasyon uygulamalarından birim simgesiyle doldurulmalıdır. Bu nedenle, veriler eşlendiğinde birim grubu diğer Dynamics 365 uygulamalarında "Harici olarak korunan" olarak ayarlanır.
+ **Diğer Dynamics 365 uygulamalarında bir birim grubuna ait olan ve finans ve operasyon uygulamalarında ilişkili birim sınıfına karşılık gelmeyen birim (diğer Dynamics 365 uygulamalarındaki birim sınıfı için finans ve operasyon uygulamalarında mevcut birim sınıfının olmaması).** Bu durumda, msdyn_symbol alanı rastgele bir dizeyle doldurulmalıdır. Bu değerin diğer Dynamics 365 uygulamalarında benzersiz olması gerektiğini unutmayın.

Diğer Dynamics 365 uygulamalarında bulunmayan finans ve operasyon uygulamalarındaki birimler ve birim sınıfları için:

Finans ve operasyon uygulamalarından birim gruplarının ve ilgili birimlerinin bir parçası olarak diğer Dynamics 365 uygulamalarında ve Dataverse'te oluşturulur ve senkronize edilir ve birim grubu "Harici olarak sağlanır" olarak ayarlanır. Ek önyükleme çalışmasına gerek yoktur.

Finans ve operasyon uygulamalarında bulunmayan diğer Dynamics 365 uygulamalarındaki birimler için:

msdyn_symbol sütunu tüm birimler için doldurulmalıdır. Birimler, her zaman karşılık gelen birim sınıfı için (varsa) finans ve operasyon uygulamalarında oluşturulabilir. Birim sınıfı yoksa, önce birim sınıfının oluşturulması (sabit listesini genişletiyorsanız uzantı dışında finans ve operasyon uygulamalarında birim sınıfı oluşturamayacağınızı unutmayın) ve diğer Dynamics 365 uygulamaları birim grubuyla eşleşmesi gerekir. Ardından birimi oluşturabilirsiniz. Birim için finans ve operasyon uygulamalarındaki birim sembolünün, birim için diğer Dynamics 365 uygulamalarında daha önce belirtilen msdyn_symbol olması gerektiğini unutmayın.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Ürün ilkeleri: boyut, izleme ve depolama grupları

Ürün ilkeleri, ürünleri ve özelliklerini stokta tanımlamak için kullanılan ilke kümeleridir. Ürün boyut grubu, ürün izleme boyut grubu ve depolama boyutu grubu ürün ilkesi olarak bulunabilir.

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları |
---|---
[Ürün boyut grupları](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Depolama boyut grupları](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[İzleme boyutu grupları](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Ürün hiyerarşileri

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları |
---|---
[Ürün kategorisi atamaları](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Ürün kategori hiyerarşileri](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Ürün kategori hiyerarşisi rolleri](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Ürünler için tümleştirme anahtarı

Dynamics 365 Finance ile Dataverse arasında ürünleri benzersiz şekilde tanımlamak için tümleştirme anahtarları kullanılır.
Ürünler için, **(productnumber)** Dataverse'te bir ürünü tanımlayan benzersiz anahtardır. Bu, bir birleşimden oluşur: **(şirket, msdyn_productnumber)**. **company** finans ve operasyon uygulamasında tüzel kişiliği, **msdyn_productnumber** ise finans ve operasyon uygulamasında belirli bir ürünün ürün numarasını belirtir.

Başka bir Dynamics 365 uygulamaları kullanıcısı için ürün, kullanıcı arabiriminde **msdyn_productnumber** ile tanımlanır (sütun etiketinin **Ürün numarası** olduğunu unutmayın). Ürün formunda, hem şirket hem de msydn_productnumber gösterilir. Ancak bir ürünün benzersiz anahtarı olan (productnumber) sütunu gösterilmez.

Dataverse üzerinde uygulama oluşturuyorsanız, tümleştirme anahtarı olarak **ProductNumber** (benzersiz ürün kodu) öğesini kullanarak ilgiyi ödemelisiniz. Benzersiz olmadığından **msdyn_productnumber** kullanmayın.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Ürünlerin başlangıç eşitlemesi ve verilerin Dataverse'ten finans ve operasyon uygulamasına taşınması

### <a name="initial-synchronization-of-products"></a>Ürünlerin başlangıç eşitlemesi

Çift yazma etkinleştirildiğinde, finans ve operasyon uygulamalarından gelen ürünler Dataverse ve müşteri etkileşimi uygulamalarıyla senkronize edilir. Çift yazma yayınlanmadan önce Dataverse ve diğer Dynamics 365 uygulamalarında oluşturulan ürünler güncellenmez veya finans ve operasyon uygulamalarındaki ürün verileriyle eşleşmez.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Finans ve operasyon uygulamaları ve diğer Dynamics 365 uygulamalarındaki ürün verilerini eşleştirme

Aynı ürünler finans ve operasyon, Dataverse ve diğer Dynamics 365 uygulamalarında tutulursa (çakışan/eşleşen), çift yazma etkinleştirildiğinde finans ve operasyon uygulaması işlemlerinden gelen ürünlerin eşitlemesi gerçekleşir ve Dataverse'te aynı ürün için yinelenen satırlar görünür.
Önceki durumdan kaçınmak için diğer Dynamics 365 uygulamalarında finans ve operasyon ile çakışan/eşleşen ürünler varsa çift yazmayı etkinleştiren yöneticinin, ürünlerin eşitlemesi gerçekleşmeden önce **Şirket** (örnek: "USMF") ve **msdyn_productnumber** (örnek: "1234:Black:S") sütunlarını önyüklemesi gerekir. Başka bir deyişle, Dataverse'te üründeki bu iki sütun, ürünün ve ürün numarasının eşleşmesi gereken finans ve operasyon uygulamasındaki ilgili şirketle doldurulmalıdır.

Böylece, eşitleme etkinleştirildiğinde ve gerçekleştiğinde finans ve operasyon'daki ürünler, Dataverse ve diğer Dynamics 365 uygulamalarındaki eşleşen ürünlerle eşitlenir. Bu hem farklı ürünler hem de ürün çeşitleri için geçerlidir.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Ürün verilerinin diğer Dynamics 365 uygulamalarından finans ve operasyon uygulamalarına taşınması

Diğer Dynamics 365 uygulamalarında finans ve operasyon uygulamaları içinde bulunmayan ürünler varsa yönetici bu ürünleri finans ve operasyon uygulamalarına içeri aktarmak için önce **EcoResReleasedProductCreationV2Entity**'yi kullanabilir. Ardından yukarıda açıklandığı gibi finans ve operasyon uygulamaları ve diğer Dynamics 365 uygulamalarındaki ürün verilerini eşleştirebilir.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

