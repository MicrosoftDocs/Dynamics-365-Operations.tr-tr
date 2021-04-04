---
title: Çözüm farkındalığıyla ilgili sorunları giderme
description: Bu konu, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f9e02a6a5afe965a1707f0b04e1b4daedd4ec1df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566801"
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