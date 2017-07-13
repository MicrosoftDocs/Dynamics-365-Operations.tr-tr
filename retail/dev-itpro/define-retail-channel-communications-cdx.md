---
title: "Perakende kanal iletişimlerini (Ticaret Veri Değişimi) tanımlayın"
description: "Bu makalede, Commerce Data Exchange ve bileşenleri hakkında genel bir bakış verilmektedir. Makalede, her bileşenin, Microsoft Dynamics 365 for Retail ve perakende kanalları arasında veri aktarımını oynadığı rol açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: tr-tr
ms.lasthandoff: 06/20/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Perakende kanal iletişimlerini (Ticaret Veri Değişimi) tanımlayın

[!include[banner](../includes/banner.md)]


Bu makalede, Commerce Data Exchange ve bileşenleri hakkında genel bir bakış verilmektedir. Makalede, her bileşenin, Microsoft Dynamics 365 for Retail ve perakende kanalları arasında veri aktarımını oynadığı rol açıklanmaktadır.

<a name="overview"></a>Özet
--------

Ticaret veri değişimi, çevrimiçi mağazalar ve fiziksel mağazalar gibi Dynamics 365 for Retail ve perakende kanalları arasında veri aktarımı sağlayan bir sistemdir. Perakende kanal için verileri depolayan veritabanı, Dynamics 365 for Retail veritabanından ayrıdır. Kanal veritabanı yalnızca perakende hareketleri için gerekli olan verileri tutar. Ana veriler Dynamics 365 for Retail'da yapılandırılır ve kanallara dağıtılır. İşlemsel veri satış noktası (POS) sisteminde veya çevrimiçi mağazada oluşturulur ve sonra Dynamics 365 for Retail'a yüklenir. Veri dağıtımı zaman uyumsuzdur. Diğer bir deyişle, kaynakta toplama ve veri paketleme işlemi hedef konumda veri alma ve uygulama işleminden ayrı olarak gerçekleşir. Fiyat ve stok aramalar gibi bazı senaryolar için gerçek zamanlı veri alınması gerekir. Bu senaryoları desteklemek için, Commerce Data Exchange ayrıca Dynamics 365 for Retail ile bir kanal arasında gerçek zamanlı iletişim sağlayan bir hizmet içerir. 

[![güncelleştirilmiş-perakende-grafik](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Hizmeti
Dynamics 365 for Retail veritabanındaki Microsoft SQL Server değişiklik izleme kanala gönderilmesi gereken veri değişikliklerini belirlemek için kullanılır. Bir dağıtım zamanlamasına göre, Dynamics 365 for Retail, bu veriyi paketler ve merkezi depolamaya (Azure blob depolama birimi) kaydeder. Ayrı bir toplu işlem bu veri paketini kanal veritabanına eklemek için Commerce Data Exchange Async Client kitaplığını kullanır. 

[![Async Hizmeti](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Perakende planlayıcısı

Planlayıcı işler verileri yerleşimlere/yerleşimlerden dağıtmanız için olan mekanizmadır. İşler dağıtılacak veriyi içeren tablolar ve tablo alanlarını belirleyen alt işlerden oluşur. Dynamics 365 for Retail, çoğu kuruluşun çoğaltma gereksinimlerini karşılayan önceden tanımlanmış zamanlayıcı işleri ve alt işleri içerir. Aşağıdaki önceden tanımlanmış iş türleri oluşturulur:

-   **Karşıdan işleri yükleme** – Karşıdan işleri yükleme, Dynamics 365 for Retail'dan kanal veritabanlarına değiştirilen verileri gönderir. Kayıtlardaki değişiklikler izlenen SQL Server değişiklik izleme ile takip edilir.
-   **İşleri (P işleri) karşıya yükleme** – İşleri karşıya yükleme, bir kanaldaki satış hareketlerini Dynamics 365 for Retail veritabanına çeker. P işleri verileri artımlı olarak yükler. Bir P işi çalıştığında, Async Client kitaplığı bir konumdan alınmış olan kayıtlar için yineleme sayacını denetler. Bir kayıt yalnızca yineleme sayacı bulunan en büyük değerden fazla olduğunda yüklenir. P işleri önceden yüklenen verileri güncelleştirmez.

Dağıtım zamanlaması veri transferini ya el ile ya da Dynamics 365 for Retail bir toplu iş planlayarak çalıştırmak için kullanılır. Bir dağıtım planı bir veya daha fazla kanal veri grubu ve bir veya daha fazla zamanlayıcı iş içerebilir.

## <a name="realtime-service"></a>Gerçek zamanlı servis
Commerce Data Exchange: Real-time Service, Dynamics 365 for Retail ve perakende kanalları arasında gerçek zamanlı iletişim sağlayan tümleşik bir hizmettir. Gerçek zamanlı hizmet ayrı ayrı POS bilgisayarların ve çevrimiçi mağazaların Dynamics 365 for Retail'dan belirli verileri gerçek zamanlı olarak almasını sağlar. Çoğu anahtar işlemler yerel kanal veritabanında gerçekleştirilebilir olsa da, aşağıdaki senaryolarda Dynamics 365 for Detail'dan uygulamasında saklanan verilere doğrudan erişimi gerektirir:

-   Hediye kartları vermek ve kullanmak.
-   Bağlılık puanlarını kullanmak.
-   Alacak makbuzları vermek ve kullanmak.
-   Müşteri kayıtları oluşturmak ve güncelleştirmek.
-   Satış siparişleri oluşturmak, güncelleştirmek ve tamamlamak.
-   Bir satınalma siparişi veya transfer emrine karşı stok almak.
-   Stok sayımları gerçekleştirmek.
-   Mağazalardan satış hareketleri almak ve iade hareketlerini tamamlamak.

[![Gerçek zamanlı servis](./media/rts.png)](./media/rts.png) 

Gerçek zamanlı servis, önceden tanımlanmış bir gerçek zamanlı hizmet profili oluşturulur.




