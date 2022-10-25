---
title: Invoice Capture çözümünü yükleme
description: Bu makalede, Invoice Capture çözümünü yükleme ve Microsoft Dynamics 365 Finance ile tümleştirme hakkında bilgi sağlanmaktadır.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691248"
---
# <a name="install-the-invoice-capture-solution"></a>Invoice Capture çözümünü yükleme

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Çözümü özel önizlemede yüklediyseniz devam etmeden önce eski çözümü kaldırmanız gerekir.

## <a name="prerequisites"></a>Ön Koşullar

Invoice Capture çözümünü yükleyebilmek için önce aşağıdaki ön koşulları tamamlamanız gerekir:

1. Uygulama kaydedin ve Azure aboneliğiniz altında Microsoft Azure Active Directory (Azure AD) bölümüne bir istemci gizli anahtarı ekleyin. Daha fazla bilgi için bkz. [AAD ile web uygulaması kaydetme](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Daha sonra ihtiyacınız olacağından **Uygulama (istemci) kimliği**, **İstemci gizli anahtarı** ve **Kiracı Kimliği** değerlerini not edin.

2. Azure uygulamasını bir Dynamics 365 Finance ortamında kaydedin. Daha fazla bilgi için bkz. [Harici uygulamanızı kaydetme](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Çözümü yükleme ve ayarlama

Invoice Capture çözümünü yüklemek için AppSource'a gidin ve [Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture) önizleme sürümü bağlantısını seçin. Yükleme tamamlandıktan sonra çözümün Power Apps'te seçili ortamda yüklü olduğunu görürsünüz.

Kurulumu tamamlamak için aşağıdaki adımları izleyin.

1. Aşağıdaki ayrıntıları ayarlamak için [yardımcı çözümü](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) indirin:

    - Microsoft Power Platform ile Finance ortamı arasındaki iletişim
    - Kanal tarafından kullanılacak Dataverse ve Office 365 Outlook için bağlantı başvurusu

2. Power Apps'te ortamınıza gidin ve **Çözümü içe aktar**'ı seçin.
3. **Gözat** seçeneğini belirleyin, indirdiğiniz yardımcı çözüm paketini seçin ve ardından **İleri** seçeneğini belirleyin.
4. **Sonraki**'yi seçin.
5. Mevcut bir bağlantıyı atayın veya **Yeni bağlantı** seçeneğini belirleyerek yeni bir bağlantı oluşturun.
6. Paket başarıyla içe aktarıldıktan sonra **Dynamics 365 Invoice Capture - Yükleme Araçları**'nı açın.
7. Microsoft Power Platform'da Invoice Capture çözümü ile Finance arasındaki bağlantıyı ayarlamak için Bulut akışını çalıştırın.
8. **Çalıştır**'ı seçin ve aşağıdaki parametreleri belirtin:

    - **Dynamics 365 Finance Url'si**: Tümleştirmek istediğiniz Finance ortamının URL'si.
    - **Kiracı Kimliği**: Finance ortamının kiracı kimliği.
    - **İstemci kimliği**: Kaydedilen Azure abonelik kimliği.
    - **İstemci Gizli Anahtarı**: Azure aboneliği için oluşturulan istemci gizli anahtarı.
