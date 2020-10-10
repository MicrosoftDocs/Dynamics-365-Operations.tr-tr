---
title: İşlem otomasyonu
description: Bu konu, işlem otomasyonunun toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya nasıl izin verdiğini açıklamaktadır.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: afbef26cb7b37bafb34f12cc20a88fb4aea9f343
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885263"
---
# <a name="process-automation"></a>İşlem otomasyonu

[!include[banner](../includes/banner.md)]

İşlem otomasyonu, toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya izin verir. Zamanlanan işin güncelleştirilmiş takvim görünümü, son kullanıcıların zamanlanmış ve tamamlanmış işleri görüntülemesine ve üzerlerinde işlem yapmasına olanak tanır.

## <a name="administration"></a>Yönetim

Tüm işlem otomasyonlarının merkezi yönetim sayfası, **Kurulum** menüsünün altında Sistem Yönetimi modülünde bulunur. Bu sayfa, sistemde ayarlanan tüm otomatik işlemleri (serileri) listeler. Bu sayfa, ayrıca, doğrudan bu sayfadan yeni işlem otomasyonları eklemenize olanak tanır. Bir seri ayarladıktan sonra, bu listeden her bir seriyi yönetebilirsiniz. Tüm seriyi düzenlemeyi, silmeyi veya tüm oluşumları liste görünümünde görüntülemeyi ya da zamanlanan işi bir süre duraklatmak istiyorsanız seriyi devre dışı bırakmayı seçebilirsiniz. 

Özellik yönetiminde devre dışı bırakılan tüm işlemler, özellik devre dışı bırakıldığında gösterilmez. Ek olarak, süreç otomasyonu zamanlama altyapısı devre dışı bırakılan bir özellik için herhangi bir oluşum veya arka plan işlemi zamanlamaz. Özelliğin yeniden etkinleştirilmesi, geçmişte zamanlanmış oluşumların veya arka plan işlemlerinin hemen çalışmasına neden olur.

## <a name="calendar-view"></a>Takvim görünümü

İşlem otomasyonunun önemli yararlarından biri, zamanlanmış işi basit bir takvim görünümünde görme yeteneğidir.  Bu görünüm bir seferde bir haftalık çalışmayı görmenizi sağlar. Bu görünümü **Süreç otomasyonu** sayfasının sağ tarafında görürsünüz. Görünüm, seçili seriler için zamanlanan işle doldurulur. 

[![İşlem otomasyonu takvimi](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Oluşum değişiklikleri

Her oluşum, kendilerinden çıkan serilerin tanımladığı diğer oluşumları etkilemeden değiştirilebilir. Zamanlanan işin oluşumları takvim görünümünden **Görüntüle/Düzenle** düğmesi ve **Oluşum** seçilerek düzenlenebilir. Bu sayfa, ilk başta seri kurulum sihirbazında gösterilen tüm ayarlara erişmenizi sağlar ve seçili oluşumda tek başına bir değişiklik yapma yeteneğini sağlar. Zamanlanan işin bir oluşumu, takvim görünümünden **Devre dışı bırak** düğmesi seçilerek de kapatılabilir.

## <a name="developer-documentation"></a>Geliştirici belgesi

Süreç otomasyonu altyapısı geliştiricilerin süreç otomasyonu altyapısını genişletmesine olanak tanır. [Süreç otomasyonu altyapısı](../process-automation/process-automation-framework.md) belgeleri, işlem otomasyonu sihirbazıyla zamanlanmış toplu iş sunucusu tarafından çalıştırılmasını ve takvim görünümünde otomatik olarak gösterilmesini istediğiniz özel işlemleri nasıl oluşturacağınız hakkında bilgiler sağlayacak.
