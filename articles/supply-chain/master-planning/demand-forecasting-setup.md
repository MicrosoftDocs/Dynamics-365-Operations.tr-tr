---
title: Talep tahmini kurulumu
description: Bu konu başlığı, talep tahmini için hazırlamak üzere gerçekleştirmeniz gereken kurulum görevlerini açıklar.
author: roxanadiaconu
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81fec20130a1621d4cb55394db75a7ac0a16fdf3
ms.sourcegitcommit: 4fbf031319109660c0462a800f85848571eb040d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2021
ms.locfileid: "7471347"
---
# <a name="demand-forecasting-setup"></a>Talep tahmini kurulumu

[!include [banner](../includes/banner.md)]

Bu konu başlığı, talep tahmini için hazırlamak üzere gerçekleştirmeniz gereken kurulum görevlerini açıklar.  

Kurulum görevleri, aşağıdaki veri ve parametreleri ayarlamayı içerir.

## <a name="item-allocation-keys"></a>Madde dağıtım anahtarları

Talep tahmini, bir öğe ve boyutları için, yalnızca o öğe bir madde tahsisat anahtarının parçasıysa hesaplanır. Bu kural, büyük öğe sayılarını gruplamak için uygulanır, böylece talep tahminleri daha hızlı oluşturulabilir. Madde tahsisatı kilit yüzdesi, talep tahmini oluştururken yok sayılır. Tahminler yalnızca geçmiş veriler temel alınarak oluşturulur.

Tahmin oluşturma sırasında madde tahsisat anahtarı kullanılıyorsa, bir madde ve boyutları sadece bir madde tahsisat anahtarının parçası olmalıdır.

Madde tahsisat anahtarına bir stok tutma birimi (SKU) eklemek için **Master planlama \> Kurulum \> Talep tahmini \> Madde tahsisat anahtarları** menüsüne gidin. Bir maddeyi bir tahsisat anahtarına atamak için **Maddeleri ata** sayfasını kullanın.

## <a name="intercompany-planning-groups"></a>Şirketlerarası planlama grupları

Talep tahmini, şirketler arası tahminler oluşturur. Dynamics 365 Supply Chain Management'ta, birlikte planlanan şirketler bir şirketlerarası planlama grubu olarak gruplandırılır. Her şirket için talep tahmininde hangi madde tahsisat anahtarlarının düşünülmesi gerektiğini belirlemek için **Master planlama \> Kurulum \> Şirketlerarası planlama grupları** menüsüne giderek bir madde tahsisat anahtarını şirketlerarası planlama grubu üyesiyle ilişkilendirin.

Varsayılan olarak, şirketlerarası planlama grubu üyelerine hiçbir madde tahsisat anahtarı atanmamışsa, tüm şirketlerden tüm madde tahsisat anahtarlarına atanan tüm maddeler için bir talep tahmini hesaplanır. Şirketler ve madde tahsisat anahtarları için ek filtreleme seçenekleri **İstatistik temel tahmin oluştur** sayfasında mevcuttur.

Tahmin edilen maddelerin sayısını gözden geçirin. Microsoft Azure Machine Learning'i kullandığınızda, gereksiz maddeler artan maliyetlere yol açabilir.

## <a name="demand-forecasting-parameters"></a>Talep tahmin parametreleri

Talep tahmin parametrelerini ayarlamak için **Master planlama \> Kurulum \> \> Talep tahmini \> Talep tahmin parametreleri** menüsüne gidin. Talep tahmini şirketler arası gerçekleştirildiği için, ayar geneldir. Bu, kurulumun tüm şirketler için geçerli olduğu anlamına gelir.

Talep tahmini, tahmini miktar cinsinden oluşturur. Bu yüzden, miktarın ifade edileceği ölçü birimi **Talep tahmin birimi** alanında belirtilmelidir. Ölçü birimi, toplam ve yüzde dağılımının anlamlı olmasını sağlamak için benzersiz olmalıdır. Toplam ve yüzde dağılımı hakkında daha fazla bilgi için bkz. [Temel tahmine manüel ayarlar yapma](manual-adjustments-baseline-forecast.md). Talep tahminine dahil edilen SKU'lar için kullanılan her ölçü birimi konusunda, ölçü birimi ve genel tahmin ölçü birimi için bir dönüştürme kuralı olduğundan emin olun. Tahmin oluşturma çalıştırıldığında, ölçü birimi dönüşümü olmayan öğelerin listesi kaydedilir, böylece ayarı kolayca düzeltebilirsiniz.

