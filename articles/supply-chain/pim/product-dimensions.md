---
title: Ürün boyutları
description: Dört ürün boyutu bulunur - Renk, Yapılandırma, Boyut ve Stil. Ürün boyutlarını boyut gruplarında birleştirebilirsiniz ve ürün master öğelerine boyut grupları atayabilirsiniz. Ürün boyutlarının kombinasyonları, ürün çeşitlerinin nasıl tanımlanacağını belirler.
author: cvocph
manager: tfehr
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5e9b10fa18ada9534ce5e279d4f1f09973a802b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208444"
---
# <a name="product-dimensions"></a>Ürün boyutları

[!include [banner](../includes/banner.md)]

Dört ürün boyutu bulunur - Renk, Yapılandırma, Boyut ve Stil. Ürün boyutlarını boyut gruplarında birleştirebilirsiniz ve ürün master öğelerine boyut grupları atayabilirsiniz. Ürün boyutlarının kombinasyonları, ürün çeşitlerinin nasıl tanımlanacağını belirler.

Ürün boyutları, ürün varyantı tanımlamaya hizmet eden özelliklerdir. Ürün boyutlarının birleşimleri, ürün varyantları tanımlamak için kullanabilirsiniz. Bir ürün varyantı oluşturmak için bir ana ürüne en az bir ürün boyutu tanımlamanız gerekir.

## <a name="product-variants"></a>Ürün çeşitleri

Ürün varyantlarına maddeler de denilir. Bir madde bir hizmetten farklı olarak somut bir üründür. Hizmet türüyle bir ana ürün tanımlamak da mümkündür. Hizmet türü kullanarak hizmetleri içerecek ürün varyantları belirtebilirsiniz. Örneğin, Danışmanlık işi için bir ana ürün ve üst düzey danışmanlar ve alt düzey danışmanlar tarafından gerçekleştirilen iş için ürün varyantları belirtebilirsiniz.

## <a name="product-dimensions"></a>Ürün boyutları
Aşağıdaki ürün boyutları mevcuttur: Yapılandırma, Renk, Boyut ve Stil. Ürün boyut değerlerini temel alan bir ürün çeşidi oluşturulabilir.

Boyut, Renk ve Stil gibi ürün boyutu değerleri **Boyut**, **Renk** ve **Stil** sayfalarında oluşturulabilir ve bu sayfalara şu konumlardan erişilebilir: **Ürün bilgileri yönetimi** &gt; **Kurulum** &gt; **Boyut ve çeşit Grupları** &gt; **Boyutlar/Renkler/Stiller**. Yapılandırma boyutuna yönelik ürün boyutu genellikle ya Ürün yapılandırıcısı ya da Boyut bazlı yapılandırıcı kullanılarak oluşturulur. Ürün boyutları, aşağıdaki konumlardan erişilebilecek **Ürün boyutları** sayfasında da oluşturulup muhafaza edilebilir:
-   **Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Ana ürünler**'e tıklayın. **Eylem Bölmesi**'nde **Ürün boyutları**'na tıklayın.
-   **Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Tüm ürünler ve ana ürünler**'e tıklayın. Bir ana ürün seçin. **Eylem Bölmesi**'nde **Ürün boyutları**'na tıklayın.
-   **Ürün bilgileri yönetimi** &gt; **Serbest bırakılan ürünler**'e tıklayın. Bir ana ürün seçin. **Eylem Bölmesi**'nde, **Ürün**'e tıklayın. **Ana ürün** grubunda **Ürün boyutları**'na tıklayın.

Maddeler için oluşturabileceğiniz varyant sayısı, olası ürün boyutu kombinasyonlarının sayısı ile sınırlıdır.

| **İpucu**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bir ürünü örneğin bir emir satırında kullanırken, birlikle çalışmak istediğiniz ürün varyantını tanımlamak için ürün boyutlarını seçerseniz. |

## <a name="example"></a>Örnek
Bir şirket kot kumaşından ürünler satıyor. Kot kumaşı maddesi Renk ve Ebat boyutlarını kullanıyor. Kot kumaşları üç farklı renk ve altı farklı ebatta satılıyor. Renkler: Mavi, Siyah, Kahverengi Boyutlar: XS, S, M, L, XL, XXL Tüm rengin tümünde tüm ebatlar yoktur. Kombinasyonların tümü mevcut olsaydı, 18 farklı kot türü oluşturacaktı. Bu örnekte, yalnızca aşağıdaki dokuz ürün varyantı kombinasyonu üretilir.

| Renk | Ebat |
|-------|------|
| Mavi  | XS   |
| Mavi  | S    |
| Mavi  | P    |
| Siyah | P    |
| Siyah | L    |
| Siyah | XL   |
| Kahverengi | L    |
| Kahverengi | XL   |
| Kahverengi | XXL  |





