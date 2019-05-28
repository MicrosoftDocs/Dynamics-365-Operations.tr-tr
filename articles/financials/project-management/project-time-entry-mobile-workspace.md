---
title: Proje saati girişi mobil çalışma alanı
description: Bu konu, Proje zaman girişi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, kullanıcıların bir projeye karşı mobil cihazlarını kullanarak zaman girmelerini ve kaydetmelerine olanak sağlar.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: e671fe6e7c99bfb6d66f3b00560c3b0c404d2343
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545136"
---
# <a name="project-time-entry-mobile-workspace"></a>Proje saati girişi mobil çalışma alanı

[!include [banner](../includes/banner.md)]

Bu konu, **Proje saati girişi** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, kullanıcıların bir projeye karşı mobil cihazlarını kullanarak zaman girmelerini ve kaydetmelerine olanak sağlar.

Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations Mobile uygulaması ile kullanılmak üzere geliştirilmiştir. 

## <a name="overview"></a>Genel bakış
Proje kaynakları, günlük işlerinin parçası olarak çoğu zaman tesiste veya seyahattedirler. **Proje zaman girişi** mobil çalışma alanı, kullanıcıların projeye karşı faturalanabilir veya faturalanamayan zamanlarını istedikleri mobil cihazdan girmelerine izin verir. Bu nedenle, proje kaynakları zaman girişlerini herhangi bir zamanda ve herhangi bir yerde yapabilirler. Daha önceden kaydettikleri zaman girişlerini de görebilirler. 

Özellikle **Proje saati girişi** mobil çalışma alanında, kullanıcılar bu görevleri gerçekleştirebilir:

-   Seçilen herhangi bir tarih için, belirli bir göreve harcadığınız saat sayısını girin.
-   Zaman girilecek projeyi bulmak için proje adı veya müşteriyi aratın.
-   Zaman harcadığınız kategori ve aktiviteyi belirtin.
-   Zamanı faturalanabilir veya faturalanamaz olarak kaydedin.
-   İsteğe bağlı olarak dahili veya harici açıklamalar girin.

## <a name="prerequisites"></a>Önkoşullar
Önkoşullar, kuruluşunuza dağıtılan Microsoft Dynamics 365 sürümüne dayalı olarak farklılık gösterir.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Microsoft Dynamics 365 for Finance and Operations kullanıyorsanız önkoşullar
Microsoft Dynamics 365 for Finance and Operations kuruluşunuza dağıtıldıysa sistem yöneticisinin **Proje saati girişi** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Microsoft Dynamics 365 for Operations sürüm 1611'i platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar
Kuruluşunuza platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir. 

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

<td>KB 4018050 uygulayın.</td>
<td>Sistem yöneticisi</td>
<td>KB 4018050, <strong>Proje zaman girişi</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. KB 4018050 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Dağıtılabilir bir paket oluşturun</a> <strong>ApplicationSuite</strong> ve <strong>ProjectMobile</strong> modellerini içeren ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Proje saati girişi</strong> mobil çalışma alanını yayımlayın.</td>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Proje zaman girişi mobil çalışma alanını kullanarak zamanı girin
1.  Mobil cihazınızda **Proje zaman girişi** çalışma alanını seçin.
2.  **Zaman girişi**'ni seçin. Geçerli hafta için takvim tarihleri gösterilir.
3.  Seçilen bir tarih için **Eylemler** &gt; **Yeni giriş**'i seçin.
4.  Kaydedilecek saatlerin sayısını girin.
5.  Zaman girişi için projeyi seçin. Bir liste çevrimdışı kullanım için uygulamanıza yüklenmiş projeleri gösterir. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Projeniz listede yoksa, **Ara**'yı seçin. Adına göre arama yapın veya proje adı veya müşteriye göre aramaya geçin.
7.  Bir kategori seçin. Bir liste çevrimdışı kullanım için uygulamanıza yüklenmiş kategorileri gösterir. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Kategoriniz listede yoksa, **Ara**'yı seçin. Kategoriye göre arama yapın veya kategori adına göre aramaya geçin.
9.  Bir faaliyet seçin. Bir liste çevrimdışı kullanım için uygulamanıza yüklenmiş faaliyetleri gösterir. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Faaliyetiniz listede yoksa, **Ara**'yı seçin. Bir etkinlik numarasıyla arama yapın veya amaca göre aramaya geçin.

11. Satır özelliğini seçin.
12. İsteğe bağlı: Dahili ve harici açıklamalar girin.
13. **Tamam**'ı seçin.
