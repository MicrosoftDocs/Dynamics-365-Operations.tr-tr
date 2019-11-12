---
title: Bütçelemeye genel bakış
description: Microsoft Dynamics 365 Finance içerisinde Finansal işlevleri kullanan hemen her şirket, bütçe - fiili karşılaştırma raporlarını oluşturmak zorunda olacaktır. Bu makale, Finance and Operations içerisinde bütçeler oluşturmak veya bunları bir üçüncü taraf programdan yüklemek için gereken asgari yapılandırmayı açıklar.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36144474defc4849a112a180247f37796de00a27
ms.sourcegitcommit: 1eaa3451275fe4223d4d25b37aaa1cd2b183e803
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667472"
---
# <a name="budgeting-overview"></a>Bütçelemeye genel bakış 

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance içerisinde Finansal işlevleri kullanan hemen her şirket, bütçe - fiili karşılaştırma raporlarını oluşturmak zorunda olacaktır. Bu makale, Finance and Operations içerisinde bütçeler oluşturmak veya bunları bir üçüncü taraf programdan yüklemek için gereken asgari yapılandırmayı açıklar.

<a name="overview"></a>Özet
--------

Tüzel kişilik için onaylanan bütçe *bütçe kayıt girişi* olarak bilinen bir belge içinde tutulur. Bütçe kaydı giriş belgesindeki satırlar *bütçe hesabı* girişleri olarak bilinir ve mali boyut bilgileri, tarihler ve onaylanan bütçelerin tutarlarını içerir. Bütçe kayıt giriş belgesi, genel muhasebe fiili tutarların bütçe tutarlarıyla karşılaştırıldığı temel mali raporlar ve sorgu sayfaları ile tümleşiktir. 

Bütçe kayıt girişleri oluşturmak için birden çok yöntem vardır:

-   Belge bilgilerini **bütçe kayıt girişleri** sayfasına el ile girin.
-   **Bütçe kayıt girişleri** sayfasında **Excel'de aç** düğmesini tıklatarak açabileceğiniz Microsoft Excel şablonunu kullanın.
-   Bütçe kayıt girişlerini almak için Veri yönetiminde **Bütçe Hesabı Girişleri** veri varlığını kullanın. Bu yöntemi kullanmayı ve bütçe hesabı girişlerini sisteme almanız gerektiğinde **Ayarlama tabanlı** **işlem** parametresini kullanmayı düşünmelisiniz.
-   Şirket bütçe verileri hazırlamak için bütçe planlama işlevini kullanıyorsa, **bütçe kayıt girdisi oluşturur** dönemsel işlemini kullanabilirsiniz.

Bütçe kayıt girişi, bütçe bakiyeleri güncelleştirildiğinde tamamlandı olarak kabul edilir. **Bütçe kayıt girişleri** sayfası üzerinde, seçilen bir bütçe kaydı girişi veya birden fazla giriş için **Bütçe bakiyelerini güncelleştir**'i tıklatın. Bütçe bakiyelerini güncelleştirdikten sonra, bütçe kayıt girişi değişiklikleri durumu **Tamamlandı** olarak değişir. Tamamlanan bütçe kayıt girişi düzenleme için yeniden açılamaz. Bu nedenle, bütçe verilerini ayarlanmalıysa, tamamlanan bütçe kayıt giriş verileri düzeltmek yerine yeni bir bütçe kayıt girişi oluşturmanız gerekir.

## <a name="configuration"></a>Yapılandırma
Bütçeleme yapılandırdığınızda, **bütçeleme parametreleri** sayfasından başlayın. Bu sayfada, bütçe günlüğü, bütçe kayıt girişlerini için numara sırası ve çalışma alanlarında varsayılan davranış tanımlamalısınız.

Sonra, bütçe kayıt girişleri onayını yöneten ilkeler varsa, bütçe türü (örneğin, aktarımlar veya düzeltmeler) temel alarak, **bütçeleme iş akışları** sayfasında bütçe kayıt girişi iş akışları oluşturmanız gerekir. Aktarımların iş akışı onayı olmadan izin verilebilir olduğu senaryolar varsa, bu senaryoları desteklemek için bütçe transfer kuralları tanımlayabilirsiniz. 

**Bütçeleme boyutları** sayfasında, hesap planında kullanılan boyutlara göre, bütçeleme için kullanılan mali boyutları seçmeniz gerekir. Tüm mali boyutları veya bunların alt kümelerini bütçeleme için seçebilirsiniz.

Tüm veya bazı bütçelere karşılık gelen bir *bütçe modeli* tanımlayın. tüm bütçe kayıt girişleri için tek bir bütçe modeli kullanabilirsiniz. Alternatif olarak, bütçe türü, coğrafi konumu veya bütçenin sınıflandırılabildiği başka bir yolla dayalı ayrı modeller oluşturabilirsiniz. 

> [!NOTE] 
> Bütçe denetimi kullanılırsa, tek bir bütçe modeli belirli bir bütçe döngüsü zaman aralığıyla ilişkilendirebilirsiniz. 

Kaydedilecek bütçe hareketlerinin ve tüm ilişkili iş akışının tipini tanımlayan *bütçe kodların* oluşturun. Bütçe kodları aşağıdaki bütçe türlerini destekleyebilir:

-   Orijinal bütçe
-   Transfer et
-   Revizyon
-   Yükümlülük
-   Ön yükümlülük
-   Nakli yekun bütçesi

