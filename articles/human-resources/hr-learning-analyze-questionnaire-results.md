---
title: Soru formu sonuçlarını analiz etme
description: Soru formu istatistikleri, ortalamalar, toplamlar ve demografik veri kümesine göre yüzdeler hesaplamak için kullanılabilir.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a1a633301097758f222f294d6a0134e67d19d38
ms.sourcegitcommit: 8246ba3872a1f3eaa18c8bb1ba86d3c2142a6e10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/31/2021
ms.locfileid: "7465137"
---
# <a name="analyzing-questionnaire-results"></a>Soru formu sonuçlarını analiz etme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Soru formu istatistikleri, ortalamalar, toplamlar ve demografik veri kümesine göre yüzdeler hesaplamak için kullanılabilir. Bu yordamı başlatmak için **Soru formu** > **Sonuçları görüntüle ve analiz et** > **Soru formu istatistikleri**'ne gidin. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-questionnaire-statistics-record"></a>Soru formu istatistik kaydı yaratın
1. **Soru formu istatistikleri**'ne gidin.
2. **Yeni**'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. **İstatistikler** alanına bir değer yazın.
5. **Tanım** alanına bir değer girin.
6. **Soru formu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. **Genel** sekmesine tıklayın.
    * Anonim sonuçlar veya çalışanların, tüm kişilerden veya başvuranların sonuçlarını dahil etmek isteyip istemediğinizi seçin.  
9. **Çalışan** onay kutusunu seçin veya temizleyin.
    * Sonuçları kıdem veya yaşa göre görüntüleyecekseniz, bu gruplama sonuçları için kullanacağınız aralıkları belirleyin.  
    * Bir yaş aralığı grubuna 5 girmek, sonuçları beş yıllık aralıklarda gruplayacaktır.  
10. **Yaş** alanına bir sayı girin.
    * Hesaplamayı tüm soru formuna karşı mı yoksa her bir sonuç grubuna, her bir soruya ya da her bir soru satırına karşı mı yapmak istediğinizi seçin.  
    * Sonuçları nasıl gruplandırmak istediğinizi seçin.  
    * Örneğin, soru başına ortalama puanı hesaplarsanız, sonuç grubuna göre gruplandırılmış soruları görmek isteyebilirsiniz.  
    * Hesaplamayı dayandırmak istediğiniz temel veriyi seçin.  
    * Örneğin, çalışanlarınız arasında soru formunda kaznaılan ortalama yüzdeyi, çalışanlarınız arasında kazanılan ortalama puana göre görmek istiyorsanız.  
11. **Aralık** sekmesine tıklayın.
    * Sonuç kümesini yalnızca aralık ölçütlerine uyanlarla kısıtlamak için aralıkları kullanın.  
12. **Şuna göre gruplandır** sekmesine tıklayın.
    * Sonuçlarının nasıl görüntüleneceğini belirlemek için gruplandırmaları kullanın.  
    * Örneğin sonuçları önce cinsiyet sonra da yaşa göre gruplayın.  
13. Listede, istenen kaydı bulun ve seçin.
    * Gruplandırmaları **Seçili** tarafa taşıyın ve istediğiniz sırada yerleştirin.  

## <a name="execute-the-statistics-calculation"></a>İstatistik hesaplamalarını çalıştırma
1. **Yürüt**'e tıklayın.
    * Sonuçların üzerinde gerçekleştirmek istediğiniz hesaplama işlevini seçin.  
    * Örneğin seçili gruplamalar için soru formları arasında ortalama yüzdeyi hesaplamak veya seçili gruplamalar arasında toplam puanları hesaplamak için.  
2. **Önceki aramaları sil** onay kutusunu işaretleyin veya işareti kaldırın.
3. **Tamam**'a tıklayın.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Soru formu istatistiklerinin çalıştırma sonucunu görüntüleyin.
1. **Sonuç**'a tıklayın.
2. **Sonuç**'a tıklayın.
3. Sayfayı kapatın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
