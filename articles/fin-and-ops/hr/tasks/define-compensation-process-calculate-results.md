--- 
title: "Ücret işlemini tanımlama ve sonuçları hesaplama"
description: "Ücret işlemleri, sabit ve değişken ücret planlarında kayıtlı çalışanlar için yeni ücret tutarlarını ve ödülleri belirlemek için kullanılır."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 950237499441e7f1d5b9e3355c4bd9513ad3783e
ms.openlocfilehash: 9705f3fd7076e010ec4d497c4d933364f3cfcc8f
ms.contentlocale: tr-tr
ms.lasthandoff: 11/01/2017

---
# <a name="define-compensation-process-and-calculate-results"></a>Ücret işlemini tanımlama ve sonuçları hesaplama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ücret işlemleri, sabit ve değişken ücret planlarında kayıtlı çalışanlar için yeni ücret tutarlarını ve ödülleri belirlemek için kullanılır. Tüm değişikliklerin ve ayarların doğruluğunu onaylamak amacıyla "ne yapmalı" analizlerini gerçekleştirmek için birden çok defa çalıştırılabilir. Bu yordam bir ücret işlemi oluşturur, işlemi çalıştırır ve sonuçları görüntüler. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-compensation-process"></a>Ücret işlemi oluşturma
1. İnsan kaynakları > Ücret > İşlem > Ücret işlemleri'ne gidin.
2. Yeni'ye tıklayın.
3. İşlem alanında bir değer girin.
4. Açıklama alanına bir değer girin.
5. İşlem türü alanında bir seçenek belirleyin.
    * Bir döngü, ücreti belirlemek için değerlendirilecek dönemi belirtir. Değerlendirme, hangi pozisyonların çalışanlar tarafından kullanıldığını, hangi performans derecelendirmesinin dahil edileceğini, döngü boyunca çalışanların çalışma süresi yüzdesi hesaplamasını ve daha fazlasını göz önüne alır. Dngü başlangıç tarihinin bir örneği önceki mali yılın ilk günü olabilir.  
6. Döngü başlangıç tarihi alanında bir tarih girin.
    * Döngü bitiş tarihi, hangi çalışanların aktif çalıştığını ve bir veya daha fazla ücret planına kaydolduğunu belirlemek için kullanılan tarih olduğundan önemlidir.  
7. Döngü bitiş tarihi alanında bir tarih girin.
    * Hareket etkin tarihi, yeni ücret oranlarının etkili olması gereken tarihtir. Birçok şirket kendi döngüsünün sonu ile yeni ücret oranlarının yürürlüğe gireceği süre arasında birkaç ay bırakır. Ek zaman, yeni maaşı işleme koyma ve gözden geçirme için kullanılır.  
8. Hareket etkin tarihi alanında bir tarih girin.
    * Zaman noktası, çalışanın ilgili zaman noktasındaki ücret oranlarına dayalı ödül miktarını belirleyen değişken ücret planları için kullanılır.  
    * Sabit ödemeli eşit dağıtılmış işe alma tarihi, işe alma kuralı yüzdesi olan sabit ücret planlarıyla birlikte kullanılır.  Döngü başlangıç tarihi ile sabit ödemeli eşit dağıtılmış işe alma tarihi arasındaki dönemde işe alınan çalışanlar eşit dağıtılmış yüzde yerine hesaplanan ücret artışlarının %100'ünü alırlar.  
9. Sabit ödemeli eşit dağıtılmış işe alma tarihi alanında bir tarih girin.
    * Gözden geçirme son tarihi, o zamana kadar tüm işlem sonuçlarının gözden geçirileceği tarihtir; böylece sonuçlar hareket etkin tarihinden önce bir çalışanın ücret kaydına yüklenebilir. Bu alan yalnızca bilgi amaçlıdır.  
10. İnceleme son tarihi alanında bir tarih girin.
11. Kaydet'e tıklayın.

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a>Bir ücret işlemi için ücret planları ve eylemleri ayarlama
1. Kurulum’u tıklatın.
    * Ayarlar sayfası bu ücret işleminin parçası olarak işlenecek planların hangileri olacağının seçmenin yanı sıra her bir plan için gerçekleştirilecek işlemleri belirlemek için de kullanılır.  