Bütçe döngüsü boyunca onaylanmış bütçedeki değişikliklerin bir denetim izlemesine sahip olmanızı bütçe kodları sağlar. Bir iş akışı bir bütçe koduyla ilişkilendirilmişse, iş akışı bu bütçe kodunu kullanan tüm bütçe kayıt girişleri için etkinleştirilecektir ve iş akışı adımları, bütçe kayıt girişi **Tamamlandı** aşamasına ulaşmadan önce tamamlanmalıdır.  

Ayrıca isteğe bağlı olarak *bütçe transfer kuralları* da ayarlayabilirsiniz. Bütçe transfer kurallarını kullanmak için **Bütçe transferleri için kuralları kullan** seçeneğini, **Bütçe parametreleri** sayfası üzerinde seçin. Bütçe transfer kuralları kullanıldığında, bir kullanıcı bir bütçe kodu kullanarak **Transfer** tipi bir belge oluşturursa, bütçe bakiyeleri bütçe transfer kuralları ihlal edilirse güncelleştirilmez. Örneğin, gider hesaplarının ana hesaplar arasında satış ve pazarlama departmanı için transfer edildiği bütçe transfer belgelerine izin verebilirsiniz, ancak o tür bütçe hesabı girişi için iş akışı onay verilmemişse o bölüme gelen veya giden aktarılan bütçeyi yasaklayabilirsiniz.

Microsoft Dynamics 365 Finance sürüm 10.0.7'de (Ocak 2020) sunulan işlev, bütçe kayıt girişleri için daha fazla yetenek ve esneklik sağlar. Bu geliştirmeleri etkinleştirmek için **Özellik yönetimi** çalışma alanına gidin ve **Yalnızca miktar için bütçe kaydı girişleri**'ni ve/veya **Tutar türü için bütçe kaydı girişleri varsayılanı**'nı seçin.

Yalnızca **miktar için bütçe kaydı girişleri** özelliği bütçe kaydı girişini yalnızca miktar tutarları ile deftere nakletmenize olanak tanır. Örneğin, miktarı 32 ve fiyatı 0 olan bir bütçeyi (bu durumda tutar 0 olur) deftere nakledebilirsiniz. Bu miktarı, miktar başına bir fiyat belirlemek için bir mali rapor bağlamında kullanabilirsiniz. Bu özelliğin bir parçası olarak hiçbir sorgu veya raporun güncelleştirilmediğini unutmayın; özellik yalnızca sıfır tutarını deftere nakletmenizi sağlar.

**Tutar türü için bütçe kaydı girişleri varsayılanı** özellği bir bütçe kaydı girişi içindeki varsayılan tutar türünün gider dışındaki bir tutar olmasına olanak sağlar. Ana hesap türü gider olduğunda, bütçe kayıt girişi satırı varsayılan olarak giderolacaktır; ana hesap türü gider olduğunda varsayılan olarak gelir ve diğer tüm hesap türleri için varsayılan olarak gider olacaktır.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Bütçe ile Gerçek tutar izlemek için çalışma alanları ve sorgulama sayfaları kullanma
Bütçe Yöneticisi **genel muhasebe bütçeleri ve tahminleri** çalışma alanında geçerli bir bütçe durumunu gözden geçirebilir. **Bütçeyi aşan gider** ve **bütçenin altında gelir** sekmeleri bütçe hedefleri karşılanmadığı veya eşiğe yaklaştığı mali boyut birleşimlerinin hızlı bir görünümünü sağlar. Bu sekmelerde kullanılan bütçe eşik yüzdesi ve mali boyut kümelerini **Çalışma alanımı yapılandır**'ı tıklatarak kişiselleştirebilirsiniz. **birim yöneticileri** tıklatarak bu sekmelerinde seçili belirli finansal boyut birleşimlerinden sorumlu çalışanları görebilirsiniz. Örneğin, İşlemler bölümünün gider bütçesinin bütçe eşiği üzerine gittiğini görürseniz, sorunu tartışmak için İşlemler bölüm yöneticisini kolayca bulabilir ve görüşebilirsiniz. 

> [!NOTE] 
> **Kuruluş Birimleri** sayfasındaki **Bölüm müdürü** alanı, hangi yöneticilerin belirli finansal boyut birleşimleri desteklediğini belirler. Sekmenin altındaki **daha fazla gör**'ü tıklatarak bütçe tutarlarını karşı gerçek tutarları hakkında daha ayrıntılı bilgi için **bütçe - fiili değerler** sorgulama sayfasını açın. 

**Gerçek - bütçe** sorgulama sayfası bütçeye karşı gerçek tutarları bütçe ayrıntısına olanak sağlar. Sorgulama sayfası üzerinde bir satır seçin ve ardından mali döneme yayılan bütçe ve fiili tutarları görmek için **dönem bakiyeleri**'ni tıklatın. **Bütçe hesabı girişleri** sayfası bütçe kayıt girişlerinde bütçe tutarı ayrıntılarını sağlar. **Genel günlük girişleri** sayfası hesaplanan **gerçek** tutara dahil edilen genel muhasebe hareketlerini açar. 

Bütçe planlama işlevselliği kullanan bir şirket **genel muhasebe bütçeleri ve tahminleri** çalışma alanı içinde *bütçe tahminleri* oluşturabilir ve kullanabilir.



