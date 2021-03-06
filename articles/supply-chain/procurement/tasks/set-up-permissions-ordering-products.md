---
title: Başkasının yerine ürün sipariş etmek için izinleri ayarlama
description: Bu konu diğer çalışanların adına satınalma talepleri hazırlamak için çalışanlara nasıl izin verileceğini açıklar.
author: kamaybac
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0408085d401a34a409bfe46bc6845a9c81a2eea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811906"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Başkasının yerine ürün sipariş etmek için izinleri ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu diğer çalışanların adına satınalma talepleri hazırlamak için çalışanlara nasıl izin verileceğini açıklar. Başka bir deyişle, bir satınalma talebi "hazırlayıcısı", başka bir "hazırlayıcı" için bir talep oluşturabilir. Bu yordam ayrıca bir çalışanın farklı tüzel varlıklarda veya işletme birimlerindeki sipariş öğelerine ve nasıl erişim verileceğini gösterir. Bu görevler genellikle bir satınalma yöneticisi tarafından yapılır. Bu prosedürü USMF demo şirketindeki verilerde veya kendi verilerinizde kullanabilirsiniz.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Başka bir çalışanın adına satınalma talepleri girmek için izin verin
1. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Kurulum > İlkeler > Satınalma talebi izinleri**'ne gidin. **Geçerli görünüm** alanının **Hazırlayana göre** olarak ayarlandığından emin olun. Sol bölmedeki liste diğer kişiler adına talepler hazırlamak için izin verilmiş kişileri gösterir.  
2. İzin verilecek kişiyi (hazırlayan) seçin.
3. **Ekle**'yi seçin.
4. Talep sahibi olarak eklemek istediğiniz kişiyi bulun ve seçin.
    - Talep sahibi hazırlayanın adına talepler oluşturabilen kişidir.  
    - Hazırlayanın seçilen çalışan adına satınalma talepleri oluşturabilmesi gerekiyorsa **Yetkilendirme** alanında **Özel**'i seçin. Hazırlayanın bu çalışana rapor veren tüm çalışanlar adına satınalma talebi oluşturabilmesi gerekiyorsa **Raporlama**'yı seçin.  
5. **Yürürlüğe giriş** alanında bir tarih girin.
6. **Bitiş** alanına bir tarih girin.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Seçilen çalışan için satınalma talebi oluşturma iznine sahip hazırlayanları görüntüleyin
1. **Geçerli görünüm** alanında **Talep sahibine göre**'yi seçin. Bu görünüm seçilen çalışan adına satınalma talepleri oluşturmak için izin verilen hazırlayanların listesini gösterir.  
2. Talep sahibi olarak yeni eklediğiniz çalışanı bulmak için Hızlı Filtre'yi kullanın.
3. Talep sahibini seçin. Hazırlayan listesi sol bölmede seçilen talep sahibi adına maddeleri sipariş etme izni olan kişileri gösterir.  Buraya ek hazırlayanlar ekleyebilirsiniz. Bu görünüm kişinin birincil tüzel kişiliği veya faaliyet birimi olamayan tüzel kişilikler ve faaliyet birimlerinde talep sahibine talepler oluşturmak için izin vermenizi de sağlar.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]