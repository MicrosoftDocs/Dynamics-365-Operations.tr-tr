---
title: Taban fiyat ve ticari sözleşmeler
description: Bu yordam kanala özel bir satış fiyatı ticari anlaşmaları oluşturma sürecini gösterir.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45d3d962958d0487c9e65910a2dce24097a83773
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017770"
---
# <a name="base-price-and-trade-agreements"></a>Taban fiyat ve ticari sözleşmeler

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam kanala özel bir satış fiyatı ticari anlaşmaları oluşturma sürecini gösterir. Bu yordam, USRT demo veri şirketini kullanır.

1. **Gezinti bölmesi**'nde, **Modüller > Perakende ve ticaret > Fiyatlandırma ve indirim yönetimi > Fiyat grupları > Tüm fiyat grupları**'na gidin. Fiyat grupları, ticari anlaşmaların belirli kanallara nasıl atandığıyla ilgilidir. Ticari anlaşmaları bir kanala atamak için fiyat grupları kullanmak kanala özel fiyatlandırma sağlar.  
2. **Yeni**'ye tıklayın.
3. **Fiyat grupları** alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Kaydet**'e tıklayın.
6. Sayfayı kapatın.
7. **Gezinme paneli**'nde, **Modüller > Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları**'na gidin.
8. Listeden 'New York'u seçin.
9. Eylem Bölmesinde **Mağaza**'ya tıklayın.
10. **Fiyat grupları**'na tıklayın.
11. **Yeni**'ye tıklayın.
12. **Fiyat grupları** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
13. Listede, istenen kaydı bulun ve seçin.
14. **Kaydet**'e tıklayın.
15. Sayfayı kapatın.
16. Sayfayı kapatın.
17. **Gezinti bölmesi**'nde, **Modüller > Perakende ve ticaret > Ürünler ve kategoriler > Kategoriye göre serbest bırakılan ürünler**'e gidin.
18. Listede, seçili satırdaki bağlantıya tıklayın.
19. **Düzenle**'yi tıklatın.
20. **Satış** hızlı sekmesini genişletin.
21. **Fiyat** alanına bir sayı girin. Geçerli herhangi bir ticari anlaşma bulunamazsa bu fiyat kullanılır.  
22. **Kaydet**'e tıklayın.
23. **Eylem bölmesi**'nde, **Satış**'a tıklayın.
24. **Ticari anlaşmalar oluştur**'a tıklayın.
25. **Yeni**'ye tıklayın.
26. **Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.
27. Listeden **Perakende**'yi seçin. Demo veride **Perakende** günlük adının varsayılan ilişkisi **Fiyat (satış)**'dır. Bu, yeni oluşturulan tüm satırların varsayılan olarak satış fiyatı ticari anlaşmalarına ayarlanır.  
28. **Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın.
29. **Hesap kodu** alanında 'Grup'u seçin.
30. **Hesap seçimi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
31. Listede, istenen kaydı bulun ve seçin. Kanaldan Fiyat grubuna, Fiyat grubundan Ticari anlaşmalara bağlantıyı tamamlar.  
32. **Madde ilişkisi** alanına bir değer yazın.
33. **Para birimi miktarı** alanına bir sayı girin.
34. **Ayrıntılar** hızlı sekmesinde **Sonrakini bul** onay kutusunu işaretleyin veya işaretini kaldırın. **Sonrakini bul** 'Evet' olarak ayarlandığında, fiyatlandırma altyapısı, daha düşük satış fiyatına sahip ilgili ticari anlaşmaları aramaya devam edecektir. **Sonrakini Bul** 'Hayır' olarak ayarlandığında, fiyat altyapısı aramayı durdurur ve ticaret anlaşmasını kullanır.  
35. **Naklet**'e tıklayın.
36. **Tamam**'a tıklayın.
37. Sayfayı kapatın.
38. **Eylem Bölmesi**'nde, Satış'a tıklayın.
39. **Satış fiyatı**'na tıklayın.

