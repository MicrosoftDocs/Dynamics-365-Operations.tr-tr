---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: peakerbl
manager: AnnBe
ms.date: 01/12/2021
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
ms.openlocfilehash: ca062ddd49f1c206c503fb6160ed436fe2d6f7e9
ms.sourcegitcommit: 9e27a097b7eb3c8f2df66011ccc597ad18bc5445
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/13/2021
ms.locfileid: "4878669"
---
# <a name="create-new-users"></a>Yeni kullanıcılar oluşturma

[!include [banner](../../includes/banner.md)]

Finance and Operations uygulamalarına erişmeden önce, **Kullanıcılar** sayfasına (**Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**) eklenmeniz gerekir. Kullanıcılar, kuruluşunuzun şirket içi çalışanlarını veya şirket dışı müşterileri ve satıcıları içerir. Kullanıcılar, içeri aktarılabilir veya el ile eklenebilir. Uyumlu kullanım için tüm kullanıcılar doğru lisansa sahip olmalıdır.

Finance and Operations uygulamalarını satın alma ve lisanslama hakkında bilgi için bkz. [Microsoft Dynamics 365 Lisanslama Kılavuzu](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Kullanıcıya lisans atama
Sistem yöneticileri [Microsoft 365 yönetim merkezinden](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) [kullanıcılara lisans atayabilir](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) .

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Harici kullanıcıyı Azure AD'ye ekleme ve lisans atama 
Harici kullanıcılara lisans atayabilmeniz için bu kullanıcıların kiracı dizininizde (Azure Active Directory (Azure AD)) temsil edilmeleri gerekir. Bu harici kullanıcılar Azure AD'de kiracıya konuk kullanıcı olarak eklenmeli ve sonra uygun lisanslara atanmalıdırlar. Finance and Operations uygulamaları için şartlardan biri, konuk kullanıcının şirketinin Azure AD kullanmasıdır. Daha fazla bilgi için bkz. [Azure portalında Azure Active Directory B2B işbirliği kullanıcıları ekleme](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Azure AD'den yeni kullanıcıları içeri aktarma 
1. **Sistem yönetimi** \> **Kullanıcı** \> **Kullanıcılar** öğesine gidin.
2. Eylem Bölmesinde, **Kullanıcıları içe aktar**'ı seçin.
3. İçeri aktarılacak kullanıcıları seçin. Bu liste, mevcut durumda bu ortamın kullanıcısı olmayan Azure AD kullanıcılarını içerir.
4. **Kullanıcıları içe aktar**'ı seçin.
5. **Kapat**'ı seçin.

> [!NOTE]
> **Şirket** alanının değeri, yöneticinin geçerli oturum şirketi temel alınarak ayarlanır. İçeri aktarmadan sonra, rolleri ve kuruluşları uygun şekilde atamanız gerekir. Daha fazla bilgi için bkz. [Kullanıcıları güvenlik rollerine atama](assign-users-security-roles.md). Koşullu olarak, kullanıcının bir **Kişi** ile ilişkilendirilmesi ve dil gibi kullanıcı seçeneklerinin güncelleştirilmesi gerekebilir.

## <a name="manually-add-a-new-user"></a>Elle yeni kullanıcı ekleme
1. **Sistem yönetimi** \> **Kullanıcılar** \> **Kullanıcılar** öğesine gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Kullanıcı Kimliği** alanına, kullanıcı için benzersiz bir tanımlayıcı girin.   
4. **Kullanıcı adı** alanına, kullanıcının adını girin.  
5. **Sağlayıcı** alanında:
 - Dahili kullanıcılar için varsayılan değeri kullanın. Örneğin, https://sts.windows.net/ ön ekiyle Azure AD kiracınız.  
 - Service-2-Service hesaplarınız gibi Azure AD dışı kullanıcılarınız için temel bir metin değeri girin. Örneğin, NA. Bu değer, geçerli bir kimlik sağlayıcısı değeri kullanıldığında hatalara neden olabilecek hatalı kimlik doğrulaması çağrılarını önlemenize yardımcı olur.  
 - Harici veya konuk kullanıcılar için Azure AD kiracı adını https://sts.windows.net/ öğesinden sonra ekleyin.
6. **E-posta** alanına, kullanıcının tam E-posta/Kullanıcı Asıl Adı'nı girin.  
7. **Şirket** alanında, kullanıcı için varsayılan başlangıç şirketini seçin. 
8. **Kaydet**'i seçin.

Kullanıcı kaydı kaydedildiğinde Kimlik sağlayıcısı ve Telemetri Kimliği değerleri [Microsoft Graph](https://docs.microsoft.com/graph/overview) çağrısına göre güncelleştirilir. Telemetri Kimliği, kullanıcının Azure AD'deki Nesne Kimliği/Güvenlik Tanımlayıcısı (SID) değerine bağlıdır.

> [!NOTE]
> Bir kullanıcıyı ekledikten sonra, rolleri ve kuruluşları uygun şekilde atamanız gerekir. Daha fazla bilgi için bkz. [Kullanıcıları güvenlik rollerine atama](assign-users-security-roles.md). Koşullu olarak, kullanıcının bir **Kişi** ile ilişkilendirilmesi ve dil gibi **Kullanıcı seçenekleri**'nin güncelleştirilmesi gerekebilir.

## <a name="change-a-user-id"></a>Kullanıcı kimliğini değiştirme
Kullanıcı kimliğini değiştirmek için veritabanındaki anahtarı yeniden adlandırmanız gerekir. Bu yordamı kullanarak bir kullanıcı kimliğini değiştirdiğinizde, ilgili tüm kullanıcı ayarları yeni kullanıcı kimliğini kullanacak şekilde değiştirilir. Örneğin, **SysLastValue** tablosundaki kullanım bilgilieri yeni kullanıcı kimliğine başvuracak şekilde güncelleştirilir.

> [!NOTE]
> Kullanıcı kimliği, kullanıcı bilgileri tablosunun birincil anahtarıdır. Anahtara yapılan tüm başvurular veritabanında da güncelleştirileceği için, birincil anahtarı yeniden adlandırma işlemi mevcut kullanıcılar için biraz uzun sürebilir. 

1. **Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.
2. Listeden bir kullanıcı seçin ve  **Seçenekler\> Kayıt bilgileri**'ni seçin.
3. **Yeniden adlandır**'ı seçin.
4. Kullanıcı kimliği için yeni ve benzersiz bir değer girin ve ardından **Tamam**'ı seçin. 
5. Onaylamak için **Evet**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

B2B kullanıcılarını eklemekle ilgili daha fazla seçenek için bkz. [B2B kullanıcılarını Azure AD'ye aktarma](../implement-b2b.md).

Önceden yapılandırılmış sistem hesapları hakkında bilgi için bkz. [Önceden yapılandırılmış sistem hesapları](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]