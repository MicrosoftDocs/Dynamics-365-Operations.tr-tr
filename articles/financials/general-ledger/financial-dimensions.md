---
title: Mali boyutlar
description: "Bu konu, çeşitli mali boyut türlerini ve nasıl ayarlandıklarını açıklar."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a>Mali boyutlar

[!include[banner](../includes/banner.md)]

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

Kullanıcı tanımlı bir mali boyut oluşturmak için, **Kullanılan değerin kaynağı** alanından, **&lt; Özel boyut &gt;**'u seçin. Boyut değerleri için girebileceğiniz bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz. Harf veya tire (-) gibi her boyut değeri için aynı kalan karakter girebilirsiniz. Bir boyut değeri her oluşturulduğunda değişen harfler ve sayılar için yer tutucular olan sayı işaretleri (\#) ve 've' işaretleri (&) de girebilirsiniz. Bir sayının yer tutucusu olarak sayı işareti (\#) ve bir harfin yer tutucusu olarak ve işareti (&) kullanın. Biçim maskesi için alan, yalnızca **&lt; Özel boyut &gt;**'u, **Kullanılan değerlerin kaynağı** alanından seçerseniz kullanılabilir.

**Örnek**

Boyutu CC" harfleri ve üç sayıyla sınırlamak için biçim maskesi olarak **CC-\#\#\#** girin.

## <a name="entity-backed-dimensions"></a>Varlığa dayalı boyutlar

Varlığa dayalı boyut oluşturmak için, **Kullanılacak değerlerin kaynağı** alanından, mali boyuta temel alınacak bir sistem tanımlı varlık seçin. Mali boyut değerleri daha sonra o varlıktan oluşturulur. Örneğin, projeler için boyut değerleri oluşturmak üzere **Projeler**'i seçin. Daha sonra her proje adı için bir boyut değeri oluşturulur. **Mali boyut değerleri** sayfası, varlık için değerleri gösterir. Bu değerler şirkete özelse, sayfa şirketi de gösterir.

## <a name="activating-dimensions"></a>Boyutları etkinleştirme

Bir mali boyutu etkinleştirdiğinizde, tablo mali boyutun adını da içermek üzere güncelleştirilir. Silinen boyutlar kaldırılır. Bir mali boyutu etkinleştirmeden önce boyut değerini girebilirsiniz. Ancak, bir mali boyut etkinleştirilene kadar hiçbir yerde tüketilemez. Örneğin, mali boyut etkinleştirilene kadar bir hesap yapısına bir mali boyut ekleyemezsiniz. **Etkinleştir** üzerine tıkladığınızda, tüm boyutlar güncelleştirilir ve gösterme durumu değiştir. 

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


Daha fazla bilgi için aşağıdaki konulara bakın:
- [Mali boyutları tanımlama](tasks/define-financial-dimensions.md)
- [Mali boyut varsayılan şablonlarını koruma](tasks/maintain-financial-dimension-default-templates.md)

