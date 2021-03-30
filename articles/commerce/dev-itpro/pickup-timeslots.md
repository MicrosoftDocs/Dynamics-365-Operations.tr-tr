---
title: Müşteri malzeme çekme için zaman aralıkları oluşturma ve güncelleştirme
description: Bu konu, Commerce Headquarters'ta müşteri teslim alma dilimlerini oluşturmayı, yapılandırmayı ve güncelleştirmeyi açıklar.
author: anupamar-ms
manager: AnnBe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: 6dc2be8a6f62ce13068ce2242f92ef17830c2447
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205759"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Müşteri malzeme çekme için zaman aralıkları oluşturma ve güncelleştirme

[!include [banner](../../includes/banner.md)]

Bu konu, Commerce Headquarters'ta müşteri teslim alma dilimlerini oluşturmayı, yapılandırmayı ve güncelleştirmeyi açıklar.

Zaman dilimi özelliği, perakendecilere, müşteri malzeme çekme teslim modunun açık olduğu maddeler için bir zaman dilimi tanımlama yolu sunar. Zaman yuvaları, perakendeciler siparişlerin bir mağazadan çekileceği gün ve saatleri tanımlamasına olanak tanır. Perakendeciler, belirli bir dönemde çekilebilecek sipariş sayısını da tanımlayabilir. Böylece perakendeciler, belirli bir tarihte ve belirli bir zamanda çekilebilecek sipariş sayısını sınırlayabilir. Sonuç, müşterilerine daha iyi kalitede bir deneyimdir.

> [!NOTE]
> Zaman dilimi özelliği Microsoft Dynamics 365 Commerce Sürüm 10.0.15 ve sonrasında kullanılabilir.

Aşağıdaki çizimde e-ticaret teslim alma sırasında zaman dilimi seçimine ilişkin bir örnek gösterilmektedir.