Talep tahmini bağımlı ve bağımsız talebi tahmin etmek için kullanılabilir. Örneğin, yalnızca **Satış siparişi** onay kutusu seçiliyse ve talep tahmini için kabul edilen tüm öğeler satılan öğeler ise, sistem bağımsız talebi hesaplar. Ancak, kritik alt bileşenler madde tahsisat anahtarlarına eklenebilir ve talep tahminine eklenebilir. Bu durumda, **Üretim satırı** onay kutusu seçildiğinde, bağımlı bir tahmin hesaplanır.

Temel tahmin oluşturmak için iki yöntem vardır. Geçmiş verilerin üstündeki tahmin modellerini kullanabilir veya sadece geçmiş verileri tahmine kopyalayabilirsiniz. **Tahmin oluşturma stratejisi** alanı bu iki yöntem arasında seçim yapmanıza olanak verir. Tahmin modellerini kullanmak için, **Azure Machine Learning** seçeneğini seçin.

**Talep tahmin parametreleri** sayfasının sol bölmesinde **Tahmin boyutları**'nı seçerek talep tahmini oluşturulurken kullanılacak tahmin boyutları kümesini de seçebilirsiniz. Bir tahmin boyutu tahminin tanımlandığı ayrıntı düzeyini gösterir. Şirket, tesis ve madde tahsisat anahtarı gerekli tahmin boyutlarıdır ancak depo, stok durumu, müşteri grubu, müşteri hesabı, ülke/bölge, şehir ve madde artı tüm madde boyutu düzeylerinde de tahminler oluşturabilirsiniz.

Herhangi bir aşamada, talep tahmini için kullanılan boyutların listesine tahmin boyutlarını ekleyebilirsiniz. Ayrıca tahmin boyutlarını listeden kaldırabilirsiniz. Ancak, bir tahmin boyutu ekler veya kaldırırsanız, manüel ayarlar kaybolur.

Talep tahmini perspektifinden bakıldığında tüm maddeler aynı şekilde performans göstermez. Benzer öğeler bir madde tahsisat anahtarında gruplandırılabilir ve hareket türleri ile tahmin yöntem ayarları gibi parametreler her madde tahsisat anahtarı için ayarlanabilir. **Talep tahmin parametreleri** sayfasının sol bölmesindeki **Madde tahsisat anahtarları**'nı seçin.

Supply Chain Management, tahmin oluşturmak için bir Machine Learning web hizmeti kullanır. Hizmete bağlanmak için, Microsoft Azure Machine Learning Studio'da (klasik) oturum açarsanız, aşağıdaki bilgileri sağlamanız gerekir:

- Ağ hizmeti uygulama programlama arabirimi (API) anahtarı
- Ağ hizmeti sonlanım noktası URL'si
- Azure depolama hesap adı
- Azure depolama hesap anahtarı

> [!NOTE]
> Yalnızca özel bir depolama hesabı kullanıyorsanız Azure depolama hesap adı ve anahtarı gerekir. Şirket içi sürümünü kullanıyorsanız, Makine Öğrenimi hizmetinin geçmiş verilere ulaşabilmesi için Azure üzerinde özel bir depolama hesabınızın olması gerekir.

Talep tahminleri oluşturmak için, Machine Learning Studio veya Supply Chain Management Talep tahmini deneylerini kullanarak kendi hizmetinizi uygulayabilirsiniz. Talep tahmin deneylerini bir ağ hizmeti olarak kullanma talimatları Supply Chain Management'ta mevcuttur. **Talep tahmin parametreleri** sayfasında, **Azure Machine Learning** sekmesini açın.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Talep tahmini makine öğrenimi hizmeti için ayarlar

Talep tahmini hizmeti için yapılandırılabilecek parametreleri görmek üzere **Master planlama \> Kurulum \> Talep tahmini \> Tahmin algoritma parametreleri**'ne gidin. **Tahmin algoritma varsayılan parametreleri** sayfası, parametreler için varsayılan değerleri gösterir. Aşağıdakileri yapabileceğiniz **Master Planlama \> Kurulum \> Talep tahmini \> Talep tahmin parametreleri**'ne giderek bu parametrelerin üzerine yazabilirsiniz:

