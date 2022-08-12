---
title: B2B siteleri için Commerce katalogları oluşturma
description: Bu makalede, Microsoft Dynamics 365 Commerce işletmeden işletmeye (B2B) siteleri için Commerce kataloglarının nasıl oluşturulacağı açıklanmaktadır.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136839"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>B2B siteleri için Commerce katalogları oluşturma

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce işletmeden işletmeye (B2B) siteleri için Commerce ürün kataloglarının nasıl oluşturulacağı açıklanmaktadır. B2B siteleri ile ilgili Commerce katalogları hakkında sık sorulan soruların yanıtları için bkz. [B2B için Commerce katalogları SSS](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Bu makale, Dynamics 365 Commerce sürüm 10.0.27 ve sonraki sürümler için geçerlidir.

B2B çevrimiçi mağazalarınızda sunmak istediğiniz ürünleri belirlemek için Commerce kataloglarını kullanabilirsiniz. Bir katalog oluşturduğunuzda, ürünlerin sunulduğu çevrimiçi mağazaları tanımlar, dahil etmek istediğiniz ürünleri eklersiniz ve ticari satış ayrıntıları ekleyerek ürün tekliflerini geliştirebilirsiniz. Aşağıdaki çizimde gösterildiği gibi her B2B çevrimiçi mağazası için birden çok katalog oluşturabilirsiniz.

![Commerce ürün katalogları önizlemesi.](./media/Commerce_Catalogs.png)

Commerce ürün katalogları aşağıdaki bilgileri tanımlamanızı sağlar:

- **Katalog türü** – Değeri **B2B** olarak ayarlayın. Katalog hiyerarşisi, müşteri hiyerarşisi ve kataloğa ait öznitelik meta verileri gibi B2B kataloğuna özgü özellikleri tanımlayabilirsiniz. 
- **Kataloğa özgü gezinti hiyerarşisi** – Kuruluşlar, belirli kataloglarında ayrı bir kategori yapısı oluşturabilir.
- **Kataloğa özel öznitelik meta verileri** – Öznitelikler bir ürünle ilgili ayrıntıları içerir. Bir gezinti hiyerarşisinin kategorisine öznitelik atayarak, o kategoriye atanan ürün düzeyinde o nitelikler için değerler tanımlayabilirsiniz. Kuruluşlar ardından şu görevleri tamamlayabilir:

    - Kataloğa özel öznitelik değerleri tanımlayın.
    - Katalog düzeyindeki özniteliklerin görünürlüğünü kontrol edin.
    - Tek bir kataloğa özel iyileştiricileri seçin.

- **Kanallar** – Kuruluşlar, bir katalogla birden fazla B2B çevrimiçi kanalını ilişkilendirebilir. Kataloglar için uçtan uca destek şu anda yalnızca B2B çevrimiçi mağazalarda kullanılabilir.
- **Müşteri hiyerarşileri** – Belirli bir B2B kanalı için kuruluşlar, müşteri hiyerarşilerini bu katalogla ilişkilendirerek, seçilen B2B ortakları için kullanılabilir bir kataloğu yapabilirler.
- **Fiyat grupları** – Belirli bir kataloğa özgü fiyatları ve yükseltmeleri konfigüre edebilirsiniz. Bu özellik, bir B2B kanalına yönelik kataloğun tanımlanması için temel bir nedendir. Katalogların fiyat grupları, kuruluşların, ürünleri amaçlanan B2B organizasyonlarına kullanabilmesini ve tercih edilen fiyatlarını ve iskontolarını uygulamasını sağlar. Konfigüre edilen bir katalogdan sipariş veren B2B müşterileri, Commerce B2B sitesinde oturum açtıktan sonra özel fiyat ve promosyonlardan yararlanabilir. Kataloğa özel fiyatları yapılandırmak için **Kataloglar** sekmesindeki **Fiyat grupları**'ni belirleyerek kataloğa bir veya daha fazla fiyat grubu bağlayın. Müşteriler bu katalogdan sipariş verdiği zaman, aynı fiyat grubuna bağlı tüm ticari sözleşmeler, fiyat ayarlaması günlükleri ve gelişmiş indirimler uygulanır. (Gelişmiş indirimler eşik, miktar ve karıştır ve eşle iskontolarını içerir.) Fiyat grupları hakkında daha fazla bilgi için bkz. [Fiyat grupları](price-management.md#price-groups).

> [!NOTE]
> Bu özellik, Dynamics 365 Commerce 10.0.27 sürümünden itibaren mevcuttur. Gezinti hiyerarşisi ve müşteri hiyerarşisi gibi kataloğa özgü yapılandırmaları konfigüre etmek için Commerce headquarters'ta, **Özellik yönetimi** çalışma alanını açın (**Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**), **Perakende kanallarda çoklu katalog kullanımını etkinleştir** özelliğini etkinleştirin ve sonra **1110 CDX** işini çalıştırın. Bu özelliği etkinleştirdiğinizde POS mağazaları veya çağrı merkezi için kullanılan tüm kataloglar, **Kataloglar** sayfasında **Katalog türü = B2C** olarak işaretlenir. Yalnızca **Katalog türü = B2C** olarak işaretlenen mevcut ve yeni kataloglar, POS mağazaları ve çağrı merkezinde uygulanabilir. 

## <a name="b2b-catalog-process-flow"></a>B2B kataloğu işlem akışı

Katalog oluşturma ve işleme işleminde dört genel adım vardır. Her adım, sonraki bölümde ayrıntılı olarak açıklanmıştır.

> [!NOTE]
> Devam etmeden önce kataloğun **Katalog türü = B2B** olarak işaretlendiğinden emin olun.

1. **[Yapılandırma](#configure-the-catalog)**

    - Gezinti hiyerarşisini ilişkilendirin.
    - Uygulanabilir olması halinde süre ve geçerlilik bitiş tarihlerini belirtin.
    - Ürün ekleyin ve kategorilendirin.
    - Fiyat gruplarını ilişkilendirin.
    - B2B kuruluşlarınıza özel bir müşteri hiyerarşisini ilişkilendirin. 
    - Boyut, stil ve renk gibi iyileştiriciler için varsayılan boyut öznitelik grubunu ilişkilendirin.
    - Öznitelik meta verileri ayarla.

1. **[Doğrulama](#validate-the-catalog)** – Bu adımda, belirli davranışı zorlayan doğrulama kuralları çalıştırırsınız. Burada bazı örnekler verilmiştir:

    - Kategorilere ayrılmamış bir ürün bulunmadığından emin olun.
    - Her bir kanala yönelik olarak sıralanmış tüm öğelerin bir katalog ile ilişkilendirildiğinden emin olun.

1. **[Onay](#approve-the-catalog)**
1. **[Yayınlama](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Kataloğu ayarlama

Kataloğunuzu ayarlamak için bu bölümdeki bilgileri kullanın.

### <a name="configure-the-catalog"></a>Kataloğu yapılandırma

Kataloğunuzu yapılandırmak için Commerce headquarters'ta **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin.

Yeni bir katalog oluştururken önce kataloğu bir veya daha fazla kanalla ilişkilendirmeniz gerekir. Katalog oluştururken yalnızca seçtiğiniz kanal [ürün çeşitlerine](/dynamics365/unified-operations/retail/assortments) bağlı maddeler kullanılabilir. Kataloğu bir veya daha fazla kanalla ilişkilendirmek için, **Katalog kurulumu** sayfasının **Commerce kanalları** hızlı sekmesinde **Ekle**'yi seçin. Kataloğun **Katalog türü = B2B** olarak işaretlendiğinden emin olun.

#### <a name="associate-the-navigation-hierarchy"></a>Gezinti hiyerarşisini ilişkilendirin

Kataloğa ürünler eklemek için bir gezinme hiyerarşisi seçilmelidir. Gezinme hiyerarşisi, katalog için kategori yapısını destekler. **Katalog kurulumu** sayfasındaki **Commerce kanalları** hızlı sekmesinde seçili kanallarla ilişkili gezinme hiyerarşilerinden birini seçmeniz gerekir. Varsayılan bir gezinti hiyerarşisini kanallarınızla ilişkilendirmek için **Retail ve Commerce \> Kanal kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.

#### <a name="specify-time-effective-and-expiration-dates"></a>Yürürlük ve bitiş tarihlerini belirtin

Kataloğa ilişkin başlangıç ve sona erme tarihlerini belirtmek için ana katalog başlık görünümüne dönmek üzere katalog hiyerarşisinin en üst düğümünü seçin. Ardından, **Genel** hızlı sekmesinde, başlangıç ve bitiş tarihlerini gerekli şekilde yapılandırın.

#### <a name="add-and-categorize-products"></a>Ürün ekleyin ve kategorilendirin

Kataloğa eklenecek ürünleri yapılandırmak için Commerce headquarters'ta **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Sonra **Kataloglar** sekmesinde **Ürün ekle**'yi seçin.

Alternatif olarak, gezinti hiyerarşisinde bir düğüm seçin. Böylece, katalogdaki bir kategoriye doğrudan ürün ekleyebilirsiniz.

#### <a name="associate-price-groups"></a>Fiyat gruplarını ilişkilendirin

Kataloğa eklenecek ürünleri yapılandırmak için Commerce headquarters'ta **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Sonra **Kataloglar** sekmesinde **Ürün ekle**'yi seçin. 

Eylem Bölmesi'nde **Ürün ekle** seçilerek gezinti hiyerarşisinin kök düğümünden kataloğa eklenen ürünler, kaynak gezinti hiyerarşisi de katalog ile ilişkilendirilmişse kategorilerini devralacaktır. Kaynak gezinti hiyerarşisinde kategorilerde yapılan değişiklikler, kataloglara anında yansıtılır. Kanalları güncelleştirmek için katalogları yeniden yayımlamanız gerekir.

Alternatif olarak gezinti hiyerarşisinde bir düğüm seçebilir ve katalogda seçili bir kategoriye doğrudan ürün ekleyebilirsiniz. 

Ürün eklediğinizde **Yalnızca ana ürün seçildiğinde tüm varyantları otomatik olarak dahil et** seçeneği kullanılabilir olacaktır. Tüm varyantların dahil olmasını önlemek için ana ürün için en az bir varyant seçin. 

> [!NOTE]
> Büyük bir ana ürün seçimine tüm varyantları otomatik olarak dahil etmeyi seçerseniz işlem süreleri uzayabilir. Daha geniş çaplı seçimler için operasyonu toplu iş modunda çalıştırmak üzere kataloglar sayfasının Eylem Bölmesi'nde **Tüm varyantları dahil et** seçeneğini belirlemeniz önerilir. Kataloğa yalnızca ana ürünü eklediyseniz ve bir varyant eklemediyseniz ürün ayrıntıları sayfasına gittiğinizde varyant seçici kullanılabilir olmayabilir. 

Kataloğa özel fiyatlar konfigüre etmek için kataloğa bir veya daha fazla fiyat grubu bağlamanız gerekir. Fiyat gruplarını katalog ile ilişkilendirmek için Commerce headquarters'ta **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde **Fiyatlandırma** altında **Fiyat grupları**'nı seçin. Müşteriler bu katalogdan sipariş verdiği zaman, aynı fiyat grubuna bağlı tüm ticari sözleşmeler, fiyat ayarlaması günlükleri ve perakende gelişmiş indirimleri (eşik değeri, miktar ve karma ve eşleşme indirimleri) uygulanır.

Fiyat grupları hakkında daha fazla bilgi için bkz. [Fiyat grupları](price-management.md#price-groups).

> [!NOTE]
> **Tüm kataloglar** sayfasından yeni bir fiyat grubu oluşturamazsınız. Bunun yerine, bunu **Tüm fiyat grupları** sayfasından oluşturmanız gerekir. **Tüm kataloglar** sayfasındaki katalogla ilişkilendirmelisiniz.

#### <a name="associate-a-customer-hierarchy"></a>Müşteri hiyerarşisi ile ilişkilendirme

Commerce headquarters'ta, müşteri hiyerarşileri ilişkilendirmek için **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde, **Müşteri hiyerarşisi** altında kataloğa bir veya daha fazla müşteri hiyerarşisi bağlamak için **Hiyerarşileri ata**'yı seçin.

> [!NOTE]
> **Tüm kataloglar** sayfasından yeni bir müşteri hiyerarşisi oluşturamazsınız. Bunun yerine, bunu **Müşteri hiyerarşileri** sayfasından oluşturmanız gerekir. **Tüm kataloglar** sayfasındaki katalogla ilişkilendirmelisiniz.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Boyut, stil ve renk gibi iyileştiriciler için varsayılan boyut öznitelik grubunu ilişkilendirin

Boyut, stil ve renk gibi iyileştiriciler için varsayılan bir boyut öznitelik grubunu Commerce headquarters'ta ilişkilendirmek üzere **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde **Öznitelikler** altında **Öznitelik grupları**'nı seçin.

#### <a name="set-attribute-metadata"></a>Öznitelik meta verileri ayarla

Commerce headquarters'ta, öznitelik meta verilerini yapılandırmak için **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde **Öznitelikler** altında **Öznitelik meta verileri ayarla**'yı seçin. Görüntülenebilir ve daraltılabilir olması gereken öznitelikleri seçmek için, ilişkili kataloğa özgü gezinti hiyerarşisinde bir kategori seçin ve sonra **Katalog ürün öznitelikleri** altında bir öznitelik seçin. Ardından, **Özniteliği kanalda göster**'i seçin. Varsayılan olarak, görüntülenebilir tüm nitelikler de aranabilir. Öznitelikleri isteğe bağlı olarak daraltmak için **Daraltılabilir**'i seçin.

### <a name="validate-the-catalog"></a>Kataloğu doğrulama

Yeni kataloğun kullanılabilmesi için doğrulanması ve yayımlanması gerekir.

Kataloğu doğrulamak için aşağıdaki adımları izleyin.

1. **Tüm kataloglar** sayfasının **Kataloglar** sekmesinde **Doğrula** altında doğrulama çalıştırmak için **Katalogları doğrula**'yı seçin. Bu adım gereklidir. Gerekli kurulumun doğruluğunu teyit eder.
1. Doğrulamanın ayrıntılarını görmek için **Sonuçları görüntüle**'yi seçin. Hatalar varsa, verileri düzeltmeniz ve doğrulama sonucu başarılı olana kadar doğrulamayı yeniden çalıştırmanız gerekir.

> [!NOTE]
> **Katalog türü = B2B** ise ve kataloğa POS mağazası veya çağrı merkezi eklediyseniz doğrulama başarısız olur. B2B katalogları ile yalnızca B2B çevrimiçi kanalları ilişkilendirilmiş olmalıdır. B2B kataloğu ile ilişkili müşteri hiyerarşisi olmaması durumunda da doğrulama başarısız olur. 

### <a name="approve-the-catalog"></a>Kataloğu onayla

Katalog doğrulandıktan sonra onaylanması gerekir.

Katalog onay iş akışını başlatmak için aşağıdaki adımları izleyin.

1. **Tüm kataloglar** sayfasının eylem bölmesinde, **İş akışı \> Gönder**'i seçin.
1. Adımları ve iş akışıyla ilgili yetkili kullanıcıları yapılandırmak için **Retail ve Commerce \> Yönetim merkezi kurulumu \> Commerce iş akışları**'na gidin. İş akışı, kataloğu bir **Onaylandı** durumuna geçirmek için gereken adımları tanımlar.

### <a name="publish-the-catalog"></a>Kataloğu yayınlayın

Katalog **Onaylanmış** duruma geçtikten sonra, **Kataloglar** menüsünden **Yayınla**'yı seçerek yayımlayabilirsiniz. Katalog **Yayımlandı** durumuna geçtikten sonra, çağrı merkezi sipariş girişinde ve katalog gönderme işlemlerinde kullanılabilir. Kataloğu el ile veya bir toplu işlem kullanarak yayımlayabilirsiniz. Katalog için tanımladığınız yürürlülük tarihi, ürünlerin çevrimiçi mağazada ne zaman kullanılabileceğini belirler. Tanımladığınız bitiş tarihi, ürünlerin çevrimiçi mağazadan ne zaman kaldırılacağını belirler.

> [!NOTE]
> Uyarıları olan ürünleri içeren bir katalog yayımlayabilirsiniz. Ancak, bu ürünler çevrimiçi mağazada görünmeyecek.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B özelleştirmeleri için Commerce kataloglarının genişletilebilirlik etkisi](catalogs-b2b-sites-dev.md)

[B2B için Commerce katalog hakkında SSS](catalogs-b2b-sites-FAQ.md)

[Katalog seçicisi modülü](catalog-picker.md)
