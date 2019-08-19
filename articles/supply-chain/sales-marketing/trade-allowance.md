---
title: Ticari tahsisat yönetimi
description: Microsoft Dynamics 365 for Finance and Operations için tahsilat kodlarının yönetimini açıklar.
author: t-benebo
manager: AnnBe
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550815c5c3fc9a24ec8b67f2a340e0553eef072d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843349"
---
# <a name="trade-allowance-management"></a>Ticari tahsisat yönetimi

[!include [banner](../includes/banner.md)]

Ticari tahsisat yönetimi, şirketlerin hacim ve davranış hedeflerini gerçekleştiren müşterilere perakende "performans için ödeme" parası teklif eden satış promosyon programlarını yönetmelerine yardımcı olur. Özelliğin yetenekleri, promosyon fon bütçesi ve tahsisatından kar işlemlerini, ödenek sözleşme ayarlamasını, talepler oluşturma ve işlemeyi, ödeme işlemesini ve promosyon etkililik analizini kapsamlı olarak yükseltmeye odaklanan şirketler için tasarlanır.


Bu makalede, ticari tahsisat yönetimine geniş çaplı genel bakış sağlanmakta ve satış promosyon programının yönetilmesinde yer alan tipik görev kümesi tanıtılmaktadır. Operasyonel ve karar alma sorumlulukları olan birkaç tür kullanıcıdan ilgili hedeflere ulaşmada bu işlevleri kullanması beklenir:

- Seçilen hesaplar için isteğe bağlı fonları tahsis etme ve (üzerinde anlaşılan bir hizmet için) sonradan faturalandırmalar ve özel peşin ödemelere bağlı olarak promosyonlar için ticari tahsisat sözleşmeleri ayarlama
- Devam eden satışlar üzerinden üzerinde anlaşılan promosyon sözleşmelerini çalıştırma ve sonradan faturalandırma taleplerini oluşturma
- Oluşturulan teklifleri hesaplama, onaylama, işleme ve bunları ödeme kapatma için kesintiler olarak Alacak hesaplarına (A/R) geçirme
- Müşterinin vadesi gelen kesintili kısa vadeli ödemesiyle mutabakat sağlama
- Promosyon fonu kullanımını izleme ve program karlılığı ile etkinliğini değerlendirme

## <a name="audience-and-purpose"></a>Kitle ve amaç

Bu belgedeki bilgiler kurumsal şirketlerdeki, satınalma yöneticisi, mali işler müdürü (CFO) ve muhasebe müdürü gibi aşağıdaki sorumluluklara sahip işletme karar alıcıları içindir:

- Üst düzey bütçeler ve fon tahsisatı
- Satış promosyonlarını planlama ve analiz etme
- Sonradan faturalandırma taleplerini işleyen, emtia olaylarına bağlı ödemeleri çalıştıran, kısa vadeli ödemeleri ve kesintileri kapatan yönetim personeli

Bu görevlerdeki kişiler, bu hedeflere ulaşmanın yollarını arar:

- Pazarlama promosyon fonlarını daha iyi kullanın.
- Çeşitli türde promosyon programlarını ve tahsisatları esnek biçimde yönetin.
- Yönetim yükünü azaltın ve promosyon performansı ve işleme talepleri ile ilişkili hataları azaltın.
- Gelecekte borçları tahakkuk ederek nakit akışı tahminlerini iyileştirin.
- Müşteriler ile promosyonlar hakkında sürmekte olan ve gelecekteki pazarlıklar hakkında temele sahip olun.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Promosyon fonu ve Ticari tahsisat sözleşmesi

Ticari tahsisat sözleşmesi, performans için ödeme parasının spesifik hacim hedeflerini ve/veya davranış hedeflerini gerçekleştiren müşterilere sunulduğu bir teşvik programıdır. Promosyon fonları, harcamalar olarak bütçelenir. Bu şekilde, promosyon kampanyaları yakalanabilir.

### <a name="promotional-fund"></a>Promosyon fonu

