--- 
title: "Mobil iş cihazını kullanarak çalışanı yapılandırma"
description: "Bu yordam, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d56f861dbbf579e44fcd3fc4d8b45c24029acecc
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Mobil iş cihazını kullanarak çalışanı yapılandırma

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


