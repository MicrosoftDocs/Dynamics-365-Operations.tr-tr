---
title: Satınalma siparişleri oluşturma
description: Bu makalede bir satınalma siparişini el ile oluşturmak için gereken işlem ve seçenekler tanımlanır.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 206d6d6769d1dedcbfefa589fd72903e65a25ba6
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439617"
---
# <a name="create-purchase-orders"></a>Satınalma siparişleri oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede bir satınalma siparişini el ile oluşturmak için gereken işlem ve seçenekler tanımlanır.

Satınalma siparişi (PO) oluşturduğunuzda, siparişin tamamı hakkında genel bilgiler PO başlığında belirtilir ve ardından bir veya daha fazla satınalma siparişi satırları eklersiniz. Bu makalede, kullanılabilecek seçeneklerden en sık kullanılanlarından bazıları açıklanmaktadır.  

Ayrıca başka bir PO belgesinden veya bir satış siparişinden satırlar kopyalayarak da PO'lar oluşturabilirsiniz. Bu durumda, alacağı göstermek için fatura üzerinde işareti tersine çevireceğiniz gibi stoktaki işareti de tersine çevirebilirsiniz.  

PO'ları el ile oluşturabilirsiniz ancak daha çok diğer işlemlerden oluşturulurlar. Siparişler talepler gibi diğer belgelere göre otomatik olarak oluşturulabilir. Alternatif olarak, planlı satınalma siparişleri sürecinde master planlamanın bir parçası olarak oluşturulabilir. Satınalma sözleşmeleri kullanırsanız, satınalma siparişleri **Siparişi serbest bırakma** eylemi tarafından oluşturulabilir. Otomatik olarak bir PO oluşturmak için daha gelişmiş yöntemler de vardır. Örneğin, doğrudan teslimi veya şirketlerarası sipariş zincirlerini kullanarak siparişleri oluşturabilirsiniz.

## <a name="creating-a-purchase-order-header"></a>Satınalma siparişi başlığı oluşturma
Yeni bir PO oluşturduğunuzda PO başlığı için en sık kullanılan bilgileri girebileceğiniz bir iletişim kutusu görüntülenir. İletişim kutusunu kapatmak için **Tamam** 'a tıkladığınızda sipariş oluşturulur ve sonra başlıkta ek bilgileri belirtebilirsiniz.  

Bir PO oluştururken dikkat edilmesi gereken ilk ayrıntı siparişin türüdür. **Satınalma siparişi** türü en sık kullanılandır. Ancak bir kredi faturası gerekiyorsa **İade edilen sipariş** türünü kullanabilirsiniz.  

**Satıcı hesabı** alanında tedarikçi belirtmeniz gerekir. Bu alan için hesap veya satıcı adı ile arama yapabilirsiniz. Bir satıcı birden çok konuma teslimat yapıyor ancak tek bir fatura hesabı kullanıyorsa **Fatura hesabı** alanında bu fatura hesabını seçebilir ve sonra bunu farklı satıcı hesaplarıyla kullanabilirsiniz. Tekrar tekrar sipariş edilemeyecek ürünler için bir PO oluşturmanız gerekirse **Tek seferlik tedarikçi** seçeneğini kullanabilirsiniz. Bu seçenek **Borç hesapları** modülünde tek seferlik hesaplar için daha sonraki bir temizlik işlemini desteklemek amacıyla otomatik olarak tek seferlik hesap olarak işaretlenen yeni bir satıcı hesabı oluşturur. Bir satıcı hesabı seçtiğinizde PO başlığındaki birçok alan varsayılan değerleri satıcı hesabıyla ilişkili bilgilerden devralır. Örneğin, varsayılan teslimat tesisi ve ambar satıcı bilgilerinden kopyalanır. Ancak satınalma başka bir konuma yönelikse varsayılan değerleri geçersiz kılabilirsiniz.  

Tedarikçi sipariş için bir referans numarası sağlamışsa bu bilgiyi **Satıcı referansı** alanında kaydedebilirsiniz. İade edilen siparişlere dair, iadeyi işlemek için tedarikçinin onayına başvurmak amacıyla **RMA** alanında bir değer belirtmeniz gerekir.  

Satınalma sözleşmesi siparişle ilişkiliyse bu bilgiyi **Satınalma sözleşmesi** alanında belirtmeniz gerekir.  

PO başlığı, tek tek satırlar yerine tüm siparişe uygulanan giderlerle ilgili bilgileri de içerir. Satıcı veya satıcının gider grubu otomatik giderlere ayarlanmışsa giderler otomatik olarak siparişe eklenebilir. Eylem bölmesindeki **Giderleri koru** seçeneğine tıklayarak giderleri sipariş başlığına el ile de ekleyebilirsiniz.

