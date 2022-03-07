---
title: Çevrimiçi siparişler için satış vergisini yapılandırma
description: Bu konu, Dynamics 365 Commerce'de farklı çevrimiçi sipariş türleri için satış vergisi grubu seçimine genel bir bakış sağlar .
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5801bbfb5b5850cb4c9ae06140bff5adca9b368febdc06d69c538fc49f9ee40a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772973"
---
# <a name="configure-sales-tax-for-online-orders"></a>Çevrimiçi siparişler için satış vergisini yapılandırma

[!include [banner](includes/banner.md)]

Bu konu, hedef tabanlı veya müşteri hesabı tabanlı vergi ayarlarını kullanan farklı çevrimiçi sipariş türleriyle ilgili satış vergisi grubu seçimine genel bir bakış sağlar. 

E-ticaret kanalınızın, çevrimiçi siparişler için teslimat ve malzeme çekme gibi seçenekleri desteklemesini isteyebilirsiniz. Satış vergi uygulanabilirliğini, çevrimiçi müşterilerinizin seçtiği seçeneğe göre yapılır. 

## <a name="destination-based-taxes-for-online-orders"></a>Çevrimiçi siparişler için hedef tabanlı vergiler

Genel olarak, Müşteri adresine sevkiyat amacıyla gönderilen çevrimiçi siparişler için vergiler hedef tarafından tanımlanır. Her satış vergisi grubunun, işletmenizin ülke veya bölge, eyalet, ilçe ve şehir gibi hedef ayrıntılarını hiyerarşik bir formda tanımlayabileceği, perakende hedefi tabanlı bir vergi konfigürasyonu vardır.

### <a name="orders-delivered-to-customer-address"></a>Müşteri adresine teslim edilen siparişler

Bir çevrimiçi sipariş verildiğinde, Commerce vergi altyapısı, siparişteki her bir satır maddesinin teslimat adresini kullanır ve hedef esaslı vergi ölçütlerine sahip satış vergisi gruplarını bulur. Örneğin, California Francisco'ya ait satır maddesi teslimat adresi olan bir çevrimiçi sipariş için vergi altyapısı, California için satış vergisi grubunu ve satış vergisi kodunu bulacak ve her satır maddesi için vergiyi hesaplayacaktır.

### <a name="order-pick-up-in-store"></a>Mağazadan sipariş teslim alma

Mağazada teslim alma veya yolda teslim alma belirtilmiş sipariş satırları için, seçili teslim alma mağazasındaki vergi grubu uygulanır. Belirli bir mağaza için satış vergisinin nasıl ayarlanacağı hakkında ayrıntılı bilgi için bkz [Mağazalar için diğer vergi seçeneklerini ayarlama](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Çevrimiçi siparişler için müşteri hesabı tabanlı vergiler

Commerce Headquarters'da belirli bir müşteri hesabında satış vergisi grubunu yapılandırmak istediğiniz bir iş senaryosu olabilir. Headquarters'ta bir müşteri hesabındaki satış vergisini yapılandırabileceğiniz iki yer vardır. Bunlara erişmek için önce **Retail ve Commerce \> Müşteriler \> Tüm müşteriler**'e gidip müşteri seçerek bir müşteri ayrıntı sayfasına gitmeniz gereklidir.

Bir müşteri hesabı için satış vergisini yapılandırabileceğiniz iki yer şunlardır:

- Müşteri ayrıntıları sayfasındaki **Fatura ve teslimat** hızlı sekmesindeki **satış vergisi grubu**. 
- **Adresleri yönet** sayfasındaki **Genel** Hızlı sekmesindeki **Satış vergisi** sayfası. Müşteri ayrıntıları sayfasından buraya gitmek için **Adresler** hızlı sekmesi altından belirli bir adres seçin ve ardından **Gelişmiş**'i seçin.

> [!TIP]
> Çevrimiçi müşteri siparişleri için, yalnızca hedef tabanlı vergileri uygulamak ve müşteri hesabı tabanlı vergileri önlemek istiyorsanız, müşteri ayrıntıları sayfasının **Fatura ve teslimat** hızlı sekmesindeki **Satış vergisi grubu** alanının boş olduğundan emin olun. Çevrimiçi kanalı kullanarak kaydolan yeni müşterilerin varsayılan müşteri veya müşteri grubu ayarlarından satış vergisi grubu ayarlarını devralmamasını sağlamak için **Satış vergisi grubu** alanının, çevrimiçi kanal varsayılan müşteri ayarları ve müşteri grubu ayarları (**Retail ve Commerce \> Müşteriler \> Müşteri grupları**) için de boş olduğundan emin olun.

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Hedef tabanlı vergi veya müşteri hesabı tabanlı vergi uygulanabilirliğini belirleme 

Aşağıdaki tabloda, çevrimiçi siparişler için hedef tabanlı vergiler mi yoksa müşteri hesabı tabanlı vergiler mi uygulandığı açıklanmaktadır. 

| Müşteri türü | Sevkiyat adresi                   | Müşteri > Fatura ve teslimat > Satış vergisi grubu? | Merkezdeki müşteri hesabındaki adres? | Müşteri adresi > Gelişmiş > Genel > Satış vergisi grubu?                                              | Uygulanan satış vergisi grubu      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Konuk         | Manhattan, NY                      | Hayır (boş)                                                | Hayır (boş)                              | Hayır (boş)                                                                                                   | NY (hedef tabanlı vergiler) |
| Oturum açıldı     | Austin, TX                          | Hayır (boş)                                             | Evet                               | Hiçbiri<br/><br/>Çevrimiçi kanal koluyla eklenen yeni adres.                                                            | TX (hedef tabanlı vergiler) |
| Oturum açıldı     | San Francisco, CA (Mağazada teslim alma) | Evet (NY)                                            | Geçerli değil                              | Geçerli değil                                                                                                    | CA (hedef tabanlı vergiler) |
| Oturum açıldı     | Houston, TX                         | Evet (NY)                                            | Evet                               | Evet (NY)<br/><br/>Yeni adres çevrimiçi kanal aracılığıyla eklendi ve satış vergi grubu müşteri hesabından devralındı. | NY (müşteri hesabı tabanlı vergiler)  |
| Oturum açıldı     | Austin, TX                          | Evet (NY)                                            | Evet                               | Evet (NY)<br/><br/>Yeni adres çevrimiçi kanal aracılığıyla eklendi ve satış vergi grubu müşteri hesabından devralındı. | NY (müşteri hesabı tabanlı vergiler)  |
| Oturum açıldı     | Sarasota, FL                       | Evet (NY)                                            | Evet                               | Evet (WA)<br/><br/>El ile WA olarak ayarlandı.                                                                          | WA (müşteri hesabı tabanlı vergiler)  |
| Oturum açıldı     | Sarasota, FL                       | Hayır (boş)                                                | Evet                               | Evet (WA)<br/><br/>El ile WA olarak ayarlandı.                                                                          | WA (müşteri hesabı tabanlı vergiler)  |

## <a name="additional-resources"></a>Ek kaynaklar

[Hedefi temel alarak çevrimiçi mağazalar için vergiler ayarlama](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Satış vergisine genel bakış](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Kaynak alanında satış vergisi hesaplama yöntemleri](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[ Satış vergisi atama ve geçersiz kılma](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Satış vergisi kodları için Tam tutar ve Aralık hesaplama seçenekleri](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Vergi muafiyeti hesaplaması](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]