---
title: Nakit akışı tahmini
description: Bu konu, nakit akışı genel görünüm işlemine bir genel bakış sağlar. Nakit akışı tahmininin sistemdeki diğer modüllerle nasıl tümleşik olduğunu da açıklar.
author: panolte
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5ad3b2444f194f8324a309df32612a5377851995
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752916"
---
# <a name="cash-flow-forecasting"></a>Nakit akışı tahmini

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nakit akışı tahmin araçlarını gelen nakit akışı ve para birimi gereksinimlerini analiz etmek için kullanabilir, böylece şirketin gelecekteki nakit ihtiyacını öngörebilirsiniz. Nakit akışının tahminini elde etmek için aşağıdaki görevleri tamamlamalısınız:

- Tüm likidite hesaplarını belirlemek ve listelemek. Likidite hesapları, şirketin nakit ve nakit eşdeğerleri için hesaplarıdır.
- Şirketin likidite hesaplarını etkileyen hareketlerin tahminleri için davranışı yapılandırın.

Bu görevleri tamamladıktan sonra nakit akışı ve gelecekteki para birimi gereksinimlerini hesaplayabilir ve analiz edebilirsiniz.

## <a name="cash-flow-forecasting-integration"></a>Nakit akışı tahmin tümleştirmesi

Nakit akışı tahmini, Genel muhasebe, Borç hesapları, Alacak hesapları, Bütçeleme ve stok yönetimi ile tümleştirilebilir, Tahmin işlemi sisteme girilen hareket bilgisini kullanır ve hesaplama işlemi, her bir hareketin beklenen nakit etkisini tahmin eder. Nakit akışı hesaplandığında aşağıdaki türdeki hareket türleri dikkate alınır:

- **Satış siparişleri** – Henüz faturalanmamış olan satış siparişleri ve fiziksel ve mali satışlarla sonuçlananlar.
- **Satınalma siparişleri** – Henüz faturalanmamış ve fiziksel veya mali satınalmayla sonuçlanan satınalma siparişleri.
- **Alacak hesapları** – Müşteri hareketlerini açın (henüz ödenmemiş faturalar).
- **Borç hesapları** – Satıcı hareketlerini açın (henüz ödenmemiş faturalar).
- **Genel muhasebe hareketleri** – Gelecekteki bir naklin göstereceğini belirten hareketler.
- **Bütçe kayıt girişleri** – Nakit akışı tahminleri için seçilen bütçe kayıtları.
- **Talep tahminleri** – Nakit akışı tahminleri için seçilen stok tahmin model satırları.
- **Tedarik tahminleri** – Nakit akışı tahminleri için seçilen stok tahmin model satırları.
- **Proje tahminleri**: Tahmin modelini kullanan proje yönetimi ve hesap tahminleri.

## <a name="configuration"></a>Konfigürasyon

Nakit akışı tahmin işlemini yapılandırmak için **Nakit akışı tahmin kurulumu** sayfasını kullanın. Bu sayfada, izlemek için likidite hesaplarını ve her bir alandaki varsayılan tahmin davranışlarını belirtirsiniz.

### <a name="general-ledger"></a>Genel muhasebe

Önce nakit akışı tahmininde izlenecek likidite hesaplarını tanımlamalısınız. Genellikle, bu likidite hesapları, nakdi alacak ve dağıtacak banka hesapları ile ilişkilendirilmiş ana hesaplardır. **Nakit akışı tahmin kurulumu** sayfasında, **Genel muhasebe** sekmesinde, tahmine dahil edilecek ana hesapları seçin. Banka hesabı ana hesap ile **Banka hesabı** sayfasında ilişkilendirilmişse, **Banka hesabı** alanında görüntülenir.

Doğrudan başka bir ana hesaptaki hareketlerle ilgili olan hareketlerin bulunduğu bir ana hesap için bağımlı bir nakit akış tahmini ayarlayabilirsiniz. **Bağlı hesaplar içinde** bölümünde eklediğiniz her satır, ana hesaba bağlı bir nakit akışı tahmin tutarı oluşturur. Bu tutar, seçmiş olduğunuz birincil ana hesaba nakit akışı tutarının yüzdesidir.

İlk olarak, **Ana hesap** alanını, hareketlerin ilk olarak gerçekleşmesi beklenen birincil ana hesaba ayarlayın. **Bağlı ana hesap** alanını, birincil ana hesaba karşı ilk hareketten etkilenecek hesaba ayarlayın. Satırdaki diğer alanlar için uygun değerler ayarlayın. **Yüzde** alanındaki değeri, birincil hesabın bağlı ana hesap üzerindeki etkisini yansıtmak üzere ayarlayabilirsiniz. Bir satış veya satınalma tahmini için, müşteri veya satıcıların çoğu için tipik olan bir **Ödeme koşulları** değeri seçin. **Nakil türü** alanını, nakit akışı tahmini ile ilişkili beklenen deftere nakil türüne ayarlayın.

