---
title: En iyi duruma getirme danışmanına genel bakış
description: Bu konuda Finance and Operations'ın optimum yapılandırmasını sağlamaya yardımcı olacak En İyi Duruma Getirme danışmanını nasıl kullanabileceğiniz açıklanmaktadır.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 1e53dbae2d139af554b1918102937f8c3579f64a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682549"
---
# <a name="optimization-advisor-overview"></a>En iyi duruma getirme danışmanına genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda Finance and Operations'ın optimum yapılandırmasını sağlamaya yardımcı olacak En İyi Duruma Getirme danışmanını nasıl kullanabileceğiniz açıklanmaktadır.

## <a name="overview"></a>Genel bakış

Bir modülün hatalı yapılandırılması ve ayarlanması, uygulama özelliklerinin kullanılmasını, sistem performansını ve iş süreçlerinin sorunsuz işlemesini olumsuz etkileyebilir. İş verilerinin kalitesi (örneğin doğruluk, tamlık ve verilerin açıklığı) de sistem performansını ve kuruluşun karar verme yeteneklerini, verimliliğini etkiler.

**En iyi duruma getirme danışmanı** çalışma alanı yetkili kullanıcılara, iş analistlerine, işlev danışmanlarına ve BT destek görevlilerine modül yapılandırmasındaki ve iş verilerindeki sorunları tanımlama olanağı sunar. En iyi duruma getirme danışmanı modülü yapılandırması için en iyi yöntemleri önerir ve eski veya yanlış iş verilerini tanımlar.

En iyi duruma getirme danışmanı düzenli aralıklarla en iyi uygulama kuralları kümesi çalıştırır. Varsayılan kurallar kümesi mevcuttur ancak kullanıcılar kendi özelleştirmelerine, bağımsız yazılım satıcılarından (ISV) aldıkları çözümlere ve iş verilerine özel kurallar da oluşturabilirler. Kural oluşturmayla ilgili daha fazla bilgi için bkz. [En iyi duruma getirme danışmanı için kurallar oluşturma](./create-rules-optimization-advisor.md).

Bir kural ihlali tespit edildiğinde, en iyi duruma getirme fırsatı oluşturulur ve **En iyi duruma getirme danışmanı** çalışma alanında görüntülenir. Bir kullanıcı doğrudan **En iyi duruma getirme danışmanı** çalışma alanından uygun düzeltici eylemi gerçekleştirebilir.

Fırsatlar, kurulumun türüne ve doğrulanan verilere bağlı olarak şirkete özel veya şirketler arası olabilir. Şirketler arası fırsatlar tüm şirketler tarafından görüntülenebilir. Belirli bir şirkete yönelik fırsatları görüntülemek için önce şirketi seçmeniz gerekir.

En iyi duruma getirme fırsatlarına standart güvenlik ilkeleri uygulanır. Örneğin, **Ambar yönetimi** modülüy yapılandırmasıyla ilişkili için en iyi duruma getirme fırsatları yalnızca Ambar yönetimine erişimi olan ve ayarını değiştirebilecek kullanıcılar tarafından görülebilir.

Bazı en iyi durumu getirme fırsatlarıyla ilgili eylem gerçekleştirdiğinizde, sistem iş süreçlerinin çalışma zamanında azalma açısından fırsatın etkisini hesaplar. Ne yazık ki, bu özellik tüm en iyi duruma getirme iş fırsatları için kullanılamaz.

