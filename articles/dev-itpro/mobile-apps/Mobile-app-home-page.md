---
title: "Mobil uygulama giriş sayfası"
description: "Bu konu, Microsoft Dynamics 365 for Unified Operations mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 08dcdf2f5c03de17d50910e617d20e734e6ee31e
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="mobile-app-home-page"></a>Mobil uygulama giriş sayfası

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Unified Operations mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar.

> [!NOTE]
> Mobil uygulamanın adı daha önce *Microsoft Dynamics 365 for Finance and Operations* idi.

<a name="overview"></a>Özet
--------

Mobil uygulama, kuruluşunuzun iş süreçlerinin mobil cihazlarda kullanılabilir olmasını sağlar. BT yöneticiniz mobil çalışma alanları, kuruluşunuz için etkinleştirdikten sonra, kullanıcılar uygulamaya oturum açabilir ve iş süreçlerini mobil cihazlarından yürütmeye anında başlayabilirler. Mobil uygulama, verimliliği artıracak aşağıdaki özellikleri içerir:

- Kullanıcılar iş verilerini görebilir, düzenleyebilir ve bunlar üzerinde harekete geçebilirler, ağ bağlantıları kesintili olsa bile veya mobil cihazları tümüyle çevrimdışı olduğunda bile. Bir cihaz ağ bağlantısını tekrar kurduktan sonra, çevrimdışı veri işlemleri, Dynamics 365 for Finance and Operations, Enterprise edition veya Microsoft Dynamics 365 for Finance and Operations ile otomatik eşitlenir.
- BT yöneticileri veya geliştiricileri, kuruluşunuz için özel hazırlanmış mobil çalışma alanları hazırlayabilir ve bunları yayınlayabilirler. Uygulama, varolan kod varlıklarınızı kullanır. Bu nedenle, doğrulama yordamlarınızı, iş mantığınızı veya güvenlik yapılandırmanızı yeniden uygulamak zorunda kalmazsınız.
- BT yöneticileri veya geliştiricileri, web istemcisi içinde dahil olan işaretle ve tıkla çalışma alanı tasarımcısını kullanarak kolayca tasarlayabilirler.
- BT yöneticileri veya geliştiricileri, İş mantığı genişletilebilme çerçevesini kullanarak çalışma alanlarının kabiliyetlerini isteğe bağlı olarak optimize edebilirler. Cihaz çevrimdışıyken de veri işlenmeye devam ettiği için cihazlarınız sürekli internet bağlantısına sahip olmasa bile mobil senaryolarınız zengin ve akıcı kalır.

## <a name="elements-of-the-mobile-app"></a>Mobil uygulamanın öğeleri
Mobil uygulamadaki gezinti, dört temel kavramdan oluşur: Pano, çalışma alanları, sayfalar ve eylemler. 

[![Mobil uygulamadaki gezinme kavramları](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Uygulamayı başlattığınızda **pano**'ya gidersiniz.
2. Panoda, yayımlanmış olan **çalışma alanlarının** bir listesini görebilirsiniz.
3. Her bir çalışma alanında, o çalışma alanı için kullanılabilen **sayfalar**'ın bir listesini görürsünüz.
4. Sayfaya ulaştıktan sonra, bir dizi eylem gerçekleştirebilirsiniz. Burada bazı örnekler verilmiştir:

    - Ayrıntılı veriyi görüntüle.
    - ilgili veri için diğer sayfalara gezinebilirsiniz, örneğin varlık ayrıntıları veya satırlar.
    - O sayfa için kullanılabilir olan **eylemlerin** bir listesini görüntüle. Eylemler veri oluşturmanıza veya mevcut veriyi düzenlemenize olanak tanır.

## <a name="implementation-process"></a>Uygulama işlemi
Aşağıdaki görsel, Microsoft tarafından sağlanan ve özel mobil çalışma alanlarının her ikisinin de uygulama işlemini gösterir. 

![Mobil uygulamalar uygulama süreci](./media/Mobile-implementation-process-5.png)

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
<td>Kuruluşunuzda Finance and Operations veya Finance and Operations'ı uygulayın.</td>
<td><ul><li>Henüz bir Microsoft Dynamics 365 sürümünü dağıtmadıysanız, bkz. <a href="../deployment/deploy-demo-environment.md">Bir gösteri sürümü dağıtmak</a>.</li><li>Kullanılabilir mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Yakın zamanda yayımlanmış olan mobil çalışma alanları</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Sistem yöneticisi</td>
<td><strong>Microsoft Dynamics 365 for Finance and Operations sürüm 1611 kullanıyorsanız:</strong> Microsoft tarafından sağlanan mobil çalışma alanlarını etkinleştiren KB'leri indir ve yükleyin.</td>
<td>Daha fazla bilgi için aşağıdaki konulara göz atın:
<ul>

<li><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Mobil çalışma alanlarının maliyet kontrolü</a></li>
<li><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Eldeki stok mobil çalışma alanı</a></li>
<li><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Satış siparişleri mobil çalışma alanları</a></li>
<li><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Satıcı işbirliği mobil çalışma alanı</a></li>
<li><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Proje saati girişi mobil çalışma alanı</a></li>
<li><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Gider yönetimi mobil çalışma alanı</a></li>

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
<td><a href="../deployment/create-apply-deployable-package.md">Dağıtılabilir paket oluşturun</a></td>
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
<td><a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Kullanıcı</td>
<td>Mobil uygulamayı indirin ve yükleyin.</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">Android telefonlar için</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">iPhone'lar için</a></li></ul>
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

