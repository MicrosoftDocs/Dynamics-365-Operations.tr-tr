---
title: Satıcı faturalarına genel bakış
description: Bu konuda, satıcı faturaları hakkında genel bilgiler verilmektedir. Satıcı faturaları, alınan ürün ve hizmetler için ödeme talepleridir. Satıcı faturaları, devam eden hizmetler için bir faturayı temsil edebileceği gibi, belirli madde ve hizmetler için satınalma siparişlerine de dayanabilir.
author: abruer
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d51a5ff2dca764a534ea4bf92c30bcf0bf0a5dad
ms.sourcegitcommit: 51cd470ee885d12f7d51c66201b092aaa16dfaa6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2020
ms.locfileid: "4701688"
---
# <a name="vendor-invoices-overview"></a>Satıcı faturalarına genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda, satıcı faturaları hakkında genel bilgiler verilmektedir. Satıcı faturaları, alınan ürün ve hizmetler için ödeme talepleridir. Satıcı faturaları, devam eden hizmetler için bir faturayı temsil edebileceği gibi, belirli madde ve hizmetler için satınalma siparişlerine de dayanabilir.

## <a name="vendor-invoices"></a>Satıcı faturaları

Bir satınalma siparişinden bir satıcı faturası, satıcıya verilmiş satınalma siparişine göre ürünler veya hizmetler alındığında, oluşturulan bir faturadır. Satıcı faturası, mallar veya hizmetler için bir başlık ve bir veya daha fazla satır içerir. Satıcı faturası, satınalma siparişinden ürün girişine ve oradan satıcı faturasına doğru oluşan döngüyü tamamlar.

Bazı satıcı faturaları bir satınalma siparişine bağlı olsalar da, satıcı faturaları satınalma siparişi satırlarına karşılık gelmeyen satırlar da içerebilirler. Herhangi bir satınalma siparişi ile ilişkili olmayan satıcı faturaları da oluşturabilirsiniz. Bu satıcı faturaları bir hizmet faturası gibi fatura devam etmekte olan hizmetleri gösterebilir ve bunları eklediğinizde, bir satınalma siparişine referans göstermeniz gerekmez.

Satıcı faturası girmek için çeşitli yollar vardır:

- Satıcı faturası kaydı, bir satınalma siparişine referans bulunmayan faturaları hızla girmenize ve bu sayede gideri tahakkuk ettirmenize olanak sağlar. Satıcı fatura onay günlüğünü kullanarak bu faturaları seçebilir ve tahakkuku tersine çevirmek için satıcı bakiyesine nakledebilirsiniz.
- Satıcı fatura günlüğü tek adımda bir satınalma siparişine referans göstermeyen faturaları hızla girmenizi sağlar.
- Satıcı faturası havuzu ile birlikte satıcı fatura kaydı, hızla gider tahakkuk etmek için faturaları girmenizi sağlar. Daha sonra gider hesabına karşı faturayı deftere nakletmek için ilişkili satınalma siparişlerini açabilirsiniz.
- **Açık satıcı faturaları** ve **Bekleyen satıcı faturaları** sayfaları onaylanmış satınalma siparişlerinden satıcı faturaları oluşturmanızı sağlar.

Aşağıdaki tartışma **Açık satıcı faturaları** veya **Bekleyen satıcı faturaları** sayfalarının bir satınalma siparişinden satıcı faturası oluşturmak üzere nasıl kullanılacağı hakkında daha fazla bilgi sağlar.

## <a name="understanding-invoice-line-quantities"></a>Fatura satırı miktarlarını anlama

Bir satıcı faturasını ilgili satınalma siparişinden açarsanız, fatura satırları satınalma siparişinden oluşturulur. Miktarlar varsayılan olarak ürün girişi miktarlarından alınır. Ancak, aşağıdaki varsayılan davranışların herhangi birini kullanabilirsiniz:

