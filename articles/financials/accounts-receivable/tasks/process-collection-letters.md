---
title: Tahsilat mektuplarını işleme
description: Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549641"
---
# <a name="process-collection-letters"></a>Tahsilat mektuplarını işleme

[!include [banner](../../includes/banner.md)]

Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir. Bu görevde USMF demo şirketi kullanılmaktadır.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Deftere nakil profilinde bir tahsilat mektubu sırası ayarlama
1. **Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri**'ne gidin.
2. **Düzenle**'yi tıklatın.
3. Açılan listeden bir tahsilat mektubu sırası seçin. Bu deftere nakil profilini kullanarak hareketler için tahsilat mektupları oluşturmak istemiyorsanız ilgili alanı boş bırakın.  
4. Tablo kısıtlaması sekmesini genişletin, tahsilat mektuplarını işleme biçimini değiştirmek için. Bu alan **Evet** olarak ayarlanırsa, bu deftere nakil profili için tahsilat mektupları oluşturulur.  

## <a name="create-collection-letters"></a>Tahsilat mektupları oluştur
1. **Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektupları oluştur**'a gidin.
2. Tahsilat mektuplarının hareket türlerini seçin. Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.  
2. **Tahsilat mektubu** alanında bir seçenek belirleyin.
3. Tahsilat mektubunun tarihini girin.
4. **Kullanılacak deftere nakil profili:** seçeneğini **Seç** olarak değiştirdiyseniz, bir deftere nakil profili seçin. İki deftere nakletme profili seçeneği vardır:   
   - **Hesap** – Her vade farkı dekontu için müşteri hesabına atanmış deftere nakil profilini kullan.   
   - **Seçim** – **Deftere nakil profili** alanında seçtiğiniz deftere nakil profilini kullanın.  
5. **Eklenecek kayıtlar** bölümünü genişletin.
6. **Filtrele** öğesine tıklayın.
7. **Ölçütler** alanına bir Müşteri kodu girin. Örneğin, 'TR-001' girin.
8. **Tamam** seçeneğini tıklatın.
9. **Tamam** seçeneğini tıklatın.

## <a name="print-collection-letters"></a>Tahsilat mektuplarını yazdırma
1. **Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle**'ye gidin.
2. **Durum** alanında, **Oluşturuldu**yu seçin.
3. **Yazdırıldı** alanında, **Yazdırılmadı**'yı seçin.
4. **Yazdır**'ı tıklatın.
5. **Tahsilat mektubu dekontu**'nu tıklatın.
6. **Eklenecek kayıtlar** bölümünü genişletin.
7. Deftere nakiller için bir fatura kesme tarihi girin.
8. Tahsilat mektubunu yazdırmak için **Tamam**'ı tıklatın.
9. Tahsilat mektubunu deftere nakletme.
   1. **Naklet**'e tıklayın.
   2. Tahsilat mektubu için deftere nakil tarihini girin.
   3. **Eklenecek kayıtlar** bölümünü genişletin.
   4. **Tamam** seçeneğini tıklatın.
   5. **Durum** alanında, **Deftere nakledildi**'yi seçin.
   6. **Yazdırılan** alanında bir seçenek belirleyin.

## <a name="control-collection-letters-at-the-customer-level"></a>Müşteri düzeyinde tahsilat mektuplarını denetleyin
Her bir hareket için tahsilat mektup kodunun izlenmesi için tahsilat mektuplarını ayarlayabilirsiniz, ancak tahsilat mektubu işleme, müşteri için kaydedilmiş tek bir tahsilat mektubu düzeyine dayanacaktır. Tek bir tahsilat mektubu, müşteri için tarihi geçmiş olan tüm hareketleri içerir. Mehil gün sayısı müşteri düzeyinde şimdi izlendiği için sıradaki bir sonraki tahsilat mektubunun vade erteleme gün sayısı geçene kadar sonra son tahsilat mektubu hareketleri süresi sona erene olsa da bir sonraki tahsilat mektubu gönderilmeyecek gönderildi. Bu seçenek, müşteri başına gönderilecek tahsilat mektuplarının sayısını azaltır. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Tahsilat mektuplarının kontrol edileceği müşteriyi müşteri düzeyinde ayarlayın
1.  **Kredi ve tahsilatlar > Kurulum > Alacak hesabı parametreleri**'ne gidin ve **Tahsilatlar** sekmesine tıklayın. 
2.  **Her seferinde tahsilat mektubu oluştur**'u **Müşteri**'ye değiştirin. 
3.  **Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle**'ye gidin. Bir müşteri için tüm tarihi geçmiş hareketler içeren tek bir tahsilat mektubu oluşturulacaktır.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak faturalarını yoksay
Tahsilat mektuplarına dahil edilecek hareketlerde ödemeler ve alacak notu dahil ederseniz, bir tahsilat mektubunu tetikleyebilecek ödemeler veya alacak notlarına sahip olabilirsiniz. Ödemeler ve alacak notlarının tahsilat mektubu kodunu nasıl kontrol edebileceğini, **Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** parametresinin değerini değiştirerek kontrol edebilirsiniz. 

Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak faturalarını yoksaymak için şunu yapın.
1. **Kredi ve tahsilatlar > Kurulum > Alacak hesabı parametreleri**'ne gidin ve **Tahsilatlar** sekmesine tıklayın. 
2. **Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay**'ın değerini **Evet** olarak değiştirin.
