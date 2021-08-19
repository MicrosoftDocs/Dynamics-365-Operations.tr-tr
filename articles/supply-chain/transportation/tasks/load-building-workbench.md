---
title: Yük oluşturma çalışma ekranı
description: Bu konuda, yük oluşturma ekranı ile nasıl çalışılacağı açıklanmaktadır.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5b1ab86be84f3ade58ea354417bfcc2dc0bd87e9e2cb8debb36ea43f7b877f54
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714270"
---
# <a name="load-building-workbench"></a>Yük oluşturma çalışma ekranı

Yük oluşturma ekranı, yük oluştururken yük oluşturma stratejilerini uygulamanıza olanak sağlar.

## <a name="create-a-load-building-strategy"></a>Yük oluşturma stratejisi oluşturma

Yükleri otomatik olarak oluşturmak için yük oluşturma stratejilerini kullanabilirsiniz. Bu özellik, aşağıdaki durumlarda yararlı olabilir:

- Belirli bir ürün kümesini düzenli olarak sevk ediyorsanız yük stratejileri zamandan tasarruf etmenize yardımcı olur çünkü her seferinde aynı yükü oluşturmak zorunda kalmazsınız.
- Verimliliği en yüksek düzeye çıkarmak için yarı dolu yükleri önlemek istiyorsanız yük stratejileri her bir yükü mümkün olduğunca doldurmaya yardımcı olabilir.

`TMSLoadBuildingVolumeStrategy` adlı bir yük oluşturma stratejisi sınıfı, *Hacim temelli yük oluşturma stratejisi* adında bir oluşturma stratejisi elde etmenizi sağlar. Bu strateji, yük şablonunda yükseklik ve ağırlık için belirtilen maksimum değerleri kullanmanıza olanak tanır; veya yeni değerler girerek ayarları geçersiz kılabilirsiniz. Bu strateji kullanıma hazır olarak sunulan tek stratejidir. (Ancak, bazı özel stratejileriniz olabilir.)

Kullanıma hazır *Hacim temelli yük oluşturma stratejisi* adlı stratejiyi kullanmak için **Yük oluşturma çalışma ekranı** sayfasındaki (**Taşıma yönetimi &gt; Planlama &gt; Yük oluşturma çalışma ekranı**) **Yük oluşturma stratejisi** alanından seçin.

Yük oluşturma stratejisi oluşturmak için şu adımları izleyin.

1. **Taşıma yönetimi &gt; Kurulum &gt;Yük oluşturma &gt; Yük oluşturma stratejileri**'ne gidin.
1. Eylem bölmesinde, tüm kullanılabilir sınıfların en son sürümlerine sahip olduğunuzdan emin olmak için **Sınıf listesini oluştur**'u seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Strateji için benzersiz bir ad girin, yük oluşturma stratejisi sınıfını seçin ve açıklama girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem Bölmesi'nde, **Parametreler**'i seçin.
1. **Yük oluşturma stratejisi** parametreleri sayfasında, listeden **Hacim kapasitesi**'ni seçin ve ardından **Değer** alanına yeni yük oluşturma stratejisi için uygulanacak yük toplam hacim kapasitesi yüzdesini girin.
1. Listeden **Ağırlık kapasitesi**'ni seçin ve ardından **Değer** alanına yeni yük oluşturma stratejisi için uygulanacak yük toplam ağırlık kapasitesi yüzdesini girin.
1. **Yük oluşturma stratejisi parametreleri** sayfasını kapatın.
1. **Yük oluşturma stratejileri** sayfasını kapatın.

Yük oluşturma stratejisini artık bir yük oluşturma şablonuna atayabilirsiniz. Alternatif olarak, bunu doğrudan yük planlama çalışma ekranında da kullanabilirsiniz.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Yük oluşturma çalışma ekranında yük oluşturma stratejisi kullanma

1. **Taşıma yönetimi &gt; Planlama &gt; Yük oluşturma çalışma ekranı**'na gidin.
1. Şu adımlardan birini izleyin:

    - **Yük oluşturma stratejisi** alanında bir strateji seçin.
    - Bir yük oluşturma şablonu tanımladıysanız ve buna yük oluşturma stratejisini atadıysanız, Eylem bölmesinde **Şablonları yönet** sekmesinde **Şablonu Uygula**'yı seçin. Sonra, **Yük oluşturma şablonu uygula** iletişim kutusunda **Yük oluşturma şablonu adı** alanından bir şablon seçin.

1. **Yük şablonları sırası** hızlı sekmesinde, bir veya daha fazla [yük şablonu](load-template.md) seçin. Çalışma ekranı, burada belirtilen sıraya göre yükü bu tür konteynerlere sığdırmaya çalışır. Genellikle en küçük konteynerleri listenin en üstüne koymanız gerekir, böylece önce olası en düşük konteynerin seçildiğinden emin olursunuz.
1. Eylem Bölmesinde, **Yük öner**'i seçin.
1. Önerilen yükleri ve önerilen yük satırlarını gözden geçirin.
1. Eylem bölmesinde, **Önerilen yük satırları** hızlı sekmesindeki kaynak belge satırlarına dayalı yükler oluşturmak için **Yük oluştur**'u seçin.
1. **Yük oluşturma çalışma ekranı** sayfasını kapatın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]