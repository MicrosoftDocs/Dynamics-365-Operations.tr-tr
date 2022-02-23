---
title: Otomatik masraf tahsisatı
description: Microsoft Dynamics 365 Supply Chain Management masraflar özelliği, Satınalma siparişlerine veya satış siparişlerine masrafları otomatik olarak tahsis etmenize yardımcı olur.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 818affc7591577b69309928eb9b0e71130884cec
ms.sourcegitcommit: 66ecc6cb36ef4f723c77e09d6a33f9c42f8fa392
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439598"
---
# <a name="automatic-allocation-of-charges"></a>Otomatik masraf tahsisatı

[!include [banner](../includes/banner.md)]

Çalıştığınız müşteriye veya sattığınız ürüne bağlı olarak belirli ek masraflar uygulamak isteyebilirsiniz. Microsoft Dynamics 365 Supply Chain Management *masraflar* özelliği, Satınalma siparişlerine veya satış siparişlerine masrafları otomatik olarak tahsis etmenize yardımcı olur.

Otomatik masraflar, bir satış siparişi veya satınalma siparişi oluşturduğunuzda otomatik olarak uygulanır. Belirli satıcılar, müşteriler, satıcı grupları veya maddeler için otomatik masraflar tanımlayabilirsiniz. Ayrıca, tüm satıcılar, müşteriler veya maddeler için geçerli olan otomatik masraflar da tanımlayabilirsiniz.

## <a name="set-up-charges-codes"></a>Masraf kodlarını ayarlama

Masrafları tahsis etmek için öncelikle masraf kodlarını tanımlamanız gerekir.

1. Şu adımlardan birini izleyin:

    - Satınalma siparişleri için: **Borç hesapları \> masraflar kurulumu \> masraflar koduna** gidin.
    - Satış siparişleri için: **Alacak hesapları \> masraflar kurulumu \> masraflar koduna** gidin.

1. Eylem bölmesinde **Yeni**'yi seçerek yeni bir masraflar kodu oluşturun.
1. Yeni kaydın üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Masraflar kodu**: Masraflar için bir kod girin.
    - **Açıklama**: Masrafların açıklamasını girin.
    - **Madde satış vergisi grubu**: Uygunsa bir madde satış vergisi grubu seçin.
    - **Eşit dağıt**: Masraflarınızı eşit dağıtmak istiyorsanız bu seçeneği *Evet* olarak ayarlayın. Bu seçenek yalnızca satış siparişleri için kullanılabilir.
    - **Maksimum tutar**: Masraf kodu için izin verilen maksimum tutarı girin. Bu alan, satıcı faturaları için masrafları doğrulamak amacıyla kullanılır. Yalnızca satınalma siparişleri için kullanılabilir.

        > [!NOTE]
        > Satınalma siparişlerinin masraflarını doğrulama işlevini etkinleştirmek için, **Borç hesapları \> Kurulum \> Borç hesapları parametrelerine** gidin. **Fatura doğrulama** hızlı sekmesinde, **Fatura doğrulama** bölümünde, **Fatura eşleştirme doğrulamasını etkinleştir** seçeneğini *Evet* olarak ayarlayın.

1. **Deftere nakil** Hızlı sekmesi, **Borç** ve **Alacak** bölümlerini içerir. Masrafları nakletmek istediğiniz kayıt defterine bağlı olarak aşağıdaki alanları ayarlayın:

    - **Tür**: Deftere nakil yaptığınız hesabın türünü seçin (*Kayıt defteri*, *müşteri* veya *madde*).
    - **Deftere nakil**: Oluşturulacak deftere nakil türünü (*Aracı masrafı* veya *Müşteri hesap kapatması gibi*) seçin.
    - **Hesap**: Masrafın nakledileceği hesabı seçin.

1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="create-charge-groups"></a>Masraf grupları oluştur

Masraf grupları bir grup müşteriye veya satıcıya otomatik olarak belirli masrafları tahsis eder. Aşağıdaki alt bölümler, bu Masraf gruplarının nasıl oluşturulacağını ve atanacağını açıklamaktadır.

