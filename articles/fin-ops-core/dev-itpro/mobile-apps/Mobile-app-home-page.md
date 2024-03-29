---
title: Mobil uygulama giriş sayfası
description: Bu makalede, finans ve operasyon (Dynamics 365) mobil uygulaması açıklanmakta ve bu uygulamayı kuruluşunuzda uygulamanıza yardımcı olabilecek kaynakların bağlantıları sunulmaktadır.
author: sericks007
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.custom: intro-internal
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.openlocfilehash: a0979df7c0cd685f810c0ab743fbede740e7aacb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284083"
---
# <a name="mobile-app-home-page"></a>Mobil uygulama giriş sayfası

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

Bu makalede **Finans ve operasyon (Dynamics 365)** mobil uygulaması açıklanmakta ve bu uygulamayı kuruluşunuzda uygulamanıza yardımcı olabilecek kaynakların bağlantıları sunulmaktadır.

## <a name="overview"></a>Genel bakış

Mobil uygulama, kuruluşunuzun iş süreçlerinin mobil cihazlarda kullanılabilir olmasını sağlar. BT yöneticiniz mobil çalışma alanları, kuruluşunuz için etkinleştirdikten sonra, kullanıcılar uygulamaya oturum açabilir ve iş süreçlerini mobil cihazlarından yürütmeye anında başlayabilirler. Mobil uygulama, verimliliği artıracak aşağıdaki özellikleri içerir:

- Kullanıcılar iş verilerini görebilir, düzenleyebilir ve bunlar üzerinde harekete geçebilirler, ağ bağlantıları kesintili olsa bile veya mobil cihazları tümüyle çevrimdışı olduğunda bile. Bir cihaz, ağ bağlantısını yeniden kurduğunda çevrimdışı veri operasyonları otomatik olarak eşitlenir.
- BT yöneticileri veya geliştiricileri, kuruluşunuz için özel hazırlanmış mobil çalışma alanları hazırlayabilir ve bunları yayınlayabilirler. Uygulama, var olan kod varlıklarınızı kullanır. Bu nedenle, doğrulama yordamlarınızı, iş mantığınızı veya güvenlik yapılandırmanızı yeniden uygulamak zorunda kalmazsınız.
- BT yöneticileri veya geliştiricileri, web istemcisi içinde dahil olan işaretle ve tıkla çalışma alanı tasarımcısını kullanarak kolayca tasarlayabilirler.
- BT yöneticileri veya geliştiricileri, İş mantığı genişletilebilme çerçevesini kullanarak çalışma alanlarının kabiliyetlerini isteğe bağlı olarak optimize edebilirler. Cihaz çevrimdışıyken de veri işlenmeye devam ettiği için cihazlarınız sürekli internet bağlantısına sahip olmasa bile mobil senaryolarınız zengin ve akıcı kalır.

## <a name="elements-of-the-mobile-app"></a>Mobil uygulamanın öğeleri
Mobil uygulamadaki gezinti, dört temel kavramdan oluşur: Pano, çalışma alanları, sayfalar ve eylemler. 

[![Mobil uygulamadaki gezinme kavramları.](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Uygulamayı başlattığınızda **pano**'ya gidersiniz.
2. Panoda, yayımlanmış olan **çalışma alanlarının** bir listesini görebilirsiniz.
3. Her bir çalışma alanında, o çalışma alanı için kullanılabilen **sayfalar**'ın bir listesini görürsünüz.
4. Sayfaya ulaştıktan sonra, bir dizi eylem gerçekleştirebilirsiniz. Burada bazı örnekler verilmiştir:

    - Ayrıntılı veriyi görüntüle.
    - ilgili veri için diğer sayfalara gezinebilirsiniz, örneğin varlık ayrıntıları veya satırlar.
    - O sayfa için kullanılabilir olan **eylemlerin** bir listesini görüntüle. Eylemler veri oluşturmanıza veya mevcut veriyi düzenlemenize olanak tanır.

## <a name="implementation-process"></a>Uygulama işlemi
Aşağıdaki görsel, Microsoft tarafından sağlanan ve özel mobil çalışma alanlarının her ikisinin de uygulama işlemini gösterir. 

[![Mobil uygulamalar uygulama süreci.](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

Aşağıdaki tablo, Microsoft ve özel mobil çalışma alanlarından sağlanan her iki mobil çalışma alanını uygulamanıza yardımcı olacak kaynaklara bağlantılar içerir. İlk sütundaki sayılar, önceki görseldeki numaralandırılmış adımlara karşılık gelir.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Aşama</th>
<th>Rol</th>
<th>Eylem</th>
<th>Eylemi tamamlamanıza yardımcı olacak kaynaklar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Sistem yöneticisi</td>
<td>Kuruluşunuzda finans ve operasyon uygulamasını uygulayın.</td>
<td><ul><li>Henüz bir Microsoft Dynamics 365 sürümünü dağıtmadıysanız, bkz. <a href="../deployment/deploy-demo-environment.md">Bir gösteri sürümü dağıtmak</a>.</li><li>Kullanılabilir mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Yakın zamanda yayımlanmış olan mobil çalışma alanları</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Sistem yöneticisi</td>
<td><strong>Microsoft Dynamics 365 for Operations sürüm 1611 kullanıyorsanız:</strong> Microsoft tarafından sağlanan mobil çalışma alanlarını etkinleştiren BB'leri indirin ve yükleyin.</td>
<td>Daha fazla bilgi için aşağıdaki konulara göz atın:
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobil çalışma alanlarının maliyet kontrolü</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Eldeki stok mobil çalışma alanı</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Satış siparişleri mobil çalışma alanları</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Satıcı iş birliği mobil çalışma alanı</a></li>
<li><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Proje saati girişi mobil çalışma alanı</a></li>
<li><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Gider yönetimi mobil çalışma alanı</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Sistem yöneticisi</td>
<td>Microsoft tarafından sağlanan mobil çalışma alanlarını yayınlayın.</td>
<td><a href="publish-mobile-workspace.md">Bir mobil çalışma alanı yayınlayın</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Geliştirici veya bağımsız yazılım satıcısı (ISV)</td>
<td>Mobil platformu, özel mobil çalışma alanları oluşturmak için kullanın.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobil platform</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Özel mobil çalışma alanları içeren bir dağıtılabilir paket oluşturun ve paketi Microsoft Dynamics Lifecycle Services'a (LCS) yükleyin.</td>
<td><a href="../deployment/create-apply-deployable-package.md">Dağıtılabilir paket oluşturma</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Sistem yöneticisi</td>
<td>Bağımsız yazılım satıcısı (ISV) tarafından sağlanan özel çalışma alanlarını içeren dağıtılabilir paketi uygulayın.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Dağıtılabilir paket uygulama</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Sistem yöneticisi</td>
<td>ISV tarafından sağlanan özel mobil çalışma alanlarını yayınlayın.</td>
<td><a href="publish-mobile-workspace.md">Mobil çalışma alanı yayımlama</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Kullanıcı</td>
<td>Mobil uygulamayı indirin ve yükleyin.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Android için finans ve operasyon uygulaması</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">iOS için finans ve operasyon uygulaması</a><BR/>
(Windows Phone desteklenmemektedir)
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Kullanıcı</td>
<td>Oturum açın ve mobil uygulamayı kullanın. Uygulama, sistem yöneticisi tarafından yayınlanan mobil çalışma alanlarını içerir.</td>
<td>Microsoft tarafından sağlanan mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Yakın zamanda yayımlanmış olan mobil çalışma alanları</a>.
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a>Sorun Giderme
[Mobil platform kaynakları](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

