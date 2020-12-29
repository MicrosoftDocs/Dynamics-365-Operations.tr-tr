---
title: Ürün boyutları
description: 'Beş ürün boyutu bulunur: renk, yapılandırma, boyut, stil ve sürüm. Ürün boyutlarını boyut gruplarında birleştirebilirsiniz ve ürün master öğelerine boyut grupları atayabilirsiniz. Ürün boyutlarının kombinasyonları, ürün çeşitlerinin nasıl tanımlanacağını belirler.'
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bdfd9482d30bd65cf84fae032df78e1243e05239
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439071"
---
# <a name="product-dimensions"></a>Ürün boyutları

[!include [banner](../includes/banner.md)]

Beş ürün boyutu bulunur: renk, yapılandırma, boyut, stil ve sürüm. Ürün boyutlarını boyut gruplarında birleştirebilirsiniz ve ürün master öğelerine boyut grupları atayabilirsiniz. Ürün boyutlarının kombinasyonları, ürün çeşitlerinin nasıl tanımlanacağını belirler.

Ürün boyutları, ürün varyantı tanımlamaya hizmet eden özelliklerdir. Ürün boyutlarının birleşimleri, ürün varyantları tanımlamak için kullanabilirsiniz. Bir ürün varyantı oluşturmak için bir ana ürüne en az bir ürün boyutu tanımlamanız gerekir.

## <a name="product-variants"></a>Ürün çeşitleri

Ürün varyantlarına maddeler de denilir. Bir madde bir hizmetten farklı olarak somut bir üründür. Hizmet türüyle bir ana ürün tanımlamak da mümkündür. Hizmet türü kullanarak hizmetleri içerecek ürün varyantları belirtebilirsiniz. Örneğin, danışmanlık işi için bir ana ürün ve üst düzey danışmanlar ve alt düzey danışmanlar tarafından gerçekleştirilen iş için ürün varyantları belirtebilirsiniz.

## <a name="product-dimensions"></a>Ürün boyutları

Ürün boyut değerlerini temel alan bir ürün çeşidi oluşturulabilir.

Boyut, renk ve stil boyutlarına ilişkin ürün boyutu değerleri aşağıdaki konumlarda oluşturulabilir:

- **Boyut** sayfası (**Ürün bilgileri yönetimi \> Kurulum \> Boyut ve varyant grupları \> Boyutlar**)
- **Renk** sayfası (**Ürün bilgileri yönetimi \> Kurulum \> Boyut ve varyant grupları \> Renkler**)
- **Stil** sayfası (**Ürün bilgileri yönetimi \> Kurulum \> Boyut ve varyant grupları \> Stiller**)

Yapılandırma boyutuna yönelik ürün boyutu genellikle ya Ürün yapılandırıcısı ya da Boyut bazlı yapılandırıcı kullanılarak oluşturulur. 

Ürün sürümleri genellikle ürün ömrü boyunca geliştiğinden belirli sürümler için oluşturulur. Ürün sürümleri bu konunun ilerleyen kısımlarında ayrıntılı olarak açıklanmıştır.

Ürün boyutları, aşağıdaki konumlardan erişilebilecek **Ürün boyutları** sayfasında da oluşturulup muhafaza edilebilir:

- **Ürün bilgi yönetimi \> Ürünler \> Ana ürünler**'e gidin. Eylem Bölmesinde **Ürün boyutları**'nı seçin.
- **Ürün bilgileri yönetimi \> Ürünler \> Tüm ürünler ve ana ürünler**'e gidin. Bir ana ürün seçin. Eylem Bölmesinde **Ürün boyutları**'nı seçin.
- **Ürün bilgileri yönetimi \> Serbest bırakılan ürünler**'e gidin. Bir ana ürün seçin. Eylem Bölmesinde, **Ürün** sekmesindeki **Ana ürün** gurubunda **Ürün boyutları**'nı seçin.

Maddeler için oluşturabileceğiniz varyant sayısı, olası ürün boyutu kombinasyonlarının sayısı ile sınırlıdır.

> [!TIP]
> Bir ürünü örneğin bir emir satırında kullanırken, birlikle çalışmak istediğiniz ürün varyantını tanımlamak için ürün boyutlarını seçerseniz.

## <a name="example"></a>Örnek

