---
title: Kullanıcı, Attract veya Onboard'da Kişi Seçici içinde bulunamadı
description: Bu konu, şirket kiracısı içindeki kullanıcılar Dynamics 365 for Talent Attract veya Onboard uygulamalarındaki Kişi Seçicide görüntülenmediğinde ne yapılacağını açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "859517"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory kullanıcıları Kişi Seçici'de bulunamadı

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Çıkış

Kiracı için Microsoft Azure Active Directory (Azure AD) içindeki çeşitli geçerli kullanıcılar, Dynamics 365 for Talent Attract veya Onboard uygulamalraında Kişi Seçicide adları aratılırken görüntülenmiyor.

## <a name="cause"></a>Nedeni

Çeşitli kullanıcı türleri Attract ve Onboard uygulamalarında şu anda desteklenmiyor. Kullanıcının bir Azure AD Business to Business (B2B) misafir kullanıcısı olmadığından emin olun. "Kullanıcı Türü" bilgisi, Azure portalındaki Azure Active Directory dikey pencere taşında bulunabilir.

Azure B2B hakkında daha fazla bilgi için bkz. [Azure Active Directory B2B'de misafir kullanıcı erişimi nedir](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

B2B olmayan kullanıcılar için bazı kullanıcılar eksik "Kullanıcı Türü" özelliğine **Kullanıcı** nesnesi üzerinde sahip olabilirler. Bu, Azure AD PowerShell modülü kullanılarak düzeltilebilir. Daha fazla bilgi için [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0) konusuna bakın.

## <a name="resolution"></a>Çözünürlük

Aşağıdaki adımları sorunu gidermek için tamamlamak için "Genel Yönetici" izinlerine Azure Active Directory kiracısı üzerinde sahip olmalısınız veya **User.ReadWrite.All** izinlerine sahip olmalısınız.

Etkilenen kullanıcı için "Kullanıcı Türünü" doğrulamak için.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Komut, aşağıdaki bilgiyi döndürür.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Kullanıcı üzerindeki **UserType** özelliğini not edin. **UserType** boş ise, örneğin "Üye" veya "Misafir" değilse, **UserType**'ı aşağıdaki komutu kullanarak güncelleştirin.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