İyileştirme danışmanı hakkında daha fazla bilgi almak için kısa [Dynamics 365 for Finance and Operations içindeki İyileştirme danışmanı](https://www.youtube.com/watch?v=MRsAzgFCUSQ) videosunu izleyin.

## <a name="optimization-rules"></a>En iyi duruma getirme kuralları

En iyi duruma getirme danışmanı kurallarının tam listesini ve kuralların ne sıklıkta değerlendirildiğini görmek için **Sistem yönetimi** &gt; **Periyodik görevleri** &gt; **Tanılama doğrulaması kuralını koru** öğesine gidin. Yalnızca **Etkin** durumunda olan kurallar değerlendirilir. Değerlendirme sıklığı **Günlük**, **Haftalık**, **Aylık** veya **Planlanmadı** olarak ayarlanabilir.

Planlanmamış kuralların değerlendirilmesini tetiklemek veya periyodik kuralları önceden tanımlanan plan dışında yeniden değerlendirmek için **Sistem yönetimi** &gt; **Periyodik görevler** &gt; **Tanılama doğrulaması kuralını planla** öğesine gidin. Sonra, **Tanılama kuralı doğrulaması** iletişim kutusunda, bir değerlendirme sıklığı seçin. Belirtilen sıklık değerine sahip tüm kurallar yeniden değerlendirilir.

Geçerli en iyi duruma getirme kural kümesi aşağıdaki kategorilere ayrılabilir.

### <a name="module-configuration-and-setup"></a>Modül yapılandırması ve ayarı

Ambar yönetimi kurulumu karmaşık bir işlemdir. İşlemi kolaylaştırmak için bazı kurallar kurulumun doğrulunu doğrulamaya yardımcı olmak amacıyla sunulmuştur. Örneğin, bir kural satış siparişleri ve transfer emirleri için sabit ürün çeşidi yerleşimlerine ilişkin ambar yerleşim yönergelerinin kurulumunu doğrular.

Ayrıca, bazı kurallar etkinleştirilen özelliklerin gerçekten kullanılıp kullanılmadığını denetler. Örneğin, bir kural **Master planlama** modülünü kullanıp kullanmadığınızı belirler. Kural modülü kullanmadığınızı belirlerse, planlama işlemlerini devre dışı bırakmanızı önermek için bir en iyi duruma getirme fırsatı oluşturulur.

### <a name="system-configuration"></a>Sistem yapılandırması

Bir yapılandırma anahtarı tarafından kontrol edilen belirli bir işlevin kullanılmıyor olması durumunda, yapılandırma anahtarını devre dışı bırakmanızı öneren bir en iyi duruma getirme fırsatı oluşturulur. Yapılandırma anahtarı örnekleri arasında **Fiili ağırlık**, **Bütçe planlama**, **Proje** ve **Onaylanan satıcı listesi** bulunur.

### <a name="business-data-consistency-and-cleanup"></a>İş verileri tutarlılığı ve temizleme

Ana veriler doğru değilse (örneğin, tanımlanmamış birimler için ölçü birimi dönüştürmeleriniz varsa veya 0 \[sıfır\] ile bölünen ölçü birimi dönüştürmeleriniz varsa), verileri düzeltmenizi öneren bir en iyi duruma getirme fırsatı oluşturulur. 

Çok fala toplu işlem iş geçmişi girişiniz, geçersiz maddeleriniz, ambarda etkinleştirilmiş maddeler için kapatılmış eldeki stok girişleriniz varsa veya bu girişler ve maddeler çok eskiyse, verileri temizlemenizi öneren bir en iyi duruma getirme fırsatı oluşturulur. Verilerinizi temiz tutarak, tüm sistem performansının artırılmasına yardımcı olabilirsiniz.

### <a name="best-practices"></a>Önerilen yöntemler

Bazı iş süreçlerini en iyi uygulamalara uygun şekilde çalıştırmıyorsanız (örneğin, stok ön kapamasını stok kapatılmadan önce çalıştırıyor veya planlanan toplu işi yardımcı defter toplu iş transferi için kullanıyorsanız), en iyi duruma getirme fırsatları en iyi uygulama hakkında sizi bilgilendirir ve buna uymanızı ister.

## <a name="optimization-opportunities"></a>En iyi duruma getirme fırsatları

En iyi duruma getirme kurallarının değerlendirilmesi sırasında oluşturulan en iyi duruma getirme fırsatlarını görüntülemek için **En iyi duruma getirme danışmanı** çalışma alanını açın.

Bu çalışma alanında, **Daha fazla bilgi**'yi seçerek bir fırsat hakkında daha fazla bilgiye ulaşabilirsiniz. Sistemin eylem gerçekleştirmesini ve kurulumu düzeltmesini, verileri temizlemesini, vb. isterseniz, (bu durumda karşılık gelen sayları sizin açmanız gerekmez) **Eylem gerçekleştir**'i seçin.

En iyi duruma getirme fırsatları için iş akışı yoktur. **Eylem gerçekleştir**'i seçtikten veya **Daha fazla bilgi** iletişim kutusunda verilen gezinme yolunu kullandıktan sonra, en iyi duruma getirme fırsatı listeden kaldırılır. Düzeltici eylem sorunu tam olarak çözmezse, fırsat kural değerlendirildiğinde yeniden oluşturulur.

Fırsat sizin rolünüze uygun değilse, **Listemde gizle**'yi seçebilirsiniz. Bu fırsatın arkasındaki kural daha sonra yeniden tetiklense bile fırsatı listenizde görmezsiniz.

Belirli kuralların değerlendirmesini devre dışı bırakmak için kural tarafından oluşturulan fırsatı seçin ve ardından **Analizi devre dışı bırak**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[En iyi duruma getirme danışmanı için kurallar oluşturma](./create-rules-optimization-advisor.md)

[Dynamics 365 for Finance and Operations içindeki İyileştirme danışmanı (Video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
