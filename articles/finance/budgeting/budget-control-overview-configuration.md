---
title: Bütçe kontrolüne genel bakış
description: Bu makalede, bütçe denetimi özelliği tanıtılmaktadır ve kuruluşunuzun mali kaynaklarının yönetimini iyileştirmek için bütçe denetimini yapılandırmanıza yardımcı olacak bilgiler sağlanmaktadır.
author: panolte
ms.date: 03/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27eb31919937e7f43a785616b547e3d6952eaaf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898312"
---
# <a name="budget-control-overview"></a>Bütçe kontrolüne genel bakış

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, bütçe denetimi özelliği tanıtılmaktadır ve kuruluşunuzun mali kaynaklarının yönetimini iyileştirmek için bütçe denetimini yapılandırmanıza yardımcı olacak bilgiler sağlanmaktadır.

Bütçe kontrolü bir kuruluşun mali kaynaklarının hesap planları, iş akışları, kullanıcı grupları, kaynak belgeleri ve günlükleri, kullanılabilir fonların yapılandırılabilir hesabı, bütçe döngüleri ve eşikler üzerinden yönetimini desteklemektedir. Denetimler oluşturulduktan sonra bir organizasyon mali yıl boyunca mali kaynaklarını planlayabilir, ölçebilir, yönetebilir ve kestirebilir. 

Bütçeler sistem içinde onaylandıktan sonra bir kuruluşun harcama bütçesini kaydetmek amacıyla bütçe kayıt girişleri oluşturmak için bütçe planlarını kullanabilirsiniz. Alternatif olarak, bütçe planlama işlevini kullanmak yerine bir üçüncü taraf programın bütçe kayıt girişlerini oluşturabilir veya içeri aktarabilirsiniz. 

Harcamalar ana hesaplar ve mali boyutlar kullanılarak kaydedilebilir. Mali boyutların ve ana hesapların birleşimlerini gruplayarak kuruluş ilkelerini ve gereksinimlerini karşılayacak şekilde genel harcama denetimini yapılandırabilirsiniz. 

Aşağıdaki çizelgede tipik bir bütçe döngüsünün aşamaları içinde bütçe denetiminin yeri gösterilmektedir.

