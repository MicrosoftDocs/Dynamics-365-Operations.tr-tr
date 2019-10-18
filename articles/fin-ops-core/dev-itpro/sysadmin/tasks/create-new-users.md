---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180956"
---
# <a name="create-new-users"></a>Yeni kullanıcılar oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Kullanıcılar, işlerini gerçekleştirmek için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Kullanıcıyı lisansla ilişkilendirme (yalnızca yeni lisans türleri)
2019 Ekim tarihinde eklenen yeni lisans türlerinden birinde olan müşterilerimiz için, kullanıcıların bir lisansla ilişkilendirilmesi gerekir. Bir lisans ile ilişkilendirilen kullanıcılar, ilk oturum açtıklarında otomatik olarak rolü olmayan sistem kullanıcıları olarak eklenir. Bir lisans ile ilişkili olmayan kullanıcılar bir uyarı iletisi alır.

Sistem yöneticileri [Microsoft 365 yönetim merkezinden](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) [kullanıcılara lisans atayabilir](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) .

## <a name="add-a-new-user"></a>Yeni bir kullanıcı ekle
1. **Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Kullanıcı Kimliği** alanına, kullanıcı için benzersiz bir tanımlayıcı girin. Bir kullanıcı kimliği gereklidir.  
4. **Kullanıcı adı** alanına, kullanıcının adını girin.  
5. **Etki alanı** alanına, kullanıcının etki alanını girin.  
6. **Diğer ad** alanına kullanıcının diğer adını girin.  
7. **Şirket** alanında, istenilen şirketi seçin. 
8. **Kullanıcı rolleri** hızlı sekmesinde, **Rol ata**'yı seçerek [kullanıcılara güvenlik rolleri atayın](assign-users-security-roles.md)
9. **Tamam**'ı seçin.
10. **Kaydet**'i seçin.

## <a name="import-users"></a>Kullanıcıları içe aktar
1. Eylem Bölmesinde, **Kullanıcıları içe aktar**'ı seçin.
2. Listede, seçili satırı işaretleyin.
3. **Kullanıcıları içe aktar**'ı seçin.
4. **Kapat**'ı seçin.

