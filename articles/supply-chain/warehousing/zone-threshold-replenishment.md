---
title: Bölge eşiği stok yenilemesi
description: Bölge tabanlı stok yenileme, minimum/maksimum (min/maks) stok yenileme stratejisi kullanır ancak yalnızca tekil yerleşimler yerine tüm ambar bölgelerini değerlendirir. Bu nedenle, ambar yöneticileri bir malzeme çekme bölgesinde ek stok gerektiğini daha çabuk öğrenebilir.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2e83d6885bf7400916d633a49d3b19b8843b0269
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965514"
---
# <a name="zone-threshold-replenishment"></a>Bölge eşiği stok yenilemesi

[!include [banner](../includes/banner.md)]

Bölge tabanlı stok yenileme, minimum/maksimum (min/maks) [stok yenileme](replenishment.md) stratejisi kullanır ancak yalnızca tekil yerleşimler yerine tüm ambar bölgelerini değerlendirir. Bu nedenle, ambar yöneticileri bir malzeme çekme bölgesinde ek stok gerektiğini daha çabuk öğrenebilir.

Bu özelliğin kurulumu, yerleşim tabanlı stok yenileme kurulumuna benzer. Ancak, minimum/maksimum stok yenileme için bir şablon ayarlarken, eşiğin yerleşim başına mı yoksa bölge başına mı değerlendirileceğini de belirtebilirsiniz. Bölgelere dayalı değerlendirme ayarlarsanız, bölge seçim sorgusuna belirli bölgeler eklemeniz gerekir.

Yerleşim tabanlı minimum/maksimum stok yenileme gibi, bölgeye dayalı minimum/maksimum stok yenileme, seçili maddeler için stok yenileme işi oluşturulmasını tetikleyen bir minimum stok eşiğinin kurulumunu temel alır. Bu stok yenileme işi, stoku bölge için belirtilen maksimum eşiğe kadar artırır.

> [!NOTE]
> Geçerli sürümde, ürün çeşitleri için bölge stok yenileme işlemleri desteklenmiyor.


Yerleşim tabanlı minimum/maksimum stok yenileme işleminden farklı olarak, bölgeye dayalı minimum/maksimum stok yenileme, sabit yerleşimlerin yerleşimlerde belirli bir maddenin depolanıp depolanmayacağını değerlendirmesini zorunlu kılmaz. Bu nedenle, bölge tabanlı stok yenileme, ambarda her madde veya madde çeşidi için sabit yerleşimleriniz olmasa da, minimum/maksimum stok yenilemeyi kullanmanıza olanak sağlar. Bölgedeki bir miktar, belirtilen minimum eşiğin altına düştüğünde stok yenileme işi oluşturulur. Yerleşim yönergeleri, stokun hangi konuma yerleştirilmesi gerektiğini belirler.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Bölge eşiği stok yenilemesi özelliğini açın

*Bölge eşiği stok yenilemesi* özelliğini kullanabilmeniz için, özelliğin sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Bölge eşiği stok yenilemesi*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Bölge tabanlı stok yenilemeyi ayarlama

Bölgeye dayalı stok yenilemeyi ayarlamak için sistemin çeşitli kısımlarını yapılandırmanız gerekir. Bu bölümde çeşitli ayarlar tanıtılmakta ve bu konunun sonundaki senaryo üzerinden çalışmak istiyorsanız girebileceğiniz tanıtım veri değerleri sağlamaktadır.

### <a name="set-up-directive-codes"></a>Yönerge kodlarını ayarlama

[Yönerge kodları ](control-warehouse-location-directives.md), bir iş şablonunda kullanılan yerleşim şablonunu tanımlarken daha kesin bilgiler belirtmenizi sağlar. Her kod, her bir şablon türünü yapılandırırken başvurabileceğiniz ortak bir değer oluşturur.

#### <a name="view-and-edit-directive-codes"></a>Yönerge kodlarını görüntüleme ve düzenleme

