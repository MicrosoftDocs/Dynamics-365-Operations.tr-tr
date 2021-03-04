---
title: Yapılandırılabilir ürün için satış siparişi oluşturma
description: Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 988d87757019d20dcaf675af925166ed376685f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439290"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Yapılandırılabilir ürün için satış siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir. Bu örnek, USMF demo veri şirketindeki D0006 hoparlör modelini kullanır. Genel olarak bu yordamı bir satış siparişi işlemcisi kullanır.


## <a name="create-a-sales-order"></a>Satış siparişi oluştur
1. Satış siparişi işleme ve sorgulama'ya tıklayın.
2. Yeni'ye tıklayın.
3. Satış siparişi'ne tıklayın.
4. Müşteri hesabı alanında US-001'i seçin. 
5. Tamam'a tıklayın.
6. Madde numarası alanında D0006 seçin.
    * Bu görev için yapılandırılabilir bir ürün seçmelisiniz.  
7. Ürün ve tedarik seçeneğine tıklayın.
8. Yapılandırma satırı'na tıklayın.
    * Fiyatın seçilen yapılandırmaya göre değiştiğini ve Kabloyu dahil et alanının şimdi Doğru olarak ayarlandığını unutmayın.  
    * Kablo için seçilen varsayılan fiyatı ve ayarları not alın.  
9. Şablonu yükle'ye tıklayın.
    * Bu örnek, önceden tanımlanmış bir yapılandırmayı seçmek için bir şablonu nasıl uygulayabileceğinizi gösterir. Bu yordamı bir görev kılavuzu olarak kullanıyorsanız ve kullanılabilir diğer öznitelik değerlerini görmek istiyorsanız Kilidi aç düğmesine tıklamalısınız.  
10. Tamam'a tıklayın.
11. Tamam'a tıklayın.
12. Satır ayrıntıları bölümünü genişletin.
13. Ürün sekmesine tıklayın.
    * Madde yapılandırılması artık ürün boyutları altında listelenir.  
14. Sayfayı kapatın.

## <a name="select-the-product-configuration"></a>Ürün yapılandırmasını seçme



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]