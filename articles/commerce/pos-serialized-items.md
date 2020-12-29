---
title: POS'ta seri hale getirilmiş maddelerle çalışma
description: Bu konu, satış noktası (POS) uygulamasında serileştirilmiş maddelerin nasıl yönetileceğini açıklar.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416539"
---
# <a name="work-with-serialized-items-in-the-pos"></a>POS'ta seri hale getirilmiş maddelerle çalışma

[!include [banner](includes/banner.md)]

Birçok perakendeci seri denetim gerektiren ürünler satar. Bu ürünlere, *serileştirilmiş öğeler* adı verilir. Bazı perakendeciler, izleme amacıyla mağaza veya ambar stokunda seri numaraları tutmak isteyebilir. Diğer perakendeciler, satış işlemi sırasında servis ve garanti amacıyla seri numaralarını yakalamak isteyebilir. Bu konu, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında serileştirilmiş maddelerin nasıl yönetileceğini açıklar.

## <a name="serial-number-configurations"></a>Seri numarası yapılandırmaları

Madde; seri numaralar için izin vermek üzere ayarlanmış bir izleme boyutu grubu atanmışsa, serileştirilmiş bir madde olarak kabul edilir. Commerce yönetim merkezinde, **Boyut gruplarını izleme** sayfasında, stok işlemi için seri numaraları etkinleştirmek üzere **Etkin** seçeneğini belirleyin veya satış işleminin seri numaralarını etkinleştirmek için **Satış işlemi içinde etkin** seçeneğini belirleyin.

**İzleme boyutları** hızlı sekmesinde, serileştirilmiş maddenin stok giriş işlemi sırasında seri numarasının isteğe bağlı giriş olmasına izin vermek için **Boş giriş izni** parametresini açın. Bu parametrenin kapatılması seri numarasının gerekli bir giriş olmasını uygular. Benzer şekilde, **İzin verilen boş çıkış** parametresi, stok sevkiyat işlemi sırasında seri numarasının gerekli olup olmayacağını kontrol eder.

> [!NOTE]
> Seri numaralarını serileştirilmiş bir madde için kaydetmek veya doğrulamak için **Gelen stok** ve **Çıkan stok** POS işlemlerini kullanmak üzere, **Etkin** seçeneği için (**Satış sürecinde etkin** seçeneği değil) seri numaralarına izin vermek üzere ayarlanmış bir izleme boyutu grubu atamak üzere maddeyi yapılandırmanız gerekir.

## <a name="serial-number-management-page"></a>Seri numarası yönetim sayfası

**Gelen stok** ve **Giden stok** POS işlemlerinde, seçilen, alınan veya sevk edilen madde serileştirilmiş bir madde ise, **Ayrıntılar** bölmesinde madde için seri numaralarını kaydedebileceğiniz veya doğrulayabileceğiniz **Seri numarası yönetim** sayfasına bağlanan bir **Seri numarasını yönet** seçeneği bulunu. Alternatif olarak, **Seri numarası yönetimi** sayfasını sipariş ayrıntıları görünümünün uygulama çubuğunda **Seri numarası** eylemini seçerek veya teslim alma veya sevkiyat işlemi sırasında istemde bulunan iletişim kutusunda **Seri numarasını yönet** öğesini seçerek açabilirsiniz. 

**Seri numarası yönetimi** sayfası, kayıt veya doğrulama için bekleyen tüm açık seri numarası satırlarını listeler. Bu sayfada iki sekme olabilir: biri geçerli madde, diğeri de siparişteki serileştirilmiş maddeler için.

**Seri numarası yönetimi** sayfasındaki **Durum** alanı her seri numarasının bulunduğu geçerli aşama hakkında bilgi sağlar:

