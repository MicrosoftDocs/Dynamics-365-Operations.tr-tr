---
title: Kılavuz yetenekleri
description: Bu konu, kılavuz denetiminin çeşitli güçlü özelliklerini açıklamaktadır. Bu yeteneklere erişim sahibi olmak için yeni kılavuz özelliğinin etkinleştirilmesi gerekir.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020051"
---
# <a name="grid-capabilites"></a>Kılavuz yetenekleri

[!include [banner](../includes/banner.md)]

Yeni kılavuz denetimi, kullanıcı üretkenliğini artırmak, verilerinizin daha ilginç görünümlerini elde etmek ve verilerinize anlamlı bilgiler yüklemek için kullanılabilecek bir dizi yararlı ve güçlü yetenek sağlar. Bu makalede aşağıdaki yetenekler ele alınıyor: 

-  Toplamlar hesaplanıyor
-  Verileri gruplandırma
-  Sistemi önceden hazırlama
-  Matematik ifadelerini değerlendirme 

## <a name="calculating-totals"></a>Toplamlar hesaplanıyor
Finance and Operations uygulamalarında kullanıcılar toplamları ızgaralardaki sayısal sütunların alt kısmında görebilme yeteneğine sahiptir. Bu toplamlar, kılavuzun alt kısmındaki bir alt bilgi bölümünde gösterilir. 

### <a name="showing-the-grid-footer"></a>Kılavuz alt bilgisini gösterme
Finance and Operations uygulamalarındaki her tablo kılavuzunda, kılavuzun alt bölümünde, görüntülenen verilerle ilgili önemli bilgileri gösterebilecek bir alt bilgi alanı vardır. Bu bilgiler şunları içerir: 
-  Tablodaki seçili satır sayısı (birden fazla kayıt seçiliyken)
-  Yapılandırılan sayısal sütunların en altındaki genel toplamlar
-  Veri kümesindeki satır sayısı 

Bu alt bilgi varsayılan olarak gizlidir ancak kolayca etkinleştirilebilir. Bir kılavuzun alt bilgisini göstermek için, kılavuzda bir sütun başlığına sağ tıklayın ve **Alt bilgiyi göster** seçeneğini belirleyin. Alt bilgi belirli bir kılavuz için etkinleştirildikten sonra, kullanıcı bir sütun başlığına sağ tıklayıp **Alt bilgiyi gizle**'yi seçerek alt bilgiyi gizlemeyi seçene kadar bu ayar hatırlanır.  **Alt bilgiyi göster/Alt bilgiyi gizle** eylem yerinin ilerideki bir güncelleştirmede değiştirilmesi bekleniyor. 

### <a name="specifying-columns-with-totals"></a>Sütunları toplamlarla belirtme
Şu anda, sütunlar varsayılan olarak toplamları gösterecek şekilde yapılandırılmayacak. Bunun yerine, bu, ızgaralardaki sütunların genişliklerini ayarlamaya benzer şekilde bir kerelik kurulum faaliyeti olarak görülüyor. Bir sütunun toplamlarını görmek istediğinizi belirttiğinizde, sayfayı bir sonraki ziyaretinizde bu ayar hatırlanır.  

Bir sütunu toplam gösterecek şekilde yapılandırmanın iki yolu vardır: 
1.  Bir toplam görmek istediğiniz sütuna sağ tıklayın ve **Bu sütunun toplamını al**'ı seçin. Bu eylem üç şey yapacaktır. İlk olarak, alt bilgiyi görünür yapar. İkincisi, bu sütunda bir toplam görme tercihinizi kaydeder. Üçüncü olarak, bu eylem bu sütun ve toplamlarını görmek istediğiniz diğer sütunlar için bir toplam hesaplaması başlatır. Bir toplamın gösterilmesi için gereken süre, toplamını aldığınız veri kümesinin boyutuyla doğrudan ilgilidir.  

2.  Alt bilgi gösterildikten sonra, alternatif olarak, bir toplam görmek istediğiniz sütunun alt kısmındaki alt bilgi bölgesinde **Toplamı göster** düğmesine de tıklayabilirsiniz. Yapılandırılmış sütun yoksa, **Toplamı göster** düğmesi tüm sayısal sütunlarda görünür. Toplamlar için en az bir sütun yapılandırıldıktan sonra, **Toplamı göster** düğmeleri yalnızca üzerine gelindiği veya odaklanıldığı zaman ortaya çıkacaktır. Bu eylem, yalnızca bu sayfaya sonraki ziyaretlerde bir toplamı görme tercihinizi kaydeder ve bu durum alt bilgide bu sütunda görünen tireyle belirtilir (veya veri kümesi yeterince küçükse, toplam doğrudan gösterilir).

