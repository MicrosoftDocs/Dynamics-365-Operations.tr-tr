---
title: Süreç otomasyonu
description: Bu makalede, işlem otomasyonunun toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya nasıl olanak tanıdığı açıklanmaktadır.
author: RyanCCarlson2
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 1a1d152a01e0ebe6a20e2e6b31f12ed7b8deb024
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423972"
---
# <a name="process-automation"></a>İşlem otomasyonu

[!include[banner](../includes/banner.md)]

İşlem otomasyonu, toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya izin verir. Zamanlanan işin güncelleştirilmiş takvim görünümü, son kullanıcıların zamanlanmış ve tamamlanmış işleri görüntülemesine ve üzerlerinde işlem yapmasına olanak tanır.

## <a name="administration"></a>Yönetim

Tüm işlem otomasyonlarının merkezi yönetim sayfası, **Kurulum** menüsünün altında Sistem Yönetimi modülünde bulunur. Bu sayfa, sistemde ayarlanan tüm otomatik işlemleri (serileri) listeler. Bu sayfa, ayrıca, doğrudan bu sayfadan yeni işlem otomasyonları eklemenize olanak tanır. Bir seri ayarladıktan sonra, bu listeden her bir seriyi yönetebilirsiniz. Tüm seriyi düzenlemeyi, silmeyi veya tüm oluşumları liste görünümünde görüntülemeyi ya da zamanlanan işi bir süre duraklatmak istiyorsanız seriyi devre dışı bırakmayı seçebilirsiniz. 

Ortamınızda çalışan tüm arka plan işlemlerini yönetmek için bu sayfadaki **Arka plan işlemleri** sekmesini kullanın. Herhangi bir arka plan işleminde zamanlama değişikliği yapmak için **Düzenle**'yi seçin. Bu değişiklikler, işlemin "uykuya geçmesine" veya her gün belirli bir dönem için çalışmayı duraklatmasına neden olacak bir uyku süresi dönemi içerebilir. Her bir arka plan işlemi için yürütme sonuçlarını görüntülemek amacıyla **En son sonuçları görüntüle**'yi seçin.

Özellik yönetiminde devre dışı bırakılan tüm işlemler, özellik devre dışı bırakıldığında gösterilmez. Ek olarak, süreç otomasyonu zamanlama altyapısı devre dışı bırakılan bir özellik için herhangi bir oluşum veya arka plan işlemi zamanlamaz. Özelliğin yeniden etkinleştirilmesi, geçmişte zamanlanmış oluşumların veya arka plan işlemlerinin hemen çalışmasına neden olur. İşlem otomasyonu planlama altyapısı,**İşlem otomasyonu yoklama sistem işi** sistem toplu işinin çalışmasına dayanır. İş, herhangi bir anda değiştirilmemelidir veya üzerinde değişiklik yapılmamalıdır. Bu toplu iş çalışmıyor veya hata durumundaysa, toplu işi sıfırlamak için **İşlem otomasyonunu başlat**'ı seçin. Bu sıfırlama, uygulamanın daha yeni bir sürümünde yayınlanan tüm yeni değerlerin başlatılmasını sağlar. 

## <a name="calendar-view"></a>Takvim görünümü

İşlem otomasyonunun önemli yararlarından biri, zamanlanmış işi basit bir takvim görünümünde görme yeteneğidir.  Bu görünüm bir seferde bir haftalık çalışmayı görmenizi sağlar. Bu görünümü **Süreç otomasyonu** sayfasının sağ tarafında görürsünüz. Görünüm, seçili seriler için zamanlanan işle doldurulur. 

[![Süreç otomasyonu takvimi.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Oluşum değişiklikleri

Her oluşum, kendilerinden çıkan serilerin tanımladığı diğer oluşumları etkilemeden değiştirilebilir. Zamanlanan işin oluşumları takvim görünümünden **Görüntüle/Düzenle** düğmesi ve **Oluşum** seçilerek düzenlenebilir. Bu sayfa, ilk başta seri kurulum sihirbazında gösterilen tüm ayarlara erişmenizi sağlar ve seçili oluşumda tek başına bir değişiklik yapma yeteneğini sağlar. Zamanlanan işin bir oluşumu, takvim görünümünden **Devre dışı bırak** düğmesi seçilerek de kapatılabilir.

## <a name="developer-documentation"></a>Geliştirici belgesi

Süreç otomasyonu altyapısı geliştiricilerin süreç otomasyonu altyapısını genişletmesine olanak tanır. [Süreç otomasyonu altyapısı](../process-automation/process-automation-framework.md) belgeleri, işlem otomasyonu sihirbazıyla zamanlanmış toplu iş sunucusu tarafından çalıştırılmasını ve takvim görünümünde otomatik olarak gösterilmesini istediğiniz özel işlemleri nasıl oluşturacağınız hakkında bilgiler sağlayacak.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
