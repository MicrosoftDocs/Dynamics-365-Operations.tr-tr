---
title: Çağrı merkezi katalogları
description: Bu konu Microsoft Dynamics 365 for Retail'te kataloglar için çağrı merkezine özel işlevler açıklanır.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 65c1c3070aa48bf7a2016534071693716fabe831
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562756"
---
# <a name="call-center-catalogs"></a>Çağrı merkezi katalogları

[!include [banner](includes/banner.md)]

Bu konuda Microsoft Dynamics 365 for Retail'de katalog yetenekleriyle bağlantılı, çağrı merkezine özel işlevler açıklanmaktadır.

Dynamics 365 for Retail'te bulunan katalog özellikleri birden çok amaç için kullanılabilir. Başlangıçta katalog özellikleri üçüncü taraf e-Ticaret entegrasyonlarını desteklemek için oluşturulmuştur. Katalog kurulumu, şirketlerin, bir üçüncü taraf e-Ticaret çözümünün kullanımı için harici olarak yayınlanabilen ürün ve öznitelik gruplaması oluşturmalarına olanak sağladı.

Dynamics 365 for Retail'e çağrı merkezi kanal desteği eklenince, katalog kavramı, geleneksel doğrudan tüketiciye pazarlama kataloglarıyla ilgili özellikleri desteklemek ve yönetmek için ek yetenekler dahil edecek şekilde genişletildi. Doğrudan tüketiciye hizmet eden bir şirket sık sık basılı kataloglar çıkarır ve bunları bir ya da birden fazla müşteri segmentine postalar. Bu kataloglar genellikle belirli promosyonlar veya müşteri sipariş oluşturma sırasında bir katalog tanımlama kodu sağladığı takdirde sunulacak teklifler içerir.

Doğrudan tüketiciye yönelik pazarlama şirketleri katalog üretim ve postalama maliyetlerinin gerekliliğinden emin olmak için bu kataloglara verilen yanıtları izlemeye çok önem verir. Yanıtı izlemek için, kataloğun arkasına geleneksel yöntemlerle bir kod yazdırılır ve katalog alıcısı telefonla sipariş vermek üzere aradığında bu kod istenir ve uygulanır (veya şimdi daha geleneksel olarak, müşteri çevrimiçi bir sipariş verirken kod girilebilir). Bu katalog izleme kodunu tanımlamak için kullanılan farklı sektör terimleri olsa da (anahtar kodu, promosyon kodu, katalog kodu, kaynak kodu vb.), Dynamics 365 for Retail'de bu koda **Kaynak kodu kimliği** diyoruz.

## <a name="basic-catalog-setup"></a>Temel katalog kurulumu

Kataloğunuzu yapılandırmak için **Perakende** \> **Kataloglar ve ürün çeşitleri** \> **Tüm kataloglar**'a gidin.

Yeni bir katalog oluştururken önce kataloğu bir veya daha fazla perakende kanalına bağlamanız gerekir. Bu işlem **Katalog kurulumu** formundaki **Perakende kanalları** hızlı sekmesinde yapılır. **Ekle**'ye tıklayın ve bir veya daha fazla perakende kanalı seçin. Katalog oluştururken yalnızca seçtiğiniz kanal [ürün çeşitlerine](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments) bağlı maddeler kullanılabilir.

Kataloğa ürünler eklemek için bir gezinme hiyerarşisi seçilmelidir. Gezinme hiyerarşisi, katalog için kategori yapısını destekler. **Katalog** sayfasındaki **Perakende kanalları** hızlı sekmesinde seçili perakende kanallarına bağlı gezinme hiyerarşilerinden birini seçmeniz gerekir. Bir kanala önceden bir gezinme kanalı bağlanmadıysa **Perakende** \> **Kanal kurulumu** \> **Kanal kategorileri ve ürün öznitelikleri**'ne giderek, perakende kanallarınızın her birine varsayılan bir gezinme hiyerarşisi bağlayın.

**Katalog kurulumu** sayfasındaki **Kataloglar** menü sekmesinde **Ürün ekle**'ye tıklayarak kataloğa eklenecek ürünleri yapılandırın veya gezinme hiyerarşisinde bir düğüm seçin (düğüm seçmek ekran sunumunu değiştirir ve kategoriye katalog içinde doğrudan ürün eklemenize olanak sağlar).

