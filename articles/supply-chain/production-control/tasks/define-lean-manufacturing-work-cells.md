--- 
title: "Yalın imalat iş hücrelerini tanımlama"
description: "İş hücresi, yalın üretim işlem faaliyetlerinde kullanılabilen kaynak gruplarının belirli bir biçimidir."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: dc9793bd59e59c96532549d73c56bad518fa7394
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="define-lean-manufacturing-work-cells"></a>Yalın imalat iş hücrelerini tanımlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

İş hücresi, yalın üretim işlem faaliyetlerinde kullanılabilen kaynak gruplarının belirli bir biçimidir. İş hücrelerinde bir üretim akışı modeline dayalı giriş ve çıkış yerleşimleri ve kapasite tanımları vardır. Yalın imalat iş hücreleri ve kapasite hesaplamalarına yönelik temel kavramlar hakkında daha fazla bilgi edinmek için Yalın üretim üzerine teknik incelemelere bakın. Bu yordamı oluşturmak için kullanılan demo verisi şirketi USMF'dir.


## <a name="create-a-work-cell"></a>Bir iş hücresi oluşturun. 
1. Organizasyon yönetimi > Kaynaklar > Kaynak grupları öğesine gidin.
2. Yeni'ye tıklayın.
3. Kaynak grubu alanına bir değer yazın.
    * İş hücre kodu genellikle sistematik bir koddur ve tüzel kişilik için benzersiz olması gerekir.  
4. Açıklama alanına bir değer girin.
    * Açıklama, iş hücresinin adını veya başlığını içerir.  
5. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bir iş hücresi tek bir belirli tesiste yer alır. Hem giriş hem çıkış ambarı ve de yerleşim bu tesiste bulunmalıdır.  
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Üretim birimi alanında, aramayı açmak için açılır menü düğmesini tıklatın.
8. Listede, seçili satırdaki bağlantıya tıklayın.
    * Bu iş hücresinin ait olduğu üretim birimi seçin.  
9. İş hücresi onay kutusunu işaretleyin.
    * Yalın iş hücresi olarak bir kaynak grubunu kullanmak için İş hücresi onay kutusunun işaretlenmesi gerekir.  Bu özelliğin kaynak grubu oluşturulduktan sonra değiştirilemeyeceğini unutmayın.  
10. Giriş ambarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.
11. Listede, seçili satırdaki bağlantıya tıklayın.
    * Muhasebe ve malzeme kontrolü için, atölyede düzenlenmiş malzeme genellikle belirli bir sanal ambara tahsis edilir. Ancak, ambar işini kullanarak yerleşimleri yenilemek istiyorsanız, bunların anlayışlı hammadde ambarının bir parçası olması gerekir.  
12. Giriş yerleşimi alanında, aramayı açmak için açılır menü düğmesini tıklatın.
13. Listede, seçili satırdaki bağlantıya tıklayın.
    * İşlem faaliyeti için, genel olarak ya da belirli bir ürün veya işlem faaliyetini besleyen malzeme çekme faaliyetleri tanımlanarak bir ürün yelpazesi için giriş yerleşiminin üzerine yazılabileceğini unutmayın. İş hücresinin giriş yerleşimleri plaka denetimli olamaz.  
14. Çıkış ambarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.
15. Listede, istenen kaydı bulun ve seçin.
    * Birden fazla üretim akışı veya üretim satırı faaliyetinde, bu, genellikle bir sonraki iş hücresinin giriş ambarı ya da ürünün her zamanki üretim işleminin ardından transfer edileceği satış veya transit ambarıdır. Yalın üretim süreçlerini modelleme sırasındaki taşıma işleminin taşıma raporlanırken olduğu gibi genellikle atık taşıma olacağı unutmayın.  
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. Çıkış yerleşimi alanında, aramayı açmak için açılır menü düğmesini tıklatın.
    * Birden çok işlem faaliyeti olan üretim akışında bu genellikle bir sonraki iş hücresinin giriş yerleşimidir.  
