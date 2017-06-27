---
title: "SEPA otomatik ödemeye genel bakış"
description: "Tek Euro ödemeleri Alanı (SEPA), Avrupa Komisyonu tarafından ayarlanır ve tüm elektronik ödemelerin birey, işletme veya kuruluş ve bankanın bulunduğu ülke/bölgeden bağımsız olarak yurtiçi olarak kabul edildiğini belirler. Ulusal ve sınır ötesi ödemeler arasında hiçbir fark yoktur. SEPA, 28 Avrupa Birliği (AB) üyesi devletlerinin yanı sıra İzlanda, Liechtenstein, Norveç, İsviçre, Monako ve San Marino'yu içerir. SEPA, Avrupa Ekonomik Alanı (EEA) içinde ödeme hareketleri için tek bir pazar oluşturulmasına yardımcı olur. Sonuçta, SEPA'nın bankalar, işyerleri ve bireylerin çalışması gereken ödeme sayısını azaltması beklenir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f3b20b033fc701204cbb3f62468a421b3bdd6a80
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="sepa-direct-debit-overview"></a>SEPA otomatik ödemeye genel bakış

[!include[banner](../includes/banner.md)]


Tek Euro ödemeleri Alanı (SEPA), Avrupa Komisyonu tarafından ayarlanır ve tüm elektronik ödemelerin birey, işletme veya kuruluş ve bankanın bulunduğu ülke/bölgeden bağımsız olarak yurtiçi olarak kabul edildiğini belirler. Ulusal ve sınır ötesi ödemeler arasında hiçbir fark yoktur. SEPA, 28 Avrupa Birliği (AB) üyesi devletlerinin yanı sıra İzlanda, Liechtenstein, Norveç, İsviçre, Monako ve San Marino'yu içerir. SEPA, Avrupa Ekonomik Alanı (EEA) içinde ödeme hareketleri için tek bir pazar oluşturulmasına yardımcı olur. Sonuçta, SEPA'nın bankalar, işyerleri ve bireylerin çalışması gereken ödeme sayısını azaltması beklenir.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>SEPA otomatik ödemelerinin amacı nedir?
---------------------------------------

SEPA otomatik ödemesi, müşteri tarafından imzalanmış talimat olduğu takdirde, alacaklının bir müşterinin banka hesabından otomatik olarak fon toplamasına izin verir. Müşteri, alacaklının tahsilat yapmasına izin veren bir yönerge imzalar ve müşteri bankasına ödemeyi yapması doğrultusunda talimat verir. 

SEPA Otomatik Ödeme, ilk kez 32 SEPA ülke/bölgesi boyunca hem ulusal hem de sınırlar arası euro doğrudan alacakların ödemesinde kullanılabilecek bir ödeme aracı oluşturur. 

İki düzenleri vardır: SEPA çekirdek otomatik ödeme düzeni ve SEPA İşletmeler Arası (B2B) Otomatik Ödeme Düzeni. Her iki düzen de aynı dosya biçimini kullanır.

