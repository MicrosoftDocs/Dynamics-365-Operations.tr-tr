---
title: Derecelendirme ve incelemeleri yönetme
description: Bu makale, Microsoft Dynamics 365 Commerce site oluşturucuda derecelendirmelerin ve incelemelerin nasıl yönetileceğini açıklamaktadır.
author: gvrmohanreddy
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79738030d4e33ceaad105a404b8188384d5a320c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881335"
---
# <a name="manage-ratings-and-reviews"></a>Derecelendirme ve incelemeleri yönetme

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce site oluşturucuda derecelendirmelerin ve incelemelerin nasıl yönetileceğini açıklamaktadır.

Dynamics 365 Commerce, kötü sözcükleri düzenleyerek metni otomatik olarak gözden geçirmek için Microsoft Azure öğretici hizmeti kullanır. Ayrıca, Moderatörler  Dynamics 365 Commerce site oluşturucuyu kullanarak aşağıdaki el ile görevleri uygulayabilir:

- Bunlara yanıt verip veya onları kaldırarak yapılan gözden geçirmeler.
- Müşterinin isteği üzerindeki müşteri incelemelerini Silin.
- Toplu içe aktarma derecelendirmeleri ve tüm ürünlerle ilgili verileri bir Microsoft Power BI şablonu olarak inceler; böylece derecelendirmelere ve incelemelere ilişkin eğilimler analiz edilebilir.

## <a name="read-a-review"></a>İncelemeyi oku 

Commerce site oluşturucuda bir inceleme okumak için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.
1. Ürün kimliği, ürün adı veya metin İnceleme tarafından gösterilen incelemelere filtre uygulamak için sayfanın sağ üst tarafındaki arama alanını kullanın.

Ek filtreler, gözden geçirmeleri dönem, derecelendirme, kanal veya ilgi durumu (kapalı, yanıtlanan veya rapor edilen) ile sınırlamanıza olanak sağlar.

