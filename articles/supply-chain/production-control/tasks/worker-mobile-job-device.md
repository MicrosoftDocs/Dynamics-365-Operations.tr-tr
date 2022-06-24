---
title: Mobil iş cihazını kullanarak çalışanı yapılandırma
description: Bu makale, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.
author: johanhoffmann
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f6f51a66d49cafd172ba123bf883fb41cdcb5c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844346"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Mobil iş cihazını kullanarak çalışanı yapılandırma

[!include [banner](../../includes/banner.md)]

Bu makale, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Bir çalışanın belirli bir role atanmasını doğrulayın

Bu örnekte, çalışan hesabı yapılandırmadan önce "SHANNON" kullanıcısının makine operatörü rolüne atanacağını doğrulayın.

1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin.
2. Hızlı filtrede bir kullanıcı arayın. Bu örnek için, `shannon` girin.
3. Görüntülenen kullanıcı hesabının **Kullanıcı kimliği** sütununda bağlantıyı seçin.
4. **Kullanıcı rolleri** ağacında **Roller > Makine operatörü** öğesini seçin.
5. Giriş sayfasına dönmek için **Kullanıcı ayrıntıları** ve **kullanıcılar** sayfalarını kapatın.

## <a name="configure-worker-account"></a>Çalışan hesabını yapılandırın
1. **Gezinti bölmesi > Modüller > İnsan kaynakları > İşçiler > İşçiler**'e gidin.
2. Hızlı filtrede bir kullanıcı arayın. Bu örnek için, `shannon` girin.
3. Görüntülenen kullanıcı hesabının **Ad** sütununda bağlantıyı seçin.
4. **Saat kaydı** sekmesini seçin.
5. **Kayıt terminallerinde etkinleştir**'i seçin.
6. Aşağıdaki alanlara değerleri girin vey seçin:  

    - **Hesaplama grubu**  
    - **Varsayılan hesaplama grubu**  
    - **Onay grubu**  
    - **Standart profil**  
    - **Profil grubu**  

7. **Tamam**'ı seçin.
8. Yeni zaman kayıt çalışanı için bir rozet numarası girmek için **Düzenle**'yi seçin. **Rozet kodu** alanında bir değer girin.
9. **Kaydet**'i seçin.
10. **Çalışan ayrıntıları** ve **İşçiler** sayfalarını kapatın.

## <a name="assign-worker-to-device-group"></a>Cihaz grubuna çalışan atayın
1. **Üretim denetimi > Ayarlar > Üretim yürütme > Cihazlar için iş kartını konfigüre et**'e gidin.
2. **Ekle**'yi seçin.
3. Listede, istediğiniz çalışanı seçin. Bu örnek için **SHANNON** seçeneğini belirtin.
4. **Tamam**'ı seçin.
5. **Düzenle** öğesini seçin.
6. **Üretim birimi** alanında çalışanın varsayılan filtresini ayarlayabilirsiniz. Bu, çalışan bu cihazda oturum açtığında yalnızca seçili üretim biriminin üretim işlerinin gösterilmesini sağlar. İstenen değeri girin.
7. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]