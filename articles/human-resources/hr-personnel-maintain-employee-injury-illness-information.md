---
title: Personelin yaralanma ve hastalık bilgilerini koruma
description: Bu görev, bir yaralanma veya hastalık durumunun nasıl oluşturulacağını açıklar.
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c351919616c8ab5cf15d14c6cc79a5097e248fc
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771278"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Personelin yaralanma ve hastalık bilgilerini koruma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bazı ayar bilgileri burada kullanıldığından, 'Yaralanma ve hastalık ayarlama' görevini önce tamamlamanız tavsiye edilir. 



Bu görev, bir yaralanma veya hastalık örneği oluşturmanın temel adımlarını açıklar. Yaralanma veya hastalık ayrıntılarının yanında bir servis talebi durumu izlenir. Varsayılan olarak, servis taleplerinin durumu **Açıktır**. Durumları, sayfanın üst kısmındaki **Servis talebi durumu** menü öğesinden yönetebilirsiniz.

1. **İnsan Kaynakları \> Çalışanlar \> Yaralanma ve hastalık \> Yaralanma veya hastalık olayları**'na gidin.
2. **Yeni**'yi seçin.
3. **Servis talebi açıklaması** alanına bir değer girin (örneğin **Bilek yaralanması**).
4. **Çalışan** alanına bir değer girin veya seçin (örneğin **Ana Bowman**).
5. **Olay tarihi ve saati** alanına bir tarih ve saat girin (örneğin, 20 Ocak 2016, 10:00).
6. **Yaralanma veya hastalık türü** alanında bir değer girin veya seçin (örneğin **Kırık**).
7. **Vücut kısmı** alanına bir değer girin veya seçin (örneğin **Bilek**).
8. **Sonuç türü** alanında bir değer girin veya bir değer seçin (örneğin **Tedavi**).
9. **Raporlanma tarihi ve saati** alanında bir tarih ve saat girin.

    Raporlanma tarih ve saat, olayın tarih ve saatinden sonra olmalıdır.

10. **Servis talebini rapor eden kişi** alanında bir değer girin veya seçin (örneğin **Ana Bowman**).

    Belirtilen kişi, olaya tanık bir çalışan veya başka bir şahit olabilir.

11. **Olay** bölümünde, **Olayın oluştuğu yer** alanına bir değer girin (örneğin **Ambar**).
12. **Şirket tesislerinde** alanında, olay iş yerinde gerçekleştiyse **Evet**'i seçin.
13. **Tarih ve saat başlangıcı** alanına, etkilenen kişinin olay yapılmadan önce çalışmaya başladığı tarihi ve saati girin.
14. **Çalışan işi veya görevi** alanında, olay oluştuğunda çalışanın gerçekleştirdiği iş veya görevi girin (örneğin, **Kutu yükleme**). 
15. **Olay nedeni** alanına olayın nedenini girin (örneğin, **Islak zeminde kaymış**).
16. **Önem düzeyi** alanında bir değer girin veya bir değer seçin.
17. **Alınacak eylem** alanında bir değer girin (örneğin, **Dökülmeler hemen silinecek**).
18. **Kaç gün işe gelmeyeceği tahmini** alanında, bireyin kaç gün çalışmaması bekleniyorsa bu değeri yazın.

    Birey işe döndükten sonra, **İşten uzakta geçen gün sayısı** alanını, çalışanın gelmediği gerçek gün sayısıyla güncelleştirin.

19. **Yaralanma veya hastalık maliyetleri** bölümünde **Ekle**'yi seçin.
20. **Tarih** alanına bir tarih girin.
21. **Maliyet türü** alanında bir değer girin veya bir değer seçin (örneğin **Tedavi**).

    Bir tutar girebilir ve faturalar veya doktorun notları gibi destekleyici belgeleri maliyete ekleyebilirsiniz.

22. **Ekle**'yi seçin.
23. **Tarih** alanına bir tarih girin.
24. **Maliyet türü** alanında bir değer girin veya bir değer seçin (örneğin **Doktor**).
25. **Yaralanma veya hastalık tedavileri** bölümünde **Ekle**'yi seçin.
26. **Tedavi tarihi** alanında bir tarih ve saat girin.
27. **Tedavi türü** alanında bir değer girin veya bir değer seçin (örneğin **Splint**).
28. İsteğe bağlı: **Acil servis hastane ziyareti** bölümünü **Evet** olarak ayarlayın.
29. **Tedavi açıklamaları** alanında bir değer girin veya bir değer seçin (örneğin **2 hafta için splint**).
30. **Hekim adı** alanına bir değer girin (örneğin **Dr. Anderson**).
31. **İşlem tesisi ve konumu** alanında bir değer girin (örneğin **Elm Sokağı Acil**).
32. **Tedavi ayrıntıları** alanına bir değer girin (örneğin, **Röntgende kırık doğrulandı, splint giyilecek**).
33. **Kaydet**'i seçin.

Servis talebi her zaman güncelleştirilebilir. Yaralanma veya hastalığın işlenmesini sürüyorsa vakayı **Devam ediyor** olarak ayarlayın. Olayı kapattıktan sonra, yalnızca maliyet, tedavi ekleyip kaldırabilir veya olayla ilgili dosyalamalar yapabilirsiniz. Diğer bilgileri değiştirmek için olayı yeniden açmanız gerekir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