### <a name="charge-groups-for-purchase-orders"></a>Satınalma siparişleri için Masraf grupları

Satınalma siparişleri için Masraf grupları oluşturmak üzere aşağıdaki adımları izleyin.

1. **Borç hesapları \>Masraf kurulumu \> Satıcı masrafları grubu**.
1. Eylem Bölmesinde, kılavuza satır eklemek için **Yeni**'yi seçin ve ardından aşağıdaki alanları ayarlayın:

    - **Masraflar grubu**: Masraflar grubunun adını girin.
    - **Açıklama**: Masraf grubunun açıklamasını girin.

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Borç hesapları \>Satıcılar \> Tüm satıcılar**'a gidin ve varolan bir satıcıyı açın ya da yeni bir satıcı oluşturun.
1. **Satınalma siparişi Varsayılanları** hızlı sekmesinde, **Satınalma siparişi** bölümünde, **Masraf grubu** alanını henüz oluşturduğunuz Masraf grubu olarak ayarlayın.

### <a name="charge-groups-for-sales-orders"></a>Satış siparişleri için Masraf grupları

Satış siparişleri için Masraf grupları oluşturmak üzere aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Masraflar kurulumu \> Müşteri Masraf grupları**'na gidin.
1. Eylem Bölmesinde, kılavuza satır eklemek için **Yeni**'yi seçin ve ardından aşağıdaki alanları ayarlayın:

    - **Masraflar grubu**: Masraflar grubunun adını girin.
    - **Açıklama**: Masraf grubunun açıklamasını girin.

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Alacak hesapları \> müşteriler \> Tüm müşteriler**'e gidin ve varolan bir müşteriyi açın veya yeni bir müşteri oluşturun.
1. **Satınalma siparişi Varsayılanları** hızlı sekmesinde, **Satış siparişi** bölümünde, **Masraf grubu** alanını henüz oluşturduğunuz Masraf grubu olarak ayarlayın.

## <a name="define-auto-charges"></a>Otomatik Masrafları tanımla

Masraf kodlarınızı ayarladıktan sonra, otomatik Masrafları tanımlamak için aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - Satınalma siparişleri için: **Tedarik ve kaynak \> Kurulum \> Masraflar \> Otomatik Masraflar**'a gidin.
    - Satış siparişleri için: **Alacak hesapları \> Kurulum \> Masraflar kurulumu \> Otomatik Masraflar**'a gidin.

1. Liste bölmesinde, **düzey** alanında otomatik masrafın geçerli olduğu düzeyi seçin:

    - *Ana*: Masrafları sipariş üst bilgisine uygular.
    - *Satır*: Masrafları sipariş satırlarına uygular.

1. Düzenlemek için varolan bir otomatik Masrafı seçin veya Yeni bir otomatik Masraf tanımlamak için **Yeni**'yi seçin.
1. **Hesap kodu** listesinde, etkilenecek hesapların kapsamını belirtmek için aşağıdaki değerlerden birini seçin:

    - *Tablo*: Masrafları belirli bir müşteriye veya satıcıya atar.
    - *Grup*: Masrafları sair masraflar grubuna atar.
    - *Tümü*: Masrafları tüm müşterilere veya satıcılara atar.

1. **Müşteri ilişkisi** veya **Satıcı ilişkisi** alanında **Hesap Kodu**'nu *Tablo* olarak ayarladıysanız belirli bir müşteriyi veya satıcıyı seçin. **Hesap kodu** alanını *Grup* olarak ayarladıysanız bir müşteri veya satıcı masraf grubu seçin.
1. **Madde kodu** alanında, etkilenecek maddelerin kapsamını belirtmek için aşağıdaki değerlerden birini seçin. Madde kodunu yalnızca, satır düzeyinde otomatik masraflar tanımladığınızda seçebilirsiniz.

    - *Tablo*: Masrafları özel bir maddeye atar.
    - *Grup*: Masrafları madde masrafları grubuna atar.
    - *Tümü*: Masrafları tüm maddelere atar.

