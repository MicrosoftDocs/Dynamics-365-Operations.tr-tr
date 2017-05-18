---
title: "Microsoft Dynamics 365 for Operations uygulaması için proje zaman girişi"
description: "Bu konu, Proje zaman girişi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, kullanıcıların bir projeye karşı mobil cihazlarını kullanarak zaman girmelerini ve kaydetmelerine olanak sağlar."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Proje saati girişi mobil çalışma alanı

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Bu konu, Dynamics 365 for Operations mobil uygulaması için Proje zaman girişi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, kullanıcıların bir projeye karşı mobil cihazlarını kullanarak zaman girmelerini ve kaydetmelerine olanak sağlar.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Proje zaman girişi mobil çalışma alanına genel bakış
---------------------------------------------------

Proje kaynakları, günlük işlerinin parçası olarak çoğu zaman tesiste veya seyahattedirler. **Proje zaman girişi** mobil çalışma alanı, kullanıcıların projeye karşı faturalanabilir veya faturalanamayan zamanlarını istedikleri mobil cihazdan girmelerine izin verir. Bu nedenle, proje kaynakları zaman girişlerini herhangi bir zamanda ve herhangi bir yerde yapabilirler. Daha önceden kaydettikleri zaman girişlerini de görebilirler. 

Özellikle, **Proje zaman girişi** mobil çalışma alanı bu özellikleri sağlar:

-   Seçilen herhangi bir tarih için, belirli bir göreve harcadığınız saat sayısını girin.
-   Zaman girilecek projeyi bulmak için proje adı veya müşteriyi aratın.
-   Zaman harcadığınız kategori ve aktiviteyi belirtin.
-   Zamanı faturalanabilir veya faturalanamaz olarak kaydedin.
-   İsteğe bağlı olarak dahili veya harici açıklamalar girin.

**Proje zaman girişi** mobil çalışma alanını uygulamak için, bu konudaki aşağıdaki bölümlere bakın.

## <a name="prerequisites"></a>Ön koşullar
**Proje zaman girişi** mobil çalışma alanını uygulamadan önce, sistem yöneticinizin aşağıdaki önkoşulları tamamladığından emin olun.

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
<td>Dynamics 365 for Operations'u kuruluşunuz için halihazırda dağıtılmadıysa, sistem yöneticiniz <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Bir Microsoft Dynamics 365 for Operations demo ortamı dağıt</a>'ı görmelidir.</td>
</tr>
<tr class="even">
<td>KB 4018050 uygulanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td>KB 4018050, <strong>Proje zaman girişi</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. KB 4018050 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li>KB 4018050'yi, Microsoft Lifecycle Services (LCS) üzerinden karşıdan yükleyin.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Dağıtılabilir bir paket oluşturun</a> <strong>ApplicationSuite</strong> ve <strong>ProjectMobile</strong> modellerini içeren ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi</a>, Dynamics 365 for Operations sisteminize uygulayın.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Proje zaman girişi</strong> mobil çalışma alanı, Dynamics 365 for Operations mobil uygulaması için yayınlanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td><ol>
<li>Dynamics 365 for Operations'ı tarayıcınızda başlatın.</li>
<li><strong>Sistem parametreleri</strong> sayfası üzerinde, <strong>Mobil çalışma alanlarını yönet</strong> sekmesinde, <strong>Proje zaman girişi</strong> çalışma alanını seçin.</li>
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
5.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemek için çekebileceğinizi unutmayın.

[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Proje zaman girişi mobil çalışma alanını kullanarak zamanı girin
1.  Mobil cihazınızda **Proje zaman girişi** çalışma alanını seçin.
2.  **Zaman girişi**'ni seçin. Geçerli hafta için takvim tarihlerinizi görürsünüz.
3.  Seçilen bir tarih için **Eylemler** &gt; **Yeni giriş**'i seçin.
4.  Kaydedilecek saatlerin sayısını girin.
5.  Zaman girişi için projeyi seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş projelerin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler daha fazla bilgi için şura bakmalıdır: [Dynamics 365 for Operations mobil platformuna](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)
6.  Projeniz listede değilse, Dynamics 365 for Operations içerisinde bir çevrimiçi arama yapmak için **Ara**'yı seçin. Adına göre arama yapın veya proje adı veya müşteriye göre aramaya geçin.
7.  Bir kategori seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş kategorilerin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler daha fazla bilgi için şura bakmalıdır: [Dynamics 365 for Operations mobil platformuna](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)
8.  Kategoriniz listede değilse, Dynamics 365 for Operations içerisinde bir çevrimiçi arama yapmak için **Ara**'yı seçin. Kategoriye göre arama yapın veya kategori adına göre aramaya geçin.
9.  Bir faaliyet seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş faaliyetlerin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler daha fazla bilgi için şura bakmalıdır: [Dynamics 365 for Operations mobil platformuna](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)
10. Faaliyetiniz listede değilse, Dynamics 365 for Operations içerisinde bir çevrimiçi arama yapmak için **Ara**'yı seçin. Bir etkinlik numarasıyla arama yapın veya amaca göre aramaya geçin.
11. Satır özelliğini seçin.
12. İsteğe bağlı: Dahili ve harici açıklamalar girin.
13. **Tamam**'ı seçin.






