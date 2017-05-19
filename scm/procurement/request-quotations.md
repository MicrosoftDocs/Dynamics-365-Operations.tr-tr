---
title: Teklif talepleri (RFQ&quot;lar)
description: "Bu makalede, madde veya hizmet satın almak zorunda olduklarında ve sayısız satıcıdan rekabetçi teklifler almak istediklerinde kuruluşların çıkardığı teklif taleplerine (RFQ&quot;ler) genel bakış sunulmuştur. Bir RFQ&quot;da, satıcılardan belirlediğiniz madde miktarları için fiyat ve teslimat süreleri vermelerini istersiniz. Satıcılardan, nakliye maliyetleri ya da büyük siparişler için indirimler veya satıcı faturalarının erken ödenmesi gibi dolaylı giderler olup olmadığını belirtmelerini de isteyebilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 20ad50ab5c2dddf4fe07ebb5bb940954c0408f8d
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="request-for-quotations-rfqs"></a>Teklif talepleri (RFQ'lar)

[!include[banner](../includes/banner.md)]


Bu makalede, madde veya hizmet satın almak zorunda olduklarında ve sayısız satıcıdan rekabetçi teklifler almak istediklerinde kuruluşların çıkardığı teklif taleplerine (RFQ'ler) genel bakış sunulmuştur. Bir RFQ'da, satıcılardan belirlediğiniz madde miktarları için fiyat ve teslimat süreleri vermelerini istersiniz. Satıcılardan, nakliye maliyetleri ya da büyük siparişler için indirimler veya satıcı faturalarının erken ödenmesi gibi dolaylı giderler olup olmadığını belirtmelerini de isteyebilirsiniz.

Teklif talebi (RFQ) işlemi aşağıdaki görevleri kapsar:

-   Bir veya daha çok satıcı için RFQ oluşturma ve gönderme
-   RFQ yanıtlarını (teklifler) alma ve kaydetme
-   Kabul edilen teklifleri satınalma siparişine, satınalma anlaşmasına veya satınalma talebine aktarma

Aşağıdaki şekilde teklif talebi sürecinin genel özet verilmektedir.  

[![Teklif talebi işlemi](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Planlanan siparişlerden, satınalma talebinden veya el ile yapılan bir girişten bir RFQ oluşturabilirsiniz. Oluşturduğunuz RFQ'ye RFQ servis talebi denir ve bu, her satıcı için RFQ düzenlerken kullandığınız temel belgedir. RFQ olayını hazırlayıp satıcıları ekledikten sonra RFQ olayında **Gönder**'e tıklayın, RFQ günlüğü RFQ'yu gönderdiğiniz her satıcı için oluşturulur. Gönder eylemi için yazdırma yönetimi ayarlarını her satıcı için arşive gönderilecek bir rapor yazdıracak veya her satıcının epostasına adresine bir rapor gönderecek şekilde ayarlayabilirsiniz. Ayrıca, her satıcıya ilişkin RFQ günlüğü, satıcıya daha sonra gönderebileceğiniz veya yeniden gönderebileceğiniz bir rapor oluşturmak için kullanılabilir. Gönder eylemini, satıcının dolduracağı bir yanıt sayfası oluşturmak için de yapılandırabilirsiniz.  

Bir RFQ'da gönderdikten sonra değişiklik yapmak isterseniz, değişikliği tamamladıktan sonra RFQ'yu satıcılara tekrar gönderebilirsiniz.  

Teklifleri aldığınızda, bunları **Teklif talebi yanıtları** sayfasına girmeniz gerekir. **Veriler yanıta kopyala** seçeneğini seçerseniz, RFQ servis talebindeki miktar ve tarih gibi veriler yanıta kopyalanır. Bu verileri satıcının teklifini yansıtacak şekilde değiştirebilirsiniz.  

Belirli bir satıcı için yanıtın ikinci defa yinelenmesi gerekirse, **Teklif talebi yanıtı** sayfasında **İade et**'e tıklayın. İade eylemi yeni bir günlük oluşturur ve yazıcı ayarlarınıza göre bir rapor yazdırılır, arşivlenir ve gönderilir.  

RFQ servis talebine puanlama ölçütü eklediyseniz, RFQ yanıtında puanlama girebileceğiniz bir puanlama paneli bulunur. Toplam puanlar **Yanıtları karşılaştır** sayfasında yanıtları karşılaştırdığınızda görüntülenir. Bu sayfada satır fiyatı, teslim tarihi ve toplam fiyat gibi diğer yanıt verilerini de karşılaştırabilirsiniz.  

Bir teklife veya kısmi tekliflere karar verdikten sonra, bunları kabul edip geri kalanları reddedebilirsiniz. Kabul günlükleri, reddetme günlükler ve ilgili raporlar oluşturulur. Bunlar yazıcı ayarlarınıza bağlı olarak yazdırılır, arşivlenir ve gönderilir. Bir teklifi veya bir teklifteki belirli satırları kabul ettiğinizde, bir satınalma anlaşması veya satınalma siparişi oluşturulur ya da RFQ satınalma türüne göre satınalma talebi güncelleştirilir. Kabul edip etmediğinize bakılmaksızın, herhangi bir yanıt için daha sonra kullanabileceğiniz bir ticari anlaşma oluşturabilirsiniz.  

Bir RFQ durumu RFQ başlığında görüntülenir ve RFQ satırlarının durumuna bağlıdır. Durum, işleme aldığınız RFQ'nun kapsamını gösterir. Her RFQ'da durum için iki değer vardır: en düşük ve en yüksek. En düşük durum RFQ'daki herhangi bir satırın en az gelişmiş aşamasıdır; en yüksek durum RFQ'daki herhangi bir satırın en ileri aşamasıdır. Örneğin, RFQ'daki en az ilerlemiş aşama oluşturulan bir satırla ilişkiliyse RFQ için en düşük durum **Oluşturuldu** olur. RFQ'daki en ileri aşama satıcılara gönderilen bir satırla ilişkiliyse RFQ için en yüksek durum **Gönderildi** olur. Bir RFQ'yu işlediğinizde durumlar otomatik olarak güncelleştirilir.  

RFQ başlığı için en düşük ve en yüksek durumlarını **Tüm teklif talepleri** sayfasında görebilirsiniz. RFQ satırı için en düşük ve en yüksek durumlarını **Tüm teklif talepleri** sayfasındaki **Satırlar** sekmesinde görebilirsiniz.  

Bir RFQ'yu işlemeyle ilgili durum serisi aşağıdaki gibidir:

1.  **Oluşturuldu**
2.  **Gönderildi**
3.  **Alındı**
4.  **Kabul edildi**/**iptal edildi**/**Reddedildi**

Bu durumlar, bu makalenin ilerleyen bölümünde daha ayrıntılı açıklanacaktır.

## <a name="setting-up-rfq-functionality"></a>RFQ işlevini ayarlama
Bir RFQ servis talebi oluşturmadan önce **Tedarik ve kaynak atama parametreleri** sayfasında RFQ bilgilerini ayarlamanız gerekir. RFQ servis talebi oluşturduğunuzda, RFQ'ya kopyalanan varsayılan değerleri belirtebilirsiniz. Aşağıdaki varsayılan değerleri belirtebilirsiniz:

-   Yeni RFQ'nun satınalma türü: **Satınalma siparişi** veya **Satınalma anlaşması**
-   Bitiş tarihi ve saati ayarları
-   Teslimat bilgileri ve ödeme koşulları.
-   RFQ yanıtına dahil edilmesi gereken alanlar

Bu değerleri belirli bir RFQ için geçersiz kılabilirsiniz. Düzeltme işlemini de yapılandırmanız gerekir. Bu yapılandırma işleminin bir parçası olarak, alan kilidini açabilirsiniz. Alan kilitleme açık olduğunda, RFQ üzerinde düzeltme yapmak isteyen bir tedarik uzmanının önce **Teklif** sekmesinin **Düzeltme** bölümündeki **Oluştur** seçeneğine tıklaması gerekir. RFQ düzeltmeyle güncelleştirildikten sonra tedarik uzmanının **Sonlandır**'a tıklayarak işlemi tamamlaması gerekir. Sonlandırma eylemi, satıcıları düzeltilen RFQ hakkında bilgilendiren bir e-posta iletisi oluşturur. Satıcılara gönderilen e-posta bildirimi şablonunu **Tedarik ve kaynak atama parametreleri** sayfasından seçebilirsiniz. Bir şablon oluşturulduğunda aşağıdaki değiştirme belirteçlerini içerebilir:

-   %Teklifi iade nedeni%
-   %Düzeltme yapma nedeni%
-   %Düzeltmeyi yapan%
-   %Şirket%

%Teklifi iade nedei% ve %Düzeltme yapma nedeni% belirteçleri, tedarik uzmanının **Düzeltme** sihirbazında düzeltme işlemini tamamlarken girebileceği metinle değiştirilir. %Düzeltmeyi yapan% ve %Şirket% belirteçleri otomatik olarak RFQ'dan alınır.  

RFQ yanıtında, teklifin neden reddedildiği veya kabul edildiğini belirtmek için neden kodları kullanmak isterseniz, **Satıcı nedenleri** sayfasında neden kodları ayarlamanız gerekir.  

Tedarik ve kaynak atamadaki **Form ayarı** sayfasında yazdırılan veya depolanan RFQ belgelerinizin görünümünü yapılandırabilirsiniz.  

Bir satınalma sipariş iiçin RFQ oluşturduğunuzda ve RFQ'ya bir stok maddesi eklediğinizde, giriş durumu **Teklif girişi** olan bir stok hareketi oluşturulur. Malzemeleri hesaplamak için bir master plan kullandığınızda yalnızca bu duruma sahip RFQ satırları göz önünde bulundurulur. Master planın RFQ satırlarını beklenen giriş olarak eklemesini istiyorsanız, master plan ayarlama aşamasında bu davranışı yapılandırmanız gerekir.  

Bir satınalma yöneticisi veya temsilcisi olarak, kuruluşunuzun tedarik gereksinimlerine uyacak talep türleri oluşturup bunları koruyabilirsiniz. Her talep türü puanlama yöntemleri uygulayabilir. Puanlama yöntemleri, teklifleri puanlarken kullanabileceğiniz ölçüt kümesinden oluşur. Talep türlerini, puanlama yöntemlerini ve puanlama ölçütünü **Talep türü** ve **Puanlama yöntemi** sayfalarından ayarlamanız gerekir.

## <a name="creating-and-sending-an-rfq"></a>RFQ oluşturma ve gönderme
RFQ oluşturmak için RFQ'ya teklif vermesini istediğiniz satıcıları seçin ve RFQ'yu bu satıcılara gönderin. RFQ raporunu ve yanıt sayfası raporlarını istediğiniz konuma yönlendirmek için yazıcı yönetimini kullanabilirsiniz.  

**Satınalma siparişi** veya **Satınalma anlaşması** türü için RFQ oluşturabilirsiniz:  

RFQ bir satınalma talebinden oluşturulursa **Satınalma talebi** türü otomatik olarak atanır. **Satınalma talebi** türü için RFQ'yu el ile oluşturamazsınız. RFQ türü **Satınalma siparişi** ise:

-   RFQ satırları oluştururken, stok hareketleri giriş durumu **Teklif girişi** olan satırlar için oluşturulur.
-   Bir teklifi kabul ettiğinizde satınalma sipariş oluşturulur.

RFQ türü **Satınalma anlaşması** ise:

-   RFQ, zaman içinde belirli bir miktarda veya değerde ürün satın almak üzere yapılan anlaşma için kullanılır. Satın alma anlaşması için geçerli tarih aralığını ve satınalma anlaşmasını yöneten kişinin adını girmeniz gerekir.
-   Bir teklifi kabul ettiğinizde satınalma anlaşması oluşturulur.

Yalnızca satınalma talebinin durumu **İncelemede** olduğunda bir satınalma talebinden RFQ oluşturabilirsiniz ve bir sonraki iş akışı görevini yapmak üzere atanırsınız. Satıcılardan alınan RFQ yanıtlarındaki (teklifleri) satırları kabul ettiğinizde, satınalma talebindeki satırlar otomatik olarak güncelleştirilir. RFQ işlenirken satınalma talebini tamamlayamaz, reddedemez, onaylayamaz veya üzerinde herhangi başka işlem yapamazsınız.  

Bir RFQ oluşturduğunuzda, belirli bir talep türü seçebilirsiniz. Talep türü, RFQ'ya gelen yanıtları puanlamak için kullanabileceğiniz puanlama ölçütü kümesini belirler.  

Bir RFQ servis talebine soru formu ekleyebilirsiniz. Bu soru formu RFQ gönderildikten sonra tüm yanıtlarda görüntülenir.  

RFQ servis talebine eklenecek satıcılar üç yolla seçilebilir:

-   Satıcıları tek tek ekleme.
-   Belirli ölçütü karşılayan tüm satıcıları arama.
-   RFQ satırlarında kullanılan tedarik kategorileri için onaylanmış olan tüm satıcıları otomatik olarak ekleme.

RFQ servis talebi hazır olduğunda **Gönder**'e tıklayın. Gönder eylemi günlükler oluşturur ve yazıcı ayarlarınıza göre raporlar yazdırılır, arşivlenir ve gönderilir.  

**Teklif talebi gönderme** sayfasında **Fiyatları yeniden hesaplamak için satıcı kullan** ve **Satıcıya özgü madde bilgilerini kullan** onay kutularını işaretlediğinizde, talebi satıcılara gönderirken satıcıya özgü bazı bilgiler otomatik olarak girilir. Bu bilgiler üzerinde **Teklif talebi yanıtı** sayfasından değişiklik yapabilirsiniz.  

Aşağıdaki tablo, bri RFQ oluşturup satıcılara gönderdiğinizde, RFQ durumunun nasıl değiştiğini göstermektedir.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Eylem**                         | **En düşük RFQ başlığı durumu** | **En yüksek RFQ başlığı durumu**                   | **En düşük RFQ satırı durumu** | **En yüksek RFQ satırı durumu** |
| RFQ başlığı ve satırı oluşturun.    | Oluşturulma                      | Oluşturulma                                         | Oluşturulma                    | Oluşturulma                     |
| RFQ'yu belirli bir satıcıya gönderin. | Gönderildi                         | Gönderildi                                            | Gönderildi                       | Gönderildi                        |
| Başka satıcı ekleyin.                | Oluşturulma                      | Gönderildi (RFQ yalnızca tek bir satıcıya gönderilmiştir.) | Oluşturulma                    | Gönderildi                        |
| RFQ'yu ikinci satıcıya gönderin. | Gönderildi                         | Gönderildi                                            | Gönderildi                       | Gönderildi                        |

**Not:** RFQ'ya istediğiniz zaman daha fazla satıcı ekleyebilirsiniz; en düşük ve en yüksek durumları yeni satıcıları yansıtacak şekilde değişir. Örneğin, tüm satıcılardan teklif alır ve teklifteki en az bir satırı kabul ederseniz, RFQ başlığındaki en düşük durum **Reddedildi** ve en yüksek durum **Kabul edildi** olur. Yeni bir satıcı eklerseniz, herhangi bir satırdaki en düşük durum **Oluşturuldu** olur. Bu nedenle, RFQ başlığındaki en düşük durum **Oluşturuldu** olarak değiştirilir ve en yüksek durum kalır **Kabul edildi** olarak kalır.

## <a name="amending-an-rfq"></a>RFQ'yu düzeltme
Bazen, gönderdikten sonra RFQ'da düzeltme yapmanız gerekir. Bunun nedeni, örneğin, teslimat tarihlerinin değişmesi veya ek ürünler ya da farklı ürün miktarları girmek istemeniz olabilir. Düzeltme işlemini, daha kısıtlayıcı veya daha az kısıtlayıcı olacak şekilde yapılandırabilirsiniz.  

Daha kısıtlayıcı düzeltme işlemi kullanırsanız, RFQ servis talebindeki alanları değiştirebilmek için bir düzeltme işlemi başlatmak üzere RFQ servis talebinde **Oluştur**'a tıklamanız gerekir. Değişiklik yapmayı tamamladıktan sonra **Sonlandır**'a tıklamanız gerekir. Ardından, satıcıları düzeltme hakkında bilgilendirmek için gönderilecek eposta iletine nasıl bilgi ekleneceği gösterilecektir. Bir düzeltme notu içeren güncelleştirilmiş RFQ raporu iletiye otomatik olarak eklenir.  

Daha az kısıtlayıcı düzeltme işlemi kullanırsanız, daha önce gönderilmiş olan RFQ üzerinde alanları değiştirmeden önce bir düzeltme oluşturmanız gerekmez. Ancak, RFQ'ya el ile bir düzeltme notu eklemeniz gerekir.

## <a name="receiving-and-registering-rfq-replies"></a>RFQ yanıtlarını alma ve kaydetme
Bir RFQ gönderdiğinizde, yanıt sayfası otomatik olarak oluşturulur. RFQ yanıtları (teklifleri) aldığınızda, her satıcıdan gelen bilgileri satıcıya özel bir RFQ yanıt sayfasına girmeniz gerekir. Puanlama ölçütü eklediyseniz, yanıtları puanlayabilirsiniz. Ardından satıcı teklifleri karşılaştırabilir ve puanlama ölçütünüze göre (en iyi toplam fiyat veya en iyi teslim tarihi gibi) derecelendirebilirsiniz.  

RFQ servis talebine bir soru formu eklendiyse, sorulara gelen yanıtları yanıt sayfasına el ile girmeniz gerekir.  

Alternatif satırlar girmeniz gerekirse ve RFQ servis talebi bunu yapmanıza olanak tanıyorsa, **Satınalma teklifi satırları** hızlı sekmesine **Satır ekle**'ye tıklayın. Ardından madde numarası, tedarik kategorisi, miktar, fiyat ve iskonto gibi ürün bilgilerini girin.  

Yanıtı girdiyseniz ancak satıcıdan yeni bir teklif istiyorsanız, RFQ'yu yeniden gönderebilirsiniz. Bu, satıcıdan değişiklik istemek üzere kullanabileceğiniz yeni bir günlük veya rapor oluşturacaktır.  

Tüm RFQ'ların genel görünümünü ve yanıt durumlarını **Teklif talebi izleme** sayfasından görebilirsiniz.  

Aşağıdaki tablo, teklifleri aldığınızda ve bilgileri RFQ yanıt sayfasına girdiğinizde RFQ durumunun nasıl değiştiğini göstermektedir.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Eylem**                                     | **En düşük teklif durumu** | **En yüksek teklif durumu** | **En düşük RFQ başlığı durumu** | **En yüksek RFQ başlığı durumu** | **En düşük RFQ satırı durumu** | **En yüksek RFQ satırı durumu** |
| Bir satıcının teklifini girin ve kaydedin.        | Gönderildi                  | Alınan               | Gönderildi                         | Alınan                      | Gönderildi                       | Alınan                    |
| İkinci satıcının teklifini girin ve kaydedin. | Alınan              | Alınan               | Alınan                     | Alınan                      | Alınan                   | Alınan                    |

**Not:** Bir teklifi ek görüşme için satıcıya geri gönderirseniz, en düşük ve en yüksek durumları **Alındı** olarak kalır.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Teklifleri kabul etme ve reddetme ve kabul edilen teklifleri aşağı doğru belgelere aktarma

Örneğin en iyi toplam fiyatı sunan teklif gibi en iyi teklifi tanımladıktan sonra teklifi kabul edin. Bu satıcı için RFQ durumu **Kabul edildi** olarak güncelleştirilir. Bir teklifi veya teklifteki belirli satırları kabul ettiğinizde, otomatik olarak bir satınalma siparişi veya satınalma anlaşması oluşturulur ve diğer satıcılardan gelen teklifleri reddedebilirsiniz.  

**Satınalma talebi** türünde RFQ yanıtını kabul ettiğinizde, RFQ yanıt satırları satınalma talebi satırlarını aşağıdaki bilgilerle güncelleştirir:

-   Birim fiyat
-   İskonto yüzdesi
-   İskonto tutarı
-   Satınalma masrafları
-   Satır giderleri
-   Satıcı
-   Harici numara
-   Harici tanım

Yanıta, teklifi neden kabul ettiğinizi veya reddettiğinizi açıklayan bir neden kodu ekleyebilirsiniz.  

Bir teklifteki bazı satırları kabul edip diğerlerini reddedebilirsiniz. Ayrıca, farklı satıcılardan gelen satırları da kabul edebilirsiniz. Bazı satırları kabul ettiğinizde, kalan diğer tüm satırları reddetmeniz istenecektir. Bu nedenle, diğer satırları da kabul etmek isterseniz, istemi aldığınızda **İptal**'e tıklamanız gerekir.  

Aşağıdaki tabloda, satıcılardan gelen teklifleri kabul ettiğinizde ve reddettiğinizde RFQ durumunun nasıl değiştiği gösterilmektedir.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Eylem**              | **En düşük teklif durumu** | **En yüksek teklif durumu** | **En düşük RFQ başlığı durumu** | **En yüksek RFQ başlığı durumu** | **En düşük RFQ satırı durumu** | **En yüksek RFQ satırı durumu** |
| Tekliflerden birini kabul edin. | Alınan              | Kabul edildi               | Alınan                     | Kabul edildi                      | Alınan                   | Kabul edildi                    |
| Diğer teklifleri reddedin.  | Reddedildi              | Kabul edildi               | Reddedildi                     | Kabul edildi                      | Reddedildi                   | Kabul edildi                    |