Yönerge kodlarınızı görüntülemek veya düzenlemek için, **Ambar yönetimi \> Kurulum \> Yönerge kodları**'na gidin.

#### <a name="prepare-demo-data-directive-codes"></a>Tanıtım verileri yönerge kodlarını hazırlama

Bu örnek, bir yönerge kodunun nasıl hazırlanacağını göstermektedir. Bu konunun sonundaki senaryo üzerinden çalışmayı planlıyorsanız, burada sağlanan tanıtım veri değerlerini kullanın. Aksi durumda, kendi değerlerinizi kullanın.

1. Tanıtım verileriyle çalışmak için **USMF** tüzel kişiliğini seçin.
1. **Ambar yönetimi \> Kurulum \> Yönerge kodları**'na gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Yönerge kodu:** _Bölge stok yenileme_
    - **Yönerge açıklaması:** _Bölge stok yenileme_

1. Yeni kodu kaydetmek için **Kaydet**'i seçin.

### <a name="set-up-replenishment-templates"></a>Stok yenileme şablonlarını ayarla

[Min/maks stok yenileme şablonları](tasks/set-up-min-max-replenishment-process.md) malzeme çekme yerleşimlerinde en uygun düzeyleri korumak için kullanılan birincil mekanizmadır. Bu şablonlarda, ambarda stok yenilemek için kullanılacak kuralları ayarlamanız gerekir. Şablonların kullanılabileceği stok yenileme, bölgeye dayalı stok yenilemeyi içerir.

#### <a name="view-and-edit-replenishment-templates"></a>Stok yenileme şablonlarını görüntüleme ve düzenleme

Stok yenileme şablonu, bir yerleşimde stokun ne zaman ve nasıl yenileneceğini denetleyen kural kümesidir. Stok yenilemenin ne zaman ve nasıl yapılacağını denetlemek için bir şablon seçersiniz. Stok yenileme şablonlarınızı görüntülemek veya düzenlemek için **Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Tanıtım verileri stok yenileme şablonu hazırlama

Bu örnek, bir stok yenileme şablonunun nasıl hazırlanacağını göstermektedir. Bu konunun sonundaki senaryo üzerinden çalışmayı planlıyorsanız, burada sağlanan tanıtım veri değerlerini kullanın. Aksi durumda, kendi değerlerinizi kullanın.

1. Tanıtım verileriyle çalışmak için **USMF** tüzel kişiliğini seçin.
1. **Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin.
1. Sayfayı düzenleme moduna sokmak için **Düzenle**'yi seçin.
1. Eylem bölmesinde, **Genel bakış** kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın. Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Stok yenileme şablonu:** _Bölge min/maks stok yenileme_
    - **Açıklama:** _Bölge min/maks stok yenileme_
    - **Stok yenileme türü:** _Minimum veya maksimum_

1. **Kaydet**'i seçin.
1. **Genel bakış** kılavuzunda yeni satır seçiliyken , yeni oluşturduğunuz *Bölge min/maks stok yenileme* stok yenileme şablonuyla ilişkili bir satır eklemek için **Stok Yenileme Şablonu Ayrıntıları** kılavuzunun yukarısındaki **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** _1_ girin.
    - **Açıklama:** _Malzeme çekme bölge stok yenileme_ girin.
    - **Stok yenileme birimi:** _beher_'i seçin.
    - **İstek türü:** Bu alanı boş bırakın.
    - **Yönerge kodu:** Bu alan, stok yenileme şablonunu bir yerleşim yönergesiyle bağlantılandırır. Daha önce oluşturduğunuz tanıtım verileri yönerge kodunu seçin (_Bölge stok yenileme_).
    - **İş şablonu:** Bu alanı boş bırakın.
    - **Minimum miktar:** Bu alan, stok yenilemenin tetikleneceği miktarı ayarlar. _50_ girin.
    - **Maksimum miktar:** Bu alan, bir maddenin bir bölgede bulunabilecek maksimum miktarını ayarlar. Oluşturulan stok yenileme işi stoku bu miktara artıracaktır. _150_ girin.
    - **Birim:** Bu alan, minimum ve maksimum değerlerin birimini ayarlar. _Beher_'i seçin.
    - **Talep artışı:** _Yuvarla_'yı seçin.
    - **Boş sabit yerleşimleri yenile:** Bu onay kutusunu işaretleyin.
    - **Yalnızca sabit yerleşimeri yenile:** Bu onay kutusunu işaretleyin.
    - **Ürün sorgu modu:** _Ürün sorgusu_'nu seçin.
    - **Stok yenileme eşik kapsamı:** Bu alan, şablonun bölgeye göre mi yoksa belirli bir yerleşime göre mi değerlendirileceğini tanımlar. _Bölge_'yi seçin.
    - **Ambar:** _61_'i seçin.

