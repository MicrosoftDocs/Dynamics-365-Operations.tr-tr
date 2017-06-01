---
title: "Eldeki stok mobil çalışma alanı"
description: "Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Eldeki stok mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, ayrılmış ve kullanılabilir stok hakkında mobil bilgileri her yerde ve her zaman edinebilmenizi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Eldeki stok mobil çalışma alanı

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Eldeki stok mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, ayrılmış ve kullanılabilir stok hakkında mobil bilgileri her yerde ve her zaman edinebilmenizi sağlar.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Eldeki stok mobil çalışma alanına genel bakış
--------------------------------------------------

Genellikle, şirketler her gün birden fazla sevkiyata ve birden fazla stok girişine sahiptirler. Bu hareketler eldeki stok durumunu sürekli olarak değiştirir. **Eldeki stok** mobil çalışma alanı, şirketler arası eldeki stok durumunu görmenizi sağlar, böylece stok verisi hakkında en son bilgileri istediğiniz mobil cihazdan edinebilirsiniz. İster ambarda, satın almada, satışta, üretimde veya yönetimde çalışıyor isterseniz de başka bir role sahip olun, eldeki stok verisine her zaman ve her yerde erişebilirsiniz. 

Mobil çalışma alanı, eldeki durumun tesisler arasında anında görülmesine olanak sağlar. Tesisler arasında eldeki stoku, geçerli malzeme rezervasyonlarını ve rezerve edilmemiş eldeki stoku görüntülemenize olanak sağlar. Eldeki stoku sorgulamak için madde numaralarını da girebilir, eldeki ürünler ve çeşitleri için filtreli arama da yapabilirsiniz. 

Özellikle, mobil çalışma alanı bu özellikleri sağlar:

-   Ürün numarasına veya ürün adına göre arama yapabilir ve eldeki stok durumlarını görmek için ürünleri bulabilirsiniz.

-   Seçili ürünler için aşağıdaki bilgileri görüntüleyebilirsiniz:
    -   Siteye göre eldeki stok
    -   Ambara başına eldeki stok
    -   Konum başına eldeki stok
    -   Toplu iş başına eldeki stok (toplu iş denetimli ürünler için=
    -   Stok durumuna göre eldeki stok
    
-   Ürün eldeki stok aşağıdaki şekillerde gösterilir:
    -   Fiziksel stoka göre (Bu görünüm, toplam tutarı temsil eder.)
    -   Fiziksel ayrılana göre (Bu görünüm ayrılan tutarı temsil eder.)
    -   Kullanılabilir fiziksele göre (Bu görünüm, rezervasyonu olmayan tutarı temsil eder.)

## <a name="prerequisites"></a>Ön koşullar
**Eldeki stok** mobil çalışma alanını kullanmadan önce, sistem yöneticinizin aşağıdaki önkoşulları yerine getirdiğinden emin olun.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Rol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations sürüm 1611 platform güncelleştirmesi 3 veya daha sonraki sürümünün uygulanmış olması gerekir.</td>
<td>Sistem yöneticisi</td>
<td>Dynamics 365 for Operations'u kuruluşunuz için halihazırda dağıtılmadıysa, sistem yöneticisi <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Bir Microsoft Dynamics 365 for Operations demo ortamı dağıt</a>'ı görmelidir.</td>
</tr>
<tr class="even">
<td>KB 4013633 uygulanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td>KB 4013633 (bir X++ güncelleştirmesi veya meta veri düzeltmesi), tedarik zinciri yönetimi için dört mobil çalışma alanı içerir. KB 4013633 uygulamak için sistem yöneticiniz bu adımları atması gerekir:
<ol>
<li>KB 4013633'yi, Microsoft Lifecycle Services (LCS) üzerinden karşıdan yükleyin.</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi</a>, Dynamics 365 for Operations sisteminize uygulayın.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Eldeki stok</strong> mobil çalışma alanı, Dynamics 365 for Operations mobil uygulaması için yayınlanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td><ol>
<li>Dynamics 365 for Operations'ı tarayıcınızda başlatın.</li>
<li><strong>Sistem parametreleri</strong> sayfasında, <strong>Mobil çalışma alanlarını yönet</strong>'i seçin.</li>
<li><strong>Eldeki stok</strong> mobil çalışma alanını seçin.</li>
<li><strong>Mobil çalışma alanını yayınla</strong> üzerine tıklayın.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobil uygulamasını yükleyin ve kurun
Dynamics 365 for Operations mobil uygulamasını mobil uygulama mağazanızdan yükleyin ve kurun.

-   Android için: [Google Play Store'da Dynamics 365 for Operations](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone için: [iTunes apps mağazsında Dynamics 365 for Operations](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobil uygulamasına oturum açın
1.  Mobil cihazınızda uygulamayı başlatın.
2.  Dynamics 365 for Operations URL'nizi girin.
3.  Oturum açılacak şirketi girin. Örneğin **USMF** yazın.
4.  İlk defa oturum açtığınızda, Dynamics 365 for Operations hesabınızın kullanıcı adı ve parolasını girmeniz için uyarılırsınız. Kimlik bilgilerinizi girin.
5.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz. Sistem yöneticiniz daha sonra yeni bir çalışma alanı yayınlarsa, mobil çalışma alanlarının listesini yenilemek için çekebileceğinizi unutmayın. 

    [![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Bir ürün için eldeki stok miktarını, Eldeki stok mobil çalışma alanını kullanarak görüntüleyin
1.  Mobil cihazınızda **Eldeki stok** çalışma alanını seçin.
2.  **Bir maddenin eldeki durumunu kontrol et** seçeneğini işaretleyin. Çevrimdışı kullanım için uygulamanıza yüklenmiş ürünlerin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler daha fazla bilgi için şura bakmalıdır: [Dynamics 365 for Operations mobil platformuna](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)
3.  Maddeniz listede değilse, Dynamics 365 for Operations içerisinde bir çevrimiçi arama yapmak için **Daha fazla ara**'yı seçin. Ürün numarası ile arayın veya ürün adına göre aramaya geçin.
4.  Bir ürün seçin. Maddenin bir resmi varsa, resim gösterilir.
5.  Eldeki stokun durumunu görmek için aşağıdaki seçeneklerden birini seçin:
    -   Siteye göre eldekini görüntüle
    -   Ambara göre eldekini görüntüle
    -   Konuma göre eldekini görüntüle
    -   Toplu iş başına eldekini görüntüle (toplu iş denetimli ürünler için=
    -   Stok durumuna göre eldekini görüntüle

    Ürün eldeki stok aşağıdaki şekillerde gösterilir:
    -   Fiziksel stoka göre (Bu görünüm, toplam tutarı temsil eder.)
    -   Fiziksel ayrılana göre (Bu görünüm ayrılan tutarı temsil eder.)
    -   Kullanılabilir fiziksele göre (Bu görünüm, rezervasyonu olmayan kullanılabilir tutarı temsil eder.)






