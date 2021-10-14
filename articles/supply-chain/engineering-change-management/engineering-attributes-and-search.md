---
title: Mühendislik öznitelikleri ve mühendislik özniteliği araması
description: Bu konu, tüm ürün ana verilerinin sisteme kaydedilebilmesini sağlamak için tüm standart dışı özellikleri belirtmek üzere mühendislik özniteliklerini nasıl kullanabileceğinizi açıklar. Ayrıca, bu kayıtlı özelliklere bağlı olarak ürünleri kolayca bulmak için mühendislik özniteliği aramasını nasıl kullanabileceğinizi de açıklar.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f8803e46ce6f104a5afee64faaf393a2df47a61
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568123"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Mühendislik öznitelikleri ve mühendislik özniteliği araması

[!include [banner](../includes/banner.md)]

Tüm ürün ana verilerinin sisteme kaydedilebilmesini sağlamak için tüm standart dışı özellikleri belirtmek üzere mühendislik özniteliklerini kullanmanız gerekir. Daha sonra, bu kayıtlı özelliklere bağlı olarak ürünleri kolayca bulmak için mühendislik özniteliği aramasını kullanabilirsiniz.

## <a name="create-engineering-attributes-and-attribute-types"></a>Mühendislik öznitelikleri ve öznitelik türleri oluşturma

Genellikle, mühendislik ürünleri, yakalamanız gereken birçok niteliğe ve özelliğe sahiptir. Bazı özellikleri standart ürün alanlarını kullanarak kaydedebilirsiniz ancak gerektiğinde yeni mühendislik özellikleri de oluşturabilirsiniz. Kendi *mühendislik özniteliklerinizi* tanımlayabilir ve bunları ürün tanımının bir parçası haline getirebilirsiniz.

Her mühendislik özniteliği bir *öznitelik türüne* ait olmalıdır. Her mühendislik özniteliği, tutabileceği değer türlerini tanımlayan bir *veri türüne* sahip olması gerektiğinden, bu gereksinim mevcuttur. Mühendislik özniteliği türü, standart bir tür (serbest metin, tamsayı veya ondalık gibi) veya özel bir tür (seçilecek belirli bir değer kümesi olan metin gibi) olabilir. Her öznitelik türünü dilediğiniz sayıda mühendislik öznitelikleriyle yeniden kullanabilirsiniz.

### <a name="set-up-engineering-attribute-types"></a>Mühendislik özniteliği türlerini ayarlama

Bir mühendislik özniteliği türünü görüntülemek, oluşturmak veya bunları yeniden oluşturmak için aşağıdaki adımları izleyin.

1. **Mühendislik değişikliği yönetimi \> Kurulum \> Öznitelikler \> Öznitelik türleri**'ne gidin.
1. Liste bölmesinden mevcut bir öznitelik türü seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir öznitelik türü oluşturun.
1. Aşağıdaki alanları ayarlayın:

    - **Öznitelik türü adı**: Öznitelik türü için bir ad girin.
    - **Tür**: Standart bir veri türü seçin (*Para Birimi*, *Tarih Saat*, *Ondalık*, *Tamsayı*, *Metin*, *Boole* veya *Başvuru*).
    - **Sabit liste**: Bu seçenek yalnızca **Tür** alanını *Metin* olarak ayarlarsanız kullanılabilir. Bu tür öznitelikler için belirli değerleri tanımlamak istiyorsanız *Evet* olarak ayarlayın. Bu durumda, bir açılır liste oluşturulur. Bu öznitelik türü için kullanılabilir değerleri oluşturmak üzere **Değer** hızlı sekmesini kullanırsınız. Kullanıcıların diledikleri değeri girebilmesi için bu seçeneği *Hayır* olarak ayarlayın. Bu durumda, bir giriş alanı oluşturulur.
    - **Değer aralığı**: Bu seçenek yalnızca **Tür** alanını *Tamsayı*, *Ondalık* veya *Para Birimi* olarak ayarlarsanız kullanılabilir. Bu tür öznitelikler için kabul edilecek minimum ve maksimum değerleri oluşturmak istiyorsanız *Evet* olarak ayarlayın. Minimum ve maksimum değerleri ile (para birimi için) girdiğiniz sınırlar için geçerli olan para birimini oluşturmak için **Aralık** hızlı sekmesini kullanırsınız. Herhangi bir değeri kabul etmek için bu seçeneği *Hayır* olarak ayarlayın. 
    - **Ölçü birimi**: Bu alan yalnızca **Tür** alanını *Tamsayı* veya *Ondalık* olarak ayarlarsanız kullanılabilir. Bu öznitelik türü için geçerli olan ölçü birimini seçin. Birim gerekmiyorsa bu alanı boş bırakın.

