---
title: "Mobil çalışma alanında gider yönetimi"
description: "Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Gider yönetimi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı kullanıcıların bir girişi yakalamasını ve yüklemesini, böylece daha sonra bir gider raporuna ekleyebilmelerini sağlar. Bu mobil çalışma alanı ayrıca kullanıcıların hızlı bir şekilde gider satırlarını, ekli bir giriş kullanarak oluşturmalarına olanak verir."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 8bc47c5b170fd7dd8f6288682aad6eae1d2dc09a
ms.openlocfilehash: 9d3b7a4d5184c3c4958f4298f1d3dd4de0cd06d6
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="expense-management-mobile-workspace"></a>Mobil çalışma alanında gider yönetimi

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Bu konu, Microsoft Dynamics 365 for Operations mobil uygulaması için kullanılabilir olan Gider yönetimi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı kullanıcıların bir girişi yakalamasını ve yüklemesini, böylece daha sonra bir gider raporuna ekleyebilmelerini sağlar. Bu mobil çalışma alanı ayrıca kullanıcıların hızlı bir şekilde gider satırlarını, ekli bir giriş kullanarak oluşturmalarına olanak verir.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanına genel bakış
---------------------------------------------------

Çoğu kuruluş, personelin iade için gönderdiği bir seyahatle ya da işle ilgili gider raporuna, bir fişin kopyasının eklenmesini gerektirir. **Gider yönetimi** mobil çalışma alanı, kullanıcıların yeni gider satırlarını, fişin fotoğrafını ekleyerek istedikleri mobil cihazda hızla oluşturmalarını sağlar. Alternatif olarak, kullanıcılar fişin fotoğrafını çekebilir ve gider raporuna daha sonra ekleyebilirler. Özellikle **Gider yönetimi** mobil çalışma alanı kullanıcıya şu olanakları sağlar:

-   Fişin bir fotoğrafını çekmek ve Microsoft Dynamics 365 for Operations'a yüklemek. Bir kullanıcı daha sonra fotoğrafı bir gider raporunu daha sonra ekleyebilir.
-   Dosyayı kaydedilen bir giriş olarak yüklemek. Bir kullanıcı dosyayı bir gider raporuna daha sonra ekleyebilir.
-   Ekli bir fişi kullanarak yeni bir gider satırı oluşturmak. Bir kullanıcı, satır maddesini bir gider raporuna daha sonra ekleyebilir ve onay ve iade için gönderebilir.

Bu konunun kalan bölümleri, **Gider yönetimi** mobil çalışma alanının nasıl uygulanacağını ve kullanılacağını açıklar.

## <a name="prerequisites"></a>Ön koşullar
**Gider yönetimi** mobil çalışma alanını uygulamadan önce, sistem yöneticinizin aşağıdaki önkoşulları tamamladığından emin olun.

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
<td>Dynamics 365 for Operations'u kuruluşunuz için halihazırda dağıtılmadıysa, sistem yöneticiniz <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Bir Microsoft Dynamics 365 for Operations demo ortamı dağıt</a>'ı görmelidir.</td>
</tr>
<tr class="even">
<td>KB 4019015 uygulanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td>KB 4019015 (bir X++ güncelleştirmesi veya meta veri düzeltmesi), tedarik zinciri yönetimi için dört mobil çalışma alanı içerir. KB 4019015 uygulamak için sistem yöneticiniz bu adımları atması gerekir:
<ol>
<li>KB 4019015'yi, Microsoft Lifecycle Services (LCS) üzerinden karşıdan yükleyin.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Dağıtılabilir bir paket oluşturun</a> <strong>ApplicationSuite</strong> ve <strong>ExpenseMobile</strong> modelini içeren ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Dağıtılabilir paketi</a>, Dynamics 365 for Operations sisteminize uygulayın.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Gider yönetimi</strong> mobil çalışma alanı, Dynamics 365 for Operations mobil uygulaması için yayınlanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td><ol>
<li>Dynamics 365 for Operations'ı tarayıcınızda başlatın.</li>
<li><strong>Sistem parametreleri</strong> sayfasında, <strong>Mobil çalışma alanlarını yönet</strong>'i seçin.</li>
<li><strong>Gider yönetimi</strong> çalışma alanını seçin.</li>
<li><strong>Mobil çalışma alanını yayınla</strong> üzerine tıklayın.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobil uygulamasını yükleyin ve kurun
Dynamics 365 for Operations mobil uygulamasını mobil uygulama mağazanızdan yükleyin ve kurun.

