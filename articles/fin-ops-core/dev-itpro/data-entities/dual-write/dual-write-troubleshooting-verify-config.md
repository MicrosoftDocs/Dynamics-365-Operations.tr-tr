---
title: Finance and Operations uygulamalarında ve Dataverse'te çift yazma yapılandırmasını doğrulama
description: Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Dataverse'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1f82705f3d8bc11eacbc13d32c14ad1765dcc559
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782639"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Finance and Operations uygulamalarında ve Dataverse'te çift yazma yapılandırmasını doğrulama

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Dataverse'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Çift yazmanın Finance and Operations uygulamalarında yapılandırıldığını denetleme

Güncelleştirme için satırları kaydetmeye çalıştığınızda gördüğünüz hataların çift yazma işleminden kaynaklanıp kaynaklanmadığını belirlemek için, önce çift yazma işleminin yapılandırıldığından emin olun.

+ Finance and Operations uygulamada yönetici ayrıcalıklarınız varsa **çalışma alanları \>veri yönetimi**'ne gidin ve **çift-yazılır** döşemeyi seçin. Bağlı ortamların ayrıntıları ve çalışmakta olan tablo eşlemeleri listesi gösteriliyorsa çift yazma hizmeti yapılandırılmıştır.

    ![Yönetici ayrıcalıklarınız olduğunda Finance and Operations uygulama bağlantısı doğrulanıyor.](media/verify_fin_ops_1.png)

+ Yönetici ayrıcalıklarınız yoksa, *\<entity name\> varlığına veri yazılamıyor* hata iletisi alırsınız. Aşağıdaki çizimde yer alan örnekte, çift yazma yapılandırılmış olmasına rağmen müşteri grubu ve ödeme koşulları başvuru verileri Dataverse'te bulunmadığından Finance and Operations uygulamasında müşteri satırı oluşturamazsınız.

    ![Yönetici ayrıcalıklarınız olmadığında Finance and Operations uygulama bağlantısı doğrulanıyor.](media/verify_fin_ops_2.png)

Finance and Operations Uygulamalarda veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Çift yazmanın Dataverse'ta yapılandırıldığını denetleme

Veri oluşturduğunuzda, Dataverse içindeki sayfalarda **Şirket** sütununu görüyorsanız çift yazma özelliği yapılandırılmıştır.

![Dataverse bağlantı doğrulanıyor.](media/verify_cds.png)

Dataverse'te veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).

Hata ayrıntılarının nasıl görüntüleneceği hakkında bilgi için Dataverse'de veri oluştururken herhangi bir hatayla karşılaşırsanız, bkz. [Hata ayrıntılarını görüntülemek için Dataverse'te eklenti izleme günlüklerini etkinleştirin ve görüntüleyin](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]