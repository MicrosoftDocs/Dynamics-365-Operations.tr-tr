---
title: Mali boyutlar
description: "Bu konu, çeşitli mali boyut türlerini ve nasıl ayarlandıklarını açıklar."
author: aprilolson
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: d6b7b1219974cb5de1a625d87c3bce2a4439470b
ms.openlocfilehash: 9973d03de031ad2fa5647bb167c12b9231633a22
ms.contentlocale: tr-tr
ms.lasthandoff: 10/01/2018

---

# <a name="financial-dimensions"></a>Mali boyutlar

[!include [banner](../includes/banner.md)]

Bu konu, çeşitli mali boyut türlerini ve nasıl ayarlandıklarını açıklar.

Hesap planları içim hesap segmentleri olarak kullanabileceğiniz mali boyutlar oluşturmak için **Mali boyutlar** sayfasını kullanın. İki tür mali boyut vardır: özel boyutlar ve varlığa dayalı boyutlar. Özel boyutlar tüzel kişilikler tarafından paylaşılır ve değerler kullanıcılar tarafından girilir ve korunur. Varlığa dayalı boyutlar için sistemin herhangi başka bir bölümünde tanımlanan değerler, örneğin Müşteriler veya Mağaza varlıkları. Bazı varlığa dayalı boyutlar tüzel kişilikler tarafından paylaşılırken, diğer varlıklar şirkete özel boyutlar olur.

Mali boyutları oluşturduktan sonra, her mali boyuta ek özellikler atamak için **Mali boyut değerleri** sayfasını kullanın.

Tüzel kişileri temsil etmek için mali boyutları kullanabilirsiniz. Tüzel varlıkları Microsoft Dynamics 365 for Finance and Operations içinde oluşturmanız gerekmez. Bununla birlikte, mali boyutlar, tüzel varlıkların operasyon veya iş gereksinimlerini karşılayacak şekilde tasarlanmamıştır. Finance and Operations'daki birimlerarası muhasebe işlevi, yalnızca her hareket tarafından oluşturulan muhasebe girişlerini karşılamak üzere tasarlanmıştır.

Mali boyutları tüzel kişilikler olarak ayarlamadan önce, bu ayarın kuruluşunuz için uygun olup olmadığını belirlemek üzere iş süreçlerini aşağıdaki alanlarda değerlendirin:

- Stok
- Mali boyutlar ile tüzel kişilikler arasındaki satışlar ve satınalmalar
- Satış vergisi hesaplama ve bildirme
- Operasyonel raporlama

Kısıtlamaların bazıları şunlardır:

- Satış vergisi işlevini yalnızca tüzel kişiliklerle kullanabilirsiniz; mali boyutlarla birlikte kullanamazsınız.
- Bazı raporlar finansal boyutlar içermez. Bu nedenle, finansal boyuta göre bildirmek için raporları değiştirmeniz gerekebilir.

## <a name="custom-dimensions"></a>Özel boyutlar

Kullanıcı tanımlı bir mali boyut oluşturmak için, **Kullan değerin kaynağı** alanından, **&lt;&nbsp;Özel boyut'u seçin&nbsp;&gt;**.

