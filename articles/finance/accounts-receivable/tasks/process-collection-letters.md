---
title: Tahsilat mektuplarını işleme
description: Bu konu, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 2b8ce102086535a5462d3fa0e8ac76e9ec3dd15c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448749"
---
# <a name="process-collection-letters"></a>Tahsilat mektuplarını işleme

[!include [banner](../../includes/banner.md)]

Bu konu, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir. Bu görevde USMF demo şirketi kullanılmaktadır.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Deftere nakil profilinde bir tahsilat mektubu sırası ayarlama
1. **Gezinti bölmesi > Modüller > Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri**'ne gidin.
2. **Düzenle**'yi tıklatın.
3. Açılan listeden bir tahsilat mektubu sırası seçin. Bu deftere nakil profilini kullanarak hareketler için tahsilat mektupları oluşturmak istemiyorsanız ilgili alanı boş bırakın.  
4. **Tablo kısıtlamaları** sekmesini genişletin, tahsilat mektuplarını işleme biçimini değiştirmek için. Bu alan **Evet** olarak ayarlanırsa, bu deftere nakil profili için tahsilat mektupları oluşturulur.  

## <a name="create-collection-letters"></a>Tahsilat mektupları oluştur
1. **Gezinti bölmesi > Modüller > Alacak ve tahsilatlar> Tahsilat mektubu > Tahsilat mektuplarını oluştur**'a gidin.
2. Tahsilat mektuplarının hareket türlerini seçin. Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.  
3. **Tahsilat mektubu** alanında bir seçenek belirleyin.
4. **Tahsilat mektubu tarihi** alanında, tahsilat mektubu tarihini girin.
5. **Kullanılacak deftere nakil profili:** seçeneğini **Seç** olarak değiştirdiyseniz, bir deftere nakil profili seçin. İki deftere nakletme profili seçeneği vardır:   

   - **Hesap** – Her vade farkı dekontu için müşteri hesabına atanmış deftere nakil profilini kullan.   
   - **Seçim** – **Deftere nakil profili** alanında seçtiğiniz deftere nakil profilini kullanın.  

6. **Eklenecek kayıtlar** bölümünü genişletin.
7. **Filtre**'yi seç.
8. **Ölçütler** alanına bir Müşteri kodu girin. Örneğin, 'TR-001' girin.
9. **Tamam**'ı seçin.
10. **Tamam**'ı seçin.

## <a name="print-collection-letters"></a>Tahsilat mektuplarını yazdırma
1. **Gezinti bölmesi > Modüller > Alacak ve tahsilatlar> Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle**'ye gidin.
2. **Durum** alanında, **Oluşturuldu** yu seçin.
3. **Yazdırıldı** alanında, **Yazdırılmadı**'yı seçin.
4. **Yazdır**'ı seçin.
5. **Tahsilat mektubu dekontu**'nu seçin.
6. **Parametreler** bölümünde, deftere nakiller için fatura kesme tarihini girin.
7. **Eklenecek kayıtlar** bölümünü genişletin ve tahsilat mektubu dekontuyla ilgili ayrıntıları girin.
8. Tahsilat mektubunu yazdırmak için **Tamam**'ı seçin.
9. Tahsilat mektubunu deftere nakletme.

    1. **Naklet**'i seçin.
    1. Tahsilat mektubu için deftere nakil tarihini girin.
    1. **Eklenecek kayıtlar** bölümünü genişletin.
    1. **Tamam**'ı seçin.
    1. **Durum** alanında, **Deftere nakledildi**'yi seçin.
    1. **Yazdırılan** alanında bir seçenek belirleyin.

## <a name="control-collection-letters-at-the-customer-level"></a>Müşteri düzeyinde tahsilat mektuplarını denetleyin
Tahsilat mektupları hareket düzeyinde ayarlanmışsa, hareketin yaşlanmasına bağlı olarak, bir müşteri için birden fazla mektup oluşturulabilir. Hareketler farklı mektup sıralarında görünüyorsa, müşteri için her vadesi geçmiş hareket grubu için ayrı tahsilat mektupları oluşturulur. Bu nedenle, örneğin bir müşteri vadesi 60 gün geçmiş hareketler için bir tahsilat mektubu ve vadesi 90 gün geçmiş hareketler için başka bir tahsilat mektubu alabilir. 

Her tahsilat mektubu bir tahsilat mektubu koduyla da ilişkilendirilir. Tahsilat mektubu kodu bireysel hareketlerle ilişkilendirilir ve her hareket için sonraki tahsilat mektubunun ne zaman oluşturulması gerektiğini belirlemek üzere kullanılır. Örneğin, bir hareketin vadesi 30 günden uzun süre geciktiyse, tahsilat mektubu kodu bir sonraki tahsilat mektubunu hareket vadesi 60 geciktiğinde gönderilmek üzere (bundan önce ödenmezse) belirler. 

Tahsilat mektupları müşteri düzeyinde de ayarlanabilir. Bu durumda, her bir hareketin tahsilat mektubu kodu izlenir tahsilat mektubu işleme, müşteri için kaydedilmiş tek bir tahsilat mektubu düzeyini temel alır. Tek bir tahsilat mektubu, müşteri için tarihi geçmiş olan tüm hareketleri içerir. Mehil gün sayısı müşteri düzeyinde şimdi izlendiği için sıradaki bir sonraki tahsilat mektubunun vade erteleme gün sayısı geçene kadar sonra son tahsilat mektubu hareketleri süresi sona erene olsa da bir sonraki tahsilat mektubu gönderilmeyecek gönderildi. Bu seçenek, her müşteriye göndermeniz gereken tahsilat mektuplarının sayısını azaltmaya yardımcı olur.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Tahsilat mektuplarının kontrol edileceği müşteriyi müşteri düzeyinde ayarlayın
1.  **Gezinti bölmesi > Modüller > Kredi ve tahsilatlar > Kurulum > Alacak hesabı parametreleri**'ne gidin ve **Tahsilatlar** sekmesini seçin. 
2.  **Her seferinde tahsilat mektubu oluştur**'u **Müşteri**'ye değiştirin. 
3.  **Gezinti bölmesi > Modüller > Alacak ve tahsilatlar> Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle**'ye gidin. Bir müşteri için tüm tarihi geçmiş hareketler içeren tek bir tahsilat mektubu oluşturulacaktır.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak faturalarını yoksay
Tahsilat mektuplarına dahil edilecek hareketlerde ödemeler ve alacak notu dahil ederseniz, bir tahsilat mektubunu tetikleyebilecek ödemeler veya alacak notlarına sahip olabilirsiniz. Ödemeler ve alacak notlarının tahsilat mektubu kodunu nasıl kontrol edebileceğini, **Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** parametresinin değerini değiştirerek kontrol edebilirsiniz. 

Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak faturalarını yoksaymak için şunu yapın.

1. **Gezinti bölmesi > Modüller > Kredi ve tahsilatlar > Kurulum > Alacak hesabı parametreleri**'ne gidin ve **Tahsilatlar** sekmesine tıklayın. 
2. **Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay**'ın değerini **Evet** olarak değiştirin.
