---
title: "Bütçelemeye genel bakış"
description: "Hemen hemen her şirket Finansmanı işlevselliği Microsoft Dynamics 365 içinde işlemlerinde kullanır gerçek tutar ile Bütçe raporlarını görebilmek sahip olacaktır. Bu makalede, bütçe işlemleri için Dynamics 365 oluşturun veya bunları bir üçüncü taraf program yüklemek için gereken en düşük yapılandırma anlatılmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Bütçelemeye genel bakış

Hemen hemen her şirket Finansmanı işlevselliği Microsoft Dynamics 365 içinde işlemlerinde kullanır gerçek tutar ile Bütçe raporlarını görebilmek sahip olacaktır. Bu makalede, bütçe işlemleri için Dynamics 365 oluşturun veya bunları bir üçüncü taraf program yüklemek için gereken en düşük yapılandırma anlatılmaktadır.

<a name="overview"></a>Özet
--------

Tüzel kişilik için onaylanan bütçe *bütçe kayıt girişi* olarak bilinen bir belge içinde tutulur. Bütçe kayıt girdi belgesindeki satırları olarak da bilinir *bir bütçe hesabına* girdi ve mali boyut bilgileri, tarihleri ve onaylanan bütçe tutarlarını içerir. Bütçe kayıt giriş belgesi, temel finansal raporlar ve sorgu sayfaları burada fiili tutarlar genel muhasebe bütçe tutarları karşılaştırılır ile tümleşiktir. 

Dynamics 365 işlemler için kayıt girişlerini bütçe oluşturmak için birden çok yöntem vardır:

-   Belge bilgilerini **bütçe kayıt girişleri** sayfasına el ile girin.
-   **Bütçe kayıt girişleri** sayfasında **Excel'de aç** düğmesini tıklatarak açabileceğiniz Microsoft Excel şablonunu kullanın.
-   Bütçe kayıt girişlerini almak için Veri yönetiminde**Bütçe Hesabı Girişleri** veri varlığını kullanın. Açma ve bu yöntemi kullanarak düşünmelisiniz **dayanarak ayarlanacağını** ** işleme ** parametre sistemine birçok bütçe hesabı girişleri alırken gerekir.
-   Şirket bütçe verileri hazırlamak için bütçe planlama işlevini kullanıyorsa, **bütçe kayıt girdisi oluşturur** dönemsel işlemini kullanabilirsiniz.

Bütçe kayıt girişi bütçe bakiyeleri güncelleştirildiği tamamlandı olarak kabul edilir. Üzerinde **bütçe girişlerini kaydetmek** sayfasında,'ı **bütçe bakiyelerini güncelleştirmek** için seçilen bütçe girişi ya da birden çok girdi kaydetmek. Bütçe bakiyelerini güncelleştirdikten sonra, bütçe kayıt girişi değişiklikleri durumu **Tamamlandı** olarak değişir. Tamamlanan bütçe kayıt girişi düzenleme için yeniden açılamaz. Bu nedenle, bütçe verilerini ayarlanmalıysa, tamamlanan bütçe kayıt giriş verileri düzeltmek yerine yeni bir bütçe kayıt girişi oluşturmanız gerekir.

## <a name="configuration"></a>Yapılandırma
Bütçeleme yapılandırdığınızda, **bütçeleme parametreleri** sayfasından başlayın. Bu sayfada, bütçe günlüğü, bütçe kayıt girişlerini için numara sırası ve çalışma alanlarında varsayılan davranış tanımlamalısınız.

Sonra, bütçe kayıt girişleri onayını yöneten ilkeler varsa, bütçe türü (örneğin, aktarımlar veya düzeltmeler) temel alarak, **bütçeleme iş akışları** sayfasında bütçe kayıt girişi iş akışları oluşturmanız gerekir. Aktarımların iş akışı onayı olmadan izin verilebilir olduğu senaryolar varsa, bu senaryoları desteklemek için bütçe transfer kuralları tanımlayabilirsiniz. 

**Bütçeleme boyutları** sayfasında, hesap planında kullanılan boyutlara göre, bütçeleme için kullanılan mali boyutları seçmeniz gerekir. Tüm mali boyutları veya bunların alt kümelerini bütçeleme için seçebilirsiniz.

Tanımladığınız bir * bütçe modeli * karşılık gelen tüm veya bazı bütçeler. tüm bütçe kayıt girişleri için tek bir bütçe modeli kullanabilirsiniz. Alternatif olarak, bütçe türü, coğrafi konumu veya bütçenin sınıflandırılabildiği başka bir yolla dayalı ayrı modeller oluşturabilirsiniz. 

