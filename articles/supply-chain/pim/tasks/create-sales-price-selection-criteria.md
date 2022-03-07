---
title: Satış fiyatı seçim ölçütü oluşturma
description: Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568459"
---
# <a name="create-sales-price-selection-criteria"></a>Satış fiyatı seçim ölçütü oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir. Bu yordam için kullanılabilir en az bir satış fiyatı modeli olması gerekir. Bu örnek için, USMF demo veri şirketinde Hoparlör çözümü satış fiyatı modeli için fiyat modeli kullanılır. Genel olarak bu yordamı bir ürün yöneticisi kullanır.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Mevcut satış fiyatı modeli için yeni bir ölçüt ekleme

1. **Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
1. Listede, Hoparlör çözümü ürün modeli için satır seçin ancak model adı bağlantısını seçmeyin.
1. Eylem Bölmesinde, **Model**'i seçin.
1. **Fiyat modeli ölçütleri**'ni seçin.
1. **Yeni**'yi seçin.
1. **Ad** alanına "Müşteri grubu 10" yazın.
    * Fiyat modeli ölçütünün adı, temel alınan seçim ölçütlerinin tanımlanmasına yardımcı olmak için kullanılır.  
1. **Fiyat modeli** alanına bir değer girin veya seçin.
1. **Sipariş türü** alanında *Satış siparişi*'ni seçin.
    * Sipariş türü seçim sorgusu için kullanılacak veri tabanı alanlarını belirler.  
1. **Geçerlilik başlangıcı** alanına bir tarih girin.
1. **Geçerlilik sonu** alanına bir tarih girin.
1. **Kaydet**'i seçin.

## <a name="create-the-query-for-the-selection-criteria"></a>Seçim ölçütleri için sorgu oluşturma

1. **Düzenle** öğesini seçin.
2. **Tablo** alanında, *Müşteriler*'i seçin.
3. **Alan** alanında *Müşteri grubu*'nu seçin.
    * Bu örnekte, seçim ölçütü için belirli bir müşteri grubu kullanacağız.  
4. **Ölçütler** alanında *Müşteri grubu 10*'u seçin.
5. **Tamam**'ı seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]