- **Şimdi alma miktarı** – Kısmi sevkiyatlar için bu seçeneği kullanın. **Miktar** alanındaki varsayılan değer satınalma siparişindeki **Şimdi al** içinde belirtilen miktarı alanından alınır.
- **Sipariş edilen miktar** – Tam sevkiyatlar için bu seçeneği kullanın. **Miktar** alanındaki varsayılan değer satınalma siparişindeki **Sipariş edildi** içinde belirtilen miktarı alanından alınır.
- **Kayıtlı miktar** – Madde kayıt gerektiriyorsa, bu seçeneği **Madde modeli grupları** sayfasında belirtildiği gibi kullanın. **Miktar** alanındaki varsayılan değer, kaydedilen fiziksel güncelleştirme miktardır.
- **Ürün giriş miktarı** – Sipariş için ürün girişi aldıysanız, bu seçeneği kullanın. **Miktar** alanındaki varsayılan değer,mevcut ürün girişlerinin toplam miktarından alınır.
- **Kayıtlı miktar ve hizmetler** – Stoklu maddeleri veya stoğu olmayan maddeler için miktarlar giriş günlüklerinde kaydedilmiş ise bu seçeneği kullanın. Bu seçenek kaydettirilmiş olup olmadığını dikkate almadan hizmetleri de içerir.

Tüzel kişiliğiniz fatura eşleştirmesi kullanıyorsa, miktar eşleştirme sonuçlarını **Ürün alış irsaliyesi miktar eşleşmesi** sütununda görüntüleyebilirsiniz. Ayrıca Eylem Panosu'nun **İnceleme** sekmesindeki **Eşleştirme ayrıntıları** düğmesini miktar eşleştirmesinin sonuçlarını görüntülemek için kullanabilirsiniz.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Satınalma siparişinde olmayan bir satır ekleme

Satıcı faturasına satınalma siparişinde bulunmayan bir satır ekleyebilirsiniz. Madde numarası veya tedarik kategori seçmelisiniz. Daha sonra satıra miktarları, fiyatları ve tutarları ekleyebilirsiniz. Satır, sadece fatura toplamları için eşleştirme ilkeleri içine eklenecektir.

## <a name="submitting-a-vendor-invoice-for-review"></a>Satıcı faturasını değerlendirilmek üzere gönderme

Kuruluşunuz, satıcı faturalarını gözden geçirme işlemini yönetmek için iş akışlarını kullanabilir. İş akışını gözden geçirmesi, faturası başlığı, fatura satırı veya her ikisi için de gerekli olabilir. İş akışı denetimleri başlığa veya satıra uygulanabilir, denetimi tıkladığınızda odağın nere olduğuna bağlı olarak. **Naklet** düğmesi yerine, bir **Gönder** düğmesi göreceksiniz ve bunu satıcı faturasını gözden geçirme sürecine göndermek için kullanabilirsiniz.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Faturanın iş akışına gönderilmesini engelleme 

Bir faturanın iş akışına gönderilmesini engelleyebilmenizin çeşitli yolları aşağıda verilmiştir.

- **Fatura toplamı ve kaydedilen toplam eşit değil.** Faturayı gönderen kişi, toplamların eşit olmadığını belirten bir uyarı alacak ve faturayı iş akışına yeniden göndermeden önce bakiyeleri düzeltebilecektir. Bu özellik, **Özellik yönetimi** sayfasındaki  **Fatura toplamı ve kaydedilen fatura toplamı eşit olmadığında iş akışına göndermeyi engelle** parametresi etkin olduğunda kullanılabilir. 

- **Fatura tahsis edilmemiş masraflar içeriyor.** Faturayı gönderen kişi, faturada tahsis edilmemiş masraflar olduğunu belirten bir uyarı alacak ve faturayı iş akışına yeniden göndermeden önce düzeltebilecektir. Bu özellik, **Özellik yönetimi** sayfasındaki  **Satıcı faturasında tahsis edilmemiş masraflar olduğunda iş akışına göndermeyi engelle** parametresi etkin olduğunda kullanılabilir.

- **Fatura, deftere nakledilen başka bir faturayla aynı fatura numarasını içeriyor.** Faturayı gönderen kişi, yinelenen numaraya sahip bir fatura bulunduğunu belirten bir uyarı alacak ve faturayı iş akışına yeniden göndermeden önce düzeltebilecektir. Bu uyarı, **Kullanılan fatura numarasını denetle** etiketli Borç hesapları parametresi **Yineleneni reddet** olarak ayarlandığında görüntülenir. Bu özellik, **Özellik yönetimi** sayfasındaki **Fatura numarası deftere nakledilmiş bir faturada zaten varsa ve sisteminiz yinelenen fatura numaralarını kabul etmek üzere yapılandırılmadıysa iş akışına gönderimi engelle** parametresi etkin olduğunda kullanılabilir.  

