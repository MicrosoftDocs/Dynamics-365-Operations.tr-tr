---
title: Ödeme tabanlı iskontolar
description: Bu konu, perakendecilere belirli ödeme türleri için iskonto yapılandırma olanağı tanıyan işlevlere genel bir bakış sağlar.
author: bebeale
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 4be0c9a6f0a32016e07b8e31d0aaff44b4a29623
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416540"
---
# <a name="tender-based-discounts"></a>Ödeme tabanlı iskontolar

[!include [banner](includes/banner.md)]


Özel, markalı kredi kartları verme perakendeciler arasında genel bir uygulamadır. Perakendeciler için, bankalardan tercih edilen oranlar aldıklarından dolayı yararlıdır. Ek olarak, bu kredi kartları müşterilerin mağazayı daha sık ziyaret etmesini teşvik ettiğinden perakendecinin alt hattını geliştirmeye yardımcı olur. Bu nedenle, perakendeciler markalı kredi kartlarının müşteri tarafından kullanımını artırmak için bir teşvikte bulunur. Bu amaca ulaşmak için genellikle bu kredi kartlarını kullanan müşterilere ek indirimler sağlarlar.

Alternatif olarak, markalı kredi kartı sağlamayan perakendeciler müşterileri nakit, hediye kartları veya bağlılık programı puanları gibi diğer ödeme türlerini kullanarak ödeme yapmaya teşvik etmek isteyebilir. Bu şekilde kredi kartı işleme masraflarına ait giderleri azaltmaya yardımcı olabilirler. Bu nedenle, perakendeciler bu alternatif ödeme türlerini kullanan müşterilere indirimler sağlayabilir.

Microsoft Dynamics 365 Commerce'de perakendeciler, tercih edilen ödeme türünü kullanarak ödeme yapılması durumunda uygun satırlara uygulanan bir iskonto yüzdesi yapılandırabilir. Müşteri kısmi ödeme mi, tam ödeme mi yapacağınıza karar verebilir ve Commerce uygun iskonto tutarını saptar. İskontonun her zaman uygun maddelerin vergi öncesi tutarı üzerinde verildiğini unutmayın.

Ödeme tabanlı iskontolar periyodik veya el ile iskontolar gibi madde tabanlı iskontolarla rekabet etmez. Bunlar her zaman madde iskontolarının üzerinden uygulanır. Bu nedenle, bir maddeye özel bir periyodik iskonto uygulanmış olsa bile, ödeme tabanlı iskonto özel periyodik iskontonun üzerine uygulanır. Benzer şekilde, harekete bir eşik iskontosu uygulanması ve ödeme tabanlı iskontonun toplamı eşiğin altına düşürmesi durumunda bile eşik indirimi harekete uygulanır.

Ödeme tabanlı iskontolar hareketin alt toplamını azaltsa da, harekete uygulanan otomatik masraflar etkilenmez. Örneğin, alt toplam 100 ABD dolarından fazla olduğundan teslimat masrafları 5 ABD doları olarak hesaplanırsa ve ödeme tabanlı iskonto tutarı tutarı 100 ABD dolarının altına düşürürse, sipariş için teslimat ücreti yine de 5 ABD doları olur.


> [!NOTE]
> Ödeme tabanlı iskontolar uygun satış satırlarına orantılı olarak dağıtılır ve bireysel satırların vergi öncesi tutarını azaltır. Bir ödeme türü (örneğin, nakit) için birden fazla ödeme tabanlı iskonto yapılandırılırsa, yalnızca en iyi ödeme tabanlı iskonto uygulanır.

Ödeme tabanlı iskontolar yalnızca fiyatların kilitli olmadığı satış satırlarına uygulanabilir. Bir siparişe yeni satış satırları eklenirse, ödeme tabanlı iskonto ödeme sırasında yalnızca yeni satış satırlarına uygulanır. Malzeme çekme veya sevkiyat için bir müşteri siparişi yerleştirildiğinde, ödeme tabanlı iskonto yalnızca depozito tutarına uygulanır. Sipariş yerleştirildikten sonra, sipariş karşılama sırasında satış satırlarının fiyatları kilitlenir. Bu nedenle, malzeme çekme sırasında ödenen veya sevkiyat sırasında onaylanan bakiyeye herhangi bir ödeme tabanlı iskonto uygulanmaz. Ödeme tabanlı iskonto, yalnızca sipariş alındığında perakendeci tüm tutarı depozito olarak tahsil ederse müşteri siparişi tutarının tamamına uygulanabilir.

