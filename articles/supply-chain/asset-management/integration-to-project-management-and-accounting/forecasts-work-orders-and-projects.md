---
title: Tahminler, iş emirleri ve projeler
description: Bu konu, Varlık yönetimindeki Proje yönetimi ve muhasebe modülüyle tahminler ve iş emri tümleştirmesini açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886828"
---
# <a name="forecasts-work-orders-and-projects"></a>Tahminler, iş emirleri ve projeler

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varlık Yönetiminde, **Proje yönetimi ve muhasebe** modülüyle tümleştirme, kullanıcıların bakım işi türü tahminlerinde ve iş emri işlerinde maliyetleri izlemesine izin vererek maliyet kontrolünü en iyi duruma getirmek için yapılır.

Bakım işi türü tahminlerini izlemek için iki ayar yapılmalıdır:

1. **Varlık yönetimi** > **Kurulum** > **Varlık yönetimi parametreleri** > **Varlık** bağlantısı > **Proje** hızlı sekmesi > **Bakım tahmini projesi** alanında bir proje seçin.

2. **Bakım iş türü varsayılanlarında** bir bakım işi türü varsayılan satırı oluşturduğunuzda, satır için otomatik olarak bir faaliyet numarası oluşturulur (**Varlık yönetimi** > **Kurulum** > **İşler** > **Bakım işi türü varsayılanları**).

Bakım işi türü tahminleri iki amaca hizmet eder: **Proje yönetimi ve muhasebe** modülündeki bakım işi türü tahminlerindeki maliyetleri izleyebilirsiniz. Ayrıca, bir iş emri işinde bir bakım işi türü seçtiğinizde, tahminler otomatik olarak bir iş emri iş projesine transfer edilir.

İş emri işlerinde maliyetleri izlemek için, önce iş emri projeleri ayarlamanız gerekir. Yordamın açıklaması için [İş emri projesi kurulumu](../setup-for-work-orders/work-order-project-setup.md) bölümüne bakın.

## <a name="work-order-job-projects"></a>İş emri işi projeleri

Bir iş emrinde iş emri işi oluşturduğunuzda iş emri projesi **Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumundaki** iş emirlerinin ana proje kurulumu tarafından belirlenir.

İş emri işi projeleri, aşağıdaki iş emri bilgilerinin bir birleşimi kullanılarak oluşturulur:

- İş emrinde seçilen iş emri türü 
- İş emri işindeki varlıkla ilgili işlem yapılacak yerleşim
- İş emri işindeki varlıkla ilgili varlık türü  
- İş emrinde ayarlanan Beklenen başlangıç ve bitiş zamanı  

Yukarıda belirtilen bilgilerin tümünün bir iş emrinde bulunmaması mümkündür. Bu nedenle, bir iş emri üst projesi için yapılan arama mevcut veri birleşimi kullanılarak ve iş emri verileriyle ilgili proje kodu seçilerek gerçekleştirilir.

Örnek: Aşağıdaki şekilde, "Kamyon Motoru" varlık türünün kurulumu, bu varlık türüyle oluşturulan her iş emri işinin "000186" Proje kodunun bir alt projesi olacağı anlamına gelir.

![Şekil 1](media/01-integration-to-pma.png)

İş emri işindeki proje kodunun ve ilgili faaliyet numarasının amacı **(Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm iş emirleri** > listeden iş emrini seçin > **Satır ayrıntıları** hızlı sekmesi > **Proje kodu** alanı ve **Faaliyet numarası** alanı), **Proje yönetimi ve muhasebe** modülünde iş emri işiyle ilgili maliyetleri ve iş emri işinde seçilen kıymetleri izlemektir. 

Aşağıdaki şekilde, iş emri projelerinin ve ilgili proje faaliyetlerinin grafik genel görünümünü görürsünüz.

![Şekil 2](media/02-integration-to-pma.png)

Bir iş emrinde yeni bir iş emri işi oluşturulduğunda, iş için otomatik olarak bir iş emri projesi oluşturulur. İş emri işiyle ilgili varlığın mali boyutları otomatik olarak iş emri projesine transfer edilir. İş emri işi için oluşturulan proje faaliyeti bakım işi türü, bakım işi türü varyantı ve ticaret ile ilgili bilgiler ile ilgilidir. Bu veriler örneğin bir iş emrinden bir satınalma siparişi oluşturursanız (bkz. [Tedarik](../work-orders/procurement.md)) veya zaman kaydı için **Proje yönetimi ve muhasebe** modülünü kullanıyorsanız yararlıdır.  

