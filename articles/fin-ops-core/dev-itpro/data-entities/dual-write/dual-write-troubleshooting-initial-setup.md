---
title: Başlangıç kurulumu sırasında sorunları giderme
description: Bu konu, Finance and Operations uygulamalar ve Dataverse arasında çift-yazma tümleştirmesinin ilk kurulumu sırasında oluşabilecek sorunları gidermenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5ac6ec5003794fb5875fed6a2c4403c1444ab8b2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685599"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Başlangıç kurulumu sırasında sorunları giderme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, çift-yazma tümleştirmesinin ilk kurulumu sırasında oluşabilecek sorunları gidermenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Bir Finance and Operations uygulamayı Dataverse'e bağlayamazsınız

**Çift yazmayı ayarlamak için gereken rol:** Finance and Operations uygulamalarında ve Dataverse'ta sistem yöneticisi.

**Dataverse'e bağlantı kur** sayfa üzerindeki hatalar genellikle tamamlanmamış kurulum veya izin sorunlarından kaynaklanır. Aşağıdaki çizimde gösterildiği gibi, tüm sistem durumu denetiminin **Dataverse'e bağlantı kur** sayfası üzerinden geçerken emin olun. Tüm sistem durumu denetimi başarılı olmadıkça çift-yazma bağlantısı yapamazsınız.

![Başarılı sistem durumu denetimi](media/health_check.png)

Finance and Operations Ve Dataverse ortamları bağlamak için Azure AD kiracı yöneticisi kimlik bilgileriniz olmalıdır. Ortamları bağladıktan sonra, kullanıcılar kendi hesap kimlik bilgilerini kullanarak oturum açabilir ve mevcut bir tablo eşlemesini güncelleştirebilir.

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>Dataverse sayfa bağlantısını açtığınızda hata oluştu

**Sorunun düzeltilmesi için gerekli olan kimlik bilgileri:** Azure AD Kiracı Yönetimi

Finance and Operations uygulamasında **Dataverse'e bağlantı** açtığınızda aşağıdaki hata iletisini alabilirsiniz:

*Yanıt durum kodu başarıyı göstermiyor: 404 (Bulunamadı)*

Bu hata, onay adımı tamamlanmamışsa oluşur. Onay adımının tamamlanıp tamamlanmadığını doğrulamak için Azure AD kiracı yöneticisi hesabını kullanarak portal.Azure.com oturum açın ve Azure AD **kurumsal uygulamalar** listesinde **33976c19-1db5-4c02-810e-c243db79efde** kimliğine sahip üçüncü taraf uygulamanın görünüp görünmeyeceğini görün. İçermiyorsa, uygulama onayı sağlamalısınız.

Uygulama onayı sağlamak için aşağıdaki adımları izleyin.

1. Yönetici kimlik bilgilerinizi kullanarak aşağıdaki URL 'YI açın. Sizden izin vermeniz istenecektir.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Kiracınıza **33976c19-1db5-4c02-810e-c243db79efde** kimliği olan uygulamayı yükleme izniniz olduğunu belirtmek için **kabul et**'i seçin.

    > [!TIP]
    > Bu uygulama Dataverse ve Finance and Operations uygulamalarını bağlamak için gerekli. Bu adımla ilgili sorununuz varsa, tarayıcınızı Google Chrome ya da Microsoft Edge'de gizli modunda açın.

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Şirket verileri ve çift-yazılır takımların bağlantı sırasında doğru şekilde ayarlandığını doğrulayın

Çift-yazmanın doğru çalışmasını sağlamak için, konfigürasyon sırasında seçtiğiniz şirketler Dataverse ortamda oluşturulur. Varsayılan olarak, bu şirketler salt okunurdur **IsDualWriteEnable** özelliği **doğru** olarak ayarlanır. Ek olarak, varsayılan sorumlu departman sahibi ve ekibi oluşturulur ve şirket adını içerir. Eşlemeleri etkinleştirmeden önce varsayılan takım sahibinin belirtildiğinden emin olun. **Şirketler (CDM\_şirketi)** varlığını bulmak için aşağıdaki adımları izleyin.

1. Dynamics 365'deki model kullanımlı uygulamada, sağ üst köşedeki filtreyi seçin.
2.  açılır listede, **Şirket**'ı seçin.
3. Sonuçları görmek için **Çalıştır** 'ı seçin.
4. Çift-yazmayı konfigüre ettiğinizde bağlanan şirketi seçin.
5. **Varsayılan sahip olan takım** alanının bir değere sahip olduğunu doğrulayın. Aşağıdaki çizimde, **varsayılan sahibi olan takım** alanı **usmf ikili yazma** olarak ayarlanır.

    ![Varsayılan sahip olan takım doğrulanıyor](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Çift-yazma için bağlanabilen yasal tablo veya şirket sayısı sınırını bulma

Haritaları etkinleştirmeyi denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*İkili yazma hatası - Eklenti kaydı başarısız oldu: \[(Proje DWM için bölüm eşlemesi alınamıyor - 1ae35e60-4bc2-4905-88ea-69efd3b29260-.7f12cb89-1550-42e2-858e-4761fc1443ea. Hata, DWM için izin verilen maksimum bölüm sayısını aşıyor - 1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], bir veya daha fazla hata oluştu.*

Ortam bağlamayla ilgili geçerli sınır yaklaşık 40 yasal tablodur. Bu hata, eşlemeleri etkinleştirmeye çalışırsanız ve ortamlar arasında 40'tan fazla yasal tablo bağlanmışsa oluşur.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]