1. **Stok Yenileme Şablonu Ayrıntıları** kılavuzunun yukarısındaki **Ürünleri seç**'i seçin.
1. **Ürün sorgusu** iletişim kutusundaki **Aralık** sekmesinde **Ekle**'yi seçerek kılavuza bir satır ekleyin:
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** _Maddeler_
    - **Türetilmiş tablo:** _Maddeler_
    - **Alan:** _Madde numarası_
    - **Ölçüt:** _A0001_

1. Sorgunuzu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. **Stok Yenileme Şablonu Ayrıntıları** kılavuzunun yukarısındaki **Stok yenilenecek bölgeleri seç**'i seçin.
1. **Bölge sorgusu** iletişim kutusundaki **Aralık** sekmesinde kılavuza bir satır ekleyin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** _Ambar bölgesi_
    - **Türetilmiş tablo:** _Ambar bölgesi_
    - **Alan:** _Bölge Kodu_
    - **Ölçütler:** _KAT_

1. Sorgunuzu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.

### <a name="set-up-location-directives"></a>Yerleşim yönergelerini kur

Yerleşim temelli min/maks stok yenileme işleminden farklı olarak, sistem giden iş için yalnızca çekme yerleşimi yerine tüm bölgeyi değerlendirdiğinden, bölge temelli min/maks stok yenileme için hem malzeme çekme yerleşim yönergelerini hem de koyma yerleşim yönergelerini ayarlamanız gerekir.

#### <a name="view-and-edit-location-directives"></a>Yerleşim yönergelerini görüntüleme ve düzenleme

Yerleşim yönergelerinizi görüntülemek veya düzenlemek için **Ambar yönetimi \> Kurulum \> Yerleşim yönergeleri**'ne gidin.

Gerekli çekme yerleşimi yönergelerini ve koyma yerleşim yönergelerini oluşturmada ayarların nasıl kullanılacağını gösteren örnekler için sonraki bölüme bakın.

#### <a name="prepare-demo-data-location-directives"></a>Tanıtım verileri yerleşim yönergelerini hazırlama

Tanıtım verilerini bu konunun sonundaki senaryoda kullanılabilecek şekilde hazırlamak için iki yerleşim yönergesi oluşturmanız gerekir: biri çekme ve diğeri koyma için.

##### <a name="create-a-replenishment-pick-directive"></a>Bir stok yenileme çekme yönergesi oluşturma

1. Tanıtım verileriyle çalışmak için **USMF** tüzel kişiliğini seçin.
1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmede, **İş emri türü** alanını _Stok yenileme_ olarak ayarlayın.
1. Eylem bölmesinde **Yeni**'yi seçerek yeni bir yönerge oluşturun.
1. Aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** Varsayılan değeri kabul edin.
    - **Ad:** _Bölge çekme_ girin.
    - **İş türü:** _Çekme_'yi seçin.
    - **Tesis:** _6_'yı seçin.
    - **Ambar:** _61_'i seçin.
    - **Yönerge kodu:** Boş bırakın.
    - **Çoklu SKU:** Bu seçeneği _Hayır_ olarak ayarlayın.

