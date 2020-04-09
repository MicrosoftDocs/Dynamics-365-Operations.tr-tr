---
title: Finance and Operations uygulamalarında Çift yazma modülüyle ilgili sorunları giderme
description: Bu konu, Finance and Operations uygulamalardaki çift-yazma modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172772"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Finance and Operations uygulamalarında Çift yazma modülüyle ilgili sorunları giderme

[!include [banner](../../includes/banner.md)]



Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, Finance and Operations uygulamalardaki **çift-yazma** modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Çift-yazılır modülü bir Finance and Operations uygulamaya yüklenemez

**Çift- yazılır** sayfayı, **veri yönetimi** çalışma alanında **ikili yazma** kutucuğunu seçerek açamazsınız, veri tümleştirme hizmeti büyük olasılıkla çalışmıyor olabilir. Veri tümleştirme hizmetinin yeniden başlatılmasını istemek için bir destek bileti oluşturun.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Yeni bir varlık eşlemesi oluşturmaya çalıştığınızda hata oluştu

**Sorunun düzeltilmesi için gerekli olan kimlik bilgileri:** Azure AD Kiracı Yönetimi

Çift-yazılır için yeni bir varlık yapılandırmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*Yanıt durum kodu başarıyı göstermiyor: 401 (yetkisiz)*

Bu hata, yalnızca bir Azure AD kiracı yöneticisinin yeni bir varlık eşlemesi ekleyebilmesi nedeniyle oluşur.

Bu sorunu gidermek için, Finance and Operations uygulamaya Azure AD yönetici kiracısı olarak oturum açın. Ayrıca Web.PowerApps.com'e gitmelisiniz ve bağlantınızı yeniden doğrular.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>İkili yazma Kullanıcı arabirimini açtığınızda hata oluştu

**Veri yönetimi** çalışma alanından çift-yazılabilir erişmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*login.microsoftonline.com bağlanmayı reddetti.*

Sorunu gidermek için, Microsoft Edge'de bir InPrivate pencere, Chromium'da bir gizli penceresi veya Google Chrome 'da bir gizli penceresi kullanarak oturum açın. Ayrıca, üçüncü taraf tanımlama bilgilerini engellemeyi veya temizlemeniz gerekir.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Ortam ikili yazma için bağlantılandırma sırasında hata oluştu veya yeni bir varlık eşlemesi ekler

**Sorunun düzeltilmesi için gerekli olan kimlik bilgileri:** Azure AD Kiracı Yönetimi

Haritaları bağlarken veya oluştururken aşağıdaki hata ile karşılaşabilirsiniz:

*Yanıt durum kodu başarı göstermiyor: 403 (tokenexchange). <br>Oturum kodu: \<oturum kimliği\><br> kök etkinlik kimliği: \<kök etkinlik kimliğiniz\>*

Bu hata, Çift-yazılabilir veya haritalar oluşturmak için yeterli izniniz yoksa oluşabilir. Ortamları bağlamak ve yeni Azure AD varlık eşlemeleri eklemek için kiracı yöneticisi hesabı kullanmalısınız. Ancak, kurulumdan sonra, durumu izlemek ve eşlemeleri düzenlemek için yönetici olmayan bir hesabı kullanabilirsiniz.

## <a name="error-when-you-stop-the-entity-mapping"></a>Varlık eşlemesini durdurduğunuzda hata oluştu

Varlık eşlemelerini durdurmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*\[Yasak\], \[{"durum": 403, "kaynak": "", "mesaj": "belirteç değiş tokuşu nedeniyle hata: kullanıcının dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]bağlantısına erişmesine izin verilmiyor uzak sunucu hata verdi: (403) yasak.*

Bu hata, bağlı Common Data Service ortam kullanılabilir olmadığında oluşur.

Bu sorunu gidermek için, veri tümleştirme ekibi için bir bilet oluşturun. Veri tümleştirme ekibinin eşlemeleri arka uçta **çalışmıyor** olarak işaretlemesi için ağ izlemesini iliştirin.
