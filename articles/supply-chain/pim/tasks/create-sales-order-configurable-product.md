---
title: Yapılandırılabilir ürün için satış siparişi oluşturma
description: Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570597"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Yapılandırılabilir ürün için satış siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir. Bu örnek, USMF demo veri şirketindeki D0006 hoparlör modelini kullanır. Genel olarak bu yordamı bir satış siparişi işlemcisi kullanır.

## <a name="create-a-sales-order"></a>Satış siparişi oluştur

1. **Satış ve pazarlama \> Çalışma alanları \> Satış siparişi işleme ve sorgulama**'ya gidin.
1. **Yeni**'yi seçin.
1. **Satış siparişi**'ni seçin.
1. **Müşteri hesabı** alanında *US-001*'ü seçin. 
1. **Tamam**'ı seçin.
1. **Öğe numarası** alanında, *D0006*'yi seçin.
    * Bu görev için yapılandırılabilir bir ürün seçmelisiniz.  
1. **Ürün ve tedarik**'i seçin.
1. **Satırı yapılandır**'ı seçin.
    * Fiyatın seçilen yapılandırmaya göre değiştiğini ve **Kabloyu dahil et** alanının şimdi *Doğru* olarak ayarlandığını unutmayın.  
    * Kablo için seçilen varsayılan fiyatı ve ayarları not alın.  
1. **Şablon yükle**'yi seçin.
    * Bu örnek, önceden tanımlanmış bir yapılandırmayı seçmek için bir şablonu nasıl uygulayabileceğinizi gösterir. Bu yordamı bir görev kılavuzu olarak kullanıyorsanız ve kullanılabilir diğer öznitelik değerlerini görmek istiyorsanız **Kilidi aç** düğmesini seçin.  
1. **Tamam**'ı seçin.
1. **Tamam**'ı seçin.
1. **Satır ayrıntıları** bölümünü genişletin.
1. **Ürün** sekmesini seçin.
    * Madde yapılandırılması artık ürün boyutları altında listelenir.  
1. Sayfayı kapatın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]