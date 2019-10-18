---
title: Varlık üreticileri ve modelleri
description: Bu konu, Varlık Yönetimi'nde varlık üreticilerinin ve ilgili modellerin nasıl ayarlanacağını açıklar.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e20ccf16bc751898b239214771821fd2872638d1
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783663"
---
# <a name="asset-manufacturers-and-models"></a>Varlık üreticileri ve modelleri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konu, Varlık Yönetimi'nde varlık üreticilerinin ve ilgili modellerin nasıl ayarlanacağını açıklar. Modeller, varlık türlerine bağlı olabilir.

## <a name="set-up-product-model-relations"></a>Ürün model ilişkileri ayarlama

1. **Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Üretici ve model**'i seçin.
2. Yeni ürün oluşturmak için **Yeni**'yi seçin.
3. **Üretici** alanına, varlık üreticisi için bir ad girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Modeller** hızlı sekmesinde, varlık üreticisiyle ilişkili olması gereken bir varlık modeli oluşturmak için **Ekle**'yi seçin.
6. **Model** alanına, varlık modeli için bir ad girin.
7. **Açıklama** alanına bir açıklama girin.
8. **Varlık türü** alanında, üretici modelinin ilgili olması gereken varlık türünü seçin.

    > [!NOTE]
    > Ayrıca varlık türleri, üreticiler ve modeller için **Varlık türleri** aramasında ilişkiler ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Varlık türü oluşturma](../setup-for-objects/object-types.md).

    **Ayrıntılar** hızlı sekmesinde, **Modeller** alanı seçili varlık üreticisinde ayarlanan varlık modeli sayısını gösterir. **Varlıklar** alanı seçili üreticiyi kullanan kıymet sayısını gösterir.
    
    **Varlıklar** alanı üretici modelini kullanan nesnelerin sayısını gösterir.

> [!NOTE]
> Bir varlık türünün hiçbir varlık üreticisi modeli ilişkisi olmayabilir, bir varlık üreticisi modeliyle ilşikili olabilir veya birden çok varlık üreticisi modeliyle ilişkili olabilir. Bir varlık türü en az bir üretici modeliyle ilişkiliyse, yalnızca **Üretici modeli** aramasında ayarlanan kombinasyonlar bir varlık türü, üretici ve model kombinasyonunun bulunduğu Varlık Yönetimi sayfalarında seçilebilir. Bu sayfalar **Tüm varlıklar**, **Varlık hizmet düzeyleri**, **iş türü varsayılanları** ve **Bakım bütçesi satırları**'nı içerir. Bazı varlık türleri herhangi bir üretici modeliyle ilişkili değilse, yalnızca bu varlık türleri ve varlık türleriyle hiçbir ilişkisi olmayan üretici modelleri sayfalarda gösterilir.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Bir nesne üzerinde üretici ve model seçme

1. **Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler** öğesini seçin.
2. **Varlık** sütununda, varlık için bağlantıyı seçin. **Ayrıntılar** sayfası görüntülenir.
3. **Düzenle** öğesini seçin.
4. **Genel** hızlı sekmesinde, **Üretici** ve **Model** alanlarında değerleri seçin.