Ticari tahsisat sözleşmeleri için tahsis edilen fonlar, **Fonlar** sayfasına kaydedilir. **Fonlar** sayfasını açmak için **Satış ve pazarlama** \> **Ticari tahsisatlar** \> **Fonlar** \> **Fonlar**'ı seçin.

![Fonlar sayfası](./media/trade-allowance-management-funds-page.png "Fonlar sayfası")

**Fonlar** sayfasında, promosyon fonlarının ayrıntılarını görüntüleyebilirsiniz.

**Genel** hızlı sekmesi, fonun geçerli olduğu dönemi ve bütçelenmiş tutarını gösterir. Fonun promosyon sözleşmesi uyarınca tahsis edilmesi için **Durum** alanında **Onaylandı** değeri bulunmalıdır.

**Müşteriler** hızlı sekmesi, müşteri hiyerarşisini gösterir. Fonun hedeflediği müşterileri seçmek için **Fon müşterileri** altında olacak şekilde müşterileri sürükleyin. Bu hızlı sekme ayrıca fonun toplam tutarının nasıl dağıtıldığını gösterir.

**Maddeler** hızlı sekmesi, promosyona dahil olan maddeleri gösterir.

### <a name="trade-allowance-agreement"></a>Ticari tahsisat sözleşmesi

Fon tanımının yerine konulmasının ardından promosyon planlamada sonraki adım (ticari tahsisat sözleşmeleri olarak bilinen) promosyon sözleşmelerini kaydetmek, fonları tahsis etmek ve her bir emtia olayı için performans hedeflerini tanımlamaktır.

Ticari tahsisat sözleşmeleri, **Ticari tahsisat sözleşmeleri** sayfasına kaydedilir. **Ticari tahsisat sözleşmeleri** sayfasını açmak için **Satış ve pazarlama** \> **Ticari tahsisatlar** \> **Ticari tahsisat sözleşmeleri**'ni seçin.

![Ticari tahsisat sözleşmeleri sayfası](./media/trade-allowance-management-agreements-page.png "Ticari tahsisat sözleşmeleri sayfası")

#### <a name="header"></a>Üstbilgi

Üstbilgi görünümünü değiştirmek için **Üstbilgi**'yi seçin.

**Genel** hızlı sekmesindeki **Sipariş bitişi** ve **Sipariş başlangıcı** alanları sözleşmenin geçerli olduğu dönemi tanımlar. Sözleşme için **Dahili onaylandı** onay durumu, sözleşmenin henüz geçerli olmadığını ve satış siparişi işleme sırasında uygulanamadığını gösterir.

**Genel** hızlı sekmesinin **Analiz** bölümü, promosyon değerlendirmesi için kullanılan miktarları ve maliyetleri tanımlayan önemli alanlar içerir:

- **Temel birimler** alanı, promosyon uygulanmadan önce belirli müşterilere satılması gereken ürün miktarını belirtir.
- **Hesaplanan sevk miktarı** değeri bu promosyon için planlanmış hedef artışı olan **Kaldırma yüzdesi** değerine göre hesaplanır.
- **Ticari tahsisat maliyeti** alanı, ticari tahsisat sözleşmesindeki çeşitli olayların miktarlarına göre hesaplanır.

**Müşteriler** hızlı sekmesinde, soldaki listede önceden tanımlanmış hiyerarşiler olarak ayarlanan müşteri gruplarını seçebilir ve görüntüleyebilirsiniz. Böylece tahsisat sözleşmesi için hedef olarak tüm hiyerarşiyi veya belirli hesapları seçebilirsiniz.

**Maddeler** hızlı sekmesinde, **Fonlar** sayfasının **Maddeler** hızlı sekmesindeki gibi, üzerinde anlaşılan tahsisatlı satışlarıyla ilişkilendirmek için ürünler sözleşmeye eklenir.

**Fonlar** hızlı sekmesinde bu sözleşmeyle ilişkili promosyon fonlarını görüntüleyebilirsiniz. Ayrıca sözleşmenin olay maliyet tahsisatını da görüntüleyebilirsiniz. Yüzde 100'lük bir olay maliyet tahsisatı bu promosyonun bir fondan özel olarak finanse edileceği anlamına gelir. Alternatif olarak, bir promosyon sözleşmesi birkaç fondan yararlanabilir ve eşit veya farklı yüzdelerde tahsisat kullanabilir.

