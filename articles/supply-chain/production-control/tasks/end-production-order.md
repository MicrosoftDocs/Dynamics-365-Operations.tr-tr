---
title: Üretim emrini bitirme
description: Bu yordam, bir üretim emrini nasıl sonlandırabileceğinizi gösterir.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb84d3b1908d6be889a49f7386de876cb52141ab
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149056"
---
# <a name="end-a-production-order"></a>Üretim emrini bitirme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir üretim emrini nasıl sonlandırabileceğinizi gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu, üretim emri ömrünü açıklayan yedi yordamdan sonuncusudur.


## <a name="end-a-production-order"></a>Üretim emrini bitirme
1. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
    * Durumu, bitirildi olarak raporlandı olan bir üretim emrini seçin.  
2. Eylem Bölmesinde, Üretim emri öğesine tıklayın.
3. Sonlandır'ı tıklatın.
    * Bu sayfada, üretim emrini sonlandırmak istediğinizi onaylayabilirsiniz.  
4. Genel sekmesine tıklayın.
5. Tarih alanına bir tarih girin.
6. Hurda yordamı alanında 'Tahsisat' seçeneğini işaretleyin.
    * Tahsisat yöntemini seçtiğinizde, hurda malzeme maliyetleri mamullere eklenir.  
7. Tamam'a tıklayın.

## <a name="validate-calculation-results"></a>Hesaplama sonuçlarını doğrulayın
1. Eylem Bölmesi'nde, Maliyetleri yönet'e tıklayın.
2. Maliyet karşılaştırmasını görüntüle'ye tıklayın.
    * Üretim emrini sona erdirdikten sonra, üretim farklarının genel bir bakış elde etmek için, tahmini maliyet fiyatını, gerçekleşmiş maliyet fiyatı ile karşılaştırabilirsiniz.  
