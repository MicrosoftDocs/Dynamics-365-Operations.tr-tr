---
title: Genel sorun giderme
description: Bu konu, Finans ve Operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında genel sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5896b031229c7fe7e02c8ccf038dd2b1a4f2de05
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614109"
---
# <a name="general-troubleshooting"></a>Genel sorun giderme

[!include [banner](../../includes/banner.md)]



Bu konu, Finans ve Operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında genel sorun giderme bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Hata ayrıntılarını görmek için Dataverse'te eklenti izleme günlüğünü etkinleştirme ve görüntüleme

İzleme günlükleri, Finans ve Operasyon uygulamaları ile Dataverse arasında çift yazma canlı eşitleme sorunlarını giderirken yararlı olabilir. Günlükler, Dynamics 365 için teknik ve mühendislik desteği sağlayan ekiplere belirli ayrıntılar sağlayabilir. Bu makalede izleme günlüklerinin nasıl etkinleştirileceği ve nasıl görüntüleneceği ele alınmaktadır. İzleme günlükleri Dynamics 365 Ayarlar sayfasında yönetilir ve yönetici düzeyinde ayrıcalıkların değiştirilmesini ve görüntülemesini gerektirir. 

**İzleme günlüğünü açmak ve hataları görüntülemek için gerekli rol:** Sistem Yöneticisi

### <a name="turn-on-the-trace-log"></a>İzleme günlüklerini açma
İz günlüğünü açmak için aşağıdaki adımları izleyin.

1.  Dynamics 365'te oturum açın ve üst gezinti çubuğunda **Ayarlar**'ı seçin. Sistemler sayfasında **Yönetim** üzerine tıklayın.
2.  Yönetim sayfasında **Sistem Ayarları**'na tıklayın.
3.  **Özelleştirme** sekmesini ve eklentiyi seçin, ardından özel iş akışı faaliyet izleme bölümünde, açılır menüyü **Tümü** olarak değiştirin. Bu, tüm faaliyetleri izler ve olası sorunları gözden geçirmesi gereken takımlar için kapsamlı bir veri kümesi sağlar.

> [!NOTE]
> Açılan menü **Özel Durum** olarak ayarlandığında, yalnızca özel durumlar (hatalar) oluştuğunda izleme bilgileri sağlanır.

Etkinleştirildiğinde, eklenti izleme günlükleri, bu konuma dönüp **Kapalı**'yı seçerek el ile kapatılıncaya kadar toplanmaya devam eder.

### <a name="view-the-trace-log"></a>İzleme günlüğünü görüntüleme
İz günlüğünü açmak için aşağıdaki adımları izleyin.

1. Dynamics 365 Ayarlar sayfasında, üst gezinti çubuğunda **Ayarlar**'ı seçin. 
2. Sayfanın **Özelleştirmeler** bölümünde **Eklenti İzleme Günlüğü**'nü seçin.
3. İzleme günlükleri listesinde, Tür adına ve/veya İleti adına dayalı olarak girişleri bulabilirsiniz.
4. Tam günlüğü görüntülemek için istediğiniz girişi açın. Yürütme bölümündeki İleti Bloğu, eklenti için kullanılabilir bilgiler sağlayacaktır. Varsa, özel durum ayrıntıları da sağlanacaktır. 

Tüm içeriği daha kolay görebilmek üzere günlükleri veya metin dosyalarını görüntülemek için izleme günlüklerinin içeriğini kopyalayabilir ve Not Defteri gibi başka bir uygulamaya veya diğer araçlara yapıştırabilirsiniz. 

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

## <a name="dual-write-ui-landing-page-showing-blank"></a>Çift yazma kullanıcı arabirimi açılış sayfası boş gösteriliyor
Çift yazma sayfasını Microsoft Edge'de veya Google Chrome tarayıcısında açarken, giriş sayfası yüklenmez ve boş bir sayfa veya "Bir sorun oluştu" gibi bir hata görürsünüz.
Devtools'da konsol günlüklerinde bir hata görürsünüz:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Failed to read the 'sessionStorage' property from 'Window': Access is denied for this document. at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

Kullanıcı arabirimi, giriş sayfasını yüklemek için bazı özellik değerlerini depolamak üzere tarayıcının "oturum depolama alanını" kullanır. Bunun çalışması için, üçüncü taraf tanımlama bilgilerine site tarayıcısında izin verilmesi gerekir. Hata, kullanıcı arabiriminin oturum depolama alanına erişememesinin bir göstergesidir. Bu sorunla karşılaşılan iki senaryo olabilir:

1.  Kullanıcı arabirimini Edge/Chrome'un gizli modunda açıyorsunuz ve gizli modunda üçüncü taraf tanımlama bilgileri engelleniyor.
2.  Edge/Chrome'da üçüncü taraf tanımlama bilgilerini tamamen engellediniz.

### <a name="mitigation"></a>Risk azaltma
Üçüncü taraf tanımlama bilgilerine tarayıcı ayarlarında izin verilmesi gerekir.

