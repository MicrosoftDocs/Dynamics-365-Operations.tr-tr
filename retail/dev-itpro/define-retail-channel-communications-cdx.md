---
title: "Perakende kanal iletişimlerini (Ticaret Veri Değişimi) tanımlayın"
description: "Bu makalede, Commerce Data Exchange ve bileşenleri hakkında genel bir bakış verilmektedir. Her bileşen Microsoft Dynamics 365 işlemleri için perakende kanalları arasındaki veri aktarımını oynadığı bölümü açıklar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Perakende kanal iletişimlerini (Ticaret Veri Değişimi) tanımlayın

Bu makalede, Commerce Data Exchange ve bileşenleri hakkında genel bir bakış verilmektedir. Her bileşen Microsoft Dynamics 365 işlemleri için perakende kanalları arasındaki veri aktarımını oynadığı bölümü açıklar.

<a name="overview"></a>Özet
--------

Ticaret veri değişimi işlemleri için Dynamics 365 ve çevrimiçi mağazalarda veya Tuğla Dibek depoları gibi perakende kanalları arasında veri aktarır bir sistemdir. Perakende kanal verilerini depolayan veritabanı işlemleri veritabanı için Dynamics 365 ayrıdır. Kanal veritabanı yalnızca perakende hareketleri için gerekli olan verileri tutar. Ana veri Dynamics 365 işlemleri için yapılandırılmış ve kanallar için Dağıtılmış. İşlemsel veri noktası (POS) satış sistemi oluşturulur veya çevrimiçi depolayabilir ve sonra Dynamics 365 işlemleri için karşıya. Veri dağıtımı zaman uyumsuzdur. Diğer bir deyişle, kaynakta toplama ve veri paketleme işlemi hedef konumda veri alma ve uygulama işleminden ayrı olarak gerçekleşir. Fiyat ve stok aramalar gibi bazı senaryolar için gerçek zamanlı veri alınması gerekir. Bu senaryoları desteklemek için Dynamics 365 işlemleri için bir kanal arasındaki gerçek zamanlı iletişim sağlayan bir hizmet ticaret veri değişimi de içerir. 

[![güncelleştirilmiş-perakende-grafik](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Hizmeti
Microsoft SQL Server Değiştir izleme işlemleri veritabanı için Dynamics 365 kanala gönderilen veri değişiklikleri belirlemek için kullanılır. Bir dağıtım zamanlamaya göre Dynamics 365 işlemleri için veri paketleri ve merkezi depolama (Azure blob depolama birimi) kaydeder. Ayrı bir toplu işlem bu veri paketini kanal veritabanına eklemek için Commerce Data Exchange Async Client kitaplığını kullanır. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Perakende planlayıcısı

Planlayıcı işler verileri yerleşimlere/yerleşimlerden dağıtmanız için olan mekanizmadır. İşler dağıtılacak veriyi içeren tablolar ve tablo alanlarını belirleyen alt işlerden oluşur. Dynamics 365 işlemleri için önceden tanımlanmış zamanlayıcı işleri ve çoğaltma çoğu kuruluşun gereksinimlerini karşılayacak alt işler içerir. Aşağıdaki önceden tanımlanmış iş türleri oluşturulur:

-   **İşleri karşıdan** – yükleme işlemleri için Dynamics 365 gelen kanal veritabanlarına değişti gönderme veri işler. Kayıtlardaki değişiklikler izlenen SQL Server değişiklik izleme ile takip edilir.
-   **İşleri (P işleri) karşıya** – karşıya yükleme işlerini bir kanaldan satış hareketleri veritabanı işlemleri için Dynamics 365 içine çeker. P işleri verileri artımlı olarak yükler. Bir P işi çalıştığında, Async Client kitaplığı bir konumdan alınmış olan kayıtlar için yineleme sayacını denetler. Bir kayıt yalnızca yineleme sayacı bulunan en büyük değerden fazla olduğunda yüklenir. P işleri önceden yüklenen verileri güncelleştirmez.

Dağıtım zamanlamasını el ile veya planlama işlemleri için Dynamics 365 toplu işlemde veri aktarımı çalıştırmak için kullanılır. Bir dağıtım planı bir veya daha fazla kanal veri grubu ve bir veya daha fazla zamanlayıcı iş içerebilir.

## <a name="realtime-service"></a>Gerçek zamanlı hizmet
Ticaret veri değişimi: Gerçek zamanlı hizmet işlemleri için Dynamics 365 ve perakende kanalları arasında gerçek zamanlı iletişim sağlayan tümleşik bir hizmettir. Gerçek zamanlı hizmet POS bilgisayarları ayrı ayrı ve gerçek zamanlı olarak Dynamics 365 işlemler için belirli veri almak için çevrimiçi mağazalar sağlar. Çoğu anahtar işlemleri yerel kanal veritabanında gerçekleştirilen rağmen aşağıdaki senaryolarda Dynamics 365 işlemleri için depolanan verileri doğrudan erişim gerekir:

-   Hediye kartları vermek ve kullanmak.
-   Bağlılık puanlarını kullanmak.
-   Alacak makbuzları vermek ve kullanmak.
-   Müşteri kayıtları oluşturmak ve güncelleştirmek.
-   Satış siparişleri oluşturmak, güncelleştirmek ve tamamlamak.
-   Bir satınalma siparişi veya transfer emrine karşı stok almak.
-   Stok sayımları gerçekleştirmek.
-   Mağazalardan satış hareketleri almak ve iade hareketlerini tamamlamak.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Önceden tanımlanmış bir gerçek zamanlı hizmet profili oluşturulur.


