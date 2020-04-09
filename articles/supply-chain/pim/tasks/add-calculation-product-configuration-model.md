---
title: Ürün yapılandırma modeline hesaplama ekleme
description: Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f8fcfdafb2d5fb5a4d4800221fabf4b2111f86
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150275"
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