### <a name="google-chrome-browser"></a>Google Chrome tarayıcısı
1. seçenek:
1.  Adres çubuğuna chrome://settings/ yazarak ayarlara gidin, ardından Gizlilik ve Güvenlik -> Çerezler ve diğer site verileri'ne gidin.
2.  'Tüm çerezlere izin ver' seçeneğini belirleyin. Bunu yapmak istemiyorsanız, ikinci seçeneğe gidin.

2. seçenek:
1.  Adres çubuğuna chrome://settings/ yazarak ayarlara gidin, ardından Gizlilik ve Güvenlik -> Çerezler ve diğer site verileri'ne gidin.
2.  'Gizli modda üçüncü taraf çerezleri engelle' veya 'Üçüncü taraf çerezleri engelle' seçiliyse 'Her zaman çerez kullanabilen siteler'e gidin ve **Ekle**'ye tıklayın. 
3.  Finans ve Operasyon uygulamaları site adınızı ekleyin - https://<your_FinOp_instance>.cloudax.dynamics.com. "Bu sitedeki üçüncü taraf çerezler dahil" onay kutusunu seçtiğinizden emin olun. 

### <a name="microsoft-edge-browser"></a>Microsoft Edge tarayıcısı
1.  Ayarlar -> Site izinleri -> Tanımlama bilgileri ve site verileri'ne gidin.
2.  'Üçüncü taraf tanımlama bilgilerini engelle' seçeneğini kapatın.  

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

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Veri tümleştirmenin en güncel Finans ve Operasyon şemasını kullandığı nasıl emin olunur

En güncel şema kullanılmıyorsa, veri tümleştirmede veri sorunları yaşayabilirsiniz. Aşağıdaki adımlar, finans ve operasyon uygulamalarındaki varlık listesini ve veri tümleştiricisi içindeki varlıkları yenilediğiniz konusunda size yardımcı olur.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Finans ve Operasyon ortamınızda varlık listesini yenileme
1.  Finans ve Operasyon ortamınızda oturum açın.
2.  **Veri yönetimi**'ni seçin.
3.  Veri yönetimi içinde, **Çerçeve parametreleri**'ni seçin.
4.  **Veri içe/dışa aktarma çerçevesi parametreleri** sayfasında, **Varlık ayarları** sekmesini seçin ve ardından **Varlık listesini yenile** sekmesini seçin. Bu işlem, ilgili varlık sayısına bağlı olarak 30 dakikadan fazla sürebilir.
5.  **Veri Yönetimi**'ne gidin ve beklenen varlıkların listelendiğini doğrulamak için **Veri varlıkları**'nı seçin. Beklenen varlıklar listelenmemişse, varlıkların finans ve operasyonlar ortamınızda göründüğünü doğrulayın ve gerektiği şekilde eksik varlıkları geri yükleyin.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Yenileme sorunu çözemezse, varlıkları silin ve yeniden ekleyin

> [!NOTE]
> Silmeden önce, varlıkları etkin şekilde kullanan tüm işlem gruplarını durdurmanız gerekebilir.

1.  Finans ve operasyonlar ortamınızda **Veri yönetimi**'ni seçin ve **Veri varlıklarını** seçin.
2.  Sorun olan varlıkları arayın ve hedef varlığı, hazırlama tablosunu, varlık adını ve diğer ayarları not alın. Varlık veya varlıkları listeden silin.
3.  **Yeni**'yi seçin ve 2. adımdaki verileri kullanarak varlığı veya varlıkları yeniden ekleyin. 

#### <a name="refresh-entities-in-data-integrator"></a>Veri tümleştiricisi içindeki varlıklar yenile
Power Platform Yönetici Merkezinde oturum açın ve **Veri tümleştirmesi**'ni seçin. Sorunların oluştuğu projeyi açın ve **Varlıkları yenile**'yi seçin.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Destek biletlerine izlemelerin eklenebilmesi için ağ izlemeyi etkinleştirme ve kaydetme

Destek ekibinin bazı sorunları gidermek için ağ izlemeyi incelemesi gerekebilir. Ağ izi oluşturmak için şu adımları izleyin:

### <a name="google-chrome-browser"></a>Google Chrome tarayıcısı

1. Açılan sekmede, **F12** tuşuna basın veya geliştirici araçlarını açmak için **Geliştirici araçları**'nı seçin.
2. **Ağ** sekmesini açın ve filtre metin kutusuna **integ** yazın.
3. Senaryonuzu çalıştırın ve günlüğe kaydedilen istekleri gözlemleyin.
4. Girişlere sağ tıklayın ve **Tümünü içerikleriyle birlikte HAR olarak kaydet**'i seçin.

### <a name="microsoft-edge-browser"></a>Microsoft Edge tarayıcısı

1. Açılan sekmede, **F12** tuşuna basın veya geliştirici araçlarını açmak için **Geliştirici araçları**'nı seçin.
2. **Ağ** sekmesini açın.
3. Senaryonuzu çalıştırın.
4. Sonuçları HAR olarak dışarı aktarmak için **kaydet**'i seçin.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
