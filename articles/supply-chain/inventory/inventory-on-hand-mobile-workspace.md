---
title: Eldeki stok mobil çalışma alanı
description: Bu konu, Eldeki stok mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, ayrılmış ve kullanılabilir stok hakkında mobil bilgileri her yerde ve her zaman edinebilmenizi sağlar.
author: yufeihuang
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yufeihuang
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b380da99b02fe9b7cd834eabac3498ee3b8e54a4
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811480"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Eldeki stok mobil çalışma alanı

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Bu konu, **Eldeki stok** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, ayrılmış ve kullanılabilir stok hakkında bilgileri her yerde ve her zaman edinebilmenizi sağlar.

Bu mobil çalışma alanı, Finance and Operations (Dynamics 365) mobil uygulaması ile kullanılmak üzere tasarlanmıştır.

## <a name="overview"></a>Genel Bakış
Genellikle, şirketler her gün birden fazla sevkiyata ve birden fazla stok girişine sahiptirler. Bu hareketler eldeki stok durumunu sürekli olarak değiştirir. **Eldeki stok** mobil çalışma alanı, şirketler arası eldeki stok durumunu görmenizi sağlar, böylece stok verisi hakkında en son bilgileri istediğiniz mobil cihazdan edinebilirsiniz. İster ambarda, satın almada, satışta, üretimde veya yönetimde çalışıyor isterseniz de başka bir role sahip olun, eldeki stok verisine her zaman ve her yerde erişebilirsiniz. 

Mobil çalışma alanı, eldeki durumun tesisler arasında anında görülmesine olanak sağlar. Tesisler arasında eldeki stoku, geçerli malzeme rezervasyonlarını ve rezerve edilmemiş eldeki stoku görüntülemenize olanak sağlar. Eldeki stoku sorgulamak için madde numaralarını da girebilir, eldeki ürünler ve çeşitleri için filtreli arama da yapabilirsiniz. 

Özellikle, mobil çalışma alanı bu özellikleri sağlar:

-   Ürün numarasına veya ürün adına göre arama yapabilir ve eldeki stok durumlarını görmek için ürünleri bulabilirsiniz.
-   Seçili ürünler için aşağıdaki bilgileri görüntüleyebilirsiniz:

    -   Siteye göre eldeki stok
    -   Ambara başına eldeki stok
    -   Konum başına eldeki stok
    -   Toplu iş başına eldeki stok (toplu iş denetimli ürünler için)
    -   Stok durumuna göre eldeki stok
    
-   Ürün eldeki stok aşağıdaki şekillerde gösterilir:

    -   Fiziksel stoka göre (Bu görünüm, toplam tutarı temsil eder.)
    -   Fiziksel ayrılana göre (Bu görünüm ayrılan tutarı temsil eder.)
    -   Kullanılabilir fiziksele göre (Bu görünüm, rezervasyonu olmayan tutarı temsil eder.)

## <a name="prerequisites"></a>Önkoşullar
Önkoşullar, kuruluşunuz için dağıtılan Supply Chain Management sürümüne göre değişiklik gösterir.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Management kullanıyorsanız önkoşullar
Supply Chain Management, kuruluşunuza dağıtıldıysa sistem yöneticisinin **Eldeki stok** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar 
Kuruluşunuza Platform güncelleştirmesi 3 veya üzeri dağıtıldıysa sistem yöneticisinin aşağıdaki önkoşulları yerine getirmesi gerekir. 

<table>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Rol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 4013633 uygulayın.</td>
<td>Sistem yöneticisi</td>

<td>KB 4013633, <strong>Eldeki stok</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. KB 4013633 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi uygulayın</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Eldeki stok mobil çalışma alanı</strong> mobil çalışma alanını yayımla.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin

Finance and Operations (Dynamics 365 ) mobil uygulamasını indirin ve yükleyin:

-   [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
-   [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın

1.  Mobil cihazınızda uygulamayı başlatın.
2.  Dynamics 365 URL'nizi girin.
3.  İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.
4.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

    [![Yenilemek için çekin.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Bir ürün için eldeki stok miktarını, Eldeki stok mobil çalışma alanını kullanarak görüntüleyin

1.  Mobil cihazınızda **Eldeki stok** çalışma alanını seçin.

2.  **Bir maddenin eldeki durumunu kontrol et** seçeneğini işaretleyin. Çevrimdışı kullanım için uygulamanıza yüklenmiş ürünlerin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Maddeniz listede yoksa, **Daha fazla ara**'yı seçin. Ürün numarası ile arayın veya ürün adına göre aramaya geçin.

4.  Bir ürün seçin. Maddenin bir resmi varsa, resim gösterilir.
5.  Eldeki stokun durumunu görmek için aşağıdaki seçeneklerden birini seçin:

    -   Siteye göre eldekini görüntüle
    -   Ambara göre eldekini görüntüle
    -   Konuma göre eldekini görüntüle
    -   Toplu iş başına eldekini görüntüle (toplu iş denetimli ürünler için)
    -   Stok durumuna göre eldekini görüntüle

    Ürün eldeki stok aşağıdaki şekillerde gösterilir:
    -   Fiziksel stoka göre (Bu görünüm, toplam tutarı temsil eder.)
    -   Fiziksel ayrılana göre (Bu görünüm ayrılan tutarı temsil eder.)
    -   Kullanılabilir fiziksele göre (Bu görünüm, rezervasyonu olmayan kullanılabilir tutarı temsil eder.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
