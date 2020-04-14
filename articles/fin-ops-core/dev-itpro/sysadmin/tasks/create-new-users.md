---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143593"
---
# <a name="create-new-users"></a>Yeni kullanıcılar oluşturma

[!include [banner](../../includes/banner.md)]

Kullanıcılar, işlerini gerçekleştirmek için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Kullanıcıyı lisansla ilişkilendirme (yalnızca yeni lisans türleri)
2019 Ekim tarihinde eklenen yeni lisans türlerinden birinde olan müşterilerimiz için, kullanıcıların bir lisansla ilişkilendirilmesi gerekir. Bir lisans ile ilişkilendirilen kullanıcılar, ilk oturum açtıklarında otomatik olarak rolü olmayan sistem kullanıcıları olarak eklenir.

Sistem yöneticileri [Microsoft 365 yönetim merkezinden](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) [kullanıcılara lisans atayabilir](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) .

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Harici kullanıcıyı lisansla ilişkilendirme (yalnızca yeni lisans türleri)
Ortamın dağıtıldığı kiracının harici kullanıcılarının lisanslara atanabilmeleri için ana bilgisayar kiracı dizininde (Azure Active Directory (Azure AD)) sunulmaları gerekir. Bu harici kullanıcılar Azure AD'de kiracıya konuk kullanıcı olarak eklenmeli ve sonra uygun lisanslara atanmalıdırlar. Daha fazla bilgi için bkz. [Azure portalında Azure Active Directory B2B işbirliği kullanıcıları ekleme](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Yeni bir kullanıcı ekle
1. **Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Kullanıcı Kimliği** alanına, kullanıcı için benzersiz bir tanımlayıcı girin. Bir kullanıcı kimliği gereklidir.  
4. **Kullanıcı adı** alanına, kullanıcının adını girin.  
5. **Etki alanı** alanına, kullanıcının etki alanını girin.  
6. **Diğer ad** alanına kullanıcının diğer adını girin.  
7. **Şirket** alanında, istenilen şirketi seçin. 
8. **Kullanıcı rolleri** hızlı sekmesinde, **Rolleri ata**'yı seçerek kullanıcıları güvenlik rollerine atayın. Daha fazla bilgi için bkz. [Kullanıcıları güvenlik rollerine atama](assign-users-security-roles.md).
9. **Tamam**'ı seçin.
10. **Kaydet**'i seçin.

## <a name="import-users"></a>Kullanıcıları içe aktar
1. Eylem Bölmesinde, **Kullanıcıları içe aktar**'ı seçin.
2. Listede, seçili satırı işaretleyin.
3. **Kullanıcıları içe aktar**'ı seçin.
4. **Kapat**'ı seçin.

