---
title: POS'ta seri hale getirilmiş maddelerle çalışma
description: Bu konu, satış noktası (POS) uygulamasında serileştirilmiş maddelerin nasıl yönetileceğini açıklar.
author: boycezhu
manager: annbe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 0431ffa45eceac5c12d8ed991b00730c50ca62f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972567"
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

## <a name="sell-serialized-items-in-pos"></a>POS'ta seri hale getirilmiş maddeleri satma

POS uygulaması serileştirilmiş ürün satışını her zaman desteklese de, Commerce 10.0.17 ve sonraki sürümlerinde kuruluşlar, seri numarası izleme için yapılandırılmış ürünler satarken tetiklenen iş mantığını geliştiren işlevleri etkinleştirebilir.

**POS sipariş yakalama ve sipariş karşılama özelliğindeki gelişmiş seri numarası doğrulaması** etkinleştirildiğinde, POS'ta seri haline getirilmiş ürünler satılırken aşağıdaki ürün yapılandırmaları değerlendirilir:

- Ürün için **Seri türü** kurulumu (**etkin** veya **satışlarda etkin**).
- Ürün için **Boş vermeye izin verilir** ayarları.
- Ürün ve/veya satış ambarı için **fiziksel negatif stok** ayarları.

### <a name="active-serial-configurations"></a>Etkin seri yapılandırmaları

Maddeler **Etkin** seri numarası izleme boyutuyla yapılandırılmış POS'ta satıldığında, POS, kullanıcıların satış ambarının geçerli stokunda bulunamayan seri numarasına sahip serileştirilmiş bir maddenin satışını tamamlamasını engelleyen doğrulama mantığını başlatır. Bu doğrulama kuralının iki istisnası vardır:

- Madde **Boş vermeye izin verilir** etkinleştirilmiş olarak da yapılandırılmışsa, kullanıcılar seri numarasının girişini atlayabilir ve seri numarası ataması olmadan maddeyi satabilir.
- Madde ve/veya satış ambarı **Fiziksel negatif stok** etkinleştirilmiş olarak yapılandırılmışsa, uygulama, satıldığı ambardaki stokta olduğu doğrulanamayan bir seri numarasını kabul eder ve satar. Bu yapılandırma, söz konusu madde/seri numarası için stok hareketinin negatife inmesine izin verir ve bu nedenle sistem bilinmeyen seri numaralarının satışına izin verir.

> [!IMPORTANT]
> POS uygulamasının, **Etkin** seri türü maddeleri için satılan seri numaralarının satış ambarı stokunda olup olmadığını doğrulayabildiğinden emin olmak için kuruluşların Commerce Headquarters'da **Ürün kullanılabilirliğini izleme boyutları** işini ve beraberindeki **1130** ürün kullanılabilirliği dağıtım işini sık sık Commerce Headquarters üzerinden çalıştırması gerekir. Seri haline getirilmiş yeni bir stok, satış ambarlarına alındıkça, POS'un satılan seri numaralarının stok kullanılabilirliğini doğrulaması için stok yöneticisinin kanal veritabanını sık sık en güncel stok kullanılabilirliği verileriyle güncelleştirmesi gerekir. **İzleme boyutlarıyla ürün kullanılabilirliği** işi, tüm şirket ambarları için seri numaraları da dahil olmak üzere ana stokun geçerli bir anlık görüntüsünü alır. **1130** dağıtım işi bu envanter anlık görüntüsünü alır ve yapılandırılmış tüm kanal veritabanlarıyla paylaşır.

### <a name="active-in-sales-process-serial-configurations"></a>Satış işlemi seri yapılandırmalarında etkin

**Satış işleminde Etkin** olarak seri boyutuyla yapılandırılan maddeler, herhangi bir stok doğrulama mantığından geçmez çünkü bu yapılandırma stok seri numaralarının stoka önceden kaydedilmediğini ve seri numaralarının yalnızca satış sırasında yakalandığını gösterir.  

**Boş vermeye izin verilir**, **Satış işleminde etkin** olarak yapılandırılmış maddelerde de yapılandırılmışsa seri numarası girişi atlanabilir. **Boş vermeye izin verilir** yapılandırılmamışsa, uygulama, kullanılabilir stoka karşı doğrulanmayacak olsa bile kullanıcının bir seri numarası girmesini gerektirir.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>POS hareketlerinin oluşturulması sırasında seri numaralarını uygulama

