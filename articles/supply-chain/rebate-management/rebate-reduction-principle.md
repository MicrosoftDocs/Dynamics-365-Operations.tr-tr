---
title: İndirim azaltma ilkeleri
description: Bu konuda, indirim azaltma ilkelerini ayarlama yöntemi açıklanmaktadır. Azaltma ilkeleri aynı madde veya işleme birden çok indirim uygulama davranışını denetler.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fec7f94aba46f8b1853e0520169dd628fd940a56
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685953"
---
# <a name="rebate-reduction-principles"></a>İndirim azaltma ilkeleri

[!include [banner](../includes/banner.md)]

Bir maddeyle ilişkilendirilmiş diğer provizyonleri azaltmak ve/veya indirim hesaplamalarının sonuç değerlerini azaltmak için indirim yönetimi anlaşmalarını *azaltma ilkeleri* olarak gruplayabilirsiniz. İndirim azaltma ilkeleri ayarladıktan sonra, bunları gerektiği şekilde, indirim yönetimi ilkelerine göre tahsis edebilirsiniz.

İndirim Azaltma ilkesi kuralları yalnızca indirim anlaşmaları çakıştığında geçerlidir. Bu nedenle, çoklu indirimin borçlu olunmadığı durumlarda Çoklu indirimler verebilir.

## <a name="manage-rebate-reduction-principles"></a>İndirim azaltma ilkelerini yönetme

İndirim azaltma ilkeleri ile çalışmak için, **indirim Yönetimi \> kurulum \> indirim azaltma ilkeleri**'ne gidin. Sonra, gereken şekilde azaltma ilkeleri eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın. Her ilke için alanları aşağıdaki tabloda açıklandığı gibi ayarlayın.

| Alan | Tanım |
|---|---|
| İndirim azaltma ilkesi | İndirim Azaltma ilkesi için benzersiz bir ad girin. |
| Tanım | İndirim Azaltma ilkesi için bir açıklama girin. |
| Azaltmayı uygulama | Bu indirim azaltma ilkesine ait indirimlere azaltma esası uygulamak için bu onay kutusunu seçin. |
| Azaltma tabanı | **İndirimi Uygula** onay kutusunu işaretlediyseniz, azaltma tabanını (*provizyon*, *indirimler* veya *her ikisi*) seçin. *Her ikisi* ni seçerseniz ve önceki bir anlaşma için hem provizyon, hem de indirim deftere nakledilmişse, yalnızca indirim uygulanır. |
| Azaltmadan hariç tut | Bu onay kutusu işaretlenirse, bu indirim azaltma ilkesine ait olan hükümler ve indirimler sonraki indirimlerde dışlanır. **Azaltma tabanı** alanının ayarı bu ayara uygulanmaz. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>İndirim Azaltma ilkesi kurulumları örnekleri

Aşağıdaki tabloda, bazı tipik indirim Azaltma ilkesi kurulumu örnekleri gösterilmiştir. Bu indirim azaltma ilkelerinin her biri için, **Açıklama** alanının değeri indirim azaltma ilkesinin amacını açıklar.

| İndirim azaltma ilkesi | Tanım | Azaltmayı uygulama | Azaltma tabanı | Azaltmadan hariç tut |
|---|---|---|---|---|
| Ertelenmiş | İndirimi azalt | Evet | İkisi birden | Hayır |
| Exclreb | İndirimi hariç tut | Evet | İndirim | Evet |
| Miktar çarpanı | Birden çok indirim | Evet | İkisi birden | Evet |
| Hiçbiri | Yalnızca provizyon ve indirim | Hayır | İkisi birden | Evet |
| Sağlama | Yalnızca provizyon | Evet | Sağlama | Hayır |
| İndirim | Yalnızca indirim | Evet | İndirim | Evet |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>İndirim Azaltma ilkesi hesaplama örnekleri

Tek bir satış siparişi satırı bulunan bir satış Siparişiniz var. Bu satır 1.000 $ değerine sahip. Aşağıdaki anlaşmalar sipariş için geçerlidir:

- **Anlaşma 1:** 1.000 $ üzerinden yüzde 10
- **Anlaşma 2:** 1.000 $ üzerinden yüzde 15
- **Anlaşma 3:** 1.000 $ üzerinden yüzde 20
- **Anlaşma 4:** 1.000 $ üzerinden yüzde 25

