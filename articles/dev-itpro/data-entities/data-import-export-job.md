---
title: Veri içe ve dışa aktarma işleri
description: Veri yönetimi çalışma alanını veri içe aktarma ve dışa aktarma işlerini oluşturmak ve yönetmek için kullanın.
author: Sunil-Garg
manager: AnnBe
ms.date: 07/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b16966fe1c3a48d772c7c9982f8802119675255f
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862916"
---
# <a name="data-import-and-export-jobs"></a>Veri içe ve dışa aktarma işleri

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 for Finance and Operations içinde veri içe ve dışa aktarma işlerini yönetmek için **Veri yönetimi** çalışma alanını kullanabilirsiniz. Varsayılan olarak, veri içe ve dışa aktarma işlemi, hedef veritabanındaki her bir varlık için bir hazırlama tablosu oluşturur. Hazırlama tabloları, taşımadan önce verileri doğrulamanızı, temizlemenizi ve dönüştürmenizi sağlar.

> [!NOTE]
> Bu konu, [veri varlıkları](data-entities.md) hakkında bilgi sahibi olduğunuzu varsayar.

## <a name="data-importexport-process"></a>Ver içe/dışa aktarma işlemi
Veri içe ve dışa aktarmak için adımlar buradadır.

1. Aşağıdaki görevleri tamamladığınız bir içe ve dışa aktarma işi oluşturun:

    - Proje kategorisini tanımlayın.
    - İçe veya dışa aktarılacak varlıkları belirleyin.
    - İş için veri biçimlerini ayarlayın.
    - Varlıkları sıralayın, böylece mantıksal gruplarda ve mantıklı bir sırada işlenebilirler.
    - Hazırlama tablolarının kullanılıp kullanılamayacağını belirleyin.

2. Kaynak veri ve hedef verinin doğru eşleştirildiğini doğrulayın.
3. İçe ve dışa aktarma işiniz için güvenliği doğrulayın.
4. İçe ve dışa aktarma işini çalıştırın.
5. İş geçmişini gözden geçirerek işin beklendiği gibi çalıştığını doğrulayın.
6. Hazırlama tablolarını temizleyin.

Bu konunun kalan bölümleri işlemin her bir adımı hakkında bilgi veri.

> [!NOTE]
> En son ilerlemeyi görmek üzere Veri içe aktarma/dışa aktarma formunu yenilemek için form yenileme simgesini kullanın. Toplu iş modunda çalıştırılmayan herhangi bir içe aktarma/dışa aktarma işini yarıda keseceği için tarayıcı düzeyinde yenileme önerilmez.

## <a name="create-an-import-or-export-job"></a>Bir içe ve dışa aktarma işi oluşturun
Bir veri içe ve dışa aktarma işi bir veya birden fazla defa çalıştırılabilir.

### <a name="define-the-project-category"></a>Proje kategorisini tanımlayın
İçe veya dışa aktarma işiniz için uygun proje kategorisi seçmek için vakit ayırmanızı öneririz. Proje kategorileri ilgili işleri yönetmenize yardımcı olur.

### <a name="identify-the-entities-to-import-or-export"></a>İçe veya dışa aktarılacak varlıkları belirleyin
Belirli varlıkları bir içe veya dışa aktarma işine ekleyin veya uygulanacak bir şablon seçin. Şablonlar, bir işi varlıkların listesi ile doldurur. **Şablonu Uygula** seçeneği, işe bir ad verdikten ve işi kaydettikten sonra kullanılabilir.

### <a name="set-the-data-format-for-the-job"></a>İş için veri biçimlerini ayarlayın
Bir varlık seçtiğinizde, içe veya dışa aktarılacak verinin biçimini seçmelisiniz. **Veri kaynakları kurulumu** kutucuğunu kullanarak biçimleri tanımlayabilirsiniz. Bir veri kaynağı biçimi **Tür**, **Dosya biçimi**, **Satır sınırlayıcı** ve **Sütun sınırlayıcı**'nin birleşimidir. Başka öznitelikler de vardır, ancak bunlar anlamanız gereken temel özniteliklerdir. Aşağıdaki tabloda geçerli bileşimler listelenmiştir.

| Dosya Biçimi            | Satır/Sütun sınırlayıcı                       | XML Stili                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-Yok-                     |
| XML                    | \-Yok-                                      | XML- XML Öğesi-Öznitelik |
| Sınırlandırılmış, sabit genişlik | Virgül, noktalı virgül, sekme, dikey çubuk, iki nokta üst üste | \-Yok-                     |

