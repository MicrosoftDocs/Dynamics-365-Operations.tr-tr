---
title: Mali yılı kapatma
description: Bu yordam, bakiyeleri yeni bir mali yıla aktaran yıl sonu kapanış işlemini adım adım açıklar.
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779825"
---
# <a name="close-the-fiscal-year"></a>Mali yılı kapatma

[!include [banner](../../includes/banner.md)]

Bu yordam, bakiyeleri yeni bir mali yıla aktaran yıl sonu kapanış işlemini adım adım açıklar.


## <a name="validate-year-end-close-parameters"></a>Yıl sonu kapatma parametrelerini doğrulama
1. **Gezinti bölmesi > Modüller > Genel muhasebe > Genel muhasebe ayarı > Genel muhasebe parametreleri**'ne gidin.
2. **Mali yıl kapanışı** bölümünü genişletin.
3. **Aktarmadan sonra Yıl kapanışı hareketlerini sil** seçeneği için **Evet** veya **Hayır**'ı seçin.
    
Mali yıl zaten kapanmışsa ve yıl sonu kapanışı tekrar çalıştırılıyorsa bu ayar önemlidir. **Evet** olarak ayarlanırsa, önceki yıl sonu kapanışına ait fiş silinecek ve tüm hesap başlangıç bakiyeleri için yeni bir fiş oluşturulacaktır. **Hayır** olarak ayarlanırsa, önceki fiş kalacak ve yeni fiş yalnızca son yıl sonu kapanışından sonra nakledilmiş ayarlama girişleri için oluşturulacaktır.

4. **Aktarma sırasında kapanış hareketleri oluştur** seçeneği için **Evet**'i veya **Hayır**'ı seçin.

**Evet** olarak ayarlanırsa, iki hareket oluşturulur. İlk fiş tüm genel muhasebe hareketlerini sıfıra getirmek için kapatılan mali yılda oluşturulur, ikinci fiş ise başlangıç bakiyeleri için bir sonraki mali yılda oluşturulur. **Hayır** olarak ayarlanırsa başlangıç bakiyeleri için bir sonraki mali yılda tek bir fiş oluşturulur.  

5. **Mali yıl durumunu kalıcı olarak kapatıldı olarak ayarla** için **Evet**'i veya **Hayır**'ı seçin.

**Evet** olarak ayarlanırsa mali yıl durumu, **Kalıcı olarak kapatıldı** olarak belirlenir. Kalıcı olarak kapatılan bir yıl yeniden açılamadığından en iyi uygulama bu seçeneği **Hayır** olarak ayarlamak olacaktır.  

6. **Yıl sonu kapanışı sırasında Fiş numarası doldurulmalıdır** seçeneği için **Evet**'i veya **Hayır**'ı seçin.

**Evet** olarak ayarlanırsa, fiş numarası yıl sonu kapanış işlemi sırasında el ile girilmelidir. Bu fiş numarasını oluşturmak için bir numara serisi kullanılmaz. En iyi uygulama bunu **Evet** olarak ayarlamaktır.  

7. Sayfayı kapatın.
8. **Genel muhasebe > Yakın dönem > Yıl sonu kapanışı**'na gidin.
9. Yıl sonu kapanış şablonu oluşturmak için **Yeni**'ye tıklayın.

Yıl sonu kapanışını çalıştırmak amacıyla tüzel kişilikler grubu için bir şablon oluşturulabilir. Bu şablon yıldan yıla yeniden kullanılabilir.  

10. **Grup adı** alanında yıl sonu kapanış şablonunun adını girin.
11. **Mali takvim** alanında, şablonun oluşturulacağı mali yılı seçin.

Yıl sonu kapanış şablonunda yalnızca aynı mali yılı kullanan tüzel kişilikler bir arada gruplandırılabilir. Bunun nedeni yıl sonu kapanışının tarih yerine mali yılın seçilmesiyle gerçekleştirilmesidir.  

12. **Eylem Bölmesi**'nde, **Kaydet** öğesine tıklayın.
13. **Tüzel kişilikler** bölmesinde, bu şablon için tüzel kişileri seçmek üzere **Ekle**'ye tıklayın.
    
Tüzel kişilikler, tüzel kişilikleri seçerek veya bir kurumsal hiyerarşi seçerek eklenebilir. Yalnızca aynı mali takvime sahip kurumsal hiyerarşi ile seçilen tüzel kişilikler eklenecektir.  

14. Tüzel kişilikleri veya kurumsal hiyerarşiyi seçin.
15. **Tamam**'a tıklayın.
16. **Bilanço boyutlarını aktar** öğesinde **Evet** ya da **Hayır**'ı seçin.

En iyi uygulama bu seçeneği Bilanço hesapları için **Evet** olarak ayarlamaktır. Bu, bilanço hesapları için başlangıç bakiyeleri oluşturulurken deftere nakledilmiş hareketler üzerinden mali boyutları günceller. Kar ve zarar hesapları için bilançolar Yedek akçelere taşındığında mali boyutları güncelleştirmeyi seçebilirsiniz (**Tümünü kapat**) veya mali boyutları farklı bir boyut değeri ile değiştirmeyi seçebilirsiniz (**Birini kapat**). **Birini kapat**'ı seçerseniz, her boyut için belirli bir boyut değeri tanımlayabilir veya boş bırakmayı seçebilirsiniz.  

17. **Kaydet**'e tıklayın.
18. **Eylem Bölmesi**'nde **Mali kapanışı çalıştır**'ı seçerek yıl sonu kapanışını başlatın. Yıl sonu kapanışı seçilen şablon için çalıştırılacaktır.  
19. Yıl sonu kapanışını çalıştırmak için şablondan tüzel kişiliklerin tamamını veya alt kümesini seçin.

İlk önce yıl sonu kapanışı çalıştırıldığında çoğu kuruluş başlangıç bakiyelerini almak için şablon dahilindeki tüm tüzel kişilikler için yıl sonu kapanışını çalıştırmayı tercih edebilir. Ayarlama girişleri bundan sonra yapılırsa yalnızca ayarları yapılan tüzel kişilikler için yıl sonu kapanışını çalıştırmayı tercih edebilirsiniz.  

20. **Tamam**'a tıklayın.
21. Yıl sonu kapanışının çalıştırılacağı mali yılı seçin.
22. **Fiş alanı**'na bir değer yazın. Oluşturulan yıl sonu kapanış fişinin bulunmasını kolaylaştırmak için en iyi uygulama mali yılı fiş numarasına dahil etmektir.  
23. Toplu iş modunda çalıştırmak için yıl sonu kapanışı varsayılanları. Uzun süreli işlemler için en iyi uygulama toplu iş modunda çalıştırmaktır. Bu, genel olarak varsayılanın iş modunda kullanılma sebebi olan süreçlerden biridir.  
24. **Tamam**'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
