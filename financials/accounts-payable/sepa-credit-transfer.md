---
title: "SEPA kredi transferine genel bakış"
description: "Bu makale, tek Euro ödemeleri alan (SEPA) kredi transferleri ve diğer elektronik ödemeler için satıcılar dahil ISO 20022 kredi transferleri hakkında genel bilgiler sağlar. SEPA kredi transferi belirli bir şirketten veya başka bir şirket için ayrı ayrı veya tek tek Euro ödeme türüdür. Konu ayrıca ayarlamak ve kredi transfer ödeme dosya aktarmak nasıl açıklar."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>SEPA kredi transferine genel bakış

Bu makale, tek Euro ödemeleri alan (SEPA) kredi transferleri ve diğer elektronik ödemeler için satıcılar dahil ISO 20022 kredi transferleri hakkında genel bilgiler sağlar. SEPA kredi transferi belirli bir şirketten veya başka bir şirket için ayrı ayrı veya tek tek Euro ödeme türüdür. Konu ayrıca ayarlamak ve kredi transfer ödeme dosya aktarmak nasıl açıklar.

## <a name="what-is-a-credit-transfer-message"></a>Kredi transfer ileti nedir?
Kredi transfer fon kendi hesabından Alacaklıya taşımak için bir başlatan taraf (şirket) gönderdiği bir istek iletisidir. İletileri kredi transferi birçok ülkeye/bölgeye özgü ve banka özel uygulamaları vardır. Bunlardan bazıları bir ülke/bölge içinde kullanılır ve bazı standartlar gelmektedir. Tanınmış bir küresel standart ISO 20022 ve onun başlatma iletiler kredi transferi ' dir. İlişkileri ve seçili kredi transfer iletiler için kapsamı aşağıda gösterilmiştir. 
![Kredi tansfer](./media/credit-transfer.jpg) kredi transfer iletileri\[/resim yazısı\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>ISO 20022 ve SEPA ödeme nedir?
Tek Euro ödemeleri Alanı (SEPA), Avrupa Komisyonu tarafından ayarlanır ve tüm elektronik ödemelerin birey, işletme veya kuruluş ve bankanın bulunduğu ülke/bölgeden bağımsız olarak yurtiçi olarak kabul edildiğini belirler. Ulusal ödemeler ve ötesi ödemeler arasında fark yoktur. SEPA 28 üye Devletleri, Avrupa Birliği (AB) ve ayrıca İzlanda, Liechtenstein, Norveç, İsviçre, Monako ve San Marino içerir. SEPA, Avrupa Ekonomik Alanı (EEA) içinde ödeme hareketleri için tek bir pazar oluşturulmasına yardımcı olur. Sonuçta, SEPA'nın bankalar, işyerleri ve bireylerin çalışması gereken ödeme sayısını azaltması beklenir. Avrupa Komisyonu, Ödeme Hizmetleri Yönergesi (PSD) aracılığıyla SEPA ödemeleri için yasal temeli kurmuştur. Avrupa Ödemeler Konseyi (EPC), aşağıdaki etkinlikler aracılığıyla SEPA'yı destekler:

-   ISO 20022 Evrensel mali sektör ileti düzeni XML biçimini kullanarak SEPA elektronik ödemeleri için standartları belirler.
-   Euro ödemelerinin işlenmesi hakkındaki kuralları ve yönergeleri oluşturur.

Avrupa bankalarından oluşan EPC, SEPA ödeme araçları için ticari ve teknik çerçeveleri geliştirir. Üç tip SEPA ödemesi kullanılır:

-   Kredi transferleri
-   Otomatik ödemeler
-   Kartlar

## <a name="what-is-a-sepa-credit-transfer"></a>SEPA kredi transferi nedir?
SEPA kredi transferi bir şirketten veya bir bireyden başka bir şirket veya bireye yapılan ödemedir. Ödemelerin Euro cinsinden olması gerekir ve her iki taraf için Uluslararası Banka Hesap Numarası (IBAN) ve Banka Tanımlayıcı Kodunu (BIC) içermelidir. (BIC da Society for Worldwide Interbank mali telekomünikasyon denir \[SWIFT\] kod.) Ayrıca, işlem maliyetleri her iki taraf arasında paylaştırılması gerekir. Taraflar arasında oluşan kredi transferlerinde ISO 20022 ödeme işleme standartları ve EPC tarafından belirtildiği gibi XML formatıyla uyumlu XML dosyaları kullanılmalıdır.

## <a name="how-is-a-credit-transfer-implemented"></a>Kredi transferi nasıl uygulanıyor?
Avrupa ülkelerinin kredi transfer ödeme biçimi içinde Dynamics 365 işlemlerinde elektronik Raporlama (ER) ve ödeme işlevini yöntemleri kullanarak uygulanır. Diğer bölgelerde kullanılan birkaç kredi aktarım biçimleri hala eski ödeme çerçevesi kullanın. Diğer birçok biçimleri arasında bulunan on iki ISO 20022 kredi transfer dosya biçimleri vardır. Bu verme biçimleri SEPA ISO 20022 XML standardına uygun. Ülkeler/bölgeler nerede kullanıldığını ve SEPA kredi Transfer düzeni, EPC yayımları Rulebook sürüm 8.2 belirtildiği gibi euro ödemeler için euro Ödeme transferleri üretmek için kullanılır. Elektronik bankacılık dosyaları karşıya yüklemek için gerekli olan yazılımı edinmek için banka, kredi transferleri uygulayabilirsiniz önce başvurmanız gerekir. Bankanız için ödeme emirleri içeren XML dosyaları transfer etmek için bu yazılımı kullanır.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Hangi kredi transfer biçimleri Dynamics 365 işlemleri için de şu anda desteklenir?
Siz her zaman Microsoft Dynamics ömrü Hizmetleri (LCS) paylaşılan varlık Kitaplığı'na gidin ve bir kıymet türü kullanılabilir dosyaları hakkında en güncel listesini görüntülemek **Tanımlanmı yapılandırma**. Sonraki "Ne ayarlamak sahibim?" bölümünde, kullanılabilir yapılandırmalarını gözden geçirin ve seçili yapılandırmaları almak için bir LCS deposunu açıklar konuya bir bağlantı sağlar.

## <a name="what-do-i-have-to-set-up"></a>Neyi ayarlamam gerekiyor?
-   Kredi transfer dosyaları oluşturmadan önce en az bir etkin kredi transfer yapılandırma ER yapılandırmalarınızı aktarılması gerekir. Yönergeler için bkz: [yükleme yapılandırmaları ömrü Hizmetleri'nden raporlama elektronik](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Borç hesabı ödeme yöntemlerini yapılandırırken, **genel elektronik raporlama** onay kutusunu işaretleyin ve uygun kredi aktarma biçimini seçin (örneğin, **ISO 20022 kredi transferi (AT)**) bir dışa aktarma biçimi yapılandırması.
-   Dynamics 365 işlemleri için yasal varlığı ve banka hesap bilgilerini de ayarlamanız gerekir.
-   Banka hesap numaraları, IBANs ve bazen SWIFT kodları (BICs) veya diğer kimlikler geçerli kredi transferi ödemeleri oluşturmak için gereklidir. Bu nedenle, Satıcı banka hesabı ve banka hesabı için aktarımı isteyen kuruluş için bunları ayarlamalısınız.
-   Ek bilgiler kredi transfer ileti içinde başvurulan taraflar için katma değer vergisi (KDV) numaraları gibi gerekli olabilir. İstek geldiğinde bu bilgileri tüzel ve satıcılar için ayarlanması gerekir.
-   Bazı hesaplar borç ödeme yöntemleri, çoğunlukla ISO 20022 tabanlı ödeme yöntemleri, için ek kurulum gerektirebilir **ödeme biçimi kod kümeleri**, aþaðýdaki gibi **hizmet türü** = **SLEV**. Bu kodlar, ek ödeme hareketleri için ödeme işleme sırasında etiketleme olarak kullanılır. Varsayılan değerleri ödeme kodları gibi **kategori amaç**, **gider taşıyıcı**, **yerel Aleti** ve **hizmet düzeyi** iki yerde ayarlanabilir. İlk yerdir **hesaplarına borç ödeme günlük başlığı** ve ikincisi ise **hesaplarına borç ödeme yöntemleri**. Bağlı ödeme günlük satırları oluşturma, ödeme günlüğü başlığındaki Ödeme kodu değerleri bir günlük satırına transfer değilse ayarlamak, ödeme yöntemleri alınan değerler kullanılır.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Hangi parametreler kredi transfer ödemeleri üretmek için kullanılabilir mi?
Özel parametre listesi kredi transfer biçimine bağlıdır. Satıcı ödeme günlüğüne Almanya için bir ISO 20022 kredi transfer ödeme dosyası oluştururken kullanılabilen parametreleri aşağıdaki tabloda gösterilmiştir. Kullanılabilir seçenekleri kullanarak **arka planda çalışan** sekmesinde, ödeme oluşturma toplu modda çalıştırabilirsiniz.

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
<li><strong>Strd</strong> – yapısal biçiminde bir ödeme satırı karşı bir fatura kapatıldığında kullanmak için bu seçeneği seçin. Fransa, Almanya ve Hollanda için ülkeye/bölgeye özgü verme biçimleri için bu seçenek kullanılamaz.</li>
<li><strong>Ustrd</strong> – Bir ödeme çok sayıda faturaya kapatıldığında yapılandırılmamış biçimi kullanmak için bu seçeneği seçin. Kapatılan faturalar için fatura numaraları birleştirilir ve havale bilgisi olarak kullanılır. ISO 20022 uygun yönergeleri, yapılandırılmamış havale bilgileri 140 karakterden oluşabilir.</li>
</ul></td>
</tr>
<tr class="even">
<td>Fatura sayısı</td>
<td>Fatura numarasını girin, <strong>ödeme ihbarnamesi</strong> rapor yazdırılır.</td>
</tr>
<tr class="odd">
<td>Numara serisi</td>
<td>Dosyayı tanımlamak için bir seri numarası girin. Sıra numarası görünür <strong>ilişkili Not</strong> rapor.</td>
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
Uluslararası Banka hesap numarası (IBAN) ve banka tanımlayıcı kodu (BIC) birçok ülkelerde/bölgelerde dünya çapında herhangi bir hesabı tanımlamak için kullanılır. Bunlar, 34 SEPA ülkeleri/bölgeleri içerir. BIC içinde girin **SWIFT kodu** alan ve IBAN'ın içinde **IBAN** alan. Alacaklı ait banka hesabı ve müşteri banka hesabı için bu alanları üzerinde bulunan **ek kimlik** üzerinde hızlı **banka hesabı** sekmesinde **banka hesaplarını** sayfa. SEPA ödemeleri için BIC kullanılması artık zorlanır.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Bir ödeme dosyasını bankaya nasıl iletirim?
Ödemeler oluşturmak, ödeme dosyası oluşturulur ve web tarayıcınızdan kullanılabilir herhangi bir konuma kaydetmek istenir. Sonraki adım, XML dosyasının bankanıza göndermektir. Bu işlem bankadan bankaya değişir. Dosyaları işlemek için bankaya göndermek için bankanızın talimatlarını izleyin.