İşlem sırası çok önemlidir. İşlem sırası [indirimleri işleme, gözden geçirme ve deftere nakletme](process-review-post.md) konularında açıklandığı gibi çalışma şeklinize göre yapılır.

Örneğin, aşağıdaki tablo *1, 2, 3, 4* sırasını kullanıyorsanız ve yalnızca provizyonları işliyorsanız sonuçları özetler.

| İşlem | Açıklama ve ayarlar | Provizyon sonucu |
|---|---|---|
| 1 | <p>Sınıflandırma, indirimlerle ilgili diğer anlaşmaları denetlemez. Denetim hem provizyonlar hem de indirimler için yapılır.</p><ul><li>**Azaltmayı uygula:** *Hayır*</li><li>**Azaltma tabanı** *Her ikisi de*</li><li>**Azaltmadan hariç tut** *Hayır*</li></ul> | 1.000 $ × %10 = 100 $ |
| 2 | <p>Sınıflandırma, indirimlerle ilgili diğer anlaşmaları denetler, ancak kendisi göz ardı edilecek şekilde işaretlenir. Denetim yalnızca indirimler için gerçekleştirilir.</p><ul><li>**Azaltmayı uygula:** *Evet*</li><li>**azaltma tabanı** *İndirim*</li><li>**Azaltmadan hariç tut** *Evet*</li></ul> | 1.000 $ × %15 = 150 $ |
| 3 | <p>Sınıflandırma, indirimlerle ilgili diğer anlaşmaları denetler. Denetim hem provizyonlar hem de indirimler için yapılır.</p><ul><li>**Azaltmayı uygula:** *Evet*</li><li>**Azaltma tabanı** *Her ikisi de*</li><li>**Azaltmadan hariç tut** *Hayır*</li></ul> | (1.000 $ – Anlaşma1) × %20 = 180 $ |
| 4 | <p>Sınıflandırma, indirimlerle ilgili diğer anlaşmaları denetler. Denetim hem provizyonlar hem de indirimler için yapılır.</p><ul><li>**Azaltmayı uygula:** *Evet*</li><li>**Azaltma tabanı** *Her ikisi de*</li><li>**Azaltmadan hariç tut** *Hayır*</li></ul> | (1.000 $ – Anlaşma 1 – Anlaşma 3) × %25 = 180 $ |

Aşağıdaki tabloda, bir provizyonun farklı siparişlerde ve bu nedenle farklı toplamların kullanıldığı bazı örnekler gösterilmiştir. Provizyonlardaki fark, sistemin anlaşmaları işleme sırasına bağlıdır. İşleme sırasının nihai indirim tutarını nasıl etkilediğini anlamanız önemlidir.

| Seri | Hesaplama |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Anlaşma 1:** 1000 $ × %10 = 100 $</li><li>**Anlaşma 2:** 1.000 $ × %15 = 150 $</li><li>**Anlaşma 3:** (1.000 $ – Anlaşma 1) × %20 = 180 $</li><li>**Anlaşma 4:** (1.000 $ – Anlaşma 1 – Anlaşma 2) × %25 = 180 $</li><li>**Toplam provizyon:** 610 $</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Anlaşma 4:** 1.000 $ x %25 = 250 $</li><li>**Anlaşma 3:** (1.000 $ – Anlaşma 4) × %20 = 150 $</li><li>**Anlaşma 2:** 1.000 $ x %15 = 150 $</li><li>**Anlaşma 1:** 1.000 $ x %10 = 100 $</li><li>**Toplam provizyon:** 650 $</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Anlaşma 3:** 1.000 $ x %20 = 200 $</li><li>**Anlaşma 2:** 1.000 $ x %15 = 150 $</li><li>**Anlaşma 1:** 1.000 $ x %10 = 100 $</li><li>**Anlaşma 4:** (1.000 $ – Anlaşma 3 – Anlaşma 1) × %25 = 175 $</li><li>**Toplam provizyon:** 625 $</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Anlaşma 2:** 1.000 $ × %15 = 150 $</li><li>**Anlaşma 4:** 1.000 $ × %25 = 250 $</li><li>**Anlaşma 1:** 1000 $ × %10 = 100 $</li><li>**Anlaşma 3:** (1.000 $ – Anlaşma 4 – Anlaşma 1) × %20 = 130 $</li><li>**Toplam provizyon:** 630 $</li></ul> |
