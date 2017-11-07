---
title: "Satıcı ödemesini tersine çevirme"
description: "Bu makalede bir ödemenin terse çevrilmesi, silinmesi, geçersiz sayılması ve reddedilmesi arasındaki farklar açıklanmıştır. İlave olarak, bir satıcı çekinin ters çevrilmesi için iki yöntem açıklanmıştır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 736432a7e128f6b7b0d7ed5e0156c0769407bbaa
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="reverse-a-vendor-payment"></a>Satıcı ödemesini tersine çevirme

[!include[banner](../includes/banner.md)]


Bu makalede bir ödemenin terse çevrilmesi, silinmesi, geçersiz sayılması ve reddedilmesi arasındaki farklar açıklanmıştır. İlave olarak, bir satıcı çekinin ters çevrilmesi için iki yöntem açıklanmıştır. 

Bazen, bir satıcı ödemesi deftere nakledildikten sonra ödemenin tersine çevrilmesi gerekir. Ters kayıt işlemleri silme, hükümsüz kılma veya ödeme reddetme işlevlerinden farklıdır. Yalnızca durumu **Oluşturuldu** olan ödemeleri silebilirsiniz. Bu durum, ödemenin ayarlandığınız ancak henüz oluşturulmadığını gösterir. Ödeme yöntemi ne olursa olsun her zaman bu sınırlama uygulanır. Deftere nakledilmemiş çekleri oluşturulduktan sonra ancak deftere nakledilmeden önce geçersiz kılabilirsiniz. Oluşturulan ödeme elektronik fon transferi (EFT) olarak yapıldığında, deftere nakledilmeden önce ödemeyi reddedebilirsiniz. Ödemeyi reddetmek için **Ödeme durumu** değerini değiştirin. Hükümsüz kılınan veya reddedilen bir ödeme **Ödeme durumu** değeri tekrar **Yok** olarak değiştirildikten sonra yeniden oluşturulabilir. 

Bir ödeme deftere nakledildikten sonra ters işlemler kullanılır. Elektronik ortamda yapılan ödemeler deftere nakledildikten sonra tersine çevrilemez. Bunun yerine, satıcının hesabından borcu geri almak üzere ödeme miktarı için yeni bir hareket oluşturulmalıdır. Deftere nakledilen çek işlemlerini tersine çevirmek için iki yöntem kullanılabilir. Bir yöntemde, tersine çevirme işlemleri **Çek** sayfasında **Ödeme ters kaydı** tıklatılarak anında deftere nakledilir. Diğer yöntemde **Çek** sayfasında **Ödeme ters kaydı**'nı tıklattığınızda, ters kayıt bir gözden geçirenin ters kaydı deftere nakledebildiği veya reddettiği Nakit ve banka yönetimi alanında çek ters işlem günlüklerine gönderilir. 

Kuruluşunuzun hangi yöntemi kullandığını öğrenmek için **Nakit ve banka yönetimi parametreleri** sayfasını görüntüleyin. **Ödeme ters işlemleri için inceleme işlemi kullan** seçeneği **Evet** olarak ayarlanmışsa, ters kayıtlar gözden geçirilmek üzere çek ters işlem günlüğüne gönderilir. Aşağıdaki tabloda çek ters işlem yöntemlerinin nasıl farklılık gösterdiği açıklanmaktadır.

| Kuruluşunuzun deftere nakletmeden önce çek tersine çevirmelerini incelemiyorsa                                                                                                                                  | Kuruluşunuzun deftere nakletmeden önce çek tersine çevirmelerini inceliyorsa                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Çek** sayfasında **Tamam**'ı tıklattığınızda çek anında tersine çevrilir.                                                                                                                      | Çek hemen tersine çevrilmez. Gözden geçirilmek üzere bir çek ters işlem günlüğü oluşturulur. Çek ters işlem günlüğü silinirse, çek yeniden tersine çevrilebilir.                                                                                                                                                                                                                                                                |
| Orijinal çek muhasebe girişleri ters çevrilir.                                                                                                                                         | Orijinal çek muhasebesindeki genel muhasebe hesabı girişi deftere nakledilmeyebilir. Orijinal çek günlüğündeki mali boyutları çek ters işlem günlüğünde varsayılan mali boyutlar olarak kullanılır. Bu varsayılan değerleri değiştirebilirsiniz. Çek ters işlem günlüğü deftere nakledildiğinde, Borç hesaplarının ana hesapları değişmiş olabilen deftere nakil profillerinden otomatik olarak girilir. |
| Orijinal çek deftere nakledildiğinde kullanılan muhasebe yapısı hesap yapısı değiştirilmiş olsa bile çek tersine çevirme işlemi için kullanılır. Hesap bileşimi doğrulanmış değildir. | Orijinal çek deftere nakledildikten sonra bir hesap yapısı değiştirildiyse, çek tersine çevirme işlemi yeni bir mali boyut gerekli olabilir. Bu mali boyut, orijinal ödeme günlüğünden otomatik olarak girilmeyebilir. Çek tersine çevirme işlemi deftere nakledildiğinde hesap bileşimi doğrulanır.                                                                                                        |
| Sabit boyutlar, aynı genel muhasebe hesaplarının tersine çevrilmesini sağlamaya yardımcı olmak için tersine çevirme işlemine uygulanmaz.                                                                                      | Sabit boyutlar, deftere nakil sırasında çek ters işlem günlüğüne uygulanır. Mali boyut değeri, sabit boyutların ne zaman tanımlandığına bağlı olarak orijinal çek için muhasebe girişinde var olmayabilir.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Deftere nakledilen çekleri gözden geçirmeden tersine çevirme
Kuruluşunuz, **Çekler** sayfasında **Ödeme ters kaydı**'nı tıklattığınızda çek tersine çevirme işlemlerinin anında deftere nakledilmesini istiyorsa. **Nakit ve banka yönetimi parametreleri** sayfasında, **Ödeme ters işlemleri için inceleme işlemi kullan** seçeneğini **Hayır** olarak ayarlayın. **Çekler** sayfasında, ters çevrilecek çeki ve **Ödeme ters kaydı**'nı seçebilirsiniz. Tarihi girebilir ve ters işlem için bir neden seçebilirsiniz.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Çek ters işlem günlüğünde gözden geçirildikten sonra deftere nakledilen çekleri ters çevirme
Kuruluşunuz çek tersine çevirmelerini deftere nakledilmeden önce gözden geçirmek isterse, gözden geçirme için bir çek ters işlem günlüğü oluşturun ve **Nakit ve banka yönetimi parametreleri** sayfasında, **Ödeme ters işlemleri için inceleme işlemi kullan** seçeneğini **Evet** olarak ayarlayın. **Çekler** sayfasında, ters çevrilecek çeki ve **Ödeme ters kaydı**'nı seçebilirsiniz. Tarihi girebilir ve ters işlem için bir neden seçebilirsiniz. Ayrıca çek ters işlem günlüğünde bir günlük oluşturmak için bir günlük adı seçmeniz de gerekir.