1. Şimdiye kadar yapılandırdığınız ayarları taşıyan bir yönerge oluşturmak için **Kaydet**'i seçin.
1. **Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** _1_ girin.
    - **Başlangıç miktarı:** _0_ girin.
    - **Son miktar:** _10000000_ girin.
    - **Birim:** Bu alanı boş bırakın.
    - **Miktarı bul:** _Yok_'u seçin.
    - **Birime göre kısıtla:** Bu onay kutusunun işaretini kaldırın.
    - **Birime yuvarla:** Bu onay kutusunun işaretini kaldırın.
    - **Ambalaj miktarını bul:** Bu onay kutusunun işaretini kaldırın.
    - **Bölmeye izin ver:** Bu onay kutusunu işaretleyin.

1. Yeni satırı kaydetmek için **Kaydet**'i seçin.
1. Yeni satırınız **Satırlar** kılavuzunda hala seçiliyken, kılavuza satır eklemek için **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** _1_ girin.
    - **Ad:** _Toplu işten çek_ girin.
    - **Sabit yerleşim kullanımı:** _Sabit ve sabit olmayan yerleşimler_'i seçin.
    - **Negatif stoka izin ver:** Bu onay kutusunun işaretini kaldırın.
    - **Toplu iş etkin:** Bu onay kutusunun işaretini kaldırın.
    - **Strateji:** _Yok_'u seçin.

1. Yeni eylemi kaydetmek için **Kaydet**'i seçin.
1. Yeni eyleminiz hala seçiliyken, **Yerleşim Yönergesi Eylemleri** kılavuzunun yukarısındaki **Sorgu düzenle**'yi seçin.
1. Stok yenileme kaynak yerleşimlerini seçebileceğiniz bir sorgu iletişim kutusu görüntülenir. **Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** _Yerleşimler_
    - **Türetilmiş tablo:** _Yerleşimler_
    - **Alan:** _Bölge Kodu_
    - **Ölçüt:** _BULK_

1. Sorgunuzu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. Yerleşim yönergenizi kaydetmek için **Kaydet**'i seçin.

##### <a name="create-a-replenishment-put-directive"></a>Bir stok yenileme koyma yönergesi oluşturma

1. **Yerleşim yönergeleri** sayfasındaki sol bölmede, **İş emri türü** alanının hala _Stok yenileme_ olarak ayarlandığından emin olun.
1. Eylem bölmesinde **Yeni**'yi seçerek yeni bir yönerge daha oluşturun.
1. Aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** Varsayılan değeri kabul edin.
    - **Ad:** _Bölge koyma_ girin.
    - **İş emri türü:** _Koyma_'yı seçin.
    - **Tesis:** _6_'yı seçin.
    - **Ambar:** _61_'i seçin.
    - **Yönerge kodu:** Bu konum yönergesini, daha önce oluşturduğunuz kodu kullanarak daha önce oluşturduğunuz stok yenileme şablonuyla bağlantılandırmak için _Bölge stok yenileme_'yi seçin.
    - **Çoklu SKU:** Bu seçeneği _Hayır_ olarak ayarlayın.

1. Şimdiye kadar yapılandırdığınız ayarları taşıyan bir yönerge oluşturmak için **Kaydet**'i seçin.
1. **Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** _1_ girin.
    - **Başlangıç miktarı:** _0_ girin.
    - **Son miktar:** _10000000_ girin.
    - **Birim:** Bu alanı boş bırakın.
    - **Miktarı bul:** _Yok_'u seçin.
    - **Birime göre kısıtla:** Bu onay kutusunun işaretini kaldırın.
    - **Birime yuvarla:** Bu onay kutusunun işaretini kaldırın.
    - **Ambalaj miktarını bul:** Bu onay kutusunun işaretini kaldırın.
    - **Bölmeye izin ver:** Bu onay kutusunu işaretleyin.

