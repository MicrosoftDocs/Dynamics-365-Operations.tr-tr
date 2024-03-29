---
title: Mali boyutlar
description: Bu makalede, çeşitli mali boyut türleri ve nasıl ayarlandıkları açıklanmaktadır.
author: aprilolson
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: adfa2c1164550e32b07da25de0d96aa82430b980
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799639"
---
# <a name="financial-dimensions"></a>Mali boyutlar

[!include [banner](../includes/banner.md)]

Bu makalede, çeşitli mali boyut türleri ve nasıl ayarlandıkları açıklanmaktadır.

Hesap planları içim hesap segmentleri olarak kullanabileceğiniz mali boyutlar oluşturmak için **Mali boyutlar** sayfasını kullanın. İki tür mali boyut vardır: özel boyutlar ve varlığa dayalı boyutlar. Özel boyutlar tüzel kişilikler tarafından paylaşılır ve değerler kullanıcılar tarafından girilir ve korunur. Varlığa dayalı boyutlar için sistemin herhangi başka bir bölümünde tanımlanan değerler, örneğin Müşteriler veya Mağaza varlıkları. Bazı varlığa dayalı boyutlar tüzel kişilikler tarafından paylaşılırken, diğer varlıklar şirkete özel boyutlar olur.

Mali boyutları oluşturduktan sonra, her mali boyuta ek özellikler atamak için **Mali boyut değerleri** sayfasını kullanın.

Tüzel kişileri temsil etmek için mali boyutları kullanabilirsiniz. Dynamics 365 Finance içinde tüzel varlıklar oluşturmanız gerekmez. Bununla birlikte, mali boyutlar, tüzel varlıkların operasyon veya iş gereksinimlerini karşılayacak şekilde tasarlanmamıştır. Finance'ta birimlerarası muhasebe işlevi, yalnızca her hareket tarafından oluşturulan muhasebe girişlerini ele almak üzere tasarlanmıştır.

Mali boyutları tüzel kişilikler olarak ayarlamadan önce, bu ayarın kuruluşunuz için uygun olup olmadığını belirlemek üzere iş süreçlerini aşağıdaki alanlarda değerlendirin:

- Stok
- Mali boyutlar ile tüzel kişilikler arasındaki satışlar ve satınalmalar
- Satış vergisi hesaplama ve bildirme
- Operasyonel raporlama

Kısıtlamaların bazıları şunlardır:

- Satış vergisi işlevini yalnızca tüzel kişiliklerle kullanabilirsiniz; mali boyutlarla birlikte kullanamazsınız.
- Bazı raporlar finansal boyutlar içermez. Bu nedenle, finansal boyuta göre bildirmek için raporları değiştirmeniz gerekebilir.

## <a name="custom-dimensions"></a>Özel boyutlar

Kullanıcı tanımlı bir mali boyut oluşturmak için, **Kullan değerin kaynağı** alanından, **Özel boyut**'u seçin.