### <a name="accounts-payable"></a>Borç hesapları

Satın almalar için tahmini, **Nakit akışı tahmin kurulumu** sayfasındaki **Borç hesapları** sekmesindeki kurulum seçeneklerini kullanarak hesaplayabilirsiniz. Nakit akışı tahminini Borç hesapları için yapılandırmadan önce, ödeme koşulları, satıcı grupları ve satıcı deftere nakil profillerini yapılandırmanız gerekir.

**Satınalma tahmin varsayılanları** bölümünde, nakit akışı tahmini için varsayılan satınalma davranışlarını seçebilirsiniz. Nakit etkisinin süresini üç alan belirler: **Teslim tarihi ve fatura tarihi arasındaki süre**, **Ödeme koşulları** ve **Fatura vade tarihi ve ödeme tarihi arasındaki süre**. Tahmin, bir hareket üzerinde bir değer belirtilmemişse, **Ödeme koşulları** alanı için varsayılan alanları kullanacaktır. İşlemin her bölümü için en genel işlem gününü tanımlamak için bir ödeme koşulunu kullanın.

**Ödemeler için likide hesapları** alanı ödemler için en sık kullanılan likidite hesabını belirtir. Tutarların bir yüzdesinin tahmin sırasında kullanılıp kullanılmayacağını belirlemek için **Nakit akışını tahsis etmek için tutarın yüzdesi** alanını kullanın. Tüm hareket tutarları tahmin sırasında kullanılacaksa bu alanı boş bırakın.

Belirli bir satıcı grubu için **Fatura vade tarihi ve ödeme tarihi** alanının varsayılan ayarını geçersiz kılabilirsiniz. Hareket üzerindeki satıcıyla ilişkili satıcı grubu için farklı bir değer belirtilmediği sürece tahmin, **Satınalma tahmin varsayılanları** bölümündeki varsayılan değeri kullanılacaktır. Varsayılan değeri geçersiz kılmak için bir satıcı grubu seçin ve daha sonra **Satın alma zamanı** alanında yeni bir değer ayarlayın.

Belirli satıcı deftere nakil profilleri için **Likidite hesabı** varsayılan ayarını geçersiz kılabilirsiniz. Hareket üzerindeki satıcıyla ilişkili deftere nakil profili için farklı likidite hesabı belirtilmediği sürece tahmin, **Satınalma tahmin varsayılanları** bölümündeki varsayılan değeri kullanılacaktır. Varsayılan değeri geçersiz kılmak için bir deftere nakil profili seçin ve etkilenmesi beklenen likidite hesabını belirtin.

### <a name="accounts-receivable"></a>Alacak hesapları

Satışlar için tahmini, **Nakit akışı tahmin kurulumu** sayfasındaki **Alacak hesapları** sekmesindeki kurulum seçeneklerini kullanarak hesaplayabilirsiniz. Nakit akışı tahminini Alacak hesapları için yapılandırmadan önce, ödeme koşulları, müşteri grupları ve müşteri deftere nakil profillerini yapılandırmanız gerekir.

**Satış tahmin varsayılanları** bölümünde, nakit akışı tahmini için varsayılan satış davranışlarını seçebilirsiniz. Nakit etkisinin süresini üç alan belirler: **Sevk tarihi ve fatura tarihi arasındaki süre**, **Ödeme koşulları** ve **Fatura vade tarihi ve ödeme tarihi arasındaki süre**. Tahmin, bir hareket üzerinde bir değer belirtilmemişse, **Ödeme koşulları** alanı için varsayılan alanları kullanacaktır. İşlemin her bölümü için en genel işlem gününü tanımlamak için bir ödeme koşulunu kullanın. 

**Ödemeler için likide hesapları** alanı ödemler için en sık kullanılan likidite hesabını belirtir. Tutarların bir yüzdesinin tahmin sırasında kullanılıp kullanılmayacağını belirlemek için **Nakit akışını tahsis etmek için tutarın yüzdesi** alanını kullanın. Tüm hareket tutarları tahmin sırasında kullanılacaksa bu alanı boş bırakın.