### <a name="set-up-engineering-attributes"></a>Mühendislik öznitelliklerini ayarlama

Bir mühendislik özniteliğini görüntülemek, oluşturmak veya bunları yeniden oluşturmak için aşağıdaki adımları izleyin.

1. **Mühendislik değişikliği yönetimi \> Kurulum \> Öznitelikler \> Mühendislik öznitelikleri**'ne gidin.
1. Liste bölmesinden mevcut bir öznitelik seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir öznitelik oluşturun.
1. Aşağıdaki alanları ayarlayın:

    - **Ad**: Öznitelik için bir ad girin. Bu ad yalnızca **Mühendislik öznitelikleri** sayfasında görünür. Sistemin diğer her yerinde, **Kolay ad** alanının değeri, genellikle özniteliği tanımlamak için gösterilir.
    - **Öznitelik türü**: Önceki bölümde tanımladığınız bir öznitelik türü seçin.
    - **Kolay ad**: Sistemde **(Mühendislik öznitelikleri** sayfası hariç) özniteliği tanımlayacak bir ad girin. 
    - **Açıklama**: Özniteliğin açıklamasını girin.
    - **Yardım metni**: Diğer kullanıcılara özniteliğin ne için kullanıldığını bildiren Yardım metni girin.
    - **Varsayılan değer**: Öznitelik için varsayılan değer girin. Sunulan seçenekler, seçtiğiniz öznitelik türüne bağlıdır.
    - **Para Birimi**: Seçtiğiniz öznitelik türü bir para birimiyse, özniteliğin kabul edeceği ve değerleri göstereceği para birimini seçin.

1. Seçtiğiniz öznitelik türü bir tamsayı veya ondalık sayı ise **Aralık** hızlı sekmesi gösterilir. Bu hızlı sekmede, aşağıdaki alanları gerektiği gibi ayarlayın:

    - **Tolerans eylemi**: Kullanıcı belirtilen aralığın dışında bir değer girerse sistemin nasıl tepki vermesi gerektiğini seçin. *Uyarı*'yı seçerseniz bir uyarı gösterilir ancak kullanıcı değeri kaydedebilir. *İzin verilmez*'i seçerseniz bir uyarı gösterilir ve kullanıcı uyarıyı giderene kadar değer kaydedilemez.
    - **Minimum**: Önerilen veya kabul edilen minimum değeri girin.
    - **Maksimum**: Önerilen veya kabul edilen maksimum değeri girin.

### <a name="engineering-attribute-inheritance"></a>Mühendislik özniteliği devralma

