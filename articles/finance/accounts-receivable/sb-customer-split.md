---
title: Faturalama planlarında müşteri bölme
description: Bu makalede, abonelik faturalaması kullanılırken müşteriyi bölme işlemi açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746324"
---
# <a name="customer-split-on-billing-schedules"></a>Faturalama planlarında müşteri bölme

Faturalama planında *fatura hesabı*, faturayı ödemek için satış siparişi faturasını alan müşteridir. Bazı senaryolarda, bir faturayı birden fazla müşteri ödeyebilir. **Müşteri bölme** işlevi, aynı faturalama planı için faturalanabilecek daha fazla müşteri eklemenize olanak tanır. Bu işlevi etkinleştirmek için **Abonelik faturalaması \> Yinelenen sözleşme faturalaması \> Kurulum \> Yinelenen sözleşme faturalama parametreleri** seçeneğine gidin ve **Müşteri bölme** seçeneğini **Evet** olarak ayarlayın.

## <a name="customer-split-on-the-billing-schedule-header"></a>Faturalama planı başlığında müşteri bölme

Faturalama planı oluşturulduktan sonra faturalama planı başlığına ek müşteriler eklenebilir.

Müşteri eklemek için şu adımları izleyin.

1. **Faturalama zamanlaması** sekmesinde **Müşteri bölme**'yı seçin. Üst kısımdaki **Müşteri hesabı** ve **Müşteri hesabı adı** alanları, **Faturalama planı müşterisi** olarak atanan müşteriyi belirtir.

    > [!NOTE]
    > Eklediğiniz müşteri hesabı fatura hesabıyla aynı olamaz.

2. **Müşteri bölme satırları** sekmesinde **Satır ekle**'yı seçin.
3. Bir müşteri seçin ve ardından bu müşteri için her faturanın yüzde değerini girin.
4. Varsayılan olarak, başlangıç ve bitiş tarihleri için faturalama planının başlangıç ve bitiş tarihleri kullanılır. Yeni müşteri, faturalama planının yalnızca bir kısmı için belirtilen yüzdeyi ödeyecekse farklı başlangıç ve bitiş tarihleri girin. Örneğin, faturalama planının başlangıç tarihi 1 Ocak ve bitiş tarihi 31 Aralık ise ve yeni müşteri ilk dokuz ay için yüzde 40 oranında faturalandıysa başlangıç tarihini 1 Ocak ve bitiş tarihini 30 Eylül olarak belirtin ve yüzde olarak **40,00** girin.

Müşteri bölme satırlarına birden fazla müşteri ekleyebilirsiniz. Bu durumda girilen toplam değer yüzde 100'ü geçmemelidir. **Fatura oluşturma** işlemi sırasında satış siparişi satırında gösterilecek bilgi alanları olarak müşteri referansı ve müşteri talebini girin.

Satır ayrıntılarında eklenen müşterilerin iletişim bilgileri, teslimat adresi, fatura adresi ve ödeme ayrıntıları gösterilir. Bu bilgiler, müşterilerin satış siparişinde de gösterilir.

Faturalama planı başlığına müşteri bölme bilgilerini eklediğinizde faturalama planında faturalanmamış faturalama planı satırları varsa değişiklikleri aşağı yuvarlamanızı isteyen şu iletiyi alısınız: "Başlıktan satırlara doğru yapılan değişikliği aşağı yuvarlamak istiyor musunuz? Değişiklikler yalnızca faturalanmamış faturalama planı satırlarını güncelleştirir." Faturalama planı satırındaki müşteri bölme bilgilerini güncelleştirmek için **Evet**'i seçin. Faturalama planı satırı zaten faturalanmışsa değişiklikler güncelleştirilmez.

**Planı kopyala** seçeneği kullanılarak bir faturalama planı oluşturulursa müşteri bölme başlık satırlarına varsayılan bilgiler girilir. Müşteri hesabıyla aynı olamaz.

**Fatura oluşturma** işlemi tamamlandığında birden çok satış siparişi oluşturulur. (Otomatik deftere nakil kullanılıyorsa birden çok satış faturası da oluşturulur.) Bu satış siparişleri ve satış faturaları, **Fatura ayrıntısını görüntüle** sayfasının **Satır ayrıntıları** hızlı sekmesindeki **Fatura** sekmesinde görüntülenebilir. **Birden çok** seçeneği, birden çok satış siparişinin ve satış faturasının oluşturulduğunu belirtmek için fatura ayrıntısı satırında gösterilir.

## <a name="customer-split-on-billing-schedule-lines"></a>Faturalama planı satırlarında müşteri bölme

Yalnızca belirli faturalama planı satırlarını bölmek istiyorsanız müşteri bölme, ayrı faturalama planı satırlarına eklenebilir. Satırda **Müşteri bölme** onay kutusunu işaretleyin ve ardından müşteri bölme bilgilerini güncelleştirmek veya girmek için faturalama planı satırının menüsünde **Müşteri bölme**'yi seçin.

Denetim bilgileri, faturalama planı önceden faturalanmışsa güncelleştirilir ancak faturalama planı satırındaki yüzde değiştirilir. Bu değişiklikten sonra faturalanan tüm satırlarda yeni yüzde kullanılır.

> [!NOTE]
> - Müşteri bölme seçeneği, stoğu tutulan ürünlerle kullanılamaz.
> - **Faturalanmamış gelir** onay kutusu işaretlenirse **Müşteri bölme** onay kutusu işaretlenemez.
> - **Yalnızca gelir bölme** seçeneğini kullanırsanız **Müşteri bölme** seçeneği üst satırda görüntülenir ancak alt satır maddelerinde görüntülenmez.