Ana katalog üst bilgisi görünümüne dönmek için katalog hiyerarşinin en üst düğümüne tıklayın. Yürürlük tarihini ve bitiş tarihini **Genel** hızlı sekmesinde gerektiği şekilde yapılandırın.

Kataloğun kullanılabilmesi için yayımlanması gerekir. Bir doğrulamayı işlemek için **Kataloglar** menüsünde **Kataloğu doğrula**'ya tıklayın. Bu gerekli bir eylemdir ve gerekli kurulumun doğruluğunu teyit eder. Doğrulamanın ayrıntılarını görmek için **Sonuçları görüntüle**'ye tıklayın. Hatalar varsa, verileri düzeltmeniz ve doğrulama sonucu başarılı olana kadar doğrulamayı yeniden çalıştırmanız gerekir.

Doğrulama onaylandıktan sonra menüdeki **İş akışı**'na tıklayarak onay iş akışını başlatın. İşlemi yürütmek için **İş akışı** menüsündeki **Gönder**'e tıklayın. İş akışı için adımları ve yetkili kullanıcıları **Perakende** \> **Genel merkez kurulumu** \> **Perakende iş akışları**'ndan yapılandırın. İş akışı, kataloğu bir **Onaylandı** durumuna geçirmek için gereken adımları tanımlar. Katalog bir **Onaylandı** durumundayken **Kataloglar** menüsündeki **Yayımla** seçeneğine tıklayarak işlemi tamamlayabilirsiniz. Katalog bir **Yayımlandı** durumuna geçtikten sonra, çağrı merkezi sipariş girişinde ve katalog gönderme işlemlerinde kullanılabilir.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Satış siparişi fiyatlandırmasını ve promosyonlarını yönetmek için katalogları kullanma

Bir çağrı merkeziyle birlikte kullanmak üzere katalog tanımlamak için temel nedenlerden biri, o kataloğa ilişkin belirli fiyatlar ve promosyonlar yapılandırabilme olanağıdır. Sipariş üst bilgisine veya satırlarına **Kaynak kodu kimliği** uygulandığı zaman, bu katalogdan sipariş veren müşteriler çağrı merkezi sipariş girişinde bu fiyatları ve promosyonları alır.

Kataloğa özel fiyatları yapılandırmak için **Kataloglar** sekmesindeki **Fiyat grupları** seçeneğini belirleyerek kataloğa bir veya daha fazla fiyat grubu bağlayın. Müşteriler bu katalogdan sipariş verdiği zaman, aynı fiyat grubuna bağlı tüm ticari sözleşmeler, fiyat ayarlaması günlükleri ve perakende gelişmiş indirimleri (eşik değeri, miktar, karma ve eşleşme) uygulanır.

Bu kataloğa bir veya daha fazla **Kaynak kodu kimliği** tanımlayıcısı eklemek için **Kaynak kodları** hızlı sekmesinde **Ekle**'ye tıklayın. Bu, çağrı merkezi sipariş girişi sırasında satış siparişi üst bilgisine (ve satırlarına) uygulanacak olan koddur. Bu kod, satış siparişini kataloğa ve sonuçta, yapılandırılmış olan fiyat gruplarına ve özel fiyatlara/promosyonlara bağlamak için kullanılır.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Maliyetleri ve yanıt oranlarını izlemek için kaynak kodu kimliğini kullanma

**Kaynak kodu kimliğini** tanımlarken, isterseniz bu kimliği bir **Hedef pazar kodu**'na bağlayabilirsiniz. **Hedef pazar kodu**, **Perakende** \> **Müşteriler** \> **Hedef pazar**'da tanımlanabilir. Hedef pazar, kullanıcı tanımlı bir segmente ait müşteri ve/veya müşteri adayları listesidir. Müşteri veya müşteri adayı verileri kaynak kodu kimliğine bağlanırsa, kataloğun alıcıları daha iyi görülebilir. Bir müşteri bir hedef pazara, o hedef pazar da etkin bir kaynak kodu kimliğine/kataloğa bağlanırsa, çağrı merkezi kullanıcıları **Müşteri hizmeti** sayfasındaki **Müşteriler** menüsünün **Kaynak kodları** seçeneğini belirleyerek bir müşterinin hangi katalogları aldığını görebilirler. Sipariş girişi sırasında çağrı merkezi kullanıcıları bir müşteriye gönderilen belirli katalogları satış siparişi üst bilgisindeki **Kaynak** açılır listesinde de görebilirler. Filtrenin **Tümü**'nden **Hedeflenmiş**'e çevrilmesi sayesinde, kullanıcı, müşteriye gönderilen belirli etkin katalogları görebilir. Müşterinin satış siparişi oluşturmak üzere aradığı zaman kataloğunu unutması veya katalog kodunu bulamaması/okuyamaması durumunda bu işlev yararlı olur.

