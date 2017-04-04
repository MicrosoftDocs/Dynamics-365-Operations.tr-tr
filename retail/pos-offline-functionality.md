---
title: "POS çevrimdışı işlevsellik"
description: "Bu makalede, Perakende Modern POS için çevrimdışı mod hakkında bilgiler verilmektedir. Bu modda perakende sunucusu kullanılamadığı zaman, POS cihazları kanal veritabanından çevrimdışı veritabanına otomatik olarak geçiş yapar. Bu makalede çevrimdışı mod genel kurulum bilgileri yer almaktadır ve çevrimdışı veritabanıyla kanal veritabanı arasındaki veri eşitleme açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>POS çevrimdışı işlevsellik

Bu makalede, Perakende Modern POS için çevrimdışı mod hakkında bilgiler verilmektedir. Bu modda perakende sunucusu kullanılamadığı zaman, POS cihazları kanal veritabanından çevrimdışı veritabanına otomatik olarak geçiş yapar. Bu makalede çevrimdışı mod genel kurulum bilgileri yer almaktadır ve çevrimdışı veritabanıyla kanal veritabanı arasındaki veri eşitleme açıklanmaktadır.

<a name="overview"></a>Özet
--------

Perakende sunucu kullanılamaz olduğunda perakende Modern POS, satış (POS) aygıtı noktası çevrimdışı moduna geçer. Bu nedenle, perakende sunucusuyla bağlantı kaybolursa, Modern POS perakende çevrimdışı veritabanına otomatik olarak geçer. Bir satış hareketi sırasında çevrimdışı profilinde yapılandırılmış zaman aşımı aralığı içinde veri isteği başarısız olursa, Perakende Modern POS perakende otomatik olarak çevrimdışı veritabanına geçiş yapar ve satış hareketi devam eder. POS aygıt çevrimdışı moddayken, Perakende Modern POS çevrimdışı profilde yapılandırılmış olan yeniden bağlanma girişimi aralığından sonra perakende sunucusuna yeniden bağlanmaya çalışır. Bu yeniden bağlanma denemesi yalnızca bir hareketin başlangıcında gerçekleşir.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Perakende Modern POS'un bağlantı modunu belirleme

Perakende Modern POS'taki durum başlığı, geçerli bağlantı durumunu gösterir ve **Bağlantı durumu** penceresi çevrimdışı veritabanıyla son eşitleme girişiminin durumunu gösterir. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Çevrimdışı ve çevrimiçi modları arasında el ile geçiş yapmak için bir düğme oluşturma

Perakende Modern POS'a çevrimiçi ve çevrimdışı modlar arasında el ile geçiş yapmak için bir düğme ekleyebilirsiniz. POS işlemi için bir düğme oluşturun **917 – Veritabanı bağlantı durumu**. Bu düğmenin adı Perakende Modern POS perakende sunucusuna bağlı olduğunda **Bağlantıyı kes** ve bağlantı kesildiğinde **Bağlan**'dır. Bu düğmeyi bağlantıyı görüntülemek ve perakende sunucusuyla bağlantıyı kesmek veya sunucuya bağlanmak için kullanabilirsiniz. [![Modern POS perakende düğmesini kesmek](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Ayar
POS aygıtının (register) çevrimdışı desteğini etkinleştirmek için set **Çevrimdışı Destek** için seçenek **Evet** üzerinde **kayıt** sayfa. Yeni bir kanal veritabanı varlık oluşturulur ve mağazanın kanal veri grubuna eklenir. Daha sonra çevrimdışı veritabanı veri paketleri oluşturmak için tüm gerekli dağıtım zamanlamalarını çalıştırın. Daha sonra çevrimdışı Modern POS perakende sürümünü yükleyin. Yükleme işlemi çevrimdışı veritabanı oluşturur. Ayrıca, gerekirse Microsoft SQL Server Express 2014 yükleyin. Çevrimdışı veri eşitleme Perakende Modern POS'a ilk oturum açıldıktan sonra başlar.

## <a name="data-synchronization"></a>Veri eşitleme
Perakende Planlayıcısı ana verileri çevrimdışı veritabanına göndermek için kullanılır. Varsayılan olarak, dağıtım zamanlamasını çalıştırdığınızda kanalı veritabanı ve çevrimdışı veritabanına veri değişiklikleri gönderilir. Perakende Modern POS tüm kullanılabilir veri paketlerini yükleyen ve bunları çevrimdışı veritabanına ekleyen zaman uyumsuz eşitleme kitaplığını içerir. İşlemler çevrimdışı oluşturulursa, Perakende Modern POS onları kanal veritabanına eklenebilmeleri için perakende sunucusuna yükler. Çevrimdışı veri eşitleme, yalnızca Perakende Modern POS çalışıyorsa oluşabilir. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


