---
title: SEPA kredi transferine genel bakış
description: Bu makale, Tek Euro Ödeme Bölgesi (SEPA) kredi transferleri ve satıcılar için diğer elektronik ödemeleri içeren ISO 20022 kredi transferleri hakkında genel bilgi sağlar.
author: mrolecki
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "11124"
- intro-internal
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 671594b1ac6f10fae7c95ed9210e16f168e8dea1
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716087"
---
# <a name="sepa-credit-transfer-overview"></a>SEPA kredi transferine genel bakış

[!include [banner](../includes/banner.md)]

Bu makale, Tek Euro Ödeme Bölgesi (SEPA) kredi transferleri ve satıcılar için diğer elektronik ödemeleri içeren ISO 20022 kredi transferleri hakkında genel bilgi sağlar. SEPA kredi transferi bir şirketten veya bir bireyden başka bir şirket veya bireye yapılan özel türde bir ödemedir (euro cinsinden). Bu makalede, bir kredi transferi ödeme dosyasının nasıl ayarlanacağı ve aktarılacağı da açıklanmaktadır.

## <a name="what-is-a-credit-transfer-message"></a>Kredi transferi iletisi nedir?
Kredi aktarma iletisi, başlatan bir tarafın (şirketinizin) kendi hesabından alacaklıya para taşımak için gönderdiği bir istektir. Kredi transferi iletilerinin ülke/bölge özelinde ve bankaya özel uygulamaları vardır. Bunlardan bazıları bir ülkede/bölgede kullanılırken, bazıları standart haline gelmektedir. İyi bilinen bir küresel standart, ISO 20022 ve Kredi transferi gibi başlatma iletileridir. Aşağıdaki şekilde, seçilen kredi aktarma iletileri arasındaki ilişkiler ve kapsam gösterilmektedir. 
![Kredi transferi.](./media/credit-transfer.jpg) Kredi transferi iletileri 

## <a name="what-are-iso-20022-and-sepa-payments"></a>ISO 20022 ve SEPA ödemeleri nedir?
Tek Euro ödemeleri Alanı (SEPA), Avrupa Komisyonu tarafından ayarlanır ve tüm elektronik ödemelerin birey, işletme veya kuruluş ve bankanın bulunduğu ülke/bölgeden bağımsız olarak yurtiçi olarak kabul edildiğini belirler. Ulusal ödemeler ve sınır ötesi ödemeler arasında hiçbir fark yoktur. SEPA, 28 Avrupa Birliği (AB) üyesi devletleri ve ayrıca İzlanda, Liechtenstein, Norveç, İsviçre, Monako ve San Marino'yu içerir. SEPA, Avrupa Ekonomik Alanı (EEA) içinde ödeme hareketleri için tek bir pazar oluşturulmasına yardımcı olur. Sonuçta, SEPA'nın bankalar, işyerleri ve bireylerin çalışması gereken ödeme sayısını azaltması beklenir. Avrupa Komisyonu, Ödeme Hizmetleri Yönergesi (PSD) aracılığıyla SEPA ödemeleri için yasal temeli kurmuştur. Avrupa Ödemeler Konseyi (EPC), aşağıdaki etkinlikler aracılığıyla SEPA'yı destekler:

-   ISO 20022 Evrensel mali sektör ileti düzeni XML biçimini kullanarak SEPA elektronik ödemeleri için standartları belirler.
-   Euro ödemelerinin işlenmesi hakkındaki kuralları ve yönergeleri oluşturur.

Avrupa bankalarından oluşan EPC, SEPA ödeme araçları için ticari ve teknik çerçeveleri geliştirir. Üç tip SEPA ödemesi kullanılır:

-   Kredi transferleri
-   Otomatik ödemeler
-   Kartlar

## <a name="what-is-a-sepa-credit-transfer"></a>SEPA kredi transferi nedir?
SEPA kredi transferi bir şirketten veya bir bireyden başka bir şirket veya bireye yapılan ödemedir. Ödemelerin Euro cinsinden olması gerekir ve her iki taraf için Uluslararası Banka Hesap Numarası (IBAN) ve Banka Tanımlayıcı Kodunu (BIC) içermelidir. (BIC, Dünya Çapındaki Bankalararası Finansal Telekomünikasyon Kurumu \[SWIFT\] kodu olarak da bilinir.) Ayrıca, işlem maliyetlerinin her iki taraf arasında paylaşılması gerekir. Taraflar arasında oluşan kredi transferlerinde ISO 20022 ödeme işleme standartları ve EPC tarafından belirtildiği gibi XML formatıyla uyumlu XML dosyaları kullanılmalıdır.