## <a name="matching-vendor-invoices-to-product-receipts"></a>Satıcı faturalarını ürün girişlerine eşleştirmek

Satıcı faturaları için bilgi girebilir ve kaydedebilirsiniz ve fatura satırlarını ürün giriş satırlarıyla eşleştirebilirsiniz. Bir satır için kısmi miktarlar da eşleştirebilirsiniz.

Belirli bir satınalma siparişinin tüm maddeleri henüz alınmamış olsa bile, geçerli tarihe kadar alınmış ürün girişi satır maddelerine dayanarak bir satıcı faturası oluşturabilirsiniz. Örneğin, ayda bir o ay içinde sevk ettikleri tüm teslimatları içeren bir faturayı göndermesi durumunda bu seçeneği kullanabilirsiniz. Her ürün girişi, satınalma siparişindeki maddelerin kısmi veya tam teslimini temsil eder.

Faturayı deftere naklettiğinizde, her maddenin **Fatura kalan tutarı** miktarı seçilen ürün girişinden alınan maddelerin toplamıyla güncelleştirilir. Eğer tüm maddeler için **Fatura kalanı** miktarı ve **Teslimat bakiyesi** satınalma siparişindeki miktarı 0 (sıfır) olursa, satınalma siparişinin durumu **Faturalandı** olarak değiştirilir. Eğer **Fatura kalanı** miktarı 0 değilse, satınalma siparişinin durumu değiştirilmez ve buna ek faturalar girilebilir.

Bu seçenek, satınalma siparişi için en az bir ürün girişinin deftere nakledildiğini varsayar. Satıcı faturası bu ürün girişlerine dayanır ve bunların miktarlarını yansıtır. Faturanın mali bilgileri, faturayı naklettiğinizde girilen bilgilere dayanır.

