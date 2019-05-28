---
title: Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmaları gözden geçirme
description: Bu adımları tamamlamak için öncelikle "ER Katıştırılmış resimler barındıran MS Office biçimlerinde raporlar hazırla (Bölüm 1 - Parametrelerin kurulumu)" görev kılavuzundaki adımları tamamlayın.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3462f16ad7638071ab0aa2175d0bc291eeae89
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551265"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmaları gözden geçirme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu adımları tamamlamak için öncelikle "ER Katıştırılmış resimler barındıran MS Office biçimlerinde raporlar hazırla (Bölüm 1: Parametrelerin kurulumu)" görev kılavuzundaki adımları tamamlayın.

Bu yordam, Microsoft Excel ve Microsoft Word'te katıştırılmış resimler içeren elektronik belgelerin Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağını gösterir. Bu örnekte, 'Litware, Inc.' örnek şirketi için ER yapılandırmalarını gözden geçireceksiniz. 

Bu yordam Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar içindir. Adımlar USMF veri kümesi kullanılarak tamamlanabilir.


## <a name="review-the-imported-data-model"></a>İçe aktarılan veri modelini gözden geçirin.
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Çekler için model' öğesini seçin.
3. Tasarımcı'yı tıklatın.
    * Bu model, bu modelin uygulamanın veri kaynaklarına işletme bakış açısından ödeme çeklerini temsil etmek için tasarlanmıştır. Bu modeli ER Operasyonlar tasarımcısında ön izleyin. Sunulan model öğelerinin özniteliklerini göz önünde bulundurun: yapı, ad, açıklama, veri türü ve benzeri.   
4. Ağaçta, 'kök' metnini genişletin.
5. Ağaçta 'kök\çekler' genişletin.
6. Ağaçta, 'kök\çekler' öğesini genişletin.
7. Ağaçta 'kök\çekler\öznitelikler' seçeneğini genişletin.
8. Ağaçta 'kök\ödeyen' seçeneğini genişletin.
9. Ağaçta 'kök\istestrun' öğesini seçin.
10. Ağaçta 'kök\düzen' öğesini seçin.
    * Bu modelin düzen öğesi, seçilen banka hesabı için yazdırılan çek biçimi düzeninin ayrıntılarını temsil eder. Resimleri depolamak için konteyner veri türünün iki düğümünü de içerir.   
11. Ağaçta 'kök\düzen' görünümünü genişletin.
12. Ağaçta 'kök\düzen\şirket logosu' öğesini seçin.
13. Ağaçta 'kök\düzen\şirket logosu' öğesini genişletin.
14. Ağaçta 'kök\düzen\şirket logosu\resim' öğesini seçin.
15. Ağaçta 'kök\düzen\şirket logosu\isprinted' öğesini seçin.
16. Ağaçta 'kök\düzen\imza' öğesini seçin.
17. Ağaçta, 'kök\düzen\imza' öğesini genişletin.
18. Ağaçta 'kök\düzen\imza\resim' öğesini seçin.
19. Ağaçta 'kök\düzen\imza\isprinted' öğesini seçin.
    * İki resim veri modeli öğesinin, şirket logosunun ve yetkili kişinin imzasının ikili biçimdeki resimlerini içeren alanlara bağlı olduğunu unutmayın.  
20. Ağaçta 'kök\düzen\filigran' öğesini genişletin.
21. Modeli veri kaynağına eşle'yi tıklayın.
22. Tasarımcı'yı tıklatın.
23. Ağaçta 'chequesselected' öğesini genişletin.
24. Ağaçta, 'düzen' metnini genişletin.
25. Ağaçta 'düzen\şirket logosu' öğesini genişletin.
26. Ağaçta, 'düzen\imza' öğesini genişletin.
27. Ağaçta, 'düzen\filigran' öğesini genişletin.
28. "Ayrıntıları göster" öğesini açın.
    * Çekler veri modeli öğesinin çalışma zamanında kullanıcının yazdırılmak üzere seçtiği çeklerin kayıtlarını içeren TmpChequePrintout tablosuna bağlı olduğunu unutmayın.   
29. Sayfayı kapatın.
30. Sayfayı kapatın.
31. Sayfayı kapatın.

## <a name="review-the-imported-format"></a>İçe aktarılan biçimi gözden geçirin.
1. Ağaçta, 'Çekler için model' öğesini genişletin.
2. Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.
3. Tasarımcı'yı tıklatın.
4. Ekler'e tıklayın.
5. Aç'a tıklayın.
    * Eklenen raporun şablonunu Excel'de açın.  
    * Eklenen raporun Excel şablonu, çekleri yazdırmak için kullanılacaktır. Şablon sayfa başına iki çek içerir ve çekleri önceden yazdırılmış biçimde yazdırmak için tasarlanmıştır. İki boş resmin katıştırılmış olduğunu unutmayın. Bu boş resimler şirket logosu ve ödemeye izin veren kişinin imzası içindir. Resimlerin Excel'de sırasıyla CompLogo ve SignatureImage olarak adlandırıldığından emin olun.   
6. Sayfayı kapatın.
7. Ağaçta, 'Rapor' öğesini genişletin.
8. Ağaçta, 'Rapor\ChequeLines' öğesini genişletin.
9. Ağaçta 'Rapor\ChequeLines\CompLogo' öğesini seçin.
10. "Ayrıntıları göster" öğesini açın.
    * 'CompLogo' biçiminin hücre öğesi, raporda şirket logosu resmini doldurmak için kullanılan Excel öğesini temsil eder. Bu biçim öğesi, çalışma zamanında bir şirket logosunu ikili biçimde içeren bir resim veri modeli öğesine bağlıdır.   
11. Eşleme sekmesini tıklatın.
12. Düzenleme etkinleştirildi'ye tıklayın.
    * 'CompLogo' biçiminin hücre öğesini daha fazla etkin olmayacağı şekilde yapabilirsiniz. Bu durumda, ilişkilendirilen Excel resim öğesi, bir şirket logosunu oluşturulan raporda gizleyecektir. Etkinleştirilen deyim DOĞRU sonucunu getirirse ve tanımlanan bağlama resim getirmez, ilişkilendirilen Excel resim dosyası, Excel şablonu kaydedilmiş olan bir resmi gösterir.   
13. Sayfayı kapatın.
14. Ağaçta, 'etiketler: Konteyner' öğesini genişletin.
    * Önceden yazdırılmış çek formunda sunulan bazı etiketler, test amaçlı oluşturulduğunda rapora dahil edilecektir. Ancak, bu etiketler gerçek yazdırma sırasında yazdırılmayacaktır çünkü önceden yazdırılmış form zaten bunları içerir.  
15. Sayfayı kapatın.

