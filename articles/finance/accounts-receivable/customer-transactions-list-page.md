---
title: Müşteri hareketleri listesi sayfası
description: Bu makalede, Microsoft Dynamics 365 Finance için Müşteri hareketleri listesi sayfası hakkında bilgi sağlanmaktadır.
author: abruer
ms.date: 08/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2ca7aaa0ccea8f4936ae4a177ef9b9eba2282ae6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864468"
---
# <a name="customer-transactions-list-page"></a>Müşteri hareketleri listesi sayfası

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Kapatmaları görüntüle

Eylem Bölmesindeki **Kapatmaları görüntüle** düğmesi, kapatma geçmişine hızlı erişim ve kapatma hareketi hakkında daha fazla bilgi sağlar. Ayrıca seçili hareketle ilgili diğer hareketleri de aynı kapatmanın parçası oldukları veya aynı ödeme günlüğünde oluşturulan ödemeler oldukları için gösterebilirsiniz.

1. **Alacak hesapları \>Tüm müşteriler** öğesine gidin.
2. Hareketleri olan bir müşteri seçin ve ardından Eylem Bölmesinde, **Müşteri** sekmesinde **Hareketler** seçeneğini belirleyin.
3. Araştırılacak bir hareketi seçin ve sonra Eylem Bölmesinde, **Kapatmaları görüntüle**'yi seçin.

    **Kapatmaları görüntüle** iletişim kutusu ortaya çıkar ve seçili hareketi ve buna mukabil kapatılan tüm belgeleri gösterir. Bu iletişim kutusu, kapatmalar geçmişi görünümüne benzer ancak tüm ilgili belgeleri de içerir.

4. İletişim kutusunda çeşitli görevleri gerçekleştirebilirsiniz. Bir veya daha fazla fiş seçin ve aşağıdaki düğmelerden birini seçin:

    - **İlgilileri göster**: Listede gösterilen belgelerin oluşturulduğu günlüklerde oluşturulan tüm ödeme günlüğü hareketlerini ve genel günlük hareketlerini müşteri için göster. Örneğin, bir ödeme gösterilirse, ödeme günlüğündeki oluşturulmuş ödemelerin tamamı gösterilecektir. Bir fatura veya ödeme gösterilirse ve genel günlükte oluşturulmuşsa, oluşturulan genel günlükteki tüm belgeler gösterilecektir. Belge listeleriyle ilişkili tüm kapatmalar da görüntülenir. Siz ilgili ödemeleri görüntülerken, bu düğmenin etiketi **Kapatmaları görüntüle** olarak değişir. **Kapatmaları görüntüle**'yi, **Kapatmaları Görüntüle** iletişim kutusunu yalnızca ilk açtığınızda gösterilen hareketleri göstermek için seçin.
    - **Geçmişi görüntüle** - Tüm fişler için kapatma geçmişini göster. İletişim kutusunu kapatmak için **Kapat**'ı seçin.
    - **Muhasebeyi görüntüle**: Seçili belgelerle ilgili tüm fişlerin tamamı gösterilir. İletişim kutusunu kapatmak için **Kapat**'ı seçin.
    - **Dışa aktar** - Seçili fişleri Microsoft Excel'e aktarın.
    - **Hareketleri kapat**: Bu düğme, yalnızca seçilen orijinal belge tam olarak kapatılmadığında görünür. Bu düğmeyi seçtiğinizde **Hareketleri kapat** iletişim kutusu görünür. Bu kutudan kapatılacak hareketleri seçebilirsiniz.
    - **Kapatmayı geri al**: Bu düğme, yalnızca seçilen orijinal belge tam olarak kapatıldığında görünür. Bu düğmeyi seçtiğinizde **Kapatmayı geri al** iletişim kutusu görünür. Bu kutudan bu belge için önceden yapılan kapatmaları geri alabilirsiniz.

## <a name="global-transactions"></a>Genel hareketler

**Genel hareketler** düğmesi **Müşteri hareketleri** liste sayfasında da görünür. Bu düğme, bir müşteri için tüm tüzel kişiliklerdeki tüm işlemleri görmenizi sağlar. **Müşteri hareketleri** listesi sayfası, yalnızca kullanıcının erişimi olan tüzel kişiliklerdeki işlemleri, onların güvenlik ayarlarına dayalı olarak gösterir.

Liste sayfası, başlatmış olduğunuz kullanıcıyla aynı taraf kimliğine sahip kullanıcılar için tüm hareketleri gösterir. Örneğin, bir tüzel varlıktaki müşteri US-001, başka bir tüzel varlıktaki müşteri DE-001 ile aynı taraf kimliğine sahipse, her iki müşteri kimliği için olan hareketler de gösterilir.

**Müşteri hareketleri** listesi sayfasındaki menüler, hareketin dayandığı tüzel kişiliğe bağlı olarak değişiklik gösterir. Örneğin, bir özellik yalnızca İsviçre'deki tüzel varlıklar için kullanılabiliyorsa, bu özellik için menü seçenekleri yalnızca bir İsviçre hareketi seçildiğinde görüntülenir.

Özelliğe erişmek için şu adımları izleyin.

