---
title: Regulatory Configuration Service (RCS) - RCS ortamını silme
description: Bu makalede, Regulatory Configuration Service (RCS) sistem yöneticisinin bir RCS ortamını ve ilgili verileri nasıl silebileceği açıklanmaktadır.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277255"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - RCS ortamını silme

[!include [banner](../includes/banner.md)]

Bu makalede, Regulatory Configuration Service (RCS) sistem yöneticisinin bir RCS ortamını ve ilgili verileri nasıl silebileceği açıklanmaktadır.

Bu makaledeki yordamı tamamlamadan önce, aşağıdaki ön koşulların yerine getirilmesi gerekir:

- RCS ortamı için size **Sistem yöneticisi** rolü atanmış olması gerekir.
- **Sistem Yöneticisi** rolüne **RCSDeleteEnvironmentDuty** rolü atanmış olmalıdır.

## <a name="delete-an-rcs-environment"></a>RCS ortamını silme

1. RCS'yi açın ve **Elektronik raporlama** çalışma alanı kutucuğunu seçin.
2. **İlgili bağlantılar** bölümünde, **RCS ortamını sil**'i seçin.

    ![İlgili bağlantılar bölümünde RCS ortamı bağlantısını silme.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Görüntülenen iletişim kutusunda, ortam silme kapsamı hakkındaki iletileri gözden geçirin.

    ![RCS ortamını sil iletişim kutusundaki iletiler.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > RCS ortamının silinmesi geri alınamaz.
    >
    > İşlem, seçilen RCS ortamını ve Genel depoda depolanan özellikler ve yapılandırmalar dahil ilgili tüm verileri siler. Diğer kuruluşlarla paylaşılan özellikler ve yapılandırmalar, bağımlılıkları yoksa paylaşımdan kaldırılır ve silinir. Bağımlılıkları olan özellikler ve yapılandırmalar devam ettirilmiyor olarak işaretlenir.

4. Sağlanan alanda, silmek istediğinizi onaylamak için RCS ortamının genel benzersiz tanımlayıcısını (GUID) girin. Ortamın GUID'i silme iletisine dahil edilir.
5. **Ortamı sil**'i seçin.
    
RCS ortamınız ve ilgili tüm veriler artık silindi.

> [!IMPORTANT]
> Bir RCS ortamını sildikten sonra, verileri kurtarmanın bir yolu yoktur. Kullanılabilir herhangi bir RCS bölgesinde yeni bir RCS ortamı oluşturulabilir.