### <a name="sequence-the-entities"></a>Varlıkları sıralayın
Varlıklar bir veri şablonunda veya içe veya dışa aktarma işlerinde sıralanabilir. Birden fazla veri varlığı içeren bir iş çalıştırdığınızda, veri varlıklarının doğru sıralandığından emin olmanız gerekir. Öncelikli olarka, varlıklar arasında işlevsel bağımlılıkları adreslendirebilmek için varlıkları sıralarsınız. Varlıklar işlevsel bağımlılıklara sahip değilse, paralel içe veya dışa aktarma için zamanlanabilirler.

#### <a name="execution-units-levels-and-sequences"></a>Yürütme birimleri, seviyeler ve sıralamalar
Yürütme birimi, yürütme birimi içindeki seviye ve bir varlığın sıralaması, verinin içe veya dışa aktarıldığı sırayı yönetmeye yardımcı olur.

- Farklı bir yürütme birimindeki varlıklar paralel şekilde işlenir.
- Her bir yürütme biriminde, aynı düzeye sahiplerse varlıklar paralel olarak işlenir.
- Her bir düzeyde, varlıklar, düzeydeki sıralama numaralarına göre işlenir.
- Bir düzey işlendikten sonra, bir sonraki düzey işlenir.

#### <a name="resequencing"></a>Yeniden sıralama
Varlıklarınızı aşağıdaki durumlarda yeniden sıralamak isteyebilirsiniz:

- Yalnızca bir veri işi tüm varlıklarınız için kullanılacaksa, yeniden sıralama seçeneklerini, tam işin yürütme süresini optimize etmek için kullanabilirsiniz. Bu gibi durumlarda, modül, modül ve dizinin varlığı temsil etmek için özellik alanını temsil eden düzeyi temsil etmek için yürütme birimi kullanabilirsiniz. Bu yöntemi kullanarak, paralel modülleri arasında çalışır, ancak modül içindeki sıra yine de çalışabilir. Paralel işlemlerin başarılı olmasına yardımcı olmak için tüm bağımlılıkları dikkate almanız gerekir.
- Birden fazla veri işi kullanılıyorsa (örneğin, her bir modül için bir iş), düzeyi ve varlıkların sırasını en iyi yürütme için sıralamayı kullanabilirsiniz.
- Hiç bağımlılık yoksa, farklı yürütme birimlerinde maksimum optimizasyon için tüm varlıkları sıralayabilirsiniz.

**Yeniden sıralama**, birden fazla varlık seçildiğinde menü kullanılabilir. Yürütme birimi, düzeyi veya sıralama seçeneklerine dayanarak yeniden sıralayabilirsiniz. Seçilen varlıkları yeniden sıralamak için bir artış ayarlayabilirsiniz. Her bir varlık için seçilen birim, düzey ve/veya sıralama numarası, belirtilen artışla güncelleştirilir.

#### <a name="sorting"></a>Sıralama
**Şuna göre sırala** seçeneğini, varlık listesini sıralama sırasında görüntülemek için kullanabilirsiniz.

### <a name="truncating"></a>Kısaltma
İçe aktarma projeleri için, içe aktarma işleminden önce varlıklardaki kayıtları kısaltmayı seçebilirsiniz. Bu, kayıtların net bir dizi tabloya aktarılması gerektiği zaman yararlı olur. Bu ayar varsayılan olarak kapalıdır.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Kaynak veri ve hedef verinin doğru eşleştirildiğini doğrulayın
Eşleşme, hem içe hem dışa aktarma işlerine uygulanan bir fonksiyondur.

- Bir içe aktarma işinin bağlamında, eşleşme kaynak dosyada hangi sütunların hazırlama tablosunda sütunlar haline geleceğini belirtir. Bu nedenle, sistem hazırlama tablosunun hangi sütuna veri kaynak dosyasındaki sütun kopyalayacağını belirtebilir.
- Bir dışa aktarma işinin bağlamında, eşleşme hazırlama tablosunda (kaynakta) hangi sütunların hedef dosyasında sütunlar haline geleceğini belirtir.