Bir kataloğa birden fazla kaynak kodu kimliği bağlanabilir. Buna, bir şirket farklı segmentler bazında yanıt oranını takip etmek istediğinde gerek duyulur. Şirket farklı müşteri segmentlerine benzersiz birer kod verir ve bu sayede belirli bir katalog etkinliğinde, yanıt oranını segment düzeyinde izleyebilir.

**Kaynak kodları** hızlı sekmesinde belirli bir **Kaynak kodu kimliği** kaydı seçilip **Ayrıntılar** seçeneğine tıklanınca, satış projeksiyonlarının, postalama maliyetlerinin ve postalama tarihlerinin elde edilebildiği ek alanlar sunulur. Kataloğun etkililiği ayrıntılı şekilde analiz edilirken bu veriler yardımcı olur. Kullanıcılar daha sonra bu sayfaya dönüp **Kaynak kodu analizi** ve **Promosyonları karşılaştır** düğmelerini kullanarak mevcut satış verilerine dayalı analiz raporları tetikleyebilir ve maliyetleri ve bütçeyi fiili değerlerle karşılaştırabilirler.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Kataloğa özel sipariş ve madde komut dosyalarını yapılandırma

Çağrı merkezi kullanıcısı bir satış siparişi oluştururken, ekranda görüntülenen komut dosyalarını kullanabilir. Bu metin tabanlı komut dosyaları, kullanıcının müşteriye söyleyebileceği ek bilgiler veya çağrı merkezi kullanıcısının satış siparişi oluştururken inceleyip karşılık vereceği dahili notlar/anımsatıcılar sağlayabilir.

Farklı kataloglar için farklı komut dosyası kümelerine sahip olmak çoğu zaman yardımcı olur. **Komut dosyaları** hızlı sekmesinde, önceden tanımlanmış komut dosyaları bir kataloğa bağlanabilir. Komut dosyasının siparişin başında (sipariş üst bilgisine kaynak kodu kimliği girilir girilmez) görünüp görünmeyeceğini belirlemek için **Zamanlama** alanını kullanın.

Kataloğun hiyerarşisinde bir düğüm seçerken ve **Ürünler** hızlı sekmesindeki verilerle çalışırken, kullanıcılar kataloglara veya maddelere özel komut dosyalarını **Komut dosyaları** eylemini kullanarak da bağlayabilirler.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Kataloğa özel dikey satış ve çapraz satış maddelerini yapılandırma

Dikey satış/çapraz satış önerilerini bir maddeye bağlama işlemi ürünler kurulumundan yapılabilir ancak bazı durumlarda bir şirket, belirli bir katalogdan belirli bir ürünü sipariş eden müşterilerine dikey satış/çapraz satış promosyonları sunmak isteyebilir. Katalogdan seçilen maddeyi satın alan müşterilere dikey satışı veya çapraz satışı yapılacak ürünleri yapılandırmak için **Ürünler** hızlı sekmesinde bir madde seçip **Dikey satış/çapraz satış maddeleri**'ne tıklayın. Çağrı merkezi sipariş girişi sırasında, ekranda, olağan ürün yapılandırmasıyla o ürün için yapılandırılmış olabilecek standart dikey satış/çapraz satış ürünleri yerine kataloğa özel dikey satış/çapraz satış maddeleri görünecektir.

Dikey satış/çapraz satış maddelerinde, sipariş girişi sırasında dikey satış/çapraz satış maddesi görüntülenirken müşterinin göreceği özel mesajları göstermek için komut dosyası özelliklerinden de yararlanılabilir. Bir katalog ürünü için özel olarak yapılandırılmış dikey satış/çapraz satış ürünlerine bağlı komut dosyaları ancak çağrı merkezi sipariş girişine kataloğun kaynak kodu uygulanınca görünür.

