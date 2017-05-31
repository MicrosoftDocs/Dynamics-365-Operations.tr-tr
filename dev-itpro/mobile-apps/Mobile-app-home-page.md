---
title: "Dynamics 365 for Operations mobil uygulama giriş sayfası"
description: "Bu konu, Microsoft Dynamics 365 for Operations mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5962fa36b061382e7f0ad55c08c81ac2cebc047d
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Dynamics 365 for Operations mobil uygulama giriş sayfası

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Operations mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar.

<a name="overview"></a>Özet
--------

Microsoft Dynamics 365 for Operations mobil uygulaması, kuruluşunuzun iş süreçlerinin mobil cihazlarda kullanılabilir olmasını sağlar. BT yöneticiniz mobil çalışma alanları özelliğini kuruluşunuz için etkinleştirdikten sonra, kullanıcılar uygulamaya oturum açabilir ve iş süreçlerini mobil cihazlarından yürütmeye anında başlayabilirler. Dynamics 365 for Operations mobil uygulaması, verimliliği artıracak aşağıdaki özellikleri içerir:

-   Kullanıcılar iş verilerini görebilir, düzenleyebilir ve bunlar üzerinde harekete geçebilirler, ağ bağlantıları kesintili olsa bile veya mobil cihazları tümüyle çevrimdışı olduğunda bile. Bir cihaz ağ bağlantısını yeniden kurduğunda, çevrimdışı veri operasyonları Dynamics 365 for Operations ile otomatik olarak eşitlenir.
-   BT yöneticileri veya geliştiricileri, kuruluşunuz için özel hazırlanmış mobil çalışma alanları hazırlayabilir ve bunları yayınlayabilirler. Uygulama, varolan kod varlıklarınızı kullanır. Bu nedenle, doğrulama yordamlarınızı, iş mantığınızı veya güvenlik yapılandırmanızı yeniden uygulamak zorunda kalmazsınız.
-   BT yöneticileri veya geliştiricileri, Dynamics 365 for Operations web istemcisi içinde dahil olan işaretle ve tıkla çalışma alanı tasarımcısını kullanarak kolayca tasarlayabilirler.
-   BT yöneticileri veya geliştiricileri, İş mantığı genişletilebilme çerçevesini kullanarak çalışma alanlarının kabiliyetlerini isteğe bağlı olarak optimize edebilirler. Cihaz çevrimdışıyken de veri işlenmeye devam ettiği için cihazlarınız sürekli internet bağlantısına sahip olmasa bile mobil senaryolarınız zengin ve akıcı kalır.

## <a name="elements-of-the-mobile-app"></a>Mobil uygulamanın öğeleri
Mobil uygulamadaki gezinti, dört basit kavramdan oluşur: Pano, çalışma alanları, sayfalar ve eylemler. 

[![Mobil uygulamadaki gezinme kavramları](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Uygulamayı başlattığınızda **pano**'ya gidersiniz.
-   Panoda, Dynamics 365 for Operations ortamınız için yayımlanmış **çalışma alanları**'nın bir listesini görürsünüz.
-   Her bir çalışma alanında, o çalışma alanı için kullanılabilen **sayfalar**'ın bir listesini görürsünüz.
-   Bir sayfada, Dynamics 365 for Operations içindeki bir veya birden fazla sayfadan toplanan verileri görürsünüz.
-   Bir sayfadan, ilgili veri için diğer sayfalara gezinebilirsiniz, örneğin varlık ayrıntıları veya satırlar.
-   Bir sayfada, bu sayfa için kullanılabilen **eylemler**'in bir listesini de görebilirsiniz.
-   Eylemler veri oluşturmanıza veya mevcut veriyi düzenlemenize olanak tanır.

## <a name="implementation-process"></a>Uygulama işlemi
Aşağıdaki görsel, Dynamics 365 for Operations mobil uygulamasını kuruluşunuzda uygulama sürecini göstermektedir. 

![Mobil uygulamalar uygulama süreci](./media/mobile-implementation-process_4.png)

Aşağıdaki tablo, Dynamics 365 for Operations mobil uygulamasını kuruluşunuza uygulamaya yardımcı olacak kaynaklara bağlantılar içerir. İlk sütundaki sayılar, önceki görseldeki numaralandırılmış adımlara karşılık gelir.

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
<td>Kuruluşunuz için Dynamics 365 for Operations uygulama.</td>
<td>Dynamics 365 for Operations'u kuruluşunuz için halihazırda dağıtılmadıysa, bakınız <a href="../deployment/deploy-demo-environment.md">Bir Microsoft Dynamics 365 for Operations demo ortamı dağıt</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Sistem yöneticisi</td>
<td>Microsoft tarafından sağlanan mobil çalışma alanlarını etkinleştiren KB'leri yükleyin ve kurun.</td>
<td>Kuruluşunuzun kullanmak istediği mobil çalışma alanları hakkındaki konudaki &quot;Önkoşullar&quot; bölümüne göz atın.
<ul>
<li><a href="/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobil çalışma alanlarının maliyet kontrolü</a></li>
<li><a href="/dynamics365/operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Eldeki stok mobil çalışma alanı</a></li>
<li><a href="/dynamics365/operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Satış siparişleri mobil çalışma alanları</a></li>
<li><a href="/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Satıcı iş birliği mobil çalışma alanı</a></li>
<li><a href="/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Proje saati girişi mobil çalışma alanı</a></li>
<li><a href="/dynamics365/operations/financials/expense-management/expense-management-mobile-workspace">Mobil çalışma alanında gider yönetimi</a></li>
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
<td>Dynamics 365 for Operations mobil çerçevesini, özel mobil çalışma alanları oluşturmak için kullanın.</td>
<td><ul>
<li><a href="mobile-platform.md">Dynamics 365 for Operations mobil çerçevesi</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Dynamics 365 for Operations çalışma alanları X++ API'leri</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Özel mobil çalışma alanları içeren bir dağıtılabilir paket oluşturun ve paketi Microsoft Dynamics Lifecycle Services'a (LCS) yükleyin.</td>
<td><a href="../deployment/create-apply-deployable-package.md">Dağıtılabilir paket oluşturun</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Sistem yöneticisi</td>
<td>ISV tarafından sağlanan özel çalışma alanlarını içeren dağıtılabilir paketi uygulayın.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Bir Microsoft Dynamics 365 for Operations sistemine bir dağıtılabilir paket uygulayın</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Sistem yöneticisi</td>
<td>ISV tarafından sağlanan özel mobil çalışma alanlarını yayınlayın.</td>
<td><a href="publish-mobile-workspace.md">Bir mobil çalışma alanı yayınlayın</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Kullanıcı</td>
<td>Dynamics 365 for Operations mobil uygulamasını yükleyin ve kurun.</td>
<td><ul>
<li>Android için: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Google Play Store'da Dynamics 365 for Operations</a></li>
<li>iPhone için: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">iTunes apps mağazsında Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Kullanıcı</td>
<td>Oturum açın ve Dynamics 365 for Operations mobil uygulamasını kullanın. Uygulama, yayınlanan mobil çalışma alanlarını içerir.</td>
<td>Microsoft tarafından sağlanan mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Dynamics 365 for Operations mobil uygulaması için son yayınlanan mobil çalışma alanları</a>
</td>
</tr>
</tbody>
</table>






