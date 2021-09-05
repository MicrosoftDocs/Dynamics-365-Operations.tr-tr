---
title: Başlangıç kurulumu sırasında sorunları giderme
description: Bu konuda, çift yazma tümleştirmesinin ilk kurulumu sırasında oluşabilecek sorunları gidermenize yardımcı olabilecek bilgiler sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2b75155aac12d79b9d68cce3e066acaaf80d6764
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380200"
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

![Başarılı sistem durumu denetimi.](media/health_check.png)

Finance and Operations Ve Dataverse ortamları bağlamak için Azure AD kiracı yöneticisi kimlik bilgileriniz olmalıdır. Ortamları bağladıktan sonra, kullanıcılar kendi hesap kimlik bilgilerini kullanarak oturum açabilir ve mevcut bir tablo eşlemesini güncelleştirebilir.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Çift-yazma için bağlanabilen yasal tablo veya şirket sayısı sınırını bulma

Haritaları etkinleştirmeyi denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*İkili yazma hatası - Eklenti kaydı başarısız oldu: [(DWM -1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea projesi için bölüm eşlemesi alınamıyor. Hata, DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea için izin verilen maksimum bölüm sayısını aşıyor)]. Bir veya daha fazla hata oluştu.*

Ortam bağlamayla ilgili geçerli sınır yaklaşık 40 yasal tablodur. Bu hata, eşlemeleri etkinleştirmeye çalışırsanız ve ortamlar arasında 40'tan fazla yasal tablo bağlanmışsa oluşur.

## <a name="connection-set-failed-while-linking-environment"></a>Ortama bağlanırken bağlantı kümesi başarısız oldu

Çift yazma ortamını bağlarken eylem şu hata iletisiyle başarısız oluyor:

*Bağlantı seti kaydedilemedi! Aynı anahtara sahip bir öğe zaten eklenmiş.*

Çift yazma, aynı ada sahip birden fazla tüzel kişiliği/şirketi desteklemez. Örneğin, Dataverse uygulamasında "DAT" adında iki şirketiniz varsa bu hata iletisini alırsınız.

Müşterinin engelini kaldırmak için Dataverse uygulamasındaki **cdm_company** tablosundan yinelenen kayıtları kaldırın. Ayrıca **cdm_company** tablosunda adı boş bırakılmış kayıtlar varsa bu kayıtları kaldırın veya düzeltin.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Finance and Operations uygulamalarında Çift yazma sayfası açılırken hata oluştu

Çift yazma için bir Dataverse ortamını bağlamaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*Yanıt durum kodu başarıyı göstermiyor: 404 (Bulunamadı)*

Bu hata, uygulama onay adımı tamamlanmamışsa oluşur. Kiracı yönetici hesabı kullanıp `portal.azure.com` uygulamasında oturum açarak onay verilip verilmediğini doğrulayabilir ve `33976c19-1db5-4c02-810e-c243db79efde` kimliğine sahip 3. taraf uygulamasının AAD'nin Kurumsal uygulamalar listesinde görünüp görünmediğini kontrol edebilirsiniz. Onay verilmemişse veya listede görünmüyorsa onay adımını bir sonraki bölümde açıklandığı şekilde yeniden çalıştırın.

### <a name="providing-app-consent"></a>Uygulama izni sağlama

+ Yönetici kimlik bilgilerinizle aşağıdaki URL'yi başlatın.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Onaylamak için **Kabul Et**'i seçin. Uygulamayı (`id=33976c19-1db5-4c02-810e-c243db79efde` ile) kiracınıza yüklemek için onay veriyorsunuz.
+ Bu uygulama, Dataverse uygulamasının Finance and Operations uygulamalarıyla iletişim kurması için gereklidir.

    ![İlk eşitleme kurulumu sorunlarını giderme.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Bu işe yaramazsa URL'yi Microsoft Edge uygulamasının özel modunda veya Chrome'un gizli modunda başlatın.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finance and Operations ortamı bulunamıyor

Aşağıdaki hata iletisini alabilirsiniz:

*Finance and Operations uygulamaları ortamı \*\*\*.cloudax.dynamics.com bulunamıyor.*

Ortamın bulunamaması sorununa neden olabilecek iki sebep vardır:

+ Oturum açmak için kullanılan kullanıcı, Finance and Operations kurulumuyla aynı kiracıda değil.
+ Microsoft tarafından barındırılan bazı eski Finance and Operations kurulumlarının bulunmalarıyla ilgili sorunlar vardır. Bu sorunu gidermek için Finance and Operations kurulumunu güncelleştirin. Ortam, herhangi bir güncelleştirmeyle bulunabilir hale gelir.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
