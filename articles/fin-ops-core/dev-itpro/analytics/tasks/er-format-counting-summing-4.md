---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 4 - Biçimi çalıştırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b89d08d8f6a4223eb592ffa2b918504839e5287b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142421"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a>ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 4 - Biçimi çalıştırma)

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar. Bu adımlar DEMF şirketinde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Sayım ve toplama yapmak için biçim yapılandırma (Bölüm 3: Çıkış yapmak için hesaplamaları kullanma)" yordamındaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Intrastat raporlarını oluşturmak için bu yapılandırmayı sınama
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.
3. Ağaçta, "Intrastat modeli" öğesini genişletin.
4. Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.
5. Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.
6. Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.
7. Kullanıcı parametreleri'ne tıklayın.
8. Çalıştırma ayarları alanında Evet'i seçin.
9. Tamam'a tıklayın.
10. Düzenle öğesine tıklayın.
11. Taslak Çalıştır alanında Evet'e tıklayın.
12. Kaydet'e tıklayın.
13. Vergi > Kurulum > Dış Ticaret > Dış Ticaret parametreleri'ne gidin.
14. Elektronik raporlama bölümünü genişletin.
15. “Sayım ve toplama ile Intrastat (DE)” yapılandırmasını seçin.
16. “Sayım ve toplama ile Intrastat (DE)” yapılandırmasını seçin.
17. Kaydet'i tıklatın.
18. Sayfayı kapatın.
19. Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.
20. Çıkış düğmesine tıklayın.
21. Rapor'a tıklayın.
    * Intrastat raporu oluşturma işlemini çalıştırın.  
22. Form tarihi alanında, tarihi '01-01-2000' olarak ayarlayın.
    * Formda var olan hareketleri içeren raporlama döneminin başlangıç ve bitiş tarihlerini tanımlayın.  
23. Bitiş tarihi alanında tarihi "31.12.2022" olarak ayarlayın.
    * Formda var olan hareketleri içeren raporlama döneminin başlangıç ve bitiş tarihlerini tanımlayın.  
24. Yön alanında "Gelen öğesini seçin.
25. Dosya oluştur alanında Evet'i seçin.
26. Tamam'a tıklayın.
    * Sondaki özet satırlarıyla oluşturulan çıktıyı gözden geçirin.  
27. Yeni'ye tıklayın.
28. Listede, seçili satırı işaretleyin.
29. Yön alanından "Sevkler" öğesini seçin.
30. Madde numarası alanında bir değer girin veya seçin.
31. Emtia alanına bir değer girin veya buradan bir değer seçin.
32. Ağırlığı "10" olarak ayarlayın.
33. Fatura tutarını "10.000" olarak ayarlayın.
34. İstatistiksel tutarı "10.000" olarak ayarlayın.
35. Çıkış düğmesine tıklayın.
36. Rapor'a tıklayın.
37. Yön alanından "Sevkler" öğesini seçin.
38. Tamam'a tıklayın.
    * Sondaki özet satırlarıyla oluşturulan çıktıyı gözden geçirin. İlk çalıştırmayla karşılaştırıldığında değiştirildiğini unutmayın.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Toplanan sayımı ve veri toplamayı gözden geçirmek için bu yapılandırmayı hata ayıklama modunda çalıştırma
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, "Intrastat modeli" öğesini genişletin.
3. Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.
4. Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.
5. Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.
6. Kullanıcı parametreleri'ne tıklayın.
7. Hata ayıklama modunda çalıştır alanında Evet'i seçin.
8. Tamam'a tıklayın.
9. Sayfayı kapatın.
10. Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.
11. Çıkış düğmesine tıklayın.
12. Rapor'a tıklayın.
13. Tamam'a tıklayın.
14. Sayfayı kapatın.
15. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
16. Ağaçta, "Intrastat modeli" öğesini genişletin.
17. Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini genişletin.
18. Ağaçta, "Intrastat modeli\Intrastat (DE)\Sayım ve toplama ile Intrastat (DE)" öğesini seçin.
19. Hata ayıklama günlükleri'ne tıklayın.
    * Seçili yapılandırmanın yürütme işlemi için bir hata ayıklama günlüğü kaydı oluşturulduğunu unutmayın.  
20. İliştir'e tıklayın.
21. Aç'a tıklayın.
    * Seçili yapılandırmanın yürütmesi sırasında toplanan sayım ve toplama ayrıntılarını içeren, yeni oluşturulan XML dosyasını gözden geçirin.  

