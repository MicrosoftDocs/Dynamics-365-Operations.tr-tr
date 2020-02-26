---
title: Derecelendirme ve incelemeleri yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce derecelendirmeleri ve incelemeler denetleme aracı kullanılarak derecelendirmelerin ve incelemelerinin nasıl yönetileceği açıklanmaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027254"
---
# <a name="manage-ratings-and-reviews"></a>Derecelendirme ve incelemeleri yönetme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce derecelendirmeleri ve incelemeler denetleme aracı kullanılarak derecelendirmelerin ve incelemelerinin nasıl yönetileceği açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce, kötü sözcükleri düzenleyerek metni otomatik olarak gözden geçirmek için Microsoft Azure öğretici hizmeti kullanır. Ayrıca, moderörler, aşağıdaki el ile görevlerde derecelendirmeler ve gözden geçirme denetleme aracını kullanabilirler:

- Bunlara yanıt verip veya onları kaldırarak yapılan gözden geçirmeler.
- Müşterinin isteği üzerindeki müşteri incelemelerini Silin.
- Toplu içe aktarma derecelendirmeleri ve tüm ürünlerle ilgili verileri bir Microsoft Power BI şablonu olarak inceler; böylece derecelendirmelere ve incelemelere ilişkin eğilimler analiz edilebilir.

## <a name="access-ratings-and-reviews-moderation-features"></a>Erişim derecelendirmeleri ve gözden geçirme denetleme özellikleri

E-Ticaret Site Yönetimi aracındaki derecelendirmelere ve gözden geçirme özelliklerine erişmek için, aşağıdaki adımları izleyin.

1. [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com)'de oturum açın.
1. E-ticaret başlatmak istediğiniz ortamı içeren projeyi açın.
1. **Ortamlar** bölümünde, ortamı seçin.
1. **Ortam özellikleri** altında, **Perakende yönetimi**'i tıklatın.
1. **Bağlantılar**'ın altındaki **e- ticaret** sekmesinde, **e- ticaret site yönetim aracı**'nı seçin.

## <a name="read-a-review"></a>İncelemeyi oku 

1. **Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.
1. Ürün kimliği, ürün adı veya metin İnceleme tarafından gösterilen incelemelere filtre uygulamak için sayfanın sağ üst tarafındaki arama alanını kullanın.

Ek filtreler, gözden geçirmeleri dönem, derecelendirme, kanal veya ilgi durumu (kapalı, yanıtlanan veya rapor edilen) ile sınırlamanıza olanak sağlar.