POS uygulaması, seri haline getirilmiş bir madde satarken kullanıcılardan hemen seri numarası yakalamasını ister ancak uygulama, kullanıcıların seri numaralarının girişini satış işleminde belirli bir noktaya kadar atlamasına izin verir. Kullanıcı ödemeyi yakalamaya başladığında, uygulama gelecekteki sevkiyatlar veya teslim alımlar aracılığıyla yerine getirilecek şekilde yapılandırılmamış maddeler için seri numarası girişini zorunlu tutar. Peşin veya taşıma karşılaması için yapılandırılan seri haline getirilmiş maddeler, kullanıcının satışı tamamlamadan önce seri numarasını yakalamasını (veya madde yapılandırması izin veriyorsa boş bırakmayı kabul etmesini) gerektirir.

Gelecekteki teslim alım veya sevkiyat için satılan seri haline getirilmiş maddeler için POS kullanıcıları başlangıçta seri numarasını girmeyi atlayabilir ve yine de müşteri siparişi oluşturma işlemini tamamlayabilir.   

> [!NOTE]
> POS uygulaması üzerinden, seri haline getirilmiş ürünler satarken veya karşılarken, satış hareketinde seri hale getirilmiş maddeler için "1" miktarı uygulanır. Bu, seri numarası bilgilerinin satış satırında nasıl izlendiklerinin bir sonucudur. POS üzerinden birden çok seri haline getirilmiş madde için bir hareket satışı veya karşılaması sırasında, her satış satırının yalnızca "1" miktarıyla yapılandırılması gerekir. 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Müşteri siparişi karşılama veya teslim alma sırasında seri numaralarını uygulama

POS'taki **Sipariş Karşılama** işlemini kullanarak seri haline getirilmiş ürünler için müşteri sipariş satırlarını karşıladığınızda, POS, son karşılamadan önce seri numarasının yakalanmasını zorunlu tutar. Bu nedenle, ilk sipariş yakalama sırasında bir seri numarası sağlanmamışsa POS'taki çekme, paketleme veya sevk işlemleri sırasında yakalanması gerekir. Her adımda bir doğrulama yapılır ve kullanıcıdan yalnızca eksikse veya artık geçerli değilse seri numarası verileri istenir. Örneğin, bir kullanıcı malzeme çekme veya paketleme adımlarını atlar ve hemen bir sevk irsaliyesi başlatırsa ve satır için bir seri numarası kaydedilmemişse POS, son fatura adımı tamamlanmadan önce seri numarasının girilmesini zorunlu kılar. POS'ta sipariş karşılama işlemleri sırasında seri numarasının yakalanmasını zorunlu tutarken, bu konuda daha önce belirtilen tüm kurallar hala geçerlidir. Yalnızca **Etkin** olarak yapılandırılan seri haline getirilmiş maddeler bir seri numarası stok doğrulamasından geçer. **Satış işleminde Etkin** olarak yapılandırılan maddeler doğrulanmaz. **Etkin** ürünler için **Fiziksel negatif stok**'a izin verilirse, stok kullanılabilirliğine bakılmaksızın herhangi bir seri numarası kabul edilir. **Etkin** ve **Satış işleminde Etkin** öğeleri için, **Boş vermeye izin verilir** ayarı yapılandırılmışsa, malzeme çekme, paketleme ve sevk adımları sırasında istenirse kullanıcı, seri numaralarını boş bırakabilir.

Seri numaraları için doğrulamalar, kullanıcı POS'taki müşteri siparişlerinde teslim alma işlemlerini gerçekleştirdiğinde de gerçekleşir. POS uygulaması, daha önce belirtildiği gibi doğrulamaları geçirmediği sürece seri hale getirilmiş bir üründe teslim alma işlemine izin vermez. Doğrulamalar her zaman ürünün izleme boyutunu ve satış ambarı yapılandırmalarını temel alır. 

## <a name="additional-resources"></a>Ek kaynaklar

[POS'ta gelen stok işlemi](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[POS'ta giden stok işlemi](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
