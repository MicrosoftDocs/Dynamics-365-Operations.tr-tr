---
title: Elektronik raporlama bileşenleri
description: Bu makalede, Elektronik raporlama (ER) bileşenleri açıklanmaktadır.
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285046"
---
# <a name="electronic-reporting-components"></a>Elektronik raporlama bileşenleri

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) aşağıdaki bileşen türlerini destekler:

- Veri modeli
- Model eşleme
- Biçim
- Meta veriler

## <a name="data-model-component"></a>Veri modeli bileşeni

Bir veri modeli bileşeni, bir veri yapısının soyut bir temsilidir. Belirli bir iş alanı alanını, o alan için raporlama gereksinimlerini karşılayacak kadar ayrıntılı olarak açıklar. Veri modeli bileşeni aşağıdaki bölümlerden oluşur:

- **Veri modeli**: Etki alanına özgü iş varlıkları kümesi olarak veri modeli ve bu varlıkların aralarındaki ilişkilerin hiyerarşik olarak tanımı.
- **Model eşleme**: Seçilen uygulama veri kaynakları, çalıştırma zamanında veri akışını ve bir veri modeli bileşenine iş verilerini girme kurallarını belirten bir veri modelinin ayrı öğelerine bağlanır.

Veri modelinin iş varlığı, konteyner veya kayıt olarak temsil edilir. İş varlığı özellikleri, veri öğeleri veya alanlar olarak temsil edilir. Her veri öğesinin benzersiz bir ad, etiket, açıklama ve değeri vardır. Her bir veri öğesinin değeri dize, tamsayı, tarih, çetele (numaralandırma) veya Boole değeri olarak tanınacak şekilde tasarlanabilir. Ek olarak, veri öğesi başka bir kayıt veya kayıt listesi olabilir.

Tek bir veri modeli bileşeni, birden fazla etki alanı iş varlığı hiyerarşisi içerebilir. Ayrıca çalıştırma zamanında rapora özel bir veri akışını destekleyen model eşlemelerini de içerebilir. Hiyerarşiler, model eşleme için bir kök olarak seçilen tek bir kayıtla ayrılır. Örneğin, ödeme etki alanının veri modeli aşağıdaki eşlemeleri destekliyor olabilir:


- Şirket \> Satıcı \> AP etki alanının ödeme hareketleri
- Müşteri \> Şirket \> AR etki alanının ödeme hareketleri

Şirket ve ödeme hareketleri gibi iş varlıkları yalnızca bir kez tasarlanır. Farklı eşlemeler bunları gerektiği gibi yeniden kullanabilir.

## <a name="model-mapping-component"></a>Model eşleme bileşeni

Model eşleme, uygulama veri kaynaklarını, çalıştırma zamanında veri akışını ve bir veri modeli bileşenine iş verilerini girmek için kuralları belirten bir veri modelinin ayrı öğelerine bağlar.

Giden elektronik belgeleri destekleyen bir model eşleştirmesi aşağıdaki özellikleri içerir:

- Veri modeli için veri kaynakları olarak farklı veri türlerini kullanabilir. Bu veri türleri tabloları, veri varlıklarını, yöntemleri ve sabit listeleri içermektedir.
- Çalışma zamanında bazı verilerin belirtilmesi gerektiğinde bir veri modeli için veri kaynakları olarak tanımlanabilen kullanıcı giriş parametrelerini destekler.
- Gerekli gruplara veri dönüştürmeyi destekler. Ayrıca verileri filtreleyebilir, sıralayabilir, toplayabilir ve Microsoft Excel formüllerine benzeyen formüller aracılığıyla tasarlanmış mantıksal hesaplanan alanlar ekleyebilirsiniz. Daha fazla bilgi için bkz. [Elektronik raporlamada (ER) formül tasarımcısı](general-electronic-reporting-formula-designer.md).

Gelen elektronik belgeleri destekleyen bir model eşleştirmesi aşağıdaki özellikleri içerir:

