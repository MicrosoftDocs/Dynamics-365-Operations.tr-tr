---
title: Teklif talepleri (RFQ)
description: "Bu konuda, teklif taleplerine (RFQ) genel bakış sağlanmaktadır. Kuruluşlar, satın almak zorunda oldukları maddeler veya hizmetler için çeşitli satıcılardan rekabetçi teklifler almak istediklerinde RFQ'lar yayınlar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b86363004b8702d1a654f2a1da49bba82fc8ff2a
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="requests-for-quotation-rfqs"></a>Teklif talepleri (RFQ)

[!include[banner](../includes/banner.md)]

Bu konuda, teklif taleplerine (RFQ) genel bakış sağlanmaktadır. Kuruluşlar, satın almak zorunda oldukları maddeler veya hizmetler için çeşitli satıcılardan rekabetçi teklifler almak istediklerinde RFQ'lar yayınlar. Bir RFQ'da, satıcılardan belirlediğiniz madde miktarları için fiyat ve teslimat süreleri vermelerini istersiniz. Satıcılardan, nakliye maliyetleri ya da büyük siparişler için indirimler veya satıcı faturalarının erken ödenmesi gibi dolaylı giderler olup olmadığını belirtmelerini de isteyebilirsiniz.

RFQ işlemi aşağıdaki görevlerden oluşur:

1. RFQ oluşturma ve bir veya daha çok satıcıya gönderme.
2. RFQ yanıtlarını (teklifler) alma ve kaydetme.
3. Kabul edilen teklifleri satınalma siparişine, satınalma anlaşmasına veya satınalma talebine aktarma.

Aşağıdaki örnekte teklif talebi sürecine genel bakış verilmektedir.