Daha fazla bilgi için bkz. [Satıcı faturasını kaydetme ve teslim alınan miktarla eşleştirme](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Satıcı faturasını toplu iş kullanarak deftere nakletmek amacıyla satıcı faturası iş akışı için otomatik bir görev yapılandırma

Faturaların toplu olarak işlenmesi için Satıcı faturası iş akışına otomatik deftere nakil görevi ekleyebilirsiniz. Faturaları toplu işle deftere nakletmek, iş akışı sürecinin deftere nakil işleminin bitmesini beklemek zorunda kalmadan devam etmesine olanak sağlar ve böylece iş akışına gönderilen tüm görevlerin genel performansı artar.

Satıcı faturasını toplu işle deftere nakletmek için **Özellik yönetimi** sayfasında **Satıcı faturası toplu deftere nakil** parametresini açın. Satıcı faturası iş akışlarını, **Borç hesapları > Kurulum > Borç hesapları iş akışları**'na giderek kolayca yapılandırabilirsiniz.

**Satıcı faturası toplu deftere nakil** parametresinin etkin olup olmamasından bağımsız olarak, iş akışı düzenleyicisinde **Satıcı faturasını toplu iş kullanarak deftere naklet** görevini görebilirsiniz. Özellik parametresi etkinleştirilmediğinde, **Satıcı faturasını toplu iş kullanarak deftere naklet** görevi içeren bir fatura, parametre etkinleştirilene kadar iş akışında işlenmez. **Satıcı faturasını toplu iş kullanarak deftere naklet** görevi **Satıcı faturalarını deftere naklet** otomatik görevi ile aynı üretim akışında kullanılmamalıdır. Ayrıca, **Satıcı faturasını toplu iş kullanarak deftere naklet** görevi, iş akışı yapılandırmasındaki son öğe olmalıdır.

Toplu işe dahil edilecek fatura sayısını ve bir toplu işi yeniden planlamadan önce beklenmesi gereken saat sayısını **Borç hesapları > Kurulum > Borç hesabı parametreleri > Fatura > Fatura iş akışı**'na giderek belirtebilirsiniz. 

## <a name="working-with-multiple-invoices"></a>Birden çok fatura ile çalışma

Aynı anda birden çok fatura ile çalışabilir ve bunların tümünü aynı anda deftere nakledebilirsiniz. Birden çok fatura oluşturmanız gerekiyorsa, **Bekleyen satıcı faturaları** sayfasını kullanın. Birden çok satıcı faturalarını deftere nakletmeniz ve yazdırmanız gerekiyorsa, fatura onay günlüğünü kullanın. Fatura onay günlüğünü kullanıyorsanız, bu satınalma siparişi için en az bir ürün girişinin deftere nakledilmesi gerekir ve bir faturanın bu satınalma siparişi için fatura kaydına nakledilmesi gerekir. Faturanın mali bilgileri, deftere nakledilmiş faturadan gelir.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Kullanımdaki satıcı faturalarını kurtarmak

Bir satıcı faturası kullanımdayken başka bir kullanıcı tarafından düzenlenemez. Ancak, bir faturanın durumu bazen faturanın kullanıldığını belirtiyor olabilir, aktif olarak düzenlenmiyor olsa bile. Örneğin, uygulama, fatura oluşturulurken yanıt vermeyi durdurmuş olabilir veya bir kullanıcı faturayı uygulamada açık unutmuş olabilir.

**Satıcı faturalarını kurtar** sayfasını kullanarak dört saatten uzun süredir kullanımda olan satıcı faturalarını kurtarabilir veya serbest bırakabilirsiniz, böylece düzenlenebilirler. Bu sayfayı **Periyodik görev** gezintisinden veya **Satıcı fatura girişi** çalışma alanındaki bir kutucuktan açabilirsiniz. Bir fatura kurtarıldıktan sonra, **Satıcı faturası** sayfasında düzenlenmeye hazır olacaktır.

**Satıcı faturalarını kurtar** sayfasına yalnızca **Kullanımdaki satıcı faturalarını kurtar** güvenlik ayrıcalığı size atanmışsa erişebilirsiniz. Ek olarak, **Satıcı faturası kurtarılmasına izin ver** parametresi, **Borç hesapları parametreleri** sayfasında açık olmalıdır.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Satıcı faturalarının iş akışı durumu düzeltilemez durumundan taslakta sıfırlanıyor

Kurtarılamayan bir hata nedeniyle durdurulan bir iş akışı örneği, iş akışı durumu **Düzeltilemez** olacaktır. Satıcı faturası iş akışının durumu **Kurtarılamaz** ise **Geri çağır**'ı seçerek bunu **Taslak** olarak sıfırlayabilirsiniz. Daha sonra satıcı faturasını düzenleyebilirsiniz. **Özellik yönetimi** sayfasında **Satıcı faturalarının iş akışı durumunu Düzeltilemez durumundan Taslak durumuna sıfırlama** parametresi açıksa bu özellik kullanılabilir.

**İş akışı geçmişi** sayfasını kullanarak iş akışı durumunu **Taslak** olarak sıfırlayabilirsiniz. Bu sayfayı **Satıcı faturasından** veya **Ortak > Sorgular > İş akışı** gezintisini açabilirsiniz. İş akışı durumunu **Taslak** olarak sıfırlamak için **Geri çağır**'ı seçin. Ayrıca,**Satıcı faturası** veya **Bekleyen satıcı faturaları** sayfasında **Geri çağır** eylemini seçerek iş akışı durumunu Taslak'a sıfırlayabilirsiniz. İş akışı durumu **Taslak** olarak sıfırlandıktan sonra, **Satıcı faturası** sayfasında düzenlenmeye açık hale gelir.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Bekleyen satıcı faturaları sayfasında fatura toplamını görüntüleme
**Borç hesapları parametreleri** sayfasındaki **Bekleyen satıcı faturaları listesinde fatura toplamını göster** parametresini etkinleştirerek, **Bekleyen satıcı faturaları** sayfasındaki fatura toplamını görüntüleyebilirsiniz. 



## <a name="additional-resources"></a>Ek kaynaklar

- [Satıcı fatura ilkelerini ayarla](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Satıcı faturası kullanarak fatura verilerini AP sistemine gir](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Fatura havuzu kullanarak fatura verilerini AP sistemine girme](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Fatura günlüğüne satıcı faturası kaydetme](tasks/record-vendor-invoice-invoice-journal.md)