- **Kayıtlı değil**: Seri numarası sağlanmadı veya önceden kaydedilmiş seri numarası henüz doğrulanmadı (teslim alma işlemi sırasında).
- **Kaydediliyor** - Seri numarası kaydedildi ve mağazanın kanal veritabanına yerel olarak kaydedildi veya önceden kaydedilmiş seri numarası doğrulandı. Yalnızca **Kaydediliyor** durumuna sahip seri numaraları teslim alma veya karşılama işlemini tamamladığınızda Commerce yönetim merkezine gönderilir.

## <a name="receive-serialized-items"></a>Serileştirilmiş maddeleri alma

**Gelen stok** POS işlemi kullanıcıların serileştirilmiş maddeler için aşağıdaki görevleri gerçekleştirmesini sağlar:

- Maddeler mağazada satınalma siparişi aracılığıyla alındığında, seri numaraları serileştirilmiş maddelere göre kaydedin.
- Maddeler mağazada satınalma siparişi veya transfer emri aracılığıyla alındığında, öncedem kaydedilmiş seri numaralarını serileştirilmiş maddelere göre kaydedin.

### <a name="register-serial-numbers-against-serialized-items"></a>Seri numaraları serileştirilmiş maddelere göre kaydetme

Satınalma siparişi için, serileştirilmiş maddeyi teslim alma işlemi sırasında **Seri numarasını yönet** seçeneğinin bulunduğu bir iletişim kutusu açılır. **Seri numarası yönetimi** sayfasını açmak ve seri numaralarını kaydetmeye başlamak için bu seçeneği belirleyebilirsiniz. Ayrıca, teslim alma işlemi sırasında bu adımı atlayabilir ve girişi daha sonra, giriş deftere nakledilmeden önce sağlayabilirsiniz.

Varsayılan olarak, geçerli maddenin sekmesi gösterilir. Tüm seri numara satırlarında boş seri numarası değeri bulunur ve durum **Kayıtlı değil**'dir. Seri numarası barkodlarını taratabilir veya devamlı olarak seri numaralarını girmek için uygulama çubuğunda **Seri numarası**'nı seçebilirsiniz. Girdiğiniz seri numaraları listede görünür ve durumları **Kaydediliyor** olarak değiştirilir. Listeye kaydedebileceğiniz maksimum seri numarası sayısı, teslim alma miktarına eşittir. Hata yaparsanız, girdiğiniz seri numaralarda değişiklik yapmak için **Ayrıntılar** bölmesinde **Düzenle** veya **Temizle**'yi seçebilirsiniz.

Ayrıca, **Seri numarası yönetimi** sayfasının **Tüm serileştirilmiş maddeler** sekmesine seri numaraları kaydedebilirsiniz. Listede, seri numaralarını kaydetmek istediğiniz maddeyi seçin.

### <a name="validate-serial-numbers-on-serialized-items"></a>Serileştirilmiş maddelerdeki seri numaralarını doğrulama

Transfer emri için, çıkış tarafının sevkiyat işlemi sırasında serileştirilmiş maddelerin seri numaralarını önceden işlemesi gerekir. Satınalma siparişi için tedarikçi bir Ön Sevkiyat Bildirimi (ÖSB) aracılığıyla seri numarası bilgilerini sağlayabilir ve sevk edilecek maddedeki numaraları önceden kaydedebilirsiniz. Her iki durumda da, seri numaraları girişten önce bilinir. Bu nedenle, gelen tarafta, yalnızca almanız beklenenleri aldığınızı doğrulamanız gerekir.