![E-ticaret kullanıma alma sırasında zaman aralığı seçimi örneği](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Zaman dilimi özellikleri

Bir müşteri belirli bir mağaza veya konumdan sipariş çekmeyi seçebiltiğinde, zaman dilimi belirli bir aralıktır. Zaman dilimi yönetimi özelliği yalnızca, müşteri malzeme çekme teslimat modu Dynamics 365 Commerce'de yapılandırıldığında kullanılabilir .

Zaman aralığı aşağıdaki özellikler kullanılarak tanımlanır:

- **Teslimat şekli** – zaman diliminin uygulandığı teslim alma şeklini belirtin.
- **Minimum gün** ve **maksimum gün sayısı** – siparişin yerleştirildiği tarihle ilgili olarak malzeme çekme için seçilebilecek en erken ve en son tarihleri belirtin. 

    **Minimum günler** özelliği, satıcının Malzeme çekme için hazır olmadan önce siparişi işlemesi için yeterli zamanı olmasını sağlar. **Maksimum gün** özelliği, kullanıcının gelecekte çok uzak bir tarih seçmesini sağlar. Örneğin, minimum değer **1** olarak ayarlanmışsa ve 20 Eylül tarihinde bir sipariş yerleştirilirse, siparişin malzeme çekme için kullanılabileceği en erken gün bir sonraki uygun gün (21 Eylül) olur. Benzer şekilde, maksimum değer ayarlayarak bir siparişin çekilebileceği maksimum gün sayısını tanımlayabilirsiniz. Minimum ve maksimum değerler tanımlandığında, site kullanıcıları kullanıma alma deneyiminde yalnızca belirli gün kümesini görebilir ve seçebilir.

    Minimum değeri 1'den az olan bir ondalık değere ayarlayabilirsiniz. Örneğin, bir sipariş yerleştirildikten sonra malzeme çekme dört saat kullanılabilir ise, minimum değerini **0,17** (= 4 ÷ 24, en fazla iki ondalık basamağa yuvarlayarak) olarak ayarlayın. Ancak, minimum değerini 1'den fazla olan bir ondalık değere ayarlarsanız, her zaman en yakın tamsayıya yukarı yuvarlanır. Örneğin, **1,2** değeri **2**'ye kadar yuvarlanır. Benzer şekilde, maksimum değeri bir ondalık değere ayarlarsanız,her zaman en yakın tamsayıya yukarı yuvarlanır. 

- **Başlangıç tarihi** ve **Bitiş tarihi** – zaman diliminin başlangıç ve bitiş tarihlerini belirtin. Her zaman dilimi girişinin başlangıç ve bitiş tarihleri vardır. Bu nedenle, yıl boyunca farklı zaman yuvalarını ekleme esnekliği vardır (örneğin, tatil saatlerinde sözcüklups). Bir sipariş yerleştirildikten sonra bir zaman diliminin başlangıç ve tarihleri değiştirilirse, değişiklikler o sırada uygulanmaz. Başlangıç ve bitiş tarihlerini tanımladığınızda, kapanış tarihlerini (örneğin, Noel günü) dikkate almanız ve zaman aralıklarının bu günler için tanımlanmamasını sağlamalısınız.
- **Etkin Teslim Alma Saatleri** – Malzeme çekme işlemine izin verildiğinde dönemi belirtin. Örneğin, toplama zamanları her gün 14.00 - 17.00 arasında olabilir. Bu özellik, malzeme çekme saatlerinin mağaza saatlerinden bağımsız olmasını sağlar. Bu nedenle, perakende malzeme çekme sürelerini belirli iş gereksinimlerini karşılayacak şekilde konfigüre edebilir. Etkin malzeme çekme saatlerini tanımladığınızda, saatleri depolamayı dikkate almanız ve malzeme çekme sürelerinin, mağazanın kapatıldığı zamanlar için tanımlanmamasını sağlamalısınız.

    > [!NOTE]
    > Mağaza malzeme çekme saatlerinin uygun mağazanın saat diliminde tanımlanması gerekir.

- **Zaman dilimi aralığı** – Her zaman dilimine göre tahsis edilebilecek süreyi belirtin. Örneğin, her zaman diliminin süresi 15 dakika, 30 dakika veya bir saatten fazla olabilir. Zaman dilimi değeri 0 ise, saat dilimi başlangıç ve bitiş saatleri arasındaki sürenin tamamı için kullanılabilir.
- **Aralık başına yuvalar**: her zaman dilimi aralığında malzeme çekme için sunulabilecek müşteri veya sipariş sayısını belirtin. Örneğin **1**, **2**, **3** veya başka herhangi bir tamsayı girin.
- **Etkin günler** – Malzeme çekme zaman yuvalarının etkin olduğu haftanın günlerini belirtin. Bu özellik, perakende satış siparişinin malzeme çekme emirlerini desteklemek istediği günleri tanımlamasını sağlar.
- **Perakende satış kanalları** – Perakende kanallarını belirtin. Her zaman dilimi bir veya daha fazla perakende depolarıyla ilişkilendirilebilir. Her mağazanın operasyon saatlerine göre, bir veya daha fazla zaman dilimi girişi oluşturulabilir ve bir kanalla ilişkilendirilebilir. 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Kanal başına yalnızca bir zaman dilimi şablonu konfigüre edilebilir. Bu kanallar arasında gerçek mekan depoları, çağrı merkezleri, mobil aygıtlar ve e-ticaret siteleri sayılabilir.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Commerce Headquarters 'da zaman dilimi özelliğini konfigüre et

Satış noktası (POS) ve e-ticaret kanalları tarafından başvuruda bulunmak için Commerce Headquarters 'da her teslim alma modu için zaman aralıklarının tanımlanması gerekir.

- Her bir mağaza veya kanal ile yalnızca bir zaman dilimi şablonu ilişkilendirilebilir.
- Her şablondaki her bir teslim modu için oluşturulan her bir zaman diliminin benzersiz olması gerekir.
- Zaman dilimi özelliği yapılandırıldıktan sonra, zaman dilimi takvimi seçili mağazalar veya mağaza grupları tarafından kullanılabilir. Ayrıca, referans olarak POS'ta da görünür olacaktır.

Commerce Headquarters'da zaman dilimi özelliğini konfigüre etmek için aşağıdaki adımları izleyin.

1. **Commerce** \> **Kanal kurulum** \> **Mağazası malzeme çekme süresi** yuvasına gidin.
1. Yeni bir zaman dilimi şablonu oluşturmak için **Yeni**'yi seçin. Varolan bir şablonu kullanmak için, sol bölmedeki şablonu seçin.
1. **Zaman dilimi kimliği** ve **Açıklama** alanlarına değer girin.
1. **Sipariş toplama zamanı ayarları** hızlı sekmesinde, **Ekle**'yi seçin.
1. **Sipariş malzeme çekme zamanı ayarları** iletişim kutusunda Tarih aralığını, teslimat şeklini, etkin saatlerin, etkin günlerin, zaman dilimi aralığı, Aralık başına Yuva ve diğer ayarlar tanımlayın.

    Süre yuvaları öngörülebilir gelecekte duracağı takdirde, **Bitiş Tarihi** alanını **Asla** olarak ayarlayın.

    > [!NOTE]
    > Birden çok şablon oluşturabilirsiniz, ancak tek bir kanal veya depoyla yalnızca bir şablon ilişkilendirilebilir.

    ![Sipariş malzeme toplama zamanı ayarları iletişim kutusu](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Tamamladıktan sonra **Tamam**'ı seçin.
1. Bir günün zaman dilimlerinde değişiklik olursa, Tarih ve saatin çakışmadığından emin olmak için **sipariş toplama zamanı ayarları** hızlı sekmesinde ek girişler oluşturun.
1. **Perakende Kanalları** hızlı sekmesinde, zaman dilimi şablonunu kullanılacak mağazalar veya kanallarla ilişkilendirmek için **Ekle**'yi seçin.
1. **Kuruluş düğümlerini Seç** iletişim kutusunda, şablonun ilişkilendirilmesi gereken depoları, bölgeleri ve organizasyonları seçmek (veya seçimi temizlemek) için ok düğmelerini kullanın.

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Tamamladıktan sonra **Tamam**'ı seçin.
1. **Dağıtım zamanlaması** sayfasında, **1070** ve **1135** işlerini veriyi kanallara senkronize etmek için kullanın.

## <a name="time-slot-selection-for-pos-orders"></a>POS siparişleri için zaman dilimi seçimi

POS'ta, malzeme çekme için bir sipariş veya sipariş satırı tanımlandığında, kasiyer malzeme çekme deposunu veya konumunu ve bir tarih ve zaman dilimini seçebilir. Bir müşterinin farklı bir mağaza için bir malzeme çekme siparişi varsa, malzeme çekme bu mağazada kullanılabilir olduğunda, kasiyer program seçebilir. Mağaza arama, tarihlere ve depolama zamanlarında bir başvuru sağlayacaktır.

Aşağıdaki çizimde POS siparişi için zaman dilimi seçimine ilişkin bir örnek gösterilmektedir.

![Bir POS siparişi için zaman aralığı seçimi örneği](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>E-ticaret siparişleri için zaman dilimi seçimi

E-ticaret siparişleri için zaman dilimi seçimini nasıl kullanılabilir hale getirmek hakkında bilgi için, bkz [Teslim bilgileri modülü](../pickup-info-module.md).

> [!NOTE]
> Kullanıcılar, bir Commerce sitesinin kullanıma alma sayfasındaki malzeme çekme zamanı yuvalarını yalnızca bu sayfaya malzeme çekme bilgileri modülü eklenmişse görüntüleyebilir veya düzenleyebilir. Kullanıma alma sayfası malzeme alma bilgileri modülünü içermiyorsa kullanıcıların zaman dilimi bilgilerini belirtmesine veya görüntülemesine izin vermeden siparişler yerleştirilir.

Aşağıdaki çizimde, malzeme çekme zamanı yuvasının seçildiği bir e-ticaret siparişi örneği gösterilmektedir.

![Malzeme çekme zamanı yuvasının seçildiği bir e-ticaret siparişi örneği](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Çağrı merkezi siparişleri için saat dilimi seçimi

Çağrı merkezi uygulamasında çağrı merkezi temsilcileri, teslim alma mağazası veya konumunu, ayrıca aşağıdaki çizimde vurgulanan tarih ve saat dilimini seçebilir.

![Malzeme çekme zamanı yuvasının seçildiği bir çağrı merkezi siparişi örneği](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Malzeme çekme bilgileri modülü](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]