-   Android için: [Google Play Store'da Dynamics 365 for Operations](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone için: [iTunes apps mağazsında Dynamics 365 for Operations](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)
-   Windows phone için (Universal Windows Platfırm \[UWP\]): Yakında geliyor!

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobil uygulamasına oturum açın
1.  Mobil cihazınızda uygulamayı başlatın.
2.  Dynamics 365 for Operations URL'nizi girin.
3.  Oturum açılacak şirketi girin. Örneğin **USMF** yazın.
4.  İlk defa oturum açtığınızda, Dynamics 365 for Operations hesabınızın kullanıcı adı ve parolasını girmeniz için uyarılırsınız. Kimlik bilgilerinizi girin.
5.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanlarını görürsünüz. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemek için çekebileceğinizi unutmayın. [![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak bir girişi yakalayın
1.  Mobil cihazınızda **Gider yönetimi** çalışma alanını seçin.
2.  **Giriş yakalama**'yı seçin.
3.  **Fotoğraf çek** veya **Resim seç**'i seçin.
4.  **Fotoğraf çek**'i seçtiyseniz, şu adımları izleyin:
    1.  Mobil cihazınızın kamerasına götürülürsünüz ve böylece fişin bir faturasını çekebilirsiniz. Fotoğraf çekmeyi bitirdiğinizde, fotoğrafı kabul etmek için **Tamam** üzerine tıklayın.
    2.  İsteğe bağlı: Fotoğraf için bir isim ve varsa not girin.

     veya **Resim seç**'i seçtiyseniz, şu adımları izleyin:
    1.  Listeden bir resim seçin.
    2.  İsteğe bağlı: Resim için bir isim ve varsa not girin.

5.  **Tamam**'ı seçin.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak hızlı gider girişi
1.  Mobil cihazınızda **Gider yönetimi** çalışma alanını seçin.
2.  **Hızlı gider girişi**'ni seçin.
3.  Gider için kategori seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş gider kategorilerinin bir listesini görürsünüz. Varsayılan olarak, 50 maddeye kadar yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler daha fazla bilgi için şura bakmalıdır: [Dynamics 365 for Operations mobil platformuna](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/) Kategoriniz listede değilse, Dynamics 365 for Operations içerisinde bir çevrimiçi arama yapmak için **Ara**'yı seçin. Gider kategorisine göre arama yapın veya gider türüne göre aramaya geçin.
4.  Giderin hareket tarihini girin.
5.  İsteğe bağlı: Gider için tüccarı girin.
6.  Giderin tutarını girin.
7.  Giderin para birimini seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş para birimlerinin bir listesini görürsünüz. Varsayılan olarak, 400 para birimine kadar yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler daha fazla bilgi için şura bakmalıdır: [Dynamics 365 for Operations mobil platformuna](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/) Para biriminiz listede değilse, Dynamics 365 for Operations içerisinde bir çevrimiçi arama yapmak için **Ara**'yı seçin. Para birimine göre arama yapın veya adına göre aramaya geçin.
8.  **Fotoğraf çek** veya **Resim seç**'i seçin.
9.  **Fotoğraf çek**'i seçtiyseniz, mobil cihazınızın kamerasına götürülürsünüz ve böylece fişin bir faturasını çekebilirsiniz. Fotoğraf çekmeyi bitirdiğinizde, fotoğrafı kabul etmek için **Tamam** üzerine tıklayın.  veya  **Resim seç**'i seçtiyseniz, listeden bir resim seçin.
10. **Tamam**'ı seçin.