2. Plan alanında bir değer girin veya bir değer seçin.
3. Kaydet'e tıklayın.
4. Ekle öğesini tıklatın.
5. İşlem alanında işlemin öz varlık türünü belirleyin.
6. Ekle öğesini tıklatın.
7. İşlem alanında işlemin liyakat türünü belirleyin.
    * Ücret işlemleri, seçilen işlem için bu işlemin hesaplamasında çalışanın taban ödemesinin mi yoksa önceki işlemin sonucunun mu başlangıç noktası olarak kullanılacağını belirlemek üzere Önceki sonucu kullan alanı kullanılarak birlikte "kayıt altına alınabilir".  
8. Önceki sonucu kullan alanında Evet'i seçin.
9. Ekle öğesini tıklatın.
10. İşlem alanında İşlemin Genel türünü belirleyin.
    * Farklı ücret işlemi türleri farklı alanları etkinleştirir. Genel ücret işlemi türü için bir artış yüzdesi veya artış miktarı belirtilebilir.  
11. Artış tutarını seç seçeneğini belirleyin.
12. Artış miktarı alanında bir sayı girin.
13. Ekle öğesini tıklatın.
14. İşlem alanında İşlemin Promosyon türünü belirleyin.
    * Terfi ve Diğer düzey değişikliği işlem türleri, kullanıcılara çalışan ücreti düzenlemelerini el ile yapma olanağı sağlar. Öneriler bu eylem türlerinin yanı sıra bir çalışan için yeni önerilen ücret değeri girilmesini sağlayacak diğer eylem türleri de etkinleştirilebilir.  
15. Ekle öğesini tıklatın.
16. Tür alanında, bir seçenek seçin.
    * Sabit ve değişken ücret planları aynı ücret işleminde çalıştırılabilir.  
17. Plan alanında bir değer girin veya bir değer seçin.
    * Sabit ve değişken ücret miktarlarının çalışanın performans derecesine göre mi düzenlenmesi gerektiğini belirlemek üzere Performans için ödemeyi etkinleştir onay kutusunu kullanın.  
    * Dengeleme, değişken ücret planlarında geçersiz kılınabilir.  
18. Kaydet'e tıklayın.
19. Ekle öğesini tıklatın.
20. Sayfayı kapatın.

## <a name="run-the-compensation-process"></a>Ücret işlemini çalıştırma
1. İşlemi çalıştır'ı tıklatın.
    * İşlem sonuçlarını göster denetimi, işleme sonlandığında tam ücret işleminin işlem iletilerini görüntülemenizi sağlar.  
2. İşlem sonuçlarını göster alanında Evet'i seçin.
3. Tamam'a tıklayın.

## <a name="view-the-results"></a>Sonuçları görüntüleme
1. İşlem sonuçları'nı tıklatın.
2. Çalışan sonuçları'nı tıklatın.
3. Listede, istenen kaydı bulun ve seçin.
4. Sabit ücret bölümünü genişletin.
    * İşleminin sonuçlarını görüntülemek için FastTabs'i genişletin. Bir ücret işlemi için Önerileri etkinleştir işaretlenmişse, bu işlem için Öneri alanları etkinleştirilir.  
5. Listede, istenen kaydı bulun ve seçin.
    * Tek bir çalışana ilişkin sonuçlar Sonuçları görüntüle düğmesi tıklatılarak görüntülenebilir.  
    * Öneri alanlarında yüzdeyi veya artış tutarını ayarlayarak hesaplanan ücret tutarının üzerine yazabilirsiniz.  
6. Yüzde önerisi alanında bir sayı girin.
7. Listede, istenen kaydı bulun ve seçin.
8. Yüzde önerisi alanında bir sayı girin.
    * Yeniden hesapla öğesi, mevcut kayda yapılan değişiklikleri yoksaymak ve seçili çalışan için yeni bir ücret sonucu oluşturmak için kullanılabilir.  
    * Bir çalışan için tüm değişiklikler tamamlandığında, durumu Onaylandı olarak değiştirin.  
9. Durumu değiştir öğesine tıklayın.
10. Onaylandı’yı tıklatın.
    * Kayıt onaylandıktan sonra çalışanın resmi ücret kaydına yüklenebilir. Yeni ücret, ücret işleminde ayarlanan hareket tarihi itibariyle geçerli olur.  