- Genel olarak parametrelerin üzerine yazmak için **Genel** sekmesini kullanın.
- Her bir madde tahsisat anahtarı için parametrelerin üzerine yazmak istiyorsanız **Madde tahsisat anahtarları** sekmesini kullanın. Bir madde tahsisat anahtarı için üzerine yazılan parametreler sadece o madde tahsisat anahtarı ile ilişkilendirilen öğelerin tahminini etkiler.

### <a name="forecast-algorithm-parameters"></a>Tahmin algoritma parametreleri

**Talep tahmin parametreleri** sayfasının **Madde tahsisat anahtarları** sekmesinde, soldaki ızgarada seçili olan madde tahsisat anahtarı için tahmin algoritma parametreleri atamak üzere **Tahmin algoritma parametreleri** hızlı sekmesini kullanabilirsiniz. Gerekli parametre koleksiyonunu oluşturmak için araç çubuğundaki **Ekle** ve **Kaldır** düğmelerini kullanın. Listedeki her parametre için **Ad** alanında aşağıdaki değerlerden birini seçin ve ardından **Değer** alanına uygun bir değer girin:

- **Güven düzeyi yüzdesi**: Güven aralığı, talep tahmini için iyi tahminler görevi gören bir değer aralığıdır. Yüzde 95'lik bir güven düzeyi yüzdesi, gelecekteki talep tahmininin güven aralığı sınırlarının dışına çıkma konusunda yüzde 5'lik bir risk bulunduğunu gösterir.
- **Mevsimselliği zorla**: Modelin belirli bir mevsimsellik türü kullanması için zorlanıp zorlanmayacağını belirtir. Bu yalnızca ARIMA ve ETS için geçerlidir. Seçenekler: OTOMATIK (varsayılan), YOK, TOPLAMSAL, ÇARPIMSAL.
- **Tahmin modeli**: Seçenekler: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALL. En uygun modeli seçmek için **TÜMÜ** seçeneğini kullanın.
- **Maksimum tahmin edilen değer**: Tahminler için kullanılacak maksimum değeri belirtir. Biçim: +1E[n] veya sayısal sabit değer.
- **Minimum tahmin edilen değer**: Tahminler için kullanılacak minimum değeri belirtir. Biçim: -1E[n] veya sayısal sabit değer.
- **Eksik değer değiştirme**: Geçmiş verilerindeki boşlukların nasıl doldurulacağını belirtir. Seçenekler: sayısal değer, ORTALAMA, ÖNCEKİ, DOĞRUSAL İLİŞKİLENDİR, POLİNOM İLİŞKİLENDİR.
- **Eksik değer değiştirme kapsamı**: Değer değiştirmenin yalnızca her bir ayrıntı düzeyi özniteliğinin tarih aralığına mı yoksa tüm veri kümesine mi uygulanacağını belirtir. Sistemin geçmiş verilerdeki boşlukları doldururken kullandığı tarih aralığını belirlemek için aşağıdaki seçenekler kullanılabilir:

  - GLOBAL: Sistem, tüm ayrıntı düzeyi özniteliklerinin tam tarih aralığını kullanır.
  - HISTORY_DATE_RANGE: Sistem, **İstatistik temel tahmini oluştur** iletişim kutusundaki **Geçmiş dönem** alan grubundaki **Başlangıç tarihi** ve **Bitiş tarihi** alanları tarafından tanımlanan belirli bir tarih aralığını kullanır.
  - GRANULARITY_ATTRIBUTE: Sistem, şu anda işlenen ayrıntı düzeyi özniteliğinin tarih aralığını kullanır.

  > [!NOTE]
  > Ayrıntı düzeyi özniteliği, tahminin yapıldığı tahmin boyutlarının bir birleşimidir. **Talep tahmin parametreleri** sayfasında tahmin boyutlarını tanımlayabilirsiniz.

- **Mevsimsellikle ilgili ipucu**: Mevsimsel veriler için tahmin doğruluğunu iyileştirmek amacıyla tahmin modeline bir ipucu sağlar. Biçim: bir talep deseninin kendisini tekrarlayacağı demet sayısını temsil eden tamsayı. Örneğin, her 6 ayda bir yinelenen veriler için "6" girin.
- **Test kümesi boyut yüzdesi**: Tahmin doğruluğu hesaplamada test kümesi olarak kullanılacak geçmiş verilerin yüzdesi.

## <a name="additional-resources"></a>Ek kaynaklar

- [Talep tahminine genel bakış](introduction-demand-forecasting.md)
- [İstatistik temel tahmini oluşturma](generate-statistical-baseline-forecast.md)
- [Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
