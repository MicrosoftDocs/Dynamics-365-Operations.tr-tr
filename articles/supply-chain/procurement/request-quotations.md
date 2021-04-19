---
title: Teklif taleplerine (RFQ'lar) genel bakış
description: Bu konuda, teklif taleplerine (RFQ) genel bakış sağlanmaktadır. Kuruluşlar, satın almak zorunda oldukları maddeler veya hizmetler için çeşitli satıcılardan rekabetçi teklifler almak istediklerinde RFQ'lar yayınlar.
author: kamaybac
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df430dada52ac1aa910a3d2007aacf65d8032383
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812559"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Teklif taleplerine (RFQ'lar) genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda, teklif taleplerine (RFQ) genel bakış sağlanmaktadır. Kuruluşlar, satın almak zorunda oldukları maddeler veya hizmetler için çeşitli satıcılardan rekabetçi teklifler almak istediklerinde RFQ'lar yayınlar. Bir RFQ'da, satıcılardan belirlediğiniz madde miktarları için fiyat ve teslimat süreleri vermelerini istersiniz.
Satıcılardan, nakliye maliyetleri ya da büyük siparişler için indirimler veya satıcı faturalarının erken ödenmesi gibi dolaylı giderler olup olmadığını belirtmelerini de isteyebilirsiniz.

RFQ işlemi aşağıdaki görevlerden oluşur:

1. RFQ oluşturma ve bir veya daha çok satıcıya gönderme.
1. Teklifleri (RFQ yanıtlarını) alma ve kaydetme.
1. Kabul edilen teklifleri satınalma siparişine, satınalma anlaşmasına veya satınalma talebine aktarma.

Aşağıdaki örnekte teklif talebi sürecine genel bakış verilmektedir.

[![RFQ işlemi](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Planlanan siparişlerden, satınalma talebinden veya el ile yapılan bir girişten bir RFQ servis talebi oluşturabilirsiniz. RFQ servis talebi, her satıcıya bir RFQ vermek için kullandığınız temel belgedir.

RFQ servis talebini hazırlayıp satıcıları ekledikten sonra RFQ servis talebinde **Gönder**'i (Kamu sektörü için **Gönder ve yayımla**) seçin. RFQ gönderdiğiniz her satıcı için bir RFQ günlüğü oluşturulur. Gönder eylemi için Yazdırma seçeneklerini her satıcı için arşive gönderilecek bir rapor yazdıracak veya her satıcının e-posta adresine bir rapor gönderecek şekilde ayarlayabilirsiniz. Ayrıca, her satıcıya ilişkin RFQ günlüğü, satıcıya daha sonra gönderebileceğiniz veya yeniden gönderebileceğiniz bir rapor oluşturmak için kullanılabilir. Gönder eylemini, satıcının dolduracağı bir yanıt sayfası oluşturmak için de yapılandırabilirsiniz.

Bu konu, satıcı işbirliği kullanılmadığında RFQ'ların işlenmesine ilişkin süreci kapsar. Sisteminiz satıcı işbirliği için ayarlanmamışsa, satıcılar tekliflerini doğrudan Supply Chain Management'ta girebilir. Daha fazla bilgi için bkz. [Harici müşterilerle satıcı işbirliği](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) ve [Harici satıcılarla satıcı işbirliği](vendor-collaboration-work-external-vendors.md).

Gönderdikten sonra bir RFQ'da düzeltme yapmanız gerekirse, RFQ'yu işleminizi tamamladıktan sonra satıcılara iki düzeltme eylemini kullanarak gönderebilirsiniz: Oluştur ve Sonlandır.

Teklifleri e-posta ile aldığınızda, bunları **Teklif talepleri** sayfasından işleyebilirsiniz.

Bir satıcıdan gelen yanıtın ikinci defa yinelenmesi gerekirse, **Teklif talebi** sayfasında **İade et**'e tıklayın. İade eylemi yeni bir günlük oluşturur ve Yazdırma ayarlarınıza göre bir rapor yazdırılır, arşivlenir ve gönderilir.

RFQ servis talebine puanlama ölçütü eklediyseniz, RFQ'da puanlama girebileceğiniz bir puanlama paneli bulunur. **Yanıtları karşılaştır** sayfasında yanıtları karşılaştırdığınızda toplam puanlar RFQ'da görüntülenir. **Yanıtları karşılaştır** sayfasında satır fiyatı, toplam fiyat ve teslimat tarihi gibi diğer yanıt verilerini de karşılaştırabilirsiniz.

Bir teklifi veya bir teklifteki birçok satırı seçtikten sonra tüm veya bazı satırları kabul edip geri kalanları reddedebilirsiniz. Kabul etme günlükleri, reddetme günlükleri ve ilgili raporlar oluşturulur ve Yazdırma ayarlarınıza göre yazdırılır, arşivlenir ve gönderilir. Bir teklifi veya bir teklifteki belirli satırları kabul ettiğinizde, bir satınalma anlaşması veya satınalma siparişi oluşturulur ya da RFQ satınalma türüne göre satınalma talebi güncelleştirilir. Kabul edip etmediğinize bakılmaksızın, herhangi bir yanıt için daha sonra kullanabileceğiniz bir ticari anlaşma oluşturabilirsiniz.

RFQ servis talebinin iki durumu bulunur: en düşük ve en yüksek. Durumu **Tüm teklif talepleri** liste sayfasında görebilirsiniz. En düşük durum RFQ servis talebindeki herhangi bir satırın en az gelişmiş aşamasıdır; en yüksek durum RFQ servis talebindeki herhangi bir satırın en ileri aşamasıdır. Örneğin, üç satırı olan bir RFQ servis talebinin iki satıcıya gönderilmesi durumunda her birinde üç satır olan iki RFQ bulunur. Tüm satırlar **Gönderildi**. Şimdi satıcılardan biri tarafından bir teklif girilir ve RFQ satırları **Alındı** durumunu alır. Bu, RFQ servis talebindeki üç satırın tümünün bir RFQ için **Gönderildiği** ve diğer RFQ için **Alındığı** anlamına gelir. En düşük durum **Gönderildi** ve en yüksek durum **Alındı** olacaktır.

Bu durumlar, bu konuda daha ayrıntılı açıklanacaktır.

## <a name="setting-up-rfq-functionality"></a>RFQ işlevini ayarlama

Bir RFQ servis talebi oluşturmadan önce **Tedarik ve kaynak atama parametreleri** sayfasında RFQ bilgilerini ayarlamanız gerekir. RFQ servis talebi oluşturduğunuzda, RFQ'ya kopyalanan varsayılan değerleri belirtebilirsiniz. Aşağıdaki varsayılan değerleri belirtebilirsiniz:

- Yeni RFQ'nun satınalma türü: **Satınalma siparişi** veya **Satınalma anlaşması**
- Bitiş tarihi ve RFQ servis talebinin oluşturulduğu günden başlayarak mahsup zamanı.
- RFQ servis talebine belirli bir puanlama yöntemini varsayılan olarak ayarlayabilecek istek türü.
- Teslimat bilgileri ve ödeme koşulları.

Bu değerleri belirli bir RFQ için geçersiz kılabilirsiniz.

Düzeltme işlemini de yapılandırmanız gerekir. Bu yapılandırma işleminin bir parçası olarak, alan kilidini açabilirsiniz. Alan kilitleme açık olduğunda, RFQ üzerinde düzeltme yapmak isteyen bir tedarik uzmanının önce RFQ servis talebindeki **Teklif** sekmesinin **Düzeltme** bölümündeki **Oluştur** seçeneğini belirlemesi gerekir. Arından, RFQ servis talebi düzeltme ile güncelleştirildikten sonra, satın alma uzmanı, işlemi **Sonlandır**'ı seçerek tamamlamalıdır. Sonlandır eylemi, satıcıları düzeltilen RFQ hakkında bilgilendiren bir e-posta oluşturur.

**Tedarik ve kaynak atama parametreleri** sayfasından satıcılara gönderilecek e-posta bildirimi için kullanılacak şablonu seçebilirsiniz. **E-posta şablonları**'nda bir şablon oluşturulduğunda aşağıdaki değiştirme belirteçlerini içerebilir:

- %RFQ servis talebi%
- %Teklifi iade nedeni%
- %Düzeltme yapma nedeni%
- %Düzeltmeyi yapan%
- %Company%
- %RFQ servis talebi adı%
- %Expiry Date Time%
- %Date%

%Teklifi iade nedei% ve %Düzeltme yapma nedeni% belirteçleri, tedarik uzmanının **Düzeltme** sihirbazında düzeltme işlemini tamamlarken girebileceği metinle değiştirilir. %Amendment prepared by% ve %Company% belirteçleri otomatik olarak RFQ'dan alınır. %Date% belirteci geçerli tarih ile değiştirilir.

Bir RFQ'yu gönderildikten sonra iptal etmek isterseniz, bunu RFQ servis talebinden yapabilirsiniz. E-posta şablonunun iptali için iptal bildiriminin satıcının ilgili kişilerine gönderilmesi gerekir. Şablonu **Tedarik ve kaynak atama parametreleri** sayfasından seçilmelidir. Şablon oluşturulduğunda aşağıdaki değiştirme belirteçlerini içerebilir:

- %İptal sebebi%
- %RFQ servis talebi%
- %RFQ'yu iptal eden%
- %Company%
- %RFQ servis talebi adı%
- %Date%

%İptal sebebi% belirteci, tedarik uzmanının **İptal** sihirbazına girebileceği bir metin ile değiştirilir. %Date% belirteci geçerli tarih ile değiştirilir.

Bir teklifte, teklifin neden reddedildiği veya kabul edildiğini belirtmek için neden kodları kullanmak isterseniz, **Satıcı nedenleri** sayfasında neden kodları ayarlamanız gerekir.

Tedarik ve kaynak atamadaki **Form ayarı** sayfasında yazdırılan veya depolanan RFQ belgelerinizin görünümünü yapılandırabilirsiniz.

> [!NOTE]
> Kamu sektörü yapılandırması için, gönderilen bir RFQ'da değişiklik yapmak için düzeltme işlemini kullanmanız gerekir. Bir RFQ gönderildiğinde alanlar kilitlenir.
Bu nedenle, RFQ'da değişiklik yapmak için daha önce açıklandığı şekilde düzeltme işlemini başlatmak üzere **Oluştur**'u seçmeniz gerekir. Kilitleme davranışı **Tedarik ve kaynak atama parametreleri** sayfasındaki **RFQ'yi gönderildiğinde kilitle** seçeneğiyle kontrol edilir. Varsayılan olarak bu parametre **Evet** olarak ayarlanır ve kamu sektörü yapılandırmasında varsayılan ayar değiştirilemez. Bu nedenle, kamu sektörü dışındaki yapılandırmada düzeltme işlemi el ile gerçekleştirilebilmesine karşın, kamu sektörü yapılandırması için kullanılmak zorundadır.

Bir satınalma sipariş için RFQ servis talebi oluşturduğunuzda ve RFQ'ya bir stok maddesi eklediğinizde, giriş durumu **Teklif girişi** olan bir stok hareketi oluşturulur. Malzemeleri hesaplamak için bir master plan kullandığınızda yalnızca bu duruma sahip RFQ servis talebi satırları göz önünde bulundurulur. Master planın RFQ servis talebi satırlarını beklenen giriş olarak eklemesini istiyorsanız, master plan ayarlama aşamasında bu davranışı yapılandırmanız gerekir.

Bir satınalma yöneticisi veya temsilcisi, kuruluşun tedarik gereksinimlerine uyacak talep türleri oluşturup bunları koruyabilir. Her istek türü bir puanlama yöntemiyle ilişkilendirilebilir. Puanlama yöntemleri, teklifleri puanlarken kullanabileceğiniz ölçüt kümesinden oluşur. Talep türlerini, puanlama yöntemlerini ve puanlama ölçütünü **Talep türü** ve **Puanlama yöntemi** sayfalarından ayarlamanız gerekir.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Satıcı RFQ Yanıt formlarına eklenecek varsayılan alanları seçme

Bir teklif talebini (RFQ) yanıtlarken (teklif verirken) satıcılardan almak istediğiniz belirli türde bilgileri belirtebilirsiniz. Varsayılan olarak işaretlediğiniz alanlar, satıcı işbirliği için sağlanan çevrimiçi forma dahil edilir. Bu ayarları yapmak için:

1. Henüz yapmadıysanız, *Satıcı RFQ yanıt formlarına dahil eldilecek RFQ alanlarını seç* özelliğini etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanın.
1. **Tedarik ve kaynak atama > Kurulum > Tedarik ve kaynak atama parametreleri**'ne gidin.
1. **Teklif talebi** sekmesini açın.
1. **Teklif talepleri için varsayılan değerleri ayarla** başığı altında **Varsayılan teklif talepleri** yanıt alanlarını seçin.
1. **Varsayılan teklif talebi yanıt alanları** iletişim kutusu açılır.
1. **Satıcı RFQ yanıt formlarına dahil edilen RFQ alanları** bölümü, RFQ yanıt formlarında kullanılabilen her alan için bir kaydırıcı içerir. Bu bölümde *Evet* olarak ayarlanan alanlar RFQ yanıt formlarına (değerleriyle birlikte) dahil edilir. Fiyat tekliflerini gözden geçirirken satıcıların verileri görmesini önlemek istediğiniz her alan için kaydırıcıyı *Hayır* olarak ayarlayın. Bu, satıcı girilen bilgileri görmeden, RFQ girişi sırasında dahili amaçlar için tahmini veya beklenen değerleri girebilmenizi sağlar.

Her bir RFQ servis talebi için bu ayarları gerektiğinde geçersiz kılabilirsiniz.

## <a name="creating-and-sending-an-rfq"></a>RFQ oluşturma ve gönderme

RFQ servis talebi oluşturmak için RFQ servis talebine teklif vermesini istediğiniz satıcıları seçin ve RFQ'ları bu satıcılara gönderin. RFQ raporunu ve yanıt sayfası raporlarını istediğiniz konuma yönlendirmek için Yazdırma ayarlarını kullanabilirsiniz.

**Satınalma siparişi** satın alma türü veya **Satınalma sözleşmesi** satın alma türü için RFQ servis talebini el ile oluşturabilirsiniz.

RFQ servis talebi **Satınalma siparişi** türünde olursa, diğer RFQ servis talebi türlerinden farklı olan aşağıdaki davranış ortaya çıkar:

- RFQ servis talebi satırları oluştururken, stok hareketleri giriş durumu **Teklif girişi** olan satırlar için oluşturulur.
- Bir teklifi kabul ettiğinizde satınalma sipariş oluşturulur.

RFQ servis talebi **Satınalma sözleşmesi** türünde olursa, diğer RFQ servis talebi türlerinden farklı olan aşağıdaki davranış ortaya çıkar:

- RFQ servis talebi, zaman içinde belirli bir miktarda veya değerde ürün satın almak üzere yapılan anlaşma için kullanılır. Satın alma anlaşması için geçerli tarih aralığını ve satınalma anlaşmasını yöneten kişinin adını girmeniz gerekir.
- Bir teklifi kabul ettiğinizde satınalma anlaşması oluşturulur.

RFQ servis talebi bir satınalma talebinden oluşturulursa **Satınalma talebi** türü otomatik olarak atanır. **Satınalma talebi** türü için RFQ servis talebini el ile oluşturamazsınız.

Yalnızca satınalma talebinin durumu **İncelemede** olduğunda bir satınalma talebinden RFQ servis talebi oluşturabilirsiniz ve bir sonraki iş akışı görevini yapmak üzere atanırsınız. Satıcılardan alınan tekliflerdeki (RFQ yanıtları) satırları kabul ettiğinizde, satınalma talebindeki satırlar otomatik olarak güncelleştirilir. Talep satırı kabul edilmiş bir RFQ satırıyla güncelleştirilene veya RFQ servis talebi iptal edilene kadar satınalma talebini tamamlayamaz, reddedemez, onaylayamaz veya üzerinde başka bir eylem gerçekleştiremezsiniz..

Bir RFQ servis talebi oluşturduğunuzda, bir talep türü seçebilirsiniz. Talep türü, RFQ servis talebine gelen RFQ yanıtlarını puanlamak için kullanabileceğiniz puanlama ölçütü kümesini belirler.

Bir RFQ servis talebine soru formu ekleyebilirsiniz. Bu soru formu RFQ gönderildikten sonra tüm RFQ yanıtlarında görüntülenir. Teklifin gönderilebilmesi için anketin tamamlanması zorunlu bir görevdir.

Varsayılanlar sağlansa da, her bir RFQ servis talebi için **Satıcı RFQ yanıt formlarına eklenen RFQ alanları** ayarlarını gereken şekilde değiştirebilirsiniz. Bunu yapmak için bir RFQ servis talebi oluşturun veya açın. Sonra, Eylem Bölmesinde **Teklif** sekmesini açın ve **Yanıtlar** bölümünde **RFQ yanıtı varsayılanlarını ayarla**'yı seçin. **Varsayılan teklif talebi yanıt alanları** iletişim kutusu açılır; bu iletişim kutusu satıcı RFQ yanıt formları için varsayılan değerler ayarlanırken olduğu gibi çalışır. Buradaki değişiklikleriniz yalnıza geçerli RFQ servis talebini etkileyecektir. Bu işlevi etkinleştirme ve nasıl çalıştığı hakkında ayrıntılı bilgi için bkz. [Satıcı RFQ yanıt formlarına dahil edilecek varsayılan alanları seçme](#default-reply-fields).

RFQ servis talebine eklenecek satıcılar üç yolla seçilebilir:

- Satıcıları tek tek ekleme.
- Belirli ölçütü karşılayan tüm satıcıları arama.
- RFQ servis talebi satırlarında kullanılan tedarik kategorileri için onaylanmış olan tüm satıcıları otomatik olarak ekleme.

RFQ servis talebi hazır olduğunda **Gönder**'i seçin. Gönder eylemi, Yazdırma ayarlarınıza göre yazdırılacak, arşivlenecek ve gönderilecek günlükler ve raporlar oluşturur.

**Teklif talebi gönderme** sayfasında **Fiyatları yeniden hesaplamak için satıcı kullan** ve **Satıcıya özgü madde bilgilerini kullan** seçeneklerini **Evet** olarak ayarladığınızda talebi satıcılara gönderirken satıcıya özgü bazı bilgiler bu satıcı için RFQ'ya otomatik olarak girilir.

## <a name="amending-an-rfq-case"></a>RFQ servis talebini düzeltme

Bazen, gönderdikten sonra RFQ servis talebinde düzeltme yapmanız gerekir. Örneğin teslimat tarihlerinin değişmesi veya ek ürünler ya da farklı ürün miktarları girmek istemeniz durumunda bir RFQ servis talebini değiştirmeniz gerekebilir. Düzeltme işlemini, daha kısıtlayıcı veya daha az kısıtlayıcı olacak şekilde yapılandırabilirsiniz.

Düzeltme işlemini daha kısıtlayıcı olacak şekilde yapılandırırsanız, zaten gönderilmiş olan bir RFQ servis talebindeki alanları değiştirebilmeniz için düzeltme işlemini başlatmak üzere RFQ'da **Oluştur**'u seçmeniz gerekir. Değişiklikleri tamamladıktan sonra **Sonlandır**'ı seçmeniz gerekir. Ardından, satıcıları düzeltme hakkında bilgilendirmek için gönderilecek e-postaya nasıl bilgi ekleneceği gösterilecektir. Bir düzeltme notu içeren güncelleştirilmiş RFQ raporu e-postaya otomatik olarak eklenir.

Düzeltme işlemini daha az kısıtlayıcı olacak şekilde yapılandırırsanız, zaten gönderilmiş olan bir RFQ'daki alanları değiştirebilmek için **Oluştur**'u seçmeniz gerekmez. Ancak, RFQ'ya el ile bir düzeltme notu eklemeniz ve servis talebini yeniden göndermeniz gerekir. Bu yöntemin yalnızca yanıtlardan (tekliflerden) hiçbirinin düzeltilmemiş olması durumunda kullanılabileceğini unutmayın. Bir yanıt girerseniz ve durumu **Alındı** olursa, **Gönder** düğmesi kullanılamaz. Böyle bir durumda, daha kısıtlayıcı bir işlem gerçekleştirmek zorunda olduğunuzdan **Oluştur**'u ve ardından **Sonlandır**'ı seçmeniz gerekir. Bundan sonra yanıt RFQ servis talebindeki değişiklikleri yansıtacak şekilde sıfırlanır.

Satıcılar teklifleri girmek için satıcı işbirliği arabirimini kullanırsa, satıcıları RFQ servis talebinde yapılan değişiklikler hakkında bilgilendirmek için her zaman düzeltme işlemini kullanmanız gerekir. Bu işlem, satıcıların teklifleri devam ederken eski bir RFQ servis talebine teklif vermeleri durumunu engellemeye yardımcı olur. Satıcı işbirliği işlevi hakkında daha fazla bilgi için bkz. [Harici satıcılarla için satıcı işbirliği](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Teklif vermek üzere ek satıcılar davet etmek isterseniz ve RFQ servis talebinde herhangi bir değişiklik yapılmadıysa **Gönder** düğmesini kullanabilirsiniz. Eklediğiniz satıcılar **Gönder** sayfasında görüntülenir ve e-posta davetini alır.

## <a name="receiving-and-registering-rfq-replies"></a>RFQ yanıtlarını alma ve kaydetme

Bir RFQ gönderdiğinizde, yanıt sayfası otomatik olarak oluşturulur. Bir RFQ için teklifleri aldığınızda, teklifleri **Teklif talebi** sayfasından **RFQ yanıtını düzenle** eylemini tıklayarak girmeniz gerekir. Bu, özel teklif formuna teklif bilgilerini girmenize olanak tanır. Başlangıçta, **Yanıt ilerlemesi** **Başlatılmadı** olacaktır. **RFQ yanıtını düzenle**'ye tıkladığınızda ilerleme durumu teklif gönderilene kadar **Satınalmacı güncelleştiriliyor** olur. Teklif bilgilerini girdiğinizde **Gönder**'e tıklayın. Yanıt İlerleme durumu **Satın alan kişi tarafından gönderildi** olarak değişir. Benzer şekilde, satıcı işbirliği etkinleştirildiğinde, **Yanıt ilerlemesi** satıcı teklifi ile etkileşim kurduğunda güncelleştirilir. Durum **Satıcı güncelleştiriyor** yerine **Satıcı tarafından gönderildi** olarak değişir. Teklif gönderildiğinde **Alındı** olarak bir günlük oluşturulur. Yanıt (teklif) alındı olarak kaydedilmesi için gönderilmelidir ve yalnızca bu aşamadan sonra kabul edildi veya reddedildi olarak işlenebilir.

Teklifi güncelleştirmeniz gerekiyorsa, yukarıdaki aynı işlemi tekrarlayın ve yeniden gönderin.

**Teklif talebi** formunu düzenlemeye yalnızca teklifin işlenmesiyle ilgili bilgiler için (teklifin girilmesiyle ilgili bilgiler değil) izin verilir. Teklifi girmek veya değiştirmek için **RFQ yanıtını düzenle**'ye tıklayın.

Teklif bilgilerini girdiğinizde ve RFQ servis talebi alternatif satırlara olanak tanıyorsa, yalnızca bir tedarik kategorisi olan ve katalog maddesi belirtilmemiş satırlar için alternatif satırlar ekleyebilirsiniz. Alternatif satırlar eklemek için **Alternatif ekle**'ye tıklayın.

Yanıtı girdiyseniz ancak satıcıdan yeni bir teklif istiyorsanız, RFQ'yu iade edebilirsiniz. Satıcıya gönderilebilecek yeni bir günlük ve rapor oluşturulur.

Tüm RFQ'ların genel görünümünü ve durumlarını (**Gönderildi, Alındı, Kabul edildi, Reddedildi, İptal edildi, Geri çevrildi**) **Teklif talebi izleme** sayfasından görebilirsiniz.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Teklifleri kabul etme ve reddetme ve kabul edilen teklifleri aşağı doğru belgelere aktarma

Örneğin en iyi toplam fiyatı sunan teklif gibi en iyi teklifi tanımladıktan sonra teklifi kabul edin. Bir teklifteki bazı satırları kabul edip diğerlerini reddedebilirsiniz.
Ayrıca, farklı satıcılardan gelen satırları da kabul edebilirsiniz. Bazı satırları kabul ettiğinizde, kalan diğer tüm satırları reddetmeniz istenebileceğini unutmayın. Bu nedenle, diğer satırları da kabul etmek isterseniz, istemi aldığınızda **İptal**'e tıklamanız gerekir. Teklifleri veya satırları kabul ettiğiniz her satıcı için RFQ yanıtı durumu **Kabul edildi** olarak güncelleştirilir.

Bir satınalma siparişi veya satınalma sözleşmesi hazırlarken RFQ'ya ek bir satır eklemeniz gerekirse, bunu **Teklif talebi** sayfası satır ızgarasındaki **Satır ekle**'ye tıklayarak yapabilirsiniz. Bu satırı yalnızca **Teklif talebi** sayfasından görebilir ve düzenleyebilirsiniz. Kabul edilmesi durumunda, fiyat teklifi sayfasında görünür.

Bir teklifi veya teklifteki bir veya daha fazla satırı kabul ettiğinizde, otomatik olarak bir satınalma siparişi veya satınalma anlaşması oluşturulur. Daha sonra diğer tüm satıcıların tekliflerini reddedebilirsiniz.

Yanıta, teklifi neden kabul ettiğinizi veya reddettiğinizi açıklayan bir neden kodu ekleyebilirsiniz.

**Satınalma talebi** türünde bir teklifi kabul ettiğinizde, satınalma talebi satırları kabul edilen teklif bilgilerini gösteren aşağıdaki bilgilerle güncelleştirilir:

- Birim fiyatı
- İskonto yüzdesi
- İskonto tutarı
- Satınalma masrafları
- Satır giderleri
- Satıcı
- Harici numara
- Harici tanım

Aşağıdaki tabloda, satıcılardan gelen teklifleri kabul ettiğinizde ve reddettiğinizde RFQ durumunun nasıl değiştiği gösterilmektedir.

## <a name="statuses--highest-and-lowest"></a>Durumlar – en yüksek ve en düşük

RFQ servis talebinin Satıcı sekmesinde, belirli bir satıcı için en yüksek ve en düşük durumdaki satırları görebilirsiniz. Satıcı eklendiğinde ve henüz hiçbir satır gönderilmediyse, hem en düşük hem de en yüksek durum <strong>Oluşturuldu</strong> olur. RFQ satıcıya tüm satırlarla gönderildiğinde, iki satırın durumu da <strong>Gönderildi</strong> olur. Satıcıdan gelen bir teklifteki bazı satırlar kabul edilir ve bazıları reddedilirse, reddedilen satırları en düşük durum olan <strong>Reddedildi</strong> durumunu, kabul edilen satırlar en yüksek durum olan <strong>Kabul edildi</strong> durumunu alır.

RFQ servis talebi satırlarında, tüm satıcılar için satır başına en yüksek ve en düşük durumu görebilirsiniz. RFQ servis talebindeki tüm satıcılara bir satır gönderirseniz ve henüz kimse yanıt vermediyse en düşük ve en yüksek durum **Gönderildi** olur. En az bir satıcı yanıtladığında, en yüksek durum **Alındı** olarak değişir. Servis talebine yeni bir satıcı eklerseniz, en düşük **Oluşturuldu** olarak değişir

RFQ servis talebinin en yüksek ve en düşük durumu \<Satıcı sekmesi ve Satırlar sekmesindeki durumun toplamıdır.

Durumlar şu şekilde en düşükten en yükseğe doğru sıralanır: Oluşturuldu, Gönderildi, Alındı, Reddedildi, Kabul edildi, Geri çevrildi, İptal edildi.

Aşağıdaki tablo, satırlar içeren bir RFQ servis talebi oluşturup satıcılara gönderdiğinizde, RFQ servis talebi durumunun nasıl değiştiğini göstermektedir.

| **İşlem**                                | **En düşük RFQ servis talebi durumu** | **En yüksek RFQ servis talebi durumu** | **En düşük RFQ servis talebi satırı durumu** | **En yüksek RFQ servis talebi satırı durumu** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| RFQ servis talebi başlığı ve satırı oluşturun.      | Oluşturma                    | Oluşturma                     | Oluşturma                         | Oluşturma                          |
| RFQ'ları RFQ servis talebindeki tüm satıcılara gönderin. | Gönderildi                       | Gönderildi                        | Gönderildi                            | Gönderildi                             |
| Başka satıcı ekleyin.                       | Oluşturma                    | Gönderildi                        | Oluşturma                         | Gönderildi                             |
| RFQ'yu ikinci satıcıya gönderin.        | Gönderildi                       | Gönderildi                        | Gönderildi                            | Gönderildi                             |

RFQ'daki RFQ servis talebiyle ilgili tüm satırlar **Gönderildi** durumunda olacaktır.

Aşağıdaki tablo, teklifleri aldığınızda ve bilgileri RFQ yanıt sayfasına girdiğinizde RFQ durumunun nasıl değiştiğini göstermektedir.

| **İşlem**                                               | **Tüm RFQ'lardaki tüm satırlarda en düşük durum** | **Tüm RFQ'lardaki tüm satırlarda en yüksek durum** | **En düşük RFQ servis talebi başlığı durumu** | **En yüksek RFQ servis talebi başlığı durumu** | **En düşük RFQ servis talebi satırı durumu** | **En yüksek RFQ servis talebi satırı durumu** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Bir satıcının RFQ'ya teklifini girin ve kaydedin.        | Gönderildi                                           | Alınan                                        | Gönderildi                              | Alınan                           | Gönderildi                            | Alınan                         |
| İkinci satıcının RFQ'ya teklifini girin ve kaydedin. | Alınan                                       | Alınan                                        | Alınan                          | Alınan                           | Alınan                        | Alınan                         |


Aşağıdaki örnekte, bir teklifin alındığı ve başka bir teklifin kabul edildiği RFQ servis talebinde en yüksek ve en düşük durumu görebilirsiniz. Alınan bir teklif reddedildiğinde, en düşük durum RFQ servis talebi başlığı ve satırı üzerinde alındı yerine reddedildi olarak değişir.


|            <strong>İşlem</strong>             | <strong>Tüm RFQ'lardaki tüm satırlarda en düşük durum</strong> | <strong>Tüm RFQ'lardaki tüm satırlarda en yüksek durum</strong> | <strong>En düşük RFQ servis talebi başlığı durumu</strong> | <strong>En yüksek RFQ servis talebi başlığı durumu </strong> | <strong>En düşük RFQ servis talebi satırı durumu</strong> | <strong>En yüksek RFQ servis talebi satırı durumu</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Tekliflerden birini kabul edin. (veya en az bir satır gereklidir) |                          Alınan                           |                           Kabul Edildi                           |                    Alınan                    |                    Kabul Edildi                     |                   Alınan                   |                   Kabul Edildi                    |
|           Diğer tüm teklifleri reddedin.           |                          Reddedildi                           |                           Kabul Edildi                           |                    Reddedildi                    |                    Kabul Edildi                     |                   Reddedildi                   |                   Kabul edildi                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]