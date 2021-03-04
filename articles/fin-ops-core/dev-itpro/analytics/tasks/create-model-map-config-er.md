---
title: Elektronik raporlama (ER) model eşleme yapılandırmaları oluşturma
description: Yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlamak ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanmak için bu yordamı kullanın.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23bc3a525be9f65b7e5100114d02f6b79a286fb5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682081"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Elektronik raporlama (ER) model eşleme yapılandırmaları oluşturma

[!include [banner](../../includes/banner.md)]

Yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlamak ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanmak için bu yordamı kullanın. Bu yordamda, Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. 

Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.

Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir. Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.  
2. Raporlama konfigürasyonları'na tıklayın.
3. Filtreleri göster'e tıklayın.
4. "Ad" alanına "Intrastat" filtre değerini girin ve "ile başlar" filtre işlecini kullanın.
    * 'Intrastat' veri modeli yapılandırmasını bulmak için bu filtreyi uygulayın. Bu model zaten yapılandırmalar ağacında bulunuyor olabilir. Varsa, bir sonraki alt görevi atlayın.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Microsoft tarafından sağlanan Intrastat modeli yapılandırmasını alma
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
4. Listede, istenen kaydı bulun ve seçin.
    * Microsoft sağlayıcısı kutucuğunu seçin.  
5. Depolar'a tıklayın.
    * Microsoft sağlayıcısı kutucuğunda Depolar'a tıklayın.  
6. Filtreleri göster'e tıklayın.
7. "Tür adı" alanına "kaynaklar" filtre değerini girin ve "içerir" filtre işlecini kullanın. 
8. Aç'a tıklayın.
9. Ağaçta, 'Intrastat modeli' öğesini seçin.
10. İçe aktar'ı tıklatın.
11. Evet'i tıklatın.
    * Yeni ER işlevinin nasıl kullanılacağını keşfetmek için kullanacağınız veri modelini içeren ER modeli yapılandırmasını içe aktardınız.  
12. Sayfayı kapatın.
13. Sayfayı kapatın.
14. Raporlama konfigürasyonları'na tıklayın.

## <a name="add-a-new-model-mapping-configuration"></a>Yeni bir model eşleme yapılandırması ekleme
1. Ağaçta, 'Intrastat modeli' öğesini seçin.
2. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
3. Yeni alanına, "Intrastat veri modeline dayalı model eşlemesi" yazın.
4. Ad alanına 'Intrastat örnek eşlemesi' yazın.
    * Intrastat örneği eşleme  
5. Konfigürasyon oluştur'u tıklatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]