Sütun adları hazırlama tablosunda ve dosyada sütun adları eşleşiyorsa, adlara dayalı olarak sistem otomatik olarak eşleşmeyi başlatır. Ancak, adları farklıysa, sütunları otomatik olarak eşleştirilmez. Bazı durumlarda, veri işindeki **Eşleşmeyi görüntüle** seçeneğini seçerek eşleşmeyi tamamlamanız gerekir.

İki eşleşme görünümü vardır: varsayılan görünüm olan **Eşleşme görselleştirmeleri** ve **Eşleştirme ayrıntıları**. Kırmızı bir yıldız (\*), varlıktaki gerekli alanları belirtir. Varlıkla çalışmadan önce bu alanların eşleşmesi gerekir. Diğer alanlar, varlık ile çalışmanız gerektiğinde eşleşmeyi iptal edebilirsiniz. Bir eşleşmeyi kaldırmak için **Varlık** sütunu veya **Kaynak** sütununda alanları seçin ve **Varlık seçimini** işaretleyin. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin ve sonra projeye dönmek için sayfayı kapatın. İçe aktardıktan sonra kaynaktan hazırlamaya alan eşleştirmeyi düzenlemek için aynı işlemi kullanabilirsiniz.

**Kaynak eşleştirme oluştur**'u seçerek sayfada bir eşleştirme oluşturabilirsiniz. Oluşturulan bir eşleme bir otomatik eşleme gibi davranır. Bu nedenle, eşlenmemiş tüm alanlar el ile eşleşmelidir.