Boyut değerleri için girilebilecek bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz. Harf veya tire (-) gibi her boyut değeri için aynı kalan karakter girebilirsiniz. Bir boyut değeri her oluşturulduğunda değişen karakterler için yer tutucular olan sayı işaretleri (\#) ve 've' işaretleri (&) de girebilirsiniz. Bir sayının yer tutucusu olarak sayı işareti (\#) ve bir harfin yer tutucusu olarak ve işareti (&) kullanın. Biçim maskesi için alan, yalnızca **Özel boyut**'u, **Kullanılan değerlerin kaynağı** alanından seçerseniz kullanılabilir.

**Örnek**

Boyutu CC" harfleri ve üç sayıyla sınırlamak için biçim maskesi olarak **CC-\#\#\#** girin.

## <a name="entity-backed-dimensions"></a>Varlığa dayalı boyutlar

Varlığa dayalı boyut oluşturmak için, **Kullanılacak değerlerin kaynağı** alanından, mali boyuta temel alınacak bir sistem tanımlı varlık seçin. Mali boyut değerleri daha sonra o varlıktan oluşturulur. Örneğin, projeler için boyut değerleri oluşturmak üzere **Projeler**'i seçin. Daha sonra her proje adı için bir boyut değeri oluşturulur. **Mali boyut değerleri** sayfası, varlık için değerleri gösterir. Bu değerler şirkete özelse, sayfa şirketi de gösterir.

## <a name="activating-dimensions"></a>Boyutları etkinleştirme

Bir mali boyutu etkinleştirdiğinizde, tablo mali boyutun adını da içermek üzere güncelleştirilir. Silinen boyutlar kaldırılır. Bir mali boyutu etkinleştirmeden önce boyut değerini girebilirsiniz. Ancak, bir mali boyut etkinleştirilene kadar hiçbir yerde tüketilemez. Örneğin, mali boyut etkinleştirilene kadar bir hesap yapısına bir mali boyut ekleyemezsiniz. **Etkinleştir** üzerine seçtiğinizde, tüm boyutlar güncelleştirilir ve gösterme durumu değiştir.

## <a name="translations"></a>Çeviriler

**Metin çevirisi** sayfası üzerinde, seçili mali boyutlar için çeşitli dillerde metin girebilirsiniz. **Ana hesap çevirisi** sayfası üzerinde, ana hesap için çeşitli dillerde metin girebilirsiniz. 

## <a name="legal-entity-overrides"></a>Tüzel varlık geçersiz kılmaları

Her tüzel varlık için tüm boyutlar geçerli değildir. Ek olarak, bazı boyutlar yalnızca belirli bir dönem için geçerli olabilir. Bu durumlarda, **Tüzel varlık geçersiz kılmaları** bölümünü, boyutun askıya alınacağı şirketleri, sahibini ve boyutun etkin olacağı dönemi belirlemek için kullanabilirsiniz.

## <a name="deleting-financial-dimensions"></a>Mali boyutları silmek

Verinin referans tutarlılığını korumaya yardımcı olmak amacıyla, mali boyutlar nadiren silinebilir. Bir mali boyutu silmeye çalışırsanız, aşağıdaki kriterler değerlendirilir:

- Mali boyut, nakledilmiş veya nakledilmemiş hareketler veya boyut değeri kombinasyonu üzerinde kullanılmış mıdır?
- Mali boyut, herhangi bir etkin hesap yapısında, gelişmiş kural yapısında veya mali boyut kümesinde kullanılıyor mu?
- Mali boyut, bir varsayılan mali boyut tümleştirme biçiminin parçası mı?
- Mali boyut, bir varsayılan mali boyut olarak ayarlanmış mı?
- Mali boyut Financial Reporting kurulumunda seçilmemiş mu? 

Kriterlerden herhangi biri karşılanıyorsa, mali boyutu silemezsiniz.

> [!NOTE]
> Finance 10.0.27 sürümünden itibaren mali boyutlar, oluşturuldukları için artık mali raporlama kurulumu için otomatik olarak seçilmeyecektir.

## <a name="default-dimension-values"></a>Varsayılan boyut değerleri

Ana kayıtlardan, örneğin müşteri ve satıcı gibi değerleri, yeni boyutlardaki değerler olarak kullanabilirsiniz. Yeni boyut oluşturulduğunda, ana kayıt kimliği, bu ana kayıtlar için boyut değerine girilir. Örneğin, yeni bir müşteri oluşturduğunuzda, müşteri kimliği, müşteri boyutuna girilir. Satış siparişleri, faturalar veya müşteri kimliği gerektiren diğer belgeleri oluşturduğunuzda, mevcut varsayılan kurallar kullanılır ve müşteri kimliği belgeye eklenir.

Bu özellik bir boyut ayarı ile denetlenir. Ayarın adı **Her yeni oluşturulan DimensionName'de bu boyuta değerleri kopyala** olarak adlandırılır, **DimensionName** ise, boyutun adıdır. Varsayılan olarak, bu özellik kapalıdır. Ancak, istenilen zaman açılabilir.

Kayıtlar için boyut varsa, ana kayıt özelliği açtığınızda güncelleştirilir. Bununla birlikte, mevcut belgeler ve hareketler güncelleştirilmez.

Bir ana kayıt oluşturmak için bir şablon oluşturuyorsanız, şablon değerinin ana boyut için boş olduğundan emin olun. Örneğin, bir şablondan müşteriler oluşturuyorsanız, şablondaki müşteri boyutunun boş olduğundan emin olun. Müşteri boyutu değeri, yeni müşteriyi oluşturduğunuzda, yeni müşteri numarasından varsayılan olacaktır.  

## <a name="derived-dimensions"></a>Türetilmiş boyutlar

Bir boyutu, belgedeki başka bir boyut için bilgileri girdiğinizde otomatik olarak girilecek şekilde yapılandırabilirsiniz. Örneğin, maliyet merkezine, 10 değerini girerseniz, **20** otomatik olarak departman boyutuna girilebilir.

Boyutlar sayfasında türetilen değerler ayarlayabilirsiniz.

1. Bir boyut seçip ardından **Türetilen boyutlar**'ı seçin.

    **Türetilen boyutlar** sayfası bir kılavuz içerir. Seçilen boyut bölümü, bu kılavuzdaki ilk sütundur.

2. Türetilecek bölümleri ekleyin. Her bir segment, sütun olarak görünür.

İlk sütundaki boyuttan türetilecek boyut kombinasyonlarını girin. Örneğin, maliyet merkezini, departman ve konumun türetileceği boyut olarak kullanmak için, maliyet merkezine 10, departmana 20 ve konuma 30 girin. Daha sonra, ana kayıtta veya bir hareket sayfasında maliyet merkezine 10 girdiğinizde, departman 20 ve konum 30 varsayıla olarak girilir.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Mevcut değerleri türetilen boyutlarla geçersiz kılma
 
Varsayılan olarak türetilen boyut işlemi, türetilen boyutlar için mevcut değerleri geçersiz kılmaz. Örneğin, maliyet merkezi 10 girip başka bir boyut girilmediğinde, departman 20 ve konum 30 varsayılan olarak girilir. Bununla birlikte, maliyet merkezini değiştirirseniz, zaten oluşturulmuş değerler değiştirilmez. Bu nedenle, ana kayıtlarda varsayılan boyutlar belirleyebilirsiniz ve bu boyutlar, türetilen boyutlar tarafından değiştirilmez.

**Türetilen boyutlar** sayfasında **Mevcut boyut değerlerini türetilen değerlerle değiştir** onay kutusunu seçerek varolan değerleri geçersiz kılmak için türetilmiş boyutlar davranışını değiştirebilisiniz. Bu alan seçilirse, türetilmiş boyut değerlerini içeren boyut girebilirsiniz ve türetilmiş boyut değerleri, önceden varolan değerleri geçersiz kılar. Önceki örneği kullanarak, maliyet merkezi 10 girip başka bir boyut girilmediğinde, departman 20 ve konum 30 varsayılan olarak girilir. Ankcar değerler zaten departman 50 ve konum 60 ise değerler şimdi departman 20 ve konum 30 olarak değiştirilecek.
 
Bu ayarla türetilmiş boyutlar, boyut değerleri varsayılan olduğunda var olan varsayılan boyut değerlerini otomatik olarak değiştirmez. Yalnızca bir sayfada, yeni bir boyut değeri girince ve sayfada bu boyut için mevcut olan türetilmiş değerler varsa boyut değerleri geçersiz kılınır.

### <a name="preventing-changes-with-derived-dimensions"></a>Türetilmiş boyutlarla değişiklikleri engelleme
 
Bir segmenti türetilmiş boyut olarak eklemek için **türetilmiş boyutları sayfasında** **Segment ekle"** yi kullanmdığınızda bir sayfada türetildiğinde o boyuta değişiklik ypamanızı önleyen **Segment ekle** sayfasının altında bir seçenek verilir. Türetilmiş boyut değerlerini değiştirilmesini önlemesi için varsayılan ayarı devre dışıdır. Boyutun türetildikten sonra değişmesini önlemek isterseniz ayarı **Evet** olarak değiştirin. Örneğin, Departman boyut değeri Maliyet merkezi boyut değerinden türetilirse Departman değeri, **Değişiklikleri engelle** ayarı **Evet** olduğunda değiştirilemez. 
 
Boyut değerinin geçerli olduğu halde türetilmiş boyutlar listesinde yoksa ayar, değişikliklere engel olmaz. Örneğin Bölüm 20, türetilen Maliyet merkezi 10'dna türetilirse ve Maliyet merkezi 10 girerseniz Bölüm 20'yi düzenleyemezsiniz. Bununla birlikte, Maliyet merkezi 20 girerseniz ve Maliyet merkezi için türetilen boyutlar listesinde yoksa Departman değeri düzenleyebilirsiniz. 
 
Türetilmiş boyutları değerleri uygulandıktan sonra her zaman tüm boyut değerleri ve hesap değeri yine de hesap yapılarıyla doğrulanacaktır. Türetilmi değerleri kullanırsanız ve bir sayfada kullanıldığında doğrulanmazlarsa harekette kullanabilmeniz için önce türetilmiş boyutlar sayfasındaki türetilmiş boyut değerlerini değiştirmeniz gerekir. 
 
**Mali boyutları** hızlı sekmesinde boyutları değiştirdiğinizde değişiklikleri önlemek için işaretlenmiş boyut düzenlenebilir olmaz. Bir sayfada bölümlenmiş giriş denetime bir hesap ve boyut giriyorsanız, boyutlar düzenlenebilir. Ancak bölümlenmiş giriş denetimi vurgusunu taşır ve başka bir alana taşırsanız ya da eylemde bulunursanız hesap ve boyutlar, uygun değerleri girdiğinizden emin olmak için türetilmiş boyutları listesine ve hesap yapılarına göre doğrulanır. 

### <a name="derived-dimensions-and-entities"></a>Türetilen boyutlar ve varlıklar

Varlıklar kullanarak türetilen boyut segmentlerini ve değerlerini ayarlayabilirsiniz.

- Türetilen boyutlar varlığı, itici boyutları ve bu boyutlar için kullanılan segmentleri ayarlar.
- Türetilen boyutlar değeri varlığı, her bir itici boyut için türetilecek değerleri içe aktarmanıza olanak sağlar.

Veri içe aktarmak için bir varlık kullanıyorsanız, bu varlık boyutları içe aktarıyorsa, türetilen boyut kuralları içe aktarma sürecinde, varlık özellikle bu boyutları geçersiz kılmıyorsa uygulanır.

## <a name="financial-dimension-service"></a>Mali boyut hizmeti

Mali boyut hizmeti eklentisi, Microsoft Dynamics Lifecycle Services ortamınızda kullanılabilir. Çok sayıda satırı olan bir günlüğü içe aktarmak için Veri yönetimi çerçevesi kullandığınızda performansın artırılmasını sağlar. Hizmeti kullanmak için, **Mali boyut hizmeti parametreleri** sayfasında etkinleştirmeniz gerekir. Şu anda hizmet yalnızca 500 satırı veya daha fazlasını içeren içe aktarılan günlüklerde çalışır. Ek olarak, şu anda sadece **Genel muhasebe** hesabı türünün günlük satırlarında ayarlandığı genel günlükleri işleyebilir. Günlük satırlarındaki **Müşteri**, **Satıcı** ve **Banka** gibi diğer hesap türleri şu anda desteklenmemektedir. Bu hizmet, türetilmiş boyutlar sistemde ayarlandığında çağrılamaz.

Günlükler, veri içe aktarma işlemiyle paralel olarak çalışan yeni bir hizmet kullanılarak içe aktarıldığında, Mali boyut hizmeti gelişmiş performans sağlar. Yalnızca günlükteki ana hesapta ve finansal boyut verilerinde çalışır ve günlük satırlarındaki genel muhasebe hesap dizesi alanında belirtilen boyut birleşimlerini oluşturur. İşlem bu dizeyi, Mali boyut çerçevesinin doğrulama, özet raporlama ve sorgulamalar için ürünün geri kalanı boyunca kullandığı yapısal veri deposuna dönüştürür. Mali boyut verilerinin özet raporu hakkında dah afazla bilgi için bkz. [Mali boyut kümeleri](financial-dimension-sets.md).

Daha fazla bilgi edinmek için aşağıdaki konulara bakın:

- [Mali boyutları tanımlama](tasks/define-financial-dimensions.md)
- [Mali boyut varsayılan şablonlarını koruma](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