Belirli bir müşteri grubu için **Fatura vade tarihi ve ödeme tarihi** alanının varsayılan ayarını geçersiz kılabilirsiniz. Hareket üzerindeki müşteriyle ilişkili müşteri grubu için farklı bir değer belirtilmediği sürece tahmin, **Satış tahmini varsayılanlar** bölümündeki varsayılan değeri kullanılacaktır. Varsayılan değeri geçersiz kılmak için bir müşteri grubu seçin ve daha sonra **Satış zamanı** alanında yeni bir değer ayarlayın.

Belirli müşteri deftere nakil profilleri için **Likidite hesabı** varsayılan ayarını geçersiz kılabilirsiniz. Hareket üzerindeki müşteriyle ilişkili deftere nakil profili için farklı likidite hesabı belirtilmediği sürece tahmin, **Satış tahmin varsayılanları** bölümündeki varsayılan değeri kullanılacaktır. Varsayılan değeri geçersiz kılmak için bir deftere nakil profili seçin ve etkilenmesi beklenen likidite hesabını ayarlayın.

### <a name="budgeting"></a>Bütçeleme

Bütçe modellerinden oluşturulan bütçeler, nakit akışı tahminlerine dahil edilebilir. **Bütçeleme** sekmesindeki **Nakit akışı tahmin kurulumu** sayfasında, tahmine dahil edilecek bütçe modellerini seçin. Varsayılan olarak yeni bütçe kayıt girişleri, bütçe modeli nakit akışı tahminleri için etkinleştirildikten sonra tahminlere dahil edilir.

Bütçe kayıt girişleri, kişiselleştirme yoluyla nakit akışı tahminine bireysel olarak dahil edilebilir. **Bütçe kaydı girişi** sayfasına "Nakit akışı tahminlerine dahil et" sütununu eklediğinizde sistem tahmine ayrı bir bütçe kaydı girişi eklemek için **Nakit akışı tahmini kurulumu** sayfasındaki ayarların üzerine yazar.


### <a name="inventory-management"></a>Stok Yönetimi

Stok tedarik ve talep tahminleri nakit akışı tahminlerine dahil edilebilir. **Nakit akışı tahmin kurulumu** sayfasındaki **Stok yönetimi** sekmesinde, nakit akışı tahminine dahil edilecek tahmin modelini seçin. Nakit akışı tahminine dahil edilme, tekil tedarik ve talep tahmin satırlarında geçersiz kılınabilir.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Nakit akışı tahmini için Boyutları ayarlama
**Nakit akışı tahmin kurulumu** sayfasındaki yeni bir sekme, **Nakit akışı tahmini** çalışma alanında filtre uygulamak için hangi mali boyutları kullanacağınızı kontrol etmenizi sağlar. Bu sekme yalnızca Finance Insights'ta Nakit akışı tahminleri etkinleştirildiğinde görüntülenir. 

**Boyutlar** sekmesinde, filtre için kullanılacak boyut listesinden seçim yapın ve bunları sağ sütuna taşımak için ok tuşlarını kullanın. Nakit akışı tahmin verilerinin filtrelenmesi için yalnızca iki boyut seçilebilir. 

### <a name="setting-up-external-source"></a>Harici kaynağı ayarlama
Dış veriler nakit akışı tahminlerine girilebilir veya içeri aktarılabilir. Harici veriler girilmeden veya içe aktarılmadan önce, harici kaynakların ayarlanması gerekir. **Harici kaynak** sekmesinde harici nakit akışı kategorileri ayarlayın. Kategori, **Giden** veya **Gelen** olabilir. **Likidite**, deftere nakil türü olarak seçilmelidir. **Yasal varlık ayarları** kılavuzunda, yasal varlıkları ve harici nakit akışı kategorilerinin uygulanacağı ilgili ana firmaları seçin.

### <a name="project-management-and-accounting"></a>Proje yönetimi ve muhasebe

10.0.17 sürümünde yeni bir özellik, proje yönetimi ve muhasebe ile nakit akışı tahminiyle tümleştirmeyi etkinleştirir. **Özellik Yönetimi** çalışma alanında, tahmin edilen maliyetleri ve gelirleri nakit akışı tahminine eklemek için **nakit akışı proje tahmini** özelliğini açın. **Nakit akışı tahmini kurulumu** sayfasının **Proje yönetimi ve muhasebe** sekmesinde, nakit akışı tahminine eklenmesi gereken proje türlerini ve işlem türlerini seçin. Ardından Proje tahmin modelini seçin. Bir azaltma türü alt modeli en iyi çalışır. Alacak hesapları kurulumuna girilen likidite hesapları varsayılan likidite hesapları olarak kullanılır. Bu nedenle, nakit akışı tahminini ayarlarken varsayılan likidite hesaplarını girmeniz gerekmez. Bütçe modeli de kullanılabilir, ancak Proje yönetimi ve muhasebe için **nakit akışı tahmin kurulumu** sayfasında yalnızca bir tür seçilebilir. Tahmin modeli, proje yönetimi ve muhasebe veya Project Operations kullanıldığında en iyi esnekliği sağlar.

