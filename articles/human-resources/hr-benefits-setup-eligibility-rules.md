---
title: Uygunluk kurallarını ve seçeneklerini yapılandırma
description: Bu makalede, Microsoft Dynamics 365 Human Resources'daki Kazanç yönetiminde uygunluk kurallarının ve seçeneklerinin nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
ms.date: 09/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 916a9955327aef67ac768d4505bdb343862058a1
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644097"
---
# <a name="configure-eligibility-rules-and-options"></a>Uygunluk kurallarını ve seçeneklerini yapılandırma 

Yan haklar yönetimi için gerekli parametreleri yapılandırdıktan sonra, kazanç planlarınızla ilişkilendireceğiniz uygunluk kuralları, demeti, dönemler ve programlar oluşturabilirsiniz.

Uygunluk kuralları, çalışanların bir plan için uygun olup olmadığını belirlemek için kullanılır. Çalışanların, yan haktan yararlanabilecek şekilde kabul edilebilmesi için en az bir kuralın koşuluna uyması gerekir. Örneğin, bir planda iki kuralınız vardır. İlk kural (satır 1), personel türünün **Personel** olması gerektiğini belirtir. İkinci kural (satır 2), personelin tam zamanlı olarak istihdam edilmiş olması gerektiğini belirtir. Bu nedenle, kural 1'i karşılayan personel sadece yarı zamanlı olarak çalıştırılsalar bile uygundur.

Ancak, birden çok koşulu olan tek bir kural ayarlayabilirsiniz. Bu durumda, personelin yan haktan yararlanmaya uygun kabul edilebilmesi için kuralın tüm koşullarını yerine getirmesi gerekir. Örneğin, **Tam Zamanlı Personel** adlı bir kuralınız vardır. Bu kural, personel türünün **Personel** olmasını *ve* personelin tam zamanlı olarak istihdam edilmiş olması gerektiğini belirtir. Bu nedenle, personelin uygun olabilmesi için kuralın her iki koşuluna da uyması gerekir.

> [!IMPORTANT]
> Her yan hak planıyla en az bir uygunluk kuralı ilişkilendirilmelidir. Bir yan hakla birden çok kuralı ilişkilendirebilirsiniz.

## <a name="create-an-eligibility-rule"></a>Uygunluk kuralı oluştur

Uygunluk kuralları, hangi çalışanların her bir kazanç planına kaydolabileceği tanımlar. Uygunluk kurallarını tanımladıktan sonra, onları kazanç planlarına atarsınız. Böylece, her plana uygun olan çalışanları görmek için kayıt uygunluğunu işleyebilirsiniz. 

Açık kayıt sırasında çalışanlar kazanç planlarını seçebilir. Zaten kaydolduktan sonra uygunluk kurallarına dayalı bir kazanç planı için uygun değilse, bunlar otomatik olarak kaydedilmezler. Genellikle, plan uygunluğunu etkileyen bir ömür olayı gerçekleştiğinde, çalışan için uygun oldukları planları seçmek amacıyla bir kayıt dönemi başlatılır. 

1. **Yan haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Uygunluk kuralları** sekmesinde, uygunluk kuralı oluşturmak için **yeni**'yi seçin. Uygunluk kuralıyla ilişkili planları görmek için **ilişik planlar**'ı seçin.