### <a name="review-a-reversal"></a>Ters işlemi inceleme

Ters işlemleri gözden geçirmesi gereken bir kullanıcıysanız, işlemi onaylayabilir veya günlüğü deftere nakledebilir ya da ters işlemi reddedebilir vea günlüğü silebilirsiniz. **Çek ters işlem günlüğü** sayfasında, gözden geçirmek üzere ters işlem günlüğünü seçebilir ve sonra **Satırlar**'ı tıklatabilirsiniz. Tersine çevrilen çeki gözden geçirebilir ve sonra aşağıdaki onay seçeneklerinden birini belirleyebilirsiniz:

-   Ters işlem günlüğünü onaylamak ve deftere nakletmek için **Deftere naklet** veya **Deftere naklet ve aktar**'ı tıklatın.
-   Bir ters işlemi reddetmek için, çek ters işlem günlüğünü silin.

> [!NOTE]
> Günlüğü silerseniz, ters işlem sistemden kaldırılır ancak orijinal çek **Çek** sayfasında kalır. Çekin durumu artık **Bekleyen iptal** şeklinde olmaz.

## <a name="results-of-posting-a-reversal"></a>Ters işlemi deftere nakletmenin sonuçları
Çeke uygulanan ters işlemi deftere naklettiğinizde aşağıdaki olaylar gerçekleşir:

-   Çek durumu **İptal** olarak güncellenir.
-   Ters çevirme işlemi sırasında ters çevirme sayfasında **Mutabakat** seçeneği belirlenirse çek üzerinde mutabakat sağlanır (**Mutabakat sağlandı** seçeneği belirlenir) ve **Hesap mutabakatı** sayfasında görünmez.
-   Ters işlem fişi, çekin verildiği banka hesabına karşılık gelecek ve banka hesabı bakiyesini artıracak şekilde deftere nakledilir.
-   Fiş Genel muhasebe defterine nakledilir.
-   Değişiklik ayrıntıları **Çek** sayfasında **Geçmiş** alan grubunda güncellenir.

> [!NOTE] 
> Şirketlerarası ticari hareket için verilen bir çeke ters işlem uyguladığınızda, mahsup girişleri orijinal hareketten değil şirketlerarası ticaret için muhasebe ayarlarından gelir. Ters işlem uygulanan çek bir satıcı ödemesi için verildiyse, ayrıca aşağıdaki olaylar da oluşur:

-   Ödeme kapanışının yapıldığı faturadaki orijinal ödeme uygulanmaz (kapanış işlemi tersine çevrilir).
-   Ödeme ters işlemi için deftere satıcı hesabına karşılık gelen bir hareket nakledilir ve tersine çevrilen ödeme orijinal ödemeyle eşlenerek kapatılır. Orijinal satıcı ödemesine yönelik olarak **Satıcı hareketleri** sayfasındaki **Son kapatma fişi** ters çevrilen hareketin fiş numarasını gösterecek şekilde güncellenir.

Ters işlem uygulanan çek bir müşteri para iadesi için çıkarıldıysa, ayrıca aşağıdaki olaylar da oluşur:

-   Ödeme ters işlemi için deftere müşteri hesabına karşılık gelen bir hareket nakledilir ve orijinal ödeme ile ödemenin orijinal olarak kapatıldığı belge arasındaki kapanış işlemi tersine çevrilir (negatif ödeme oluşturulur).
-   Ödeme ters işlemi orijinal ödemeye uygulanır. Orijinal müşteri ödemesine yönelik olarak **Müşteri hareketleri** sayfasındaki **Son kapatma fişi** ters çevrilen hareketin fiş numarasını gösterecek şekilde güncellenir.