> [!IMPORTANT]
> Commerce'de, ödeme tabanlı iskontolar şu anda iki ödeme türü ile sınırlıdır: kredi kartları ve nakit.

## <a name="pos-user-experience"></a>POS kullanıcı deneyimi

Ödeme tabanlı iskonto nakit olarak ayarlanmışsa ve satış noktasındaki kasiyer (POS) Nakit ödeme işlemiyle eşlenen bir düğmeyi seçerse, ödeme tabanlı iskonto harekete otomatik olarak uygulanır. Azaltılan tutar daha sonra bakiye olarak görüntülenir. Ancak, kasiyer ödeme ekranında **Geri** düğmesini seçerse, iskonto kaldırılır ve hareket ekranında orijinal tutar gösterilir. Ödeme satırı hükümsüz kılınırsa, ödeme tabanlı iskonto kaldırılır.

Kart ödemeleri için, perakendeciler bir veya daha fazla kredi kartı türünde ödeme tabanlı iskontoyu ayarlayabilir. Ancak, sistem kart yetkilendirilmediği sürece kullanılan kredi kartı türünü doğrulayamaz. İskonto yetkilendirmeden sonra uygulanırsa, ödeme onayı daha büyük bir tutar için olacaktır, ancak ödeme yakalama daha küçük bir tutar için gerçekleşecektir.

Bu durumu engellemeye yardımcı olmak için, bir müşteri kredi kartıyla ödeme yaptığı takdirde, kasiyer müşteriye ek tasarruf sağlayacak kredi kartlarını listeleyen bir iletişim kutusu görür. Böylece kasiyer, müşterinin ek indirim elde etmek için tercih edilen kartlardan birini kullanmak isteyip istemediğini sorabilir. Kasiyer tercih edilen bir kartı kullanırsa, ödeme tabanlı iskonto harekete uygulanır ve azaltılan tutar ödeme ekranında gösterilir. Onay, düşürülen tutar için olacaktır. Müşteri, kasiyerin seçtiği karttan farklı bir kart takarsa, bir hata iletisi gösterilir ve yetkilendirme geçersiz kılınır.


## <a name="call-center-user-experience"></a>Çağrı merkezi kullanıcı deneyimi

Kullanıcı bir açağrı merkezi sırasında **Tamamla**'yı seçerse **Toplamlar** ekranı gösterilir. Önce, ödeme yöntemi henüz seçilmediğinden bu ekrandaki toplamlar ödeme tabanlı iskontoları içermez. **Ödeme ekle** ekranında, kullanıcı ödeme tabanlı iskontonun yapılandırıldığı ödeme yöntemini seçerse, ödeme tutarı indirimli tutarı yansıtacak şekilde otomatik olarak ayarlanacaktır. POS'taki müşteri gibi, çağrı merkezi müşterisi de tam ödeme mi, yoksa kısmi ödeme mi yapacağına karar verebilir. Ödenen tutara dayalı olarak, ödeme tabanlı iskonto satış siparişine uygulanır.

> [!NOTE]
> Çağrı merkezi siparişleri için kart doğrulaması yapılmaz. Örneğin, çağrı merkezi kullanıcısı kredi kartı olarak Visa seçerse ancak müşteri Mastercard kullanırsa, sistem indirimi yine de uygular.

## <a name="exclude-items-from-discounts"></a>Maddeleri iskontolar dışında tutma

Perakendeciler, yeni maddeler veya talep edilen maddeler gibi bazı ürünleri iskontolar dışında tutmayı seçer. Ancak, yine de, ödeme tabanlı iskontolar uygulamak isteyebilir. Örneğin, bir perakendeci Commerce'i madde tabanlı iskontolara veya el ile iskontolara izin vermeyecek şekilde yapılandırabilir. Ancak, müşteri tercih edilen ödemeyi kullanarak ödeme yaparsa, Commerce ödeme tabanlı iskontoyu uygular. Commerce'i bu şekilde ayarlamak için perakendecilerin **Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gitmesi, maddeyi seçmesi ve ardından **Commerce** hızlı sekmesinde **Tüm iskontoları engelle** ve **Ödeme tabanlı iskontoları engelle** seçeneklerini **Hayır** olarak ve **İskontolarını engelle** ve **El ile iskontoları engelle** seçeneklerini **Evet** olarak ayarlaması gerekir.

> [!NOTE]
> **Tüm iskontoları engelle** yapılandırması **Evet** olarak ayarlandığında ürüne iskonto uygulanmaz. Ödeme tabanlı iskontolar bile uygulanmayacaktır.