1. **Madde ilişkisi** alanında **Madde kodu**'nu *Tablo* olarak ayarladıysanız belirli bir maddeyi seçin. **Madde kodu** alanını *Grup* olarak ayarladıysanız bir madde masraf grubu seçin.
1. **Yalnızca satış siparişleri için:** **Teslimat kodu şekli** alanında, etkilenecek teslimat şekillerinin kapsamını belirtmek için aşağıdaki değerlerden birini seçin:

    - *Tablo*: Masrafları belirli bir teslimat şekline atar.
    - *Grup*: Masrafları bir teslimat grubu şekline atar.
    - *Tümü*: Masrafları tüm teslimat şekillerine atar.

1. **Yalnızca satış siparişleri için:** **Teslimat ilişkisi şekli** alanında **Teslimat kodu şeklini** *Tablo* olarak ayarladıysanız belirli bir teslimat şekli seçin. **Teslimat kodu şekli** alanını *Grup* olarak ayarladıysanız bir teslimat grubu şekli seçin.
1. **Satırlar** hızlı sekmesinde, geçerli otomatik masraf uygulandığında kullanılacak masrafları ve masraf oranlarını tanımlayın. İstediğiniz sayıda satır eklemek için bu hızlı sekmede araç çubuğunu kullanabilirsiniz. Her satırda, aşağıdaki alanları ayarlayın:

    - **Para birimi**: Masrafı hesaplamak için kullanılması gereken para birimini seçin.
    - **Masraflar kodu**: Masraf kodunu seçin.
    - **Kategori**: Aşağıdaki değerlerden birini seçin:

        - *Sabit*: Masraf satıra sabit bir tutar olarak girilir. Sabit masraflar hem sipariş üst bilgisinde hem de sipariş satırlarında bulunan masraflarda kullanılabilir.
        - *Prç*: Masraf, birime göre belirlenir. Bu masraflar yalnızca sipariş satırlarında kullanılabilir. Bunlar, sipariş toplamını hesapladığınızda görüntülenir.
        - *Yüzde*: Masraf satıra yüzde olarak girilir. Yüzde masraflar hem sipariş üst bilgisinde hem de sipariş satırlarında bulunan masraflarda kullanılabilir.
        - *Şirketlerarası yüzde*: Masraf şirketlerarası siparişler için satırda bir yüzde olarak girilir. Şirketlerarası yüzde masraflar yalnızca sipariş satırlarında kullanılabilir.
        - *Harici*: Masraf, bir veya daha fazla sevkiyat taşıyıcısıyla ilişkilendirilmiş olan bir üçüncü taraf servis tarafından hesaplanır.

    - **Masraf değeri**: Seçtiğiniz kategoriye göre masraf değerini girin.
    - **Masraflar para birimi kodu**: **Para birimi** alanında belirttiğiniz para biriminden farklı bir para birimi kullanmak istiyorsanız, masraf için bir para birimi belirtin. Yalnızca seçili masraf kodu için **borç türü** veya **alacak türü** *Kayıt defteri hesabı* veya *Madde* olarak ayarlandığı takdirde farklı bir para birimi kullanabilirsiniz.
    - **Başlangıç tutarı**: Otomatik masrafın uygulanacağı başlangıç tutarını belirtin. Bu içerikte, tutar sipariş toplamını ifade eder.
    - **Bitiş tutarı**: Otomatik masrafın uygulanacağı bitiş tutarını belirtin. Bu içerikte, tutar sipariş toplamını ifade eder.
    - **Satış vergisi grubu**: Bir satış vergisi grubu belirtin.
    - **Site** ve **Ambar**: Masrafların yalnızca belirli bir site ve ambar için uygulanması gerekiyorsa, bir site ve ambar belirtin.
    - **Sakla**: Faturalamadan sonra masraf işlemlerini saklamak için bu onay kutusunu işaretleyin. Böylece seçili müşteri hesabı için her yeni fatura oluşturduğunuzda bu masraf uygulanır.

