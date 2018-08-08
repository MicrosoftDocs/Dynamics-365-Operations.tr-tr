--- 
title: "RFQ tekliflerini girip karşılaştırma ve işi verme"
description: "Bu prosedürde bir RFQ'ya yanıtların nasıl girileceği, tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından teklif için satıcılardan birinin nasıl seçileceği gösterilmiştir."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>RFQ tekliflerini girip karşılaştırma ve işi verme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde bir RFQ'ya yanıtların nasıl girileceği, tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından teklif için satıcılardan birinin nasıl seçileceği gösterilmiştir. Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz. Başlamadan önce, en az iki satıcıya gönderilmiş iki satır içeren bir RFQ'ya sahip olmanız gerekir. Bunun oluşturulması için bir ön şart olarak "Teklif için bir talep oluştur" prosedürünü yürütebilirsiniz. Bu prosedürü yürütmeden önce puanlama ölçütlerini belirlemeniz gerekir.


## <a name="enter-a-reply-from-a-vendor"></a>Bir satıcı yanıtı girin.
1. Tedarik ve kaynak atama > Teklif talepleri > Tüm teklif talepleri öğesine gidin.
2. Gönderilmiş durumuna sahip bir RFQ seçin ve Teklif talebi olay numarası üzerindeki bağlantıyı tıklayın.
    * RFQ en az 2 satıcıya gönderilmiş olmalıdır.  
3. Satıcıların listesine gitmek için Başlığı tıklayın.
4. RFQ için bir yanıt girmek istediğiniz satıcıyı seçin.
5. Yanıt gir düğmesini tıklayın.
6. Eylem Bölmesinde, Yanıtla öğesine tıklayın.
7. Verileri yanıta kopyala düğmesini tıklayın.
    * Bu eylem seçili verileri, örneğin, RFQ olayındaki miktarları RFQ yanıtına kopyalar. Alternatif olarak, bu eylemi atlayabilir ve yanıtı düzenlerken tüm yanıt alanlarını el ile doldurabilirsiniz.  
8. Düzenle öğesine tıklayın.
9. Birim fiyatı alanına bir sayı girin.
10. Başka bir teklif satırı seçin.
11. Birim fiyatı alanına bir sayı girin.

## <a name="score-the-bid"></a>Teklifi puanlama
1. Teklif puanlamasına gitmek için Başlığı tıklayın.
2. Teklif puanlama bölümünü genişletin.
3. Puan alanına, bir puanlama ölçütü için bir sayı girin.
    * Fare imlecini bir puanlama ölçütünün üzerine getirdiğinizde, puanınızın bulunması gereken aralığı gösteren bir araç ipucu açılır. Bu demoda tüm ölçütler için 1 ile 5 arasında bir sayı ekleyebilirsiniz.  
4. Başka bir puanlama ölçütünü seçin.
5. Puan alanına bir sayı girin.
6. Anketler bölümünü genişletin.
    * RFQ olayı, satıcılara gönderilen bir ankete sahipse, satıcıların yanıtlarını anket bölümüne girebilirsiniz.  
7. Sayfayı kapatın.

## <a name="enter-a-reply-for-another-vendor"></a>Başka bir satıcı için yanıt girme
1. Bir az önce yanıt girdiğiniz satıcıyı silerek ve ardından bir sonraki satıcı için satırı seçerek bir sonraki satıcıyı seçin.
2. Listede, istenen kaydı bulun ve seçin.
3. Yanıt gir düğmesini tıklayın.
4. Verileri yanıta kopyala düğmesini tıklayın.
5. Düzenle öğesine tıklayın.
6. Birim fiyatı alanına bir sayı girin.
7. Başka bir teklif satırı seçin.
8. Birim fiyatı alanına bir sayı girin.

## <a name="score-the-second-bid"></a>İkinci teklifi puanlama
1. Teklif puanlamasına gitmek için Başlığı tıklayın.
2. Puan alanına bir sayı girin.
3. Listede, istenen kaydı bulun ve seçin.
4. Puan alanına bir sayı girin.

