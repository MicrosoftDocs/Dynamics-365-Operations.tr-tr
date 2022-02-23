---
title: Genel sorun giderme
description: Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında genel sorun giderme bilgileri sağlar.
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
ms.openlocfilehash: b01ef3da908739d17f2a03398ae56f35191e8db6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744553"
---
# <a name="general-troubleshooting"></a>Genel sorun giderme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında genel sorun giderme bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>İkili yazma paketini paket dağıtıcı aracını kullanarak yüklemeye çalıştığınızda, kullanılabilir çözüm gösterilmemiştir

Paket Dağıtıcı aracının bazı sürümleri çift yazma çözüm paketiyle uyumsuz. Paketi başarılı bir şekilde yüklemek için, paket dağıtıcı aracının [sürüm 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) veya üstünü kullandığınızdan emin olun.

Package Deployer aracını yükledikten sonra, aşağıdaki adımları izleyerek çözüm paketini yükleyin.

1. Yammer.Com ' dan en son çözüm paketi dosyasını karşıdan yükle. Paket ZIP dosyası karşıdan yüklendikten sonra sağ tıklatın ve **Özellikler** 'i seçin. **Engeli kaldır** onay kutusunu seçin ve **Uygula**'yı seçin. **Engellemeyi kaldır** onay kutusunu görmüyorsanız, zip dosyasının engeli zaten kaldırılır ve bu adımı atlayabilirsiniz.

    ![Özellikler iletişim kutusu](media/unblock_option.png)

2. Paket ZIP dosyasını ayıklayın ve **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** klasöründeki tüm dosyaları kopyalayın.

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 klasörü içeirği](media/extract_package.png)