1. **Yalnızca satış siparişleri için:** Katmanlı masrafları hesaplamak istiyorsanız, bilgi için [satış siparişlerindeki katmanlı masraflar](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) konusuna bakın.

## <a name="allocate-charges-from-the-header-to-a-line"></a>Masrafları üst bilgiden satıra tahsis et

Aşağıdaki yordamda, üst bilgi düzeyindeki masrafların bir satıra nasıl tahsis edileceği gösterilir. Bu yordama başlamadan önce *sabit tutar* türünün bir üst bilgi düzeyinde masrafınızın ve bu masrafın uygulandığı siparişinizin olması gerekir. Ek olarak, siparişte zaten en az bir satır maddesi bulunmalıdır.

1. Satınalma siparişi veya masraf siparişini açın.
1. Eylem bölmesinde aşağıdaki adımlardan birini izleyin:

    - Satınalma siparişleri için: **Satınalma** sekmesinde, **Masraflar** grubunda, **Masrafları tahsis et**'i seçin.
    - Satış siparişleri için: **Sat** sekmesinde, **Masraflar** grubunda, **Masrafları tahsis et**'i seçin.

1. **Masrafları sipariş satırlarına tahsis et** iletişim kutusunda, aşağıdaki alanları ayarlayın:

    - **Masraf tahsisatı**: Masrafların nasıl tahsis edileceğini belirtmek için aşağıdaki değerlerden birini seçin:

        - *Net tutar*: Masrafları toplam net tutara görece her satır tutarına göre tahsis edin.
        - *Miktar*: Masrafları, toplam birim sayısına ilişkin her satır için birim sayısına göre tahsis edin.
        - *Satır başına*: Masrafları toplam satır sayısına göre eşit olarak tahsis edin.

    - **Masrafları satırlara tahsis et**: Masrafların tüm satırlara mı, yalnızca pozitif satırlara mı, yoksa yalnızca negatif satırlara mı tahsis edileceğini belirten bir değer seçin.
    - **Tümünü tahsis et**: Masraf kodunda *Madde* dışında bir borç türü olsa bile masrafları sipariş satırlarına tahsis etmek için bu onay kutusunu seçin.
    - **Alınan**: Masrafları yalnızca alınan sipariş satırlarına tahsis etmek için bu onay kutusunu seçin.
    - **Stoğu tutulan**: Masrafları yalnızca stoğu tutulan sipariş satırlarına tahsis etmek için bu onay kutusunu seçin.
    - **Seçimleri göster ve belirli satırları Temizle**: Belirli satırları bu tahsisatın dışında tutmak için bu onay kutusunu seçin. Bu onay kutusunu seçtiğinizde, **Tahsisatın dışında tutulacak satırları Seç** ızgarası açılır. Bu ızgara yalnızca **Masrafları satırlara tahsis et** ve **Stoğu tutulan** ayarlarında tanımlanan ölçütü karşılayan satırları içerir. Örneğin, **Masrafları satırlara tahsis et** alanını *Pozitif satırlar* olarak ayarlayıp **Stoğu tutulan** onay kutusunu belirlerseniz, ızgarada yalnızca hem pozitif hem de stoğu tutulan satırlar görüntülenir. Buna ek olarak, ızgara otomatik olarak, tam miktarın teslim alındığı satırları filtreler. Izgara açıkken, tahsisattan hariç tutulması gereken her satır için **dahil et** onay kutusunu temizleyin. 

        > [!IMPORTANT]
        > **Tahsisattan hariç tutulacak satırları Seç** ızgarasıyla çalışırken **tahsis et**'i seçene kadar ızgarayı açık bırakmayı unutmayın. **Tahsisatı** seçmeden önce ızgarayı kapatırsanız ızgaradaki ayarlarınız kaybolur. Bu nedenle, masraflar daha önce tanımladığınız ölçütlere göre tahsis edilir.

1. Ayarlarınızı uygulayıp iletişim kutusunu kapatmak için **Tahsis Et**'i seçin.