![Düzenleme giriş sayfası.](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>İncelemeyi yanıtlama 

Bazı durumlarda, bir ürünü satın alan müşteriler memnuniyet veya memnuniyetini veya ürünün nasıl kullanıldığını anlamamaktadır. Bir moderatör olarak, bir gözden geçirme yanıtı postalayabilirsiniz. Bu yanıt, sitede gözden geçirme ile birlikte görüntülenir. 

Commerce site oluşturucuda bir incelemeyi yanıtlamak için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.
1. Yanıt gerektiren incelemeyi bulun ve seçin.
1. Sağdaki özellikler bölmesinde, **Yanıt Ekle**'yi seçin.
1. Yanıt metnini ve Yanıtlayıcı için gösterilmesi gereken adı girin. Varsayılan Yanıtlayıcı adı **moderatör**'dür.
1. Tamamladıktan sonra **Yanıt gönder**'i seçin.

![İncelemeyi yanıtlama.](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Bir inceleme atın 

Bazen, moderatörlerde müşteri incelemelerini ele almak için bir iş doğrulaması vardır. 

Commerce site oluşturucuda bir inceleme almak için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.
1. Alınması gereken incelemeyi bulun ve seçin.
1. Sağdaki Özellikler bölmesinde **İnceleme Kaydet** altından bir kaydetme nedeni seçin ve ardından **Kaydet**'i seçin.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Müşterinin isteği üzerindeki müşteri incelemelerini Silin 

Bazen müşteriler derecelendirmelerinin ve veri incelemelerinin bir e-ticaret Web sitesinden kalıcı olarak silinmesini ister. Müşteriden kaldırma isteği alan bir yönetici, gözden geçirme silme özelliğini kullanarak müşterinin verilerini kaldırabilir. Müşterinin verilerini bulmak ve silmek için, aracının, müşterinin oturum açmak ve gözden geçirmeleri sağlaması için kullandığı e-posta adresini gerekli kılar. 

Commerce site oluşturucuda müşteri verilerini bulmak ve silmek için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Sil**'ne gidin.
1. **E- posta adresine göre kullanıcıları ara** kutusuna müşterinin e-posta adresini girin ve **Ara**'yı seçin.
1. Müşterinin herhangi bir gözden geçirme faaliyeti varsa (örneğin, gönderimleri gözden geçirin, başka bir müşterinin incelemelerinin yardım veya başka bir müşterinin inceliğindeki Yorumlar hakkında oy varsa), sonuçlar gösterilir. Her madde için **Sil** düğmesi bulunur.
1. Silinmesi gereken her bir madde için **Sil**'i seçin. Onaylamanız istendiğinde **Evet**'i seçin. 
    
![Müşteri verilerini silme.](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Verilerin sistemden tümüyle kaldırılması yedi gün kadar sürebilir. Moderatörler müşterileri bu gecikmeyle bilgilendirmelidir.
> - Müşteriler kendi hesap ayarlarında adlarını değiştirdiyseniz, arama sonuçlarında birden çok öğe görünebilir. Bu durumda, müşterinin verilerini tamamen silmek için, aracının her madde için **Sil**'i seçmeniz gerekir. 

## <a name="download-ratings-and-reviews-data"></a>Derecelendirme ve inceleme verileri karşıdan yükleyin

Commerce site oluşturucu moderatörlerin, eğilimleri çözümleyebilmeleri için toplu olarak derecelendirmelere ve verileri gözden geçirmelerine olanak tanır. Temel ölçümleri içeren bir Power BI şablon kullanılabilir. Moderatörler Bu şablonu, Toplu içe aktarılan verileri bağlamak ve bir panoyu görüntülemek için kullanabilir. Özel bir pano oluşturmak zorunda kalmaları gerekmez. Moderatörler, belirli ihtiyaçları karşılamak üzere Power BI şablonu da özelleştirebilir. 

Commerce site oluşturucuda dereceledirmeler ve incelemeler verilerini indirmek için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.
1. Derecelendirmeleri ve inceleme verilerini virgülle ayrılmış değerler (CSV) biçiminde toplu olarak indirmek için **İnceleme verileri indir** i seçin.

## <a name="view-ratings-and-reviews-trends"></a>Derecelendirmelere ve incelemeler trendine bak

Moderatörler, Power BI şablonu bir panodaki eğilimleri görüntüleyebilmeleri için indirebilir.

Commerce site oluşturucuda dereceledirmeler ve incelemeler eğilimlerini görmek için aşağıdaki adımları izleyin.

1. **Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.
1. Şablonu indirmek için **PowerBI şablonu** seçin.

    ![Power BI şablonunu indirme.](media/rnr-moderation-reports.png) 

1. Power BI uygulamayı kullanarak karşıdan yüklenen şablonu açın. Görüntülenen **Web içeriğine erişim** iletişim kutusunu kapatın ve sonra da görüntülenen "Yenile" hata iletisini kapatın.
1. **Giriş** sayfasına gidin, **Düzenle sorgular**'ı seçin ve sonra **veri kaynağı ayarlarını** seçin.
1. **Veri kaynağı ayarları** iletişim kutusunda **kaynağı değiştir** 'i seçin.
1. **URL** alanına önceki yordama indirdiğiniz İnceleme verilerinin yolunu girin (örneğin, **c:\\incelemeler\\İncelemelerVerileri.csv**).

    ![Virgülle ayrılmış değerler iletişim kutusundaki URL alanı.](media/rnr-powerbi-datasource-settings.png) 

1. **Tamam** seçin ve daha sonra **Değişiklikleri uygulay**'ı seçin. Değişikliklerinizi veri kaynağına uygulamak için iki dakika arasında bir süre sürer.
1. Derecelendirmeleri ve İnceleme eğilimlerini görüntülemek için **eğilim sayfası** seçin.

    ![Derecelendirmelere ve incelemeler trendleri.](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirmelere ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri kullanmayı kabul etme](opt-in-ratings-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

[Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme](sync-product-ratings.md)

[Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirme](manual-publish-rating-reviews.md)

[Derecelendirmeleri ve değerlendirmeleri içe ve dışa aktarma](import-export-reviews.md)

[Hizmetten hizmete kimlik doğrulamasını yapılandırma](service-to-service-auth.md)

[Derecelendirmeler ve incelemelerle ilgili SSS](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
