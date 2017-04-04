---
title: "Sabit Kıymetleri Ayarlama"
description: "Bu konu, Sabit kıymetler modülünün kurulumu hakkında genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: dde8053df96d03c8c8e52fa6d2fdf7f74e95ec92
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fixed-assets"></a>Sabit Kıymetleri Ayarlama

Bu konu, Sabit kıymetler modülünün kurulumu hakkında genel bir bakış sağlar.

<a name="overview"></a>Özet
--------
Parametreler, Sabit kıymetler içindeki genel davranışı kontrol eder.

Sabit kıymet grupları, kıymetlerinizi gruplamanızı ve bir gruba atanan her kıymet için varsayılan öznitelikleri belirtmenizi sağlar. Defterler, sabit kıymet gruplarına atanır. Defterler, amortisman profilinde tanımlanan amortisman yapılandırmasını kullanarak bir sabit kıymetin zaman içindeki mali değerini izler.

Sabit kıymetler oluşturulduklarında bir gruba atanır. Varsayılan olarak, sabit kıymet grubuna atanan defterler ardından sabit kıymete atanır. Genel muhasebeye nakledilmek üzere yapılandırılan defterler deftere nakil profiliyle ilişkilendirilir. Genel muhasebe hesapları, deftere nakil profilinde her defter için tanımlanır ve sabit kıymet hareketleri deftere nakledildiğinde kullanılır. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Amortisman profilleri
Öncelikle amortisman profillerini oluşturulmanız gerekir. Amortisman profilinde bir kıymetin değerinin zaman içinde nasıl amorti edildiğini yapılandırırsınız. Amortisman yöntemini, amortisman yılını (takvim yılı veya mali yıl) ve amortisman sıklığını tanımlamanız gerekir.

## <a name="books"></a>Defterler
Amortisman profillerini ayarladıktan sonra kıymetleriniz için gerekli defterleri oluşturmanız gerekir. Her defter, bir kıymetin bağımsız mali yaşam döngüsünü izler. Defterler ilişkili hareketleri genel muhasebeye nakletmek için yapılandırılabilir. Bu yapılandırma varsayılan ayar, çünkü genellikle şirket mali raporlama için kullanılır. Genel muhasebeye nakletmek olmayan kitaplar yalnızca sabit kıymet muavin defteri deftere nakletmek ve genellikle vergi raporlama amaçları için kullanılır.

Her deftere bir birincil amortisman profili atanır. Bu tür bir profil uygulanabilirse defterlerde ayrıca bir alternatif veya değişim amortismanı profili de bulunur. Sabit kıymet defterini amortisman işlemlerine otomatik olarak eklemek için Amortismanı hesapla seçeneğini etkinleştirmelisiniz. Bir kıymet için bu seçenek seçili değilse, kıymet amortisman teklifi atlar.

Ayrıca türetilmiş defterleri de ayarlayabilirsiniz. Belirtilen türetilmiş hareketler, temel hareketin türetilmiş defterlere karşı tam bir kopyası olarak nakledilir. Bu nedenle, türetilmiş hareketler amortisman hareketleri için değil, genel olarak alımlar ve elden çıkarmalar için ayarlanır.

## <a name="fixed-asset-posting-profiles"></a>Sabit kıymet deftere nakil profilleri
Defterleri ayarladıktan sonra deftere nakil profilini oluşturabilirsiniz. Deftere nakil profili, defter tarafından tanımlanmalıdır ancak daha ayrıntılı bir düzeyde de tanımlanabilir. Örneğin, bir defter birleşimi ve bir sabit kıymet grubu veya tek bir sabit kıymet defteri için deftere nakil profili tanımlayabilirsiniz. Varsayılan olarak, tanımlanan genel muhasebe hesapları sabit kıymet hareketleri için kullanılır.

