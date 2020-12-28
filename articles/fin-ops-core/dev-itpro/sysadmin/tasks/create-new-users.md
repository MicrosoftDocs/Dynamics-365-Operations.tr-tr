---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: peakerbl
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f861b7493d039b332358be7df7d0198cbadcb7a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679852"
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
1. **Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.
2. Eylem Bölmesinde, **Kullanıcıları içe aktar**'ı seçin.
3. Listede, seçili satırı işaretleyin.
4. **Kullanıcıları içe aktar**'ı seçin.
5. **Kapat**'ı seçin.