Seri numaralarını doğrulamak için, teslim alma işlemi sırasında veya giriş deftere nakledilmeden önce istediğiniz zaman **Seri numarası yönetimi** sayfasını açabilirsiniz. Seri numaraları önceden kaydedilmiş olan her serileştirilmiş madde için, tüm seri numaraları otomatik olarak bu sayfadaki **Kayıtlı değil** başlangıç durumunda ayarlanır. Seri numaralarını doğrulamak için, onları tarayabilir veya girebilirsiniz. Seri numarası girildiğinde, uygulama girilen numaranın önceden kaydedilmiş seri numaralarıyla eşleşip eşleşmediğini doğrular. Eşleşiyorsa, durum **Kaydediliyor** olarak değiştirilir. Aksi halde, bir hata iletisi alırsınız. Alternatif olarak, doğrudan bir seri numarası seçebilir, daha sonra bu seri numarasını hızlı şekilde doğrulanmış olarak işaretlemek için **Ayrıntılar** bölmesindeki **Seri numarasını doğrula** seçeneğini belirleyebilirsiniz. Listede doğrulayabileceğiniz maksimum seri numarası sayısı, teslim alma miktarına eşittir.

Ayrıca, **Seri numarası yönetimi** sayfasının **Tüm serileştirilmiş maddeler** sekmesinde seri numaralarını doğrulayabilirsiniz. Listede, seri numaralarını doğrulamak istediğiniz maddeyi seçin.

## <a name="ship-serialized-items"></a>Serileştirilmiş maddeleri sevk etme

Transfer emri aracılığıyla geçerli mağaza dışına sevk edildiğinde serileştirilmiş maddeler için seri numaraları kaydetmek için **Çıkan stok** POS işlemini kullanabilirsiniz.

### <a name="register-serial-numbers-against-serialized-items"></a>Seri numaraları serileştirilmiş maddelere göre kaydetme

Transfer emri için, serileştirilmiş maddenin sevkiyatı sırasında **Seri numarasını yönet** seçeneğinin bulunduğu bir iletişim kutusu açılır. **Seri numarası yönetimi** sayfasını açmak ve seri numaralarını kaydetmeye başlamak için bu seçeneği belirleyebilirsiniz. Ayrıca, sevkiyat işlemi sırasında bu adımı atlayabilir ve girişi daha sonra, sevkiyat deftere nakledilmeden önce sağlayabilirsiniz.

Varsayılan olarak, geçerli maddenin sekmesi gösterilir. Tüm seri numara satırlarında boş seri numarası değeri bulunur ve durum **Kayıtlı değil**'dir. Seri numarası barkodlarını taratabilir veya devamlı olarak seri numaralarını girmek için uygulama çubuğunda **Seri numarası**'nı seçebilirsiniz. Girdiğiniz seri numaraları listede görünür ve durumları **Kaydediliyor** olarak değiştirilir. Listeye kaydedebileceğiniz maksimum seri numarası sayısı, sevkiyat miktarına eşittir. Hata yaparsanız, girdiğiniz seri numaralarda değişiklik yapmak için **Ayrıntılar** bölmesinde **Düzenle** veya **Temizle**'yi seçebilirsiniz.

Ayrıca, **Seri numarası yönetimi** sayfasında **Tüm serileştirilmiş maddeler** sekmesine seri numaraları kaydedebilirsiniz. Listede, seri numaralarını kaydetmek istediğiniz maddeyi seçin.

İsteğe bağlı olarak, çıkan transfer emri için seri numarası kaydı sırasında seri numarası kullanılabilirliği doğrulamasını etkinleştirebilirsiniz. Bu doğrulamada, sevkiyat mağazasının envanterinde bulunmayan bir seri numarası sevk etmeye çalışırsanız, bir hata iletisi alırsınız ve farklı bir numara girmeniz gerekir.

Bu tür bir doğrulamayı önkoşul olarak etkinleştirmek için, aşağıdaki işleri yinelenecek şekilde zamanlamanız gerekir:

- **Retail and Commerce** > **Retail and Commerce BT** > **Ürünler ve stok** > **Ürün kullanılabilirliği**
- **Retail and Commerce** > **Dağıtım planları** > **1130** (**Ürün kullanılabilirliği**)

## <a name="additional-resources"></a>Ek kaynaklar

[POS'ta gelen stok işlemi](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[POS'ta giden stok işlemi](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