3. Kopyalanan tüm dosyaları, Paket Dağıtıcı aracı'nın **Araçlar** klasörüne yapıştırın. 
4. Dataverse Ortamı seçmek ve çözümleri yüklemek için **PackageDeployer. exe** dosyasını çalıştırın.

    ![Araçlar klasörünün içeriği](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Hata ayrıntılarını görmek için Dataverse'te eklenti izleme günlüğünü etkinleştirme ve görüntüleme

**İzleme günlüğünü açmak ve hataları görüntülemek için gerekli rol:** Sistem Yöneticisi

İz günlüğünü açmak için aşağıdaki adımları izleyin.

1. Dynamics 365'teki model yönetimli uygulamada oturum açın, **Ayarlar** sayfasını açın ve sonra **Sistem** altında **Yönetim**'i seçin.
2. **Yönetim** sayfasında **Sistem Ayarları**'nı seçin.
3. **Özelleştirme** sekmesinde, eklenti izleme günlüğünü etkinleştirmek için **Eklenti ve özel iş akışı etkinliği izleme** sütununda **Tümü** seçeneğini belirleyin. Yalnızca özel durumlar gerçekleştiğinde izleme günlüklerini günlüğe kaydetmek istiyorsanız, bunun yerine **özel durum** seçebilirsiniz.


İz günlüğünü açmak için aşağıdaki adımları izleyin.

1. Dynamics 365'teki model yönetimli uygulamada oturum açın, **Ayarlar** sayfasını açın ve sonra **Özelleştirme** altında **Eklenti İzleme Günlüğü**'nü seçin.
2. **Tür Adı** sütununun **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** olarak ayarlandığı izleme günlüklerini bulun.
3. Tam günlüğü görüntülemek için bir öğeyi çift tıklatın ve sonra **yürütme** hızlı sekmesinde **ileti öbeği** metnini gözden geçirin.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Finance and Operations Uygulamalardaki canlı eşitleme sorunlarını gidermek için hata ayıklama modunu etkinleştir

**Hataları görüntülemek için gerekli olan rol:** Dataverse uygulamasında yer alan sistem yöneticisi Çift yazma hataları Finance and Operations uygulamasında görünebilir. Bazı durumlarda, ileti çok uzun veya kişisel tanımlayıcı bilgiler (PII) içerdiğinden hata iletisinin tam metni kullanılamıyor. Hata için ayrıntılı günlüğü, aşağıdaki adımları izleyerek açabilirsiniz.

1. Finance and Operations uygulamalarındaki tüm proje yapılandırmalarında **DualWriteProjectConfiguration** tablosunda bir **IsDebugMode** özelliği vardır. **DualWriteProjectConfiguration** tablosunu Excel eklentisini kullanarak açın.

    > [!TIP]
    > Tabloyu açmanın kolay bir yolu, Excel eklentilerinde **Tasarım** modunu etkinleştirmek ve sonra da çalışma sayfasına **DualWriteProjectConfigurationEntity** öğesini eklemektir. Daha fazla bilgi için bkz. [Tablo verilerini Excel'de açma ve Excel eklentisini kullanarak güncelleştirme](../../office-integration/use-excel-add-in.md).

2. **Isdebugmode** özelliğini proje için **Evet** olarak ayarlayın.
3. Hata oluşturan senaryoyu çalıştırın.
4. Ayrıntılı Günlükler DualWriteErrorLog tablosunda bulunur. Verileri tablo tarayıcısında aramak için aşağıdaki URL 'yi kullanın (**xxx**'yi uygun şekilde değiştirin):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Finance and Operations Uygulamaya ilişkin sanal makinedeki eşitleme hatalarını denetle

**Hataları görüntülemek için gerekli rol:** Sistem yöneticisi

1. Microsoft Dynamics Lifecycle Services (LCS)'de oturum açın.
2. Çift yazma sınaması gerçekleştirmek için seçtiğiniz LCS projesini açın.
3. **Bulutta barındırılan ortamlar** kutucuğunu seçin.
4. Finance and Operations Uygulamanın sanal makinesine (VM) oturum açmak Için uzak masaüstü 'nü kullanın. LCS içinde gösterilen yerel hesabı kullanın.
5. Olay Görüntüleyiciyi açın.
6. **Uygulamalar ve Hizmetler günlükleri \> Microsoft \> Dynamics \> AX-DualWriteSync \> İşletim**'e gidin.
7. En son hataların listesini gözden geçirin.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamadan başka bir Dataverse ortam bağlantısını kaldır ve bağlantıyı kes

**Ortamın bağlantısını kaldırmak için gerekli rol:** Finance and Operations veya Dataverse uygulaması için sistem yöneticisi.

1. Finance and Operations Uygulamaya oturum açın.
2. **Çalışma alanları \> veri yönetimi**'ne gidin ve **ikili yazma** kutucuğunu seçin.
3. Çalışan tüm eşlemeleri seçin ve **Durdur**'u tıklatın.
4. **Ortam bağlantısını kaldırma**'yı seçin.
5. Operasyonu onaylamak için **Evet**'i seçin.

Şimdi yeni bir ortam bağlayabilirsiniz.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Satış siparişi satırı Bilgi formu görüntülenemiyor 

Dynamics 365 Sales içinde bir satış siparişi oluşturduğunuzda, **+ Ürün ekle**'ye tıklamak, sizi Dynamics 365 Project Operations sipariş satırı formuna yönlendirebilir. Satış siparişi satırı **Bilgi** formunu görüntülemek için bu formdan bir yol yoktur. **Bilgi** seçeneği, **Yeni Sipariş Satırı** altındaki açılan listede görüntülenmez. Bunun nedeni, Project Operations'ın ortamınıza yüklenmiş olmasıdır.

**Bilgi** formu seçeneğini yeniden etkinleştirmek için şu adımları izleyin:
1. **Sipariş Satırı** tablosuna gidin.
2. Formlar düğümünün altından **Bilgi** formunu bulun. 
3. **Bilgi** formunu seçin ve **Güvenlik rollerini etkinleştir**'e tıklayın. 
4. Güvenlik ayarını **Herkese göster** olarak değiştirin.
