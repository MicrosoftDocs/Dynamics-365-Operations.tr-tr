---
title: Talep tahmini kurulumu
description: "Bu konu başlığı, talep tahmini için hazırlamak üzere gerçekleştirmeniz gereken kurulum görevlerini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Talep tahmini kurulumu

Bu konu başlığı, talep tahmini için hazırlamak üzere gerçekleştirmeniz gereken kurulum görevlerini açıklar.  

Kurulum görevleri, aşağıdaki veri ve parametreleri ayarlamayı içerir.

## <a name="item-allocation-key"></a>Madde dağıtım anahtarı
Talep tahmini, bir öğe ve boyutları için, yalnızca o öğe bir madde tahsisat anahtarının parçasıysa hesaplanır. Böylece talep tahminleri daha hızlı bir şekilde oluşturulabilir Grup çok sayıda öğe için bu kural uygulanır. Talep tahminleri yaratılırken madde tahsisat anahtarı yüzdesi yok sayılır. Tahminler yalnızca geçmiş veriler temel alınarak oluşturulur. 

Tahmin oluşturma sırasında madde tahsisat anahtarı kullanılıyorsa, bir madde ve boyutları sadece bir madde tahsisat anahtarının parçası olmalıdır. 

Bir madde tahsisat anahtarı için bir stok tutma birimi (STB) eklemek için Git **Master planlama**&gt;**Kurulum**&gt;**talep tahmin**&gt;**madde tahsisat anahtarları**. Bir maddeyi bir tahsisat anahtarına atamak için **Maddeleri ata** sayfasını kullanın.

## <a name="intercompany-planning-groups"></a>Şirketlerarası planlama grupları
Talep tahmini, şirketler arası tahminler oluşturur. İşlemler için Microsoft Dynamics 365 içinde birlikte planlanan şirketler bir şirketlerarası planlama Grup gruplandırılır. , Hangi madde tahsisat anahtarları sayılacağı Talep tahmini için şirket bazında belirtmek için bir madde tahsisat anahtarı giderek grup üyesi planlama şirketlerarası ilişkilendirmek **Master planlama**&gt;**Kurulum**&gt;**şirketlerarası planlama grupları**. 

Hiçbir madde tahsisat anahtarları şirketlerarası planlama Grup üyelerinin, atanmış olan, varsayılan olarak, tüm madde tahsisat anahtarları için tüm Dynamics 365 işlemleri şirketler için atanmış olan tüm öğeler için bir talep tahmin hesaplanır. Şirketler ve madde tahsisat anahtarları için ek filtreleme seçenekleri **İstatistik temel tahmin oluştur** sayfasında mevcuttur. 

Tahmin edilen maddelerin sayısını gözden geçirin. Microsoft Azure Machine Learning'i kullandığınızda, gereksiz maddeler artan maliyetlere yol açabilir.

## <a name="demand-forecasting-parameters"></a>Talep tahmin parametreleri
İsteğe bağlı parametreleri tahmini ayarlamak için Git **Master planlama**&gt;**Kurulum**&gt;**isteğe bağlı parametreleri tahmin**. Talep tahmini şirketler arası gerçekleştirildiği için, ayar geneldir. Diğer bir deyişle, ayar tüm şirketler için geçerlidir. 

Talep tahmini, tahmini miktar cinsinden oluşturur. Bu yüzden, miktarın ifade edileceği ölçü birimi **Talep tahmin birimi** alanında belirtilmelidir. Ölçü birimi, toplam ve yüzde dağılımının anlamlı olmasını garantiye almak için benzersiz olmalıdır. Toplam ve yüzde dağılımı hakkında daha fazla bilgi için, bkz. [Temel tahmine manüel ayarlar yapma](manual-adjustments-baseline-forecast.md). Talep tahminine dahil edilen SKU'lar için kullanılan her ölçü birimi konusunda, ölçü birimi ve genel tahmin ölçü birimi için bir dönüştürme kuralı olduğundan emin olun. Tahmin oluşturma çalıştırıldığında, ölçü birimi dönüşümü olmayan öğelerin listesi kaydedilir, böylece ayarı kolayca düzeltebilirsiniz. 

Talep tahmini bağımlı ve bağımsız talebi tahmin etmek için kullanılabilir. Örneğin, yalnızca **Satış emri** onay kutusu seçiliyse ve talep tahmini için kabul edilen tüm öğeler satılan öğeler ise, sistem bağımsız talebi hesaplar. Ancak, kritik alt bileşenler madde tahsisat anahtarlarına eklenebilir ve talep tahminine eklenebilir. Bu durumda, **Üretim satırı** onay kutusu seçildiğinde, bağımlı bir tahmin hesaplanır. 

