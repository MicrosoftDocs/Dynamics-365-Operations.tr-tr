--- 
title: "Personelin yaralanma ve hastalık bilgilerini koruma"
description: "Bazı ayar bilgileri burada kullanıldığından, 'Yaralanma ve hastalık ayarlama' görevini önce tamamlamanız tavsiye edilir."
author: ShielaSogge
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e3b7dea463ce154df29844af95789611faae405b
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="maintain-employee-injury-and-illness-information"></a>Personelin yaralanma ve hastalık bilgilerini koruma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bazı ayar bilgileri burada kullanıldığından, 'Yaralanma ve hastalık ayarlama' görevini önce tamamlamanız tavsiye edilir. 



Bu görev, bir yaralanma veya hastalık örneği oluşturmanın temel adımlarını kapsar. Yaralanma veya hastalık ayrıntılarını izlemenin yanı sıra, izlenen bir servis talebi de vardır.  Vaka varsayılan olarak 'açık' durumundadır.  Durumlar, uygulama formun üst tarafındaki çubuğundaki 'Servis talebi' menü öğesinden yönetilebilir.

1. İnsan Kaynakları > Çalışanlar > Yaralanma ve hastalık > Yaralanma veya hastalık olayları'na gidin.
2. Yeni'ye tıklayın.
3. Olay açıklaması alanında bir değer girin.
    * Örnek: Bilek sakatlığı  
4. Çalışan alanında bir değer girin veya bir değer seçin.
    * Örnek: Ahmet Bora  
5. Olayın tarihi ve saati alanında bir tarih ve saat girin.
    * Örnek: 1/20/2016 10:00 AM  
6. Yaralanma veya hastalık türü alanında bir değer girin veya seçin.
    * Örnek: Kırık  
7. Vücut bölümü alanında bir değer girin veya bir değer seçin.
    * Örnek: Bilek  
8. Sonuç türü alanında bir değer girin veya bir değer seçin.
    * Örnek: Terapi  
9. Raporlanma tarihi ve saati alanında bir tarih ve saat girin.
    * Raporlanan tarih ve saat, olayın tarih ve saatinden sonra olmalıdır.  
10. Servis talebini rapor eden kişi alanında bir değer girin veya seçin.
    * Bu, olaya tanık bir çalışan veya başka bir şahit olabilir.  Örnek: Ahmet Bora  
11. Olay bölümünü genişletin.
12. Olayın oluştuğu yer alanında bir değer girin.
    * Örnek: Ambar  
13. Çalışılan yerde alanında Evet'i seçin.
    * Olay çalışılan yerde meydana geldiyse, evet'i seçin.  
14. İşe başladığı tarih ve saat alanında bir tarih ve saat girin.
    * Olay gerçekleşmeden önce bireyin çalışmaya başlamasını etkileyen tarih ve saati girin.  
15. Çalışanın işi veya görevi alanında bir değer girin.
    * Olay meydana geldiğinde çalışanın yapmakta olduğu işi veya görevi girin.  Örnek: Kutuları yükleme  
16. Olayın nedeni alanında bir değer girin.
    * Olayın nedenini girin.  Örnek: Islak zeminde kayma  
17. Önem düzeyi alanında bir değer girin veya bir değer seçin.
18. Gerçekleştirilecek eylem alanında bir değer girin.
    * Örnek: Dökülen sıvıları hemen temizleme  
19. İşbaşı yapmadan geçirmesi beklenen gün sayısı alanında bir sayı girin.
    * Bireyin işten uzak kalması beklenen gün sayısını girin.  Birey işe döndüğünde, 'İşten uzakta geçen gün sayısı' alanını gelmediği gerçek gün sayısıyla güncelleştirin.  
20. Yaralanma veya hastalık maliyetleri bölümünü genişletin.
21. Ekle öğesini tıklatın.
22. Tarih alanına bir tarih girin.
23. Maliyet türü alanında bir değer girin veya bir değer seçin.
    * Örnek:  Terapi    Bir tutar girebilir ve faturalar veya doktorun notları gibi destekleyici belgeleri maliyete ekleyebilirsiniz.  
24. Ekle öğesini tıklatın.
25. Tarih alanına bir tarih girin.
26. Maliyet türü alanında bir değer girin veya bir değer seçin.
    * Örnek: Doktor  
27. Yaralanma veya hastalık tedavileri bölümünü genişletin.
28. Ekle öğesini tıklatın.
29. Tedavi tarihi alanında bir tarih ve saat girin.
30. Tedavi türü alanında bir değer girin veya seçin.
    * Örnek: Atel  
31. İsteğe bağlı olarak, acil servis hastane ziyareti bölümünü Evet olarak ayarlayın.
32. Tedavi açıklamaları alanında bir değer girin.
    * Örnek: 2 hafta süresince atel  
33. Doktorun adı alanında bir değer girin.
    * Örnek: Dr. Yılmaz  
34. Tedavi tesisi ve yeri alanında bir değer girin.
    * Örnek: Vatan Cad. Acil Servis  
35. Tedavi ayrıntıları alanında bir değer girin.
    * Örnek: Kırık röntgende görünüyor, atel takıldı  
36. Kaydet'e tıklayın.
    * Servis talebi her zaman güncelleştirilebilir.  Yaralanma veya hastalığın işlenmesini sürüyorsa vakayı 'süren iş' olarak ayarlayın.  Olayı bir defa kapattığınızda, yalnızca maliyet, tedavi ekleyip kaldırabilir veya olayla ilgili dosyalamalar yapabilirsiniz.  Diğer bilgileri değiştirmek için olayı yeniden açın.  


