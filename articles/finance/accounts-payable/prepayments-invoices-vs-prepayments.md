---
title: Ön ödeme faturaları ve ön ödemeler karşılaştırması
description: Bu konuda kuruluşların peşin ödemeler (ön ödemeler) için kullanabileceği iki yöntem açıklanmış ve karşılaştırılmıştır.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f05f1d8d2a1fb454f3f227d2cc8138f2b779ff87
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716339"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Peşinat faturaları ve ön ödemeler karşılaştırması

[!include [banner](../includes/banner.md)]

Bu konuda kuruluşların peşin ödemeler (ön ödemeler) için kullanabileceği iki yöntem açıklanmış ve karşılaştırılmıştır. Bir yöntemde bir satın alma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturulur. Diğer yöntemde ise günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturulur.

Kuruluşlar, satıcılara mal veya hizmetleri için bu mal veya hizmetler karşılanmadan önce ön ödeme (avans ödeme) yapabilirler. Satıcılara ön ödeme yapmak için iki yöntem kullanılabilir. Riski en aza indirmek için, bir satınalma emrine ön ödeme tanımlayarak ön ödemeleri izleyebilirsiniz. Bu yöntem için satınalma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturmanız gerekir. Bu yöntem ön ödeme faturalandırması olarak adlandırılır. Ön ödemeleri yakında takip etmek istemeyen veya satıcılarından ön ödeme faturası almayan kuruluşlar, ön ödeme faturalandırması yöntemi yerine ön ödeme günlüğü fişleri kullanabilirler. Günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturabilirsiniz. Bu yöntemde, bir satıcıya hangi ön ödemelerin hangi satınalma emirlerine karşı yapıldığını takip edemezsiniz. Ancak, deftere nakledilen bir ön ödemeyi bir satınalma emrine karşı kapatma olarak işaretleyebilirsiniz.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Ön ödeme faturalandırması - ön ödemeler ne zaman kullanılır

| Ön ödeme faturalandırması                                                                | Ön ödemeler                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Satınalma emrine bir ön ödeme değeri tanımlayın.                                    | Satınalma emrine hiçbir ön ödeme değeri tanımlanmamıştır.                    |
| Ön ödeme faturası ve nihai fatura deftere nakledilmelidir.                       | Deftere hiçbir ön ödeme faturası nakledilmemelidir.                                    |
| Ön ödeme yükümlülüğü ön ödeme hesabında tutulur, AP hesabında değil. | Ön ödeme yükümlülüğü AP hesabında tutulur.                  |
| Satıcı bakiyesi ön ödeme değerini işlem boyunca yansıtmaz.     | Satıcı bakiyesi ön ödeme değerini işlem boyunca yansıtır. |
| Ön ödeme faturalandırması yalnızca Borç hesaplarında kullanılabilir.                         | Ön ödemeler Borç hesabında ve Alacak hesaplarında kullanılabilir.    |

## <a name="overview-of-the-prepayment-process"></a>Ön ödeme işlemine genel bakış
Birçok ülke/bölgedeki muhasebe uygulamaları, bir müşteriden veya satıcıdan gelen peşinatların müşteri veya satıcı için normal özet hesaplara nakledilmemesini gerektirir. Bunun yerine, bu ön ödemeler, ön ödemeler için olan özel genel muhasebe hesaplarına nakledilir. Bir satış siparişi veya satın alma siparişi oluşturulduğunda, müşteriye bir fatura düzenler veya satıcıdan alınır. Fatura ödenirken, ön ödeme genel muhasebe hesaplarındaki ön ödeme ve satış vergisi ön ödemesi fişi ters çevrilir ve fatura tutarları otomatik olarak genel özet hesaplarına nakledilir. Bir ön ödeme oluşturmak için şu adımları izleyin.

