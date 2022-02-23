---
title: Görev kayıtları için güvenlik tanılaması
description: Bu konu, bir görev kaydı temel alınarak güvenlik izni gereksinimlerinin nasıl analiz edileceği ve yönetileceği hakkında bilgi sağlar.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679802"
---
# <a name="security-diagnostics-for-task-recordings"></a>Görev kayıtları için güvenlik tanılaması

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Başlamadan önce

Bu konu, bir görev kaydı temel alınarak güvenlik izni gereksinimlerinin nasıl analiz edileceği ve yönetileceği hakkında bilgi sağlar. Bu konudaki adımları gerçekleştirmeden önce, analiz etmek istediğiniz iş süreci için bir görev kaydınız olmalıdır. Bir iş süreci kaydetmek için [Görev kaydedici kaynakları](../../user-interface/task-recorder.md)'na bakın. 

## <a name="manage-security-for-a-task-recording"></a>Görev kaydı için güvenliği yönetme

1. **Sistem yönetimi** > **Güvenlik** > **Görev kaydı için güvenlik tanılamaları**'na gidin.
2. Görev kaydını konumundan açın. **Bu bilgisayardan aç**'ı veya **Lifecycle Services'tan aç**'ı seçin ve sonra **Kapat**'ı seçin.
3. Bu süreç için gerekli güvenlik nesnelerini listeleyen **Güvenlik menüsü öğe ayrıntıları** sayfasını açar.

 > [!NOTE]
 > **Eylem** ve **Çıkış** menü öğeleri listeye dahil edilmemiştir.

4. **Kullanıcı kimliği** alanında bir kullanıcı seçin. Kullanıcının bazı menü öğeleri için izni yoksa, **Eksik izinler** alanı **Evet** olarak güncelleştirilir.
  
  ![Güvenlik menü öğesi ayrıntıları sayfası](../media/Security-Menu-Item-Details.png)

5. Eksik izni veren roller, görevler ve ayrıcalıklar gibi güvenlik nesnelerinin listesini görmek için **Referans ekle**'yi seçin.
6. Listeden bir güvenlik nesnesi seçin:

    - **Rol** seçiliyse, **Kullanıcıya rol ekle**'yi seçin. Bu, **Kullanıcıları rollere ata** sayfasını açar. Daha fazla bilgi için bkz. [Kullanıcıları güvenlik rollerine ata](assign-users-security-roles.md) sayfasına bakın.
    - **Görev** seçilmişse, **Role görev ekle**'yi seçin, görevin ekleneceği rolleri ve ardından **Tamam**'ı seçin.
    - **Ayrıcalık** seçilmişse, **Görevlere ayrıcalık**'yi seçin, görevin ekleneceği rolleri ve ardından **Tamam**'ı seçin.
