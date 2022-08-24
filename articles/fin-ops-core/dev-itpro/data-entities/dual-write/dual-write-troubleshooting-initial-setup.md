---
title: Başlangıç kurulumu sırasında sorunları giderme
description: Bu makalede, çift yazma tümleştirmesinin ilk kurulumu sırasında oluşabilecek sorunları gidermenize yardımcı olabilecek bilgiler sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289529"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Başlangıç kurulumu sırasında sorunları giderme

[!include [banner](../../includes/banner.md)]

Bu makalede, finans ve operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında sorun giderme bilgileri sağlanmaktadır. Bu konu, çift-yazma tümleştirmesinin ilk kurulumu sırasında oluşabilecek sorunları gidermenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu makalede ele alınan bazı sorunlar için sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Bir finans ve operasyon uygulamasını Dataverse'e bağlayamazsınız

**Çift yazmayı ayarlamak için gereken rol:** Finans ve operasyon uygulamalarında ve Dataverse'te sistem yöneticisi.

**Dataverse'e bağlantı kur** sayfa üzerindeki hatalar genellikle tamamlanmamış kurulum veya izin sorunlarından kaynaklanır. Aşağıdaki çizimde gösterildiği gibi, tüm sistem durumu denetiminin **Dataverse'e bağlantı kur** sayfası üzerinden geçerken emin olun. Tüm sistem durumu denetimi başarılı olmadıkça çift-yazma bağlantısı yapamazsınız.

![Başarılı sistem durumu denetimi.](media/health_check.png)

Finans ve operasyon ile Dataverse ortamlarını bağlamak için Azure AD kiracı yöneticisi kimlik bilgileriniz olmalıdır. Ortamları bağladıktan sonra, kullanıcılar kendi hesap kimlik bilgilerini kullanarak oturum açabilir ve mevcut bir tablo eşlemesini güncelleştirebilir.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Çift-yazma için bağlanabilen yasal tablo veya şirket sayısı sınırını bulma

Haritaları etkinleştirmeyi denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*İkili yazma hatası - Eklenti kaydı başarısız oldu: [(DWM -1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea projesi için bölüm eşlemesi alınamıyor. Hata, DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea için izin verilen maksimum bölüm sayısını aşıyor)]. Bir veya daha fazla hata oluştu.*

Ortam bağlamayla ilgili geçerli sınır yaklaşık 40 yasal tablodur. Bu hata, eşlemeleri etkinleştirmeye çalışırsanız ve ortamlar arasında 40'tan fazla yasal tablo bağlanmışsa oluşur.

## <a name="connection-set-failed-while-linking-environment"></a>Ortama bağlanırken bağlantı kümesi başarısız oldu

Çift yazma ortamını bağlarken eylem şu hata iletisiyle başarısız oluyor:

*Bağlantı seti kaydedilemedi! Aynı anahtara sahip bir öğe zaten eklenmiş.*

Çift yazma, aynı ada sahip birden fazla tüzel kişiliği/şirketi desteklemez. Örneğin, Dataverse uygulamasında "DAT" adında iki şirketiniz varsa bu hata iletisini alırsınız.

Müşterinin engelini kaldırmak için Dataverse uygulamasındaki **cdm_company** tablosundan yinelenen kayıtları kaldırın. Ayrıca **cdm_company** tablosunda adı boş bırakılmış kayıtlar varsa bu kayıtları kaldırın veya düzeltin.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarında Çift yazma sayfası açılırken hata oluştu

Çift yazma için bir Dataverse ortamını bağlamaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*Yanıt durum kodu başarıyı göstermiyor: 404 (Bulunamadı)*

Bu hata, uygulama onay adımı tamamlanmamışsa oluşur. Kiracı yönetici hesabı kullanıp `portal.azure.com` uygulamasında oturum açarak onay verilip verilmediğini doğrulayabilir ve `33976c19-1db5-4c02-810e-c243db79efde` kimliğine sahip 3. taraf uygulamasının AAD'nin Kurumsal uygulamalar listesinde görünüp görünmediğini kontrol edebilirsiniz. Onay verilmemişse veya listede görünmüyorsa onay adımını bir sonraki bölümde açıklandığı şekilde yeniden çalıştırın.

### <a name="providing-app-consent"></a>Uygulama izni sağlama

+ Yönetici kimlik bilgilerinizle aşağıdaki URL'yi başlatın.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Onaylamak için **Kabul Et**'i seçin. Uygulamayı (`id=33976c19-1db5-4c02-810e-c243db79efde` ile) kiracınıza yüklemek için onay veriyorsunuz.
+ Bu uygulama, Dataverse'ün finans ve operasyon uygulamalarıyla iletişim kurması için gereklidir.

    ![İlk eşitleme kurulumu sorunlarını giderme.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Bu işe yaramazsa URL'yi Microsoft Edge uygulamasının özel modunda veya Chrome'un gizli modunda başlatın.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finans ve operasyon ortamı bulunabilir değil

Aşağıdaki hata iletisini alabilirsiniz:

*Finans ve operasyon uygulamaları ortamı \*\*\*.cloudax.dynamics.com bulunabilir değil.*

Ortamın bulunamaması sorununa neden olabilecek iki sebep vardır:

+ Oturum açmak için kullanılan kullanıcı, finans ve operasyon kurulumuyla aynı kiracıda değil.
+ Microsoft tarafından barındırılan bazı eski finans ve operasyon kurulumlarının bulunmalarıyla ilgili sorunlar vardır. Bu sorunu gidermek için finans ve operasyon kurulumunu güncelleştirin. Ortam, herhangi bir güncelleştirmeyle bulunabilir hale gelir.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>403 (Yasak) bağlantılar oluşturulurken hata oluştu

Çift-yazma bağlama işleminin bir parçası olarak, bağlantılı Dataverse ortamında kullanıcı adına iki Power Apps bağlantısı (*Apihub* bağlantıları olarak da bilinir) oluşturulur. Müşterinin Power Apps ortamı için lisansı yoksa, ApiHub bağlantıları oluşturma işlemi başarısız olur ve 403 (yasak) hatası gösterilir. Burada hata mesajının bir örneği verilmiştir:

> MSG=\[Çift yazma ortamı ayarlanamadı. Hata Ayrıntıları: Yanıt durum kodu başarıyı göstermiyor: 403 (Yasak). - Yanıt durum kodu başarıyı göstermiyor: 403 (Yasak).\] STACKTRACE=\[   at Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- End of stack trace from previous location where exception was thrown --- at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) at Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

Bu hata bir Power Apps lisansı olmaması nedeniyle oluşur. Kullanıcıya, bağlantıları oluşturma izni olacak şekilde uygun bir lisans atayın (örneğin, Power Apps Deneme 2 Planı). Müşteri, lisansı doğrulamak için, kullanıcıya o anda atanmış olan lisansları görüntülemek üzere [Hesabım](https://portal.office.com/account/?ref=MeControl#subscriptions) sitesine gidebilir.

Power Apps lisansı hakkında daha fazla bilgi için aşağıdaki makalelere bakın:

- [Kullanıcılara lisans atama](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Kuruluşunuz için Power Apps satın alma](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

