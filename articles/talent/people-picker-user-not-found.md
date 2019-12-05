---
title: Kullanıcı, Attract veya Onboard'ta Kişi Seçici içinde bulunamadı
description: Bu konuda şirket kiracısındaki kullanıcılar Dynamics 365 Talent - Attract veya Onboard'taki Kişi Seçici'de görüntülenmediğinde ne yapılacağı açıklanmaktadır.
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
ms.openlocfilehash: a6d916f87ca30aa7405a51841e56ab31bbe31ac8
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832616"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a>Kullanıcı, Attract veya Onboard'ta Kişi Seçici içinde bulunamadı

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Çıkış

Kiracı için Microsoft Microsoft Azure Active Directory (Azure AD) üzerindeki çeşitli geçerli kullanıcılar, Dynamics 365 Talent: Attract veya Dynamics 365 Talent: Onboard uygulamalarında Kişi Seçici'de adları aranırken görüntülenmiyor.

## <a name="cause"></a>Nedeni

Bazı kullanıcı türleri, Attract ve Onboard uygulamalarında şu anda desteklenmemektedir. Kullanıcının bir Azure AD Business to Business (B2B) misafir kullanıcısı olmadığından emin olun. "Kullanıcı Türü" bilgisi, Azure portalındaki Azure Active Directory dikey pencere taşında bulunabilir.

Azure B2B hakkında daha fazla bilgi için bkz. [Azure Active Directory B2B'de misafir kullanıcı erişimi nedir](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).

B2B olmayan kullanıcılar için bazı kullanıcılar eksik "Kullanıcı Türü" özelliğine **Kullanıcı** nesnesi üzerinde sahip olabilirler. Bu, Azure AD PowerShell modülü kullanılarak düzeltilebilir. Daha fazla bilgi için [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0) konusuna bakın.

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