1. Yeni satırı kaydetmek için **Kaydet**'i seçin.
1. Yeni satırınız **Satırlar** kılavuzunda hala seçiliyken, kılavuza satır eklemek için **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** _1_ girin.
    - **Ad:** _Bölge koyma_ girin.
    - **Sabit yerleşim kullanımı:** _Sabit ve sabit olmayan yerleşimler_'i seçin.
    - **Negatif stoka izin ver:** Bu onay kutusunun işaretini kaldırın.
    - **Toplu iş etkin:** Bu onay kutusunun işaretini kaldırın.
    - **Strateji:** _Konsolide et_'i seçin.

1. Yeni eylemi kaydetmek için **Kaydet**'i seçin.
1. Yeni eyleminiz hala seçiliyken, **Yerleşim Yönergesi Eylemleri** kılavuzunun yukarısındaki **Sorgu düzenle**'yi seçin.
1. Stok yenilenecek bölgeyi seçebileceğiniz bir sorgu iletişim kutusu görüntülenir. Bu bölge, stok yenileme şablonunda belirtilen bölgeyle aynı olmalıdır. **Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** _Yerleşimler_
    - **Türetilmiş tablo:** _Yerleşimler_
    - **Alan:** _Bölge Kodu_
    - **Ölçütler:** _KAT_

1. Sorgunuzu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. Yerleşim yönergenizi kaydetmek için **Kaydet**'i seçin.

## <a name="scenario"></a>Senaryo

Bu bölümde, özellikle nasıl çalışılacağını gösteren örnek bir senaryo verilmektedir.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Örnek senaryo için gereken örnek verileri hazırlama

Senaryo üzerinden çalışmaya başlamadan önce, örnek verileri etkinleştirmeniz ve özelliği bu bölümde ve bu konunun önceki bölümlerinde açıklandığı şekilde ayarlamanız gerekir.

#### <a name="use-the-usmf-legal-entity"></a>Tüzel kişilik olarak USMF'yi kullanın

Burada belirtilen örnek kayıtları ve değerleri kullanarak senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

#### <a name="prepare-additional-sample-data"></a>Ek örnek veriler hazırlama

