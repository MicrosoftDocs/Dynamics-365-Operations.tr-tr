---
title: Uygulama verileri içeren belgeler oluşturmak için yapılandırmaları içeri aktarma
description: Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve bunu etkin olarak işaretleme" yordamını tamamlamanız gerekir.
author: kfend
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccff17ad83b6840b5e8f327e24f8ac8a5e8ff620
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290589"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Uygulama verileri içeren belgeler oluşturmak için yapılandırmaları içeri aktarma

[!include [banner](../../includes/banner.md)]

Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlamanız gerekir.

Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak için nasıl kullanılacağını açıklar. Bu yordamda, örnek şirket Litware, Inc. için oluşturulmuş ER yapılandırmalarını içe aktaracak ve bunları elektronik belgeler oluşturmak için kullanacaksınız. Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir. Başlamadan önce "Elektronik belgeler oluşturma ve uygulama verisini ER aracı ile güncelleştirme" başlıklı Yardım makalesinde belirtilen dosyaları indirin ve kaydedin (generate-electronic-documents-update-application-data/). Dosyalar Intrastat (model).xml, Intrastat (eşleme).xml ve Intrastat (biçim).xml.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.  
    * Bu yordamdaki adımlar ER yeteneklerinin bir uygulama veri güncelleştirmesini tamamlamak ve bir Intrastat raporunu oluşturmak için nasıl kullanılacağını gösterir. Raporlama işleminin ayrıntıları uygulama tablolarında arşivlenir. Şu anda, Intrastat raporlama işlemi Intrastat formunda etkinleştirildiğinde, arşivleme mevcut kaynak kodundaki mantığa dayalı olarak gerçekleştirilir. Bu yordamda, uygulama verisinin benzeri ancak basitleştirilmiş mantığını, yalnızca ER çerçevesini kullanarak yapılandıracaksınız. Kaynak kodda hiçbir değişiklik yapılmayacak.   

## <a name="import-er-configurations"></a>ER yapılandırmaları içe aktarın
1. Raporlama konfigürasyonları'na tıklayın.
2. Değiştir seçeneğine tıklayın.
3. XML dosyasından yükle'ye tıklayın.
    * Intrastat raporunu oluşturmak için veri kaynağı olarak kullanılmak üzere tasarlanmış veri modelini içeren ER model yapılandırmasını içe aktarın. Daha sonra bu veri modeli tanımını, Intrastat raporlama işleminin ayrıntılarını arşivlemek için bir uygulama veri güncelleştirmesi olarak kullanmak üzere genişleteceksiniz.   
    * Gözat'ı tıklatın ve Intrastat (model).xml dosyasını seçin.  
4. Tamam'a tıklayın.
5. Ağaçta, 'Intrastat (model)' öğesini seçin.
6. Tasarımcı'yı tıklatın.
7. Ağaçta 'Giden belge' öğesini genişletin.
8. Ağaçta 'Giden belge\Hareketler' öğesini genişletin.
    * İçe aktarılan veri modelinin yapısını gözden geçirin. 'Giden belge' için ana öğenin uygulamadan veri almak için veri akışı belirtmek için tanımlanır ve Intrastat raporu oluşturmak için veri kaynağı olarak kullanılır. 'Hareketler (Kayıt listesi)' raporlanması gereken Intrastat hareketlerinin listesini temsil etmekte kullanılır. Raporlanan emtia kodlarını arşivleyeceğiniz için, tek bir emtia kodunun benzersiz kimlik tanımlayıcısı 'Emtia rec id (Int64)' bu veri akış içerisinde gereklidir.   
9. Sayfayı kapatın.
10. Değiştir seçeneğine tıklayın.
11. XML dosyasından yükle'ye tıklayın.
    * Uygulamadan veri almak ve bunu daha sonra Intrastat raporunu kullanmak için veri akışını belirten ER eşleme yapılandırmasını içe aktarın. Daha sonra bu model eşleme tanımını, Intrastat raporundan veri almak için genişleteceksiniz ve uygulama verisi güncelleştirmesinde, Intrastat raporlama işleminin ayrıntılarını güncelleştirmek için kullanacaksınız.   
    * Gözat'ı tıklatın ve Intrastat (eşleme).xml dosyasını seçin.  
12. Tamam'a tıklayın.
13. Ağaçta, 'Intrastat (model)' öğesini genişletin.
14. Ağaçta, 'Intrastat (model)\Intrastat (eşleme)' öğesini seçin.
15. Tasarımcı'ya tıklayın.
    * Bu geçerli model eşlemesinin 'Modele' değerini Yön alanında içerdiğini unutmayın. Bu, bu model eşlemesinin uygulamadan veri almak ve veri modelinde depolamak üzere tasarlandığı anlamına geliyor.  
16. Tasarımcı'yı tıklatın.
17. Ağaçta, 'Liste' metnini genişletin.
18. Ağaçta, 'Hareketler= Liste'yi genişletin.
    * 'Giden belge için' kök öğesine dayanarak veri modelini kullanan model eşlemesinin yapısını gözden geçirin. Eklenen veri kaynağı 'Liste'nin, gerekli uygulama verisine erişim sağladığını, bunun da Intrastat tablosundaki kayıtların listesi olduğunu unutmayın.  
19. Sayfayı kapatın.
20. Sayfayı kapatın.
21. Değiştir seçeneğine tıklayın.
22. XML dosyasından yükle'ye tıklayın.
    * Intrastat raporunun biçimini ve veriyi rapora doldurma işlemini belirten ER biçim yapılandırmasını içe aktarın. Daha sonra bu biçim tanımını, Intrastat raporundan veri modeline veri yerleştirmek için genişleteceksiniz ve daha sonra uygulama verisi güncelleştirmesinde, Intrastat raporlama işleminin ayrıntılarını güncelleştirmek için kullanacaksınız.   
    * Gözat'ı tıklatın ve Intrastat (biçim).xml dosyasını seçin.  
23. Tamam'a tıklayın.
24. Ağaçta, 'Intrastat (model)\Intrastat (biçim)' öğesini seçin.
25. Tasarımcı'yı tıklatın.
26. Genişlet/daralt'a tıklayın.
27. Ağaçta 'Dosya\Bildirim' öğesini seçin.
28. Eşleme sekmesini tıklatın.
29. Ağaçta, 'Dosya' metnini seçin.
    * Intrastat raporunu oluşturmak için kullanılan biçimin yapısını gözden geçirin. 'Giden belge' ana öğesi üzerine dayanan veri modelinden verileri yerleştirerek bir XML dosyası oluşturmak üzere tasarlandığını unutmayın. Oluşturulan dosyanın adının kullanıcı iletişim kutusunda tanımlandığından emin olun (bunun için 'fn' veri kaynağı kullanılır).   
30. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