Bir hata yapar ve artık belirli bir sütundaki toplamı artık görmek istemezseniz, sütuna sağ tıklayın ve **Toplamı gizle**'yi seçin veya bu sütundaki alt bilgide bulunan **Toplamı gizle** düğmesini seçin. Bu tercih, sayfaya ileride yapılacak ziyaretler için de kaydedilecektir. 

### <a name="calculating-totals"></a>Toplamlar hesaplanıyor
Alt bilginin görünür olduğu ve sütunların toplamlar için daha önce yapılandırıldığı bir sayfaya geldiğiniz zaman, toplamlar alt bilgide gösterilebilir veya gösterilmeyebilir. Bu durum sayfadaki veri kümesinin boyutuna bağlıdır. Veri kümesi yeterince küçükse, veri kümesindeki satır sayısıyla birlikte toplamlar otomatik olarak gösterilecektir. Toplamlar için yapılandırdığınız sütunların altındaki alt bilgide tireler varsa, veri kümesi sistemin toplamları hemen gösteremeyeceği kadar büyüktür ve toplamları hesaplamak için belirli bir eylem gerekir. Bunu yapmak için, alt bilgideki **Hesapla** düğmesine tıklayın veya toplamını almak istediğiniz bir sütuna sağ tıklayın ve **Bu sütunun toplamını al**'ı seçin.  

Hesaplama çok uzun sürerse, **İptal** düğmesini seçerek işlemi iptal edebilirsiniz. Ancak bazen veri kümesi toplamları hesaplamak için çok büyük olur (kuruluşunuz tarafından uygulanan bir sınıra göre) ve bunun yerine size verilerinizi daha fazla filtrelemeniz gerektiği bildirilir.

Siz veri kümesinde güncelleştirme, silme veya satır oluşturma işlemleri yaptıkça toplamlar otomatik olarak güncelleştirilir.  

## <a name="grouping-data"></a>Verileri gruplandırma
İş kullanıcılarının sıklıkla anlık olarak veri analizi yapmaları gerekir. Bu işlem Microsoft Excel'e veri aktararak ve özet tablolar kullanarak yapılırken, sekmeli kılavuzlardaki **Gruplandırma** yeteneği sayesinde kullanıcılar verilerini Finance and Operations uygulamalarında ilginç yollarla organize edebilirler. Bu özellik **Toplamlar** özelliğini genişlettiği için, **Gruplandırma** da grup düzeyinde alt toplamlar sunarak verilere anlamlı bilgiler yüklemenize olanak sağlar.

Bu özelliği kullanmak için, gruplandırmada kullanmak istediğiniz sütuna sağ tıklayın ve **Bu sütuna göre gruplandır**'ı seçin. Bu eylem, verileri, seçilen sütuna göre sıralar, kılavuzun başına yeni bir Tabloya göre gruplandır özelliği ve her grubun başına "üst bilgi satırları" ekler. Bu üst bilgi satırları her grup hakkında aşağıdaki bilgileri sağlar: 
-  Grubun veri değeri 
-  Sütun etiketi. Bu, birden çok gruplandırma düzeyi desteklenirken özellikle yararlı olacaktır.  
-  Bu gruptaki veri satırlarının sayısı
-  Toplamları gösterecek şekilde yapılandırılan sütunların alt toplamları

[Kayıtlı görünümler](saved-views.md) etkinleştirildiğinde, sayfayı bir sonraki ziyaretinizde hızlı erişim için bir görünümün parçası olarak bu gruplandırma kişiselleştirerek gruplandırılabilir.  

Başka bir sütunda **Bu sütuna göre gruplandır**'ı seçerseniz, 10.0.9/Platform güncelleştirmesi 33'te yalnızca gruplandırma düzeyi desteklendiği için, özgün gruplandırma değiştirilecektir.

Bir kılavuzda gruplandırmayı geri almak için, gruplandırma sütununa sağ tıklayın ve **Grubu çöz**'ü seçin.  


## <a name="evaluating-math-expressions"></a>Matematik ifadelerini değerlendirme
Bir verimlilik dopingi olarak, kullanıcı sistem dışındaki bir uygulamada hesaplama yapmak zorunda kalmadan bir kılavuzdaki sayısal hücrelere matematiksel formüller girebilir. Örneğin **=15\*4** girip sekmeyi kapatarak alanın dışına çıkabilirsiniz. Sistem ifadeyi değerlendirir ve alan için "60" değerini kaydeder.

Sistemin bir değeri ifade olarak tanımasını sağlamak için, değeri bir eşittir işaretiyle (**=**) başlatın. Desteklenen işleçler ve söz dizimi hakkında daha ayrıntılı bilgi edinmek için bkz. [Desteklenen matematik simgeleri](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
