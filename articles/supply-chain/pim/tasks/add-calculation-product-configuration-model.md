---
title: Ürün yapılandırma modeline hesaplama ekleme
description: Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb753878a3ce8c29e2a7e7e90e1d6cf6d56c0358d16e3173253ae729cb123502
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731829"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Ürün yapılandırma modeline hesaplama ekleme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir. Beyaz hoparlörler için hoparlör yüksekliğini 10 ve diğer dolaplar için 15 olarak ayarlamak için "If" işlecini kullanarak bir mantıksal ifadeyi nasıl oluşturabileceğinizi gösterir. Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.


## <a name="add-a-calculation"></a>Hesaplama ekleme

## <a name="create-calculation-expression"></a>Hesaplama ifadesi oluşturma
1. İfadeyi düzenle'yi tıklatın.
2. ConstraintBody alanında, 'If[CabinetFinish=="White", 10, 15]' değerini girin.
3. Doğrula'ya tıklayın.
4. Kapat’a tıklayın.
5. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]