1.  Ön ödemeler için deftere nakil profilleri ayarlayın.
2.  Alacak hesapları parametreleri Borç hesapları parametrelerinde, **Genel muhasebe ve satış vergisi** altında, **Ön ödemeli ödeme günlüğü için deftere nakil profili** parametresini kullanarak yeni deftere nakil profilini seçin.
3.  Bir ödeme günlüğü oluşturun ve sonra yeni ödemeyi oluşturun.
4.  Ödemeyi ön ödeme olarak işaretleyebilirsiniz. Bir ödeme peşinat olarak işaretlenirse ödeme, 1 ve 2. adımlarda ayarladığınız deftere nakil profilinde tanımlı genel muhasebe hesaplarına nakledilir. Ek olarak, ödeme ön ödeme olarak işaretlenmişse, vergiler de hesaplanır. Bazı hükümetler, fatura olmasa ön ödeme kaydedildiğinde vergilerin ödenmesini gerektirir.
5.  Ön ödemeyi nakledin.
6.  İsteğe bağlı: Faturayı oluşturmadan önce ön ödemeleri satın alma siparişi veya satış siparişi karşılığında kapatabilirsiniz. Satış siparişi veya satın alma siparişi sayfasında, Eylem Bölmesi'nde **Hareketleri kapat**'ı kullanın.
7.  Satıcı mal veya hizmetleri teslim ettikten sonra faturayı kaydedin. 6. adımda satınalma emrine veya satış emrine karşı ön ödemeyi kapattıysanız, ön ödeme oluşturduğunuz faturaya karşı otomatik olarak kapatılır. Ön ödemeyi satın alma siparişi veya satış siparişi karşılığında kapatmadıysanız müşteri veya satıcı sayfasındaki **Hareketleri kapat**'ı kullanarak fatura karşılığında el ile kapatabilirsiniz. Ardından ön ödeme tutarı, geçici olarak AP/AR genel muhasebesinden tersine çevrilir. Ek olarak, vergiler hesaplandıysa bunlar tersine çevrilir çünkü fatura gerçek vergileri içerir.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Ön ödeme faturalandırma işlemine genel bakış
Ön ödeme faturaları yaygın bir iş uygulamasıdır. Bir satıcı, satınalma emri karşılanmadan önce satınalma teminatı istemek için ön ödeme faturaları çıkarır. Örneğin, bazı satıcılar özel mallar veya hizmetler için ön ödeme gerektirir. Bir satıcı ön ödeme gerektiren bir fatura çıkarırsa, ön ödeme faturalandırma özelliğini kullanabilirsiniz. Satın alma siparişinde bir ön ödeme değeri tanımlanabilir, ön ödeme faturası kaydedilir ve ödenir ve ardından ön ödeme faturası son faturaya uygulanır. Bir ön ödeme oluşturmak için şu adımları izleyin.

1.  Satınalma temsilcisi, satıcının ön ödeme istediği bir satınalma emrini oluşturur, onaylar ve ardından gönderir. Ön ödeme değeri, satınalma emrinde anlaşmasının parçası olarak tanımlıdır.
2.  Satıcı bir ön ödeme faturası gönderir.
3.  Borç hesapları koordinatörü, satınalma emrine karşı ön ödeme faturasını kaydeder ve ardından ön ödeme faturası ödenir.
4.  Satıcı, standart satıcı faturası olarak anılan bir ödeme talebi gönderir. Satıcı mal veya hizmetleri sağladıktan ve ilgili standart satıcı faturaları alındıktan sonra, Borç hesapları koordinatörü standart faturaya karşı zaten ödenmiş olan ön ödeme tutarını uygular.
5.  Borç hesapları koordinatörü standart faturanın kalan tutarını öder ve kapatır.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Ön ödeme faturalama işlemini etkinleştirmek için parametreleri ayarlama
**Stok deftere nakil** sayfasının **satın alma siparişi** sekmesinde bir ön ödeme hesabı tanımlanmalıdır (**Stok Yönetimi \>Ayarlama \> Deftere nakil \> deftere nakil**). Ön ödeme hesabı, ön ödeme faturası deftere nakledildiğinde, genellikle borç kaydedilir. Ön ödeme faturasına uygulanan standart fatura deftere nakledildiğinde, ön ödeme hesabındaki bakiye tersine çevrilir. Ön ödeme faturasını standart faturaya uygulamadan önce bir ödemeye kapatmazsanız standart fatura deftere nakledildiğinde, deftere nakledilen ön ödeme faturasındaki muhasebe girişlerine ters işlem uygulanır.

Mahsup Özet borç hesapları hesabı **satıcı deftere nakil** profilinde tanımlanmıştır. Varsayılan deftere nakil profilini tanımlamak için **Borç hesapları \>Ayarlama \> Borç hesapları parametreleri \>Kayıt defteri ve satış vergisi sekmesi \> Ön ödeme satıcı faturası ile deftere nakil profili**'ne tıklayın.

**Ön ödeme uygulama ilkesi** sistemin kapatılan ön ödeme faturalarının el ile oluşturulan son faturaya otomatik olarak uygulanıp uygulanmayacağını belirtir. Bir veri varlığı kullanılarak oluşturulan faturalar **ön ödeme uygulama ilkesine** başvurmayacaktır. Kapatılan ön ödeme faturalarını bir veri varlığı kullanılarak oluşturulmuş faturalara el ile uygulamanız gerekir. İlkeyi tanımlamak için, **Borç hesapları \>Ayarlama \> Borç hesapları parametreleri \> Kayıt defteri ve satış vergisi sekmesi \> Ön ödeme uygulama ilkesi**'ne gidin. **Ön ödeme uygulama ilkesi** alanı **otomatik** olarak ayarlanmışsa ön ödeme faturası son faturayla kapatılmak üzere otomatik olarak işaretlenir. Alan **bildirim** olarak ayarlandıysa, son fatura oluşturulduğunda, uygulama için ön ödeme faturasının kullanılabilir olduğu belirten görsel bir gösterge görüntülenir.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Ön ödeme fatura bilgilerini içeren bir satın alma siparişi oluşturma
Bir satıcı, bir satın alma siparişinde bulunan mal ve servisler için ön ödeme gerektirdiğini söylerse, ilgili satın alma siparişi için ön ödeme değerini tanımlamanız gerekir. **Borç hesapları \> Genel \> Satın alma siparişleri \> tüm satın alma siparişleri**'ne gidin ve satıcının satın alma siparişini bulun. Eylem bölmesinde, **Satın al** sekmesini ve ardından **Ön ödeme**'yi seçin. Ön ödeme için bir açıklama, ön ödeme değeri, ön ödemenin sabit bir tutar veya yüzde olduğu ve bir ön ödeme kategori kodu da dahil olmak üzere, ön ödeme bilgilerini girin. 

