---
title: Çözüm farkındalığıyla ilgili sorunları giderme
description: Bu makalede, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c280eef995664c640e382817dda9d6e1cde154c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871509"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Çözüm farkındalığıyla ilgili sorunları giderme

[!include [banner](../../includes/banner.md)]





Bu makalede, Finans ve Operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında sorun giderme bilgileri sağlanmaktadır. Bu konu, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu makalede ele alınan bazı sorunlar için sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="error-on-the-dual-write-page"></a>Çift-yazma sayfasında hata

**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:

*namemapping='Logical' bulunan, adı 'msdyn\_dualwriteentitymap' olan varlık MetadataCache içinde bulunamadı.*

Bu sorunu gidermek için, Çift-Write Core çözümünün Dataverse'te yüklü olduğundan emin olun . Çift-yazılır çekirdek çözümü, çözüm tanıma için bir önkoşuldur.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]