#### <a name="lines"></a>Hatlar

Ardından, Hatlar görünümünü değiştirmek için **Hatlar**'ı seçin.

**Emtia olayları** sekmesi bir sözleşme kapsamındaki olay türlerini gösterir. Üç türü vardır: sonradan faturalandırma, peşin ödeme ve kapalı fatura.

Emtia olayını ve ardından **Tutarlar** sekmesini seçtiğinizde olayın detayları bulunur.

![Ticari tahsisat sözleşmesi satırları](./media/trade-allowance-management-agreements-lines.png "Ticari tahsisat sözleşmesi satırları")

**Ticari tahsisat satırları** bölümünde, müşterinin ödül elde etmek için tanımlananları gerçekleştirmek zorunda olduğu miktar veya tutar aralıklarını belirtirsiniz.

**Sonradan faturalandırma** türünün emtia olayı durumunda **Tutarlar** sekmesinin üst bölümü, sonradan faturalandırmanın uygulanma, oluşturulma ve ödenme kurallarını tanımlar. Örneğin, kurallar sonradan faturalandırma talebi için aşağıdaki koşulları belirtebilir:

- Satış siparişinin oluşturulma tarihi esas alınır ( **Hesaplama tarihi türü** değeri **Oluşturuldu**).
- Satış sipariş satırının net tutarına değil, iskontoları içeren iskonto öncesi tutarına göre hesaplanır ( **Alınan yer** değeri **Brüt**).
- Tutara göre değil, satılan ürünlerin hacmine göre hesaplanır ( **İndirim satır sonu türü** değeri **Miktar**).
- Aylık döneme göre hesaplanır ( **Satışların toplamını alma ölçütü** değeri **Ay**). 
- A/P kullanılarak değil, kesinti olarak kapatılır ( **Ödeme türü** değeri **Müşteri kesintileri**).

**Peşin ödeme** türünün emtia olayı durumunda **Tutarlar** sekmesi, müşteri özel performans gerçekleştirdiğinde indirim formu olarak müşteriye ödenecek miktarı gösterir. **Açık** onay durumu, peşin ödemenin henüz ödenmemiş olduğunu gösterir.

Sözleşmeyi sözleşme koşullarını karşılayan satış siparişlerine uygulamak için sözleşme durumu **Onaylandı** olmalıdır. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Planlanan emtia olayı altında satışları gerçekleştirme ve sonradan faturalandırma taleplerini oluşturma

Sözleşmenin gereksinimlerini karşılayan hatlara sahip olan bir satış siparişi oluştururken **Satış siparişi** sayfasında **Satış siparişi hattı** \> **Görünüm** \> **Fiyat ayrıntıları**'nı seçerek ilgili bilgileri görüntüleyebilirsiniz.

**Fiyat ayrıntıları** sayfasında **İndirimler** hızlı sekmesinde satış görevlisi, geçerli ticari tahsisat sözleşmesinden gelen bir sonradan faturalandırmayı (indirim programı kodu gösterilir) ve satıra uygulanan toplam tutarı görebilir. Bu tutar ayrıca **Fiyat ayrıntıları** sayfasının **Marj tahmini** bölümünde **İndirim tutarı** alanında gösterilir.

Satış faturaları deftere nakledilirken her bir fatura satırı için karşılık gelen sonradan faturalandırma talebi oluşturulur.

> [!NOTE]
> **Fiyat ayrıntıları** sayfasını görmek için **Alacak hesapları parametreleri** sayfasında **Fiyatlar** sekmesinde **Fiyat ayrıntılarını etkinleştir** onay kutusunu seçin. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Talepleri işleyin ve bunları kesintiler olarak A/R'ye geçirin

Sonradan faturalandırmaları işlemek için işlemdeki sonraki adımlar talepleri incelemek, hesaplamak ve onaylamak ve sonrasında bunları kesintilere dönüştürmektir.

