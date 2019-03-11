---
title: Sevk eden taşımacıları ayarlama
description: Bu yordam, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "314498"
---
# <a name="set-up-shipping-carriers"></a>Sevk eden taşımacıları ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir. Ulaşım Koordinatörü, daha sonra, gelen veya giden bir yük için Sevkiyat taşıyıcısı atayabilir.


## <a name="create-a-new-shipping-carrier"></a>Yeni bir Sevkiyat taşıyıcısı oluşturun
1. Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Sevkiyat taşıyıcıları alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Mod alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Sevkiyat taşıyıcısı için genel bilgileri doldurun
1. Genel Bakış bölümünün genişletilmiş görünümüne geçin.
2. Sevkiyat taşıyıcısını etkinleştir onay kutusunu işaretleyin veya temizleyin.
3. Satıcı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Sevkiyat taşıyıcısının atanacağı satıcı hesabını seçin.  
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Taşıma ödemesi tipi alanında bir seçenek belirleyin.
    * Taşıma ödemesi sayfasını kullanmak için El ile'yi seçin veya EDI'yi seçerek ödemeyi Elektronik Veri Değişimi (EDI) kullanarak güncelleştirin.  
7. Taşıyıcısını değerlendirmesini etkinleştir onay kutusunu işaretleyin veya temizleyin.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Sevkiyat taşıyıcısı için gerekli hizmetleri oluşturun
1. Hizmetler bölümünün genişletilmiş görünümüne geçin.
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Taşıyıcı hizmeti alanına bir değer yazın.
5. İsim alanına bir değer yazın.
6. Taşıma yöntemi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Taşıyıcı için adresi (isteğe bağlı) ayarlayın
1. Adres bölümünün genişletilmiş görünümüne geçin.
2. Yeni'ye tıklayın.
3. Ad veya açıklama alanına bir değer yazın.
4. Ülke/bölge alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Posta kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Cadde alanına bir değer yazın.
10. Tamam'a tıklayın.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Sevkiyat taşıyıcısı için derecelendirme profilini ayarlayın
1. Değerlendirme profilleri bölümünün genişletilmiş görünümüne geçin.
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Değerlendirme profili numarası alanına bir değer yazın.
5. İsim alanına bir değer yazın.
6. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
10. Listede, istenen kaydı bulun ve seçin.
11. Listede, seçili satırdaki bağlantıya tıklayın.
12. Değerlendirme altyapısı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Taşıyıcı ile aranızdaki sözleşmeye uyugn olacak Değerlendirme altyapısını seçin.  
13. Listede, istenen kaydı bulun ve seçin.
14. Listede, seçili satırdaki bağlantıya tıklayın.
15. Ana oran alanında, aramayı açmak için açılır menü düğmesine tıklayın.
16. Listede, istenen kaydı bulun ve seçin.
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. Taşıma süresi altyapıları alanında, aramayı açmak için açılır menü düğmesine tıklayın.
19. Listede, seçili satırdaki bağlantıya tıklayın.
20. Kaydet'e tıklayın.

