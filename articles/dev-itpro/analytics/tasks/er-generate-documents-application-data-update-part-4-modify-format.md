--- 
title: "Elektronik raporlama (ER) için uygulama verileri güncelleştirmesiyle belge oluşturmak üzere biçimi değiştirme"
description: "Bu yordamdaki adımları tamamlamak için ilk önce \"ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 3 - Model ve eşlemeyi değiştir)\" yordamını tamamlamalısınız."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 47a1fe9cbfc80adbd5d375221912a2fa9787af19
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="modify-format-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için uygulama verileri güncelleştirmesiyle belge oluşturmak üzere biçimi değiştirme

[!include[task guide banner](../../includes/task-guide-banner.md)]

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
41. İsim alanına 'Emtia rec id' yazın.
    * Emtia rec id  
42. Veri türü alanında 'Int64' seçin.
43. Tamam'a tıklayın.
44. Eşleme sekmesini tıklatın.
45. Ağaçta 'Dosya\Bildirim\Veri\Dosya adı'nı seçin.
46. Bağla'ya tıklayın.
47. Ağaçta, 'model'i genişletin.
48. Ağaçta 'model\Hareketler'i seçin.
49. Ağaçta 'Dosya\Bildirim\Veri\Madde = model.TransactionsEmtia rec id'i seçin.
50. Ağaçta 'model\Hareketler\Emtia rec id'i seçin.
51. Bağla'ya tıklayın.
52. Kaydet'e tıklayın.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Raporlama ayrıntılarını belleğe almak için biçimi değiştirin
1. Biçimi modelle eşle'ye tıklayın.
2. Yeni'ye tıklayın.
3. Tanım alanında, 'Uygulama veri güncelleştirmesi' kök maddesini girin veya seçin.
    * Uygulama için veri güncelleştirmesi  
4. Ad alanına 'Veri güncelleştirmek için eşleme' yazın.
    * Veriyi güncelleştirmek için eşleme  
5. Kaydet'e tıklayın.
    * Bu eşleme, Intrastat raporunun ayrıntılarının veri modelinde nasıl toplandığını, seçilen kök öğesi 'Uygulama veri güncelleştirmesi için' belirtilen yapının hangisi olduğunu tanımlar. Bu ayrıntılar, aynı kök öğesi 'Uygulama veri güncelleştirmesi için' model eşleme ve yön 'Hedefe' uygulama veri güncelleştirmesi için kullanılır. Uygulama veri güncelleştirmesi, giden Intrastat raporu oluşturulduktan hemen sonra başlar. Uygulama veri güncelleştirilmesinin çalıştırma zamanında atlanabileceğini, ancak veri modelinin boş olması (boş kayıt listesi içermesi) gerektiğini unutmayın.   
6. Tasarımcı'yı tıklatın.
    * Giden Intrastat rapor biçimi, bu model eşleme için bir veri kaynağı olarak varsayılan şekilde eklenir.  
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
21. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)'yi genişletin.
22. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Öğe: XML Öğe 0..*(Öğe)'yi genişletin.
23. Veri kaynağı ekle'ye tıklayın.
24. Formül alanında 'COUNT(format.Declaration.Data.Item)' girin.
    * COUNT(format.Declaration.Data.Item)  
25. Kaydet'e tıklayın.
26. Sayfayı kapatın.
27. Ağaçta 'Arşiv başlığı\Dosya adı'nı seçin.
28. Ağaçta 'biçim\Bildirim: XML Element(Bildirim)\Veri: XML Öğe 1..* (Veri)\Dosya adı: Madde Dizesi (Dosya adı)'nı seçin.
29. Bağla'ya tıklayın.
30. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Öğe: XML Öğe 0..*(Öğe)\Dim4: XML Öğe 1..1 (Öğe)sayı: Dize(sayı)'yı seçin.
31. Ağaçta 'Arşiv başlığı\Arşiv satırları\Öğe numarası'nı seçin.
32. Bağla'ya tıklayın.
33. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Öğe: XML Öğe 0..*(Öğe)\Dim3: XML Öğe 1..1 (Tutar)değre: Sayısal Gerçek(değer)'i seçin.
34. Ağaçta 'Arşiv başlığı\Arşiv satırları\Tutar'ı seçin.
35. Bağla'ya tıklayın.
36. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Madde: XML Öğe 0..*(Madde)\Emtia rec id: Madde Int64(Emtia rec id)'i seçin.
37. Ağaçta 'Arşiv başlığı\Arşiv satırları\Emtia rec id'i seçin.
38. Bağla'ya tıklayın.
39. Ağaçta 'Arşiv başlığı\Arşiv satırları'nı seçin.
40. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)\Öğe: XML Öğe 0..*(Öğe)'yi genişletin.
41. Bağla'ya tıklayın.
42. Ağaçta, 'Arşiv başlığı' metnini seçin.
43. Ağaçta 'biçim\Bildirim: XML Madde(Bildirim)\Veri: XML Öğe 1..* (Veri)'yi seçin.
44. Bağla'ya tıklayın.
45. Kaydet'e tıklayın.
46. Sayfayı kapatın.
47. Sayfayı kapatın.
48. Sayfayı kapatın.