Sonradan faturalandırma workbench, promosyon sözleşmesi sahibinin oluşturulan talepleri periyodik olarak incelediği ve işlediği yerdir. Ayrıca talep için ödeme yöntemine bağlı olarak, A/R yöneticisinin onaylanmış talepleri kesintilere veya düzenli ödemelere dönüştürdüğü yerdir.

**Sonradan faturalandırma workbench** sayfasında, talep satırlarını inceleyebilirsiniz. Talepler **Yeniden hesaplanacak** durumundaysa herhangi bir toplam etki için yeniden hesaplanmalıdırlar.

### <a name="recalculate-claims"></a>Talepleri yeniden hesaplayın

Talepleri yeniden hesaplamak için Eylem Bölmesi'nde **Biriktir**'i seçin. Ardından, **İndirimleri biriktir** iletişim kutusunda müşteriyi seçin.

Yeniden hesaplama sonucu olarak program, orijinal talepleri her bir birim için uygun tutara düzeltmek üzere tutarlar için yeni talepler oluşturur. Her bir benzersiz müşteri, madde, para birimi, ölçü birimi, stok boyutları, mali boyutlar ve satış vergisi grupları bileşimi için bir düzeltme talebi oluşturulur. Bu düzeltme talepleri düzeltilen (başka bir deyişle aslen satış belgesinden oluşturulan) talepler olarak satış siparişi ve fatura numarası ile aynı referansa sahip olur. Orijinal talebin aksine, düzeltme talebi orijinal satış sipariş satırı tutarı ve miktarını tanımlayan alanlarda değerlere sahip değildir.

Yeniden hesaplama tamamlandıktan sonra taleplerin durumu **Hesaplandı** olarak değiştirilir. Talepleri onaylamak için Eylem Bölmesi'nde **Onayla**'yı seçin.

### <a name="process-claims-and-pass-them-to-ar"></a>Talepleri işleyin ve bunları A/R'ye geçirin

Talepler artık A/R işlemesine hazırdır. Talepleri işlemek için Eylem Bölmesi'nde **İşle**'yi seçin. 

Taleplerin işlenmesinin ardından durum **İşaretle** olarak değiştirildi ve bu, günlüğün deftere naklinin (A/R parametrelerinde belirtildiği üzere, deftere nakledilen günlük İndirim tahakkuk günlüğüdür) aşağıdaki olayların oluşmasına neden olduğunu gösterir: 

- Talepler, kesintiler olarak geçici müşteri bakiyesine aktarıldı.
- İndirim tahakkuk hesabı, müşterinin gelecekteki borcunu temsil etmek üzere alacaklandırıldı.
- İndirim gider hesabı, satışlarla bağlantılı tahakkuk eden maliyeti tanımak üzere borçlandırıldı.

İşlemi tamamlamak için A/R görevlisi artık tahakkuk kesintilerini alacak dekontu (pasif) olarak müşterinin bakiyesine aktararak işlemelidir. 

Görevi başlatmak için **Müşteri** sayfasının Eylem Bölmesi'nde **Tahsil et** \> **Hareketleri kapat**'ı seçin. Ardından, **Hareketleri kapat** sayfasında **İşlevler** \> **Sonradan faturalandırma programı**'nı seçin. Bu indirim sayfası, önceden işlenmiş olan tüm sonradan faturalandırma taleplerini gösterir.

Alacak dekontu oluşturmak istediğiniz tüm hatlar için **İşaretle** onay kutusunu seçin ve sonrasında **İşlevler** \> **Alacak dekontu oluştur**'u seçin.

Alacak dekontu oluşturulduktan sonra günlük deftere nakledilir. (A/R parametrelerinde belirtildiği üzere deftere nakledilen günlük AR tüketim günlüğüdür.) Sonuç olarak gerçek borç (alacak) tutarı müşterinin bakiyesine taşındı. Mali olarak bu durum aşağıdaki olayların meydana geldiği anlamına gelir:

- Müşterinin alacak hesabı alacaklandırıldı.
- İndirim tahakkuk hesabı borçlandırıldı.