Varlık işlem yapılacak bir yerleşime yüklenmişse ve bu varlık daha sonra başka bir işlem yapılacak yerleşime yüklenmişse, yeni işlem yapılacak yerleşimle ilgili mali boyutlar varlıkta otomatik olarak güncelleştirilir. Ardından, varlık için bir iş emri işi oluşturduğunuzda, iş emri işi için iş emri projesi artık varlıkla ilgili olan mali boyutları otomatik olarak alır. Bu, işlem yapılacak yerleşimleri kullandığınızda, maliyetlerin herhangi bir zamanda yüklenmiş olduğu işlem yapılacak yerleşimlerde her zaman izlenebileceği anlamına gelir. Mali boyutların otomatik güncelleştirilmesi, proje denetleme ve raporlama maliyetlerinin eksiksiz olarak izlenebilmesini sağlar.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>İş emri projeleri, iş emri yaşam döngüsü durumları, proje aşamaları ve proje türleri

İş emri yaşam döngüsü durumlarının ve iş emirlerindeki ilgili proje aşamalarının doğru kullanımını sağlamak için **Proje yönetimi ve muhaseb** modülüyle ilişkili olarak bağımlılıkları göz önünde bulundurun:

- **Proje yönetimi ve muhasebe** modülünde, proje aşamaları **Proje yönetimi ve muhasebe parametrelerindeki** proje türlerinde ayarlanır.  
- **Proje yönetimi ve muhasebe parametrelerinde**, kullanacağınız tüm proje türleri için ilgili proje aşaması onay kutularını seçmeyi unutmayın. Aşağıdaki şekilde, "Zaman ve malzeme" ve "Dahili" proje türleri için beş aşama seçilmiştir: **Oluşturuldu** - **Tahmin edildi** - **Zamanlandı** - **İşlemde"** - **Tamamlandı**. Bu beş aşama hem dahili bakım hem de servis bakım işleri için geçerlidir.  
- **Varlık Yönetiminde** proje türleri **İş emri proje kurulumu** formu > **Proje grubu** bağlantısında ayarladığınız proje grupları tarafından tanımlanır.  
- **İş emri proje kurulumunda** oluşturduğunuz iş emirleri iş emirleri oluştururken kullanılır. Bir iş emri oluşturulduğunda, iş emri için otomatik olarak bir iş emri projesi oluşturulur.  
- İş emri yaşam döngüsü durumlarının her birinin ilgili proje aşaması olması gerekir.  
- Bir iş emri yaşam döngüsü durumuyla ilgili proje aşaması, iş emri projesinde tanımlanan proje grubu için etkin bir aşama olarak tanımlanmalıdır. İş emri projesi, bir iş emrinde otomatik olarak oluşturulur.  
- Yeni bir iş emri oluşturduğunuzda iş emri projesi otomatik tahsisatı **İş emri projesi kurulumundaki** (**Varlık yönetimi** > **Kurulum** > **İŞ emirleri** > **Proje kurulumu**) kurulumu temel alır.  

İş emri proje grupları, ilgili proje türleri, proje aşamaları ve iş emri yaşam döngüsü durumları arasındaki ilişkilendirmeler aşağıdaki şekilde gösterilmiştir.  

![Şekil 3](media/03-integration-to-pma.png)

![Şekil 4](media/04-integration-to-pma.png)

![Şekil 5](media/05-integration-to-pma.png)

İş emri projelerinin nasıl ayarlanacağı ile ilgili olarak [İş emri proje kurulumu](../setup-for-work-orders/work-order-project-setup.md), iş emri yaşam döngüsü durumlarının nasıl oluşturulacağıyla ilgili olarak [İş emri yaşam döngüsü durumları](../setup-for-work-orders/work-order-lifecycle-states.md) konularına bakın.

Aşağıdaki şekil **Proje yönetimi ve muhasebe** modülüyle tümleştirmeye olanak tanımak için **Varlık Yönetimi** modülünde oluşturulan çeşitli projelerin grafik genel görünümünü ve projelerin ilgili olduğu iş süreçlerini gösterir.

![Şekil 6](media/06-integration-to-pma.png)

