---
title: Ürün yapılandırma modeline bir ifade kısıtlaması ekleme
description: Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43d7f768069c5ef201a2823a9aa626b38220073
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439312"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Ürün yapılandırma modeline bir ifade kısıtlaması ekleme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir. Kullanıcı ön ızgarayı metal olarak seçtiyse bir hoparlöre köşe koruması uygulanması gerektiğini nasıl zorunlu kılacağınızı gösterir. Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.


## <a name="create-an-expression-constraint"></a>Bir ifade kısıtlaması oluşturma
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
    * Bu örnek, son teknoloji hoparlör modeli kullanır.  
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Sınırlamalar bölümünü genişletin.
6. Ekle öğesini tıklatın.
7. Oluştur'a tıklayın.
8. İsim alanına bir değer yazın.

## <a name="enter-expression"></a>İfade girin
1. İfadeyi düzenle'yi tıklatın.
    * Bu aşamada görev kaydında kullanıcı arabiriminin kilidini açarsanız, kısıtlama ifadesi oluşturmak için IntelliSense'i ve simgeler listesini kullanabilirsiniz.  
2. ConstraintBody alanında, 'Implies[FrontGrill=="Metal", CornerProtection] ' değerini girin.
    * Bu ifade mantığı şu anlamdadır: Ön ızgara metalse, köşe koruma seçeneği seçili olmalıdır.  
3. Doğrula'ya tıklayın.
    * Doğrulama işlevi, kısıtlama ifadesini gözden geçirir ve sözdizimi hatalarını denetler.  
4. Kapat’a tıklayın.
5. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]