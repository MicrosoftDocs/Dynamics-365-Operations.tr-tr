---
title: RFQ tekliflerini girip karşılaştırma ve işi verme
description: Bu makalede bir teklif talebine (RFQ) yanıtların nasıl girileceği, tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından sözleşme için satıcılardan birinin nasıl seçileceği açıklanmıştır.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3ef754f2d5d58254a7c6f0e572115f8a2981ad9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893395"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>RFQ tekliflerini girip karşılaştırma ve işi verme

[!include [banner](../../includes/banner.md)]

Bu makalede bir teklif talebine (RFQ) yanıtların nasıl girileceği, tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından sözleşme için satıcılardan birinin nasıl seçileceği açıklanmıştır. Bu yordamı **USMF** demo veri şirketinde kullanabilirsiniz.

Bu yordama başlamadan önce, en az iki satıcıya gönderilmiş ve iki satır içeren bir RFQ'ya sahip olmanız gerekir. Bu RFQ'yu oluşturmak için [Teklif talebi oluşturma](create-request-quotation.md) yordamını tamamlayın. Bu prosedürü tamamlamadan önce puanlama ölçütlerini belirlemeniz gerekir.

Teklifi satıcı veya tedarik uzmanı olarak girebilirsiniz. Daha fazla bilgi için bkz. [Satıcı işbirliğini ayarlama ve sürdürme](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Bir satıcı olarak yanıt girme

1. **Satıcı işbirliği \> Çalışma alanları \> Satıcı teklifi**'ne gidin.
2. **Yeni teklif davetleri** listesinde, henüz gönderilmiş bir RFQ bulun. Neyin istenmiş olduğunu incelemek için RFQ'yu seçin.
3. Eklenmiş ekleri gözden geçirmek için **RFQ ekleri**'ni seçin.
4. Alanları düzenlenebilir yapmak için **Teklif**'i seçin. **Teklif ilerlemesi** alanının **Satıcı güncelleştiriliyor** olarak ayarlandığından emin olun.
5. Başlık ve satırlara, teklif yanıtındaki değerleri girin.
6. Teklife ek eklenmesi gerekiyorsa, **Teklif ekleri**'ni seçin.
7. Herhangi bir belge gerekip gerekmediğini görmek için **Teklif kılavuzu maddeleri** hızlı sekmesini seçin.
8. RFQ'nun değiştirilip değiştirilmediğini görmek için **Değişiklikler** hızlı sekmesini seçin.
9. **Soru formu** hızlı sekmesini seçin. Burada görünen soru formlarının yanıtlanması gerekir.
10. Satırla ilgili genişletilmiş bilgileri görüntülemek için **Satır ayrıntıları** hızlı sekmesini seçin.
11. Girilmiş değerleri orijinal RFQ değerlerine sıfırlamanız gerekiyorsa **RFQ'dan Sıfırla** seçeneğini belirleyin.
12. Teklifi istediğiniz zaman kaydedebilir ve sona erme tarihi ve saatinin geçmemiş olması koşuluyla daha sonra ek işlem yapabilirsiniz. Bu durumda, teklifi **Satıcı teklifi** çalışma alanındaki **Devam eden teklifler** listesinde bulabilirsiniz.
13. Teklif gönderilmeye hazır olduğunda **Gönder**'i seçin. Teklif vermek istemiyorsanız **Reddet**'i seçin Gönderilen teklifler **Satıcı teklifi** çalışma alanındaki **Gönderilen teklifler** listesinde bulunur.  
14. Teklif gönderildikten sonra, zaman aşımı tarihi ve saatinden önce istediğiniz zaman geri çağırabilirsiniz. Bir teklif geri çağrıldığında gönderilmiş olarak değerlendirilmez. Teklif tedarik departmanı tarafından kabul edildiğinde veya reddedildiğinde **Satıcı teklifi** çalışma alanındaki **Kazanılan teklifler** veya **Kaybedilen teklifler** listesinde görünür.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Tedarik uzmanı olarak bir satıcıdan gelen yanıtı girme

1. Satıcı tekliflerini düzenleme izninin ayarlandığından emin olun. **Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama parametrelerine** gidin. **Teklif talebi** sekmesinde, **Satınalmacı satıcı teklifini düzenleyebilir** seçeneğini **Evet** olarak ayarlayın.
2. **Tedarik ve kaynak atama \> Teklif talepleri \> Tüm teklif talepleri**'ne gidin.
3. **Gönderildi** durumuna sahip bir RFQ seçin ve **Teklif talebi olayı** alanındaki bağlantıyı seçin.
4. **Yanıtları yönet**'i seçin. Beliren sayfa, teklife davet edilen her satıcı için bir RFQ gösterir.
5. Yanıtmamış bir RFQ seçin. ( **Yanıt ilerlemesi** alanı **Başlatılmadı** olarak ayarlanmalıdır.)
6. **Düzenle \> RFQ yanıtını düzenle**'yi seçin. **RFQ yanıtı** sayfası görüntülenir. Tedarik uzmanı olarak, şimdi satıcı adına yanıt girebilirsiniz. **Teklif ilerlemesi** alanının **Satınalmacı güncelleştiriliyor** olarak ayarlandığından emin olun.  
7. Teklif verilerini girin. Tamamladıktan sonra **Gönder**'i seçin.

## <a name="score-the-bids"></a>Teklifleri puanlama

1. **Tüm teklif talepleri** sayfasında, yanıtlarını puanlamak istediğiniz RFQ olayını seçin.
2. **Yanıtları yönet**'i seçin.
3. Puanlanacak yanıtı seçin.
4. Teklif için puanı görüntüleyebilmek üzere **Başlık**'ı seçin.
5. **Teklif puanı** hızlı sekmesinde **Puan** alanına, bir puanlama ölçütü için bir sayı girin. Fare imlecini bir puanlama ölçütünün üzerine getirdiğinizde, puanınızın yer alması gereken aralığı gösteren bir araç ipucu açılır. Bu demoda tüm puanlama ölçütleri için 1 ile 5 arasında bir sayı girebilirsiniz.  
6. Başka bir puan ölçütü için 5. adımı yineleyin.
7. RFQ olayı, satıcılara gönderilen bir soru formuna sahipse, satıcıların yanıtlarını **Soru formları** hızlı sekmesinden girebilirsiniz.
8. Sayfayı kapatın.
9. Tüm diğer teklifler için 1 ile 8 arasındaki adımları yineleyin.

## <a name="compare-the-replies"></a>Teklifleri karşılaştırma

1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Yanıtları karşılaştır**'ı seçin.
2. **Sıralama** alanına bir sayı girin.  
    - Bu sayfada başlık ve satır bilgileriyle birlikte teklifler ve başlık seviyesinde toplam puan gösterilir. Satırları, karşılaştırabilir satırlar birbirinin yanına gelecek şekilde ızgarada sıralayarak karşılaştırabilirsiniz. Aşağıdaki bilgiler de eklenir:
    - **Miktar**: Satıcı tarafından teklif edilen miktar. Bu miktar, RFQ'da belirtilen miktara eşit olmayabilir.
    - **Net tutar**: Satıcı tarafından satırda belirtilen maddeler için iskontolar çıkarıldıktan sonra teklif edilen fiyat.
    - **Sapma**: Teklif başlığında veya satırında belirtilen teslimat tarihinin RFQ başlığında veya satırında talep edilen teslimat tarihine göre, gün cinsinden sapma miktarı. Her bir teklif için bira aralık girebilirsiniz.  
3. Sıralamak istediğiniz diğer tekliflerin başlık satırlarını seçin.
4. **Sıralama** alanına bir sayı girin.
5. **Kaydet**'i seçin.

## <a name="reject-a-bid"></a>Bir teklifi reddetme

1. Reddetmek istediğiniz teklifin başlık satırını seçin. Aynı anda sadece bir teklifi veya bir teklifteki satırları kabul edebilir, reddedebilir veya iade edebilirsiniz.
2. **İşaretle** onay kutusunu seçin.  
    - Teklif başlığındaki **İşaretle** onay kutusunu seçerseniz tüm satırlar işaretlenecektir. Teklifteki bazı satırları reddetmek veya kabul etmek için, yalnızca bu satırları işaretleyebilirsiniz. Ek olarak, bir RFQ'daki bazı satırlar için bir satıcının teklifini kabul edebilir ve diğer RFQ satırlarını farklı bir satıcıya verebilirsiniz. Ancak, bir seferde tek bir teklif yapmanız gerekir.  
    - Başka satırlar varsa, orijinal teklif satırını veya başka bir satırı kabule edebilirsiniz, her ikisini aynı anda kabul edemezsiniz.  
3. **Reddet**'i seçin.
4. **Parametreleri** seçin ve ardından **Reddetme nedeni** alanında, teklifi reddetme nedeninizi girin veya seçin. Neden yanıtta saklanır.  
5. **Tamam**'ı seçin.
6. **Tamam**'ı seçin.

## <a name="accept-a-bid"></a>Bir teklifi kabul etme

1. Kabul etmek istediğiniz teklifi seçin ve ardından **Teklif talebi** alanındaki bağlantıyı tıklayın. **Teklif talebi yanıtlarını karşılaştır** sayfasında iseniz, vurgulanmış teklif sistemin Kabul etme eylemi sırasında göz önünde bulundurduğu tekliftir. Bir seferde yalnızca bir teklifin satırlarını kabul edebilirsiniz.  
2. Eylem Bölmesinde, **Yanıtla**'yı seçin.
3. **Kabul et**'i seçin. Yalnızca belirli satırları işaretlediyseniz, Kabul et eylemi yalnızca bu satırları dahil eder. Teklifteki tüm satırları kabul etmek isterseniz, satırları işaretlemenize gerek yoktur.  
4. **Parametreler**'i seçin ve ardından **Kabul etme nedeni** alanında, teklifi kabul etme nedeninizi girin veya seçin. Neden teklifte saklanır.  
5. **Tamam**'ı seçin.
6. **Tamam**'ı seçin. **Tamam**'ı seçtiğinizde RFQ kabulüne dahil edilen satırlara dayalı olarak bir satın alma emri oluşturulur. Henüz işlenmemiş (kabul edilmiş, reddedilmiş veya iade edilmiş) başka teklifler varsa sistem bunları reddetmeniz için bir mesaj görüntüler.  

## <a name="view-the-purchase-order-that-is-generated"></a>Oluşturulmuş bir satın alma emrini görüntüleme

Eylem Bölmesi'ndeki **Genel** sekmesinde, **Satınalma emri**'ni seçin. Görüntülenen sayfada teklifi kabul ettiğinizde oluşturulmuş olan satın alma emrini görebilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]