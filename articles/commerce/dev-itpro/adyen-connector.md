---
title: Adyen için Dynamics 365 Payment Connector'a genel bakış
description: Bu makale, Adyen için Microsoft Dynamics 365 Payment Connector'a genel bir bakış sağlar.
author: rassadi
ms.date: 10/27/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 931fc69cda8daa2e06b6f1155fbf0369fd2bca55
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728315"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Adyen için Dynamics 365 Payment Connector'a genel bakış

[!include [banner](../includes/banner.md)]

Bu makale, Adyen için Microsoft Dynamics 365 Payment Connector'a genel bir bakış sağlar ve desteklenen özellikler ve işlevlerin kapsamlı bir listesini içerir. İlgili makaleler, Adyen kayıt, bağlayıcı konfigürasyonu, sık sorulan soruların ve bazı genel sorunlar için sorun giderme kılavuzuna sahiptir.

## <a name="key-terms"></a>Önemli terimler

| Vade | Açıklama |
|---|---|
| Ödeme bağlayıcısı | Microsoft Dynamics 365 Commerce (ve ilişkili bileşenler) ve ödeme servisi arasında iletişim kolaylaştıran dahili bir uzantı. Bu makalede açıklanan bağlayıcı, standart ödeme yazılımı geliştirme seti (SDK) kullanılarak uygulanmıştır. |
| Kart mevcut | Fiziksel bir kartın sunulduğu ve Dynamics 365 Point of Sale sisteminde bir ödeme terminal bağlayıcısında kullanıldığı ödeme hareketlerine atıfta bulunur. |
| Kart mevcut değil | E-ticaret veya arama merkezi senaryoları gibi fiziksel bir kartın bulunmadığı ödeme hareketlerini gösterir. Bu senaryolarda, ödeme ile ilgili bilgiler bir E-ticaret web sitesine, bir Arama Merkezi akışına veya satış noktası veya ödeme terminali üzerine el ile girilir. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Desteklenen özellikler, işlevler, sürümler ve terminaller

Adyen için kullanıma hazır Dynamics 365 Payment Connector standart ödemeler SDK'sını kullanır. Bu nedenle, diğer ödeme bağlayıcılarında da kullanılamayan özel yetenekler yoktur.

### <a name="supported-versions"></a>Desteklenen sürümler

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 desteklenen sürümler
Adyen için ilk parti kullanıma hazır Dynamics 365 Payment Connector, Microsoft Dynamics 365 Finance sürüm 8.1.3 (Ocak 2019) veya sonrasında ve Microsoft Dynamics 365 Retail Sürüm 8.1.3 veya sonraki sürümlerde desteklenir. Ancak, üçüncü taraflar Microsoft Dynamics 365'in önceki sürümleri için başka ödeme bağlayıcıları geliştirebilirler.

#### <a name="supported-adyen-firmware-versions"></a>Desteklenen Adyen ürün bilgisi sürümleri

Aşağıdaki liste, Microsoft Dynamics 365 Retail POS'un her sürümü için desteklenen minimum ve maksimum Adyen bellenim sürümlerini açıklamaktadır.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS sürüm 10.0.25
| Minimum Adyen ürün bilgisi sürümü | Maksimum Adyen ürün bilgisi sürümü |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS sürüm 10.0.26
| Minimum Adyen ürün bilgisi sürümü | Maksimum Adyen ürün bilgisi sürümü |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS sürüm 10.0.27
| Minimum Adyen ürün bilgisi sürümü | Maksimum Adyen ürün bilgisi sürümü |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS sürüm 10.0.28
| Minimum Adyen ürün bilgisi sürümü | Maksimum Adyen ürün bilgisi sürümü |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS sürüm 10.0.29
| Minimum Adyen ürün bilgisi sürümü | Maksimum Adyen ürün bilgisi sürümü |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS sürüm 10.0.30
| Minimum Adyen ürün bilgisi sürümü | Maksimum Adyen ürün bilgisi sürümü |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Microsoft ana sürümü test ettikten sonra Adyen, ikincil sürüm güncelleştirmelerini serbest bırakabilir. Ana sürüm desteklendiği sürece, aynı ana sürüm içinde alt sürüm güncelleştirmeleri olması uygundur. Aynı ana ürün bilgisi sürümü daha önce sınandığı sürece, bu güncelleştirmeler normalde çok hedeflenmiş düzeltmelerdir ve tam yeniden test için çıtayı karşılamamaktadır. Güncelleştirmeler, belgelerde listelenen Adyen ürün bilgisi sürümünü aşmamalıdır. 
>
> 53 sürümünden önceki bir Adyen ürün bilgisi sürümüne geçiş yapmak için 53 sürümü, Commerce için POS KB **4577957** aylık ticari güncelleştirmeleri (10.0.11 ile 10.0.14 arasında) gerektirir. Bu sürümlerden biri kullanılıyorsa ve düzeltmeyi içermiyorsa, ödeme terminalinin yükseltme sonrası ödemelere yalnızca NFC aracılığıyla ödeme yapılmasına izin verilir. Düzeltmeyi POS'a uygulamak bu sorunu çözer. POS sürümü 10.0.11 sürümünden eskiyse, bir servis dışı MPOS için bir KB **4577957** düzeltmesi gerektiğini belirten bir destek isteği yapın.
> 
> Adyen üretici yazılımı sürümleri (59p7 ve 62p9 arası) için, **hediye kartı nakit çıkışı** işlemi, hediye kartının el ile girildiği senaryolarda iki kez PIN kodu ister. Hediye kartı kaydırıldığında bu sorun yeniden oluşturulmaz. Adyen araştırmaktadır. 