Bir satın alma siparişinde birden fazla ön ödeme tanımına izin verilmediğini unutmayın. Bir satın alma siparişinde birden fazla ön ödeme yapılmasına izin vermeniz gerekiyorsa, ödemeleri ön ödeme faturası yerine ödeme günlüğünü kullanarak deftere nakledin.

Ön ödeme, deftere nakledilen ön ödeme faturasına göre önceden kapatmadığınız veya standart faturayı deftere nakletmediğiniz sürece satın alma siparişinden çıkarılabilir. Satın alma siparişinden ön ödeme bilgilerini kaldırmak için, **Borç hesapları \> Genel \> Satın alma siparişleri \> Tüm satın alma siparişleri**'ni seçin ve satıcının satın alma siparişini bulun. Eylem bölmesinde, **Satın al** sekmesini ve ardından **Ön ödemeyi kaldır**'ı seçin.

## <a name="create-and-post-a-prepayment-invoice"></a>Bir ön ödeme faturası oluşturma ve deftere nakletme
Satıcının ön ödeme faturasını kaydetmek için, **Satın alma siparişleri** sayfasında **ön ödeme faturası** seçeneğini seçerek **satıcı faturası** sayfasına gidin (**Borç hesapları \> ortak \> Satın alma siparişleri \> tüm satın alma siparişleri \> Fatura sekmesi \> ön ödeme faturası**). Fatura numarası dahil olmak üzere, ön ödeme faturasıyla ilgili bilgileri girin. Bir ön ödeme faturasının miktarlarını değiştiremezsiniz. Satıcı, satın alma siparişinde tanımlanan ön ödeme değerinde kısmi bir tutar faturalanmışsa, birim fiyatı kısmi değeri yansıtacak şekilde güncelleştirebilirsiniz.

Ön ödeme faturası deftere nakledildiğinde, satıcı bakiyesi ve ön ödeme hesabı güncelleştirilir. Satın alma siparişinde yer alan ön ödeme tanımındaki **ön ödeme uygulaması** değeri de güncelleştirilecektir. Deftere nakledilen ön ödeme fişi için varsayılan mali boyut girişleri satın alma siparişindeki başlık bilgilerinden alınır.

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Ön ödeme faturası için ödemeleri deftere nakletme ve Kapatma
Sonra, ön ödeme faturası **ödeme günlüğü** sayfasından ödenir. Ödeme günlüklerine erişmek için, **Borç hesapları \> günlükler \> ödemeler \> Ödeme günlüğü**'ne tıklayın. Ödeme kapanışını ön ödeme faturasına kaydettikten sonra, satın alma siparişinin **Kalan ön ödeme uygulaması** değeri güncelleştirilir.

Ön ödeme faturasının standart faturasını deftere nakletmeden önce, ödeme kapanışını ön ödeme faturasından tersine çevirebilirsiniz. Ancak ön ödeme faturasına standart fatura uygulanmadan önce, ödeme kapanışı ön ödeme faturasından tersine çevrilemez.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Satın alma siparişi için standart satıcı faturasını deftere nakledin ve ön ödeme faturasını standart faturaya uygulayın
Satıcıdan alınan standart faturayı kaydedin. Bu işlemin bir parçası olarak, kapatılan ön ödeme faturasını satıcı faturasına uygulayarak faturanın değerinin zaten ödenmiş olan tutar kadar azalmasını sağlayabilirsiniz. Ön ödeme faturasının satıcı faturasına uygulanması, ön ödeme faturasından muhasebe girişlerinin ters çevrilmesini sağlar.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Standart fatura deftere nakledildikten sonra ön ödeme faturasını uygulama
Ön ödemeyi satıcı faturasını deftere naklederken standart satıcı faturasına uygulamayı unutursanız, **Satıcılar** sayfasından (**Borç hesapları \> ortak \> Satıcılar \> Tüm satıcılar \> faturası sekmesi  \> Uygula**) kapatılan ön ödeme bu satıcı için diğer faturalara uygulanmak üzere kullanılabilecektir.

## <a name="reversal-of-the-prepayment-application-process"></a>Ön ödeme uygulama işleminin tersine çevrilmesi
Bir ön ödeme faturasının uygulamasını açmanız veya standart bir faturadan tersine çevirmeniz gerekiyorsa **Satıcılar** sayfasından **Tersine çevir** eylemini (**Borç hesapları \> Ortak \> Satıcılar \> Tüm satıcılar \> Fatura sekmesi \> Tersine çevir**) seçin. Ön ödeme uygulaması ters çevrildikten sonra, ön ödemeyi başka bir standart faturaya uygulayabilirsiniz. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
