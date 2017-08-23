--- 
title: "El ile ambalajlamayı ayarlama (yalnızca Şubat ve Mayıs 2016)"
description: "Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c8cec376bcc8c50fb9a78bed039505608cd7782d
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a>El ile ambalajlamayı ayarlama (yalnızca Şubat ve Mayıs 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir. Bu süreçte ambar çalışanları ürünleri depolama konumlarından çeker ve onları ürün miktarları ve türlerini denetledikleri bir paketleme istasyonuna taşır ve daha sonra onları uygun konteynerlere atar. Bir konteyner tam olarak paketlendiğinde, bunu kapatıp çıkış noktalarına taşıyabilirler ve böylece ürünler sevk edilmeye hazır hale gelir. Bu yordam, USMF demo şirketini kullanır. Bu yordam yalnızca Dynamics 365 for Operations'ın Şubat 2016 ve Mayıs 2016 sürümleri içindir.


## <a name="set-up-location-profiles"></a>Yerleşim profillerini ayarla
1. Ambar yönetimi > Kurulum > Ambar > Konum profilleri öğesine gidin.
2. Yeni'ye tıklayın.
    * Konum profili paketleme istasyonları için kullanılır ve bir konum için bilgiler ve kurallar içerir.  
3. Konum profili numarası alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Konum biçimi alanında bir değer girin veya seçin.
6. Konum türü alanında bir değer girin veya seçin.
7. Karışık öğelere izin ver alanında Evet'i seçin.
8. Karışık stok durumlarına izin ver alanında Evet'i seçin.
9. Toplu iş günleri alanı için geçersiz kılma kurallarında Evet'i seçin.
10. Sayfayı kapatın.

## <a name="set-up-warehouse-management-parameters"></a>Ambar yönetimi parametreleri ayarla 
1. Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.
2. Paketleme sekmesine tıklayın.
3. Paketleme konumu için profil kimliği alanına bir değer girin veya buradan bir değer seçin.
    * Paketleme için kullanmak istediğiniz konum profilini seçin.  
4. Sayfayı kapatın.

## <a name="set-up-container-types"></a>Konteyner türlerini ayarla
1. Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri öğesine gidin.
2. Yeni'ye tıklayın.
    * Kullanılacak konteyner türlerini tanımlayabilirsiniz. Konteynerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve ağırlık da dahil olmak üzere belirtebilirsiniz.  Öznitelikler, konteyner türüne ek boyutlar eklemenize olanak sağlayan özelleştirilmiş alanlardır.     
3. Konteyner türü alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Dara alanına bir sayı girin.
6. Maksimum ağırlık alanında bir sayı girin.
7. Hacim alanına bir sayı girin.
8. Uzunluk alanına bir sayı girin.
9. Genişlik alanına bir sayı girin.
10. Yükseklik alanına bir sayı girin.
11. Kaydet'e tıklayın.
12. Sayfayı kapatın.

## <a name="set-up-packing-profiles"></a>Paketleme profilleri ayarla
1. Ambar yönetimi > Kurulum > Sevk > Sevk profilleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Paketleme profili kimliği alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Konteyner kapatma profili kimliği alanında bir değer girin veya bir değer seçin.
    * Bir konteyner kapatma profil kimliği isteğe bağlıdır ve bu paketleme profili için varsayılan konteyner kapatma profilidir.  
6. Konteyner kimliği modu alanında bir seçenek seçin.
    * Bu seçenek, bir konteyner oluşturulduğunda bir konteyner kimliğinin otomatik olarak mı oluşturulacağını yoksa konteyner kimliğinin el ile mi oluşturulacağını belirler.  
7. Konteyner türü alanında bir değer girin veya seçin.
    * Yeni konteyner türü oluşturulduğunda varsayılan olarak bu konteyner türü kullanılır.  
8. Konteyner kapatmada konteyneri otomatik oluştur onay kutusunu seçin.
9. Kaydet'e tıklayın.
10. Sayfayı kapatın.

## <a name="set-up-container-closing-profiles"></a>Konteyner kapanış profilleri ayarlama
1. Ambar yönetimi > Kurulum > Konteynerler > Konteyner kapanış profilleri öğesine gidin.
    * Konteyner kapanış profilleri, bir konteyner kapandığında ne olacağını tanımlar. Birden fazla konteyner kapatma profili ayarlayabilirsiniz.       
2. Yeni'ye tıklayın.
3. Konteyner kapanış profili kimliği alanında bir değer girin.
4. Açıklama alanına bir değer girin.
5. Manifesto yeri alanında, bir seçenek seçin.
    * Sevk irsaliyesinin konteyner kapatmasında mı yoksa sevkiyatın onaylanmasında mı gerçekleşeceğini belirtin. Manifestolamak Taşımacılık yönetimini gerektirir. Manifestolamanın çalışması için taşımacılık motorunda uygulanmış olması gereklidir.  
6. Ambar alanında bir değer girin veya bir değer seçin.
7. Son sevkiyat alanı için varsayılan konum alanına bir değer girin veya seçin.
    * Bu, konteynerler kapatıldıktan sonra ürünlerin taşınacağı konum olacaktır. Bu konumun Ambar parametrelerinde tanımlanmış bir konum profili olmalıdır.  
8. Ağırlık birimi alanına bir değer girin veya buradan bir değer seçin.
9. Kaydet'e tıklayın.