[![Tipik bütçeleme döngüsü.](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Bütçe denetimini birkaç etkene göre yapılandırabilirsiniz:

- **Mali boyutlar**: Bütçenin ve fiili tutarların raporlanması için hangi mali boyutlar kullanılmalıdır ve bütçelerin denetlenmesi için hangi mali boyutlar gereklidir? Özel dikkat gerektiren, belirli boyut kombinasyonları veya ana hesaplar var mı? Örneğin, bütçenin maliyet merkezine ve programa göre fiili tutarlara kadar takip edilmesine yönelik bir ihtiyaç var mı? Seyahat masrafları özel dikkat gerektirir mi?
- **Zaman** - Mevcut bütçe fonlarının değerlendirilmesi için hangi zaman dilimi (mali dönem, bugüne kadar mali dönem vb.) kullanılacak?
- **Kaynak belgeler** – Bütçe denetimi için hangi kaynak belgelerinin değerlendirilmesi gerekir? Belgeler, belge veya satır başına mı değerlendirilmelidir?
- **Kullanılabilir fon hesaplama** - Satın alma talepleri (ön yükümlülükler) ve satın alma emirleri (yükümlülükler) belgelerin kullanılabilir fonların hesaplanmasında dikkate alınması gerekiyor mu? Taslak durumundaki belgelerin hesaplamada dikkate alınması gerekiyor mu?
- **Aşım izni** -Kimler mevcut bütçeyi aşma yetkisine sahip olacak?

Bütçe denetimi uygulamayla tamamen tümleşiktir. Bu nedenle, planlı satınalma hem de gerçek satınalmalar için kullanılabilen bütçeyi değerlendirebilirsiniz. Bütçe sorguları ve raporları mevcuttur. Bu nedenle, kullanıcılar bütçeyi değerlendirebilir ve bütçe döngüsü boyunca bütçe revizyonları veya transferleri yardımıyla gereken düzenlemeleri yapabilir. Ayrıca, bütçe yöneticileri gerektiğinde daha iyi analiz etmek ve kestirimlerde bulunmak üzere bütçeyi ve fiili tutarları Microsoft Excel'e aktarabilir.

## <a name="configuring-budget-control"></a>Bütçe kontrolünü yapılandırma

### <a name="budget-cycle-time-span"></a>Bütçe döngüsü zaman aralığı

Temel bütçeleme yapılandırıldıktan sonra bütçeleme ve bütçe kontrolü için zamanı veya başlangıç ve bitiş dönemlerini **Bütçe döngüsü süresi** sayfasında tanımlayabilirsiniz. Bütçe döngüleri genellikle mali takvimlere karşılık gelir, ancak mali yıllara da yayılabilmektedir.

Yapılandırmadaki sonraki adımlar, **Bütçe kontrolü yapılandırması** sayfasından açılan sekmelerde tamamlanır.

### <a name="define-parameters"></a>Parametreleri tanımla

Bütçe için etkinleştirilen mali boyutlara bağlı olarak, bütçe denetimi için mali boyutların tamamını veya bir alt kümesini kullanabilirsiniz. 

Ayrıca, bütçe kontrolünün ilgili bütçenin çalıştırılacağı varsayılan zaman aralığını (örneğin, **Mali yıl**, **Mali yıldan bugüne**, **Mali dönem** veya **Üç Aylık**) belirtebilirsiniz. Ayrıca, varsayılan bir bütçe yöneticisi ve eşik aşıldığında kullanıcılara bildirmek için kullanılacak bir eşik belirtebilirsiniz. Bu alanlardaki değerler oluşturulan yeni bütçe denetim kuralı ya da bütçe grubunda varsayılan değerler olarak kullanılacaktır. Ancak, varsayılan değerler bireysel gruplar veya kurallar için değiştirilebilir. 

Bütçelerin nasıl oluşturulduğu ve bütçe kaydına nasıl kaydedildiği, mevcut bütçe fonları değerlendirilirken seçilecek zaman aralığının belirlenmesine yardımcı olur. Bir boyut değeri kombinasyonu için yıla dağıtılan bir tutar geliştirilir ve kullanılırsa mali yıl veya bugüne kadar geçen mali yıl yaklaşımının kullanılması mantıklı olacaktır. Ancak, bütçeleri mali döneme göre oluşturan veya mali dönemlere tahsis eden kuruluş daha ayrıntılı denetim isterse bugüne kadar geçen mali dönem veya üç aylık dönem zaman aralıklarını kullanmayı düşünebilir. 

Buna ek olarak, bir kuruluşun bütçeleme ve bütçe kontrolü ile ilgili kültürü de yapılandırmanın belirlenmesine yardımcı olur.

### <a name="over-budget-permissions"></a>Bütçe aşımı izinleri

Ardından, **Bütçe aşımı izinleri** sekmesinde, kullanıcı gruplarını belirtebilirsiniz. Ayrıca, bir grubun üyesi olan kullanıcıların bütçeyi aşma iznine sahip olup olmadığını da belirtebilirsiniz. Kullanıcıların **Bütçe parametreleri** sayfasında ayarlanan bütçe eşiğini aşmalarını engelleyebilirsiniz veya eşikten bağımsız olarak bütçenin herhangi bir tutarla aşılmasını engelleyebilirsiniz. Bir kuruluşun kendi harcamalarını yönetirken ne kadar proaktif davrandığına bağlı olarak bu izinler mali kaynakların yönetilmesine yardımcı olabilir. 

### <a name="budget-funds-available"></a>Kullanılabilen bütçe fonları

Ardından **Kullanılabilen bütçe fonları** sekmesinde, kullanılabilir bütçe fonlarını hesaplamak için kullanılan formülü tanımlayabilirsiniz. Bir kuruluşun mali kaynaklarını yönetmede ne kadar tutucu davrandığına dayalı olarak veya yönetmelikler veya endüstri gereksinimleri dikkate alınarak bu hesaplama, taslak veya nakledilmemiş belgeleri içerebilir. 

> [!NOTE]
> Hesaplama bir bütçe döngüsü sırasında değiştirilirse daha önce bütçe kontrolü denetimlerinden geçen ve nakledilen veya tamamlanan belgeler bu değişikliklerden etkilenmez. **Yalnızca kullanılabilir bütçe fonları hesaplamasındaki izleme tutarları** adlı bir özellik, BudgetSourceTracking tablolarında hangi verilerin izleneceğini değiştirmenize olanak sağlar. Bu özellik açıldığında, tutarlar yalnızca kullanılabilir bütçe fonları hesaplamasında kullanılmak üzere seçilmişse depolanır. Daha fazla bilgi için bkz. [Kullanılabilir bütçe fonları](budget-funds-available.md).

### <a name="documents-and-journals"></a>Belgeler ve günlükler

**Belgeler ve günlükler** sekmesinde hangi kaynak belgelerinin ve günlüklerinin bütçe kontrolü denetimlerine tabi tutulacağını ve denetimin satır girişinde mi, yoksa tüm belge düzeyinde mi gerçekleştirileceğini tanımlayabilirsiniz. Ayrıca, Microsoft Dynamics 365 Finance sürümü 10.0.27 itibariyle kullanılabilen yeni **Bütçe kontrol belgesi filtreleme geliştirmesi** özelliği, bütçe kontrolüne dahil edilen her belge için sorgu tabanlı bir filtre seçeneği sağlar. Bu nedenle, bütçe için hangi bütçe kontrol belgelerinin kontrol edilebilir olduğunu belirtebilirsiniz. Bu şekilde, özellik bir belge türünün yalnızca bir alt kümesinin bütçe denetimli olmasını sağlar. Örneğin, yalnızca **Havuz** alanı **01** olarak ayarlanmış olan satınalma siparişlerini kontrol edebilirsiniz. **Belgeler ve günlükler** sekmesine eklenen yeni bir sütun, seçili belge türü için bir sorgunun tanımlanıp tanımlanmadığını gösterir. Ek olarak, belge kılavuzunun üzerine araç çubuğuna eklenen iki yeni düğme filtre eklemenizi, düzenlemenizi veya silmenizi sağlar. 

Kullanılabilir bütçe fonlarının hesaplanmasına dahil edilen onay kutularıyla seçilen kaynak belgeleri eşleştirmeniz gerekir. Örneğin, **Yükümlülükler için bütçe rezervleri** ayarını seçerseniz **Satın alma emirleri** seçimini yapmanız gerekir. Bir satın alma satırındaki tutarlar ve hesaplar için bir bütçe denetimi gerçekleştirildiğinde, rezerve atanan bütçe kontrolü kategorisi, **Yükümlülük** kategorisi olacaktır. Bir satın alma talebindeki tutarlar ve hesaplar için bir bütçe denetimi gerçekleştirildiğinde, rezerve atanan bütçe denetimi kategorisi, **Ön yükümlülük** kategorisi olacaktır. 

**Yükümlülükler için bütçe rezervleri** ve/veya **Ön yükümlülükler için bütçe rezervleri** kullanılabilir bütçe fonlarının hesaplanmasına dahil edilirse ve bunların genel muhasebedeki nakillere yansıtılması gerekiyorsa bu seçimleri **Genel muhasebe parametreleri** sayfasındaki **Taahhüt muhasebesi** grubunda işaretlemeniz gerekir.

### <a name="assign-budget-models"></a>Bütçe modellerini ata

Ardından, **Bütçe modelleri ata** sekmesinde, bütçe denetimine dahil edilecek bütçe döngüsü zaman aralıklarına bütçe modelleri atarsınız.

### <a name="define-budget-control-rules"></a>Bütçe kontrolü kuralları tanımla

Ardından, **Bütçe denetim kurallarını tanımla** sekmesinde, bütçe denetimi için etkinleştirilen mali boyutlara dayalı olarak belirli kurallar oluşturmanız gerekir. Örneğin, bir departman için harcamaya veya harcama aralığına odaklanılıyorsa bu harcamaları tanımlamak ve değerlendirmek için bu sekmedeki ayarları kullanabilirsiniz. Her bir bütçe denetim kuralı için farklı eşik değerleri tanımlayabilirsiniz. 

> [!Important]
> Bütçe denetimi, **Kar ve Zarar**, **Masraf**, **Gelir, Bilanço, Pasif, Öz Varlık** veya **Kıymet** türündeki her ana hesap için etkinleştirilecektir. **Bütçe kontrol kurallarını tanımla** sekmesi boş kriteri olan bir kural içeriyorsa bütçe denetimi bu türde ana hesap içeren **tüm** mali boyut birleşimleri için etkinleştirilecektir. Bu nedenle, bütçe denetiminin uygulanmasının önemli olduğu durumlarda, sadece mali boyut birleşimlerinin aralıklarını tanımlayan bütçe denetim kurallarını oluşturduğunuzdan emin olun.

### <a name="select-main-accounts"></a>Ana hesapları seç

**Parametreleri tanımla** sayfasında **Ana hesap** bütçe denetim boyutu olarak seçilmediyse ve belirli harcamalar yönetiliyorsa bu harcamaları **Ana hesapları seç** sekmesinde seçebilirsiniz. **Ana hesap** bir bütçe denetim boyutu olarak seçildiyse, giriş gerekmez.

### <a name="define-budget-groups"></a>Bütçe grupları tanımla

Ardından, **Bütçe gruplarını tanımla** sekmesinde, bütçe kaynaklarının ikincil bütçe denetimi için havuza alındığı özgün mali boyut kombinasyonlarını isteğe bağlı olarak tanımlayabilirsiniz. Tüm kuruluşu içeren tek bir kayıt oluşturabilir veya tek tek departmanları veya maliyet merkezlerini temsil eden birden fazla grup tanımlayabilirsiniz.

### <a name="define-message-levels"></a>İleti düzeylerini tanımla

Tüm kullanıcı grupları için bütçe denetimi uyarı iletileri bastırılacaksa bu grupları **İleti düzeylerini tanımla** sayfasında belirtebilirsiniz. Kullanıcı gruplarının üyeleri, bütçe aşım izinlerine bağlı olarak, kullanılabilir bütçe fonlarını aştıklarında hata iletileri almaya devam eder.

### <a name="activate-budget-control"></a>Bütçe kontrolünü etkinleştir

Bütçe denetimi yapılandırıldıktan sonra, **Bütçe denetimi etkinleştir** sekmesinde açabilir ve etkinleştirebilirsiniz. Taslak sürümü o zaman etkin olacaktır.

> [!Important]
> Bütçe denetimi açık konuma getirildikten ve etkinleştirildikten sonra hareketler nakledilirse, bütçe kontrolü yıl ortasında kapalı konuma getirilmemelidir. Bütçe denetimi kapalı konuma getirildiğinde, bütçe denetim amacıyla etkinlikler kaydedilmez ve bundan sonra bütçe denetimleri gerçekleştirilemez. Bu nedenle, deftere nakledilmiş olan belgeler hafifletme tutarlarını veya sorgu ve raporlardaki bütçe denetimi ile ilgili bakiyeleri doğru olarak yansıtmayabilir. Bunlar, herhangi bir aşağı akış veya ayarlama belgeleri ve günlükleri için bütçe denetim istatistikleri içerir. 

Ayrıca, bütçe kayıt girişleri de dahil olmak üzere, bütçe denetimi açık konuma getirilmeden önce nakledilen hareketlerin bütçe denetimi için dikkate alınmayacağını unutmayın. Bu nedenle, bütçe denetiminin sadece yeni bütçe döngüsünün başında açık konuma getirilmesi iyi bir fikirdir. Bütçe denetimi için başlangıç bütçe bakiyelerini içeren bütçe kaydı girişlerinin, bütçe bakiyesi güncellemelerini sadece bütçe denetimi açık konuma getirildikten sonra aldığından emin olun. Kullanıcı, belgede el ile bütçe kontrol denetimini başlattığında tüm açık belgeler (örneğin, satın alma siparişi), kullanılabilir bütçe fonu için kontrol edilir ve bütçe denetimi için bir bütçe rezervi alır.

## <a name="using-budget-control"></a>Bütçe kontrolünü kullanma
Bütçe denetimi açık konuma getirildikten sonra, bütçe denetimi için yapılandırılan belgelerde ve günlüklerde bütçe denetim uyarısı ve hata iletileri alırsınız. Unutmayın, kullanıcıların bütçe fonlarını aştıklarında uyarılmaları için bütçe denetimini yapılandırabilirsiniz ancak onaylamaya ve hareketleri deftere nakletmeye devam edebileceksiniz. Başarısız bütçe kontrollerinin ayrıntılarını **Bütçe denetimi hataları ve uyarıları** sayfasında görüntüleyebilirsiniz.

Bu sayfadan, kullanıcılar **Döneme göre bütçe denetim istatistikleri** sayfasının ayrıntılarına girerek belirli bir bütçe denetim boyutu birleşimi için bütçe kullanılabilirliği ayrıntılarını ve rezervasyonları görüntüleyebilir. Kullanıcılar ayrıca bütçe denetiminde kullanılan tüm mali boyut birleşimlerinin bütçe kullanılabilirliğini görüntülemek için **Bütçe denetimi istatistiği** sayfasının ayrıntılarına girebilir. 

Bütçe denetimi satın alma siparişleri için etkinleştirilmişse bütçe yöneticisi bütçe kontrolü uyarıları ve hataları olan onaylanmamış tüm satın alma siparişlerinin sırasını görüntülemek için **Genel muhasebe bütçeleri ve tahminleri** çalışma alanını kullanabilir. Bütçe yöneticisi yapılandırılmış bütçe aşım izinlerine sahipse satın alma siparişleri doğrudan çalışma alanında onaylanabilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