### <a name="supported-payment-terminals"></a>Desteklenen ödeme terminalleri
Adyen için Dynamics 365 Payment Connector, aygıt agnostik [Adyen ödeme terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) avantajlarından yararlanır. Bu uygulama programlama arabiriminin (API) desteklediği tüm ödeme terminallerini destekler. Desteklenen ödeme terminallerinin tam listesi için, bkz. [Adyen POS terminalleri](https://www.adyen.com/pos-payments/terminals) sayfası.

### <a name="supported-payment-instruments"></a>Desteklenen ödeme araçları

#### <a name="supported-debit-and-credit-cards"></a>Desteklenen banka ve kredi kartları

| Marka | Varyant | Kart mevcut | e-Ticaret | Çağrı Merkezi |
|---|---|:-:|:-:|:-:|
| MasterCard | Kredi | ✔ | ✔ | ✔ |
| MasterCard | Borç | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | Kredi | ✔ | ✔ | ✔ |
| VISA | Borç | ✔ | ✔ | ✔ |
| VISA | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Ödemesi | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia Card | ✔ | ✔ | ✔ |
| AMEX | Kredi | ✔ | ✔ | ✔ |
| AMEX | Borç | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| Bul | Standart | ✔ | ✔ | ✔ |
| Bul | Android Pay | ✔ |  |  |
| Bul | Apple Pay | ✔ |  |  |
| Bul | Samsung Pay | ✔ |  |  |
| Diners   | Standart | ✔ | ✔ | ✔ |
| Dineromail | Standart | ✔ | ✔ | ✔ |
| JCB | Standart | ✔ | ✔ | ✔ |
| Union Pay\* | Standart | ✔ |  |  |
| Interac Debit\* | Standart | ✔ |  |  |

\*Interac ve Union Pay yinelenen kart belirteçleri Adyen tarafından sağlanmamıştır bu nedenle, kart mevcut olmayan hareketler için desteklerden etkilenmezler.

#### <a name="supported-gift-cards"></a>Desteklenen hediye kartları
| Şema | Kart mevcut | Kart mevcut değil |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Adyen için Dynamics 365 Payment Connector aracılığıyla bu harici hediye kartı şemalarını desteklemek için ek adımları tamamlamanız gerekir. Daha fazla bilgi için bkz. [Harici hediye kartları için destek](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Desteklenen cüzdanlar

| Şema | Kart mevcut | Kart mevcut değil |
|---|---|---|
| Alipay | Destek, gelecekteki bir sürümde eklenecektir. | No. |
| WeChat | Destek, gelecekteki bir sürümde eklenecektir. | No. |

#### <a name="supported-card-present-input-methods"></a>Desteklenen kart sunum giriş yöntemleri
| Giriş yöntemi | Destekleniyor | Notlar |
|---|:-:|---|
| Dip | ✔ | |
| Kartı geçir | ✔ | |
| Dokundurma | ✔ | |
| POS UI aracılığıyla el ile giriş. |  | Şu anda desteklenmiyor |
| Ödeme terminali aracılığıyla el ile giriş. | ✔ | PIN girişi ile banka, borç ve hediye kartlarının el ile girişini destekler. | 


#### <a name="supported-card-present-countries"></a>Desteklenen kart mevcut ülkeler

Aşağıdaki ülkelerde ticari bileşenler kullanılabilir ve Adyen kart mevcut desteği sunar. Commerce'in geçerli uluslararası kullanılabilirliği için bkz. [Uluslararası kullanılabilirlik sayfası](/dynamics365/get-started/availability).

| Ülke/Bölge | Destekleniyor |
| --- | :-: |
| Avustralya | ✔ |
| Avusturya | ✔ |
| Belçika | ✔ |
| Kanada | ✔ |
| Çek Cumhuriyeti | ✔ |
| Danimarka | ✔ |
| Estonya | ✔ |
| Finlandiya | ✔ |
| Fransa | ✔ |
| Almanya | ✔ |
| Hong Kong ÖİB | ✔ |
| Macaristan | ✔ |
| İzlanda | ✔ |
| İrlanda | ✔ |
| İtalya | ✔ |
| Japonya | Gelecekteki sürüm |
| Letonya | ✔ |
| Litvanya | ✔ |
| Malezya | ✔ |
| Hollanda | ✔ |
| Yeni Zelanda | ✔ |
| Norveç | ✔ |
| Polonya | ✔ |
| Singapur | ✔ |
| İsviçre | ✔ |
| İspanya | ✔ |
| İsveç | ✔ |
| İsviçre | ✔ |
| Birleşik Krallık | ✔ |
| Amerika Birleşik Devletleri | ✔ |
| Brezilya | Gelecekteki sürüm |

#### <a name="supported-card-not-present-countries"></a>Desteklenen kart mevcut olmayan ülkeler

Aşağıdaki ülkeler kart, mevcut olmayan hareketler için Adyen tarafından desteklenir. Belirli bir ülkeye ilişkin destek hakkında ayrıntılar için [Adyen'e başvurun](https://www.adyen.com/contact/sales). Commerce'in geçerli uluslararası kullanılabilirliği için bkz. [Uluslararası kullanılabilirlik sayfası](/dynamics365/get-started/availability).

| Ülke/Bölge | 
| --- |
| Arjantin |
| Ermenistan |
| Avustralya |
| Avusturya |
| Bahreyn |
| Belçika |
| Brezilya |
| Bulgaristan |
| Kanada |
| Şili |
| Çin |
| Kolombiya |
| Hırvatistan |
| Kıbrıs |
| Çek Cumhuriyeti  |
| Danimarka |
| Mısır |
| Estonya |
| Finlandiya |
| Fransa |
| Gürcistan |
| Almanya |
| Cebelitarık |
| Yunanistan |
| Guernsey |
| Hong Kong ÖİB |
| Macaristan |
| İzlanda |
| Hindistan |
| Endonezya |
| İrlanda |
| Man Adası |
| İsrail |
| İtalya |
| Japonya |
| Jersey |
| Kore |
| Kuveyt |
| Letonya |
| Litvanya |
| Lüksemburg |
| Malezya |
| Malta |
| Meksika |
| Fas |
| Hollanda |
| Yeni Zelanda |
| Norveç |
| Peru |
| Polonya |
| Portekiz |
| Katar |
| Romanya |
| Suudi Arabistan |
| Sırbistan |
| Singapur |
| Slovakya |
| Slovenya |
| Güney Afrika |
| İspanya |
| İsveç |
| İsviçre |
| Tayvan |
| Tanzanya |
| Tayland |
| Türkiye |
| Birleşik Arap Emirlikleri (BAE) |
| Birleşik Krallık |
| Porto Riko dahil Amerika Birleşik Devletleri  |

#### <a name="supported-dynamics-365-payment-features"></a>Desteklenen Dynamics 365 ödeme özellikleri

Aşağıdaki tabloda, Adyen'in desteklediği Dynamics 365 Payment Connector'ın özellikler kümesi gösterilmiştir. Bu özellikler, ödemeler SDK'da tanıtılan geliştirmeleri ve Aralık 2018'deki bazı bileşenleri kullanır. Adyen için Dynamics 365 Payment Connector için özel değildir. Farklı bir ödeme bağlayıcısına yönelik bu geliştirmeleri nasıl ele alacağınız hakkında daha fazla bilgi için, bkz. [Ödeme terminali için uçtan uca ödeme entegrasyonu oluşturma](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Şema | Kart mevcut | Kart mevcut değil |
|---|:-:|:-:|
| [Hediye Kartı Bakiyesini Nakde Çevirme](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Yinelenen Ödemeleri Engelleme](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Çok Yönlü Kanal Belirteçlere Ayırma | ✔ | ✔ |
| Bağlantılı Geri Ödemeler | ✔<br>(10.0.1'den başlayarak) | ✔<br>(10.0.1'den başlayarak) |
| [Çevrimiçi ödemeleri kaydet](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(10.0.2'den başlayarak) | 
| [Arama merkezi ve e-ticaret için harici hediye kartları](./gift-card.md) | ✔<br>(10.0.10'den başlayarak) | 
| [SCA ödeme yeniden yönlendirmesi](../adyen_redirect.md) | | ✔<br>(10.0.12'den başlayarak) |
| [Yazıcı ve kasa çekmecesi için ayrılmış ödeme terminalleri ve istemleri](../pos-multi-hws.md) | ✔<br>(10.0.12'den başlayarak) | |
| [Adyen konnektörü aracılığıyla SDK düzeyinde bahşiş desteği](tipping.md) | ✔<br>(10.0.14'den başlayarak) | |
| [Sipariş faturalaması için artımlı yakalama](incremental-capture.md) |  | ✔<br>(10.0.18'den başlayarak) |
| [Cüzdan Ödemeleri](../wallets.md) |  | ✔<br>(10.0.20'den başlayarak) |
| [Adyen ile Google Pay](google-pay-adyen.md) |  | ✔<br>(10.0.27'den başlayarak) |

## <a name="next-steps"></a>Sonraki adımlar

Adyen için Dynamics 365 Payment Connector'a kaydolma ve bunu yapılandırma hakkında daha fazla bilgi için bkz. [Adyen için Dynamics 365 Payment Connector kurulumu](adyen-connector-setup.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Adyen için Dynamics 365 Payment Connector'ı ayarlama](adyen-connector-setup.md)

[Adyen için Dynamics 365 Payment Connector ile ilgili SSS](adyen-connector-faq.md)

[Adyen için Dynamics 365 Payment Connector sorunlarını giderme](adyen-connector-troubleshoot.md)

[Ödemeler ile ilgili SSS](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
