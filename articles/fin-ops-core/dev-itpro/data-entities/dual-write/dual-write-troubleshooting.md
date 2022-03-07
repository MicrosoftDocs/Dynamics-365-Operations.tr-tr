---
title: Genel sorun giderme
description: Bu konu, Finans ve Operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında genel sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6f5b9f26990e2f4db9bf69040a6c4be31400b40
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062350"
---
# <a name="general-troubleshooting"></a>Genel sorun giderme

[!include [banner](../../includes/banner.md)]



Bu konu, Finans ve Operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında genel sorun giderme bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Hata ayrıntılarını görmek için Dataverse'te eklenti izleme günlüğünü etkinleştirme ve görüntüleme

**İzleme günlüğünü açmak ve hataları görüntülemek için gerekli rol:** Sistem Yöneticisi

İz günlüğünü açmak için aşağıdaki adımları izleyin.

1. Müşteri etkileşimi uygulamasında oturum açın, **Ayarlar** sayfasını açın ve **Sistem** altında **Yönetim**'i seçin.
2. **Yönetim** sayfasında **Sistem Ayarları**'nı seçin.
3. **Özelleştirme** sekmesinde, eklenti izleme günlüğünü etkinleştirmek için **Eklenti ve özel iş akışı etkinliği izleme** sütununda **Tümü** seçeneğini belirleyin. Yalnızca özel durumlar gerçekleştiğinde izleme günlüklerini günlüğe kaydetmek istiyorsanız, bunun yerine **özel durum** seçebilirsiniz.


İz günlüğünü açmak için aşağıdaki adımları izleyin.

1. Müşteri etkileşimi uygulamasında oturum açın, **Ayarlar** sayfasını açın ve **Özelleştirme**'nin altında **Eklenti İzleme Günlüğü** öğesini seçin.
2. **Tür Adı** sütununun **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** olarak ayarlandığı izleme günlüklerini bulun.
3. Tam günlüğü görüntülemek için bir öğeyi çift tıklatın ve sonra **yürütme** hızlı sekmesinde **ileti öbeği** metnini gözden geçirin.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Finans ve Operasyon uygulamalarındaki canlı eşitleme sorunlarını gidermek için hata ayıklama modunu etkinleştirme

**Hataları görüntülemek için gerekli rol:** Sistem Yöneticisi

Dataverse'te ortaya çıkan çift yazma hataları Finans ve Operasyon uygulamasında görünebilir. Hatalar için ayrıntılı günlük kaydını etkinleştirmek üzere aşağıdaki adımları izleyin:

1. Finans ve Operasyon uygulamasındaki tüm proje yapılandırmaları için **DualWriteProjectConfiguration** tablosunda bir **IsDebugMode** bayrağı vardır.
2. Excel eklentisini kullanarak **DualWriteProjectConfiguration** öğesini açın. Eklentiyi kullanmak Finans ve Operasyon Excel eklentisinde tasarım modunu etkinleştirin ve sayfaya **DualWriteProjectConfiguration** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
3. Projede **IsDebugMode** öğesini **Evet** olarak ayarlayın.
4. Hata oluşturan senaryoyu çalıştırın.
5. Ayrıntılı günlükler **DualWriteErrorLog** tablosunda saklanır.
6. Tablo tarayıcısında veri aramak için şu bağlantıyı kullanın: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, gerektiğinde `999` değiştirilir.
7. 37 ve sonraki platform güncelleştirmeleri için kullanılabilen [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe)'ten sonra yeniden güncelleştirin. Bu düzeltmeyi yüklediyseniz hata ayıklama modu daha fazla günlük yakalar.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Finans ve Operasyon uygulamasına ilişkin sanal makinedeki eşitleme hatalarını denetleme

**Hataları görüntülemek için gerekli rol:** Sistem yöneticisi

1. Microsoft Dynamics Lifecycle Services (LCS)'de oturum açın.
2. Çift yazma sınaması gerçekleştirmek için seçtiğiniz LCS projesini açın.
3. **Bulutta barındırılan ortamlar** kutucuğunu seçin.
4. Finans ve Operasyon uygulamasının sanal makinesine (VM) oturum açmak için Uzak Masaüstü'nü kullanın. LCS içinde gösterilen yerel hesabı kullanın.
5. Olay Görüntüleyiciyi açın.
6. **Uygulamalar ve Hizmetler günlükleri \> Microsoft \> Dynamics \> AX-DualWriteSync \> İşletim**'e gidin.
7. En son hataların listesini gözden geçirin.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Finans ve Operasyon uygulamasından başka bir Dataverse ortam bağlantısını kaldırma

**Ortamın bağlantısını kaldırmak için gerekli rol:** Finans ve Operasyon uygulaması veya Dataverse için sistem yöneticisi.

1. Finans ve Operasyon uygylamasında oturum açın.
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

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Destek biletlerine izlemelerin eklenebilmesi için ağ izlemeyi etkinleştirme ve kaydetme

Destek ekibinin bazı sorunları gidermek için ağ izlemeyi incelemesi gerekebilir. Ağ izi oluşturmak için şu adımları izleyin:

### <a name="chrome"></a>Chrome

1. Açılan sekmede, **F12** tuşuna basın veya geliştirici araçlarını açmak için **Geliştirici araçları**'nı seçin.
2. **Ağ** sekmesini açın ve filtre metin kutusuna **integ** yazın.
3. Senaryonuzu çalıştırın ve günlüğe kaydedilen istekleri gözlemleyin.
4. Girişlere sağ tıklayın ve **Tümünü içerikleriyle birlikte HAR olarak kaydet**'i seçin.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Açılan sekmede, **F12** tuşuna basın veya geliştirici araçlarını açmak için **Geliştirici araçları**'nı seçin.
2. **Ağ** sekmesini açın.
3. Senaryonuzu çalıştırın.
4. Sonuçları HAR olarak dışarı aktarmak için **kaydet**'i seçin.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
