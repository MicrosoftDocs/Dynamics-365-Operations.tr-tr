---
title: Uygulama verileri içeren belgeler oluşturmak için biçimleri değiştirme
description: Bu makalede, elektronik belge oluşturmak ve uygulama verilerini güncelleştirmek için raporlama yapılandırmalarının nasıl tasarlanacağı açıklanmaktadır.
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecd301b60f804328f3b6652df8c38edf42eb79f0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290499"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Uygulama verileri içeren belgeler oluşturmak için biçimleri değiştirme

[!include [banner](../../includes/banner.md)]

Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 3: Model ve eşlemeyi değiştir)" yordamını tamamlamalısınız.

Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak ve uygulama verisini güncelleştirmek için nasıl kullanılacağını açıklar. Bu yordamda, ER yapılandırmaları sadece elektronik belgeler oluşturmakta kullanmak için değil, aynı zamanda uygulama verisini güncelleştirmek için de değiştirirsiniz. Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir.


## <a name="modify-format-to-collect-details-of-reporting"></a>Raporlama ayrıntılarını toplamak için biçimi değiştirin
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Intrastat (model)' öğesini genişletin.
3. Ağaçta, 'Intrastat (model)\Intrastat (biçim)' öğesini seçin.
4. Tasarımcı'yı tıklatın.
5. Ağaçta, 'Dosya'yı genişletin.
6. Ağaçta, 'Dosya\Bildirim' öğesini genişletin.
7. Ağaçta, 'Dosya\Bildirim\Veri'yi seçin.
8. Çokluluk alanında 'Bir fazla'yı seçin.
    * Intrastat raporlama işleminin ayrıntılarını arşivlemek için bu biçim öğesini yapılandırın. Bu öğe, arşiv başlığının kaydını temsil eder.  
9. Ağaçta 'Dosya\Bildirim\Veri'yi genişletin.
10. Ağaçta 'Dosya\Bildirim\Veri\Öğe'yi seçin.
11. Çokluluk alanında 'Sıfır fazla'yı seçin.
    * Intrastat raporlama işleminin ayrıntılarını arşivlemek için bu biçim öğesini yapılandırın. Bu öğe arşivlenen satırların listesini temsil eder.  
12. Ağaçta 'Dosya\Bildirim\Veri\Öğe'yi genişletin.
13. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim1'i seçin.
14. Dışarıda bırakılan alanında Evet'i seçin.
    * Bu veriyi arşivlemezsiniz, böylece bu biçim öğesini Intrastat raporlama ayrıntılarının veri kaynağından dışarıda bırakabilirsiniz.  
15. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim1'i genişletin.
16. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim1\özellik'i seçin.
17. Dışarıda bırakılan alanında Evet'i seçin.
18. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim1\tarih'i seçin.
19. Dışarıda bırakılan alanında Evet'i seçin.
20. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim2'yi seçin.
21. Dışarıda bırakılan alanında Evet'i seçin.
22. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim2'yi genişletin.
23. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim2\özellik'i seçin.
24. Dışarıda bırakılan alanında Evet'i seçin.
25. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim2\kod'u seçin.
26. Dışarıda bırakılan alanında Evet'i seçin.
27. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim3'ü seçin.
    * Çok sayıda biçim öğesi aynı ada sahip olabilir. Örneğin, Dim. Onları, bu biçimi Intrastat raporlama ayrıntılarını arşivlerken bir veri kaynağı olarak açıkça tanımlayamazsınız, böylece bu biçim öğeleri için alternatif adlar tanımlamanız gerekir.   
28. İsim alanına 'Tutar' yazın.
    * Tutar  
29. Çokluluk alanında 'Tam bir'i seçin.
30. Ağaçta 'Dosya\Bildirim\Veri\Öğe\Dim4'ü seçin.
31. İsim alanına 'Madde' yazın.
    * Madde  
32. Çokluluk alanında 'Tam bir'i seçin.
    * Tasarım biçim öğelerine ek olarak, aşağıdaki Intrastat raporlama ayrıntılarının arşivlenmesi gerekir: raporlanan her emtia öğesinin benzersiz kayıt kimlik saptaması ve oluşturulan dosyanın adı. Bu veri, Intrastat raporunda doldurulmayacağı için, bu ayrıntı öğeleriyle ilişkili biçimi veri kaynağı öğeleri olarak eklemeniz gerekir.  
33. Ağaçta, 'Dosya\Bildirim\Veri'yi seçin.
34. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
35. Ağaçta 'Veri kaynağı\Öğe'yi seçin.
36. Ad alanına "Dosya adı" yazın.
    * Dosya adı  
37. Veri türü alanında 'Dize' seçin.
38. Tamam'a tıklayın.
39. Ağaçta 'Dosya\Bildirim\Veri\Öğe'yi seçin.
40. Madde Ekle üzerine tıklayın.
41. Ad alanına "Commodity rec ID" adını girin.
    * Commodity rec ID  