## <a name="compare-the-replies"></a>Teklifleri karşılaştırma
1. Eylem Bölmesinde, Genel öğesine tıklayın.
2. Yanıtları karşılaştır düğmesini tıklayın.
3. Sıralama alanına bir sayı girin.
    * Bu sayfada başlık ve satırlarıyla birlikte teklifler ve başlık seviyesinde toplam puan gösterilir. Satırları, karşılaştırabilir satırlar birbirinin yanına gelecek şekilde ızgarada sıralayarak karşılaştırabilirsiniz. Bu bilgiler ayrıca şunları içerir:   Miktar: Satıcı tarafından teklif edilen miktar. Bu miktar, RFQ tarafından belirtilen miktara eşit olmayabilir.   Net miktar: Bir satıcı tarafından satırda belirtilen maddeler için iskontolar çıkarıldıktan sonra teklif edilen fiyattır.   Sapma: Teklif başlığında veya satırında belirtilen teslimat tarihinin RFQ başlığında veya RFQ satırında talep edilen teslimat tarihine göre, gün cinsinden sapma miktarı.   Her bir teklif için bira aralık girebilirsiniz.  
4. Sıralamak istediğiniz diğer tekliflerin başlık satırlarını seçin.
5. Sıralama alanına bir sayı girin.
6. Kaydet'e tıklayın.

## <a name="reject-a-bid"></a>Bir teklifi reddetme
1. Reddetmek istediğiniz teklifin başlık satırını seçin.
    * Aynı anda sadece bir teklifi veya bir teklif içindeki satırları kabul edebilir, reddedebilir veya iade edebilirsiniz.  
2. İşaret onay kutusunu seçin.
    * Teklif başlığındaki seçim kutusunu İşaretle seçimini yaparsanız tüm satırlar işaretlenecektir. Ayrıca, reddetmek veya kabul etmek için bir teklif içindeki satırların bir alt kümesini de işaretlemeyi seçebilirsiniz. Bir satıcının teklifinin bir RFQ'nun bazı satırları için kabul edilmesi ve ardından diğer RFQ satırlarının başka bir satıcıya verilmesi mümkündür, ancak aynı anda bir teklif olacak şekilde bunu 2 adımda gerçekleştirmeniz gerekir. Başka satırlar varsa, sadece orijinal teklif satırını veya başka bir satırı kabule edebilirsiniz, her ikisini aynı anda kabul edemezsiniz.  
3. Reddet düğmesini tıklayın.
4. İletişim kutusunu açmak için Parametreler'i tıklatın
5. Reddetme gerekçesi alanında, bir değer girin veya bir değer seçin.
    * Reddetme nedeni cevaba kaydedilecektir.  
6. Tamam'a tıklayın.
7. Tamam'a tıklayın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.
10. Sayfayı yenileyin.

## <a name="accept-a-bid"></a>Bir teklifi kabul etme
1. Kabul etmek istediğiniz teklifi seçin ve ardından Teklif talebi alanında bağlantıyı tıklayın.
2. Eylem Bölmesinde, Yanıtla öğesine tıklayın.
3. Kabul et düğmesini tıklatın.
    * Belirli satırları işaretler ve belirli satırları işaretlemezseniz, kabul eylemi sadece işaretlenmiş satırları içerecektir. Teklifteki tüm satırları kabul etmek isterseniz, satırları işaretlemenize gerek yoktur.  
4. İletişim kutusunu açmak için Parametreler'i tıklatın
    * Bu da teklifin kabul edilmesi için bir gerekçe kaydetmenize olanak verir. Gerekçe, teklif üzerine kaydedilir.  
5. Kabul gerekçesi alanında, bir değer girin veya bir değer seçin.
6. Tamam'a tıklayın.
7. Tamam'a tıklayın.
    * Tamam düğmesini tıkladığınızda RFQ kabulüne dahil edilen satırlara dayalı olarak bir satın alma emri oluşturulur. Henüz işlenmemiş (kabul edilmiş, reddedilmiş veya iade edilmiş) başka teklifler varsa sistem, kalan teklifleri reddetmeniz için bir mesaj görüntüler.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Oluşturulmuş bir satın alma emrini görüntüleme
1. Eylem Bölmesinde, Genel öğesine tıklayın.
2. Satın alma siparişini tıklatın.
    * Burada, teklifi kabul ettiğinizde oluşturulmuş olan satın alma emrini görebilirsiniz.  
3. Sayfayı kapatın.
4. Sayfayı kapatın.
5. Sayfayı kapatın.
6. Sayfayı kapatın.


