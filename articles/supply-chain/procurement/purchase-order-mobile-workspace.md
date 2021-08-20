---
title: Satınalma siparişi onayı mobil çalışma
description: Bu konu satın alma siparişlerini görmenizi ve eylemler aracılığıyla yanıt vermenizi sağlayan Satınalma siparişi onayı mobil çalışma alanı hakkında bilgi sağlar. Örneğin, bir satınalma siparişini onaylayabilir veya reddedebilirsiniz.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8a1a9e62b542bfd46607da213225338354187e29caa94ba6e67f8c4ca38e5437
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781453"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Satınalma siparişi onayı mobil çalışma

[!include [banner](../includes/banner.md)]

Bu konu, **Satınalma siparişi onayı** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, satınalma siparişlerini görüntülemenizi ve bunları eylemleri kullanarak yanıtlamanızı sağlar. Örneğin, bir satınalma siparişini onaylayabilir veya reddedebilirsiniz.
 
## <a name="overview"></a>Özet 
Onay gerektiren satınalma siparişleri bir onay iş akışından geçer. İş akışı bir veya daha fazla kişinin eylem gerçekleştirmesini gerektiren çeşitli adımlar içerebilir. Örneğin, bir kişinin görevi tamamlaması veya satınalma siparişini onaylaması gerekebilir. 

**Satınalma siparişi onayı** mobil çalışma alanı satınalma siparişlerini mobil cihazınızdan kolaylıkla görmenizi ve yanıtlamanızı sağlar. Bu çalışma alanı, web istemcisinden alabileceğiniz aynı iş akışı eylemlerini almanıza da olanak tanır.

## <a name="prerequisites"></a>Önkoşullar
Önkoşullar, kuruluşunuza dağıtılan Supply Chain Management sürümüne göre değişiklik gösterir.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Management kullanıyorsanız önkoşullar 
Supply Chain Management kuruluşunuza dağıtıldıysa sistem yöneticisinin **Satınalma siparişi onayı** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Microsoft Dynamics 365 for Operations sürüm 1611'i Platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar
Kuruluşunuza Platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir. 

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
<td>KB 4017918 uygulayın.</td>
<td>Sistem yöneticisi</td>
<td>KB 4017918, <strong>Satınalma siparişi onayı</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. KB 4017918 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi uygulayın</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><strong>Satınalma siparişi onayı</strong> mobil çalışma alanını yayımlayın.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin
Finance and Operations mobil uygulamasını indirip yükleyin:

- [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
- [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın

1. Mobil cihazınızda uygulamayı başlatın.
2. Microsoft Dynamics 365 URL'nizi girin.
3. İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.
4. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

![Kullanılabilir çalışma alanları listesindeki satınalma siparişi onayı çalışma alanı.](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Size atanmış olan siparişleri görüntüleyin
1. Mobil cihazınızda **Satınalma siparişi onayı** çalışma alanını seçin.
2. Satınalma siparişi onayı çalışma alanında işlem yapmanız istenen tüm satınalma siparişlerini görüntülemek için **Bana atanan siparişler**'i seçin.
3. Bir sipariş seçin. **Sipariş ayrıntıları** sayfasında, sipariş başlığı bilgileri ve satırları görüntülenir. Ayrıca iş akışı görevinden gelen yönergeleri de bulabilirsiniz.
4. **Muhasebe dağılımları**'nı seçerek **Başlık muhasebe dağıtımları** sayfasını açın.
5. **Sipariş ayrıntıları** sayfasına dönün ve bir satır seçin. Sipariş satırı ayrıntılarından satıra özel muhasebe dağıtımlarını da keşfedebilirsiniz.

## <a name="complete-an-action-on-the-purchase-order"></a>Satınalma siparişinde bir eylemi tamamlama
Size atanan satınalma siparişini görüntüledikten ve iş akışı talimatlarını okuduktan sonra, işlem yapmaya hazır olmanız gerekir.

1. Mobil cihazınızda **Satınalma siparişi onayı** çalışma alanını seçin.
2. Satınalma siparişi onayı çalışma alanında işlem yapmanız istenen tüm satınalma siparişlerini görüntülemek için **Bana atanan siparişler**'i seçin.
3. Bir sipariş seçin ve ayrıntılar sayfasını görüntüleyin.
4. Kullanılabilir eylemleri görüntülemek için **Eylemler**'i seçin. Kullanılabilir eylemler size atanan göreve bağlıdır.

    | Görev eylemi    | Onay eylemi  |
    |----------------|------------------|
    | Tam       | Onayla          |
    | İade         | Reddet           |
    | İstek değişikliği | İstek değişikliği   |
    | Temsilci Seç       | Temsilci Seç         |

5. Uygun olan eylemi seçin.
6. **Görevi tamamla** sayfasında, bir açıklama girin. **Temsilci ata** eylemini seçerseniz, görevi atayacağınız bir temsilci seçmeniz gerekir.
7. **Tamam**'ı seçin. Çalışma alanını yeniledikten sonra satın alma siparişi artık listenizde olmayacaktır. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]