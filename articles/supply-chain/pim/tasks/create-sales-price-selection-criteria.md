---
title: Satış fiyatı seçim ölçütü oluşturma
description: Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae444008e550d808a02d55dad02cc1b52874f0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439289"
---
# <a name="create-sales-price-selection-criteria"></a>Satış fiyatı seçim ölçütü oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, öznitelik tabanlı satış fiyat modelleri için satış fiyatı seçim ölçütlerinin nasıl oluşturulacağını gösterir. Bu yordam için kullanılabilir en az bir satış fiyatı modeli olması gerekir. Bu örnek için, USMF demo veri şirketinde Hoparlör çözümü satış fiyatı modeli için fiyat modeli kullanılır. Genel olarak bu yordamı bir ürün yöneticisi kullanır.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Mevcut satış fiyatı modeli için yeni bir ölçüt ekleme
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Listede, Hoparlör çözümü ürün modeli için satır seçin ancak model adı bağlantısına tıklamayın.
4. Eylem Bölmesinde,Model öğesine tıklayın.
5. Fiyat modeli ölçütlerine tıklayın.
6. Yeni'yi tıklatın.
7. Ad alanına "Müşteri grubu 10" yazın.
    * Fiyat modeli ölçütünün adı, temel alınan seçim ölçütlerinin tanımlanmasına yardımcı olmak için kullanılır.  
8. Fiyat modeli alanına bir değer girin veya seçin.
9. Sipariş türü alanında Satış siparişi'ni seçin.
    * Sipariş türü seçim sorgusu için kullanılacak veri tabanı alanlarını belirler.  
10. Geçerlilik başlangıcı alanına bir tarih girin.
11. Geçerlilik sonu alanına bir tarih girin.
12. Kaydet'e tıklayın.

## <a name="create-the-query-for-the-selection-criteria"></a>Seçim ölçütleri için sorgu oluşturma
1. Düzenle öğesine tıklayın.
2. Tablo alanında, Müşteriler'i seçin. 
3. Alan alanında Müşteri grubu'nu seçin.
    * Bu örnekte, seçim ölçütü için belirli bir müşteri grubu kullanacağız.  
4. Ölçütler alanında Müşteri grubu 10'u seçin. 
5. Tamam'a tıklayın.