## <a name="adding-purchase-order-lines"></a>Satınalma siparişi satırlarını ekleme
PO'lar fiziksel ürünler veya hizmetler için olabilir. Stok modeli grubundaki ayar belirli bir madde numarasının bir ürüne veya bir hizmete uygulanıp uygulanmadığını belirler. Genellikle, satın alınan maddenin bir madde numarası tarafından belirtilir. Ancak sipariş doğrudan tüketilen ürünler veya hizmetler içinse tedarik kategorisini kullanarak maddeyi belirtebilirsiniz.  

POS satırları birçok alan içerir ancak bu alanların bir çoğu varsayılan değere veya sipariş başlığından devralınan bir değere sahiptir. Bir ürün veya hizmeti seçtiğinizde ek alanlar ayarlanır. En sık el ile ayarlanan alanlar madde numarası, miktar ve istenen teslim tarihine ait alanları içerir. Birim fiyatla ilgili bilgiler ve iskontolar çok önemlidir ancak bu alanların değerleri genellikle ticari sözleşmeler veya satınalma sözleşmeleri ile belirlenir.  

Bir ürün seçtiğinizde madde numarası kullanmak yerine ürün adının tamamı veya bir parçasıyla arama yapabilirsiniz. Ürünün farklı boyutlar gibi birkaç varyantı varsa **Satır ekle** işlevini veya **Varyant numarası** alanında bulunan aramayı kullanarak mevcut varyantların özetini görebilirsiniz.  

Genellikle, her bir PO satırında seçilen madde için birkaç boyut belirtmeniz gerekir. Belirtilmesi gereken boyutlar ana ürün tanımına atanan boyut gruplarına bağlıdır. Örneğin, ürünün teslim edilmesi gereken yeri göstermek için genellikle bir tesis ve ambar belirtmeniz gerekir. Ürün varyantlarını bir varyant numarası belirterek veya renk, boyut, yapılandırma veya stil gibi bir veya daha fazla ürün boyutu için değerleri girerek tanımlayın. Toplu iş ve seri numarası gibi izleme boyutları her bir stok lotunu benzersiz şekilde tanımlamanızı sağlar. Bir sipariş oluşturduktan sonra **Kayıt** eylemini kullanarak sipariş üzerinden boyut değerlerini yakalayabilirsiniz. Örneğin, bir maddeden beş parça miktarında sipariş ettiniz. Sonra bu parçalardan üçünü siyah ve ikisini mavi olacak şekilde kaydedin. Bu yaklaşım, varış kaydı sırasında boyut bilgilerini yakalamak için bir alternatiftir.  

Stoğu tutulan ürünler için stok hareketi durumunun ayrıntılarını kontrol edebilirsiniz. Örneğin, sipariş miktarına karar vermenize yardımcı olmak için eldeki stoğu kontrol etmek isteyebilirsiniz. Alternatif olarak, gelen varış kaydının oluşup oluşmadığını görmek için sipariş edilen miktarın stok durumunu gözden geçirmek isteyebilirsiniz.  

Bir ürünü satıcıya iade etmek için kullanılan bir PO satırı negatif miktara sahip olacaktır. **Rezervasyon** eylemini kullanarak iade etmek için belirli bir lot seçebilirsiniz.  

Bazı durumlarda, sipariş ettiğiniz miktarı farklı tarihlerde farklı parçalarını teslim edebilecek şekilde bölmek isteyebilirsiniz. Bu teslimatları **Satırlar** görünümündeki **Satınalma sipariş satırı** menüsünde bulunan **Teslimat zaman çizelgesi** eylemini kullanarak ayarlayabilirsiniz.  

Satıcı veya satıcı gider grubu ve madde veya madde gider grubu otomatik giderlere ayarlanmışsa giderler otomatik olarak PO satırlarına eklenebilir. Ancak, giderler sipariş satırı düzeyinde genellikle el ile eklenir. Gider eklemek için **Satırlar** görünümündeki **Finansal öğeler** menüsü üzerinden **Giderleri koru** eylemini kullanarak **Giderleri koru** sayfasını açın. Sipariş satırı düzeyinde doğrudan giderleri eklemenin avantajı giderin stok maliyeti olarak tahsis edilebilmesidir. Gider kodlarını hesap ürün maliyetine ayarlamak için **Madde** borç seçeneğini kullanın. Bu gider türleri sipariş onaylanmadan önce PO başlığından satırlara tahsis edilmelidir. Örneğin, her bir satırdaki miktara göre giderleri tahsis etmek isteyebilirsiniz. Gider kategorisi giderlerin muhasebesinin nasıl yapıldığını da etkiler. Örneğin, sabit giderler sabit bir tutarı belirtir ve yüzde giderleri sipariş satırı için net tutarın yüzdesi olarak hesaplanır. PO'lar bir yüke atanabilir ve yük, ulaştırma maliyeti için beklenen gider tahminini içerebilir. Bu gideri yükten geri dönerek PO satırlarına tahsis edebilirsiniz.