1. **Alacak hesapları \>Tüm müşteriler** öğesine gidin.
2. Bir müşteri seçin ve ardından Eylem Bölmesinde, **Müşteri** sekmesinde **Hareketler** grubunda, **Genel hareketler** seçeneğini belirleyin.

## <a name="more-transaction-filters"></a>Daha fazla hareket filtresi 

Açık hareketleri gösterme filtresi, daha fazla hareket kombinasyonu görüntülemenize izin ver yeni bir filtre ile değiştirilmiştir. Aşağıdaki seçenekler **Göster** alanında kullanılabilir:

- **Tümü** - Seçilen müşteriler için tüm hareketleri göster (açık ve kapalı).
- **Kapalı** – Yalnızca tam olarak kapatılmış ve kapatılan hareketleri göster.
- **Açık** – Yalnızca tam olarak kapatılmamış göster.
- **Kapanış veya sonrası dahil açık** – Yalnızca belirttiğiniz tarihte veya daha sonra tam olarak kapatılmış hareketleri gösterir. Bu seçeneği seçtiğinizde, filtrenin yanında gösterilen tarihi değiştirebilirsiniz. Sizin belirttiğinizde tarihte veya daha sonra bir **Son kapatma tarihi** değeri olan hareketler için listede gösterilir, bu hareketler şu anki tarihte tümüyle kapatılmış olsalar bile. Bununla birlikte, bakiyeler seçili tarih itibariyle değil, geçerli tarih itibarıyla bakiyeleri temsil eder.

Para birimi dönüştürme işlemleri gizlemek için **Para birimi yeniden değerlemelerini gizle** onay kutusunu seçin.

## <a name="modify-due-dates-and-discount-dates"></a>Son tarihleri ve iskonto tarihlerini değiştirin

Açık müşteri hareketleri için son tarihleri ve iskonto tarihlerini güncelleştirebilirsiniz. 8.1 sürümünde artık **Müşteri hareketleri** liste sayfasına son tarihleri ekleyebilirsiniz. **Müşteri hareketleri** liste sayfasındaki son tarihler üzerine tıklayarak **Son tarih ve nakit iskonto tarihlerini güncelleştir**  iletişim kutusundaki son tarihleri, indirim tarihlerini, ödeme koşullarını ve nakit indirimleri değiştirebilirsiniz.

### <a name="activate-the-feature"></a>Özelliği etkinleştirme

**Müşteri hareketleri** liste sayfasına son tarihler eklemek ve **Son tarih ve nakit iskonto tarihlerini güncelleştir** iletişim kutusunu kullanarak ödeme ayarlarını değiştirmek için şu adımları izleyin.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ni seçin.
2. **Kapatmalar** sekmesinde, **Son tarihi göster ve düzenlemeye izin ver** seçeneğini **Evet** olarak ayarlayın.
3. Bu özelliği etkinleştirmek için yeni alanlar müşteri hareketlere eklenmiş olabilir. Bu alanlar, yeni bir hareket tamamlandığında doldurulacaktır. Bunlar ayrıca **Son tarih ve nakit iskonto tarihlerini güncelleştir** iletişim kutusunu açtığınızda da doldurulacaktır. **Son tarihi göster ve düzenlemeye izin ver** seçeneğini **Evet** olarak ayarladığınızda, **Ödeme bilgisini güncelleştir** iletişim kutusunu göreceksiniz.  Varolan hareketlerden hemen güncelleştirmek için **Varolan tüm hareketleri güncelleştir**'i seçin. Alternatif olarak, yalnızca yeni hareketler için alanları doldurmak **Güncelleştirme olmadan devam et**'i seçin.

Son tarih şimdi **Müşteri hareketleri** liste sayfasına eklendi, böylece son tarih ve nakit iskontosu tarihlerini hareketler için kolayca değiştirebilirsiniz.

### <a name="modify-the-payment-settings"></a>Ödeme ayarlarını değiştirme

**Müşteri hareketleri** liste sayfası bir müşteri için tüm hareketleri gösterir. Bir hareket için son tarihi seçtiğinizde **Son tarihi ve nakit iskonto tarihlerini güncelleştir** iletişim kutusu görüntülenir. Bu iletişim kutusu, son tarih ve iskonto hesaplamaları, son tarih, ödeme koşulları, nakit iskontosu koşulları ve nakit iskontosu tarihleri için temel tarihi gösterir,

Her alan, düzenlediğinizde hareket üzerinde farklı bir etkiye sahiptir:

- **Taban tarihi düzenle** - Son tarih ve iskonto tarihleri, taban tarih belge tarihiymiş gibi değiştirilir.
- **Son tarihi düzenle** - Yalnızca son tarih değiştirilir.
- **İskonto tarihlerini değiştir** - Yalnızca iskonto tarihleri değiştirilir.
- **Ödeme koşullarını düzenle** - Son tarih değiştirilir, taban tarihe ve ödeme koşullarına dayanarak.
- **Nakit iskonto şartlarını düzenle:** - Nakit iskontolar, taban tarih ve nakit iskontosu koşullarına dayanarak değiştirilir.

Ödeme ayarları düzenlemeyi bitirdiğinizde, **Kapat**'ı seçerek yaptığınız değişiklikleri kaydedin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
