---
title: Satış siparişleri mobil çalışma alanı
description: Bu konu, Satış siparişleri mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, satış siparişleri konusunda her zaman ve her yerde güncel kalmanıza yardımcı olur.
author: Mirzaab
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 03e8908ecb78b4f72dae8426b0165f9350d5fe85
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "365075"
---
# <a name="sales-orders-mobile-workspace"></a>Satış siparişleri mobil çalışma alanı

[!include [banner](../includes/banner.md)]

Bu konu, **Satış siparişleri** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, satış siparişleri konusunda her zaman ve her yerde güncel kalmanıza yardımcı olur. 

Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations Mobile uygulaması ile kullanılmak üzere geliştirilmiştir.

## <a name="overview"></a>Genel bakış
**Satış siparişleri** mobil çalışma alanı her satış siparişi ile ilgili ayrıntılı bilgileri görüntülemenizi sağlar. Bu bilgi siparişin durumunu, müşteri için iletişim numarasını ve siparişi alanın iletişim numarasını içerir. **Satış siparişleri** mobil çalışma alanı, satış siparişlerinin anlık görünümünü sağlar. Müşteri bazında satış siparişlerini, tüm satış siparişlerini ya da belirli bir satış siparişiyle ilgili bilgileri görüntüleyebilirsiniz. 

Mobil çalışma alanı, satış siparişlerini derinlemesine çözümlemenize yardımcı olacak iki görünüm sağlar.

### <a name="view-all-sales-orders"></a>Tüm satış siparişlerini görüntüle
Bu görünüm tüm satış siparişlerini listeler.

-   Görüntülenecek satış siparişlerini seçmek için aşağıdaki filtrelerden birini kullanın:

    -   Satış siparişine göre ara
    -   Müşteri hesabına göre ara
    -   Müşteri adına göre ara
    -   Duruma göre ara
    -   Serbest bırakma durumuna göre ara
    -   Oluşturma tarih ve saatine göre ara
    
-   Satış siparişlerini seçtikten sonra belirli siparişlerin ayrıntılarını görüntüleyebilirsiniz. Özellikle aşağıdaki bilgileri görüntüleyebilirsiniz:

    -   Müşteri adı ve adres bilgileri
    -   Örneğin talep edilen sevk tarihi ve onaylanan sevk tarihi gibi satış siparişi için çeşitli tarihleri
    -   Sipariş alanın iletişim bilgileri
    -   Müşteri iletişim bilgileri
    -   Sipariş satırları
    -   Bir satış siparişinin nasıl ve ne zaman sevk edildiğini gösteren sevkiyatlar

### <a name="view-orders-for-a-customer"></a>Bir müşteri için siparişleri görüntüle
Bu görünüm, siparişleri müşteriye göre listeler.

-   Bir müşterinin siparişlerini görüntülemek için aşağıdaki filtrelerden birini kullanın:

    -   Ada göre ara
    -   Hesaba göre ara

-   Müşteri seçtikten sonra aşağıdaki bilgileri görüntüleyebilirsiniz:

    -   Müşteri adı ve grubu
    -   Müşteri iletişim bilgileri
    -   Müşteri satış siparişleri ve bu satış siparişleri hakkındaki ayrıntılar:
    
        -   Müşteri adı ve adres bilgileri
        -   Çeşitli satış siparişi tarihleri
        -   Sipariş alanın iletişim bilgileri
        -   Müşteri iletişim bilgileri
        -   Sipariş satırları
        -   Bir satış siparişinin nasıl ve ne zaman sevk edildiğini gösteren sevkiyatlar

## <a name="prerequisites"></a>Önkoşullar
Önkoşullar, kuruluşunuza dağıtılan Microsoft Dynamics 365 sürümüne dayalı olarak farklılık gösterir.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Microsoft Dynamics 365 for Finance and Operations kullanıyorsanız önkoşullar 
Eğer Dynamics 365 for Finance and Operations kuruluşunuza dağıtıldıysa sistem yöneticisinin **Satış siparişleri** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Dynamics 365 for Operations sürüm 1611'i platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar
Kuruluşunuza platform güncelleştirmesi 3 veya üzeri ile Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir. 

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

<td>KB 4013633, <strong>Satış siparişleri</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. KB 4013633 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Satış siparişleri</strong> mobil çalışma alanını yayımlayın.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin
Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:

-   [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
-   [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın

1.  Mobil cihazınızda uygulamayı başlatın.
2.  Dynamics 365 URL'nizi girin.
3.  İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.
4.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Bir müşteri için satış siparişi hakkındaki bilgileri, Satış siparişi mobil çalışma alanını kullanarak görüntüleyin

1.  Mobil cihazınızda **Satış siparişleri** çalışma alanını seçin.
2.  **Bir müşterinin siparişlerini görüntüle**'yi seçin.
3.  Müşteriyi bulmak için hesap veya müşteri adı bilgilerini kullanın.
4.  Müşteriyi seçin.
5.  **İletişim bilgileri**'ni veya **Satış siparişleri**'ni seçin. **Satış siparişleri** seçerseniz, müşterinin satış siparişlerinin listesi gösterilir.
6.  **Satış siparişi**'ni seçin. Şimdi satış siparişi satırları hakkında bilgileri, sevkiyatlar hakkındaki bilgileri, müşteri iletişim bilgilerini ve siparişi alan için iletişim bilgilerini görüntüleyebilirsiniz.