[![RFQ işlemi](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Planlanan siparişlerden, satınalma talebinden veya el ile yapılan bir girişten bir RFQ oluşturabilirsiniz. Oluşturduğunuz RFQ'ya RFQ servis talebi adı verilir. RFQ servis talebi, her satıcıya bir RFQ vermek için kullandığınız temel belgedir.

RFQ servis talebini hazırlayıp satıcılar ekledikten sonra RFQ servis talebinde **Gönder**'i seçin. RFQ gönderdiğiniz her satıcı için bir RFQ günlüğü oluşturulur. Gönder eylemi için Yazdırma yönetimi ayarlarını her satıcı için arşive gönderilecek bir rapor yazdıracak veya her satıcının e-posta adresine bir rapor gönderecek şekilde ayarlayabilirsiniz. Ayrıca, her satıcıya ilişkin RFQ günlüğü, satıcıya daha sonra gönderebileceğiniz veya yeniden gönderebileceğiniz bir rapor oluşturmak için kullanılabilir. Gönder eylemini, satıcının dolduracağı bir yanıt sayfası oluşturmak için de yapılandırabilirsiniz.

Bu konu, satıcı işbirliği kullanılmadığında RFQ'ların işlenmesine ilişkin süreci kapsar. Sisteminiz satıcı işbirliği için ayarlanmışsa, satıcılar teklifleri doğrudan Microsoft Dynamics 365 for Finance and Operations'dan girebilir. Daha fazla bilgi için bkz. [Müşterilerle satıcı işbirliği](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Gönderdikten sonra bir RFQ'da düzeltme yapmanız gerekirse, RFQ'yu işleminizi tamamladıktan sonra satıcılara iki düzeltme eylemini kullanarak gönderebilirsiniz: Oluştur ve Sonlandır.

Teklifleri e-posta ile aldığınızda, bunları **Teklif talebi yanıtları** sayfasına girmeniz gerekir. **Veriler yanıta kopyala** seçeneğini seçerseniz, RFQ servis talebindeki miktar ve tarih gibi veriler yanıta kopyalanır. Bu verileri satıcının teklifini yansıtacak şekilde değiştirebilirsiniz.

Bir satıcı için yanıtın ikinci defa yinelenmesi gerekirse, **Teklif talebi yanıtı** sayfasında **İade et**'e tıklayın. İade eylemi yeni bir günlük oluşturur ve Yazdırma yönetimi ayarlarınıza göre bir rapor yazdırılır, arşivlenir ve gönderilir.

RFQ servis talebine puanlama ölçütü eklediyseniz, RFQ yanıtında puanlama girebileceğiniz bir puanlama paneli bulunur. **Yanıtları karşılaştır** sayfasında yanıtları karşılaştırdığınızda toplam puanlar görüntülenir. Bu sayfada satır fiyatı, toplam fiyat ve teslimat tarihi gibi diğer yanıt verilerini de karşılaştırabilirsiniz.

Bir teklifi veya kısmi teklifleri seçtikten sonra, bunları kabul edip geri kalanları reddedebilirsiniz. Kabul etme günlükleri, reddetme günlükleri ve ilgili raporlar oluşturulur ve Yazdırma yönetimi ayarlarınıza göre yazdırılır, arşivlenir ve gönderilir. Bir teklifi veya bir teklifteki belirli satırları kabul ettiğinizde, bir satınalma anlaşması veya satınalma siparişi oluşturulur ya da RFQ satınalma türüne göre satınalma talebi güncelleştirilir. Kabul edip etmediğinize bakılmaksızın, herhangi bir yanıt için daha sonra kullanabileceğiniz bir ticari anlaşma oluşturabilirsiniz.

Bir RFQ durumu RFQ başlığında görüntülenir ve RFQ satırlarının durumuna bağlıdır. Durum, işleme aldığınız RFQ kapsamını gösterir. Her RFQ'da durum için iki değer vardır: en düşük durum ve en yüksek durum. En düşük durum RFQ'daki herhangi bir satırın en az gelişmiş aşamasıdır; en yüksek durum RFQ'daki herhangi bir satırın en ileri aşamasıdır. Örneğin, RFQ'daki en az ilerlemiş aşama oluşturulan bir satırla ilişkiliyse RFQ için en düşük durum **Oluşturuldu** olur. RFQ'daki en ileri aşama satıcılara gönderilen bir satırla ilişkiliyse RFQ için en yüksek durum **Gönderildi** olur. Bir RFQ'yu işlediğinizde durumlar otomatik olarak güncelleştirilir.

RFQ başlığı için en düşük ve en yüksek durumlarını **Tüm teklif talepleri** sayfasında görebilirsiniz. RFQ satırı için en düşük ve en yüksek durumlarını **Tüm teklif talepleri** sayfasındaki **Satırlar** sekmesinde görebilirsiniz.

Bir RFQ'yu işlemeyle ilgili durum serisi aşağıdaki gibidir:

1. **Oluşturuldu**
2. **Gönderildi**
3. **Alındı**
4. **Kabul edildi**, **İptal edildi** veya **Reddedildi**

Bu durumlar, bu konuda daha ayrıntılı açıklanacaktır.

## <a name="setting-up-rfq-functionality"></a>RFQ işlevini ayarlama

Bir RFQ servis talebi oluşturmadan önce **Tedarik ve kaynak atama parametreleri** sayfasında RFQ bilgilerini ayarlamanız gerekir. RFQ servis talebi oluşturduğunuzda, RFQ'ya kopyalanan varsayılan değerleri belirtebilirsiniz. Aşağıdaki varsayılan değerleri belirtebilirsiniz:

- Yeni RFQ'nun satınalma türü: **Satınalma siparişi** veya **Satınalma anlaşması**
- Bitiş tarihi ve saati
- Teslimat bilgileri ve ödeme koşulları
- RFQ yanıtına dahil edilmesi gereken alanlar

Bu değerleri belirli bir RFQ için geçersiz kılabilirsiniz.

Düzeltme işlemini de yapılandırmanız gerekir. Bu yapılandırma işleminin bir parçası olarak, alan kilidini açabilirsiniz. Alan kilitleme açık olduğunda, RFQ düzenlemek isteyen bir satınalma uzmanı önce **Teklif** sekmesinin **Değişiklik** bölümündeki **Oluştur** üzerine tıklamalıdır. RFQ değişiklik ile güncelleştirildikten sonra, satınalma uzmanı işlemi **Sonlandır** üzerine tıklayarak tamamlamalıdır. Sonlandır eylemi, satıcıları düzeltilen RFQ hakkında bilgilendiren bir e-posta oluşturur.

**Tedarik ve kaynak atama parametreleri** sayfasından satıcılara gönderilecek e-posta bildirimi için kullanılacak şablonu seçebilirsiniz. Bir şablon oluşturulduğunda aşağıdaki değiştirme belirteçlerini içerebilir:

- %RFQ servis talebi%
- %Teklifi iade nedeni%
- %Düzeltme yapma nedeni%
- %Düzeltmeyi yapan%
- %Şirket%
- %RFQ servis talebi adı%
- % ExpiryDateTime %
- %Tarih%

%Teklifi iade nedei% ve %Düzeltme yapma nedeni% belirteçleri, tedarik uzmanının **Düzeltme** sihirbazında düzeltme işlemini tamamlarken girebileceği metinle değiştirilir. %Düzeltmeyi yapan% ve %Şirket% belirteçleri otomatik olarak RFQ'dan alınır. %Tarih% belirteci geçerli tarih ile değiştirilir.

Bir RFQ'yu gönderildikten sonra iptal etmeniz durumunda da bir e-posta şablonu gerekir. Bu e-posta şablonu iptal bildirimini satıcının ilgili kişilerine göndermek için kullanılır. Şablonu **Tedarik ve kaynak atama parametreleri** sayfasından seçilmelidir. Şablon oluşturulduğunda aşağıdaki değiştirme belirteçlerini içerebilir:

- %İptal sebebi%
- %RFQ servis talebi% 
- %RFQ'yu iptal eden%
- %Şirket%
- %RFQ servis talebi adı%
- %Tarih%

%İptal sebebi% belirteci, tedarik uzmanının **İptal** sihirbazına girebileceği bir metin ile değiştirilir. %Tarih% belirteci geçerli tarih ile değiştirilir.

RFQ yanıtında, teklifin neden reddedildiği veya kabul edildiğini belirtmek için neden kodları kullanmak isterseniz, **Satıcı nedenleri** sayfasında neden kodları ayarlamanız gerekir.

Tedarik ve kaynak atamadaki **Form ayarı** sayfasında yazdırılan veya depolanan RFQ belgelerinizin görünümünü yapılandırabilirsiniz.

> [!NOTE]
> Kamu sektörü yapılandırması için, gönderilen bir RFQ'da değişiklik yapmak için düzeltme işlemini kullanmanız gerekir. Bir RFQ gönderildiğinde alanlar kilitlenir. Bu nedenle, RFQ'da değişiklik yapmak için daha önce açıklandığı şekilde düzeltme işlemini başlatmak üzere **Oluştur**'u seçmeniz gerekir. Kilitleme davranışı **Tedarik ve kaynak atama parametreleri** sayfasındaki **RFQ'yi gönderildiğinde kilitle** seçeneğiyle kontrol edilir. Varsayılan olarak bu parametre **Evet** olarak ayarlanır ve kamu sektörü yapılandırmasında varsayılan ayar değiştirilemez. Bu nedenle, kamu sektörü dışındaki yapılandırmada düzeltme işlemi el ile gerçekleştirilebilmesine karşın, kamu sektörü yapılandırması için kullanılmak zorundadır.

Bir satınalma sipariş iiçin RFQ oluşturduğunuzda ve RFQ'ya bir stok maddesi eklediğinizde, giriş durumu **Teklif girişi** olan bir stok hareketi oluşturulur. Malzemeleri hesaplamak için bir master plan kullandığınızda yalnızca bu duruma sahip RFQ satırları göz önünde bulundurulur. Master planın RFQ satırlarını beklenen giriş olarak eklemesini istiyorsanız, master plan ayarlama aşamasında bu davranışı yapılandırmanız gerekir.

Bir satınalma yöneticisi veya temsilcisi, kuruluşun tedarik gereksinimlerine uyacak talep türleri oluşturup bunları koruyabilir. Her istek türü bir puanlama yöntemiyle ilişkilendirilebilir. Puanlama yöntemleri, teklifleri puanlarken kullanabileceğiniz ölçüt kümesinden oluşur. Talep türlerini, puanlama yöntemlerini ve puanlama ölçütünü **Talep türü** ve **Puanlama yöntemi** sayfalarından ayarlamanız gerekir.

## <a name="creating-and-sending-an-rfq"></a>RFQ oluşturma ve gönderme

RFQ oluşturmak için RFQ'ya teklif vermesini istediğiniz satıcıları seçin ve RFQ'yu bu satıcılara gönderin. RFQ raporunu ve yanıt sayfası raporlarını istediğiniz konuma yönlendirmek için Yazdırma yönetimini kullanabilirsiniz.

**Satınalma siparişi** satın alma türü veya **Satınalma sözleşmesi** satın alma türü için RFQ oluşturabilirsiniz.

RFQ **Satınalma siparişi** türünde olursa aşağıdaki davranış gerçekleşir:

- RFQ satırları oluştururken, stok hareketleri giriş durumu **Teklif girişi** olan satırlar için oluşturulur.
- Bir teklifi kabul ettiğinizde satınalma sipariş oluşturulur.

RFQ **Satınalma sözleşmesi** türünde olursa aşağıdaki davranış gerçekleşir:

- RFQ, zaman içinde belirli bir miktarda veya değerde ürün satın almak üzere yapılan anlaşma için kullanılır. Satın alma anlaşması için geçerli tarih aralığını ve satınalma anlaşmasını yöneten kişinin adını girmeniz gerekir.
- Bir teklifi kabul ettiğinizde satınalma anlaşması oluşturulur.

RFQ bir satınalma talebinden oluşturulursa **Satınalma talebi** türü otomatik olarak atanır. **Satınalma talebi** türü için RFQ'yu el ile oluşturamazsınız.

Yalnızca satınalma talebinin durumu **İncelemede** olduğunda bir satınalma talebinden RFQ oluşturabilirsiniz ve bir sonraki iş akışı görevini yapmak üzere atanırsınız. Satıcılardan alınan RFQ yanıtlarındaki (teklifleri) satırları kabul ettiğinizde, satınalma talebindeki satırlar otomatik olarak güncelleştirilir. RFQ işlenirken satınalma talebini tamamlayamaz, reddedemez, onaylayamaz veya üzerinde herhangi başka işlem yapamazsınız.

Bir RFQ oluşturduğunuzda, bir talep türü seçebilirsiniz. Talep türü, RFQ'ya gelen yanıtları puanlamak için kullanabileceğiniz puanlama ölçütü kümesini belirler.

Bir RFQ servis talebine soru formu ekleyebilirsiniz. Bu soru formu RFQ gönderildikten sonra tüm yanıtlarda görüntülenir.

RFQ servis talebine eklenecek satıcılar üç yolla seçilebilir:

- Satıcıları tek tek ekleme.
- Belirli ölçütü karşılayan tüm satıcıları arama.
- RFQ satırlarında kullanılan tedarik kategorileri için onaylanmış olan tüm satıcıları otomatik olarak ekleme.

RFQ servis talebi hazır olduğunda **Gönder**'i seçin. Gönder eylemi, Yazdırma yönetimi ayarlarınıza göre yazdırılacak, arşivlenecek ve gönderilecek günlükler ve raporlar oluşturur.

**Teklif talebi gönderme** sayfasında **Fiyatları yeniden hesaplamak için satıcı kullan** ve **Satıcıya özgü madde bilgilerini kullan** seçeneklerini **Evet** olarak ayarladığınızda talebi satıcılara gönderirken satıcıya özgü bazı bilgiler otomatik olarak girilir. Bu bilgiler üzerinde **Teklif talebi yanıtı** sayfasından değişiklik yapabilirsiniz.

Aşağıdaki tablo, bri RFQ oluşturup satıcılara gönderdiğinizde, RFQ durumunun nasıl değiştiğini göstermektedir.

| Eylem                             | En düşük RFQ başlığı durumu | En yüksek RFQ başlığı durumu                        | En düşük RFQ satırı durumu | En yüksek RFQ satırı durumu |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| RFQ başlığı ve satırı oluşturun.    | Oluşturulma                  | Oluşturulma                                          | Oluşturulma                | Oluşturulma |
| RFQ'yu belirli bir satıcıya gönderin. | Gönderildi                     | Gönderildi                                             | Gönderildi                   | Gönderildi |
| Başka satıcı ekleyin.                | Oluşturulma                  | Gönderildi (RFQ yalnızca tek bir satıcıya gönderilmiştir.) | Oluşturma                | Gönderildi |
| RFQ'yu ikinci satıcıya gönderin. | Gönderildi                     | Gönderildi                                             | Gönderildi                   | Gönderildi |

> [!NOTE]
> RFQ'ya istediğiniz zaman daha fazla satıcı ekleyebilirsiniz; en düşük ve en yüksek durumları yeni satıcıları yansıtacak şekilde güncelleştirilir. Örneğin, tüm satıcılardan teklif alır ve teklifteki en az bir satırı kabul ederseniz, RFQ başlığındaki en düşük durum **Reddedildi** ve en yüksek durum **Kabul edildi** olur. Yeni bir satıcı eklerseniz, herhangi bir satırdaki en düşük durum **Oluşturuldu** olur. Bu nedenle, RFQ başlığındaki en düşük durum **Oluşturuldu** olarak güncelleştirilir ve en yüksek durum **Kabul edildi** olarak kalır.

## <a name="amending-an-rfq"></a>RFQ'yu düzeltme

Bazen, gönderdikten sonra RFQ'da düzeltme yapmanız gerekir. Örneğin teslimat tarihlerinin değişmesi veya ek ürünler ya da farklı ürün miktarları girmek istemeniz durumunda bir RFQ'yu değiştirmeniz gerekebilir. Düzeltme işlemini, daha kısıtlayıcı veya daha az kısıtlayıcı olacak şekilde yapılandırabilirsiniz.

Düzeltme işlemini daha kısıtlayıcı olacak şekilde yapılandırırsanız, zaten gönderilmiş olan bir RFQ servis talebindeki alanları değiştirebilmeniz için düzeltme işlemini başlatmak üzere RFQ'da **Oluştur**'u seçmeniz gerekir. Değişiklikleri tamamladıktan sonra **Sonlandır**'ı seçmeniz gerekir. Ardından, satıcıları düzeltme hakkında bilgilendirmek için gönderilecek e-postaya nasıl bilgi ekleneceği gösterilecektir. Bir düzeltme notu içeren güncelleştirilmiş RFQ raporu e-postaya otomatik olarak eklenir.

Düzeltme işlemini daha az kısıtlayıcı olacak şekilde yapılandırırsanız, zaten gönderilmiş olan bir RFQ'daki alanları değiştirebilmek için **Oluştur**'u seçmeniz gerekmez. Ancak, RFQ'ya el ile bir düzeltme notu eklemeniz ve servis talebini yeniden göndermeniz gerekir. Bu yöntemin yalnızca yanıtlardan (tekliflerden) hiçbirinin düzeltilmemiş olması durumunda kullanılabileceğini unutmayın. Bir yanıt girerseniz ve durumu **Alındı** olursa, **Gönder** düğmesi kullanılamaz. Böyle bir durumda, daha kısıtlayıcı bir işlem gerçekleştirmek zorunda olduğunuzdan **Oluştur**'u ve ardından **Sonlandır**'ı seçmeniz gerekir. Bundan sonra yanıt RFQ servis talebindeki değişiklikleri yansıtacak şekilde sıfırlanır. 

Satıcılar teklifleri girmek için satıcı işbirliği arabirimini kullanırsa, satıcıları RFQ servis talebinde yapılan değişiklikler hakkında bilgilendirmek için her zaman düzeltme işlemini kullanmanız gerekir. Bu gereksinim, satıcıların teklifleri devam ederken eski bir RFQ servis talebine teklif vermeleri durumunu engellemeye yardımcı olur. Satıcı işbirliği işlevi hakkında daha fazla bilgi için bkz. [Harici satıcılarla için satıcı işbirliği](vendor-collaboration-work-external-vendors.md). 

Teklif vermek üzere ek satıcılar davet etmek isterseniz ve RFQ servis talebinde herhangi bir değişiklik yapılmadıysa **Gönder** düğmesini kullanabilirsiniz. Eklediğiniz satıcılar **Gönder** sayfasında görüntülenir ve e-posta davetini alır.

## <a name="receiving-and-registering-rfq-replies"></a>RFQ yanıtlarını alma ve kaydetme

Bir RFQ gönderdiğinizde, yanıt sayfası otomatik olarak oluşturulur. RFQ yanıtları (teklifleri) aldığınızda, her satıcıdan gelen bilgileri satıcıya özel bir RFQ yanıt sayfasına girmeniz gerekir. Puanlama ölçütü eklediyseniz, yanıtları puanlayabilirsiniz. Ardından satıcı teklifleri karşılaştırabilir ve puanlama ölçütünüze göre (en iyi toplam fiyat veya en iyi teslim tarihi gibi) derecelendirebilirsiniz.

RFQ servis talebine bir soru formu eklendiyse, sorulara gelen yanıtları yanıt sayfasına el ile girmeniz gerekir.

RFQ servis talebi alternatif satırlara izin veriyorsa başka satırlar da girebilirsiniz. **Satınalma teklifi satırları** hızlı sekmesinde **Satır ekle**'yi seçin. Ardından madde numarası, tedarik kategorisi, miktar, fiyat ve iskonto gibi ürün bilgilerini girin.

Yanıtı girdiyseniz ancak satıcıdan yeni bir teklif istiyorsanız, RFQ'yu yeniden gönderebilirsiniz. Yeni bir günlük veya rapor oluşturacaktır. Bunları satıcıdan değişiklik istemek için kullanabilirsiniz.

Tüm RFQ'ların genel görünümünü ve yanıt durumlarını **Teklif talebi izleme** sayfasından görebilirsiniz.

Aşağıdaki tablo, teklifleri aldığınızda ve bilgileri RFQ yanıt sayfasına girdiğinizde RFQ durumunun nasıl değiştiğini göstermektedir.

| Eylem                                         | En düşük teklif durumu | En yüksek teklif durumu | En düşük RFQ başlığı durumu | En yüksek RFQ başlığı durumu | En düşük RFQ satırı durumu | En yüksek RFQ satırı durumu |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Bir satıcının teklifini girin ve kaydedin.        | Gönderildi              | Alınan           | Gönderildi                     | Alınan                  | Gönderildi                   | Alınan |
| İkinci satıcının teklifini girin ve kaydedin. | Alınan          | Alınan           | Alınan                 | Alınan                  | Alınan               | Alınan |

> [!NOTE]
> Bir teklifi ek görüşme için satıcıya geri gönderirseniz, en düşük ve en yüksek durumları **Alındı** olarak kalır.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Teklifleri kabul etme ve reddetme ve kabul edilen teklifleri aşağı doğru belgelere aktarma

Örneğin en iyi toplam fiyatı sunan teklif gibi en iyi teklifi tanımladıktan sonra teklifi kabul edin. Bir teklifteki bazı satırları kabul edip diğerlerini reddedebilirsiniz. Ayrıca, farklı satıcılardan gelen satırları da kabul edebilirsiniz. Bazı satırları kabul ettiğinizde, kalan diğer tüm satırları reddetmeniz istenebileceğini unutmayın. Bu nedenle, diğer satırları da kabul etmek isterseniz, istemi aldığınızda **İptal**'e tıklamanız gerekir. Teklifleri veya satırları kabul ettiğiniz her satıcı için RFQ yanıtı durumu **Kabul edildi** olarak güncelleştirilir. 

Bir teklifi veya teklifteki belirli satırları kabul ettiğinizde, otomatik olarak bir satınalma siparişi veya satınalma anlaşması oluşturulur. Daha sonra diğer tüm satıcıların tekliflerini reddedebilirsiniz.

Yanıta, teklifi neden kabul ettiğinizi veya reddettiğinizi açıklayan bir neden kodu ekleyebilirsiniz.

**Satınalma talebi** türünde RFQ yanıtını kabul ettiğinizde, RFQ yanıt satırları satınalma talebi satırlarını aşağıdaki bilgilerle güncelleştirir:

- Birim fiyat
- İskonto yüzdesi
- İskonto tutarı
- Satınalma masrafları
- Satır giderleri
- Satıcı
- Harici numara
- Harici tanım

Aşağıdaki tabloda, satıcılardan gelen teklifleri kabul ettiğinizde ve reddettiğinizde RFQ durumunun nasıl değiştiği gösterilmektedir.

| Eylem                      | En düşük teklif durumu | En yüksek teklif durumu | En düşük RFQ başlığı durumu | En yüksek RFQ başlığı durumu | En düşük RFQ satırı durumu | En yüksek RFQ satırı durumu |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Tekliflerden birini kabul edin.     | Alınan          | Kabul Edildi           | Alınan                 | Kabul Edildi                  | Alınan               | Kabul Edildi |
| Diğer tüm teklifleri reddedin.  | Reddedildi          | Kabul Edildi           | Reddedildi                 | Kabul Edildi                  | Reddedildi               | Kabul edildi |

