---
title: Talep tahmini kurulumu
description: "Bu konu başlığı, talep tahmini için hazırlamak üzere gerçekleştirmeniz gereken kurulum görevlerini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f9b0930ac8d26f83be077fe0e6edf917e8fb0f58
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="demand-forecasting-setup"></a>Talep tahmini kurulumu

[!include[banner](../includes/banner.md)]


Bu konu başlığı, talep tahmini için hazırlamak üzere gerçekleştirmeniz gereken kurulum görevlerini açıklar.  

Kurulum görevleri, aşağıdaki veri ve parametreleri ayarlamayı içerir.

## <a name="item-allocation-key"></a>Madde dağıtım anahtarı
Talep tahmini, bir öğe ve boyutları için, yalnızca o öğe bir madde tahsisat anahtarının parçasıysa hesaplanır. Bu kural, büyük öğe sayılarını gruplamak için uygulanır, böylece talep tahminleri daha hızlı oluşturulabilir. Madde tahsisatı kilit yüzdesi, talep tahmini oluştururken yok sayılır. Tahminler yalnızca geçmiş veriler temel alınarak oluşturulur. 

Tahmin oluşturma sırasında madde tahsisat anahtarı kullanılıyorsa, bir madde ve boyutları sadece bir madde tahsisat anahtarının parçası olmalıdır. 

Bir madde tahsisat anahtarına bir stok tutma birimi (SKU) eklemek için, **Master planlama** &gt; **Kurulum** &gt; **Talep tahmini** &gt; **Madde tahsisat anahtarları** menüsüne gidin. Bir maddeyi bir tahsisat anahtarına atamak için **Maddeleri ata** sayfasını kullanın.

## <a name="intercompany-planning-groups"></a>Şirketlerarası planlama grupları
Talep tahmini, şirketler arası tahminler oluşturur. Microsoft Dynamics 365 for Operations'ta, birlikte planlanan şirketler bir şirketlerarası planlama grubu olarak gruplandırılır. Her şirket için talep tahmininde hangi madde tahsisat anahtarlarının düşünülmesi gerektiğini belirlemek için, **Master planlama** &gt; **Kurulum** &gt; **Şirketlerarası planlama grupları** menüsüne giderek bir madde tahsisat anahtarını şirketlerarası planlama grubu üyesi ile ilişkilendirin. 

Varsayılan olarak, şirketlerarası planlama grubu üyelerine hiçbir madde tahsisat anahtarı atanmamışsa, tüm Dynamics 365 for Operations şirketlerinden tüm madde tahsisat anahtarlarına atanan tüm maddeler için bir talep tahmini hesaplanır. Şirketler ve madde tahsisat anahtarları için ek filtreleme seçenekleri **İstatistik temel tahmin oluştur** sayfasında mevcuttur. 

Tahmin edilen maddelerin sayısını gözden geçirin. Microsoft Azure Machine Learning'i kullandığınızda, gereksiz maddeler artan maliyetlere yol açabilir.

## <a name="demand-forecasting-parameters"></a>Talep tahmin parametreleri
Talep tahmin parametrelerini ayarlamak için, **Master planlama** &gt; **Kurulum** &gt; **Talep tahmin parametreleri** menüsüne gidin. Talep tahmini şirketler arası gerçekleştirildiği için, ayar geneldir. Diğer bir deyişle, ayar tüm şirketler için geçerlidir. 

Talep tahmini, tahmini miktar cinsinden oluşturur. Bu yüzden, miktarın ifade edileceği ölçü birimi **Talep tahmin birimi** alanında belirtilmelidir. Ölçü birimi, toplam ve yüzde dağılımının anlamlı olmasını garantiye almak için benzersiz olmalıdır. Toplam ve yüzde dağılımı hakkında daha fazla bilgi için, bkz. [Temel tahmine manüel ayarlar yapma](manual-adjustments-baseline-forecast.md). Talep tahminine dahil edilen SKU'lar için kullanılan her ölçü birimi konusunda, ölçü birimi ve genel tahmin ölçü birimi için bir dönüştürme kuralı olduğundan emin olun. Tahmin oluşturma çalıştırıldığında, ölçü birimi dönüşümü olmayan öğelerin listesi kaydedilir, böylece ayarı kolayca düzeltebilirsiniz. 

Talep tahmini bağımlı ve bağımsız talebi tahmin etmek için kullanılabilir. Örneğin, yalnızca **Satış emri** onay kutusu seçiliyse ve talep tahmini için kabul edilen tüm öğeler satılan öğeler ise, sistem bağımsız talebi hesaplar. Ancak, kritik alt bileşenler madde tahsisat anahtarlarına eklenebilir ve talep tahminine eklenebilir. Bu durumda, **Üretim satırı** onay kutusu seçildiğinde, bağımlı bir tahmin hesaplanır. 

