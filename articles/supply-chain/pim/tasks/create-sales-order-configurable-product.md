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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e69fd2aa04a65d64db4d34f1839a01fb0f8e018
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213205"
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

