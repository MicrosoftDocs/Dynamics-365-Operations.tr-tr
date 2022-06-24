---
title: İndirim yönetimi modülüne genel bakış
description: Bu makale Microsoft Dynamics 365 Supply Chain Management indirim yönetim modülü hakkında bir genel bakış sağlar.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cfba391536559ed3a967d0aafe2e352486777dda
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873651"
---
# <a name="rebate-management-module-overview"></a>İndirim yönetimi modülüne genel bakış

[!include [banner](../includes/banner.md)]

İndirim, kesintiler ve kâr paylarını hesaplayabilmek için işiniz ve müşterileriniz ya da satıcılarınız arasında kontratlar, anlaşmalar veya sözleşmeler oluşturmak için **indirim yönetimi** modülünü kullanabilirsiniz. İndirim yönetimi, indirim ve kesinti işlemlerini kullanıcıların etkili şekilde oluşturabilecekleri, gözden geçirecekleri ve işleyebilecekleri merkezi bir konumda izler ve korur.

İndirim yönetimi, *indirimleri* oluşturmayı, bakımını yapmayı ve işlemeyi destekler. İndirim, bir satıcı veya bir alıcı tarafından satın alma fiyatının bir kısmının geri döndürülmesidir. İndirimler genellikle belirli bir dönem içinde belirli bir miktar veya mal değerinin satın alınmasına dayanır. İskontolardan farklı olarak, satın alma tutarı tam olarak faturalandıktan sonra gerçekleştirilir.

İndirim yönetimi *kesintileri* de destekler. Kesinti; marka, telif hakkı veya patent gibi fikri mülkiyeti kullanma lisansı ya da ayrıcalığı veya avcılık veya araştırma gibi amaçlarla doğal bir kaynağı kullanma ayrıcalığı için ödenen tazminat, bir değerlendirme veya ücrettir. Kesintiler genellikle, gerçekleşen kullanım için gelir veya kâr yüzdesi olarak hesaplanır. fikri mülkiyet veya doğal kaynak ne kadar çok kullanılırsa gerçekleşen kesinti o kadar yüksek olur.

Ek olarak, indirim Yönetimi Müşteri *kâr paylarını* destekler. Kâr payları, bir tarafın bir varlığı kullanım hakkı için lisans sahibine ya da Franchise verilen tarafa yaptığı ödemelerdir.

İndirim yönetimi, provizyonlar, indirimler ve gider yazma için deftere nakil profillerini tanımlamanızı sağlar. Ayrıca, deftere nakiller belirli bir müşteri veya satıcı için tanımlanabilir. Bu şekilde, tüm müşteri veya satıcı senaryoları için geçerli olmayan anlaşmalar deftere nakil yoluyla izlenebilir.

Toplu işlemlerde seçilen ve planlanan hesaplama yöntemine göre, indirim hareketleri otomatik olarak oluşturulur. Ek olarak, anlaşmaları yönetmek, gözden geçirmek ve onaylamak için iş akışları ayarlayabilirsiniz.

## <a name="basis-calculation"></a>Temel hesaplama

Müşteri indirimleri, müşteri kâr payları ve satıcı indirimleri, iş gereksinimlerinize bağlı olarak farklı bir temel kullanabilir:

- Müşteri indirimleri, satış siparişlerini, teslimat notlarını veya faturaları temel alabilir.
- Müşteri kâr payları satış siparişlerini, teslimat notlarını veya ödenen faturaları temel alabilir.
- Satıcı indirimleri, satın alma siparişlerini veya satış siparişlerini temel alabilir. Bunlar, indirim satıcısından satın alınan ve satış faturalarıyla müşterilere satılan ürünlere göre hesaplanabilir.

## <a name="flexible-calculations"></a>Esnek hesaplamalar

İndirim hesaplama dönemleri hem müşteri anlaşmaları hem de satıcı anlaşmaları için kullanılabilir. Bir hesaplama dönemi, anlaşma uzunluğunu, hesaplama sıklığını ve hesaplama dönemini tanımlar. İndirimler, indirim dönemi sırasında satış siparişi miktarları veya niteliği onaylı ürünlerin tutarları temel alınarak tahakkuk edilebilir.

Her anlaşma hesaplaması için, aşağıdaki dönemlerin herhangi biri ayarlanabilir:

- Fatura
- Gün
- Hafta
- Ay
- Üç aylık dönem
- Yıl
- Özelleştirilmiş dönem
- Önceden listelenmiş olan dönemlerden herhangi birinin katı

