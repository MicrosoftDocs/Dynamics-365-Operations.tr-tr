---
title: ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 1 - Biçimi tasarlama)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e36a2238ab4c67a2384d6da2a1e2c767414c21a1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684511"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 1 - Biçimi tasarlama)

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için önce bu üç görev kılavuzunu tamamlamalısınız: 

"ER Konfigürasyon sağlayıcısı oluşturma ve etkin olarak işaretleme"

"ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)"

"ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 2 - Model eşleme)"

Ayrıca [Örnek Finansal Boyutlar Web Hizmeti Raporu](https://go.microsoft.com/fwlink/?linkid=862266)'nda bir örnek raporla birlikte şablonu indirmeniz ve yerel bir kopyasını oluşturmanız gerekir.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="create-a-new-report-configuration"></a>Yeni bir rapor konfigürasyonu oluşturma
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.
3. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
4. Yeni alanına, 'Mali boyutlar örnek modeli veri modeline dayalı biçim' yazın.
    * Önceden oluşturulan modeli, yeni raporunuz için veri kaynağı olarak kullanın.  
5. Ad alanına, "Yatay olarak genişletilebilir aralıklarla örnek rapor" yazın.
    * Yatay olarak genişletilebilir aralıklarla örnek rapor  
6. Açıklama alanına, "Dinamik olarak sütunlar ekleyerek Excel çıktısı oluşturma" yazın.
    * Dinamik olarak sütunlar ekleyerek Excel çıktısı oluşturma  
7. Veri modeli tanımı alanında Giriş'i seçin.
8. Konfigürasyon oluştur'u tıklatın.

## <a name="design-the-report-format"></a>Rapor biçimini tasarlama
1. Tasarımcı'ya tıklayın.
2. "Ayrıntıları göster" geçiş düğmesini açın.
3. Eylem Bölmesinde, İçeri Al'a tıklayın.
4. Excel'den içe aktar'a tıklayın.
5. Ekler'e tıklayın.
    * Raporun şablonunu içe aktarın. Bunun için indirdiğiniz Excel dosyasını kullanın.  
6. Yeni'yi tıklatın.
7. Dosya'ya tıklayın.
8. Sayfayı kapatın.
9. Şablon alanına bir değer girin veya seçin.
    * İndirilen şablonu seçin.  
10. Tamam'a tıklayın.
    * Mali boyutlar için (kullanıcı iletişim formunda) seçtiğiniz kadar sütunu olan Excel çıktısını dinamik olarak oluşturmak için yeni bir aralık ekleyin. Her sütun için her bir hücre, tek bir finansal boyutun adını temsil eder.  
11. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
12. Ağaçta, "Excel\Aralık" öğesini seçin.
13. Excel aralık alanına "DimNames" yazın.
    * DimNames  
14. Yineleme yönü alanında "Yatay" öğesini seçin.
15. Tamam'a tıklayın.
16. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<DimNames>: Yatay" öğesini seçin.
17. Yukarı taşı'ya tıklayın.
18. Ağaçta, "Excel = "SampleFinDimWsReport"\Hücre<DimNames>" öğesini seçin.
19. Kes'e tıklayın.
20. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<DimNames>: Yatay" öğesini seçin.
21. Yapıştır'a tıklayın.
22. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<DimNames>: Yatay" öğesini genişletin.
23. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>: Dikey" öğesini genişletin.
24. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>Dikey\Aralık<TransactionLine>: Dikey" öğesini genişletin.
25. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>Dikey\Aralık<TransactionLine>: Dikey" öğesini seçin.
    * Mali boyutlar için (kullanıcı iletişim formunda) seçtiğiniz kadar sütunu olan Excel çıktısını dinamik olarak oluşturmak için yeni bir aralık ekleyin. Her sütundaki her bir hücre, her raporlama hareketi için tek bir finansal boyutun değerini temsil eder.  
26. Aralık Ekle'ye tıklayın.
27. Excel aralık alanına "DimValues" yazın.
    * DimValues  
28. Yineleme yönü alanında "Yatay" öğesini seçin.
29. Tamam'a tıklayın.
30. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Hücre<DimValues>" öğesini seçin.
31. Kes'e tıklayın.
32. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Aralık<DimValues>:Dikey" öğesini seçin.
33. Yapıştır'a tıklayın.
34. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Aralık<DimValues>:Dikey" öğesini genişletin.

## <a name="map-format-elements-to-data-sources"></a>Biçim öğelerini veri kaynaklarıyla eşleme
1. Eşleme sekmesini tıklatın.
2. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli' öğesini genişletin
3. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini genişletin.
4. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini genişletin.
5. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini genişletin.
6. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Aralık<DimValues>:Dikey\Hücre<DimValues>" öğesini seçin.
7. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Kod: Dize' öğesini seçin.
8. Bağla'ya tıklayın.
9. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Aralık<DimValues>:Dikey" öğesini seçin.
10. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini seçin.
11. Bağla'ya tıklayın.
12. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Hücre<Credit>" öğesini seçin.
13. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Alacak: Gerçek' öğesini seçin.
14. Bağla'ya tıklayın.
15. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Hücre<Debit>" öğesini seçin.
16. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Borç: Gerçek' öğesini seçin.
17. Bağla'ya tıklayın.
18. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Hücre<Currency>" öğesini seçin.
19. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Para Birimi: Dize' öğesini seçin.
20. Bağla'ya tıklayın.
21. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Hücre<TransDate>" öğesini seçin.
22. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Tarih: Tarih' öğesini seçin.
23. Bağla'ya tıklayın.
24. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Hücre<TransVoucher>" öğesini seçin.
25. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Fiş: Dize' öğesini seçin.
26. Bağla'ya tıklayın.
27. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Aralık<TransactionLine>: Dikey\Hücre<TransBatch>" öğesini seçin.
28. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Toplu İş: Dize' öğesini seçin.
29. Bağla'ya tıklayın.
30. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>Dikey\Aralık<TransactionLine>: Dikey" öğesini seçin.
31. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini seçin.
32. Bağla'ya tıklayın.
33. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey\Hücre<Batch>" öğesini seçin.
34. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Toplu İş: Dize' öğesini seçin.
35. Bağla'ya tıklayın.
36. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<JournalLine>:Dikey" öğesini seçin.
37. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini seçin.
38. Bağla'ya tıklayın.
39. Ağaçta, "model: Veri modeli Mali boyutlar örnek modeli\Boyutlar ayarı: Kayıt listesi" öğesini genişletin.
40. Ağaçta, "model: Veri modeli Mali boyutlar örnek modeli\Boyutlar ayarı: Kayıt listesi\Kod: Dize" öğesini seçin.
41. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<DimNames>: Yatay\Hücre<DimNames>" öğesini seçin.
42. Bağla'ya tıklayın.
43. Ağaçta, "model: Veri modeli Mali boyutlar örnek modeli\Boyutlar ayarı: Kayıt listesi" öğesini seçin.
44. Ağaçta, "Excel = "SampleFinDimWsReport"\Aralık<DimNames>: Yatay" öğesini seçin.
45. Bağla'ya tıklayın.
46. Ağaçta, "Excel = "SampleFinDimWsReport"\Hücre<CompanyName>" öğesini seçin.
47. Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Şirket: Dize' öğesini seçin.
48. Bağla'ya tıklayın.
49. Kaydet'e tıklayın.
50. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]