**Peşin ödeme** türünün emtia olayını onaylamak için **Ticari tahsisat sözleşmeleri** sayfasında olayı seçin ve sonrasında **Tutar** sekmesinde **Onayla**'yı seçin.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Kesinti workbench'ini kullanarak vadesi gelen kesintiyi ve müşterinin kısa vadeli ödemesini kapatın

Sonradan faturalandırma beklentisinde olan müşteriler çoğunlukla kısa vadeli ödeme seçimli faturaları seçer. Gelecekteki ödeme mutabakatı sorunlarının önüne geçmek için A/R görevlisi gerçek müşteri ödemelerini kaydederken bu kısa vadeli ödemeleri kesinti olarak kaydeder. Daha sonra Kesinti workbench'i üzerinde bu müşteri kesintileri, şirketten gelen vadesi gelen talep tutarları karşısında kolaylıkla kapatılabilir.

Müşterinin kısa vadeli ödemesini Ödeme günlüğüne kaydetmek için **Alacak hesapları** \> **Ödemeler** \> **Ödeme günlüğü**'nü seçin ve yeni bir ödeme günlüğü oluşturun. Ardından, Eylem Bölmesi'nde **Kesintiler**'i seçin. **Kesinti** sayfasında, kısa vadeli ödenmiş tutarı oluşturabilir ve izleyebilirsiniz.

Tahsilat yöneticisi artık Kesinti workbench'inde karşılıklı açık alacak dekontu hareketini ve kısa vadeli ödeme hareketini kapatmaktan sorumludur.

Kesintileri yönetmek için **Satış ve pazarlama** \> **Ticari tahsisatlar** \> **Kesintiler** \> **Kesinti workbench'i** seçeneğini belirleyin. Sayfanın üst kısmında, müşteriden gelen kısa vadeli ödemeleri temsil eden satırlar bulunur. Sayfanın alt bölümünde müşterilerin açık alacak hareketleri bulunur. 

Açık hareketteki kesintiyi kapatmak için kesinti satırını işaretleyin ve sonrasında Açık hareketler sekmesinde satırı işaretleyin. Eylem Bölmesi'nde Koru > Eşleştir'e tıklayın.

Başlangıçtaki taleplerin durumu artık **Tamamlandı** olarak ayarlanır.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Promosyon ve fon tüketiminin etkinliğini çözümleme

Programın başlıca istatistiklerine ve fon kullanımına dair bir genel bakış elde etmek için Ticari tahsisat yönetiminde mevcut olan çeşitli raporları ve analitik incelemeleri kullanabilirsiniz.

**Ticari tahsisat faaliyeti** sayfasındaki **Genel bakış** sekmesi, ticari tahsisat sözleşmesinin temel ayrıntılarını gösterir. Diğer sekmeler programla ilgili ilişkili belgeler, ödemeler ve diğer olaylar hakkında daha spesifik ayrıntıları gösterir.

**Özet** sekmesi, promosyon altında satılmış ürünlerin toplam miktarını, faturalandırılmış satış tutarını ve ödemesi yapılmış sonradan faturalandırmalar ve peşin ödemeleri gösterir.

**Sonradan faturalandırma kredileri** sekmesi, müşteri için kredilendirilmiş bireysel sonradan faturalandırma detaylarını içerir.

Promosyon için çeşitli performans ölçümlerine dair daha analitik bir genel bakış elde etmek isterseniz Analiz görünümünü kullanabilirsiniz. Analiz görünümüne gitmek için **Satış ve pazarlama** \> **Ticari tahsisatlar** \> **Ticari tahsisat sözleşmeleri**'ne tıklayın. Eylem Bölmesi'nde **Analiz**'e tıklayın.  

Promosyon için çeşitli performans ölçümlerine dair daha analitik bir genel bakış elde etmek isterseniz Analiz görünümünü kullanabilirsiniz. Analiz görünümüne gitmek için **Satış ve pazarlama** \> **Ticari tahsisatlar** \> **Ticari tahsisat sözleşmeleri**'ne tıklayın. Eylem Bölmesi'nde **Analiz**'e tıklayın. 