Elden çıkarma işlemleri (elden çıkarma satışları ve hurdaları elden çıkarma) sırasında kullanılacak genel muhasebe hesaplarını tanımlamanız gerekir. Elden çıkarma zamanında, önceden nakledilen sabit kıymet hareketleri, orijinal hesaplardan tersine çevrilir ve net tutar, kıymetin elden çıkarılması için ilgili kar ve zarar hesabına aktarılır. Hareketlerin doğru bir şekilde tersine çevrilmesine yardımcı olması için işinizde kullandığınız her hareket türü için hesapları ayarlamanız gerekir. Ana hesap, bu hareket türü için deftere nakil profilinde ayarladığınız orijinal hesap olmalıdır ve mahsup hesap, elden çıkarma hesabının karı ve zararı olmalıdır. Net defter değeri istisnadır. Bu durumda, hem ana hesap hem de mahsup hesap elden çıkarma hesabının karı ve zararı olarak ayarlanmalıdır.

## <a name="fixed-asset-groups"></a>Sabit kıymet grupları
Sabit kıymet grubu bir sabit kıymet oluşturduğunuzda gerekli olan tek alandır. Bu alanın değeri, kıymet için çeşitli bilgi alanlarının varsayılan değerini belirler. Defterler, grup içindeki her kıymete bir varsayılan defter atanacak şekilde ayarlanır. Ardından Servis ömrü ve Amortisman yöntemi gibi bir kıymet grubuna özgü defterler için öznitelikler ayarlayabilirsiniz.

Ayrıca bir sabit kıymet grubu ve defterin belirli bir birleşimi için özel amortisman payları veya ek amortisman da tanımlayabilirsiniz. Deftere birden fazla pay atandığında hesaplanan payların sırasını belirtmek için özel amortisman payına öncelik atamanız gerekir.

## <a name="fixed-asset-parameters"></a>Sabit kıymet parametreleri
Son adım, sabit kıymet parametrelerini güncelleştirmektir.

Aktifleştirme eşiği alanı amorti edilmiş kıymetleri belirler. Bir sabit kıymet bir satınalma satırı seçilir, ancak belirtilen Aktifleştirme eşiği karşılamıyor, sabit kıymet hala oluşturulduğunda veya güncelleştirildiğinde, ancak Amortisman Hesapla seçeneği Hayır olarak ayarlanır. Bu nedenle, kıymet amortisman tekliflerinin bir parçası olarak otomatik olarak amorti olmaz.

Bir önemli seçenek de Elden çıkarmayı içeren amortisman düzeltme tutarlarını otomatik olarak oluştur seçeneğidir. Bu seçeneği Evet olarak ayarladığınızda kıymet amortismanı, kıymeti elden çıkarma zamanındaki amortisman ayarlarına göre otomatik olarak ayarlanır. Başka bir seçenek, bir satıcı faturası kullanarak sabit kıymetleri aldığınızda nakit iskontoları alım tutarınızdan düşmenizi sağlar.

Kıymetlerin satınalma işleminin parçası olarak nasıl oluşturulacağını Satınalma siparişleri Hızlı Sekmesinde yapılandırabilirsiniz. İlk seçenek, Satınalmadan kıymet alımına izin ver seçeneğidir. Bu seçeneği Evet olarak ayarlarsanız fatura deftere nakledildiğinde kıymet alımı gerçekleşir. Bu seçenek Hayır olarak ayarlarsanız, bir satınalma siparişi (PO) ve fatura yine sabit kıymet koyabilirsiniz, ancak alım deftere olmaz. Deftere nakletme, sabit kıymet günlüğünden ayrı bir adım olarak yapılmalıdır. Hareket önce bir sabit kıymet olarak ayarlanması gerekmez böylece oluşturma kıymet ürün alış irsaliyesi veya fatura deftere nakil sırasında deftere nakil sırasında ekranda"" yeni kıymet oluşturmanızı sağlar. Son seçenek olan Satır girişi sırasında sabit kıymetler oluşturmayı denetle, yalnızca satınalma talepleri için geçerlidir.

Sabit kıymette yapılacak değişiklikler veya belirli sabit kıymet hareketleri için gerekli olacak şekilde neden kodlarını yapılandırılabilirsiniz.

Son olarak, Sabit kıymetler için numara serilerini Numara serileri sekmesinde tanımlarsınız. Sabit kıymet numarası sırası, belirtilmişse Sabit kıymet grup numarası sırasını geçersiz kılar.


