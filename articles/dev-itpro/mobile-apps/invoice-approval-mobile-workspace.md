---
title: "Fatura onayları mobil çalışma alanı"
description: "Bu konu, Fatura onayları mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, fatura başlığı iş akışı işlemi üzerinden size atanmış olan faturaların bir listesini sağlar."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 190f48f4d5e304902b701f74f2cbefcbe7b36b15
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="invoice-approvals-mobile-workspace"></a>Fatura onayları mobil çalışma alanı

[!include[banner](../includes/banner.md)]

Bu konu, **Fatura onayları** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, fatura başlığı iş akışı işlemi üzerinden size atanmış olan faturaların bir listesini sağlar. 

Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations mobil uygulaması ile kullanılmak üzere geliştirilmiştir.

## <a name="overview"></a>Özet

**Fatura onayları** mobil çalışma alanı, Borç hesapları memurları ve yöneticilerinin, onlara atanmış olan faturalarını bir satıcı faturası başlığı iş akışı işlemi olarak görmelerine olanak sağlar. Fatura bilgisini görüntüleyebilir ve hatta satır ve dağıtım ayrıntılarını, bilgili onay kararları vermenize yardımcı olmak için kullanabilirsiniz. Çalışma alanından, faturayı iş akışı işleminde taşımak için eylem alabilirsiniz. 

## <a name="prerequisites"></a>Ön koşullar

Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.

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
<td>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017), kuruluşunuzda dağıtılmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="../deployment/deploy-demo-environment.md">Tanıtım ortamını dağıtma</a>.
</td>
</tr>
<tr class="even">
<td><strong>Fatura onayları</strong> mobil çalışma alanını yayımlanmış olması gerekir.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin

Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:

-   [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
-   [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın

1.  Mobil cihazınızda uygulamayı başlatın.
2.  Microsoft Dynamics 365 URL'nizi girin.
3.  İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.
4.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

    [![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Fatura onayları mobil çalışma alanını kullanarak faturaları onaylayın
1.  Mobil cihazınızda **Fatura onayları** çalışma alanını seçin.
2.  Satıcı fatura başlığı iş akış işlemi tarafından size atanmış olan faturayı seçin.
3.  **Fatura ayrıntıları** sayfasında, satıcı ve tarih bilgisi gibi fatura başlığı bilgisini gözden geçirin.
4.  Fatura üzerinde, **Fatura satırı ayrıntıları** görünümünde daha ayrıntılı bilgi görmek için bir satır seçin.
5.  **Fatura satırı ayrıntıları** görümünde, **Dağıtımlar**'ı seçerek satır dağılımlarını görüntüleyin. Burada fatura satırı için muhasebeyi görebilirsiniz. Gösterilen bilgi, mali boyutları ve ana hesabı içerir.
6.  **Fatura satırı ayrıntıları** sayfasında , **Dağıtımlar**'ı seçerek tüm dağılımları görüntüleyin. Burada, faturanın tamamı için muhasebeyi görebilirsiniz. Gösterilen bilgi, mali boyutları ve ana hesapları içerir. 
7.  Faturaya eklenmiş herhangi bir notu veya dosyaları görmek için **Ekler**'i seçin.
8.  **Fatura ayrıntıları** sayfasında, gözden geçirme işleminizi tamamlamak için ilgili iş akışı eylemini seçin.
9.  **Tamam**'ı seçin.

