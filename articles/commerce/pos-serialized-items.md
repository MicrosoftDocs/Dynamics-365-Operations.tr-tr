---
title: POS'ta seri hale getirilmiş maddelerle çalışma
description: Bu konu, satış noktası (POS) uygulamasında serileştirilmiş maddelerin nasıl yönetileceğini açıklar.
author: boycezhu
manager: annbe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eedb64ae04345cb94bdd8cc68de833cfcfd40119
ms.sourcegitcommit: 39981582778b0a62567324452485a6721ca18284
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2020
ms.locfileid: "3407510"
---
# <a name="work-with-serialized-items-in-the-pos"></a>POS'ta seri hale getirilmiş maddelerle çalışma

[!include [banner](includes/banner.md)]

Birçok perakendeci seri denetim gerektiren ürünler satar. Bu maddelere, *serileştirilmiş öğeler* adı verilir. Bazı perakendeciler, izleme amacıyla seri numaraları tutmak isteyebilir. Diğer perakendeciler, satış işlemi sırasında servis ve garanti amacıyla seri numaralarını yakalamak isteyebilir. Bu konu, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında serileştirilmiş maddelerin nasıl yönetileceğini açıklar.

## <a name="serial-number-configurations"></a>Seri numarası yapılandırmaları

Madde, seri numaralar için izin vermek üzere ayarlanmış bir izleme boyutu grubu atanmışsa, serileştirilmiş bir madde olarak kabul edilir. Commerce Headquarters'ta, **İzleme boyutu grupları** sayfasında, stok işlemi için seri numaraları etkinleştirmek üzere **Etkin** seçeneğini seçin. Satış işlemi için seri numaralarını etkinleştirmek üzere **Satış işleminde etkin** seçeneğini belirleyin.

**İzleme boyutları** hızlı sekmesinde, **Boş giriş izni** seçeneği açıksa, stok giriş işlemi sırasında seri numarası isteğe bağlı bir giriştir. Bu seçenek kapalıysa, seri numarası gereklidir.

**Seri numaraları** hızlı sekmesinde, **Seri numarası denetimi** seçeneği açıksa, seri numarası her birim için benzersiz olmalıdır. Başka bir deyişle, yinelenen seri numaralarına izin verilmez.

## <a name="serialized-items-in-the-receiving-process"></a>Teslim alma işlemindeki serileştirilmiş maddeler

POS uygulamasındaki **Gelen stok** işlemi kullanıcıların serileştirilmiş maddeler için aşağıdaki görevleri gerçekleştirmesini sağlar:

- Maddeler mağazada satınalma siparişi aracılığıyla alındığında, seri numaraları serileştirilmiş maddelere göre kaydedin.
- Maddeler mağazada satınalma siparişi veya transfer emri aracılığıyla alındığında, öncedem kaydedilmiş seri numaralarını serileştirilmiş maddelere göre kaydedin.

> [!NOTE]
> Serileştirilmiş bir maddeyi kaydetmek veya doğrulamak için **Gelen stok** işlemini kullanmak üzere, maddeye **Etkin** seçeneği için (**Satış işlemindeetkin** seçeneği değil) seri numaralarına izin vermek üzere ayarlanmış bir izleme boyutu grubu atanması gerekir.

Teslim alma işlemine başlamak için, **Gelen stok** işleminde, madde barkodunu tarayarak veya madde kodunu girerek **Şimdi alınıyor** görünümünde başlatabilirsiniz. Alternatif olarak, maddeyi el ile seçerek **Tam sipariş listesi** görünümünde başlatabilirsiniz.

Seçilen veya alınan madde serileştirilmiş bir madde ise, maddenin **Ayrıntılar** bölmesi **Seri numarası yönetimi** sayfasını açan bir **Seri numarasını yönet** bağlantısı içerir. Alternatif olarak, **Seri numarası yönetimi** sayfasını sipariş ayrıntıları görünümünün uygulama çubuğunda **Seri numarası**'nı seçerek veya teslim alma işlemi sırasında istemde bulunan iletişim kutusunda **Seri numarasını yönet**'i seçerek açabilirsiniz. **Seri numarası yönetimi** sayfası, kayıt veya doğrulama için bekleyen tüm açık seri numarası satırlarını listeler. Bu sayfada iki sekme olabilir: biri geçerli madde, diğeri de siparişteki serileştirilmiş maddeler için.

**Seri numarası yönetimi** sayfasındaki **Durum** alanı her seri numarasının bulunduğu geçerli aşama hakkında bilgi sağlar:

