---
title: Mobil iş cihazını kullanarak çalışanı yapılandırma
description: Bu yordam, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571371"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Mobil iş cihazını kullanarak çalışanı yapılandırma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.


## <a name="assign-roles-to-user-account"></a>Kullanıcı hesabına roller atama
1. Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.
2. Kullanıcı hesabının makine operatörü rolüyle ilişkili olduğu çalışanın adına filtre uygulamak için Hızlı Filtre'yi kullanın. Örnek verilerde çalışanın adı Shannon olacaktır.
3. Kullanıcı hesabı kaydını vurgulayın.
4. Listede, kullanıcı hesabının ayrıntılarını görüntülemek için seçili satırdaki "Ad" bağlantısını tıklatın.
5. Ağaçta, 'Roller\Makine operatörü' öğesini seçin.
6. Kullanıcı hesabı ayrıntıları sayfasını kapatın.
7. Sayfayı kapatın.

## <a name="configure-worker-account"></a>Çalışan hesabını yapılandırın.
1. İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin.
2. Kullanıcı hesabının makine operatörü rolüyle ilişkili olduğu çalışanın adına filtre uygulamak için Hızlı Filtre'yi kullanın. Örnek verilerde çalışanın adı Shannon olacaktır.
3. Kullanıcı hesabı kaydını vurgulayın.
4. Listede, kullanıcı hesabının ayrıntılarını görüntülemek için seçili satırdaki "Ad" bağlantısını tıklatın.
5. İstihdam sekmesine tıklayın.
6. Saat kayıt FastTab'ini genişletin ve kayıt terminallerinde etkinleştir'i tıklatın.
7. Kayıt terminallerinde etkinleştir'i tıklatın.
8. Hesaplama grubu alanında bir değer girin veya seçin.
9. Varsayılan hesaplama grubu alanında +bir değer girin veya seçin.
10. Onay grubu alanında bir değer girin veya seçin.
11. Standart profil alanında bir değer girin veya bir değer seçin.
12. Profil grubu alanında bir değer girin veya bir değer seçin.
13. Tamam'ı tıklatın.
14. Yeni zaman kayıt çalışanı için bir rozet numarası girmek için Düzenle'yi tıklatın.
15. Rozet Kodu alanında bir değer girin.
16. Kaydet'i tıklatın.
17. SaveRecord kısayolunu kullanın.
18. Çalışan ayrıntıları sayfasını kapatın.
19. Sayfayı kapatın.

## <a name="assign-worker-to-device-group"></a>Cihaz grubuna çalışan atayın.
1. Üretim denetimi > Ayarlar > Üretim yürütme > Cihazlar için iş kartını konfigüre et'e gidin.
2. Ekle öğesini tıklatın.
3. Listede, seçili satırı işaretleyin.
4. Tamam'a tıklayın.
5. Düzenle öğesine tıklayın.
6. Üretim birimi alanında çalışanın varsayılan filtresini ayarlayabilirsiniz. Bu, çalışan bu cihazda oturum açtığında yalnızca seçili üretim biriminin üretim işlerinin gösterilmesini sağlar.
7. Sayfayı kapatın.

