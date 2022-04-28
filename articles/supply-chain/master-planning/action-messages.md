---
title: Eylem iletileri
description: Bir eylem mesajı, geçerli bir planlanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570268"
---
# <a name="action-messages"></a>Eylem iletileri

[!include [banner](../includes/banner.md)]

Bir eylem iletisi, geçerli bir planlanmış, onaylanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir.

Eylem iletileri değişen gereksinimlere yanıt olarak master planlama hesaplaması tarafından oluşturulur. Örneğin, bir satış siparişi için talebi karşılamak üzere zaten bir satın alma siparişi oluşturduktan sonra söz konusu satış siparişindeki sevk tarihi veya miktarı değiştirilir. Bu durumda master planlama, satın alma siparişini güncelleştirmenizi öneren bir veya birden çok eylem iletisi oluşturur. Tavsiye edilen değişiklikleri yapıp yapmayacağınıza karar verebilirsiniz.

Bir öğeye eklediğiniz bir karşılama grubu için eylem iletilerinin nasıl hesaplanacağını ayarlayabilirsiniz.

## <a name="select-action-messages"></a>Eylem iletilerini seç

**Karşılama grupları** sayfası üzerinde, sistemin üretmesini istediğiniz eylem iletilerini ve iletilerin uygulanacağı Karşılama gruplarını veya öğelerini seçebilirsiniz. Aşağıdaki tabloda, seçebileceğiniz eylem iletileri listelenmiştir.

| İleti | Açıklama |
|---|---|
| İlerlet | Sistem, siparişleri önceki bir tarihe taşımak için gerektiğinde eylem iletilerini oluşturacaktır. **İlerletme marjı** alanı içinde, ilerletme eylemi olmadan giriş ve çıkış arasında geçebilecek maksimum gün sayısını belirtebilirsiniz. |
| Ertele | Sistem, siparişleri sonraki bir tarihe taşımak için gerektiğinde eylem iletilerini oluşturacaktır. **Erteleme marjı** alanı içinde, erteleme eylemi olmadan giriş ve çıkış arasında geçebilecek maksimum gün sayısını da belirtebilirsiniz. |
| Azalt | Sistem, fazladan stok düzeylerini önlemek üzere üretim emirleri, satın alma siparişleri ve diğer giriş hareketlerinin düşürülmesi gerektiğinde eylem iletileri oluşturacaktır. |
| Artış | Sistem, stok düzeylerinde noksanlığı önlemek üzere üretim emirleri, satın alma siparişleri ve diğer giriş hareketlerinin artırılması gerektiğinde eylem iletileri oluşturacaktır. |
| Türev eylemler | Giriş hareketleri için oluşturulan eylem iletileri türetilmiş gereksinimlere çoğaltılır ve bu gereksinimleri karşılayan giriş hareketleri için gerekli eylem iletileri oluşturulur. |

Aşağıdaki bölümler birkaç detaylı senaryo sağlar.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Ürün varsayılan sipariş miktarları ile eylemleri artırma ve azaltma

Bir maddenin **Varsayılan sipariş ayarları** sayfasında, minimum sipariş miktarı, maksimum sipariş miktarı ve birden fazla değer ayarlayabilirsiniz. Daha sonra sistem, eylemler önerdiğinde, önerilerin hiçbir zaman yetersiz tedarike yol açmamasını sağlamak için bu ayarları dikkate alır.

Örneğin, **Varsayılan sipariş ayarları** sayfasında aşağıdaki ayarlara sahip bir öğeniz var:

- **Minimum sipariş miktarı:** *0*
- **Maksimum sipariş miktarı:** *90*
- **Çarpan:** *20*

Bu maddenin 60 adedi için talep varsa master planlama, 60 adet için planlı bir satın alma siparişi oluşturur. Talep 30 adet artarsa master planlama 40 adetlik bir artış önerecektir, çünkü 20 çarpanını dikkate alır ve hiçbir şekilde yetersiz tedarike neden olmaz.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Emniyet stoğu ile ilgili siparişler için eylem iletileri

Emniyet stoğu tedarik edilen siparişlere yönelik eylem iletileri, miktarı hiçbir zaman emniyet stoğu için gerekli olan miktarın altına düşürmeyi önermez. Başka bir deyişle, emniyet stoğu ve müşteri talebi tedarik edilen bir sipariş varsa ve talep azalır veya iptal edilirse master planlama, planlı siparişi azaltılan talebe göre azaltmayı önerir. Ancak, gerekli olan emniyet stoğundan daha düşük bir değer önermeyecektir.

Güvenlik stoğunun gerekli sürede ve gerekli tarihte sağlanması gerektiği varsayıldığından sistem, güvenlik stoğu sağlamaya yönelik eylemleri ertelemeyi önermeyecektir.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Ürün reçeteleriyle ilgili ilerletme ve erteleme eylemleri

Üst düzey ürün reçeteleriyle ilgili başka siparişler etkilenebileceğinden, ürün reçetelerinin bileşenleriyle ilgili eylemlerin, üst maddelerinin eylemlerinden önce uygulanması gerekir. Gerekli eylemleri yeniden hesaplamak ve önermek için master planlamayı yeniden çalıştırmalısınız.

Örneğin, aşağıdaki durumla karşı karşıyasınız:

- *Üretim* türündeki *FG* son ürünü, *RM* hammaddesini içeren bir ürün reçetesine sahip.
- Bugünün tarihi 21 Ocak.
- *FG* için varolan, serbest bırakılmış bir üretim emri 25 Ocak'a zamanlanmıştır.
- Varolan üretim emrini desteklemek amacıyla master planlama, gerekli hammadde *RM* için planlı bir satın alma siparişi oluşturdu. Bu siparişin gereksinim tarihi 25 Ocak'tır.
- *FG* için bugün yeni bir satış siparişi oluşturulur. Gereksinim tarihi bugündür (21 Ocak).
- 21 Ocak, *RM* takviminde teslimat için kapalı ancak 22 Ocak açıktır.

Master planlama çalıştırıldığında, bugünün siparişini yerine getirebilmek için daha önce zamanlanmış üretimin yukarı taşınmasını öneren gelişmiş eylem iletileri oluşturur.

- Yeni talebi karşılamak için, *FG* için bu üretim emrinin 21 Ocak'a kadar yukarı taşınması önerilir. (Bu öneriyi *RM* için kapanış tarihini dikkate almadan yapar.)
- *RM*, üretim emri için hâlâ gerekli olduğundan, planlı satın alma siparişini de yukarı taşıma önerisinde bulunur. Ancak bu kez *RM* takvimini kontrol eder. Bu nedenle, *RM* için planlı satın alma siparişinin 22 Ocak'a (21 Ocak kapalı olduğu için) taşınması önerilir.

Gördüğünüz gibi, gerekli hammadde *RM*, *FG*'nin zamanlanan üretimi için çok geç ulaşır. Bu nedenle, önce *RM* için planlanan satın alma siparişine ilerletme eylemini uygulamanız, sonra da master planlamayı yeniden çalıştırmanız gerekir. Bu noktada master planlama, *FG* için üretim emrinin 22 Ocak'a taşınmasını öneren yeni bir eylem iletisi oluşturacaktır.