- Farklı güncelleştirilebilir veri öğelerini hedefler olarak kullanabilir. Bu veri öğeleri tablolar, veri varlıkları ve görünümler içerir. Veriler, elektronik belgelerden gelen veri ile güncelleştirilebilir. Birden çok hedef tek bir model eşlemede kullanılabilir.
- Çalışma zamanında bazı verilerin belirtilmesi gerektiğinde bir veri modeli için veri kaynakları olarak tanımlanabilen kullanıcı giriş parametrelerini destekler.

Raporlama için birleşik veri kaynağı olarak kullanılan her iş alanına bir veri modeli bileşeni tasarlanmıştır. Birleşik veri kaynağı, raporlamayı veri kaynaklarının fiziksel uygulamasından ayırır. Bileşen, bir raporlama formatının ilk tasarımını ve sonraki bakımlarını daha verimli hale getiren bir biçimde alana özgü iş kavramlarını ve işlevlerini temsil eder.

## <a name="format-component"></a>Biçim bileşeni

### <a name="format-components-for-outgoing-electronic-documents"></a>Giden elektronik belgeler için biçim bileşenleri

Biçim bileşeni, çalışma zamanında oluşturulan raporlamanın çıkış şemasıdır. Plan aşağıdaki öğelerden oluşur:

- Çalışma zamanında oluşturulan giden elektronik belgenin yapısını ve içeriğini tanımlayan biçim.
- Bir dizi kullanıcı giriş parametresi ve seçilen model eşlemesini kullanan etki alanına özgü veri modeli olarak veri kaynakları.
- Çalışma zamanında veri akışı ve biçim çıkışı oluşturma kurallarını belirleyen biçimin ayrı öğelerine sahip olan bir küme biçim veri kaynağı bağlaması olarak biçim eşlemesi.
- Çalışan bağlama bağlı olarak, çalışma zamanında rapor oluşturmayı kontrol eden yapılandırılabilir kurallar kümesi olarak biçim doğrulaması. Örneğin, bir satıcının ödemelerinin çıktı oluşturmasını durduran bir kural olabilir ve seçilen satıcının, örneğin banka hesap numarası gibi belirli öznitelikleri eksik olduğunda bir özel durum ilan edebilir.

Biçim bileşeni aşağıdaki işlevleri destekler:

- Metin, XML, Microsoft Word belgesi veya çalışma sayfası gibi çeşitli formatlarda tek tek dosyalar olarak raporlama çıktısı oluşturma
- Birden fazla dosyayı ayrı ayrı oluşturma ve bu dosyaları zip dosyalarına kapsülleme

Biçim bileşeni, raporlama çıktısında kullanılabilen belirli dosyaları eklemenize olanak sağlar:

- OPENXML çalışma biçiminde çıktı için şablon olarak kullanılabilen bir çalışma sayfasını içeren Excel çalışma kitapları
- Word dosyaları, Microsoft Word belgesi biçiminde çıktı için bir şablon olarak kullanılabilecek bir belge içerebilirler.
- Önceden tanımlanmış dosyalar olarak biçim çıktısına dahil edilebilen diğer dosyalar

Aşağıdaki görsel, verinin bu biçimler için nasıl aktığını gösterir.

