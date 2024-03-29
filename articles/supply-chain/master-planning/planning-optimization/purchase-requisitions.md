---
title: Satın alma talepleri
description: Bu makalede satınalma talepleri açıklanmaktadır.
author: t-benebo
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: d9d55186307b18f4c3be78ae0828b08d3c987aad
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740697"
---
# <a name="purchase-requisitions"></a>Satın alma talepleri

[!include [banner](../../includes/banner.md)]

Master planlama onaylı satın alma taleplerini yenileyebilir. Bu sayede, kullanıcılar satın alma taleplerini karşılamak için iş akışı kullanarak satınalma siparişi oluşturmak zorunda kalmaz. Bunun yerine, satınalma talepleri master planlama tarafından karşılanabilir. Bu işlevsellik sayesinde satınalma talebi, ilgili ürün için ayarlanan **Planlı sipariş türü** değerine bağlı olarak satınalma siparişi, transfer emri veya üretim emri oluşturabilir.

## <a name="enable-master-plans-to-include-requisitions"></a>Talepleri dahil etmek için master planları etkinleştirme

Bir master plan için karşılama hesaplaması sırasında talepleri dahil etmek üzere aşağıdaki adımları izleyin.

1. **Master planlama** \> **Kurulum** \> **Planlar** \> **Master planlar** bölümüne gidin.
1. Bir master plan oluşturun veya seçin.
1. **Genel** hızlı sekmesinde, **Talepleri dahil et** seçeneğini *Evet* olarak ayarlayın.
1. Talepleri dahil etmek istediğiniz her ek master plan için 2 ve 3 numaralı adımları yineleyin.

## <a name="approved-requisitions-time-fence"></a>Onaylanmış talepler zaman dilimi

*Onaylı talepler zaman dilimi*, master planın onaylı stok yenileme taleplerinde ne kadar önceden (gün cinsinden) talepleri dahil edeceğini belirler. Onaylı talep zaman dilimini, hem kapsam grubu düzeyinde hem de master plan düzeyinde ayarlayabilirsiniz.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Kapsam grubu için onaylı taleplerin zaman dilimini ayarlama

1. **Master planlama** \> **Kurulum** \> **Kapsam** \> **Kapsam grupları**'na gidin.
1. Kapsam grubu oluşturun veya seçin.
1. **Diğer** hızlı sekmesinde, **Onaylanmış talepler zaman dilimi (gün)** alanını zaman dilimine dahil edilecek gün sayısına göre ayarlayın.
1. Onaylanmış talepler zaman dilimini ayarlamak istediğiniz her ek kapsam grubu için 2. ve 3. adımları tekrarlayın.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Ayrı master planlar için onaylanmış talepler zaman dilimini ayarlama

Ayrı master planlar için onaylanmış taleplerin zaman dilimi ayarladığınızda ayar, geçerli kapsam grubunun zaman dilimi ayarını geçersiz kılar.

1. **Master planlama** \> **Kurulum** \> **Planlar** \> **Master planlar** bölümüne gidin.
1. Bir master plan oluşturun veya seçin.
1. **Gün cinsinden zaman dilimleri** hızlı sekmesinde, **Onaylanmış talepler zaman dilimi (gün)** alanını zaman dilimine dahil edilecek gün sayısına göre ayarlayın.
1. Onaylanmış talepler zaman dilimini ayarlamak istediğiniz her ek master plan için 2. ve 3. adımları tekrarlayın.

> [!IMPORTANT]
> Onaylı taleplerin zaman dilimleri, Planlama Optimizasyonu için desteklenmemektedir. Desteklenene kadar **Onaylanmış talepler zaman dilimi (gün)** alanına gireceğiniz tüm değerler yoksayılır.

## <a name="independent-supply-regardless-of-coverage-code"></a>Kapsam koduna bakılmaksızın bağımsız tedarik

Kapsam kodu ne olursa olsun, satın alma talepleri he zaman bağımsız planlı siparişler tarafından kapsanır. Bu davranış, satın alma talepleri ve stok yenileme siparişleri arasında daha net izlenebilirlik ve iş akışları sağlar.

### <a name="example-1"></a>Örnek 1

**Kapsam kodu** değeri *Min/maks* olacak şekilde bir ürün ayarlanır. Ürünün, stok ve talep durumları aşağıdaki şekildedir.

- Eldeki stok miktarı = 10.
- Minimum stok miktarı = 15.
- Maksimum stok miktarı = 20.
- Tek bir adet için satınalma talebi var. Talep edilme tarihi bugün.

Master planlama çalıştırıldığında, iki planlı sipariş oluşturulur: Biri, stoku maksimum miktara göre yenilemek için 10 adede göre, diğeri ise satınalma talebini karşılamak için bir adede göredir.

### <a name="example-2"></a>Örnek 2

**Kapsam kodu** değeri *Min/maks* olacak şekilde bir ürün ayarlanır. Ürünün, stok ve talep durumları aşağıdaki şekildedir.

- Eldeki stok miktarı = 17.
- Minimum stok miktarı = 15.
- Maksimum stok miktarı = 20.
- Tek bir adet için satınalma talebi var. Talep edilme tarihi bugün.

Master planlama çalıştırıldığında, satınalma talebini karşılamak için bir adet için bir planlı sipariş oluşturulur.

### <a name="example-3"></a>Örnek 3

**Kapsam kodu** *Dönem* olak ve dönem uzunluğu yedi gün olan bir ürün ayarlanır. Aşağıdaki stok, satış siparişi ve talep durumlarına sahiptir:

- Eldeki stok miktarı = 0.
- Beş adet için bir satış siparişi var. Beklenen sevkiyat tarihi bugün artı bir gündür.
- Üç adet için satınalma talebi var. Talep edilme tarihi bugün artı üç gündür.

Master planlama çalıştırıldığında, iki planlı sipariş oluşturulur: Biri, satınalma talebini karşılamak için üç adede göre, diğer satış siparişi talebini karşılamak için beş adede göredir.

> [!NOTE]
> Bir satınalma talebiyle ilişkilendirilmiş bir planlı sipariş kesinleştirildikten sonra, planlama altyapısı, satınalma talebiyle ilişkilendirmeyi korur. Kesinleştirilmiş siparişin satınalma talebini yerine getirmek için gerekli miktara sahip olmadığı görülürse sistem, aradaki fark için yeni bir planlı sipariş oluşturur.

Satın alma talepleri hakkında daha fazla bilgi için bkz. [Satınalma talebine genel bakış](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]