Nakit akışı proje tahmini özelliği açık olduğunda, nakit akışı tahmini **tüm projeler** sayfasında her proje için görüntülenebilir. Eylem Bölmesindeki **Plan** sekmesinde yer alan **Tahmin** grubunda **Nakit akışı tahmini**'ni seçin. **Nakit genel bakış** çalışma alanlarında (bu konunun ilerleyen bölümlerindeki [raporlama ](#reporting) bölümüne bakın), proje tahmin işlem türü, girişleri (proje tahmini geliri) ve çıkışları (proje tahmin maliyetleri) gösterir. Tutarlar ancak, **Nakit genel bakış** çalışma alanlarında **proje aşaması** alanı **İşlemde** olarak ayarlanmışsa dahil edilebilir.

**Nakit akışı proje tahmini** özelliğinin açık olup olmamasına bakmaksızın, proje işlemleri çeşitli yollarla nakit akışı tahminine dahil edilir. Deftere nakledilen proje faturaları, açık müşteri hareketlerinin bir parçası olarak tahmine dahil edilir. Proje tarafından başlatılan satış siparişleri ve satınalma siparişleri, sisteme girildikten sonra açık siparişler olarak tahmin dahil edilir. Proje tahminlerini bir genel muhasebe bütçe modeline de aktarabilirsiniz. Bu genel muhasebe bütçe modeli daha sonra nakit akışı tahminine, bütçe kayıt varlıklarının bir parçası olarak dahil edilir. **Nakit akışı proje tahmini** özelliğini etkinleştirdiyseniz, Proje tahminlerini bir kayıt defteri bütçe modeline transfer etmeyin, çünkü bu eylem proje tahminlerinin iki kere sayılmasına neden olur.

### <a name="calculation"></a>Hesaplama

Nakit akışı tahmin analizlerini görüntülemek için önce nakit akışı hesaplama işlemini çalıştırmanız gerekir. Hesaplama işlemi, girilmiş olan hareketlerin gelecekteki nakit etkilerini öngörecektir.

**Nakit akışı tahminlerini hesapla** sayfasını kullanarak nakit akışı tahminini hesaplayın. İster tam nakit akışı tahminini isterseniz de artımlı nakit akışı tahminini hesaplayabilirsiniz. 

- Tüm nakit akışı tahminlerini silmek ve yeniden hesaplamak için **Nakit akışı tahmin hesaplama yöntemi** alanını **Toplam** olarak ayarlayın. Uzun süredir nakit akışı tahminlerini güncelleştirmediyseniz bu yaklaşımı kullanmanızı öneririz. 
- Mevuct nakit akışı bilgisini yalnızca yeni hareketler için güncelleştirmek isterseniz, **Nakit akışı tahmini hesaplama yöntemi** alanını **Yeni** olarak ayarlayın. Bu sayfa, nakit akışı hesaplamanızın en son çalıştırıldığı tarihi gösterecektir.

Nakit akışı tahmininiz için toplu iş işleme de kullanabilirsiniz. Tahmin analizlerinizin düzenli olarak güncelleştirilmesini sağlamaya yardımcı olmak için nakit akışı tahmin hesaplaması için bir yinelenen toplu iş işlemi ayarlayın.

Sürüm 10.0.13'te nakit akışı hesaplama işini zamanlamak için işlem otomasyonu çerçevesini kullanan bir hesaplama işlemi geliştirme yayımlandı. Bu, **Özellik Yönetimi** çalışma alanındaki **Nakit akışı tahmin otomasyonu** özelliği kullanılarak etkinleştirilir. Etkinleştirildikten sonra, nakit akışı hesaplama işlemini zamanlayabileceğiniz yeni otomasyon sayfasını görüntülemek için **Nakit akışı tahmin otomasyonu** bağlantısını seçin. Yeni bir nakit akışı tahmin zamanlaması oluşturmak için **Yeni işlem otomasyonu oluştur**'u seçin ve ardından **Zamanlama türü** açılır menüsünde **Nakit akışı tahmin otomasyonu**'nu seçin. Nakit akışı tahmin verilerini güncelleştirdiğiniz her şirket için bir zamanlama ayarlamanız gerekir.  Bu sayfa ayrıca, bekleyen nakit akışı tahmin otomasyonu işlerinin ve son işin ne zaman tamamlandığını gösterir.  

