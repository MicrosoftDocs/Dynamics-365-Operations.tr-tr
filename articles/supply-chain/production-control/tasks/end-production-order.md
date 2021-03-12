---
title: Üretim emrini bitirme
description: Bu yordam, bir üretim emrini nasıl sonlandırabileceğinizi gösterir.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f3e121fdc0f69ace15e0fa08bde0af739ef7d28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977825"
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
