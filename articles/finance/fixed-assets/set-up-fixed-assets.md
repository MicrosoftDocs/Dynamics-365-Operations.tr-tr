---
title: Sabit kıymetleri ayarlama
description: Bu konu, Sabit kıymetler modülünün kurulumu hakkında genel bir bakış sunar.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9eef9d8c58d19b05901035f4c679ee7d9902819
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180318"
---
# <a name="set-up-fixed-assets"></a>Sabit kıymetleri ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, **Sabit kıymetler** modülünün kurulumu hakkında genel bir bakış sunar.

## <a name="overview"></a>Özet

Parametreler, Sabit kıymetler içindeki genel davranışı kontrol eder.

Sabit kıymet grupları, kıymetlerinizi gruplamanızı ve bir gruba atanan her kıymet için varsayılan öznitelikleri belirtmenizi sağlar. Defterler, sabit kıymet gruplarına atanır. Defterler, amortisman profilinde tanımlanan amortisman yapılandırmasını kullanarak bir sabit kıymetin zaman içindeki mali değerini izler.

Sabit kıymetler oluşturulduklarında bir gruba atanır. Varsayılan olarak, sabit kıymet grubuna atanan defterler ardından sabit kıymete atanır. Genel muhasebeye nakledilmek üzere yapılandırılan defterler deftere nakil profiliyle ilişkilendirilir. Genel muhasebe hesapları, deftere nakil profilinde her defter için tanımlanır ve sabit kıymet hareketleri deftere nakledildiğinde kullanılır.