Ürün reçeteleri (BOM'lar) veya formüller gibi ürün yapıları için seçilen öznitelikler alt öğelerden üst öğelere aktarılabilir. Bu süreci "ters devralma" olarak düşünebilirsiniz.

#### <a name="turn-on-this-feature-for-your-system"></a>Sisteminiz için bu özelliği etkinleştirme

Sisteminiz bu bölümde açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Mühendislik Değişiklik Yönetimi için iyileştirilmiş öznitelik devralma* özelliğini açın.

#### <a name="attribute-inheritance-example"></a>Öznitelik devralma örneği

Havuçlu kek gibi bir gıda ürünü için sistem, ürünün içerdiği alerji yapan her maddeyi kaydetmelidir. Havuçlu kek, formülü olan bir mühendislik ürünü olarak sistemde modellenebilir. Bu formül havuçlu kekin un, süt, havuç ve fındık gibi bileşenlerini içerir. Bu örnekte şirket, havuçlu kek için biri laktozlu diğeri laktozsuz olmak üzere iki model sunmaktadır.

Laktozlu kek, içerik düzeyinde aşağıdaki özniteliklere sahiptir:

- Bileşen "un": öznitelik "gluten" = evet
- Bileşen "süt": öznitelik "laktoz" = evet
- Bileşen "fındık": öznitelik "fındık" = evet

Laktozsuz kekte laktozsuz süt kullanılır ve içerik düzeyinde aşağıdaki özniteliklere sahiptir:

- Bileşen "un": öznitelik "gluten" = evet
- Bileşen "süt": öznitelik "laktoz" = hayır
- Bileşen "fındık": öznitelik "fındık" = evet

Bu ürünler çoğunlukla benzer olduğu için bu öznitelikleri alt ürünlerden (iki çeşit) ana ürüne (temel havuçlu kek) aktarmak uygun olabilir. Bu "ters devralmayı" uygulamak için *Öznitelik devralma* işlevini kullanabilirsiniz. Bu işlev, her [mühendislik sürümü](engineering-versions-product-category.md) için tanımlanmıştır.

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Mühendislik özelliklerini bir mühendislik ürünü kategorisine bağlama

Bazı mühendislik öznitelikleri tüm ürünler için geçerli, diğerleri ise tekli ürünlere veya ürün kategorilerine özgüdür. Örneğin, mekanik ürünler için elektrik öznitellikleri gerekmez. Bu nedenle, *mühendislik ürünü kategorileri* ayarlayabilirsiniz. Mühendislik ürünü kategorisi, bu kategoriye ait ürünler için tanımın bir parçası olması gereken mühendislik öznitelikleri koleksiyonunu belirler. Ayrıca, hangi mühendislik özniteliklerinin zorunlu olduğunu ve bunlar için varsayılan değer olup olmadığını da belirtebilirsiniz.

Öznitelikleri kategorilere bağlama da dahil olmak üzere mühendislik ürün kategorileriyle nasıl çalışacağı hakkında daha fazla bilgi için [Mühendislik sürümleri ve mühendislik ürünü kategorilerine](engineering-versions-product-category.md) bakın.

## <a name="set-attribute-values-for-engineering-attributes"></a>Mühendislik öznitelikleri için öznitelik değerleri ayarlama

Bir mühendislik ürünü kategorisine bağlı olan mühendislik öznitelikleri, bu kategoriye göre yeni bir mühendislik ürünü oluşturduğunuzda sunulur. Bu durum gerçekleştiğinde, öznitelikler için değerler ayarlayabilirsiniz. Daha sonra, bu değerler **Mühendislik sürümü** sayfasında veya mühendislik değişikliği emrinde mühendislik değişikliği yönetiminin bir parçası olarak değiştirilebilir. Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Mühendislik ürünü oluşturma

Bir mühendislik ürünü oluşturmak için **Serbest bırakılan ürünler** sayfasını açın. Ardından, Eylem Bölmesi'nde, **Ürün** sekmesindeki **Yeni** gurubunda **Mühendislik**'nü seçin.

Ürünün ait olduğu mühendislik kategorisini belirtmeniz gerekir. Kategori, ürünün tüm varsayılan değerlerini ve özelliklerini ayarlar. Ayrıca ürün için geçerli olan öznitelikleri ayarlar. Kategori seçildikten sonra öznitelikler için değerler ayarlanır. Daha sonra bu değerleri değiştirebilirsiniz.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Mühendislik öznitelik değerlerini kullanarak ürünleri arama

Mühendislik öznitelikleri değerlerini arayarak ürünleri bulmak için mühendislik özniteliği aramasını kullanabilirsiniz. Böylece, mühendislik ürünlerini özelliklerine göre kolayca bulabilirsiniz. Mühendislik ürünü kategorisine ait ürünlerde arama yapabilir veya tüm mühendislik ürünlerinde arama yapabilirsiniz.

Arama, ürün ana veri sayfalarında ve satış siparişleri gibi sistemdeki işlem kalemlerinde kullanılabilir. Bir işlem öğesinde, bir ürünü aramak için **Mühendislik özniteliği arama** sayfasını kullanabilirsiniz. Daha sonra ürünü satış siparişi satırlarına eklemek için **Yeni satır olarak ekle** düğmesini kullanabilirsiniz. Arama sonuçlarındaki ürünler de doğrudan siparişe eklenebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