Temel işlemleri için Dynamics 365, tahmin oluşturmak için iki yöntem vardır. Geçmiş verilerin üstündeki tahmin modellerini kullanabilir veya sadece geçmiş verileri tahmine kopyalayabilirsiniz. **Tahmin oluşturma stratejisi** alanı bu iki yöntem arasında seçim yapmanıza olanak verir. Tahmin modellerini kullanmak için, **Azure Machine Learning** seçeneğini seçin. 

**Talep tahmini parametreleri** sayfasının sol bölmesinde **Tahmin boyutları** seçeneğine tıklayarak, talep tahmini oluşturulurken kullanılacak tahmin boyutları kümesini de seçebilirsiniz. Bir tahmin boyutu tahminin tanımlandığı ayrıntı düzeyini gösterir. Şirket, tesis ve madde tahsisat anahtarı zorunlu tahmin boyutlarıdır, ancak ayrıca depo, envanter durumu, müşteri grubu, müşteri hesabı, ülke/bölge, şehir ve öğe artı tüm öğe boyut seviyelerinde de tahminler oluşturabilirsiniz. 

Herhangi bir aşamada, talep tahmini için kullanılan boyutların listesine tahmin boyutlarını ekleyebilirsiniz. Ayrıca tahmin boyutlarını listeden kaldırabilirsiniz. Ancak, bir tahmin boyutu ekler veya kaldırırsanız, manüel ayarlar kaybolur. 

Tüm öğeler talep tahmini perspektifinden aynı şekilde davranmaz. Benzer öğeler bir madde tahsisat anahtarında gruplandırılabilir ve hareket türleri ile tahmin yöntem ayarları gibi parametreler her madde tahsisat anahtarı için ayarlanabilir. **Talep tahmin parametreleri** sayfasının sol bölmesindeki **Madde tahsisat anahtarları** öğesine tıklayın. 

Tahmin oluşturmak için bir makine öğrenme web hizmet işlemleri için Dynamics 365 kullanır. Microsoft Azure makine öğrenme Studio oturum hizmetine bağlanmak için Dynamics 365 işlemleri için aşağıdaki bilgileri sağlamalısınız:

-   Ağ hizmeti uygulama programlama arabirimi (API) anahtarı
-   Ağ hizmeti sonlanım noktası URL'si
-   Azure depolama hesap adı
-   Azure depolama hesap anahtarı

**Not:** Sadece özel bir depolama hesabı kullanıyorsanız Azure depolama hesap adı ve anahtarı gerekir. Şirket içi sürüm dağıtırsanız, makine öğrenme hizmeti geçmiş verilerini erişebilmesi için Azure, özel depolama hesabında olmalıdır. 

İsteğe bağlı Öngörüler oluşturmak için kendi servis işlemleri Talep tahmini deneyler makine öğrenme Studio veya Dynamics 365 kullanarak dağıtabilirsiniz. İşlemler için kullanılabilir Dynamics 365 deneyler bir web hizmeti olarak tahmin işlemlerinin talep için Dynamics 365 dağıtma yönergeleri verilmiştir. **Demand forecasting parameters** sayfasında, **Azure Machine Learning** öğesine tıklayın.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Tahmin makine öğrenme hizmeti ayarlarını Dynamics 365 işlemleri için talep
Tahmin hizmet işlemleri talep için Dynamics 365 için yapılandırılabilir parametreleri görüntülemek için Git **Master planlama**&gt;**Kurulum**&gt;**talep tahmin**&gt;**algoritma parametreleri tahmin**. **Algoritma parametreleri tahmin** sayfa parametreler için varsayılan değerleri gösterir. Bu parametreler üzerine yazabilir **isteğe bağlı parametreleri tahmin** sayfa. Genel olarak parametrelerin üzerine yazmak için **Genel** öğesini kullanın veya her bir madde tahsisat anahtarı için parametrelerin üzerine yazmak istiyorsanız **Madde tahsisat anahtarları** öğesini kullanın. Bir madde tahsisat anahtarı için üzerine yazılan parametreler sadece o madde tahsisat anahtarı ile ilişkilendirilen öğelerin tahminini etkiler.

<a name="see-also"></a>Ayrıca bkz.
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


