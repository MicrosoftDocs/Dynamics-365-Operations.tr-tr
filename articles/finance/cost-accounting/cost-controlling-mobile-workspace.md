---
title: Mobil çalışma alanının maliyet denetimi
description: Bu makalede, Maliyet kontrolü mobil çalışma alanı hakkında bilgi sağlanmaktadır. Bu çalışma alanı, maliyet merkezi yöneticilerinin maliyet merkezi performansı hakkındaki bilgileri her zaman ve her yerde görebilmelerini sağlar.
author: AndersGirke
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d6d3fdcc0b0387a92f138b0ba7cf537f473b91a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069578"
---
# <a name="cost-controlling-mobile-workspace"></a>Mobil çalışma alanının maliyet denetimi

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Bu makalede, **Maliyet kontrolü** mobil çalışma alanı hakkında bilgi sağlanmaktadır. Bu çalışma alanı, maliyet merkezi yöneticilerinin maliyet merkezi performansı hakkındaki bilgileri her zaman ve her yerde görebilmelerini sağlar.

Bu mobil çalışma alanı, finans ve operasyon (Dynamics 365) mobil uygulaması ile kullanılmak üzere tasarlanmıştır.

## <a name="overview"></a>Genel Bakış
**Maliyet denetleme** mobil çalışma alanı, maliyet merkezlerinin mevcut performansı hakkında anında bilgiyi, ffili maliyetleri, bütçelendirilmiş maliyete kıyaslayarak sağlar. Tekil maliyet öğelerinin durumunun detayına inebilirsiniz.

Örneğin, bir personel uluslararası bir konferansa davetiye almıştır ancak kuruluşun tüm seyahat masraflarını üstlenmesi gerekir. Personel, yöneticisine konferansa katılıp katılamayacağını sorar. Yönetici, personelin konferansa katılması için bütçenin olup olmadığını görmek için mobil cihazında **Maliyet denetimi** mobil çalışma alanını açar.

### <a name="data-security"></a>Veri güvenliği
**Maliyet denetimi** mobil çalışma alanındaki veriler, kullanıcı kimlik bilgileriyle güvenlik altına alınır. Maliyet merkezi yöneticilerinin yalnızca kendi maliyet merkezleri için verileri görmelerine izin verilir. Erişim düzeyi güvenliği **Maliyet muhasebesi** modülünde yönetilir.

Maliyet muhasebecileri, **Maliyet muhasebesi** modülünde **Maliyet denetimi** mobil çalışma alanının yapılandırmasını tanımlar. Çalışma alanı mobil uygulamada yayımlandıktan sonra, uygulamada kullanılabilir. Bu sayede, kuruluşunuzdaki tüm maliyet merkezi yöneticilerinin aynı biçimdeki veriyi görüntüleyebilirler.

### <a name="actions-views-and-links"></a>Eylemler, görünümler ve bağlantılar
**Maliyet denetleme** mobil çalışma alanı aşağıdaki eylemleri, görünümleri ve bağlantıları sağlar:

-   **Eylemler:**

    -   Düzeni seçmek için **Yapılandırmayı seç**'i kullanın.
    -   **Maliyet nesnesini seç**'i, verinin filtreleneceği maliyet merkezini seçmek için kullanın.
    
        > [!NOTE]
        > Listede görünen maliyet merkezleri, **Maliyet muhasebesi** modülünde verilmiş olan erişime bağlıdır.

-   **Görünümler:** **Maliyet muhasebesi** modülünün yapılandırmasında seçilen eylemlere dayanarak, kartlarda aşağıdaki bilgileri görüntüleyebilirsiniz:

    -   Gerçek tutar ile bütçe karşılaştırması (geçerli dönem)
    -   Gerçek tutar ile düzeltilmiş bütçe karşılaştırması (geçerli dönem)
    -   Fiili - bütçe (önceki dönem) karşılaştırması
    -   Fiili - revize edilmiş bütçe (önceki dönem) karşılaştırması
    -   Fiili - bütçe (günümüze kadar yıl) karşılaştırması
    -   Fiili - revize edilmiş bütçe (günümüze kadar yıl) karşılaştırması

    Şu tutarlar tüm kartlarda gösterilir: Fiili, Bütçe, Fark ve Fark Yüzdesi.

-   **Bağlantılar:**

    -   Geçerli dönem için ayrıntılar
    -   Önceki dönem için ayrıntılar
    -   Yıl başından bu güne için ayrıntılar

    Bir bağlantıyı seçtiğinizde, her bir maliyet öğesi için bir kart gösterilir. Her kart için aşağıdaki tutarlar gösterilir: Fiili, Bütçe, Bütçe farkı, Bütçe farkı yüzdesi, Revize edilmiş bütçe, Revize edilmiş bütçe farkı ve Revize edilmiş bütçe farkı yüzdesi.
    
    [![Bir maliyet öğesi için kart.](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Önkoşullar
Önkoşullar, kuruluşunuza dağıtılan Microsoft Dynamics 365 sürümüne dayalı olarak farklılık gösterir.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Microsoft Dynamics 365 Finance'i kullanıyorsanız önkoşullar
Finance kuruluşunuza dağıtıldıysa sistem yöneticisinin **Maliyet kontrolü** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Sürüm 1611'i Platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar
Kuruluşunuza Platform güncelleştirmesi 3 veya üzeri ile 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir.

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
<td>BB 4013633 uygulayın.</td>
<td>Sistem yöneticisi</td>

<td>BB 4013633, <strong>Maliyet denetleme</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. BB 4013633 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi uygulayın</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Maliyet denetleme</strong> mobil çalışma alanını yayımlayın.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin
Finans ve operasyon (Dynamics 365) mobil uygulamasını indirin ve yükleyin:

-   [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
-   [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın

1.  Mobil cihazınızda uygulamayı başlatın.
2.  Dynamics 365 URL'nizi girin.
3.  İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.
4.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

[![Yenilemek için çekin.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Maliyet merkezinizin performansını Maliyet denetimi mobil çalışma alanını kullanarak görüntüleyin

1.  Mobil cihazınızda **Maliyet denetleme** çalışma alanını seçin.
2.  **Maliyet nesnesi denetleme** seçeneğini işaretleyin.
3.  **Eylemler**'i seçin.
4.  **Yapılandırma seç**'i seçerek bir maliyet denetleme biçimi seçin.
5.  **Tamam**'ı seçin.
6.  **Eylemler**'i seçin.
7.  **Maliyet nesnesi seç**'i seçerek erişiminizin sağlandığı maliyet merkezlerini seçin.
8.  **Tamam**'ı seçin.
9.  Maliyet merkezinizin toplam performansını görün.
10. **Geçerli dönem için ayrıntılar** bağlantısını seçin.
11. Bireysel maliyet öğelerinin performansını görün.
12. Belirli maliyet öğeleri için de arama yapabilirsiniz.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

