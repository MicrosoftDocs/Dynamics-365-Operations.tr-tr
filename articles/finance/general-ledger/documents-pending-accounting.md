---
title: Muhasebe bekleyen belgeler
description: Bu makalede, Muhasebe bekleyen belgeler sayfasındaki işlevler açıklanmaktadır.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f37d46659b2fc5bf9933719811a7b90cc4e80f52
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709264"
---
# <a name="documents-pending-accounting"></a>Muhasebe bekleyen belgeler

[!include [banner](../includes/banner.md)]

Bu makalede, **Muhasebe bekleyen belgeler** sayfasındaki işlevler açıklanmaktadır.

Microsoft Dynamics 365 Finance 10.0.30 sürümünde **Kaynak belge muhasebe altyapısı için geliştirilmiş performans** özelliği bulunur. Bu özellik, serbest metin faturalarının deftere nakil işleminden başlayarak kaynak belge destekli belge deftere nakilleri için deftere nakil işlemlerini iyileştirir.

Bu özellik etkinleştirildiğinde yardımcı defter belgelerinin deftere nakil işlemi, genel kayıt defterine nakledilen eksiksiz muhasebe ayrıntıları oluşturan muhasebe oluşturma veya *günlüğe kaydetme* işleminden ayrı olarak gerçekleştirilir. Örneğin serbest metin fatura deftere nakli işleminde, **Alacak hesapları** modülündeki müşteri faturası, eksiksiz muhasebe oluşturulmadan önce kaydedilir. Bu iyileştirilmiş performans özelliği, muhasebe oluşturmayı geciktirirken müşteri faturalarının daha hızlı kaydedilmesine olanak tanır.

**Muhasebe bekleyen belgeler** sayfasında aşağıdaki düğmeler bulunur.

- **Muhasebe oluştur** – Deftere kayıt için halihazırda muhasebe oluşturma bekleyen bir belgeyi gönderir.
- **Dağıtımları görüntüle** – Listedeki seçili belge için muhasebe dağıtımlarını görüntüler.
- **Hata günlüğünü görüntüle** – Muhasebe durumunun hata belirttiği belgelerle ilgili hata iletisi ayrıntılarını görüntüler. Aynı hata iletisi ayrıntılarını, belge satırında **Hata günlüğü** bağlantısını seçerek de görüntüleyebilirsiniz.

Muhasebe oluşturma işlemi, **Muhasebe çerçeve işlemcisi** adlı bir işlem otomasyonu arka plan işlemi tarafından gerçekleştirilir. Kurulum ve tüm işlem otomasyonları hakkında daha fazla bilgi için bkz. [İşlem otomasyonu](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
