---
title: Görev kayıtları için güvenlik tanılaması
description: Bu makale, bir görev kaydı temel alınarak güvenlik izni gereksinimlerinin nasıl analiz edileceği ve yönetileceği hakkında bilgi sağlar.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: cb69bf997100f25cd0ad2b7e34139857199e5d00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880181"
---
# <a name="security-diagnostics-for-task-recordings"></a>Görev kayıtları için güvenlik tanılaması

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Başlamadan önce

Bu makale, bir görev kaydı temel alınarak güvenlik izni gereksinimlerinin nasıl analiz edileceği ve yönetileceği hakkında bilgi sağlar. Bu makaledeki adımları gerçekleştirmeden önce, analiz etmek istediğiniz iş süreci için bir görev kaydınız olmalıdır. Bir iş süreci kaydetmek için [Görev kaydedici kaynakları](../../user-interface/task-recorder.md)'na bakın. 

## <a name="manage-security-for-a-task-recording"></a>Görev kaydı için güvenliği yönetme

1. **Sistem yönetimi** > **Güvenlik** > **Görev kaydı için güvenlik tanılamaları**'na gidin.
2. Görev kaydını konumundan açın. **Bu bilgisayardan aç**'ı veya **Lifecycle Services'tan aç**'ı seçin ve sonra **Kapat**'ı seçin.
3. Bu süreç için gerekli güvenlik nesnelerini listeleyen **Güvenlik menüsü öğe ayrıntıları** sayfasını açar.

 > [!NOTE]
 > **Eylem** ve **Çıkış** menü öğeleri listeye dahil edilmemiştir.

4. **Kullanıcı kimliği** alanında bir kullanıcı seçin. Kullanıcının bazı menü öğeleri için izni yoksa, **Eksik izinler** alanı **Evet** olarak güncelleştirilir.
  
  ![Güvenlik menü öğesi ayrıntıları sayfası.](../media/Security-Menu-Item-Details.png)

5. Eksik izni veren roller, görevler ve ayrıcalıklar gibi güvenlik nesnelerinin listesini görmek için **Referans ekle**'yi seçin.
6. Listeden bir güvenlik nesnesi seçin:

    - **Rol** seçiliyse, **Kullanıcıya rol ekle**'yi seçin. Bu, **Kullanıcıları rollere ata** sayfasını açar. Daha fazla bilgi için bkz. [Kullanıcıları güvenlik rollerine ata](assign-users-security-roles.md) sayfasına bakın.
    - **Görev** seçilmişse, **Role görev ekle**'yi seçin, görevin ekleneceği rolleri ve ardından **Tamam**'ı seçin.
    - **Ayrıcalık** seçilmişse, **Görevlere ayrıcalık**'yi seçin, görevin ekleneceği rolleri ve ardından **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]