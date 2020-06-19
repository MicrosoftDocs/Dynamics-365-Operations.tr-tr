---
title: Perakende satışlar için kupon ayarlama
description: Bu konu kuponlarına genel bakış sağlar ve bunların nasıl ayarlanacağını açıklar.
author: scott-tucker
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a07bed244152327047efd68cfacb329a722c0049
ms.sourcegitcommit: 97206552616b248f88e516fea08b3f059257e8d1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431990"
---
# <a name="set-up-coupons-for-retail-sales"></a>Perakende satışlar için kupon ayarlama

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Kuponlara genel bakış

Kuponlar, hareketleri iskontoları eklemek için kullanılan barkodlar ve kodlardır. Her kuponda birden fazla kod olabilir ve her kodun kendi geçerlilik tarihleri bulunabilir.

Her kupon bir iskontosuyla ilişkilidir. İskontoyla ilişkilendirilen fiyat grupları bir kuponu kullanabilecek müşteriyi veya kuponun geçerli olduğu kanalları tanımlar.

Esas olarak, kuponlar iskontoları üzerinde ek bir doğrulamadır. Kuponlar, gerekli olan kupon kodları ve bar kodlar ile bu kodların tarih aralığını sağlar. Kupon ayrıca isteğe bağlı kullanım sınırları ve müşterinin gerektirdiği özellikleri de sağlar. İskonto kuponun geçerli olduğu ürün kümesini sağlar. İskonto için fiyat grupları kuponun geçerli olduğu müşteri kümelerini, kanalları veya katalogları sağlar.

Kupon oluşturmak için iskontoyu ve kuponu ayrı olarak oluşturun. Bunun ardından Commerce'deki kupon sayfasında iskontoyu seçerek bunları birbirine bağlayın.

> [!NOTE]
> Bir Kupon bir iskontoya bağlandıktan sonra, kupon ayarları tarafından yönetildiklerinden Commerce'deki iskonto sayfasında için birçok alan salt okunur olur. Bu alanlar standart tarih aralıkları ve durum alanlarını içerir.

### <a name="limited-use-coupons"></a>Sınırlı kullanım kuponları

Kuponlar sınırlı kullanım kuponları olarak yapılandırılabilir. Kullanım sınırı müşteri ya da kanal başına ya da genel bir sınır olarak tanımlanabilir. Kod veya barkod girildiğinde veya POS'ta tarandığında veya satış siparişi girişi sırasında bu sınır zorlanır.

Limit, kupondaki kupon kodu başına zorlanır. Örneğin, iki kupon kodu içeren bir tek kullanım kupon iki kez kullanılabilir: her kupon kodu için bir kez. Kupondaki her kod bağımsız olarak etkin olacak şekilde ayarlanabilir.

Kuponlar tüm satış kanallarda kullanılabilir ancak, çağrı merkezi siparişleri için sınırlı kullanım kuponları yalnızca çağrı merkezindeki **sipariş tamamlama** ayarının etkin olduğu çağrı merkezleri siparişleri için kullanılabilir. Bu etkin değilse, arama merkezi siparişlerinde yalnızca sınırlı olmayan kullanım tipi Kuponlar kullanılabilir.

> [!NOTE]
> Kupon kodu kullanım sınırına ulaştığında sistem kupon kod durumunu otomatik olarak "Kullanıldı" olarak *değiştirmez*. Ancak bu kupon kodu kullanım sınırına ulaşmış olduğundan kullanılamaz. Kupon kod durumu **Etkin** dışında bir ayara el ile ayarlanmışsa, bu kupon kodu herhangi bir kanalda kullanılamaz.  

## <a name="managing-coupons"></a>Kupon yönetimi

İskontoyu ve kuponu ayrı olarak oluşturmanız gerekir. Ardından kupon sayfasında iskontoyu seçerek bunları birbirine bağlayın. Kuponu bir iskontoya bağladıktan sonra, kupon ayarları tarafından yönetildiklerinden iskonto için birçok alan salt okunur olur. Bu alanlar standart tarih aralıkları ve durum alanlarını içerir.

