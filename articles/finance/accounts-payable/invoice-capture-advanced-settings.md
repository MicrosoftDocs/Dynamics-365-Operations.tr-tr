---
title: Invoice Capture çözümü gelişmiş ayarları
description: Bu makalede, Invoice Capture çözümünde gelişmiş ayarlar hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691245"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Invoice Capture çözümü gelişmiş ayarları

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, Invoice Capture çözümünde gelişmiş ayarlar hakkında bilgi sağlanmaktadır.

## <a name="create-additional-connections-for-channels"></a>Kanallar için ek bağlantılar oluşturma

Farklı kanallardan gelen faturaların izlenmesini etkinleştirmek üzere e-posta veya dosya depolama alanı için bağlantılar oluşturmanız gerekir. Çözümde kullanılan otomatik akışlara erişim izni vermek için bağlantıları başlangıçta kaydetmeniz gerekir.

Aşağıdaki bağlantı türleri, faturaları içe aktarmak için kullanılır:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Fatura içe aktarmaya yönelik kanal, diğer yapılandırma adımlarındaki bağlantıları kullanır. Kullanıcıların belirli bir bağlantının kanalını oluşturabilmesi için kendilerine **Yönetici** güvenlik rolünün verilmesi ve bağlantıları oluşturmaları gerekir.

Microsoft Dataverse için bağlantı oluşturmak üzere aşağıdaki adımları izleyin.

1. **Yönetici sistemi \> Varsayılan çözüm** bölümüne gidin.
2. **Yeni**'yi seçin ve ardından **Bağlantı Başvurusu** seçeneğini belirleyin.
3. **Görünen ad** alanına bir ad girin.
4. Bağlayıcı olarak **Microsoft Dataverse**'i seçin.
5. Bağlantıyı ilk defa ayarlıyorsanız **Yeni bağlantı**'yı seçin.
6. Görüntülenen iletişim kutusunda Dataverse bağlantısı oluşturun ve ardından **Oluştur**'u seçin.
7. Dataverse hesabını ve parolasını girin.
8. Doğrulama geçtikten sonra bağlantı sayfasına gidin, **Yenile** seçeneğini belirleyin, hesabı seçin ve ardından **Oluştur** seçeneğini belirleyin.

E-posta veya dosya depolama alanı bağlantısı oluşturmak için aşağıdaki adımları izleyin.

1. **Bağlantı oluşturma** sayfasında **Bağlantı türü** alanında **Office 365 Outlook**'u seçin.
2. E-posta bağlantısı için bağlayıcı olarak **Outlook.com** veya **Office 365 Outlook**'u seçebilirsiniz. Dosya depolama alanı bağlantısı için **OneDrive** veya **SharePoint**'i seçebilirsiniz.

Mevcut bağlantıları gözden geçirmek için **Varsayılan çözüm \> Nesneler \> Bağlantı Başvuruları**'na gidin. Kanalları oluşturan kullanıcının, belirli e-posta veya dosya depolama alanı bağlantılarına ek olarak en az bir Dataverse bağlantısına sahip olmalıdır. Yeni kanalın oluşturucusu, bağlantının sahibi olmalıdır.