**USMF** tüzel kişiliğini seçtikten sonra, bu konunun önceki [Bölge tabanlı stok yenileme](#setup) bölümünde açıklandığı gibi gerekli ek örnek verileri ekleyin.

#### <a name="check-your-on-hand-inventory"></a>Eldeki stokunuzu denetleme

Sisteminizde örnek senaryoyu destekleyecek yeterli sayıda stok bulunduğundan emin olmak için bu adımları izleyin.

1. Stok yenileme şablonunda belirtilen çekme bölgesindeki (*KAT*) iki farklı konumda *A0001* kodlu madde için eldeki stok bulunduğundan emin olun. Ancak, toplam stok, stok yenileme şablonunda belirtilen gerekli minimum miktardan (*50*) az olmalıdır. Böylece, tek bir yerleşim yerine, tüm bölge için hesaplamanın nasıl gerçekleşeceğinin benzetimini yapabilirsiniz. **Stoku gerektiği gibi ayarlamak için ambar işlemlerini kullanın.**
1. Stok yenileme işinin maddeleri *TOPLU* kodlu bölgeden çekeceği bölge çekme konumu yönergesinde belirtilen bir toplu yerleşimde madde *A0001* için yeterli stok bulunduğundan emin olun. Toplam stok, stok yenileme şablonunda belirtilen gerekli maksimum miktardan (*150*) fazla olmalıdır.
1. İsteğe bağlı olmakla birlikte önerilir: Stok ayarlama günlüğü oluşturmak için şu adımları izleyin:

    1. **Stok yönetimi \> Günlük girişleri \> Maddeler \> Stok ayarlama**'ya gidin.
    1. **Yeni**'yi seçin.
    1. **Stok günlüğü oluştur** iletişim kutusundaki **Ambar** alanında *61*'i seçin.
    1. **Tamam**'ı seçin.
    1. **Günlük satırları** hızlı sekmesinde **Yeni** düğmesini kullanarak kılavuza üç satır ekleyin ve aşağıdaki değerleri ayarlayın. Her satırı ayarlamayı bitirdikten sonra **Kaydet**'i seçin.

        - **Satır 1:**

            - **Madde numarası:** *A0001*
            - **Tesis:** *6*
            - **Ambar:** *61*
            - **Yerleşim:** *02A01R1S1B*
            - **Plaka:** Listeden varolan bir plakayı seçin veya yeni bir plaka oluşturun.
            - **Miktar:** *1000*

        - **Satır 2:**

            - **Madde numarası:** *A0001*
            - **Tesis:** *6*
            - **Ambar:** *61*
            - **Yerleşim:** *07A01R2S1B*
            - **Plaka:** Listeden varolan bir plakayı seçin veya yeni bir plaka oluşturun.
            - **Miktar:** *15*

        - **Satır 3:**

            - **Madde numarası:** *A0001*
            - **Tesis:** *6*
            - **Ambar:** *61*
            - **Yerleşim:** *07A01R1S1B*
            - **Plaka:** Listeden varolan bir plakayı seçin veya yeni bir plaka oluşturun.
            - **Miktar:** *10*

    1. Eylem bölmesinde **Doğrula**'yı seçin. Bir sonraki adıma geçmeden önce bulunan tüm hataları çözün.
    1. Eylem bölmesinde, stoku ambara nakletmek için **Deftere naklet**'i seçin.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Örnek senaryo: Bölge tabanlı min/maks stok yenilemeyi çalıştırma

Tüm önkoşul örnek verileri oluşturulduktan sonra, bu adımları izleyerek stok yenilemeyi tetikleyebilirsiniz.

1. **Ambar yönetimi \> Stok yenileme \> Stok yenilemeleri**'ne gidin.
1. **Stok yenileme** iletişim kutusundaki **Eklenecek kayıtlar** hızlı sekmesinde **Filtre**'yi seçin.
1. **Sorgulama** iletişim kutusundaki **Aralık** sekmesinde, varsayılan tablo satırını aşağıdaki şekilde düzenleyin:

    - **Tablo:** _Stok yenileme şablonları_'nı seçin.
    - **Türetilmiş tablo:** _Stok yenileme şablonları_'nı seçin.
    - **Alan:** _Stok yenileme şablonu_'nu seçin.
    - **Ölçütler:** _Bölge min/maks stok yenileme_'yi seçin. Bu stok yenileme şablonu, bu senaryo için tanıtım verilerini hazırlarken oluşturduğunuz stok yenileme şablonudur.

1. Sorguyu kaydetmek için **Tamam**'ı seçin ve **Stok yenileme** iletişim kutusuna dönün.
1. Stok yenileme şablonunu çalıştırmak için **Tamam**'ı seçin.

*TOPLU İŞ* bölgesinden stok çekmek ve bunu *KAT* bölgesinde stok yenilemek için artık stok yenileme işi oluşturulmuştur.

## <a name="notes-and-tips"></a>Notlar ve ipuçları

Özellikle çalışma hakkında birkaç not ve ipucu:

- İstenen bölgeye giden stok yenileme işi ayarlamak için, stok yenileme şablonu satırlarını ve yerleşim yönergelerini aşağıdaki yollardan biriyle bağlantılandırabilirsiniz:

    - Yerleşim yönergesi başlık sorgusunu düzenleyin ve seçili stok yenileme şablonu satırlarına filtre uygulayın.
    - Stok yenileme şablonu satırında bir yönerge kodu kullanın ve bu kodu, koyma yerleşimi yönergesiyle eşleştirin.

- Dinamik yerleşimleri kullanıyorsanız ve yerleşim yönergesi eylemi **Konsolide etme** stratejisini kullanacak şekilde ayarlandıysa, stok yenileme işi ya ilk uygun yerleşim için veya zaten stok içeren bir yerleşim için oluşturulacaktır.
- Bölgeler yerine sabit yerleşimler kullanıyorsanız [standart min/maks stok yenilemeyi](tasks/set-up-min-max-replenishment-process.md) kullanmanız gerekir.