## <a name="catalog-page-analysis"></a>Katalog sayfası analizi

**Kataloglar** sekmesinde, **Katalog sayfalarını** yapılandırmak için seçenekler mevcuttur. Bu özellik, basılı katalog için belirli sayfaları, sayfa türlerini ve bunlarla ilişkili masrafları tanımlamanıza olanak sağlar.

Katalogdaki ürünleri yapılandırırken madde için özel sayfalar, sayfa yüzdesi ve sayfa konumu ayrıntılarını tanımlamak için **Ürün sayfası düzeni** eylemini kullanın. Bu verilerin yapılandırılması, kullanıcıların **Katalog alanı analiz raporundan** yararlanmasına olanak sağlar. Bu rapor **Perakende** \> **Çağrı merkezi raporları** \> **Katalog alanı analizi** raporu altında bulunur. Bu rapor, katalogdan yapılan satışı (kataloğun kaynak kodu kimliğinin sipariş üst bilgisine veya satırına bağlandığı satış siparişleri) ve ilişkili sayfa yüzdesini ve maliyetleri analiz ederek, geleneksel bir doğrudan pazarlama **İnç kare analizi** raporu elde edilmesini sağlar.

## <a name="catalog-requests"></a>Katalog istekleri

Kataloglar Dynamics 365 for Retail'de yapılandırılıp yayımlandığı için, **Kataloğu gönder** özelliğinden yararlanılabilir. Bu özellik **Müşteri arama** ve **Müşteri hizmeti** sayfalarında mevcuttur. **Müşteri arama**'dan bir müşteri kaydı seçildikten sonra veya **Müşteri hizmeti**'nden seçili bir müşteri hesabı görüntülenirken, kullanıcılar, bir yayımlanmış ve etkin kataloglar listesinden seçim yapmalarına olanak sağlayan bir iletişim kutusunu açacak olan **Kataloğu gönder** seçeneğini belirleyebilirler. Kullanıcı, gönderilecek bir katalog, bir miktar ve belirli bir kaynak kodu kimliği seçebilir. Kullanıcılar **Gönder** düğmesine tıklayınca, daha sonra **Katalog istekleri** raporunu yazdırarak yönetilebilecek bir istek depolanır. Bu rapor **Perakende** \> **Çağrı merkezi raporları** \> **Katalog istekleri raporu** altında bulunur. Tüm katalog isteklerini, kataloğu isteyen müşterinin müşteri adı ve adres bilgileriyle listeler. Bu rapor dahili olarak kullanılabilir veya veriler, kataloğun müşteriye fiziksel olarak gönderilmesi için harici işlemleri destekleyen üçüncü bir tarafa aktarılabilir.

## <a name="additional-features"></a>Ek özellikler

**Kataloglar** sekmesinde bir **Ödeme planı** ve **Ücretsiz ürünler** yapılandırma seçenekleri de mevcuttur. Çağrı merkezi sipariş girişi sırasında kataloğa bağlı kaynak kodu kimliği uygulanırsa, müşteri ücretsiz ürünleri almaya veya tanımlanan belirli katalog ödeme planlarından yararlanmaya uygun olur. Müşterinin sistemdeki tüm etkin ödeme planlarından değil de, yalnızca kataloğuyla bağlantılı ödeme planlarından birini seçebileceği şekilde sınırlama getirmek gerekirse, bu sınırlamayı uygulamak için, bir veya daha fazla kaynak kodu kimliği için **Yalnızca katalog planlarına izin ver** onay kutusu işaretlenebilir.

## <a name="additional-notes"></a>Ek notlar

Şimdilik, çağrı merkezinde bir satış siparişine uygulanan kaynak kodu kimliği; fiyatları, promosyonları, komut dosyalarını ve dikey satış/çapraz satışları yönetmek için kullanılmaktadır. Sistem, katalogda olmayan bir ürünün satış siparişinde sipariş edilmesine bir yasak veya engel getirmeyecektir. Katalogda yer almayan bir madde sipariş edilirse, sistem ilk olarak çağrı merkezi kanalında (**Perakende** \> **Kanallar** \> **Çağrı merkezleri** \> **Tüm çağrı merkezleri**) madde fiyatı ve promosyonları için tanımlanan **Fiyat grubunu** kullanır. Belirli bir kanal fiyatı bulunamazsa, maddenin taban satış fiyatı kullanılır.