Bu hesaplama bağımsız müşterilere ve ürünlere, müşteri ve ürün gruplarına veya tüm müşteriler ve ürünlere uygulanabilir. Birden çok ayrıntı satırı olan indirimler farklı belirleyici tarih aralıklarına sahip olabilir. Provizyon ve talep süreleri farklı olabilir. Örneğin, provizyonlar her gün işlenebilir, talepler ise ayda bir işlenir.

İndirimler birçok farklı parametreye göre konfigüre edilebilir. Örneğin, bir yüzde, bir oran veya sabit bir tutar olarak konfigüre edilebilir. Dört ana hesaplama yöntemi vardır:

- Adımlı
- Birikmeli
- Hareketli
- Toplam değer

İndirim hesaplama sonuçları, indirimin net tutara göre hesaplama için ayarlanıp ayarlanmadığına bağlı olarak diğer indirimler tarafından da azaltılabilir.

Satıcı tarafında, satış siparişini temel alan indirimler ilk giren ilk çıkar (FIFO) kuralını, en son satın alma fiyatını, ortalama satın alma fiyatını veya satış fiyatını temel alarak fiyatı hesaplayabilir.

## <a name="rebate-target-transactions"></a>İndirim hedef hareketleri

İndirim anlaşması veya sözleşmesinin ürettiği çıktılar mali veya maddeler olabilir.

Mali çıkışlar, deftere nakil profilinden anlaşmaya atanan ödeme tipine göre belirlenir. Bu çıkışlar müşteri kesintisi günlüklerini, serbest metin faturalarını ve satıcı faturalarını içerebilir. Denetleme amacıyla, finansal indirim hedef hareketleri, kaynak indirim anlaşmasına bir referans içerir.

Madde çıkışları, Müşteri indirimleri için ücretsiz madde satış siparişi ve satıcı indirimleri için bir satın alma siparişi oluşturur. Madde indirim hedef işlemleri serbest madde satış siparişi veya satın alma siparişinde hangi indirim başvurusunun girilmesi gerektiğini belirleyen seçenekler içerir.

## <a name="accurate-rebate-calculations"></a>Doğru indirim hesaplamaları

İlişkili anlaşmalar, hesaplamaların sıklığı, hesaplama esası ve seçilen hesaplama yöntemi birleşimi, indirim hesaplamalarının doğruluğunu ve kesinliğini belirler. İndirim provizyonları, deftere nakledilen ve talep edilen değerleri tahakkuk ettirmek için kullanılabilir.

Provizyonlar günlük, haftalık, aylık olarak veya özel bir döneme göre yönetilebilir. Ancak, bu işlev indirimi tahsis edebilir veya ödeyebilir veya sağlama sıklığından daha uzun veya aynı uzunluktaki tanımlanan sıklıkta ödemesini alabilir. Silme indirim ile aynı sıklığı kullanır. Kullanıcılar, ödeme sırasında herhangi bir zamanda bir planı veya ödeme tutarlarını kolayca ayarlayabilir.

Kullanıcıların artık iki adımda yapılan anlaşmaları veya provizyonlarını işlemesi gerekmez. Provizyonlar ve gider yazmalar doğrudan kayıt defterine nakledilir. Ayrıca, alacak dekontları otomatik olarak oluşturulabilir. Bu nedenle, borç hesapları ve alacak hesapları ile tam bütünleşme vardır. İşlem sırasında, hesaplamalar hesap ve değerlerin doğru hesaplanmasını sağlamak için kapatma iskontolarını, ücretli faturaları, ticari indirimleri ve varolan borç dekontlarını dikkate alır.

İndirimler hesaplanırken, işlem deftere nakil gerçekleşmeden önce gözden geçirilebilecek işlemler oluşturur. Ayrı bir işlem, indirim ve yönetim hareketlerini deftere nakleder. Daha sonra teklif edilen hareketlere nakil sırasında bir günlük, alacak dekontu veya borç hareketi oluşturulabilir. Uyumluluk, verimlilik ve saydamlık sağlamak için raporlama beyanları ve işlem listeleri elde edilebilir.

## <a name="guaranteed-royalty-payments"></a>Garantili kâr payı ödemeleri

İndirim yönetiminde, otomatik ödeme oluşturma, garantili minimumlar geçerli olsa bile, kâr paylarını hızlı ve kolay bir şekilde ele almanıza olanak tanır.

## <a name="maximizing-spend-versus-rebates"></a>Harcama - indirim oranını en yüksek düzeye çıkarma

Satıcılar ve ürünler bölgelere göre gruplanabilir ve işlemin ülkesine veya bölgesine göre farklı teklifler sağlanabilir. Kullanıcılar ürün seçerken dahil edilen maddeleri ve indirim kapanışında kullanılacak madde sayısını tanımlayabilirler.
