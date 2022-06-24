---
title: Ölçü birimi ayarlarını uygulama
description: Bu makale, ölçü birimlerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ca95bd31af8f244f60f12120bc6df121f48cc7ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884827"
---
# <a name="apply-unit-of-measure-settings"></a>Ölçü birimi ayarlarını uygulama

[!include [banner](includes/banner.md)]

Bu makale, ölçü birimlerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .

Bir ürün, "tekli" "çift" ve "düzine" gibi farklı birimlerde satılabilir. Commerce genel merkezde bir ürünün satış ile ilgili ölçü birimi tanımlanabilir ve bir e-ticaret sitesinde görüntülenebilir. Örneğin, bir satıcı bir ürünü tek başına ve düzineler olarak satıyorsa kullanılabilir ölçü birimleri diğer ürün bilgileriyle birlikte gösterilebilir.

Aşağıdaki görseldeki örnekte, Commerce genel merkezde bir ürün için **beher** (tekli) satış ölçü birimi yapılandırılmıştır.

![Commerce genel merkezde ölçü birimiyle yapılandırılmış bir ürün örneği.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Ölçü birimini uygulama ve gösterme desteği, Commerce sürümü 10.0.19 itibariyle kullanılabilir.

## <a name="unit-of-measure-settings"></a>Ölçü birimi ayarları

Ölçü birimi görüntüleme ayarları, Commerce site oluşturucuda, **Site ayarları \> Uzantılar \>Ürünlerin görünüm ölçü birimleri** bölümünde belirlenir. Desteklenen üç ayar vardır:

- **Görüntüleme** – Bu ayar seçildiğinde, e-ticaret sitesi ürünün ölçü birimini göstermez. Bu davranış, varsayılan davranıştır.
- **Ürün satın alma deneyiminde görüntüle** - Bu ayar seçildiğinde, ölçü birimi; ürün detayları, sepet, ödeme, sipariş geçmişi ve sipariş ayrıntıları sayfalarında gösterilir.
- **Ürün tarama ve satın alma deneyiminde görüntüle** - Bu ayar seçildiğinde, ölçü birimi ürün satın alma deneyimi sayfalarında ve ayrıca ürün tarama deneyimi sırasında gösterilir. Bu davranışın bir parçası olarak, arama sonuçlarında ve ürün koleksiyonu modüllerinde ölçü birimleri gösterilir.

> [!IMPORTANT]
> Ölçü birimi görüntüleme ayarları Commerce sürüm 10.0.19'dan itibaren mevcuttur. Commerce'ün eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir. Talimatlar için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Ölçü birimi ayarlarını kullanan modüller

Ölçü birimi ayarlarını kullanan modüllere satınalma kutusu, istek listesi, sepet, sepet simgesi, arama sonuçları konteyneri, ürün koleksiyonu, ödeme ve sipariş ayrıntıları dahildir.

Aşağıdaki görselde yer alan örnekte, bir ürün ayrıntıları sayfası (PDP) bir ürünün ölçü birimini (**beher**) gösterir.

![Ölçü birimini gösteren bir PDP örneği.](./media/Productunit-PDP.png)

Aşağıdaki görselde yer alan örnekte, bir ürün koleksiyon modülü bir ürünün ölçü birimini (**beher**) gösterir.

![Ölçü birimini gösteren bir ürün koleksiyon modülü örneği.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Hesap yönetimi sayfaları ve modülleri](account-management.md)

[SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