## <a name="purchase-order-actions"></a>Satın alma siparişi eylemleri
PO'ya başlık ve satırları ekledikten sonra sipariş onaya hazır olmadan önce ek adımları tamamlamanız gerekir. Çok fazla seçenek olduğundan geçerli menü öğesini bulmak için [Eylem araması](../../fin-and-ops/get-started/action-search.md) seçeneğini kullanmak yararlı olabilir.  

Siparişteki ürünleri tamamlayıcı maddelere sahip olacakları şekilde yapılandırabilirsiniz. Tamamlayıcı maddeler diğer ürünlerle satın alınması gereken veya satın alınabilen ürünlerdir. Tamamlayıcı ürünler ürünlere iliştirilmiş olarak ücretsiz eklenebilir veya bunları siparişe ekleyip eklememeye karar verebilirsiniz. Eklenen her sipariş satırından sonra tamamlayıcı maddeleri gözden geçirebilirsiniz. Ancak büyük olasılıkla Eylem Bölmesinden açabileceğiniz **Tamamlayıcı maddeler** sayfasını kullanarak tüm sipariş satırları için ilgili tamamlayıcı maddeleri gözden geçirmek veya eklemek daha kolay olabilir.  

İskontolar genellikle oluşturuldukları satırlara eklenirler. Ancak, birkaç iskonto tüm siparişe uygulanır.

-   **Toplam iskonto** eylemi tüm siparişe uygulanan toplam iskonto yüzdesini hesaplar. Bu iskontoyu nakit iskontosu indirimi ile karıştırmayın. Nakit iskontoları fatura ödendiğinde uygulanır ve belirli bir tarih itibariyle ödeme kapanışına bağlıdırlar.
-   Çok satırlı iskonto uygulanıyorsa bunu hesaplamak ve siparişe atamak için **Çok satırlı iskonto** eylemini kullanmanız gerekir. Çok satırlı iskontolar siparişteki ürün karışımı ortak eşik değerini aştığında teklif edilebilen iskontolardır. Yalnızca birkaç şirket bu iskonto türünü kullanır.

**Madde** borç türünü kullanan bir gider koduna sahip giderler sipariş onaylanmadan önce satır düzeyinde atanmalıdır. Giderin toplam tutarını belirtmek için bu giderleri sipariş başlığı düzeyinde atamak daha uygun olabilir. Ancak bu durumda gider sipariş onaylanmadan önce her bir satıra kadar atanmalıdır. Tutarları sipariş satırlarına kadar başlık düzeyinde atanan giderlerden bölmek için **Giderleri tahsis et** eylemini kullanabilirsiniz. Giderleri her bir satırın net tutarına göre, sipariş edilen miktara göre veya sipariş satırları arasında eşit olarak bölebilirsiniz. Giderleri satırlara atadığınızda gider sipariş başlığından kaldırılır.  

PO'lar bütçe fonlarının işleme konulmadan önce siparişe atanmasını gerektirecek şekilde yapılandırılabilir. Bu durumda bütçeyi tahsis etmek için **Bütçe kontrolü** eylemini kullanabilirsiniz.  

Bir PO'nun tamamlanmasını geciktirmek zorunda kalabilirsiniz. Örneğin, ürünler veya hizmetlerle ilgili bilgilere ihtiyaç duyabilirsiniz veya harcama için yetki almanız gerekebilir. Bir siparişi durdurmanın birçok yolu vardır. Örneğin, siparişi onaylamak için bekleyebilirsiniz. Alternatif olarak, bir değişiklik yönetimi iş akışı kullanılıyorsa siparişi onaya göndermeyin. Belirli bir satıcı için tüm siparişleri engellemeniz gerekiyorsa satıcı aslı üzerinden işlem yapmak için satıcıyı **Beklemede** olarak da işaretleyebilirsiniz. Siparişin işlenmesini önleyen koşullar da vardır. Örneğin, kredi limitleri aşıldıysa veya gerekli bütçe fonları kullanılamıyorsa işlem önlenebilir.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Satın alma siparişine genel bakış](purchase-order-overview.md)

[Satınalma siparişlerini onaylama](purchase-order-approval-confirmation.md)

[Ürün girişi ve satınalma siparişleri karşılaştırması](product-receipt-against-purchase-orders.md)

[Satıcı faturalarına genel bakış](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]