![Sabit kıymet bileşenleri](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Amortisman profilleri

Öncelikle amortisman profillerini oluşturulmanız gerekir. Amortisman profilinde bir kıymetin değerinin zaman içinde nasıl amorti edildiğini yapılandırırsınız. Amortisman yöntemini, amortisman yılını (takvim yılı veya mali yıl) ve amortisman sıklığını tanımlamanız gerekir. Daha fazla bilgi için bkz. [Amortisman profilleri ayarlama ve oluşturma](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Defterler

Amortisman profillerini ayarladıktan sonra kıymetleriniz için gerekli defterleri oluşturmanız gerekir. Her defter, bir kıymetin bağımsız mali yaşam döngüsünü izler. Defterler ilişkili hareketleri genel muhasebeye nakletmek için yapılandırılabilir. Bu yapılandırma varsayılan ayardır çünkü genellikle kurumsal mali raporlama için kullanılır. Genel muhasebeye nakledilmeyen defterler yalnızca Sabit kıymete nakledilir ve genel olarak vergi raporlama amacıyla kullanılır.

Her deftere bir birincil amortisman profili atanır. Bu tür bir profil uygulanabilirse defterlerde ayrıca bir alternatif veya değişim amortismanı profili de bulunur. Sabit kıymet defterini amortisman işlemlerine otomatik olarak eklemek için **Amortismanı hesapla** seçeneğini etkinleştirmelisiniz. Kıymet için bu seçenek etkinleştirilmemişse amortisman teklifi, kıymeti atlar.

Ayrıca türetilmiş defterleri de ayarlayabilirsiniz. Belirtilen türetilmiş hareketler, temel hareketin türetilmiş defterlere karşı tam bir kopyası olarak nakledilir. Bu nedenle, türetilmiş hareketler amortisman hareketleri için değil, genel olarak alımlar ve elden çıkarmalar için ayarlanır. Daha fazla bilgi için bkz. [Defterleri ayarlama](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Sabit kıymet deftere nakil profilleri

Defterleri ayarladıktan sonra deftere nakil profilini oluşturabilirsiniz. Deftere nakil profili, defter tarafından tanımlanmalıdır ancak daha ayrıntılı bir düzeyde de tanımlanabilir. Örneğin, bir defter birleşimi ve bir sabit kıymet grubu veya tek bir sabit kıymet defteri için deftere nakil profili tanımlayabilirsiniz. Varsayılan olarak, tanımlanan genel muhasebe hesapları sabit kıymet hareketleri için kullanılır.

Elden çıkarma işlemleri (elden çıkarma satışları ve hurdaları elden çıkarma) sırasında kullanılacak genel muhasebe hesaplarını tanımlamanız gerekir. Elden çıkarma sırasında, daha önce deftere nakledilen sabit kıymet hareketleri orijinal hesaplardan tersine çevrilir. Bu durumda net tutarlar, kıymet elden çıkarma için uyun kazanç ve kayıp hesabına taşınır. Hareketlerin doğru bir şekilde tersine çevrilmesine yardımcı olması için işinizde kullandığınız her hareket türü için hesapları ayarlamanız gerekir. Ana hesap, bu hareket türü için deftere nakil profilinde ayarladığınız orijinal hesap olmalıdır ve mahsup hesap, elden çıkarma hesabının karı ve zararı olmalıdır. Net defter değeri istisnadır. Bu durumda, hem ana hesap hem de mahsup hesap elden çıkarma hesabının karı ve zararı olarak ayarlanmalıdır. Daha fazla bilgi için bkz. [Sabit kıymet deftere nakil profilleri ayarlama](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Sabit kıymet grupları

**Sabit kıymet grubu** alanı bir sabit kıymet oluşturduğunuzda gerekli olan tek alandır. Bu alanın değeri, kıymet için çeşitli bilgi alanlarının varsayılan değerini belirler. Defterler, grup içindeki her kıymete bir varsayılan defter atanacak şekilde ayarlanır. Bu şekilde, defterler için ayarladığınız öznitelikler bir kıymet grubuna özel olabilir. Bu öznitelikler servis ömrünü ve amortisman yöntemini içerir.

Ayrıca bir sabit kıymet grubu ve defterin belirli bir birleşimi için özel amortisman payları veya ek amortisman da tanımlayabilirsiniz. Deftere birden fazla pay atandığında hesaplanan payların sırasını belirtmek için özel amortisman payına öncelik atamanız gerekir. Daha fazla bilgi için bkz. [Sabit kıymet grupları ayarlama](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Günlük adları

**Günlük adları** sayfasında, Sabit kıymetler günlüğüyle birlikte kullanılması gereken günlük adlarını oluşturmanız gerekir. **Günlük türü** alanını **Sabit kıymetleri naklet** olarak ayarlamanız gerekir. **Fiş serisi** alanını günlük adları Sabit kıymetler günlüğü için kullanılacak şekilde ayarlayın. Sabit kıymet günlükleri **Yalnızca bir fiş numarası** ayarını kullanmamalıdır; çünkü transferler ve bölmeler gibi birçok otomatik işlem için benzersiz bir fiş numarası gerekir.

## <a name="fixed-asset-parameters"></a>Sabit kıymet parametreleri

Son adım, sabit kıymet parametrelerini güncelleştirmektir.

**Aktifleştirme eşiği** alanı amorti edilmiş kıymetleri belirler. Satınalma satırı bir sabit kıymet olarak seçilirse ancak belirtilen aktifleştirme eşiğini karşılamazsa yine de bir sabit kıymet oluşturulur veya güncelleştirilir ancak **Amortismanı hesapla** seçeneği **Hayır** olarak ayarlanır. Bu nedenle, amortisman tekliflerinin bir parçası olarak kıymet otomatik olarak amorti edilmez.

Bir önemli seçenek de **Elden çıkarmayı içeren amortisman düzeltme tutarlarını otomatik olarak oluştur** seçeneğidir. Bu seçeneği **Evet** olarak ayarladığınızda kıymet amortismanı, kıymeti elden çıkarma zamanındaki amortisman ayarlarına göre otomatik olarak ayarlanır. Başka bir seçenek, bir satıcı faturası kullanarak sabit kıymetleri aldığınızda nakit iskontoları alım tutarınızdan düşmenizi sağlar.

Kıymetlerin satınalma işleminin parçası olarak nasıl oluşturulacağını **Satınalma siparişleri** Hızlı Sekmesinde yapılandırabilirsiniz. İlk seçenek, **Satınalmadan kıymet alımına izin ver** olarak adlandırılır. Bu seçeneği **Evet** olarak ayarlarsanız fatura deftere nakledildiğinde kıymet alımı gerçekleşir. Bu seçeneği **Hayır** olarak ayarlarsanız bir satın alma siparişi (PO) ve fatura üzerine hala bir sabit kıymet yerleştirebilirsiniz ancak alım deftere nakledilmez. Deftere nakletme, Sabit kıymet günlüğünden ayrı bir adım olarak yapılmalıdır. **Ürün girişi veya fatura deftere nakli sırasında kıymet oluştur** seçeneği deftere nakil sırasında "hemen" yeni bir kıymet oluşturmanıza olanak tanır. Bu nedenle, kıymetin hareketten önce sabit kıymet olarak ayarlanması gerekmez. Son seçenek olan **Satır girişi sırasında sabit kıymetler oluşturmayı denetle**, yalnızca satınalma talepleri için geçerlidir.

Sabit kıymette yapılacak değişiklikler veya belirli sabit kıymet hareketleri için gerekli olacak şekilde neden kodlarını yapılandırılabilirsiniz.

Son olarak, sabit kıymetler için numara serilerini **Numara serileri** sekmesinde tanımlarsınız. **Sabit kıymet** numarası sırası, belirtilmişse **Sabit kıymet grup** numarası sırası tarafından geçersiz kılınır.

Daha fazla bilgi için bkz. [Sabit kıymet oluşturma](tasks/create-fixed-asset.md).