## <a name="how-is-a-credit-transfer-implemented"></a>Kredi transferi nasıl uygulanır?
Avrupa ülkeleri için kredi transferi ödeme biçimi, Microsoft Dynamics 365 Finance uygulamasında Elektronik raporlama (ER) ve Ödeme yöntemleri işlevi kullanılarak uygulanır. Diğer bölgelerde kullanılan birkaç kredi aktarma biçimi, eski ödeme çerçevesini kullanmaya devam etmektedir. Diğer pek çok biçim arasında on iki ISO 20022 kredi aktarım dosyası biçimi mevcuttur. Bu dışa aktarma biçimleri SEPA ISO 20022 XML standardına uygundur. Bunlar, kullanıldıkları ülkeler/bölgeler için euro dışı ödeme transferleri ve EPC'nin yayınladığı SEPA Kredi Transfer Şeması Kural Kitabı'nın 8.2 sürümünde belirtilen euro ödemeleri için kullanılır. Kredi transferlerini uygulamadan önce, elektronik bankacılık dosyalarını yüklemek için gereken yazılımı edinmek için bankanıza başvurmanız gerekir. Bu yazılımı ödeme emirlerini içeren XML dosyalarını bankanıza aktarmak için kullanacaksınız.

## <a name="what-credit-transfer-formats-are-currently-supported"></a>Şu anda hangi kredi transfer biçimleri desteklenmektedir?
Sürekli olarak Microsoft Dynamics Lifecycle Services'daki (LCS) Paylaşılan varlık kitaplığına gidip varlık türü **GER yapılandırması** olan mevcut dosyaların en güncel listesini görüntülemeniz gerekir. Sonraki "Neyi ayarlamam gerekiyor?" bölümünde, mevcut yapılandırmaları incelemek ve seçili yapılandırmaları içeri aktarmak için bir LCS deposunun nasıl oluşturulacağının açıklandığı makalenin bağlantısı verilmektedir.