3. Aşağıdaki alanların değerleri belirtin.

   | Alan | Tanım |
   | --- | --- |
   | **Uygunluk kuralı** | Uygunluk kuralı için benzersiz bir tanımlayıcı. |
   | **Açıklama** | Uygunluk kuralının açıklaması. |
   | **Geçerlilik başlangıç tarihi ve saati** | Uygunluk kuralının başlangıç tarihi. | 
   | **Geçerlilik bitiş tarihi ve saati** | Uygunluk kuralının bitiş tarihi. |
   | **Kullanıcı personel türü** | Yan hak uygunluğu kuralını, çalışanın çalışan tarafından mı kullanacağınızı belirtir. |
   | **Çalışan türü** | Çalışan türü, **Personel türünü kullan** **Evet** olarak ayarlanmışsa. |
   | **Personel durumu kullan** | Yan hak uygunluğu kuralında çalışanın istihdam durumu tarafından mı kullanacağınızı belirtir. |
   | **Durum** | Personel durumu, **Personel durumu kullan** **Evet** olarak ayarlanmışsa. **Personel durumunu kullan** **Hayır** olarak ayarlanmışsa alan kullanılmaz. |
   | **İstihdam kategorisi kullan** | Yan hak uygunluğu kuralının parçası olarak personelin **İstihdam kategorisi** değerinin kullanılıp kullanılmayacağını belirtir. | 
   | **İstihdam kategorisi** | **İstihdam kategorisini kullan** geçişi **Evet** olarak ayarlanmışsa personelin istihdam kategorisi. |
   | **Yeni işe alma kuralı kullan** | Yan haklar kuralının bir parçası olarak yeni işe alma dönemi değerinin kullanılıp kullanılmayacağını belirtir. |
   | **Kayıt dönemi** | Yeni işe alma kaydına izin verildiği zaman dilimi. Bunu aynı zamanda parametrelerde ayarlarsanız, parametreler ayarı da bunun üzerine öncelik kazanır. |
   | **Önceki istihdam durumunu kullan** | Yan hak uygunluğu kuralının parçası olarak personelin önceki istihdam durumunun kullanılıp kullanılmayacağını belirtir. Örneğin, önceki istihdamını takip eden 90 gün içinde **İşten çıkarıldı** durumundan **İstihdam edildi** durumunda geçil yapmış tüm çalışanlar için bir karşılama bekleme dönemini uygulatmayan bir uygunluk kuralı belirtebilirsiniz. |

4. **Ek ölçütler** altında, aşağıdaki seçenekleri seçin ve gerekli bilgileri ekleyin.

   | Seçenek | Tanım |
   | --- | --- |
   | **Uygun yaş** | Uygunluk kuralını karşılamak için gerekli yaş veya Aralık aralıklarını belirtir. |
   | **Uygun departman** | Uygunluk kuralını karşılamak için çalışanın içinde olması gereken Departmanı veya departmanları belirtir. |
   | **Uygun istihdam türü** | Uygunluk kuralını karşılamak için çalışanın içinde olması gereken istihdam türü veya türleri belirtir. Örneğin, tam saat veya parça zaman. |
   | **Uygun iş** | Uygunluk kuralına uyan işi veya işleri belirtir. İşler pozisyonlarla ilişkilendirilir ve pozisyonlar çalışanlar tarafından doldurulur. |
   | **Uygun iş görevi** | Uygunluk kuralına uyan işlevi veya işlevleri belirtir. Örneğin, satış çalışanları veya teknisyenler. |
   | **Uygun iş türü** | Uygunluk kuralına uyan türü veya türleri belirtir. Örneğin, bir büro memuru veya yönetici. |
   | **Uygun tüzel kişilik** | Uygunluk kuralı için geçerli olan yasal varlığı veya yasal varlıkları belirtir. Örneğin, Contoso eğlence sistemi USA. |
   | **Uygun ücret bölgesi** | Uygunluk kuralına uyan çalışan konumunu belirtir. Örneğin, merkez ABD |
   | **Uygun pozisyon** | Uygunluk kuralına uyan pozisyon veya pozisyonları belirtir. Örneğin, İK Yardımcısı veya İK müdürü. |
   | **Uygun pozisyon türü** | Uygunluk kuralına uyan pozisyon veya pozisyonları belirtir. Örneğin, tam zaman. |
   | **Uygun eyalet** | Uygunluk kuralına uyan iller veya eyaletleri belirtir. Örneğin, Kuzey Dakota ABD veya İngiliz Columbia, Kanada. |
   | **Uygun istihdam koşulları** | Uygunluk kuralına uyan istihdam şartları belirtir. Örneğin, grupta veya grup sözleşmeniz. |
   | **Uygun sendika** | Uygunluk kuralına uyan işçi sendikası üyelikleri belirtir. Örneğin, Amerika Forklift sürücüleri.</br></br>Sendika tabanlı uygunluk kuralı kullanırken, çalışanın sendika kaydı bitiş tarihine sahip olmalıdır. Boş bırakamazsınız. |
   | **Uygun Posta kodu** | Uygunluk kuralına uyan ZIP/posta kodu belirtir. Örneğin, 58104. |

