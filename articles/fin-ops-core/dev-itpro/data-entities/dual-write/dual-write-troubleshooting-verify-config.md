---
title: Finans ve operasyon uygulamaları ve Dataverse'teki çift yazma yapılandırmasını doğrulama
description: Bu makalede, çift yazmanın finans ve operasyon uygulamalarında ve Dataverse'te yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğiniz açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289405"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Finans ve operasyon uygulamaları ve Dataverse'teki çift yazma yapılandırmasını doğrulama

[!include [banner](../../includes/banner.md)]





Bu makalede, finans ve operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında sorun giderme bilgileri sağlanmaktadır. Bu konu, Çift yazma'nın finans ve operasyon uygulamalarında ve Dataverse'te yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Finans ve operasyon uygulamasında çift yazma özelliğinin yapılandırıldığını doğrulama

Güncelleştirme için satırları kaydetmeye çalıştığınızda gördüğünüz hataların çift yazma işleminden kaynaklanıp kaynaklanmadığını belirlemek için, önce çift yazma işleminin yapılandırıldığından emin olun.

+ Finans ve operasyon uygulamasında yönetici ayrıcalıklarınız varsa **Çalışma alanları \> Veri yönetimi**'ne gidin ve **Çift Yazma** kutucuğunu seçin. Bağlı ortamların ayrıntıları ve çalışmakta olan tablo eşlemeleri listesi gösteriliyorsa çift yazma hizmeti yapılandırılmıştır.

    ![Yönetici ayrıcalıklarınız olduğunda finans ve operasyon uygulama bağlantısı doğrulanır.](media/verify_fin_ops_1.png)

+ Yönetici ayrıcalıklarınız yoksa, *\<entity name\> varlığına veri yazılamıyor* hata iletisi alırsınız. Aşağıdaki çizimde yer alan örnekte, çift yazma yapılandırılmış olmasına rağmen müşteri grubu ve ödeme koşulları referans verileri Dataverse'te bulunmadığından finans ve operasyon uygulamasında müşteri satırı oluşturamazsınız.

    ![Yönetici ayrıcalıklarınız olmadığında finans ve operasyon uygulama bağlantısı doğrulanır.](media/verify_fin_ops_2.png)

Finans ve operasyon uygulamalarında veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için bkz. [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Çift yazmanın Dataverse'ta yapılandırıldığını denetleme

Veri oluşturduğunuzda, Dataverse içindeki sayfalarda **Şirket** sütununu görüyorsanız çift yazma özelliği yapılandırılmıştır.

![Dataverse bağlantı doğrulanıyor.](media/verify_cds.png)

Dataverse'te veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için bkz. [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).

Hata ayrıntılarının nasıl görüntüleneceği hakkında bilgi için Dataverse'de veri oluştururken herhangi bir hatayla karşılaşırsanız, bkz. [Hata ayrıntılarını görüntülemek için Dataverse'te eklenti izleme günlüklerini etkinleştirin ve görüntüleyin](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
