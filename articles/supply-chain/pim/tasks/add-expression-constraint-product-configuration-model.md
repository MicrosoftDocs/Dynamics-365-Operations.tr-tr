---
title: Ürün yapılandırma modeline bir ifade kısıtlaması ekleme
description: Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859c25fd361063d4c5a8544c4b488adfab4238e6cc079fa96efe1c71777779e9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730334"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Ürün yapılandırma modeline bir ifade kısıtlaması ekleme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir. Kullanıcı ön ızgarayı metal olarak seçtiyse bir hoparlöre köşe koruması uygulanması gerektiğini nasıl zorunlu kılacağınızı gösterir. Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.

## <a name="create-an-expression-constraint"></a>Bir ifade kısıtlaması oluşturma

1. **Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
3. Listede, istenen kaydı bulun ve seçin.
    * Bu örnek, son teknoloji hoparlör modeli kullanır.  
4. Listeden, seçilen satırdaki bağlantıyı seçin.
5. **Sınırlamalar** bölümünü genişletin.
6. **Ekle**'yi seçin.
7. **Oluştur**'u seçin.
8. **Ad** alanına bir değer yazın.

## <a name="enter-expression"></a>İfade girin

1. **İfadeyi Düzenle**'yi seçin.
    * Bu aşamada görev kaydında kullanıcı arabiriminin kilidini açarsanız, kısıtlama ifadesi oluşturmak için IntelliSense'i ve simgeler listesini kullanabilirsiniz.  
2. **ConstraintBody** alanında, 'Implies[FrontGrill=="Metal", CornerProtection] ' değerini girin.
    * Bu ifade mantığı şu anlamdadır: Ön ızgara metalse, köşe koruma seçeneği seçili olmalıdır.  
3. **Doğrula**'yı seçin.
    * Doğrulama işlevi, kısıtlama ifadesini gözden geçirir ve sözdizimi hatalarını denetler.  
4. **Kapat**'ı seçin.
5. **Tamam**'ı seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]