Bir şirket kot kumaşından ürünler satıyor. *Kot* maddesi renk ve boyut boyutlarını kullanıyor. Kot kumaşları üç farklı renk ve altı farklı ebatta satılıyor. Renkler mavi, siyah ve kahverengi. Boyutlar XS, S, M, L, XL ve XXL. Tüm boyutlar her üç renkte de mevcut değil. Kombinasyonların tümü mevcut olsaydı, 18 farklı kot türü olacaktı. Ancak, bu örnekte, yalnızca aşağıdaki dokuz ürün varyantı kombinasyonu üretilir.

| Renk | Ebat |
|-------|------|
| Mavi  | XS   |
| Mavi  | C    |
| Mavi  | P    |
| Siyah | P    |
| Siyah | L    |
| Siyah | XL   |
| Kahverengi | L    |
| Kahverengi | XL   |
| Kahverengi | XXL  |

## <a name="the-version-product-dimension"></a>Sürüm ürün boyutu

Sürüm, tedarik zincirinde bir ürünün birden fazla sürümünü korumanıza ve izlemenize yardımcı olmayı amaçlayan bir ürün boyutudur. Sürüm izleme, ürün kullanım ömrü, artan kalite ve güvenilirlik gereksinimleri ve ürün güvenliği gerektiren bir dünyada çalışan üreticilerin başarısı için gereklidir.

Standart ürün boyutu olarak sürüm, varolan ürün boyutlarına (boyut, stil, renk ve yapılandırma) benzer şekilde davranır. Bu nedenle, bunu ürün sürümlerinin izlenmesi dışında başka amaçlar için kullanabilirsiniz.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Sürüm boyutunu açma

#### <a name="before-you-turn-on-the-version-dimension"></a>Sürüm boyutunu açmadan önce

Sürüm boyutunu etkinleştirdiğinizde, stok boyutlarına özelleştirmeler ekleyen başka çözümler yüklediyseniz, bazı işlevler bozulabilir veya beklendiği şekilde çalışmayı durdurabilir. Sürüm boyutunun tam olarak işlevsel olması için, stok boyutlarına yaptıkları başvurulara sürüm boyutunu dahil etmek üzere bu çözümleri güncelleştirmeniz gerekebilir.

Çözümlerinizi sürüm boyutuyla uyumluluk için test ederken, aşağıdaki öğeleri arayın:

1. **İşlevsellik:** En önemlisi, stok boyutlarını içeren tüm özelleştirmeleri, sürüm boyutuyla birlikte çalışabildiklerinden emin olmak üzere değerlendirmektir.
1. **Stok boyutlarına referans:** Stok boyutlarına yapılan (boyutlara özel olarak başvurulan yerler) referansları arayın. `InventDimId` öğesine yapılan referanslar kullanıma hazır şekilde çalışır ancak stil veya renk başvurularını araştırın. Örneğin, aşağıdaki öğeleri kontrol edin:

    - Genişletilmiş sınıflarda API çağrıları
    - Uzantı kodundaki belirli stok boyutlarına yapılan tüm referanslar (Bu kod sürüm boyutunu stil, renk ve boyut boyutlarıyla birlikte döndürmelidir.)

1. **Eski API çağrılarına başvurular:** Sürüm boyutu kullanıma sunulduğunda Microsoft, mümkün olduğunca eski API'larla aynı sayıda API yapmayı denedi. Kullanımdan kalkmış olan birkaç API **Ürün boyutu - sürüm** yapılandırma anahtarını etkinleştirdiğinizde bir uyarı verebilir. Sürüm boyutunu bir üretim sisteminde etkinleştirmeden önce bu API için yapılan çağrıların genişletilmiş çözümlerinizde düzeltilmesi gerekir. Sürüme özgü eski API'lar şunlardır:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Eşlemeler:** Herhangi bir eşleme stok boyutlarını kullanıyorsa, bu eşlemelere karşılık gelen ilişki eşlemesinin sürüm boyutunu içerecek şekilde güncelleştirilmesi gerekir. Genişletilmiş model veya tablo uzantılarında, alanların stok boyutlarını içerdiği tabloları arayın.
1. **Microsoft Dynamics 365 Commerce işlevi:** Etkinleştirildikten sonra, sürüm boyutu Dynamics 365 Supply Chain Management'taki Commerce'a özgü kodun tamamında görüntülenir. Ancak, sürüm boyutu henüz Commerce kanalı veritabanı tarafından veya satış noktası (POS) uygulamalarında ya da e-ticaret uygulamalarında desteklenmemektedir. Bu Commerce'e özel uygulamalar, sürüm boyutuna göre kullanıcıların stoku satmasını/sevk etmesini veya iade etmesini/almasını desteklemez. Stok kullanılabilirliği arama işlevleri, Commerce uygulamalarındaki sürüm boyutuna göre stoku ayırmayacaktır. Bu davranış, Commerce'taki yapılandırma boyutunun geçerli davranışına benzer.