## <a name="what-is-the-core-direct-debit-scheme"></a>SEPA Çekirdek Otomatik Ödeme düzeni nedir?
SEPA Çekirdek Otomatik Ödeme Düzeni, temel düzendir. Aşağıdaki özniteliklere sahiptir:
-   Fon aktarımı (banka hesaplarının fonları diğer para birimleri cinsinden olsa bile) Euro cinsinden olur.
-   Hem müşteri ve hem de alacaklının firma SEPA içinde bulunan bir kredi kurumunda bir hesaplarının bulunması gerekir.
-   Müşterinin alacaklıya imzalı bir yönerge ile izin vermesi gerekir.
-   Yönergelerin kullanım süresi, son tahsilat sürecinden 36 ay sonra dolar.
-   Alacaklıların, yönergeyi geçerli olduğu müddetçe ve son tahsilattan en az 14 ay sonrasına kadar muhafaza etmeleri gereklidir.
-   Düzen sadece tek bir seferlik veya tekrar eden otomatik ödeme tahsilatları için kullanılabilir.
-   Müşterilerin, hesaplarından tahsilat yapıldıktan sekiz hafta sonrasına kadar sorgusuz sualsiz geri ödeme alma hakları vardır.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a> SEPA İşletmeler Arası Otomatik Ödeme düzeni nedir?
SEPA İşletmeler Arası Otomatik Ödeme Düzeni, işletmeler arasında gerçekleşen hareketlerde geçerlidir ve SEPA Çekirdek Otomatik Ödeme Düzeni'nine dayanır. Ana farklar şunlardır:
-   SEPA İşletmeler Arası Otomatik Ödeme Düzeni, müşteri bir birey (tüketici) ise izin verilmez.
-   Müşterinin yetkili bir hareketin para iadesi almaya hakkı yoktur.
-   Müşterinin bankası, yönergedeki bilgileri doğrulayarak, ödemenin yetkilendirilmiş olduğundan emin olmalıdır. Müşteri bankaları ve müşteriler her otomatik ödemede gerçekleşecek onaylamayı kabul etmek zorundadırlar.
-   Bu düzen otomatik ödemelerin sunulması için daha kısa bir zaman çizelgesi sunar ve dönüş süresini kısaltır.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a> Otomatik ödeme yönergeleri için COR1 düzenini kullanabilir miyim?
Evet. Avusturya, Belçika, Almanya, Fransa, İtalya, İspanya ve Hollanda içinde SEPA otomatik ödeme yönergesi için COR1 düzeni kullanabilirsiniz. Düzen, alacaklı için tahsilatın daha kısa süreli bir ön bildirim süresine sahip olmasını sağlar.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a> Uluslararası Banka hesap numarası (IBAN) ve banka tanımlayıcı kodu (BIC) nedir?
Uluslararası Banka Hesap Numarası (IBAN) ve Banka Tanımlayıcı Kodu (BIC), 32 SEPA ülkesindeki/bölgesindeki hesapları tanımlamak için kullanılır. SWIFT kodu alanına BIC'yi ve IBAN alanına IBAN'ı girin. Her iki alan da Banka hesapları sayfasının Banka hesabı sekmesindeki Ek Kimlik hızlı sekmesinde bulunur. Bu hem alacaklı banka hesabı hem de müşteri banka hesabı için geçerlidir.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a> Alacaklı tanımlayıcılarını (Otomatik ödeme kodu) nereye girilir?
SEPA içinde her Alacaklı benzersiz bir Alacaklı tanımlayıcısına göre tanımlanır. Bu tanımlayıcı müşterinin ve müşterinin bankasının her otomatik ödemeyi filtrelemesine ve daha sonra müşteri talimatına göre onaylamasına ya da reddetmesine yarar. Alacaklıların bu tanımlayıcıyı kendi bankaları aracılığıyla istemesi gerekir. Bu tanımlayıcıyı, tüzel kişiliğin banka hesabının Otomatik Ödeme Kodu alanına girin.

## <a name="what-are-mandates"></a> Yönergeler nedir?
Müşteri, alacaklının tahsilat yapmasına izin veren bir yönerge imzalar ve müşteri bankasına ödemeyi yapması doğrultusunda talimat verir. Müşteri, yönergeyi kağıda basılı ya da elektronik olarak çıkartabilir. Varsayılan olarak, doğrudan borç son kez başlatıldıktan 36 ay sonra yönerge sona erer.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a> SEPA Otomatik ödeme dosya biçimini (ISO 20022) nerede belirtirim?
SEPA veri biçimleri ISO 20022 ileti standartlarını temel alır. Genel elektronik raporlama onay kutusunu işaretleyin ve Alacak hesapları ödeme yöntemlerini yapılandırırken dışa aktarma biçimi yapılandırması olarak SEPA Otomatik ödeme biçimini seçin. Müşteri ödeme günlüğünde ödeme dosyası oluşturduğunuzda, bu ödeme yöntemini kullanırsınız.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a> SEPA otomatik ödeme dosyalarını hangi dosya formatında oluşturabilirim?
SEPA otomatik ödeme için elektronik ödeme dosyalarını aşağıdaki biçimlerde oluşturabilirsiniz:
-   Belçika, Almanya, İspanya, Fransa, İtalya ve Hollanda için PAIN.008.001.02 XML dosya biçimindeki SEPA otomatik ödeme dosyaları.
-   Avusturya için PAIN.008.001.02 XML ve Almanya için PAIN.008.003.02 XML dosya biçiminde SEPA otomatik ödeme dosyaları.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a> SEPA otomatik ödemelerde iadeler ve geri almalar nasıl işler?
Her iki SEPA Otomatik Ödeme düzeninde de, müşterilerin iade almaya çeşitli hakları vardır. Yetkilendirilmiş tüm hareketleri vade tarihinden sekiz hafta sonrasına kadar, bir sebep göstermeksizin geri çekme hakkı müşteriye verilmiştir. Yetkisiz işlemler söz konusu olduğunda ise bu süre vade tarihinden sonraki 13 aya kadar genişletilir. Yapılmış herhangi ödemelerin geri çevrilmesi, Müşteri hareketleri sayfasında elden Ödemeyi iptal et butonuna tıklayarak yapılır.