## <a name="what-do-i-have-to-set-up"></a>Neyi ayarlamam gerekiyor?
-   Kredi transfer dosyaları oluşturmadan önce en az bir etkin kredi transferi yapılandırmasının ER yapılandırmalarınıza aktarılması gerekir. Yönergeler için bkz. [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Borç hesapları ödeme yöntemlerini yapılandırırken **Genel elektronik raporlama** onay kutusunu işaretleyin ve dışa aktarma biçimi yapılandırması olarak uygun kredi transferi biçimini (örneğin **ISO 20022 Kredi transferi (AT)**) seçin.
-   Tüzel kişiliği ve banka hesap bilgilerini de ayarlamanız gerekir.
-   Banka hesabı numaraları, IBAN'lar ve bazen SWIFT kodları (BIC'ler) veya diğer kimlikler geçerli kredi transferi ödemeleri oluşturmak için gereklidir. Bu nedenle, satıcı banka hesabı ve transferi isteyen kuruluşun banka hesabı için bunları ayarlamanız gerekir.
-   Kredi transfer iletisinde atıfta bulunulan taraflar için katma değer vergisi (KDV) numaraları gibi ek bilgiler gerekebilir. İstendiğinde satıcılar ve tüzel kişiler için bu bilgilerin ayarlanması gerekir.
-   Borç hesapları ödeme yöntemlerinden bazıları, çoğunlukla ISO 20022 tabanlı ödeme yöntemleri **Ödeme biçimi kod kümeleri** için **Hizmet türü** = **SLEV** gibi ek kurulumlar gerektirebilir. Bu kodlar, ödeme işleme sırasında ödeme hareketleri için ek etiketleme olarak kullanılır. Varsayılan Ödeme kodu değerleri (örneğin **Kategori amacı**, **Masrafı taşıyan**, **Yerel enstrüman** ve **Hizmet düzeyi**) iki yerde ayarlanabilir. İlk yer **Borç hesapları ödeme günlüğü başlığı** ve ikincisi ise **Borç hesapları ödeme yöntemleri**'dir. Ödeme günlüğü satırları oluşturulurken, ödeme günlüğü başlığında ayarlanan Ödeme kodu değerleri bir yevmiye defteri satırına aktarılır; ayarlanmazsa, Ödeme yöntemlerinden alınan değerler kullanılır.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Kredi transfer ödemeleri üretmek için hangi parametreler kullanılabilir?
Özel parametreler listesi kredi transfer biçimine bağlıdır. Aşağıdaki tabloda, bir satıcı ödeme günlüğünde Almanya için ISO 20022 kredi transfer ödeme dosyası oluştururken kullanılabilecek parametrelerin listesi gösterilmektedir. **Arka planda çalıştır** sekmesindeki seçenekleri kullanarak, ödeme üretimini toplu iş modunda çalıştırabilirsiniz.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alan</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Toplu kayıt</td>
<td>Toplu kayıt etiketi XML dosyasında dahil etmek için bu onay kutusunu seçin.</td>
</tr>
<tr class="even">
<td>İşlem tarihi</td>
<td>Bankanın ödemeleri işlemesi gereken tarihi girin.</td>
</tr>
<tr class="odd">
<td>Biçim</td>
<td>Ülke/bölge veya banka gereksinimlerine bağlı olarak havale bilgileri için biçim seçin:
<ul>
<li><strong>Strd</strong> – Bir ödeme bir faturaya kapatıldığında yapılandırılmış biçimi kullanmak için bu seçeneği belirleyin. Bu seçenek, Fransa, Almanya veya Hollanda için ülkeye/bölgeye özgü aktarma biçimlerinde kullanılamaz.</li>
<li><strong>Ustrd</strong> – Bir ödeme çok sayıda faturaya kapatıldığında yapılandırılmamış biçimi kullanmak için bu seçeneği seçin. Kapatılan faturalar için fatura numaraları birleştirilir ve havale bilgisi olarak kullanılır. ISO 20022 yönergeleri gereğince, yapılandırılmamış havale bilgileri 140 karakterle sınırlıdır.</li>
</ul></td>
</tr>
<tr class="even">
<td>Fatura sayısı</td>
<td><strong>Ödeme ihbarı</strong> raporunun yazdırıldığı kaynak fatura sayısını girin.</td>
</tr>
<tr class="odd">
<td>Numara serisi</td>
<td>Dosyayı tanımlamak için bir seri numarası girin. Seri numarası <strong>İlişkili not</strong> raporunda görünür.</td>
</tr>
<tr class="even">
<td>İlişkili notu yazdır</td>
<td><strong>İlişkili not</strong>raporunu yazdırmak için bu onay kutusunu işaretleyin.</td>
</tr>
<tr class="odd">
<td>Kontrol raporu yazdır</td>
<td>Ödeme bilgisini içeren bir rapor yazdırmak için bu onay kutusunu işaretleyin.</td>
</tr>
<tr class="even">
<td>Kapak yazısı yazdır</td>
<td><strong>Ödeme ihbarı</strong>raporu yazdırmak için bu onay kutusunu işaretleyin.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>IBANs ve BICs nedir?
Uluslararası Banka Hesap Numarası (IBAN) ve Banka Tanımlayıcı Kodu (BIC), birçok ülkedeki/bölgedeki hesapları tanımlamak için kullanılır. Bu kodlar 34 SEPA ülkesini/bölgesini içermektedir. **SWIFT kodu** alanına BIC'yi ve **IBAN** alanına IBAN'ı girin. Alacaklı banka hesabı ve müşteri banka hesabı için, bu alanlar **Banka hesapları** sayfasının **Banka hesabı** sekmesindeki **Ek kimlik** Hızlı Sekmesinde yer alır. SEPA ödemeleri için BIC kullanımı artık zorunlu değildir.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Bir ödeme dosyasını bankaya nasıl iletirim?
Ödemeler oluşturduğunuzda, ödeme dosyası oluşturulur ve web tarayıcınızdan mevcut herhangi bir konuma kaydetmeniz istenir. Sonraki adım, XML dosyasını bankanıza göndermektir. Bu işlem bankadan bankaya değişir. Dosyaları işlemek için bankaya göndermek için bankanızın talimatlarını izleyin.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