![Veri eşleme](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>İçe ve dışa aktarma işiniz için güvenliği doğrulayın
**Veri yönetimi** çalışma alanına erişim kısıtlanmış olabilir, bu yüzden yönetici olmayan kullanıcılar yalnızca belirli veri işlerine erişebilir. Bir veri işine erişim, söz konusu işin yürütme geçmişine ve hazırlama tablolarına tam erişim anlamına gelir. Bu nedenle, bir veri işi oluşturduğunuzda, uygun erişim denetimlerinin mevcut olduğundan emin olun.

### <a name="secure-a-job-by-roles-and-users"></a>Bir işi roller ve kullanıcılarla güvenli hale getirin
**Uygulanabilir roller** menüsünü, işi birden fazla güvenlik rolüne kısıtlama için kullanın. Yalnızca bu rollerdeki kullanıcıların işe erişimi olacaktır.

Bir işi belirli kullanıcılara da kısıtlayabilirsiniz. Bir işi roller yerine kullanıcılarla güvenli hale getirirseniz, birden fazla kullanıcı bir role atanmışsa daha fazla kontrol olur.

### <a name="secure-a-job-by-legal-entity"></a>Tüzel kişiliğe göre bir işi güvenli hale getirin
Veri işleri doğaları gereği geneldir. Bu nedenle, bir veri işi oluşturulursa ve bir tüzel varlıkta kullanılırsa, iş sistemdeki diğer yasal varlıklarda görünür olur. Bu varsayılan davranış, bazı uygulama senaryolarında tercih edilebilir. Örneğin, veri varlıklarını kullanarak faturaları içe aktaran bir kuruluş, kuruluş içindeki tüm departmanlar için fatura hatalarını yönetmekten sorumlu merkezi bir fatura işleme ekibi oluşturabilir. Bu senaryoda, merkezi fatura işleme ekibinin tüm tüzel varlıklardaki tüm fatura içe aktarma işlerine erişiminin olması faydalıdır. Bu nedenle, varsayılan davranış açısından bir tüzel kişilik gereksinimini karşılar.

Ancak, bir kuruluş tüzel varlık başına fatura işleme ekiplerine sahip olmak isteyebilir. Bu durumda, bir tüzel kişilikteki bir ekip, yalnızca kendi tüzel varlığındaki fatura içe aktarma işine erişime sahip olmalıdır. Bu gereksinimi karşılamak için veri işleri üzerindeki tüzel varlığa dayalı erişim denetimini, veri işi içindeki **Uygulanabilir tüzel varlıklar** menüsünü kullanarak yapılandırabilirsiniz. Yapılandırma sona erdikten sonra, kullanıcılar yalnızca mevcut olarak oturum açılmış oldukları tüzel varlıktaki işleri görebilirler. Diğer tüzel varlıklardaki işleri görmek için kullanıcıların söz konusu tüzel varlığa geçmeleri gerekir.

Bir iş aynı anda roller, kullanıcılar ve tüzel varlıklarla güvenlik altına alınabilir.

## <a name="run-the-import-or-export-job"></a>İçe ve dışa aktarma işini çalıştırın
Bir işi tanımladıktan sonra **İçe aktar** veya **Dışa aktar** seçerek bir defa çalıştırabilirsiniz. Yinelenen bir iş ayarlamak için **Yinelenen veri işi oluştur** seçebilirsiniz.

> [!NOTE]
> Bir içe aktarma veya dışa aktarma işi zaman uyumsuz olarak **İçe aktar** veya **Dışa aktar** düğmesini seçerek çalıştırılabilir. Zaman uyumsuz olarak çalıştırmak, Finance and Operations içinde zaman uyumsuz çerçeveyi kullanır, bu da toplu iş çerçevesinden farklıdır. Ancak, toplu iş çerçevesi gibi, zaman uyumsuz çerçeve de azaltma uygulayabilir ve sonuç olarak, iş derhal yürütülmeyebilir. İşler, **Şimdi içe aktar** veya **Şimdi dışa aktar** seçerek eşzamanlı olarak da çalıştırılabilir. Bu, işi derhal başlatır ve zaman uyumsuz veya bir toplu iş, azaltma nedeniyle başlatılmazsa faydalıdır. İşler, **Toplu iş içinde çalıştır** seçeneği seçilerek toplu iş içinde de çalıştırılabilir. Toplu iş kaynakları, azaltılabilir, bu nedenle toplu iş derhal başlatılmayabilir. Zaman uyumsuz seçeneği, kullanıcılar doğrudan kullanıcı arabirimi ile etkileşime girdiklerinde ve toplu iş zamanlamayı anlamayan ileri düzey kullanıcı olmadıklarında yararlıdır. Büyük miktarların dışa veya içe aktarılması gerektiğinde toplu bir toplu işi alternatif bir seçenek olarak kullanmak. Toplu işler, belirli bir toplu iş grubunda yürütülmek üzere zamanlanabilir, bu da bir yük dengeleme perspektifinden bakınca daha fazla denetime izin verir. Zaman uyumsuz ve toplu iş, sistemdeki yüksek kaynak kullanımı nedeniyle azaltılıyorsa, anında etki edecek bir geçici çözüm olarak, içe/dışa aktarmanın eşzamanlı sürümü kullanılabilir. Eşzamanlı seçenek, anında başlatılır ve kullanıcı arabirimini engelleyecektir çünkü eşzamanlı olarak yürütülür. Tarayıcı penceresinin eşzamanlı işlem devam ederken açık tutulması gerekir.

## <a name="validate-that-the-job-ran-as-expected"></a>İşin beklendiği çalıştığını doğrulayın.
İş geçmişi hem içe hem de dışa aktarma işlerinde sorun giderme ve sorgulama için kullanılabilir. Tarihi iş yürütmeleri zaman aralıkları ile düzenlenir.

![İş geçmişi aralıkları](./media/dixf-job-history.md.png)

Çalıştırılan her iş aşağıdaki ayrıntıları sağlar:

- Yürütme ayrıntıları
- Yürütme günlüğü

Yürütme ayrıntıları, işin işlediği her bir veri varlığın durumunu gösterir. Bu nedenle, aşağıdaki bilgileri hızlı bir şekilde bulabilirsiniz:

- Hangi varlıkları işlendi.
- Bir varlık için, kaç kaydın başarıyla işlendiği ve kaçının başarısız olduğu.
- Her bir varlık için hazırlama kayıtları.

Dışa aktarma işleri için hazırlama verisini bir dosya içinde indirebilir veya içe ve dışa aktarma işleri için bir paket olarak indirebilirsiniz.

Yürütme ayrıntılarından yürütme kaydını da açabilirsiniz.

## <a name="clean-up-the-staging-tables"></a>Hazırlama tablolarını temizleyin
Platform Update 29'dan başlayarak, bu işlevselliği kullanımdan kaldırılmıştır. Bu, aşağıda açıklanan iş geçmişi temizleme işlevselliği yeni bir sürümü ile değiştirilir.

Hazırlama tablolarını **Veri yönetimi** çalışma alanındaki **Hazırlama temizleme** özelliğini kullanarak temizleyebilirsiniz. Aşağıdaki seçenekleri, hangi kayıtların hangi hazırlama tablosundan silineceğini seçmek için kullanabilirsiniz:

- **Varlık**: Yalnızca bir varlık sağlandıysa, o varlığın hazırlama tablosundaki tüm kayıtlar silinir. Varlık için tüm veri projeleri ve tüm işler için tüm veriyi silmek için bu seçeneği işaretleyin.
- **İş Kodu**: Yalnızca bir iş kodu sağlandıysa, seçilen işteki tüm varlıklar için tüm kayıtlar uygun hazırlama tablolarından silinir.
- **Veri projeleri**: Yalnızca bir veri projesi seçiliyse, seçilen veri projesi için tüm işler arasındaki tüm varlıklar için tüm kayıtlar silinir.

Silinen kayıt kümesini daha da kısıtlamak için seçenekleri birleştirebilirsiniz.

## <a name="job-history-clean-up-available-in-platform-update-29-and-later"></a>İş geçmişi temizleme (Platform Update 29 ve sonraki sürümlerde kullanılabilir)

Veri yönetimindeki iş geçmişi temizleme işlevselliği, yürütme geçmişinin periyodik olarak temizlenmesini zamanlamak için kullanılmalıdır. Bu işlevsellik, şimdi kullanımdan kaldırılan önceki hazırlama tablolarını temizleme işlevselliğini değiştirir. Aşağıdaki tablolar temizleme işlemi tarafından temizlenecektir.

-   Tüm hazırlama tabloları

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

İşlevselliğe **Veri yönetimi \> İş geçmişi temizleme**'den erişilebilir.

### <a name="scheduling-parameters"></a>Parametreleri zamanlama

Temizleme işlemini zamanlarken, temizleme ölçütlerini tanımlamak için aşağıdaki parametrelerin belirtilmesi gerekir.

-   **Geçmişi korumak için gün sayısı** – Bu ayar korunacak yürütme geçmişini miktarını denetlemek için kullanılır. Bu, günlerin sayısını belirtir. Temizleme işi yinelenen bir toplu iş olarak zamanlandığında, bu ayar sürekli olarak hareket eden bir pencere gibi hareket eder, böylece kalanı silirken her zaman belirtilen gün sayısı için geçmişi bırakır. Varsayılan değer 7 gündür.

-   **İş yürütmek için saat sayısı** – Temizlenecek geçmiş miktarına bağlı olarak, temizleme işi için toplam yürütme süresi birkaç dakikadan birkaç saate kadar değişebilir. Sistemde başka bir veri yönetimi etkinliği olduğunda belirtilen tabloların temizlenmesi gerektiğinden, temizleme işi yürütülür ve iş etkinliği başlamadan önce tamamlandığından emin olmak önemlidir.

    En fazla yürütme süresi, iş bu ayarı kullanılarak çalıştırmanız gereken saat sayısı maksimum sınırı ayarlayarak belirtilebilir. Temizleme mantığı, kronolojik olarak düzenlenmiş bir sıradaki bir iş yürütme kimliğinden tek seferde geçer, bunlardan en eskisi ilgili yürütme geçmişinin temizliği için ilk sırada yer alır. Kalan yürütme süresi belirtilen sürenin son %10'unun içinde olduğundan, temizleme için yeni yürütme kimliğini çekme durduracaktır. Bazı durumlarda, temizleme işinin belirtilen en fazla süre içinde devam etmesi beklenir. Bu büyük ölçüde %10 eşiğine ulaşılmadan önce başlatılan geçerli yürütme kimliği için silinecek kayıtların sayısına bağlıdır. Veri bütünlüğünü sağlamak için başlatılan temizlemenin tamamlanması gerekir, yani temizleme belirtilen sınırı aşmasına rağmen devam edecektir. Bu tamamlandığında, yeni yürütme kimliği çekilmez ve temizleme işi tamamlar. Yürütme süresinin yetersizliği nedeniyle temizlenemeyen geri kalan yürütme geçmişi, temizlik işinin bir sonraki programlanışında çekilecektir. Bu ayarın varsayılan ve en düşük değeri 2 saate ayarlanır.

-   **Yinelenen toplu iş** – Temizleme işi tek seferlik, el ile yürütme olarak çalıştırılabilir veya toplu olarak yinelenen yürütme için de zamanlanabilir. Toplu iş, standart toplu iş kümesi olan **Arka planda çalıştır** ayarları kullanılarak zamanlanabilir.
