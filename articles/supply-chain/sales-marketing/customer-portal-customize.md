---
title: Müşteri portalını özelleştirme ve kullanma
description: Bu makale, müşteri portalının sisteminize eklendikten sonra nasıl özelleştirileceğini açıklamaktadır.
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85ec4beda2efe62ff5076a5ed694efbc47c6d87f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878888"
---
# <a name="customize-and-use-the-customer-portal"></a>Müşteri portalını özelleştirme ve kullanma

[!include [banner](../includes/banner.md)]


Bu makalede, kutudan bulunmayan farklı sayfalar müşteri portalında açıklanmıştır. Sayfaların ne yaptığını ve bunları nasıl özelleştirebileceğinizi açıklar.

Müşteri Portalı birkaç Web sayfası ve kutudan birinin dışında bir eylem sunar. Aşağıdaki site haritası bu Web sayfalarının ve eylemlerin genel görünümünü ve eylemleri gerçekleştirebilecek rolleri sağlar.

![Müşteri Portalı site haritası.](media/customer-portal-site-map.png "Müşteri Portalı site haritası")

## <a name="typical-customizations"></a>Normal özelleştirmeler

Aşağıdaki makaleler Power Apps portalların ve portalların nasıl özelleştirilebileceği hakkında temel bilgileri öğrenmenize yardımcı olur:

- [Şablonlarla çalışma](/powerapps/maker/portals/work-with-templates) – Bu makalede, Power Apps portalların nasıl çalıştığı ve portallardaki basit özelleştirmelerin nasıl yapılacağı ile ilgili genel bir bakış sunulmaktadır.
- [Portal içeriğini yönetme](/dynamics365/portals/manage-portal-content) – Bu makale, portalınızda yüzeyiniz içeriği nasıl yöneteceğinizi ve özelleştirebileceğinizi açıklamaktadır.
- [CSS Düzenle](/powerapps/maker/portals/edit-css) – Bu makale, portalınızdaki Kullanıcı arabirimi (UI) için daha karmaşık özelleştirmeler yapmanıza yardımcı olur.
- [Portalınız için bir tema oluşturun](/dynamics365/portals/create-theme) – Bu makale, portalınız için bir UI teması oluşturmanıza yardımcı olur.
- [Portal içeriğini kolayca oluşturma ve gösterme](/dynamics365/portals/create-expose-portal-content): Bu makale, portalınız için kullandığınız temel verileri ve tabloları yönetmenize yardımcı olur.
- [Bir ilgili kişiyi portalda kullanılmak üzere konfigüre etme](/powerapps/maker/portals/configure/configure-contacts) – Bu makale Kullanıcı rollerinin nasıl oluşturulacağını ve özelleştirileceğini ve güvenlik ve kimlik doğrulamanın Power Apps portalda nasıl çalıştığını açıklamaktadır.
- [Tablo formları ve portallardaki Web formları için notları yapılandırma](/powerapps/maker/portals/configure-notes): Bu makale, portala nasıl belge ve ek depolama alanı ekleneceğini açıklamaktadır.
- [Portal Web sitesi için hata işleme](/powerapps/maker/portals/admin/view-portal-error-log) – Bu makale, portal hata günlüklerinin nasıl görüntüleneceğini ve bunları Microsoft Azure BLOB depolama hesabınızda nasıl depolayabileceğinizi açıklamaktadır.

## <a name="customize-the-order-creation-process"></a>Sipariş oluşturma işlemini Özelleştir

Bir kullanıcı müşteri portalını kullanarak sipariş gönderdiğinde, sipariş ilgili Dynamics 365 Supply Chain Management ortamla otomatik olarak eşitlenir. Kullanıcı harici bir müşteri olduğu için, gerekli bazı bilgiler kasıtlı olarak kendi kendine gizlenir. Bu bilgiler form gönderildiğinde otomatik olarak doldurulacaktır.

Bu bölüm, ilgili kişilerin hataları önlemek amacıyla nasıl ayarlanacağını gösterir. Otomatik olarak ayarlanan alanları ve gerekiyorsa bu alanların değerini nasıl değiştirebileceğinizi açıklar.

### <a name="the-out-of-box-order-creation-process"></a>Kullanıma hazır sipariş oluşturma işlemi

Müşteri portalından sipariş gönderme standart adımları aşağıda verilmektedir.