42. Veri türü alanında 'Int64' seçin.
43. Tamam'a tıklayın.
44. Eşleme sekmesini tıklatın.
45. Ağaçta 'Dosya\Bildirim\Veri\Dosya adı'nı seçin.
46. Bağla'ya tıklayın.
47. Ağaçta, 'model'i genişletin.
48. Ağaçta 'model\Hareketler'i seçin.
49. Ağaçta "File\Declaration\Data\Item = model.Transactions\Commodity rec ID" öğesini seçin.
50. Ağaçta "model\Transactions\Commodity rec ID" öğesini seçin.
51. Bağla'yı tıklatın.
52. Kaydet'i tıklatın.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Raporlama ayrıntılarını belleğe almak için biçimi değiştirin

1. Biçimi modelle eşle'ye tıklayın.
2. Yeni'yi tıklatın.
3. Tanım alanında, 'Uygulama veri güncelleştirmesi' kök maddesini girin veya seçin.
    * Uygulama veri güncelleştirmesi için.
4. Ad alanına 'Veri güncelleştirmek için eşleme' yazın.
    * Veriyi güncelleştirmek için eşleme  
5. Kaydet'e tıklayın.
    * Bu eşleme, Intrastat raporunun ayrıntılarının veri modelinde nasıl toplandığını, seçilen kök öğesi 'Uygulama veri güncelleştirmesi için' belirtilen yapının hangisi olduğunu tanımlar. Bu ayrıntılar, aynı kök öğesi 'Uygulama veri güncelleştirmesi için' model eşleme ve yön 'Hedefe' uygulama veri güncelleştirmesi için kullanılır. Uygulama veri güncelleştirmesi, giden Intrastat raporu oluşturulduktan hemen sonra başlar. Uygulama veri güncelleştirilmesi çalıştırma zamanında atlanabilir ancak veri modelinin boş olması (boş kayıt listesi içermesi) gerekir.
6. Tasarımcı'ya tıklayın.
    * Giden intrastat rapor biçimi, bu model eşleme için bir veri kaynağı olarak varsayılan şekilde eklenir.  
    * Tasarlanan raporun öğelerini (veri kaynağında sunulan), seçilmiş modelin kök öğesine dayanarak filtrelenen veri modelinin öğelerine bağlama.  
7. Ağaçta, 'Arşiv başlığı' metnini genişletin.
8. Ağaçta 'Arşiv başlığı\Arşiv satırları'nı genişletin.
9. Ağaçta, 'biçim' metnini genişletin.
10. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)'i seçin.
11. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)'yi genişletin.
12. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Öğe: XML Öğe 0..*(Öğe)'yi seçin.
13. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Öğe: XML Öğe 0..*(Öğe)\Dim3: XML Öğe 1..1 (Tutar)'ı seçin.
14. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Öğe: XML Öğe 0..*(Öğe)\Dim4: XML Öğe 1..1 (Öğe)'yi seçin.
15. Ağaçta 'Arşiv başlığı\Satır sayısı'nı seçin.
16. Düzenle öğesine tıklayın.
17. Ağaçta, 'Liste\COUNT' öğesini seçin.
18. Fonksiyon ekle'ye tıklayın.
19. Ağaçta, 'biçim' metnini genişletin.
20. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)'i seçin.
21. Ağaçta, `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)` öğesini genişletin.
22. Ağaçta, `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)` öğesini seçin.
23. Veri kaynağı ekle'ye tıklayın.
24. Formül alanında 'COUNT(format.Declaration.Data.Item)' girin.
    * COUNT(format.Declaration.Data.Item)  
25. Kaydet'e tıklayın.
26. Sayfayı kapatın.
27. Ağaçta 'Arşiv başlığı\Dosya adı'nı seçin.
28. Ağaçta 'biçim\Bildirim: XML Element(Bildirim)\Veri: XML Öğe 1..* (Veri)\Dosya adı: Madde Dizesi (Dosya adı)'nı seçin.
29. Bağla'yı tıklatın.
30. Ağaçta, `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)` öğesini seçin.
31. Ağaçta 'Arşiv başlığı\Arşiv satırları\Öğe numarası'nı seçin.
32. Bağla'yı tıklatın.
33. Ağaçta, `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)` öğesini seçin.
34. Ağaçta 'Arşiv başlığı\Arşiv satırları\Tutar'ı seçin.
35. Bağla'yı tıklatın.
36. Ağaçta, `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)` öğesini seçin.
37. Ağaçta "Archive header\Archive lines\Commodity rec ID" öğesini seçin.
38. Bağla'yı tıklatın.
39. Ağaçta 'Arşiv başlığı\Arşiv satırları'nı seçin.
40. Ağaçta, `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)` öğesini seçin.
41. Bağla'yı tıklatın.
42. Ağaçta, 'Arşiv başlığı' metnini seçin.
43. Ağaçta, `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)` öğesini seçin.
44. Bağla'yı tıklatın.
45. Kaydet'i tıklatın.
46. Sayfayı kapatın.
47. Sayfayı kapatın.
48. Sayfayı kapatın.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