> [!NOTE] 
> Bütçe denetimi kullanılırsa, tek bir bütçe modeli belirli bir bütçe döngüsüyle ilişkilendirebilirsiniz zaman aralığı. 

Kaydedilecek bütçe hareketlerinin ve tüm ilişkili iş akışının tipini tanımlayan *bütçe kodların * oluşturun. Bütçe kodları aşağıdaki bütçe türlerini destekleyebilir:

-   Orijinal bütçe
-   Transfer et
-   Revizyon
-   Yükümlülük
-   Ön yükümlülük
-   Nakli yekun bütçesi

Bütçe döngüsü boyunca onaylanmış bütçedeki değişikliklerin bir denetim izlemesine sahip olmanızı bütçe kodları sağlar. Bütçe kodu ile ilişkili bir iş akışı, iş akışı bu bütçe kodu kullanan tüm bütçe kayıt girişlerini etkinleştirilecek ve iş akışı adımlarını tamamlanması gerekir önce bütçe kayıt girişi ulaşabilirsiniz, **tamamlandı** aşaması.  

Ayrıca isteğe bağlı olarak ayarlayabilirsiniz *Bütçe transfer kuralları*. Bütçe transfer kuralları kullanmayı seçin **bütçe transferleri için kuralları kullan** üzerinde **bütçe parametreleri** sayfa. Bütçe transfer kuralları kullanıldığında, bir kullanıcı bir bütçe kodu kullanarak **Transfer** tipi bir belge oluşturursa, bütçe bakiyeleri bütçe transfer kuralları ihlal edilirse güncelleştirilmez. Örneğin, gider hesaplarının ana hesaplar arasında satış ve pazarlama departmanı için transfer edildiği bütçe transfer belgelerine izin verebilirsiniz, ancak o tür bütçe hesabı girişi için iş akışı onay verilmemişse o bölüme gelen veya giden aktarılan bütçeyi yasaklayabilirsiniz.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Bütçe ile Gerçek tutar izlemek için çalışma alanları ve sorgulama sayfaları kullanma
Bütçe Yöneticisi **genel muhasebe bütçeleri ve tahminleri** çalışma alanında geçerli bir bütçe durumunu gözden geçirebilir. **Bütçeyi aşan gider** ve **bütçenin altında gelir** sekmeleri bütçe hedefleri karşılanmadığı veya eşiğe yaklaştığı mali boyut birleşimlerinin hızlı bir görünümünü sağlar. Bu sekmelerde kullanılan bütçe eşik yüzdesi ve mali boyut kümelerini **Çalışma alanımı yapılandır**'ı tıklatarak kişiselleştirebilirsiniz. **birim yöneticileri** tıklatarak bu sekmelerinde seçili belirli finansal boyut birleşimlerinden sorumlu çalışanları görebilirsiniz. Örneğin, İşlemler bölümünün gider bütçesinin bütçe eşiği üzerine gittiğini görürseniz, sorunu tartışmak için İşlemler bölüm yöneticisini kolayca bulabilir ve görüşebilirsiniz. 

> [!NOTE] 
> **Bölüm Müdürü** alanına **kuruluş birimlerini** sayfa belirler hangi yöneticileri belirli finansal boyut birleşimleri destekler. Sekmenin altındaki **daha fazla gör**'ü tıklatarak bütçe tutarlarını karşı gerçek tutarları hakkında daha ayrıntılı bilgi için **bütçe - fiili değerler** sorgulama sayfasını açın. 

**Gerçek - bütçe** sorgulama sayfası bütçeye karşı gerçek tutarları bütçe ayrıntısına olanak sağlar. Sorgulama sayfası üzerinde bir satır seçin ve ardından mali döneme yayılan bütçe ve fiili tutarları görmek için **dönem bakiyeleri**'ni tıklatın. **Bütçe hesabı girişleri** sayfası bütçe kayıt girişlerinde bütçe tutarı ayrıntılarını sağlar. **Genel günlük girişleri **sayfası hesaplanan **gerçek** tutara dahil edilen genel muhasebe hareketlerini açar. 

Bütçe planlama işlevselliği kullanan bir şirket **genel muhasebe bütçeleri ve tahminleri** çalışma alanı içinde *bütçe tahminleri * oluşturabilir ve kullanabilir.


