---
title: "Satış siparişleri mobil çalışma alanı"
description: "Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Satış siparişleri mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, satış siparişleriyle her zaman ve her yerde güncel kalmanıza yardımcı olur."
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
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11898146a13756a6bb22a769e37e8773484e0d04
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Satış siparişleri mobil çalışma alanı

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Satış siparişleri mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, satış siparişleriyle her zaman ve her yerde güncel kalmanıza yardımcı olur. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Satış siparişleri mobil çalışma alanına genel bakış
---------------------------------------------

**Satış siparişleri** mobil çalışma alanı, Microsoft Dynamics 365 for Operations'a erişir ve her bir satış siparişi hakkında ayrıntılı bilgi edinmenizi sağlar. Bu bilgi siparişin durumunu, müşteri için iletişim numarasını ve siparişi alanın iletişim numarasını içerir. **Satış siparişleri** mobil çalışma alanı, satış siparişlerinin anlık görünümünü sağlar. Müşteri bazında satış siparişlerini, tüm satış siparişlerini ya da belirli bir satış siparişiyle ilgili bilgileri görüntüleyebilirsiniz. 

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

## <a name="prerequisites"></a>Ön koşullar
**Satış siparişleri** mobil çalışma alanını kullanmadan önce, sistem yöneticinizin aşağıdaki önkoşulları yerine getirdiğinden emin olun.

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
<td>Dynamics 365 for Operations sürüm 1611 platform güncelleştirmesi 3 veya daha sonraki sürümünün uygulanmış olması gerekir.</td>
<td>Sistem yöneticisi</td>
<td>Dynamics 365 for Operations'u kuruluşunuz için halihazırda dağıtılmadıysa, sistem yöneticisi <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment/">Bir Microsoft Dynamics 365 for Operations demo ortamı dağıt</a>'ı görmelidir.</td>
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
<td><strong>Satış siparişleri</strong> mobil çalışma alanı, Dynamics 365 for Operations mobil uygulaması için yayınlanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td><ol>
<li>Dynamics 365 for Operations'ı tarayıcınızda başlatın.</li>
<li><strong>Sistem parametreleri</strong> sayfasında, <strong>Mobil çalışma alanlarını yönet</strong>'i seçin.</li>
<li><strong>Satış siparişleri</strong> çalışma alanını seçin.</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Bir müşteri için satış siparişi hakkında bilgiyi, mobil çalışma alanını kullanarak görüntüleyin
1.  Mobil cihazınızda **Satış siparişleri** çalışma alanını seçin.
2.  **Bir müşterinin siparişlerini görüntüle**'yi seçin.
3.  Müşteriyi bulmak için hesap veya müşteri adı bilgilerini kullanın.
4.  Müşteriyi seçin.
5.  **İletişim bilgileri**'ni veya **Satış siparişleri**'ni seçin. **Satış siparişleri** seçerseniz, müşterinin satış siparişlerinin listesi gösterilir.
6.  **Satış siparişi**'ni seçin. Şimdi satış siparişi satırları hakkında bilgileri, sevkiyatlar hakkındaki bilgileri, müşteri iletişim bilgilerini ve siparişi alan için iletişim bilgilerini görüntüleyebilirsiniz.