5. **Ek ayrıntılı** bilgi için aşağıdaki ek ayrıntıları görüntüleyebilirsiniz.

   | Alan | Tanım |
   | --- | --- |
   | **Uygun kullanıcı alanı** | Müşteri tanımlı alanlara dayalı olarak ek uygunluk kurallarını belirtir. |
   | **Uygunluk türü** | **Ek ölçütler** altında seçtiğiniz ölçüt kategorisini belirtir. |
   | **Uygunluk referansı** | **Ek ölçütler** altında seçtiğiniz değerleri belirtir. |
   | **Açıklama** | **Ek ölçütler** altında seçtiğiniz açıklama. |

6. **Kaydet**'i seçin.

## <a name="using-custom-fields-in-eligibility-rules"></a>Özel alanların uygunluk kurallarında kullanılması

Ek bilgileri izlemek için insan kaynakları içinde [özel alanlar](hr-developer-custom-fields.md) oluşturulabilir. Bu alanlar doğrudan Kullanıcı arabirimine eklenebilir ve bir sütun, temel alınan tabloya dinamik olarak eklenir.  

Özel alanlar uygunluk sürecinde kullanılabilir. Uygunluk kuralları bir çalışanın uygunluğunu belirlemek için bir veya daha fazla özel alan değeri kullanabilir.  Varolan bir kurala özel alan eklemek veya yeni bir kural oluşturmak için, **sosyal haklar yönetimi > bağlantılar > Kurulum > Uygunluk kuralları > özel alan uygunluğu**'na gidin. Bu sayfa içinde, bir veya birden çok özel alan kullanan bir kural oluşturabilir ve uygunluğu belirlemek üzere her özel alan için birden fazla değer tanımlayabilirsiniz.

Aşağıdaki tablolar, uygunluk işlemede kullanılabilen özel alanları destekler:

- Çalışan (HcmWorker)  
- İş (HcmJob)  
- Pozisyon (HcmPosition)  
- Pozisyon ayrıntısı (HcmPositionDetail)  
- Pozisyon Çalışan Ataması  
- Çalışma (Hcmemplone)  
- EmploymentDetails (HcmEmploymentDetails)  
- İş Ayrıntıları (HcmJobDetails)  

Aşağıdaki özel alan türleri, uygunluk işlemede desteklenir:

- Metin  
- Seçim listesi  
- Sayı  
- Ondalık  
- Onay kutusu  

Aşağıdaki tablo özel alan uygunluk formu alan bilgilerini gösterir.

| Alan  | Tanım |
|--------|-------------|
| Kuruluş adı | Oluşturulan ölçütlerin adı. |
| Tablo adı | Uygunluk kuralı için kullanılan özel alanı içeren tablo adı. |
| Alan adı | Uygunluk kuralı olarak kullanılacak alan. |
| İşleç türü | Özel alan uygunluk yapılandırmasında kullanılan operatörü görüntüler. |
| Değer | Özel alan uygunluk yapılandırmasında kullanılan değeri görüntüler. |

## <a name="eligibility-logic"></a>Uygunluk mantığı

Aşağıdaki bölümlerde, yararlı uygunluk haklarının nasıl işlendiği açıklanmaktadır.

### <a name="rules-assigned-to-a-plan"></a>Plana atanan kurallar 
Bir kazanç planına birden fazla uygunluk kuralı atandığında, bir çalışan en az bir kurala, kazanç planına kaydolmaya uygun olacak şekilde uyması gerekir.  Aşağıdaki örnekte, çalışan **iş türü** kuralı veya **etkin çalışanlar** kuralındaki gereksinimleri karşılamalıdır.

