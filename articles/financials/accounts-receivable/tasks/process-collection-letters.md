--- 
title: "Tahsilat mektuplarını işleme"
description: "Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Tahsilat mektuplarını işleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir. Bu görevde USMF demo şirketi kullanılmaktadır.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Deftere nakil profilinde bir tahsilat mektubu sırası ayarlama
1. Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri'ne gidin.
2. Düzenle öğesine tıklayın.
    * Açılan listeden bir tahsilat mektubu sırası seçin. Bu deftere nakil profilini kullanarak hareketler için tahsilat mektupları oluşturmak istemiyorsanız ilgili alanı boş bırakın.  
    * Tablo kısıtlaması sekmesi, tahsilat mektuplarını işleme biçimini değiştirmenize olanak sağlar. Bu alan Evet olarak ayarlanırsa, bu deftere nakil profili için tahsilat mektupları oluşturulur.  
3. Sayfayı kapatın.

## <a name="create-collection-letters"></a>Tahsilat mektupları oluştur
1. Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektupları oluştur'a gidin.
    * Tahsilat mektuplarının hareket türlerini seçmeniz gerekir. Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.  
2. Tahsilat mektubu alanında bir seçenek belirleyin.
3. Tahsilat mektubunun tarihini girin.
    * İki deftere nakil profili seçeneği vardır:   Hesap – Her bir vade farkı dekontunun müşteri hesabına atanan deftere nakil profilini kullanın.   Seçim – Deftere nakil profili alanında seçtiğiniz deftere nakil profilini kullanın.  
    * "Kullanılacak deftere nakil profili:" seçeneğini "Seç" olarak değiştirdiyseniz, bir deftere nakil profili seçin.  
4. Eklenecek kayıtlar bölümünü genişletin.
5. Filtre'ye tıklayın.
6. Ölçüt alanında, bir Müşteri Kodu girin. Örneğin, TR-001 girin.
7. Tamam'a tıklayın.
8. Tamam'a tıklayın.

## <a name="print-collection-letters"></a>Tahsilat mektuplarını yazdırma
1. Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle'ye gidin.
2. Durum alanında, "Oluşturuldu"yu seçin.
3. Yazdırıldı alanında, "Yazdırılmadı"yı seçin.
4. Yazdır'ı tıklatın.
5. Tahsilat mektubu dekontu'nu tıklatın.
6. Eklenecek kayıtlar bölümünü genişletin.
7. Deftere nakiller için bir fatura kesme tarihi girin.
8. Tahsilat mektubunu yazdırmak için Tamam'ı tıklatın.

## <a name="post-the-collection-letter"></a>Tahsilat mektubunu deftere nakletme
1. Deftere Naklet öğesine tıklayın.
2. Tahsilat mektubu için deftere nakil tarihini girin.
3. Eklenecek kayıtlar bölümünü genişletin.
4. Tamam'a tıklayın.
5. Durum alanında, "Deftere nakledildi"yi seçin.
6. Yazdırılan alanında bir seçenek belirleyin.