Esas olarak, kuponlar iskontoları üzerinde ek bir doğrulamadır. Kuponlar, kupon kodlarını ve bar kodları, tarih aralıklarını, kullanım limitlerini ve gerekli müşteri özelliğini sağlar. İskonto kuponun geçerli olduğu ürün kümesini sağlar. İskonto fiyat grupları kuponun geçerli olduğu müşteri kümelerini, kanalları veya katalogları sağlar.

## <a name="system-setup-for-coupons"></a>Kuponlar için sistem kurulumu

Kupon ayarlamadan önce, kupon bar kodu ve iki numara serisi ayarlamanız gerekir.

1. **Maske karakterleri** sayfasında, kupon kodu için yeni bir maske karakteri oluşturun. Kullanılmamış herhangi bir karakteri seçebilirsiniz.
2. **Barkod maskesi kurulumu** sayfasında, yeni bir barkod maskesi oluşturun. **Tür** alanını **Kupon** olarak ayarlayın.
3. **Barkod kurulumu** sayfasında, az önce oluşturduğunuz barkod maskesini kullanan yeni bir bar kod oluşturun.
4. **Numara serileri** sayfasında, iki yeni numara serisi oluşturun. Bir seri kupon kodu kimliği ve diğer seri kupon numarası içindir. Kupon kodu kimliği bir kupondaki her kupon kodu için benzersiz tanımlayıcıdır. Kupon numarası, kupon için benzersiz bir tanımlayıcıdır. Her kuponda kuponu tetikleyen birden fazla kod ve barkod olabilir.

    > [!NOTE]
    > Her iki numara serisi için **Kapsam** alanını **Şirket** olarak ayarlamanız gerekir. Çoğu durumda, her iki numara serisini otomatik olarak oluşturmanız gerekir.

5. **Commerce parametreleri** sayfasında, **Barkodlar** sekmesinde, daha önce oluşturduğunuz barkodu seçin.
6. **Commerce paylaşılan parametreleri** sayfasında, **Numara serileri** sekmesinde, kupon numarası ve kupon kodu kimliği için oluşturduğunuz numara serilerini seçin.
7. Artık **Kuponlar** sayfasını açıp yeni kuponlar oluşturabilirsiniz.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Kısmi güncelleştirmelerin kupon üzerindeki etkisi

Kupon işlevi birçok farklı özellik içerir. Commerce Headquarters (HQ) ve kanalı bileşenler arasında kısmi olarak güncelleştirilebilir. Bu nedenle, kısmi güncelleştirmelerin kuponun tüm işlevselliği nasıl etkilediğini anlamanız önemlidir.

- **Genel merkez kısmen güncelleştirildi ancak Commerce Scale Unit ve POS güncelleştirilmedi** Bir Genel Merkez güncelleştirmesinde, kupon ve iskonto sayfaları güncelleştirilir ve ticaret fiyatı altyapısı da güncelleştirilir. Bu iki bileşenden yalnızca biri güncelleştirilirse, Commerce'deki bazı sayfalar fiyat hesaplama verileriyle eşleşmeyecektir. Bu nedenle, iskonto hesaplamaları sırasında beklenmeyen iskonto hesaplamaları veya hatalar oluşabilir.
- **Genel merkez güncelleştirildi ancak Commerce Scale Unit ve POS güncelleştirilmedi (N-1).** Aynı anda tüm mağazalar güncelleştirilemediğinden, genel merkezi mağazaları güncelleştirmeden önce güncelleştirmenizi öneririz. N-1 senaryosunda, kuponlarla ilişkili yeni işlev henüz güncelleştirilmemiş mağazalarda kullanılamaz. Örneğin, kupon işlevi satırları "hariç tut" işlevi sunar. Bir iskontoda satırları hariç tut özelliği kullanırsanız, daha önceki bir sürümü çalıştıran bir mağaza uygulanmaz.
- **Genel merkez güncelleştirilmedi ancak Commerce Scale Unit ve POS güncelleştirildi (N+1).** Commerce Scale Unit'deki güncelleştirilmiş fiyat alt yapısı hesaplamalar sırasında eski iskonto kodlarını işleyebildiğinden, güncelleştirmenin bu senaryo üzerinde etkisi olmayacaktır.