1. Giriş sayfasında, **Sipariş Oluştur** Sihirbazını açmak için **sipariş oluştur** kutucuğunu seçin.
1. **Sipariş bilgileri** sayfasında, aşağıdaki alanları ayarlayın:

    - **Talep edilen giriş tarihi** – teslimat tarihini belirtin.
    - **Teslimat adresi** – Siparişin teslim edileceği adresi girin.
    - **Şirket** -Müşteri şirketin adını seçin. Bu alan yönetici olmayan kullanıcılar için otomatik olarak ayarlanır.
    - **Talep numarası** – Siparişin talep numarasını girin. Bu alanın doldurulması zorunlu değildir.
    - **Sevkiyat ülkesi/bölgesi** – Maddelerin teslim edileceği ülkeyi veya bölgeyi girin. Bu alan yönetici olmayan kullanıcılar için otomatik olarak ayarlanır.

    ![Sipariş Bilgileri sayfası.](media/customer-portal-order-information.png "Sipariş Bilgileri sayfası")

1. **Sonraki**'yi seçin.
1. **Öğeler** sayfasında **Öğe Ekle**'yi seçin.

    ![Öğeler sayfası.](media/customer-portal-items.png "Öğeler sayfası")

1. **Öğe bilgileri** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Ürün adı** - Siparişe eklenecek bir ürün bulun ve seçin.
    - **Miktar** - Seçili ürünün miktarını girin.
    - **Birim** – ölçü birimini belirtin (örneğin, **EA.**, **kgs** veya **kutu**).
    - **Tahmini Net tutar** – değer, maddenin tahmini fiyatı olarak seçilen birimin miktarını × olarak hesaplanır.

    ![Öğe Bilgileri iletişim kutusu.](media/customer-portal-item-information.png "Öğe Bilgileri iletişim kutusu")

1. Siparişineöğe eklemek için **Gönder**'i seçin.
1. Sipariş vermek istediğiniz tüm öğeleri ekleyinceye kadar 4 ile 6 arasındaki adımları yineleyin.
1. Öğeleri eklemeyi bitirdiğinizde, **öğeler** sayfasında **ileri** 'yi seçin.
1. **Sipariş bilgileri** sayfası siparişin özetini sağlar. Sipariş içeriğini ve teslimat ayrıntılarını gözden geçirin. Her şey doğru görünüyorsa, siparişi göndermek için **Gönder** 'i seçin.

    ![Tamamlanan sipariş Bilgileri sayfası.](media/customer-portal-order-submit.png "Tamamlanna sipariş Bilgileri sayfası")

### <a name="standard-data-setup"></a>Standart veri ayarlama

Sorunsuz bir kullanıcı deneyiminin sağlanmasına yardımcı olmak için, müşteri portalı gerekli birkaç alana ait değerleri otomatik olarak doldurur. Bu değerler siparişi gönderen müşterinin ilgili kişi kaydındaki bilgileri temel alınır.

Siparişleri göndermek için müşteri portalını kullanacak bir müşteriye ait her [ilgili kişi satırı](/powerapps/maker/portals/configure/configure-contacts) için, aşağıdaki gerekli alanlar için değerlerin belirtilmesi gerekir. Aksi takdirde, hatalar oluşur.

- **Şirket** – Siparişin ait olduğu yasal varlık
- **Olası müşteri** - Siparişle ilişkilendirilen müşteri hesabı.
- **Fiyat listesi** – Müşteri için özel fiyat listesi
- **Para birimi** – Fiyatın para birimi
- **Sevkiyat ülkesi/bölgesi** – Maddelerin teslim edileceği ülkeyi veya bölge

Satış siparişi tablosu için aşağıdaki alanlar otomatik olarak ayarlanır:

- **Dil** – Siparişin dili (varsayılan olarak, değer, ilgili kişi kaydından alınır.)
- **Sevkiyat ülkeye/bölgeye** - Maddelerin teslim edileceği ülke veya bölge (varsayılan olarak, değer ilgili kişi kaydından alınır.)
- **İlgili kişi** - Sipariş hakkında bilgi için iletişim kurulabilecek Kullanıcı (varsayılan olarak, değer ilgili kişi kaydından alınır.)
- **Şirket** – Siparişin ait olduğu yasal varlık (varsayılan olarak, değer ilgili kişi kaydından alınır.)
- **Potansiyel müşteri** -Siparişle ilişkilendirilmiş müşteri hesabı (varsayılan olarak, değer, ilgili kişi kaydından alınır.)
- **Fatura müşterisi** -Siparişle ilişkilendirilmiş faturaladırma hesabı (Varsayılan değer, ilgili kişi kaydından olası müşteridir.)
- **Satış siparişi adı** – Satış siparişinin adı (varsayılan değer **Satış siparişi**.)
- **Para birimi** – Fiyat para birimi (varsayılan olarak, değer, ilgili kişi kaydından alınır.)
- **Fiyat listesi** – Müşteri için özel fiyat listesi (varsayılan olarak, değer, ilgili kişi kaydından alınır).
- **Teslimat adresi açıklaması** – Satış siparişinin teslimat adresi (varsayılan değer **Teslimat adresi açıklamasıdır**.)