[![Giden biçim bileşenleri için veri akışı](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Biçim yapılandırmasının eşleşmesini, tek bir ER biçim yapılandırmasını çalıştırmak ve giden bir elektronik belge oluşturmak için tanımlamanız gerekir.

#### <a name="format-components-for-incoming-electronic-documents"></a>Gelen elektronik belgeler için biçim bileşenleri
Bir biçim bileşeni, çalışma zamanında içe aktarılan gelen belgenin planıdır. Plan aşağıdaki öğelerden oluşur:

- Çalışma zamanında içe aktarılan veriyi içeren gelen elektronik belgenin yapısını ve içeriğini tanımlayan bir biçim. Bir biçim bileşeni, bir gelen belgeyi metin ve XML gibi çeşitli biçimlerde ayrıştırmak için kullanılır.
- Etki alanına özel bir veri modelinin öğelerine ayrı ayrı biçim öğeleri bağlayan bir biçim eşlemesi. Çalışma zamanında, veri modelindeki öğeler, bir gelen belgedeki verileri içe aktarmak için veri akışını ve kuralları belirtir ve daha sonra veriyi bir veri modelinde depolar.
- Bir biçim doğrulaması bağlamında çalışan bağlı olarak çalışma zamanında veri içe aktarmayı denetleyen yapılandırılabilir kurallar kümesi olarak. Örneğin, bir satıcının ödemelerini içeren bir banka ekstresinin veri içe aktarması durduran bir kural olabilir ve satıcının satıcı kimlik saptama kodu gibi belirli öznitelikleri eksik olduğunda bir özel durum ilan edebilir.

Aşağıdaki görsel, verinin bu biçimler için nasıl aktığını gösterir.

[![Gelen biçim bileşenleri için veri akışı](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Gelen bir elektronik belgeden veri içe aktarmak için tek bir ER biçim yapılandırması çalıştırmak için bir biçim yapılandırmasının arzulanan eşlemesini ve ayrıca bir model eşlemesinin tümleştirme noktasını tanımlamanız gerekir. Aynı model eşlemesini ve hedefleri, farklı türde gelen belgeler için farklı biçimlerle birlikte kullanabilirsiniz.


## <a name="component-versioning"></a>Bileşen sürüm oluşturma

Sürüm Oluşturma ER bileşenleri için desteklenir. Aşağıdaki iş akışı ER bileşenlerindeki değişiklikleri yönetmek için sağlanır:

1. Başlangıçta oluşturulan sürüm **Taslak** sürüm olarak işaretlenir. Bu sürüm düzenlenebilir ve test çalıştırmaları için kullanılabilir.
2. **Taslak** sürümü **Tamamlandı** sürümüne dönüştürülebilir. Bu sürüm yerel raporlama işlemlerinde kullanılabilir.
3. **Tamamlandı** sürümü **Paylaşımlı** sürümüne dönüştürülebilir. Bu sürüm, Microsoft Dynamics Lifecycle Services (LCS) içinde yayımlanır ve genel raporlama işlemlerinde kullanılabilir.
4. **Paylaşılan** sürümü **Devam ettirilmeyen** sürümüne dönüştürülebilir. Bu sürüm silinebilir.

**Tamamlandı** veya **Paylaşılan** durumuna sahip sürümler diğer veri değişimleri için kullanılabilir. Aşağıdaki eylemler, şu durumlara sahip bir bileşen üzerinde gerçekleştirilebilir:

- Bileşen, XML biçiminde sıralanabilir ve XML biçiminde bir dosya olarak dışa aktarılabilir.
- Bileşen bir XML dosyasından tekrar sıralanabilirler ve ER bileşeninin yeni bir sürümü olarak uygulamadan içe aktarılabilirler.

Daha fazla bilgi için bkz. [Yeni bir veri modeli yapılandırmasını içe aktarma](er-quick-start1-new-solution.md#ImportDataModel) ve [Türetilmiş bir biçimin tamamlanmış sürümünü dışa aktarma](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Çalışma zamanında taslak sürümleri

ER çerçevesi için kişisel kullanıcı parametreleriniz içinde, çalışma zamanında ER yapılandırmasının taslak sürümünün kullanılması gerektiğini belirtmenize olanak tanıyan seçeneği etkinleştirebilirsiniz. Kendi ER yapılandırmalarınız için **Taslak Çalıştır** seçeneğini kullanılabilir hale getirme hakkında bilgi için bkz. [Özel bir biçimi çalıştırılabilir olarak işaretleme](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> ER kullanıcı parametreleri şirkete özgü ve kullanıcıya özgüdür.

### <a name="draft-format-versions-at-runtime"></a>Çalışma zamanında taslak biçimi sürümleri

Varsayılan olarak, bir ER çözümü çalıştırdığınızda, denetimin biçim bileşenlerinin taslak sürümleri dikkate alınmaz. Bunun yerine, yalnızca **Taslak** dışında bir durumu olan ilgili sürüm kullanılır. Bazen, çalışma zamanında, ER'yi biçim yapılandırmanızın taslak sürümünü kullanmaya zorlamak isteyebilirsiniz. Örneğin, taslak sürümünüze gerekli değişiklikleri sunduktan sonra, test çalıştırması yapmak için söz konusu taslak sürümünü kullanabilirsiniz. Bu şekilde, değişikliklerinizin doğruluğunu teyit edebilirsiniz. Taslak biçimi sürümünü kullanmaya başlamak için ilgili ER yapılandırmasının **Taslak Çalıştır** seçeneğini **Evet** olarak [ayarlamanız](er-quick-start2-customize-report.md#MarkFormatRunnable) gerekir.

### <a name="draft-model-mapping-versions-at-runtime"></a>Çalışma zamanında taslak modeli eşleme sürümleri

Varsayılan olarak, bir ER çözümü çalıştırdığınızda, çözümün model eşleme bileşenlerinin taslak sürümleri her zaman kullanılır. Bazen, çalışma zamanında, ER'yi ER modeli eşleme yapılandırmanızın taslak sürümünü kullanmaya zorlamak isteyebilirsiniz. **Sürüm 10.0.29 ve sonrasında**, çalışma zamanında kullanılan model eşleme sürümünü denetlemek üzere **ER model eşlemeleri için her zaman "Taslak çalıştır" seçeneğini dikkate al** özelliğini etkinleştirebilirsiniz. Bu özellik etkinleştirildiğinde, aşağıdaki davranış ortaya çıkar:

- Bir model eşleme yapılandırması için **Taslak Çalıştır** seçeneği **Hayır** olarak ayarlandığında, çalışma zamanında o yapılandırmanın taslak olmayan en yüksek sürümü kullanılır. Yapılandırma geçerli Finance örneğinde yoksa, özel durum oluşur.
- Bir model eşleme yapılandırması için **Taslak Çalıştır** seçeneği **Evet** olarak ayarlandığında, çalışma zamanında o yapılandırmanın taslak sürümü kullanılır.

## <a name="component-date-effectivity"></a>Bileşen tarihi geçerlilik

ER biçimi bileşen sürümlerinin geçerlilik tarihi vardır. ER biçim bileşeninin raporlama süreçleri için etkin hale geldiği tarihi belirtmek üzere "geçerlilik başlangıç tarihini" ayarlayabilirsiniz. Uygulama oturum tarihi bir bileşenin yürütme için geçerli olup olmadığını tanımlamak için kullanılır. Belirli bir tarih için birden fazla sürüm geçerliyse raporlama işlemleri için en son sürüm kullanılır.

## <a name="component-access"></a>Bileşen erişim

ER biçimi ve model eşleme bileşenlerine çalışma zamanında erişim Uluslararası Standartlar Teşkilatı (ISO) ülke/bölge kodu ayarına bağlıdır. Bu ayar bir biçim veya model eşleme yapılandırmasının seçili sürümü için boşsa çalışma zamanında herhangi bir şirketten biçim veya model eşleme bileşenine erişilebilir. Ayar ISO ülke/bölge kodlarını içeriyorsa biçim veya model eşleme bileşeni yalnızca biçim bileşeninin ISO ülke/bölge kodlarından biri için tanımlanmış birincil adresi olan şirketlerde kullanılabilir.

Bir biçim veya model eşleme bileşeninin farklı sürümleri ISO ülke/bölge kodları için farklı ayarlara sahip olabilir.

Daha fazla bilgi için bkz. [Ülke bağlamına bağımlı ER model eşlemelerini yapılandırma](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