- **Kayıtlı değil** – Seri numarası sağlanmadı veya önceden kaydedilmiş seri numarası henüz doğrulanmadı.
- **Kaydediliyor** - Seri numarası kaydedildi ve mağazanın kanal veritabanına yerel olarak kaydedildi veya önceden kaydedilmiş seri numarası doğrulandı. Yalnızca **Kaydediliyor** durumuna sahip seri numaraları teslim alma işlemini tamamladığınızda Commerce Headquarters'a gönderilir.

### <a name="register-serial-numbers-against-serialized-items"></a>Seri numaraları serileştirilmiş maddelere göre kaydetme

Satınalma siparişi için, serileştirilmiş maddeyi teslim alma işlemi sırasında istemde bulunan bir iletişim kutusu **Seri numarasını yönet** seçeneğini sunar. **Seri numarası yönetimi** sayfasını açmak ve seri numaralarını kaydetmeye başlamak için bu seçeneği belirleyebilirsiniz. Ayrıca, teslim alma işlemi sırasında bu adımı atlayabilir ve girişi daha sonra, giriş deftere nakledilmeden önce sağlayabilirsiniz.

Varsayılan olarak, geçerli maddenin sekmesi gösterilir. Tüm seri numara satırlarında boş seri numarası değeri bulunur ve durum **Kayıtlı değil**'dir. Seri numarası barkodlarını taratabilir veya  iletişim kutusuna devamlı olarak seri numaralarını girmek için uygulama çubuğunda **Seri numarası**'nı seçebilirsiniz. Girdiğiniz seri numaraları listede görünür ve seri numarası satırlarının durumu **Kaydediliyor** olarak değiştirilir. Listeye kaydedebileceğiniz maksimum seri numarası sayısı, teslim alma miktarına eşittir. Hata yaparsanız, girdiğiniz seri numaralarda değişiklik yapmak için **Ayrıntılar** bölmesinde **Düzenle** veya **Temizle**'yi seçebilirsiniz.

Ayrıca, **Seri numarası yönetimi** sayfasının **Tüm serileştirilmiş maddeler** sekmesine seri numaraları kaydedebilirsiniz. Listede, seri numaralarını kaydetmek istediğiniz maddeyi seçin.

Bu sayfada seri numarası kaydı sırasında, yineleme doğrulaması gerçekleşir. Seri numarası denetiminin açık olduğu bir maddeye karşılık yinelenen bir seri numarası girmeyi denerseniz, bir hata iletisi alırsınız ve farklı bir numara girmeniz gerekir.

### <a name="validate-serial-numbers-on-serialized-items"></a>Serileştirilmiş maddelerdeki seri numaralarını doğrulama

Transfer emri için, çıkış tarafının sevkiyat işlemi sırasında serileştirilmiş maddelerin seri numaralarını önceden işlemesi gerekir. Satınalma siparişi için tedarikçi bir Ön Sevkiyat Bildirimi (ÖSB) aracılığıyla seri numarası bilgilerini sağlayabilir ve sevk edilecek maddedeki numaraları önceden kaydedebilirsiniz. Her iki durumda da, seri numaraları girişten önce bilinir. Bu nedenle, gelen tarafta, yalnızca almanız beklenenleri aldığınızı doğrulamanız gerekir.

Seri numaralarını doğrulamak için, teslim alma işlemi sırasında veya giriş deftere nakledilmeden önce istediğiniz zaman **Seri numarası yönetimi** sayfasını açabilirsiniz. Seri numaraları önceden kaydedilmiş olan her serileştirilmiş madde için, tüm seri numaraları otomatik olarak bu sayfadaki **Kayıtlı değil** başlangıç durumunda ayarlanır. Seri numaralarını doğrulamak için, onları tarayabilir veya girebilirsiniz. Seri numarası girildiğinde, uygulama girilen numaranın önceden kaydedilmiş seri numaralarıyla eşleşip eşleşmediğini doğrular. Eşleşiyorsa, durum **Kaydediliyor** olarak değiştirilir. Aksi halde, bir hata iletisi alırsınız. Listede doğrulayabileceğiniz maksimum seri numarası sayısı, teslim alma miktarına eşittir.

Ayrıca, **Seri numarası yönetimi** sayfasının **Tüm serileştirilmiş maddeler** sekmesinde seri numaralarını doğrulayabilirsiniz. Listede, seri numaralarını doğrulamak istediğiniz maddeyi seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[POS'ta gelen stok işlemi](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
