---
title: Çevrimiçi siparişler için satış vergisini yapılandırma
description: Bu konu, Dynamics 365 Commerce'de farklı çevrimiçi sipariş türleri için satış vergisi grubu seçimine genel bir bakış sağlar .
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254853"
---
# <a name="configure-sales-tax-for-online-orders"></a>Çevrimiçi siparişler için satış vergisini yapılandırma

[!include [banner](includes/banner.md)]

Bu konu, farklı çevrimiçi sipariş türleri için satış vergisi grubu seçimine genel bir bakış sağlar. 

E-ticaret kanallarınız, çevrimiçi siparişler için teslimat ve malzeme çekme gibi seçenekleri desteklemek isteyebilir. Satış vergi uygulanabilirliğini, çevrimiçi kullanıcılarınızın seçtiği seçeneğe göre yapılır. Bir site müşterisi, bir maddeyi çevrimiçi olarak satın almayı ve onu bir adrese sevk edilmesini seçtiğinde, satış vergisi müşterinin sevkiyat adresi vergi grubu ayarına göre belirlenir. Bir müşteri bir mağazada satın alınan bir maddeyi çekme işlemi yaparken, satış vergisi malzeme çekme deposunun vergi grubu ayarına göre belirlenir. 

## <a name="orders-shipped-to-a-customer-address"></a>Müşteri adresine sevk edilen siparişler 

Genel olarak, Müşteri adresine sevkiyat amacıyla gönderilen çevrimiçi siparişler için vergiler hedef tarafından tanımlanır. Her satış vergisi grubunun, işletmenizin İlçe/Bölge, eyalet, ilçe ve şehir gibi hedef ayrıntılarını hiyerarşik bir formda tanımlayabileceği, perakende hedefi tabanlı bir vergi konfigürasyonu vardır. Bir çevrimiçi sipariş verildiğinde, Commerce vergi altyapısı, siparişteki her bir satır maddesinin teslimat adresini kullanır ve hedef esaslı vergi ölçütlerine sahip satış vergisi gruplarını bulur. Örneğin, California Francisco'ya ait satır maddesi teslimat adresi olan bir çevrimiçi sipariş için vergi altyapısı, California için satış vergisi grubunu ve satış vergisi kodunu bulacak ve her satır maddesi için vergiyi hesaplayacaktır.  

## <a name="customer-based-tax-groups"></a>Müşteri tabanlı vergi grupları

Commerce Headquarters'da, müşteri vergi gruplarının konfigüre edildiği iki yer vardır:

- **Müşterinin profili**
- **Müşterinin sevkiyat adresi**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Bir müşterinin profilinde konfigüre edilmiş bir vergi grubu varsa

Müşteri merkezindeki bir müşterinin profil kaydının konfigüre edilmiş bir satış vergisi grubu olabilir; ancak çevrimiçi siparişler için vergi altyapısı tarafından konfigüre edilen satış vergisi grubu kullanılmaz. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Bir müşterinin teslimat adresinde konfigüre edilmiş bir vergi grubu varsa

Müşterinin sevkiyat adresi kaydının konfigüre edilmiş bir vergi grubu varsa ve müşterinin sevkiyat adresine bir çevrimiçi sipariş (veya satır maddesi) sevk edilmişse, müşterinin adres kaydında konfigüre edilen vergi grubu vergi hesaplamaları için vergi alt yapısı tarafından kullanılacaktır.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Bir müşterinin teslimat adresi kaydı için vergi grubunu yapılandırın

Commerce Headquarters'da müşterinin sevkiyat adresi kaydı için bir vergi grubu konfigüre etmek üzere aşağıdaki adımları izleyin.

1. **Tüm müşteriler**'e gidin ve istediğiniz müşteriyi seçin. 
1. **Adresler** hızlı sekmesinde, istediğiniz adresi seçin ve **Daha fazla seçenek \> Gelişmiş**'i seçin. 
1. **Adresleri Yönet** sayfasının **Genel** sekmesi altında satış vergisi değerini gerektiği gibi ayarlayın.

> [!NOTE]
> Vergi grubu sipariş satırının teslimat adresi ve hedef esaslı vergiler vergi grubunun kendisinde konfigüre edilmiş olarak tanımlanır. Daha fazla bilgi için, bkz [Hedefe bağlı olara çevrimiçi mağazalar için vergiler ayarlayın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Mağazadan sipariş teslim alma

Mağazada malzeme çekme veya perde çekme belirtilmiş sipariş satırları için, seçili malzeme çekme deposundaki vergi grubu uygulanır. Belirli bir mağaza için vergi grubunun nasıl konfigüre nakledileceği hakkında ayrıntılı bilgi için bkz [Mağazalar için diğer vergi seçenekleri ayarlayın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Bir mağazada sipariş satırı çekildiğinde, vergi altyapısı (ayarlanmış ise) için müşterinin adres vergi ayarları yoksayılacaktır ve malzeme çekme deposunun vergi konfigürasyonu uygulanır. 

## <a name="additional-resources"></a>Ek kaynaklar

[Satış vergisine genel bakış](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Kaynak alanında satış vergisi hesaplama yöntemleri](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ Satış vergisi atama ve geçersiz kılma](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Satış vergisi kodları için Tam tutar ve Aralık hesaplama seçenekleri](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Vergi muafiyeti hesaplaması](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]