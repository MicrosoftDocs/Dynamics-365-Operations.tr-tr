---
title: Çift yazmanın Finance and Operations uygulamalarında ve Common Data Service'ta yapılandırıldığını denetleme
description: Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Common Data Service'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997242"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Çift yazmanın Finance and Operations uygulamalarında ve Common Data Service'ta yapılandırıldığını denetleme

[!include [banner](../../includes/banner.md)]



Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Common Data Service'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Çift yazmanın Finance and Operations uygulamalarında yapılandırıldığını denetleme

Güncelleştirme için kayıtları kaydetmeye çalıştığınızda gördüğünüz hataların çift dosyadan gelip gelmediğini belirlemek için, önce çift Yazımın konfigüre edilmiş olduğunu doğrulayın.

+ Finance and Operations uygulamada yönetici ayrıcalıklarınız varsa **çalışma alanları \>veri yönetimi** 'ne gidin ve **çift-yazılır** döşemeyi seçin. Bağlı ortamların ayrıntıları ve çalışmakta olan varlık haritaları listesi gösteriliyorsa, çift yazım yapılandırılır.

    ![Yönetici ayrıcalıklarınız olduğunda Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_1.png)

+ Yönetici ayrıcalıklarınız yoksa, *\<entity name\> varlığına veri yazılamıyor* hata iletisi alırsınız. Aşağıdaki çizimde yer alarak, Çift yazılı konfigüre edilmiş, ancak müşteri grubu ve ödeme koşulları referans verileri Common Data Service' nde bulunmadığından, Finance and Operations uygulamada müşteri kaydı oluşturamazsınız.

    ![Yönetici ayrıcalıklarınız olmadığında Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_2.png)

Finance and Operations Uygulamalarda veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Çift yazmanın Common Data Service'ta yapılandırıldığını denetleme

Veri oluşturduğunuzda, Common Data Service içindeki sayfalarda **Şirket** alanını görüyorsanız, Çift-yazılır olarak yapılandırılır.

![Common Data Service bağlantı doğrulanıyor](media/verify_cds.png)

Common Data Service'te veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).

Hata ayrıntılarının nasıl görüntüleneceği hakkında bilgi için Common Data Service'de veri oluştururken herhangi bir hatayla karşılaşırsanız, bkz. [Hata ayrıntılarını görüntülemek için Common Data Service'te eklenti izleme günlüklerini etkinleştirin ve görüntüleyin](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