Boyut değerleri için girilebilecek bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz. Harf veya tire (-) gibi her boyut değeri için aynı kalan karakter girebilirsiniz. Bir boyut değeri her oluşturulduğunda değişen karakterler için yer tutucular olan sayı işaretleri (\#) ve 've' işaretleri (&) de girebilirsiniz. Bir sayının yer tutucusu olarak sayı işareti (\#) ve bir harfin yer tutucusu olarak ve işareti (&) kullanın. Biçim maskesi için alan, yalnızca **&lt;&nbsp;Özel boyut&nbsp;&gt;**'u, **Kullanılan değerlerin kaynağı** alanından seçerseniz kullanılabilir.

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

Kriterlerden herhangi biri karşılanıyorsa, mali boyutu silemezsiniz.

## <a name="default-dimension-values"></a>Varsayılan boyut değerleri

Ana kayıtlardan, örneğin müşteri ve satıcı gibi değerleri, yeni boyutlardaki değerler olarak kullanabilirsiniz. Yeni boyut oluşturulduğunda, ana kayıt kimliği, bu ana kayıtlar için boyut değerine girilir. Örneğin, yeni bir müşteri oluşturduğunuzda, müşteri kimliği, müşteri boyutuna girilir. Satış siparişleri, faturalar veya müşteri kimliği gerektiren diğer belgeleri oluşturduğunuzda, mevcut varsayılan kurallar kullanılır ve müşteri kimliği belgeye eklenir.

Bu özellik bir boyut ayarı ile denetlenir. Ayarın adı **Her yeni oluşturulan DimensionName'de bu boyuta değerleri kopyala** olarak adlandırılır, **DimensionName** ise, boyutun adıdır. Varsayılan olarak, bu özellik kapalıdır. Ancak, istenilen zaman açılabilir.

Kayıtlar için boyut varsa, ana kayıt özelliği açtığınızda güncelleştirilir. Bununla birlikte, mevcut belgeler ve hareketler güncelleştirilmez.

## <a name="derived-dimensions"></a>Türetilmiş boyutlar

Bir boyutu, belgedeki başka bir boyut için bilgileri girdiğinizde otomatik olarak girilecek şekilde yapılandırabilirsiniz. Örneğin, maliyet merkezine, 10 değerini girerseniz, **20** otomatik olarak departman boyutuna girilebilir.

Boyutlar sayfasında türetilen değerler ayarlayabilirsiniz.

1. Bir boyut seçip ardından **Türetilen boyutlar**'ı seçin.

    **Türetilen boyutlar** sayfası bir kılavuz içerir. Seçilen boyut bölümü, bu kılavuzdaki ilk sütundur.

2. Türetilecek bölümleri ekleyin. Her bir segment, sütun olarak görünür.

İlk sütundaki boyuttan türetilecek boyut kombinasyonlarını girin. Örneğin, maliyet merkezini, departman ve konumun türetileceği boyut olarak kullanmak için, maliyet merkezine 10, departmana 20 ve konuma 30 girin. Daha sonra, ana kayıtta veya bir hareket sayfasında maliyet merkezine 10 girdiğinizde, departman 20 ve konum 30 varsayıla olarak girilir.

Türetilen boyut işlemi, türetilen boyutlar için mevcut değerleri geçersiz kılmaz. Örneğin, maliyet merkezi 10 girip başka bir boyut girilmediğinde, departman 20 ve konum 30 varsayılan olarak girilir. Bununla birlikte, maliyet merkezini değiştirirseniz, zaten oluşturulmuş değerler değiştirilmez. Bu nedenle, ana kayıtlarda varsayılan boyutlar belirleyebilirsiniz ve bu boyutlar, türetilen boyutlar tarafından değiştirilmez.

### <a name="derived-dimensions-and-entities"></a>Türetilen boyutlar ve varlıklar

Varlıklar kullanarak türetilen boyut segmentlerini ve değerlerini ayarlayabilirsiniz.

- Türetilen boyutlar varlığı, itici boyutları ve bu boyutlar için kullanılan segmentleri ayarlar.
- DerivedDimensionValue varlığı, her bir itici boyut için türetilecek değerleri içe aktarmanıza olanak sağlar.

Veri içe aktarmak için bir varlık kullanıyorsanız, bu varlık boyutları içe aktarıyorsa, türetilen boyut kuralları içe aktarma sürecinde, varlık özellikle bu boyutları geçersiz kılmıyorsa uygulanır.

Daha fazla bilgi için aşağıdaki konulara bakın:

- [Mali boyutları tanımlama](tasks/define-financial-dimensions.md)
- [Mali boyut varsayılan şablonlarını koruma](tasks/maintain-financial-dimension-default-templates.md)