![Çalışan iş türü kuralı veya etkin çalışanlar kuralındaki gereksinimleri karşılamalıdır.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Uygunluk kuralı içindeki ölçütler 
Kural içinde, kuralı oluşturan ölçütü tanımlarsınız. Yukarıdaki örnekte, **İş türü** kuralının ölçütü, İş Türü = Direktör şeklindedir. Bu nedenle, uygun olması için çalışanın bir yönetmen olması gerekir. Bu, kural içinde yalnızca bir ölçütün bulunduğu bir kuraldır.

Birden çok ölçütü olan kurallar tanımlayabilirsiniz. Uygunluk kuralı içinde birden çok ölçüt tanımladığınızda, bir çalışan, kazanç planı için uygun olacak şekilde kural içindeki tüm kriterleri karşılamalıdır. 

Örneğin, yukarıdaki **Aktif personel** kuralı aşağıdaki ölçütlerden oluşur. Çalışanın **etkin çalışanlar** kuralına dayalı olarak uygun olabilmesi için , çalışanın yasal MF varlığında *ve* tam zamanlı bir pozisyon türüne sahip olması gerekir.  

![Uygunluk kuralı içindeki ölçütler.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Ölçüt içinde birden çok koşul

Kurallar, tek bir ölçüt içinde çoklu koşulları kullanmak üzere daha fazla genişletilebilir. Çalışan, uygun olması için en az bir koşulu karşılamalıdır. Yukarıdaki örnekte oluşturmak için, **etkin çalışanlar** kuralı, aynı zamanda yarı zamanlı çalışan çalışanları içerecek şekilde daha da genişletilebilir. Sonuç olarak, artık çalışan USMF'de çalışan *ve* tam zamanlı veya yarı zamanlı çalışan olmalıdır.  

![Ölçüt içinde birden çok koşul.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Özel alan ölçütündeki uygunluk koşulları 
Yukarıdakiyle benzerlik olarak, özel alanlar uygunluk kuralları oluştururken ve aynı şekilde çalışırken kullanılabilir. Örneğin, internet maliyetleri bu konumlarda daha yüksek olduğu için evden çalışan Fargo ve Kopenhag çalışanlarına Internet geri ödeme teklif etmek isteyebilirsiniz. Bunu yapmak için, iki özel alan oluşturun: **Office konumu** (seçim listesi) ve **evden çalışma** (onay kutusu). Sonra **WFH Çalışanları** adında bir kural oluşturun. Kural ölçütü, **Office konumu = Fargo** veya **Kopenhag** *ve* **Evden çalışma = Evet** şeklindedir.

Özel uygunluk kurallarının aşağıdaki görüntüde belirtildiği gibi ayarlanması gerekir. 

![Özel alan ölçütündeki uygunluk koşulları.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Ürün demetlerini yapılandırma

Bir dizi ilgili kazanç planları kümesidir. Bir çalışanın, başka bir kazanç planına bağımlı olabilecek belirli bir avantaj planına kayıt yapmak için seçmesi gereken kazanç planlarını gruplamak için kazançlar demeti kullanabilirsiniz. Bir ürün demetini kullanmak isteyebileceğiniz durumlarda örnekler şunlardır:

- İlişkili bir sistem durumu tasarruf hesabı (HSA) içeren yüksek kesinti yapılabilen sağlık sigortası içeren bir sistem durumu planı paketi.

- Bir bağımlı ömür planıyla birlikte gelen zorunlu çalışan ömür sigortası planı olan bir ömür sigortası planı. Bu, çalışanın çalışan kapsamı için kaydolmadan bağımlı ömür kapsamını seçmemesini sağlar.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Ürün demetleri** sekmesinde, bir paket oluşturmak için **yeni**'yi seçin. Ürün paketiyle ilişkili planları görmek için **ilişik planlar**'ı seçin.

3. Aşağıdaki alanların değerleri belirtin.

   | Alan | Tanım |
   | --- | --- |
   | **Görev Demeti** | Ürün demeyinin benzersiz tanımlayıcısı |
   | **Açıklama** | Ürün demeti açıklaması. |
   | **Ana** | Paketteki planlardan birinin Master plan olarak işaretlenip işaretlenmemesi gerektiğini gösterir. Ana plan açık kayıt sırasında, yan haklar yöneticisi personelin yan haklarının koşullarını onaylayabilmesi için başlangıçta seçilen kümenin bir parçası olarak seçilmelidir. |
   | **Gerekli**| Ürün demetindeki başka bir plan kullanıma almak için planın seçilmesi gerektiğini belirtir. Birden fazla plan, **Gerekli** olarak işaretlenebilir. Bu durumda, **Gerekli** olarak işaretlenen tüm planların ürün demetindeki herhangi bir planın kullanıma alınması için seçilmesi gerekir.|
   | **Geçerlilik başlangıç tarihi ve saati** | Ürün demetinin etkin olduğu tarih ve saat. |
   | **Geçerlilik bitişi** | Ürün demetinin bitiş tarihi. Varsayılan 12/31/2154'dir ve hiçbir zamanı belirtir. |

4. **Kaydet**'i seçin.

## <a name="configure-periods"></a>Dönemlerini yapılandırma

Dönemler, kazançların etkili olduğu ve çalışanların ne zaman kayıt yapmasına izin verileceğini tanımlar. Yararları korumak için istediğiniz sayıda dönem oluşturabilir, açık kayıt ve kazanç tedarik dönemleri oluşturabilirsiniz. Kazanç planı yıllar takvim yılını izleyebilir veya izleyemeyebilir. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Dönemler** sekmesinde, bir dönem oluşturmak için **yeni**'yi seçin. Geçerli tüm etkin kazanç planlarını avantaj dönemine bağlayan bir işlemi çalıştırmak için, ilgili **Plan Ekle**'yi seçin. Ürün paketiyle ilişkili planları görmek için **ilişik planlar**'ı seçin. 

3. Aşağıdaki alanların değerleri belirtin.

   | Alan | Tanım |
   | --- | --- |
   | **Dönem** | Dönemi için benzersiz bir tanımlayıcı. |
   | **Geçerlilik başlangıç tarihi ve saati** | Sosyal haklar döneminin etkin olduğu başlangıç tarihi ve saati. |
   | **Geçerlilik bitiş tarihi ve saati** | Sosyal haklar döneminin devre dışı olduğu tarihi ve saati. |
   | **Kayıt başlangıcı** | Açık kayıt için başlangıç tarihi. Açık kayıt, bir çalışanın self servis avantajlarında avantajlara sahip olması halinde olabilir. |
   | **Kayıt bitişi** | Açık kayıt için bitiş tarihi. |
   | **Aç** | Dönemin, sistem tarihi ve geçerlilik başlangıç ve bitiş tarihleri ile saatleri temel alınarak açık olup olmadığını gösterir. | 
   | **Önceki dönem** | Seçilen kazançlar döneminin önündeki kazançlar dönemini belirtir. Bu bilgiler, önceki bir yıldan planlar, kapsam seçenekleri ve görevlendirilenleri atamak için kazanç uygunluğu kaydı sırasında kullanılır. |
 
4. **Kaydet**'i seçin.

## <a name="use-a-flex-credit-program"></a>Esnek kredi programı kullanma

Çalışanları, önceden belirlenmiş esnek kredi sayısına göre sosyal haklar kaydetmek için, esnek kredi programlarını kullanabilirsiniz. Çalışanlar esnek kredileri nasıl tahsis etmek için seçim yapabilir. Örneğin, bir personelin eşinin sağlık durumu planı kapsamında olması durumunda, yan haklardaki kullanılması gereken kredilerini diğer yan haklar kapsamında kullanılmasını isteyebilir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Dönemler** sekmesinde, **esnek kredi programlarını** seçin.

3. Uygulanacak esnek kredi programını seçin. Alanlar şu bilgileri kapsar.

   | Alan | Tanım |
   | --- | --- |
   | **Kazanç kredisi kodu** | Esnek kredi programının benzersiz tanımlayıcısı. |
   | **Tanım** | Esnek kredi programı açıklaması. | 
   | **Başlangıç tarihi** | Esnek kredi programının etkin olacağı tarih. |
   | **Bitiş tarihi** | Esnek kredi programının son tarihi. Esnek kredi programının zamanlanan bir sona erme tarihi olmadığını belirtmek için varsayılan değeri (12/31/2154) boş bırakabilirsiniz. |
   | **Toplam Kredi Değeri** | Her çalışanın avantajları için kullanması gerekecektir kullanılan alacak sayısı. |
   | **Eşit Dağıtma Kuralı** | Esnek kredi dönemi ortasında bir çalışan işe alındığında, esnek krediler için kullanılacak kural. </br></br><ul><li>**Hiçbiri** – esnek kredi programı başlatıldıktan sonra işe alındığında çalışan esnek kredi almaz.</li><li>**Tam kredi** – çalışan, işe alındıklarında bağımsız olarak, tüm esnek kredi tutarını alır.</li><li>**Eşit dağıt** – çalışan, başlangıç tarihlerine göre eşit miktarda esnek kredi alır.</li></ul> |
   | **Esnek Kredi Eşit Dağıtma Formülü** | Esnek kredi programının kazanç dönemi ortasında bir çalışan işe alındığında, esnek krediler için kullanılacak kural. Kat, istihdam başlangıç tarihine dayanır. Bu alan yalnızca **eşit dağıtma kural** ı alanında **eşit dağıt** seçeneği seçildiğinde kullanılır. </br></br><ul><li>**Günlük** – bir çalışanın gün düzeyine alacağı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki gün sayısına bölünür. Örneğin, bir avantaj dönemi 400 gün ise, sistem günde alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 400 ile bölecektir.</li><li>**Geçerli ay** - Bir çalışanın geçerli aya yuvarlanmış, ay düzeyine aldığı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki ay sayısına bölünür. Örneğin, bir avantaj dönemi 15 ay ise, sistem ayda alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 15 ile bölecektir.</li><li>**Sonraki ay** - Bir çalışanın sonraki aya yuvarlanmış, ay düzeyine aldığı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki ay sayısına bölünür. Örneğin, bir avantaj dönemi 15 ay ise, sistem ayda alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 15 ile bölecektir.</li></ul> |
   
   Her bir kazanç planının her bir avantaj dönemine göre yalnızca bir esnek kredi programına kaydedildiğinizden emin olun. Aksi durumda, sistem, esnek jenerik vermek için hangi esnek kredi programını kullanacağınızı bilmeyecek ve sorunlarla karşılaşacaksınız. 

## <a name="configure-programs"></a>Programları konfigüre et

Programlar, ortak uygunluk kuralları kümesini paylaşan bir dizi kazanç planındaysa. Her bir plan için, programın tamamı yerine uygunluk kuralları tanımlayabilirsiniz. Örneğin, contoso Kanada FTE programı veya contoso Avrupa Executive-seviye programı. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Programlar** sekmesinde, bir program oluşturmak için **yeni**'yi seçin. Uygunluk kuralı gereksinimlerini karşılamayan çalışanlara özel durumlar yapmak için **uygunluk kuralı geçersiz kılma**'yi seçin. Programla ilişkili planları görmek için **ilişik planlar**'ı seçin.

3. Aşağıdaki alanların değerleri belirtin.

   | Alan | Tanım |
   | --- | --- |
   | **Program** | Program için benzersiz tanımlayıcı. |
   | **Açıklama** | Programın bir açıklaması | 
   | **Geçerlilik başlangıç tarihi ve saati** | Programın etkin olduğu tarih ve saat. |
   | **Geçerlilik bitiş tarihi ve saati** | Programın süresinin dolduğu olduğu tarih ve saat. Varsayılan 12/31/2154'dir ve hiçbir zamanı belirtir. |
   | **Karşılama bekleme dönemi** | Kazanç programı için, bir çalışanın tedarik başlangıcından önce beklemesi gereken dönem. |
   | **Kesinti bekleme dönemi** | Kazanç programı için kesintiler başlamadan önce bir çalışanın beklemesi gereken dönem. |
   | **Uygunluk kuralları** | Kazançlar programına uygulanacak uygunluk kurallarını seçin. Uygunluk kurallarını bu sayfadaki **uygunluk kuralları** sekmesinde tanımlarsınız. |
   
4. **Kaydet**'i seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
