---
title: ISO20022 alacak transferi yapılandırmasını içe aktarma
description: Bu yordam, satıcı ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140053"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>ISO20022 alacak transferi yapılandırmasını içe aktarma

[!include [banner](../../includes/banner.md)]

Bu yordam, satıcı ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir. Örnek olarak Alman ISO 20022 alacak transfer biçimi kullanılır. Bu yordam diğer mevcut elektronik raporlama biçimleri için kullanılabilir. 

Bu görev, demo veri şirketi DEMF kullanılarak oluşturulmuştur ancak bu görevi tamamlamak için herhangi bir demo veri şirketini kullanabilirsiniz.

Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş görevin birincisidir. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Kullanılabilir yapılandırma sağlayıcıları listesinden Microsoft'u seçin.
3. Etkin olarak ayarla'ya tıklayın.
4. Depolar'a tıklayın.
5. Aç'a tıklayın.
6. Filtreleri göster'e tıklayın.
7. Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Yapılandırma adı" alanında "ISO20022 Alacak Transferi (DE)" için bir filtre değeri girin
    * Alternatif olarak listede yapılandırmayı bulup seçin ve ardından İçe Aktar görevine taşıyın.  
8. İçe aktar'ı tıklatın.
    * İçe Aktar düğmesi kullanılamıyorsa yapılandırma zaten içe aktarılmış demektir.  
9. Evet'i tıklatın.