Dynamics 365 for Operations'ta bir temel tahmin oluşturmak için iki yöntem vardır. Geçmiş verilerin üstündeki tahmin modellerini kullanabilir veya sadece geçmiş verileri tahmine kopyalayabilirsiniz. **Tahmin oluşturma stratejisi** alanı bu iki yöntem arasında seçim yapmanıza olanak verir. Tahmin modellerini kullanmak için, **Azure Machine Learning** seçeneğini seçin. 

**Talep tahmini parametreleri** sayfasının sol bölmesinde **Tahmin boyutları** seçeneğine tıklayarak, talep tahmini oluşturulurken kullanılacak tahmin boyutları kümesini de seçebilirsiniz. Bir tahmin boyutu tahminin tanımlandığı ayrıntı düzeyini gösterir. Şirket, tesis ve madde tahsisat anahtarı zorunlu tahmin boyutlarıdır, ancak ayrıca depo, envanter durumu, müşteri grubu, müşteri hesabı, ülke/bölge, şehir ve öğe artı tüm öğe boyut seviyelerinde de tahminler oluşturabilirsiniz. 

Herhangi bir aşamada, talep tahmini için kullanılan boyutların listesine tahmin boyutlarını ekleyebilirsiniz. Ayrıca tahmin boyutlarını listeden kaldırabilirsiniz. Ancak, bir tahmin boyutu ekler veya kaldırırsanız, manüel ayarlar kaybolur. 

Tüm öğeler talep tahmini perspektifinden aynı şekilde davranmaz. Benzer öğeler bir madde tahsisat anahtarında gruplandırılabilir ve hareket türleri ile tahmin yöntem ayarları gibi parametreler her madde tahsisat anahtarı için ayarlanabilir. **Talep tahmin parametreleri** sayfasının sol bölmesindeki **Madde tahsisat anahtarları** öğesine tıklayın. 

Dynamics 365 for Operations, tahmin oluşturmak için bir Machine Learning ağ hizmeti kullanır. Hizmete bağlanmak için, Microsoft Azure Machine Learning Studio'da oturum açarsanız, Dynamics 365 for Operations'a aşağıdaki bilgileri sağlamanız gerekir:

-   Ağ hizmeti uygulama programlama arabirimi (API) anahtarı
-   Ağ hizmeti sonlanım noktası URL'si
-   Azure depolama hesap adı
-   Azure depolama hesap anahtarı

**Not:** Sadece özel bir depolama hesabı kullanıyorsanız Azure depolama hesap adı ve anahtarı gerekir. Şirket içi sürümünü kullanıyorsanız, Makine Öğrenimi hizmetinin geçmiş verilere ulaşabilmesi için Azure üzerinde özel bir depolama hesabınızın olması gerekir. 

Talep tahminleri oluşturmak için, Machine Learning Studio veya Dynamics 365 for Operations Talep tahmin deneylerini kullanarak kendi hizmetinizi uygulayabilirsiniz. Dynamics 365 for Operations talep tahmin deneylerini bir ağ hizmeti olarak kullanma talimatları Dynamics 365 for Operations'ta mevcuttur. **Talep tahmin parametreleri** sayfasında, **Azure Machine Learning** öğesine tıklayın.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Dynamics 365 for Operations talep tahmini makine öğrenimi hizmeti için ayarlar
Dynamics 365 for Operations talep tahmini hizmeti için yapılandırılabilecek parametreleri görmek için, **Master planlama** &gt; **Kurulum** &gt; **Talep tahmini** &gt; **Tahmin algoritma parametreleri** konumuna gidin. **Tahmin algoritma parametreleri** sayfası, parametreler için varsayılan değerleri gösterir. Bu parametrelerin üzerine **Talep tahmini parametreleri** sayfasında yazabilirsiniz. Genel olarak parametrelerin üzerine yazmak için **Genel** öğesini kullanın veya her bir madde tahsisat anahtarı için parametrelerin üzerine yazmak istiyorsanız **Madde tahsisat anahtarları** öğesini kullanın. Bir madde tahsisat anahtarı için üzerine yazılan parametreler sadece o madde tahsisat anahtarı ile ilişkilendirilen öğelerin tahminini etkiler.

<a name="see-also"></a>Ayrıca bkz.
--------

[Talep tahminine giriş](introduction-demand-forecasting.md)

[İstatistik temel tahmin oluşturma](generate-statistical-baseline-forecast.md)

[Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)