![Düzenleme giriş sayfası](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>İncelemeyi yanıtlama 

Bazı durumlarda, bir ürünü satın alan müşteriler memnuniyet veya memnuniyetini veya ürünün nasıl kullanıldığını anlamamaktadır. Bir moderatör olarak, bir gözden geçirme yanıtı postalayabilirsiniz. Bu yanıt, sitede gözden geçirme ile birlikte görüntülenir. 

Bir incelemeyi yanıtlamak için şu adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.
1. Yanıt gerektiren incelemeyi bulun ve seçin.
1. Sağdaki özellikler bölmesinde, **Yanıt Ekle**'yi seçin.
1. Yanıt metnini ve Yanıtlayıcı için gösterilmesi gereken adı girin. Varsayılan Yanıtlayıcı adı **moderatör**'dür.
1. Tamamladıktan sonra **Yanıt gönder**'i seçin.

![İncelemeyi yanıtlama](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Bir inceleme atın 

Bazen, moderatörlerde müşteri incelemelerini ele almak için bir iş doğrulaması vardır. 

Bir incelemeyi göndermek için şu adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.
1. Alınması gereken incelemeyi bulun ve seçin.
1. Sağdaki Özellikler bölmesinde bir alt neden seçin ve sonra **aşağı al** 'ı seçin.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Müşterinin isteği üzerindeki müşteri incelemelerini Silin 

Bazen müşteriler derecelendirmelerinin ve veri incelemelerinin bir e-ticaret Web sitesinden kalıcı olarak silinmesini ister. Müşteriden kaldırma isteği alan bir yönetici, gözden geçirme silme özelliğini kullanarak müşterinin verilerini kaldırabilir. Müşterinin verilerini bulmak ve silmek için, aracının, müşterinin oturum açmak ve gözden geçirmeleri sağlaması için kullandığı e-posta adresini gerekli kılar. 

Müşteri verilerini bulmak ve silmek için, aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Sil**'ne gidin.
1. **E- posta adresine göre kullanıcıları ara** alanına müşterinin e-posta adresini girin ve **ara** 'yı seçin.
1. Müşterinin herhangi bir gözden geçirme faaliyeti varsa (örneğin, gönderimleri gözden geçirin, başka bir müşterinin incelemelerinin yardım veya başka bir müşterinin inceliğindeki Yorumlar hakkında oy varsa), sonuçlar gösterilir. Her madde için **Sil** düğmesi bulunur.
1. Silinmesi gereken her bir madde için **Sil**'i seçin. Onaylamanız istendiğinde **Evet**'i seçin. 
    
![Müşteri verilerini silme](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Verilerin sistemden tümüyle kaldırılması yedi gün kadar sürebilir. Moderatörler müşterileri bu gecikmeyle bilgilendirmelidir.
> - Müşteriler kendi hesap ayarlarında adlarını değiştirdiyseniz, arama sonuçlarında birden çok öğe görünebilir. Bu durumda, müşterinin verilerini tamamen silmek için, aracının her madde için **Sil**'i seçmeniz gerekir. 

## <a name="download-ratings-and-reviews-data"></a>Derecelendirme ve inceleme verileri karşıdan yükleyin

Derecelendirmeler ve inceleme denetleme aracı, moderatörlerin, eğilimleri çözümleyebilmeleri için toplu olarak derecelendirmelere ve verileri gözden geçirmelerine olanak tanır. Temel ölçümleri içeren bir Power BI şablon kullanılabilir. Moderatörler Bu şablonu, Toplu içe aktarılan verileri bağlamak ve bir panoyu görüntülemek için kullanabilir. Özel bir pano oluşturmak zorunda kalmaları gerekmez. Moderatörler, belirli ihtiyaçları karşılamak üzere Power BI şablonu da özelleştirebilir. 

Derecelendirmeleri karşıdan yüklemek ve verileri gözden geçirmeleri için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.
1. Derecelendirmeleri ve inceleme verilerini virgülle ayrılmış değerler (CSV) biçiminde toplu olarak indirmek için **inceleme verileri indir**i seçin.

## <a name="view-ratings-and-reviews-trends"></a>Derecelendirmelere ve incelemeler trendine bak

Moderatörler, Power BI şablonu bir panodaki eğilimleri görüntüleyebilmeleri için indirebilir.

Derecelendirmeleri karşıdan göstermek ve trendleri gözden geçirmeleri için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.
1. Şablonu indirmek için **PowerBI şablonu** seçin.

    ![Power BI şablonunu indirme](media/rnr-moderation-reports.png) 

1. Power BI uygulamayı kullanarak karşıdan yüklenen şablonu açın. Görüntülenen **Web içeriğine erişim** iletişim kutusunu kapatın ve sonra da görüntülenen "Yenile" hata iletisini kapatın.
1. **Giriş** sayfasına gidin, **Düzenle sorgular**'ı seçin ve sonra **veri kaynağı ayarlarını** seçin.
1. **Veri kaynağı ayarları** iletişim kutusunda **kaynağı değiştir** 'i seçin.
1. **URL** alanına önceki yordama indirdiğiniz İnceleme verilerinin yolunu girin (örneğin, **c:\\incelemeler\\İncelemelerVerileri.csv**).

    ![Virgülle ayrılmış değerler iletişim kutusundaki URL alanı](media/rnr-powerbi-datasource-settings.png) 

1. **Tamam** seçin ve daha sonra **Değişiklikleri uygulay**'ı seçin. Değişikliklerinizi veri kaynağına uygulamak için iki dakika arasında bir süre sürer.
1. Derecelendirmeleri ve İnceleme eğilimlerini görüntülemek için **eğilim sayfası** seçin.

    ![Derecelendirmelere ve incelemeler trendleri](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirme ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri kullanmayı kabul etme](opt-in-ratings-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

[Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme](sync-product-ratings.md)