> [!NOTE] 
> Varolan toplu işler, nakit akışı tahminleri için zaten zamanlanmışsa, bir hata iletisi alırsınız ve bu özelliği etkinleştiremezsiniz. Bu özelliği etkinleştirmeden önce varolan toplu işlerin temizlenmesi gerekir. 

Daha fazla bilgi için bkz. [İşlem otomasyonu](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Raporlama

Nakit akışı tahmini hesaplandıktan sonra, ilişkilendirilmiş varlık bilgisini analitik raporlama için yenilemeniz gerekir. **Varlık depolama** sayfasında, **LedgerCovLiquidityMeasurement toplamı** ölçümünü seçin ve daha sonra **Yenile** üzerine tıklayın.

Nakit akışı tahmin verisi içeren iki çalışma alanı vardır. Bir çalışma alanı tüm şirketler için veriye sahiptir, diğer çalışma alanı ise yalnızca geçerli şirket için veriye sahiptir.

Tüm şirketlerin çalışma alanına erişim **Tüm şirketlerin nakit akışını görüntüle çalışma alanı** görevi aracılığıyla denetlenir. **Nakit akışı – tüm şirketler** çalışma alanı varsayılan olarak aşağıdaki rollerin kullanımına açıktır:

- Yönetim kurulu başkanı
- Mali işler müdürü
- Mali denetleyici

Geçerli şirketin çalışma alanına erişim **Geçerli şirketin nakit akışını görüntüle çalışma alanı** görevi aracılığıyla denetlenir. **Nakit akışı – geçerli şirket** çalışma alanı varsayılan olarak aşağıdaki rollerin kullanımına açıktır:

- Muhasebeci
- Muhasebe müdürü
- Muhasebe gözetmeni
- Borç hesapları müdürü
- Alacak hesapları yöneticisi

**Nakit genel bakışı - tüm şirketler** çalışma alanı, nakit akışı tahminini sistem para birimi cinsinden gösterir. Sistem analizleri için kullanılan para birimi ve sistem döviz kuru türü, **Sistem parametreleri** sayfasında tanımlanır. Bu çalışma alanı, tüm şirketler için nakit akışı tahmini ve banka hesabı bakiyelerine bir genel bakışı gösterir. Nakit girişleri ve çıkışlarının bir grafiği, gelecekteki nakit hareketleri ve bakiyeleri sistem para birimi cinsinden, tahmin edilen hareketler hakkında ayrıntılı bilgiyle birlikte gösterir. Tahmin edilen para birimi bakiyelerini de görebilirsiniz.

**Nakit genel bakış – geçerli şirket** çalışma alanı, nakit akışı tahmin analizlerini şirketin tanımlanmış muhasebe para birimi cinsinden gösterir. Analizler için kullanılan muhasebe para birimi, **Genel muhasebe** sayfasında tanımlanır. Bu çalışma alanı, geçerli şirket için nakit akışı tahmini ve banka hesabı bakiyelerine bir genel bakışı gösterir. Nakit girişleri ve çıkışlarının bir grafiği, gelecekteki nakit hareketleri ve bakiyeleri muhasebe para birimi cinsinden, tahmin edilen hareketler hakkında ayrıntılı bilgiyle birlikte gösterir. Tahmin edilen para birimi bakiyelerini de görebilirsiniz.

Nakit akışı tahmin analizleri hakkında daha fazla bilgi için bkz. [Nakit genel bakışı Power BI içeriği](Cash-Overview-Power-BI-content.md).

Ek olarak, belirli hesaplar, siparişler ve maddeler hakkındaki nakit akışı tahmin verisini aşağıdaki sayfalarda görebilirsiniz:

- **Mizan bakiyesi**: Seçili an hesap için gelecek nakit akışını görüntülemek için **Nakit akışı tahminleri**'ni seçin.
- **Tüm satış siparişleri**: Seçili satış siparişlerinin tahmin edilen nakit etkisinin görmek için **Fatura** sekmesinde, **Nakit akışı tahmini**'ni seçin.
- **Tüm satınalma siparişleri**: Seçili satınalma siparişlerinin tahmin edilen nakit etkisinin görmek için **Fatura** sekmesinde, **Nakit akışı tahmini**'ni seçin.
- **Tedarik tahmini**: Seçili madde tedarik tahmini ile ilişkilendirilmiş gelecek nakit akışlarını görüntülemek için **Nakit akışı tahminleri**'ni seçin.
- **Talep tahmini**: Seçili madde talep tahmini ile ilişkilendirilmiş gelecek nakit akışlarını görüntülemek için **Nakit akışı tahminleri**'ni seçin.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
