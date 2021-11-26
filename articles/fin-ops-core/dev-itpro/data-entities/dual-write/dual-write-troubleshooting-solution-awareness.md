---
title: Çözüm farkındalığıyla ilgili sorunları giderme
description: Bu konu, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: ec5afd92a71c8b12c913de78a513abb0959df88a
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782073"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Çözüm farkındalığıyla ilgili sorunları giderme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="error-on-the-dual-write-page"></a>Çift-yazma sayfasında hata

**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:

*namemapping='Logical' bulunan, adı 'msdyn\_dualwriteentitymap' olan varlık MetadataCache içinde bulunamadı.*

Bu sorunu gidermek için, Çift-Write Core çözümünün Dataverse'te yüklü olduğundan emin olun . Çift-yazılır çekirdek çözümü, çözüm tanıma için bir önkoşuldur.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]