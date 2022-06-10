---
title: B2B siteleri için ticari Katalog oluştur
description: Bu konuda, Microsoft Dynamics 365 Commerceişletmeden işletmeye (B2B) siteleri için Commerce katalogları oluşturma açıklanmaktadır.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7382062706c2de01c499ee05aeb0b45ff6fb37cb
ms.sourcegitcommit: bca0cb730307948368a9aabe322cf963688ed8b1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782849"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>B2B siteleri için ticari Katalog oluştur

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerceişletmeden işletmeye (B2B) siteleri için Commerce ürün katalogları oluşturma açıklanmaktadır. B2B siteleri ile ilgili Commerce katalogları hakkında sık sorulan soruların yanıtları için, bkz. [B2B için Commerce katalogları SSS](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Bu konu, Dynamics 365 Commerce sürüm 10.0.27 ve sonraki sürümler için geçerlidir.

B2B çevrimiçi mağazalarınızda sunmak istediğiniz ürünleri belirlemek için Commerce kataloglarını kullanabilirsiniz. Bir katalog oluşturduğunuzda, ürünlerin sunulduğu çevrimiçi mağazaları tanımlar, dahil etmek istediğiniz ürünleri eklersiniz ve ticari satış ayrıntıları ekleyerek ürün tekliflerini geliştirebilirsiniz. Her B2B çevrimiçi deposu için birden çok katalog oluşturabilirsiniz.

Commerce ürün katalogları aşağıdaki bilgileri tanımlamanızı sağlar:

- **Kataloğa özgü gezinti hiyerarşisi** – Kuruluşlar, belirli kataloglarında ayrı bir kategori yapısı oluşturabilir.
- **Kataloğa özel öznitelik meta verileri** – Öznitelikler bir ürünle ilgili ayrıntıları içerir. Bir gezinti hiyerarşisinin kategorisine öznitelik atayarak, o kategoriye atanan ürün düzeyinde o nitelikler için değerler tanımlayabilirsiniz. Kuruluşlar ardından şu görevleri tamamlayabilir:

    - Kataloğa özel öznitelik değerleri tanımlayın.
    - Katalog düzeyindeki özniteliklerin görünürlüğünü kontrol edin.
    - Tek bir kataloğa özel iyileştiricileri seçin.

- **Kanallar** – Kuruluşlar, bir katalogla birden fazla B2B çevrimiçi kanalını ilişkilendirebilir. Kataloglar için uçtan uca destek şu anda yalnızca B2B çevrimiçi mağazalarda kullanılabilir.
- **Müşteri hiyerarşileri** – Belirli bir B2B kanalı için kuruluşlar, müşteri hiyerarşilerini bu katalogla ilişkilendirerek, seçilen B2B ortakları için kullanılabilir bir kataloğu yapabilirler.
- **Fiyat grupları** – Belirli bir kataloğa özgü fiyatları ve yükseltmeleri konfigüre edebilirsiniz. Bu özellik, bir B2B kanalına yönelik kataloğun tanımlanması için temel bir nedendir. Katalogların fiyat grupları, kuruluşların, ürünleri amaçlanan B2B organizasyonlarına kullanabilmesini ve tercih edilen fiyatlarını ve iskontolarını uygulamasını sağlar. Konfigüre edilen bir katalogdan sipariş veren B2B müşteriler, Commerce B2B sitesinde oturum açtıktan sonra özel fiyat ve promosyonlardan yararlanabilir. Kataloğa özel fiyatları yapılandırmak için **Kataloglar** sekmesindeki **Fiyat grupları**'ni belirleyerek kataloğa bir veya daha fazla fiyat grubu bağlayın. Müşteriler bu katalogdan sipariş verdiği zaman, aynı fiyat grubuna bağlı tüm ticari sözleşmeler, fiyat ayarlaması günlükleri ve gelişmiş indirimler uygulanır. (Gelişmiş indirimler eşik, miktar ve karıştır ve eşle iskontolarını içerir.) Fiyat grupları hakkında daha fazla bilgi için bkz. [Fiyat grupları](price-management.md#price-groups).

> [!NOTE]
> Bu özellik Dynamics 365 Commerce 10.0.27 sürümünden itibaren mevcuttur. Gezinti merkezleri ve müşteri hiyerarşisi gibi kataloğa özgü yapılandırmaları konfigüre etmek için, Commerce yönetim merkezinde, **Özellik yönetimi** çalışma alanını açın (**Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**), **Perakende kanallarda çoklu katalog kullanımını etkinleştir** özelliğini etkinleştirin ve sonra **1110 CDX** işini çalıştırın.

## <a name="catalog-process-flow"></a>Katalog işleme akışı

Katalog oluşturma ve işleme işleminde dört genel adım vardır. Her adım, sonraki bölümde ayrıntılı olarak açıklanmıştır.

1. **[Yapılandırma](#configure-the-catalog)**

    - Gezinti hiyerarşisini ilişkilendirin.
    - Uygulanabilir olmaları halinde, süre ve geçerlilik bitiş tarihlerini belirtin.
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

Commerce yönetim merkezinde, katalog yapılandırmak için **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin.

Yeni bir katalog oluştururken önce kataloğu bir veya daha fazla kanalla ilişkilendirmeniz gerekir. Katalog oluştururken yalnızca seçtiğiniz kanal [ürün çeşitlerine](/dynamics365/unified-operations/retail/assortments) bağlı maddeler kullanılabilir. Kataloğu bir veya daha fazla kanalla ilişkilendirmek için, **Katalog kurulumu** sayfasının **Commerce kanalları** hızlı sekmesinde **Ekle**'yi seçin.

#### <a name="associate-the-navigation-hierarchy"></a>Gezinti hiyerarşisini ilişkilendirin

Kataloğa ürünler eklemek için bir gezinme hiyerarşisi seçilmelidir. Gezinme hiyerarşisi, katalog için kategori yapısını destekler. **Katalog kurulumu** sayfasındaki **Commerce kanalları** hızlı sekmesinde seçili kanallarla ilişkili gezinme hiyerarşilerinden birini seçmeniz gerekir. Bir varsayılan gezinti hiyerarşisini kanallarınızla ilişkilendirmek için, **Retail ve Commerce \> Kanal kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.

#### <a name="specify-time-effective-and-expiration-dates"></a>Yürürlük ve bitiş tarihlerini belirtin

Kataloğa ilişkin başlangıç ve sona erme tarihleri belirtmek için, ana katalog başlık görünümüne dönmek üzere katalog hiyerarşisinin en üst düğümünü seçin. Ardından, **Genel** hızlı sekmesinde, başlangıç ve bitiş tarihlerini gerekli şekilde yapılandırın.

#### <a name="add-and-categorize-products"></a>Ürün ekleyin ve kategorilendirin

Commerce yönetim merkezinde, kataloğa eklenecek ürünleri yapılandırmak için **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Sonra, **Kataloglar** sekmesinde **Ürün ekle**'yi seçin.

Alternatif olarak, gezinti hiyerarşisinde bir düğüm seçin. Böylece, katalogdaki bir kategoriye doğrudan ürün ekleyebilirsiniz.

#### <a name="associate-price-groups"></a>Fiyat gruplarını ilişkilendirin

Kataloğa özel fiyatlar konfigüre etmek için kataloğa bir veya daha fazla fiyat grubu bağlamanız gerekir. Commerce yönetim merkezinde, fiyat gruplarını bir katalog ile ilişkilendirmek için **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde **Fiyatlandırma** altında **Fiyat grupları**'nı seçin. Müşteriler bu katalogdan sipariş verdiği zaman, aynı fiyat grubuna bağlı tüm ticari sözleşmeler, fiyat ayarlaması günlükleri ve perakende gelişmiş indirimleri (eşik değeri, miktar ve karma ve eşleşme indirimleri) uygulanır.

Fiyat grupları hakkında daha fazla bilgi için bkz. [Fiyat grupları](price-management.md#price-groups).

> [!NOTE]
> **Tüm kataloglar** sayfasından yeni bir fiyat grubu oluşturamazsınız. Bunun yerine, bunu **Tüm fiyat grupları** sayfasından oluşturmanız gerekir. **Tüm kataloglar** sayfasındaki katalogla ilişkilendirmelisiniz.

#### <a name="associate-a-customer-hierarchy"></a>Müşteri hiyerarşisi ile ilişkilendirme

Commerce yönetim merkezinde, müşteri hiyerarşileri ilişkilendirmek için **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde, **Müşteri hiyerarşisi** altında kataloğa bir veya daha fazla müşteri hiyerarşisi bağlamak için **Hiyerarşileri ata**'yı seçin.

> [!NOTE]
> **Tüm kataloglar** sayfasından yeni bir müşteri hiyerarşisi oluşturamazsınız. Bunun yerine, bunu **Müşteri hiyerarşileri** sayfasından oluşturmanız gerekir. **Tüm kataloglar** sayfasındaki katalogla ilişkilendirmelisiniz.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Boyut, stil ve renk gibi iyileştiriciler için varsayılan boyut öznitelik grubunu ilişkilendirin

Boyut, stil ve renk gibi iyileştiriciler için varsayılan bir boyut öznitelik grubunu Commerce yönetim merkezinde ilişkilendirmek üzere, **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde **Öznitelikler** altında **Öznitelik grupları**'nı seçin.

#### <a name="set-attribute-metadata"></a>Öznitelik meta verileri ayarla

Commerce yönetim merkezinde, öznitelik meta verilerini yapılandırmak için **Retail ve Commerce \> Kataloglar ve sınıflamalar \> Tüm kataloglar**'a gidin. Ardından, **Kataloglar** sekmesinde **Öznitelikler** altında **Öznitelik meta verileri ayarla**'yı seçin. Görüntülenebilir ve daraltılabilir olması gereken öznitelikleri seçmek için, ilişkili kataloğa özgü gezinti hiyerarşisinde bir kategori seçin ve sonra **Katalog ürün öznitelikleri** altında bir öznitelik seçin. Ardından, **Özniteliği kanalda göster**'i seçin. Varsayılan olarak, görüntülenebilir tüm nitelikler de aranabilir. Öznitelikleri isteğe bağlı olarak daraltmak için **Daraltılabilir**'i seçin.

### <a name="validate-the-catalog"></a>Kataloğu doğrulama

Yeni kataloğun kullanılabilmesi için doğrulanması ve yayımlanması gerekir.

Kataloğu doğrulamak için aşağıdaki adımları izleyin.

1. **Tüm kataloglar** sayfasının **Kataloglar** sekmesinde **Doğrula** altında doğrulama çalıştırmak için **Katalogları doğrula**'yı seçin. Bu adım gereklidir. Gerekli kurulumun doğruluğunu teyit eder.
1. Doğrulamanın ayrıntılarını görmek için **Sonuçları görüntüle**'yi seçin. Hatalar varsa, verileri düzeltmeniz ve doğrulama sonucu başarılı olana kadar doğrulamayı yeniden çalıştırın.

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