### <a name="modify-the-order-creation-process"></a>Sipariş oluşturma işlemini değiştirme

Temel sipariş oluşturma sürecini değiştirmezseniz, müşteri portalının görünümünü ve Kullanıcı arabirimini serbestçe değiştirebilirsiniz. Sipariş oluşturma sürecini değiştirmek istiyorsanız, aklınızda tutmanız gereken birkaç nokta vardır.

Aşağıdaki sütunların çift yazılır olarak satış siparişi oluşturması gerektiğinden bu sütunları Microsoft Dataverse'teki satış siparişi tablosundan bu sütunları silmeyin:

- **Şirket** – Siparişin ait olduğu yasal varlık
- **Ad** - Satış siparişi adı
- **Para birimi** – Fiyatın para birimi
- **Fiyat listesi** – Müşteri için özel fiyat listesi
- **Sevkiyat ülkesi/bölgesi** – Maddelerin teslim edileceği ülkeyi veya bölge
- **Olası müşteri** - Siparişle ilişkilendirilen müşteri hesabı.
- **Dil** – Siparişin dili (genellikle, bu dil potansiyel müşterinin dilidir.)
- **Teslimat adresi açıklaması** – Satış siparişinin teslimat adresi

Maddeler için aşağıdaki sütunlar gereklidir:

- **Ürün** - Sipariş ürünü
- **Miktar** - Seçili ürünün miktarı
- **Birim** – ölçü birimini (örneğin, **EA.**, **kgs** veya **kutu**)
- **Sevkiyat ülkesi/bölgesi** – Ülke veya teslimat bölgesi
- **Teslimat adresi açıklaması** – Siparişinin teslimat adresi

Müşteri portalınızın tüm bu sütunlar için değer gönderdiğinden emin olmanız gerekir.

Sayfaya sütun eklemek veya sütunları kaldırmak istiyorsanız bkz. [Kolaylaştırılmış bir veri girişi deneyimi için hızlı kayıt formları oluşturma veya düzenleme](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Sütunların önceden belirlenme şeklini ve bu sayfa kaydedildiğinde değerlerin nasıl ayarlanacağını değiştirmek istiyorsanız Power Apps portal belgelerinde aşağıdaki bilgileri inceleyin:

- [Önceden doldurulan alan](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Kaydederken değeri ayarla](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Giriş sayfasını Özelleştir

Müşteri Power Apps portalındaki tüm kontroller yerleşik Portal denetimleridir. Bunları, Power Apps Portal belgelerinde [sayfa oluşturma](/powerapps/maker/portals/compose-page) içindeki adımları izleyerek özelleştirebilirsiniz.

Ana sayfada kutucukları oluşturmak için müşteri portalı şablonunda bulunan tek özel kontrol kullanılır.

![Giriş sayfasındaki kutucuklar.](media/customer-portal-home-page-tiles.png "Giriş sayfasındaki kutucuklar")

Kutucukları değiştirmek için aşağıdaki adımları izleyin.

1. [Portal Yönetimi uygulamasını](/powerapps/maker/portals/configure/configure-portal) açın.
1. Soldaki gezinti bölmesinde **Sayfa Şablonları**'nı seçin.

    ![Portal Yönetimi gezinti bölmesi.](media/customer-portal-nav.png "Portal Yönetimi gezinti bölmesi")

1. **Giriş** adlı bir sayfa şablonu seçin.
1. **Web şablonu** alanında, ilgili sayfanın kaynak kodunu açmak için **giriş** bağlantısını seçin.

    ![Web şablonu alanı.](media/customer-portal-web-template.png "Web şablonu alanı")

1. Artık giriş sayfasının tüm kaynak kodunu görmelisiniz ve bunu gereksinim duyduğunuz gibi değiştirebilirsiniz.

## <a name="resources"></a>Kaynaklar

Müşteri portalını nasıl ayarlayabileceğinizi ve özelleştirebileceğinizi öğrenmek için aşağıdaki kaynaklara bakın:

- [Power Apps portal belgeleri](/powerapps/maker/portals/overview)
- [Çift yazma belgeleri](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Portal yaşam döngüsü hakkında](/powerapps/maker/portals/admin/portal-lifecycle)
- [Bir portalı yükselt](/powerapps/maker/portals/admin/upgrade-portal)
- [Portal konfigürasyonu geçir](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Çözüm yaşam döngüsü yönetimi: Customer Engagement için Dynamics 365 uygulamaları](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]