#### <a name="turn-on-the-version-dimension"></a>Sürüm boyutunu açma

Sürüm boyutunu kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Bu görev yönetici izinleri gerektirir.

1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. *Ürün boyut sürümü* olarak adlandırılan özelliği açın. (Daha fazla bilgi için bkz. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Sisteminizi [Bakım moduna](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) sokun.
1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
1. **Yapılandırma anahtarları** sekmesinde, **Ticaret** öğesisini genişletin ve **Ürün boyutu - sürüm** onay kutusunu seçin.
1. [Bakım modunu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kapatın.

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Sürüm boyutunun desteklenmediği alanlar

Bu boyutun girişi hataya neden olan değişikliklere yol açacağından aşağıdaki alanlar sürüm boyutunu desteklemez:

- Maliyet nesnesi aylık ekstresi
- Maliyet nesnesi raporu önbelleği
- Madde başına MCR satış istatistikleri
- Satıcı katalogları
- EcoResProductDimensionGroupEntity

Ayrıca, Commerce'taki sipariş oluşturma ve sipariş işleme özellikleri (örneğin POS, çağrı merkezi ve e-ticaret siparişleri için) sürüm boyutunu desteklemez. Commerce siparişlerinin bu boyutu desteklemek üzere geliştirilmesine ilişkin onaylannmış bir zaman çizelgesi yoktur.

### <a name="functional-characteristics-of-the-version-dimension"></a>Sürüm boyutunun işlevsel özellikleri

Sürüm boyutu diğer ürün boyutları gibi çalışır. Ancak, özel yapısı nedeniyle ve bir ürünün birden çok sürümünü korumak ve izlemek amacıyla tasarlandığından, biraz farklı davranır. Aşağıda bazı farklılıklar ve benzerlikler verilmiştir:

- **Sürüm grubu yoktur.**

    Boyut, renk ve stil (renk grubu, boyut grubu ve stil grubu) için grup kavramı var olsa da, sürüm grubu kavramı yoktur. Gruplar, örneğin bir ürüne renk grubu atamanız durumunda, ürünün o renk grubundaki tüm renkleri kullanabileceği durumlarda, uygun değerleri önceden tanımlamayı sağlar. Ürün oluşturulduğunda ürünün alacağı sürümler önceden tanımlı olmadığı için, bu kavram sürüm boyutuna uygulanmaz. Bunun yerine, sürümler ürünün kullanım ömrü sırasında gerekli olduklarında oluşturulur. Genellikle, ürünün formu, yapısı ve işlevi aynı kalsa da yeni bir ürün yerine yeni bir sürüm oluşturursunuz.

- **Ürün çeşidi önerileri şu anda çalıştıkları gibi çalışır.**

    Ürün varyantı önerileri, diğer boyutlarda olduğu gibi, tüm sürüm boyut değerleri için öneriler oluşturacaktır. Sürümleri oluşturulan ürünlerin oluşturulması ve serbest bırakılması işlemi diğer boyutları kullanan ürünlerle aynıdır. Sürümü oluşturulan bir ürün oluşturduğunuzda, ilk sürüm (V1) ürün boyutu olarak oluşturulur ve varyantlar serbest bırakılır. Ürün değiştikçe ve yeni bir sürüm gerekli olduğunda, yeni sürüm değeri (sürüm 2) eklenecek ve gereken varyantlar serbest bırakılacaktır. Tüm sürümlerin (V1, V2 ve V3) ürün için önceden oluşturulacağı beklentisi yoktur.

> [!IMPORTANT]
> Sürüm boyutunu açar ve kullanırsanız, stok boyutlarına başvuran bazı çözümler beklendiği gibi çalışmayı durdurabilir. Bu sorunları onaylamak ve gidermek için, etkilenen çözümlerinizin bağımsız yazılım satıcısına (ISV) başvurun. Daha fazla bilgi için bkz. [Sürüm boyutunu etkinleştirme](#enable-version-dim).
