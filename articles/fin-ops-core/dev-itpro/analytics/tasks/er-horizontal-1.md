---
title: ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 1 - Biçimi tasarlama)
description: Bu makalede, OPENXML çalışma sayfası (Excel) dosyaları olarak rapor oluşturmak için Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır. (1. Bölüm)
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: 3fa8dcac309220d05225e87fd29ef6b741bfcc54
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290439"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 1 - Biçimi tasarlama)

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için önce bu üç görev kılavuzunu tamamlamalısınız:

"ER Konfigürasyon sağlayıcısı oluşturma ve etkin olarak işaretleme"

"ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)"

"ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 2 - Model eşleme)"

Ayrıca [Örnek Finansal Boyutlar Web Hizmeti Raporu](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx)'nda bir örnek raporla birlikte şablonu indirmeniz ve yerel bir kopyasını oluşturmanız gerekir.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.

## <a name="create-a-new-report-configuration"></a>Yeni bir rapor konfigürasyonu oluşturma

1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, `Financial dimensions sample model` öğesini seçin.
3. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
4. Yeni alanına `Format based on data model Financial dimensions sample model` yazın.
    * Önceden oluşturulan modeli, yeni raporunuz için veri kaynağı olarak kullanın.  
5. İsim alanına `Sample report with horizontally expandable ranges`. yazın.
    * Yatay olarak genişletilebilir aralıklarla örnek rapor  
6. Açıklama alanına `To make Excel output with dynamically adding columns` yazın.
    * Dinamik olarak sütunlar ekleyerek Excel çıktısı oluşturma  
7. Veri modeli tanımı alanında Giriş'i seçin.
8. Konfigürasyon oluştur'u tıklatın.

## <a name="design-the-report-format"></a>Rapor biçimini tasarlama

1. Tasarımcı'ya tıklayın.
2. `Show details` geçiş düğmesini açın.
3. Eylem Bölmesinde, İçeri Al'a tıklayın.
4. Excel'den içe aktar'a tıklayın.
5. Ekler'e tıklayın.
    * Raporun şablonunu içeri aktarın. Bunun için indirdiğiniz Excel dosyasını kullanın.  
6. Yeni'yi tıklatın.
7. Dosya'ya tıklayın.
8. Sayfayı kapatın.
9. Şablon alanına bir değer girin veya seçin.
    * İndirilen şablonu seçin.  
10. Tamam'a tıklayın.
    * Mali boyutlar için (kullanıcı iletişim formunda) seçtiğiniz kadar sütunu olan Excel çıktısını dinamik olarak oluşturmak için yeni bir aralık ekleyin. Her sütun için her bir hücrede, tek bir finansal boyutun adı temsil edilir.  
11. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
12. Ağaçta, `Excel\Range` öğesini seçin.
13. Excel aralık alanına `DimNames` yazın.
    * DimNames  
14. Çoğaltma yönü alanında `Horizontal` seçeneğini belirleyin.
15. Tamam'a tıklayın.
16. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` öğesini seçin.
17. Yukarı taşı'ya tıklayın.
18. Ağaçta, `Excel = "SampleFinDimWsReport"\Cell<DimNames>` öğesini seçin.
19. Kes'e tıklayın.
20. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` öğesini seçin.
21. Yapıştır'a tıklayın.
22. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` öğesini genişletin.
23. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` öğesini genişletin.
24. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` öğesini genişletin.
25. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` öğesini seçin.
    * Mali boyutlar için (kullanıcı iletişim formunda) seçtiğiniz kadar sütunu olan Excel çıktısını dinamik olarak oluşturmak için yeni bir aralık ekleyin. Her sütundaki her bir hücre ve raporlama hareketi için tek bir finansal boyutun değerini temsil eder.  
26. Aralık Ekle'ye tıklayın.
27. Excel aralık alanına `DimValues` yazın.
    * DimValues  
28. Çoğaltma yönü alanında `Horizontal` seçeneğini belirleyin.
29. Tamam'a tıklayın.
30. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>` öğesini seçin.
31. Kes'e tıklayın.
32. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` öğesini seçin.
33. Yapıştır'a tıklayın.
34. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` öğesini genişletin.

## <a name="map-format-elements-to-data-sources"></a>Biçim öğelerini veri kaynaklarıyla eşleme

1. Eşleme sekmesini tıklatın.
2. Ağaçta, `model: Data model Financial dimensions sample model` öğesini genişletin.
3. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list` öğesini genişletin.
4. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` öğesini genişletin.
5. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` öğesini genişletin.
6. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>` öğesini seçin.
7. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String` öğesini seçin.
8. Bağla'yı tıklatın.
9. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` öğesini seçin.
10. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` öğesini seçin.
11. Bağla'yı tıklatın.
12. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>` öğesini seçin.
13. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real` öğesini seçin.
14. Bağla'yı tıklatın.
15. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>` öğesini seçin.
16. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real` öğesini seçin.
17. Bağla'yı tıklatın.
18. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>` öğesini seçin.
19. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String` öğesini seçin.
20. Bağla'yı tıklatın.
21. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>` öğesini seçin.
22. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date` öğesini seçin.
23. Bağla'yı tıklatın.
24. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>` öğesini seçin.
25. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String` öğesini seçin.
26. Bağla'yı tıklatın.
27. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>` öğesini seçin.
28. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` öğesini seçin.
29. Bağla'yı tıklatın.
30. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` öğesini seçin.
31. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` öğesini seçin.
32. Bağla'yı tıklatın.
33. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>` öğesini seçin.
34. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` öğesini seçin.
35. Bağla'yı tıklatın.
36. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` öğesini seçin.
37. Ağaçta, `model: Data model Financial dimensions sample model\Journal: Record list` öğesini seçin.
38. Bağla'yı tıklatın.
39. Ağaçta, `model: Data model Financial dimensions sample model\Dimensions setting: Record list` öğesini genişletin.
40. Ağaçta, `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String` öğesini seçin.
41. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>` öğesini seçin.
42. Bağla'yı tıklatın.
43. Ağaçta, `model: Data model Financial dimensions sample model\Dimensions setting: Record list` öğesini seçin.
44. Ağaçta, `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` öğesini seçin.
45. Bağla'yı tıklatın.
46. Ağaçta, `Excel = "SampleFinDimWsReport"\Cell<CompanyName>` öğesini seçin.
47. Ağaçta, `model: Data model Financial dimensions sample model\Company: String` öğesini seçin.
48. Bağla'yı tıklatın.
49. Kaydet'e tıklayın.
50. Sayfayı kapatın.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
