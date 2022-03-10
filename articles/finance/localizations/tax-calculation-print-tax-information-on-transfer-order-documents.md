---
title: Transfer emri belgelerinde vergi bilgilerini yazdır
description: Bu konu, vergi hesaplama servisi tarafından belirlenen vergi bilgilerinin transfer emri belgelerine nasıl basılabileceği bilgisi açıklamaktadır.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 174cbd85139db5cee75481041fb721dc7646ab66
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913614"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Transfer emri belgelerinde vergi bilgilerini yazdır

[!include [banner](../../includes/banner.md)]

Bu konuda, transfer emri belgelerinde vergi bilgilerinin nasıl yazdırılacağı açıklanmaktadır. Avrupa Birliği (AB) katma değer vergisi (KDV) düzenelemeleri kapsamında topluluk içi tedarik ve topluluk içi satın alımlar olarak kabul edilen stok transferleri için transfer emrinin proforma fatura belgesini yazdırabilirsiniz. 

Aşağıdaki vergiyle ilgili veriler transfer emri belgelerine eklenir:

- Stok transferinin adları ve sevk edilen ve sevk edilecek adresler
- Tedarikçinin ve alıcının vergi kimlik numaraları
- Sağlanan malların birim fiyatı ve vergiye tabi tutarı
- Vergi kodu, vergi oranı, vergi tutarı ve vergi yönergeleri

Bu verileri konfigüre etmek için aşağıdaki ana adımları tamamlamanız gerekir.

1. [Transfer emirleri için vergi özelliğini etkinleştirin ve ayarlayın](tasks/Tax-feature-support-for-transfer-order.md).
2. [Geçerli bir varlık için çoklu vergi kayıt numaraları oluşturun ve ayarlayın](emea-multiple-vat-registration-numbers.md).
3. Muafiyet kodunu, açıklamayı, vergi yönergelerini ve vergi kodlarındaki yazdırma kodunu ayarlayın. Bu örnekte, üç vergi kodu oluşturulur ve Microsoft Dynamics 365 Finance'ta eşitlenir: **NL-Exempt**, **BE-RC-21** ve **BE-RC+21**.

    1. Finance'te, **Vergi** \> **Kurulum** \> **Satış vergisi** \> **Satış vergisinden muaf kodlar**'a gidin.
    2. **Düzenle**'yi seçin ve **EC** muafiyet kodu için bir açıklama girin. Örneğin **Vergi sicil numarası ile vergiden muaf EC sevkiyatları** girin.
    3. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kodları**'na gidin.
    4. **BE RC-21** vergi kodunu seçin ve ardından **Vergi yönergeleri** seçeneğini belirleyin.
    5. **Yeni**'yi seçin.
    6. **Dil** alanında, **EN-US**'yi seçin. Daha sonra, **Metin** alanına, **AB KDV Yönergesi 2006/112/EC'nin 138. 2.c) maddesine göre malların transferini belirten belge**.
    7. Sayfayı kapatın.
    8. **Genel** hızlı sekmesinde, **Yazdır** alanında, **Satış vergisi oranı**'nı seçin.
    8. **NL muafiyet** vergi kodunu seçin ve **Genel** hızlı sekmesinde, **Yazdır** alanında **Satış vergisi oranı**'nı seçin.

    > [!NOTE] 
    > Vergi kodu için muafiyet kodu açıklaması veya vergi emirleri yoksa vergi kodu, vergi oranı ve vergi muafiyet açıklaması transfer emri belgelerine basılmamaktadır.

## <a name="print-the-transfer-order---shipment-document"></a>Transfer emri, sevkiyat belgesini yazdır

Transfer sevk edildiğinde, transfer emri sevkiyat belgesini yazdırmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi** \> **Sorgular ve raporlar** \> **Transfer emirleri** \> **Sevkiyat**'a gidin.
2. **Parametreler** sekmesinde, **Yazdır** grubunda **Vergi bilgilerini** etkinleştirin.
3. **Dahil edilecek kayıtlar** sekmesinde **Filtre**'yi seçin, transfer emri numarasını seçin ve **Tamam**'ı seçin.
4. Transfer emri, sevkiyat belgesini yazdırmak için **Tamam**'ı seçin.

## <a name="print-the-transfer-order---receipt-document"></a>Transfer emri, makbuz belgesini yazdır

Transfer alındıktan sonra, transfer emri makbuz belgesini yazdırmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi** \> **Sorgular ve raporlar** \> **Transfer emirleri** \> **Alma**'ya gidin.
2. **Parametreler** sekmesinde, **Yazdır** grubunda **Vergi bilgilerini** etkinleştirin.
3. **Dahil edilecek kayıtlar** sekmesinde **Filtre**'yi seçin, transfer emri numarasını seçin ve **Tamam**'ı seçin.
4. Transfer emri, makbuz belgesini yazdırmak için **Tamam**'ı seçin.

## <a name="print-the-transfer-overview-document"></a>Transfer genel bakış belgesini yazdırma

Transfer genel görünümü belgesini yazdırmak için bu adımları izleyin.

> [!NOTE]
> Vergi bilgileri yalnızca transfer emri sevk edildiğinde veya alındığında kullanılabilir.

1. **Stok yönetimi** \> **Sorgular ve raporlar** \> **Transfer emirleri** \> **Transfer genel bakış**'a gidin.
2. **Parametreler** sekmesinde, **Yazdır** grubunda **Vergi bilgilerini** etkinleştirin.
3. **Dahil edilecek kayıtlar** sekmesinde **Filtre**'yi seçin, transfer emri numarasını seçin ve **Tamam**'ı seçin.
4. Transfer emri, genel bakış belgesini yazdırmak için **Tamam**'ı seçin.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
