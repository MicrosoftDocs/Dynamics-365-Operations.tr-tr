--- 
title: Elektronik imza ayarlama
description: "Bu yordamı kullanarak elektronik imzaları ayarların."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 43ac3aecd9290e496fc8dd237c0d09b60638f442
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-electronic-signatures"></a>Elektronik imza ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordamı kullanarak elektronik imzaları ayarların. Elektronik imza bir hesaplama işlemi başlatmak veya onaylamak üzere olan kişinin kimliğini doğrular. Bu yöntemi oluşturmak için kullanılan demo verisi şirketi DAT'dir.


## <a name="enable-the-electronic-signature-configuration-key"></a>Elektronik imza konfigürasyon anahtarını etkinleştirin
1. Sistem Yönetimi > Kurulum > Lisans yapılandırma seçeneğine gidin.
2. Ağaçta, 'Yönetim' öğesini genişletin veya daraltın.
    * Elektronik imza onay kutusunun işaretlendiğinden emin olun.  
    * Elektronik imza onay kutusu seçili değilse, bakım modunu etkinleştirmeniz gerekir. Bakım modu bu ortamda Lifecycle Services'den bir bakım işi çalıştırılarak ya da Deployment.Setup aracını yerel ortamda kullanarak etkin hale getirilebilir.  
3. Sayfayı kapatın.

## <a name="set-up-electronic-signature-parameters"></a>Elektronik imza parametrelerini ayarlama
1. Kuruluş yönetimi > Kurulum > Elektronik imza > Elektronik imza parametreleri seçeneğine gidin.
2. Düzenle öğesine tıklayın.
3. Bildirim alanına bir değer yazın.
    * İmza istendiğinde imzalayanların alacağı bildirimi girin. Herhangi bir metni girebilirsiniz. Genellikle bu metin kullanıcılara, bir belgenin imzalanmasının ne anlama geldiğini açıklar.  
    * Bildirim metninin başka dillerde girmek isterseniz, çeviriler düğmesini tıklatın.  
4. Kaydet'e tıklayın.
5. Sayfayı kapatın.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Elektronik imzalar için neden kodları ayarlama
1. Kuruluş yönetimi > Kurulum > Elektronik imza > Elektronik imza sebep kodları seçeneğine gidin.
2. Yeni'ye tıklayın.
    * Elektronik imzaları kullanmadan önce neden kodları ayarlamanız gerekir. Bir belgeyi imzalarken geçerli bir neden kodu gerekir.     İmzalayan, bir elektronik imzanın amacını belirtmek üzere bir neden kodu seçer. Örneği, yasal onayı belirtmek için bir neden kodu kullanılabilir.  
3. Sebep kodu alanına bir değer girin.
4. Açıklama alanına bir değer girin.
    * Gerekirse ek neden kodlarını girin.  
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.

## <a name="require-electronic-signatures-for-existing-processes"></a>Varolan bir işlemler için elektronik imzayı gerekli kılın
1. Kuruluş yönetimi > Kurulum > Elektronik imza > Elektronik imza gereksinimleri seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * Elektronik imza gerektiren bir işlem seçme.  
3. İmza gerekli onay kutusunu seçin veya temizleyin.
    * Elektronik imza gerektiren her işlem için bu adımları yineleyin.  
4. Kaydet'e tıklayın.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Elektronik imzalar için özel bir gereksinim oluşturun
1. Yeni'ye tıklayın.
2. İmza gerekli onay kutusunu seçin veya temizleyin.
3. Ad alanında, elektronik imza gerektiren bir işlem için bir ad girin.
4. Tablo adı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listeden, imzalanması gereken verilerin depolandığı tabloyu bulun ve seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Alan ismi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Listede, izlemek istediğiniz tabloyu bulun ve seçin.
9. Listede, seçili satırdaki bağlantıya tıklayın.
    * İmzanın ne zaman gerekli olacağını belirtin.     Alan içindeki veri değiştiğinde imza gerekliyse Her zaman'ı seçin.     Yalnızca belirli koşullarda imza gerekliyse, Yalnızca'yı seçin. Yalnızca'yı seçerseniz, ayrıca aşağıdaki seçeneklerden birini seçmelisiniz: bir kayıt silindiğinde, bir kayıt güncelleştirildiğinde veya bir kayıt eklendiğinde.  
10. Kaydet'e tıklayın.
11. Sayfayı kapatın.

