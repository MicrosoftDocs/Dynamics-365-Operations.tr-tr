--- 
title: "Başkasının yerine ürün sipariş etmek için izinleri ayarlama"
description: "Bu prosedür diğer çalışanların adına satınalma talepleri hazırlamak için çalışanlara nasıl izin verileceğini gösterir."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Başkasının yerine ürün sipariş etmek için izinleri ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür diğer çalışanların adına satınalma talepleri hazırlamak için çalışanlara nasıl izin verileceğini gösterir. Başka bir deyişle, bir satınalma talebi "hazırlayıcısı", başka bir "hazırlayıcı" için bir talep oluşturabilir. Bu yordam ayrıca bir çalışanın farklı tüzel varlıklarda veya işletme birimlerindeki sipariş öğelerine ve nasıl erişim verileceğini gösterir. Bu görevler genellikle bir satınalma yöneticisi tarafından yapılır. Bu prosedürü USMF demo şirketindeki verilerde veya kendi verilerinizde kullanabilirsiniz.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Başka bir çalışanın adına satınalma talepleri girmek için izin verin
1. Tedarik ve kaynak atama > Ayarlar > İlkeler > Satınalma talebi izinleri'ne gidin.
    * Geçerli görünüm alanının Hazırlayana göre olarak ayarlandığından emin olun.  Sol bölmedeki liste diğer kişiler adına talepler hazırlamak için izin verilmiş kişileri gösterir.  
2. İzin verilecek kişiyi (hazırlayan) seçin.
3. Ekle öğesini tıklatın.
4. Talep sahibi olarak eklemek istediğiniz kişiyi bulun ve seçin.
    * Talep sahibi hazırlayanın adına talepler oluşturabilen kişidir.  
    * Hazırlayanın seçilen çalışan adına satınalma talepleri oluşturabilmesi gerekiyorsa Yetkilendirme alanında Özel'i seçin. Hazırlayanın bu çalışana rapor veren tüm çalışanlar adına satınalma talebi oluşturabilmesi gerekiyorsa Raporlama'yı seçin.  
5. Etkili alanında bir tarih girin.
6. Bitiş alanına bir tarih girin.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Seçilen çalışan için satınalma talebi oluşturma iznine sahip hazırlayanları görüntüleyin
1. Geçerli görünüm alanından 'Talep sahibine göre'yi seçin.
    * Bu görünüm seçilen çalışan adına satınalma talepleri oluşturmak için izin verilen hazırlayanların listesini gösterir.  
2. Talep sahibi olarak yeni eklediğiniz çalışanı bulmak için Hızlı Filtre'yi kullanın.
3. Talep sahibini seçin.
    * Hazırlayan listesi sol bölmede seçilen talep sahibi adına maddeleri sipariş etme izni olan kişileri gösterir.   Buraya ek hazırlayanlar ekleyebilirsiniz.   Bu görünüm kişinin birincil tüzel kişiliği veya faaliyet birimi olamayan tüzel kişilikler ve faaliyet birimlerinde talep sahibine talepler oluşturmak için izin vermenizi de sağlar.  