18. Listede, istenen kaydı bulun ve seçin.
19. Listede, seçili satırdaki bağlantıya tıklayın.
20. Operasyon bölümünü genişletin veya daraltın.
    * Maliyet hesaplaması ve yalın kanban işlerinin işleme alınmasını sağlamak için bir Çalışma zamanı kategorisi belirtilmelidir.  
21. Çalışma zamanı kategorisi alanında, aramayı açmak için açılır menü düğmesini tıklat<ın.
22. Listede, istenen kaydı bulun ve seçin.
    * Çalışma zamanı maliyet kategorisi, standart maliyet hesaplamasında ve geriye dönük maliyet çıkarma işleminde kullanılır.  
23. Listede, seçili satırdaki bağlantıya tıklayın.
24. Takvimler bölümünü genişletin veya daraltın.
25. Ekle öğesini tıklatın.
26. Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.
27. Listede, istenen kaydı bulun ve seçin.
    * Genellikle belirli bir tesisin iş hücreleri aynı çalışma zamanı takvimini kullanır. İş hücrelerinde tek bir çalışma zamanı varsa, iş hücresi için belirli bir çalışma zamanı takvimi oluşturmanız gerekebilir. Yalın iş hücresi için kullanıldığında, kapasite tanımlamasının genellikle bir iş gününün standart çalışma süresiyle ilgisi olduğundan takvimin standart çalışma zamanının tanımlanması gerektiğini unutmayın.  
28. Listede, seçili satırdaki bağlantıya tıklayın.
29. İş hücresi kapasitesi bölümünü genişletin veya daraltın.
30. Ekle öğesini tıklatın.
31. Üretim akışı modeli alanında, aramayı açmak için açılır menü düğmesini tıklatın.
32. Listede, istenen kaydı bulun ve seçin.
    * Bu yordamlar, iş çıkarma kapasitesinin tanımını gösterebilmek için İş çıkarma yeteneği üretim akışı modeli türünün kullanılmasını gerektirir.  
33. Listede, seçili satırdaki bağlantıya tıklayın.
34. Kapasite dönemi alanında bir seçenek belirtin.
    * Seçenekler şunlardır:   Standart iş günü - Kapasite, iş hücresi için çalışma zamanı takviminin standart çalışma gününün uzunluğuyla ifade edilir. Her gün için, fiili çalışma süresi takvimden belirlenir ve etkin kullanılabilir kapasite bu temel alınarak hesaplanır.   Hafta - Bir haftalık kapasite sağlar. Fiili çalışma zamanına göre yapılan bir ayarlama yoktur.   Ay - Bir aylık kapasite sağlar. Fiili kapasiteye göre yapılan bir ayarlama yoktur.   Genellikle, standart iş günü günlük dönemler için kullanılırken haftalık kapasite haftalık kapasite dönemleri için kullanılır.  
35. Ortalama iş çıkarma yeteneği miktarı alanında bir sayı girin.
    * Yalın bir işlemin hiçbir zaman ideal bir ortamda olası maksimum kapasite için ayarlanmayacağını unutmayın. Bunun yerine, normal koşullar altında çalışan işlemler için her zaman bir kapasite tanımlanmalıdır.  
36. Birim alanında, aramayı açmak için açılır menü düğmesini tıklatın.
37. Listede, seçili satırdaki bağlantıya tıklayın.
38. Birimi ResolveChanges.

## <a name="add-a-financial-dimension"></a>Bir mali boyut ekleme
1. Mali boyutlar bölümünü genişletin veya daraltın.
    * Üretim akışında tanımlanan mali boyutların iş hücresinin sağlanan mali boyutunu geçersiz kılacağını unutmayın.    Hangi mali boyutların seçilebileceği sistemdeki mali boyutların yapılandırmasına bağlıdır. Aşağıdaki adımlar, USMF şirketindeki Demo verileri kümesiyle ilgilidir. Farklı veriler kullanılırken, bu adımlar uygun olmayabilir.  
2. CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
    * Yalın iş hücrelerinde seçilmesi gereken boyutlar belirli bir tüzel kişilik için muhasebe modelinin uygulamasına bağlı olarak belirlenir.  
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. ItemGroup modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="save"></a>Kaydet
1. Kaydet'e tıklayın.


