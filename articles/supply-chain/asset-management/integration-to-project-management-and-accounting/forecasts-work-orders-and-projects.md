---
title: Tahminler, iş emirleri ve projeler
description: Bu konu, Varlık yönetimindeki Proje yönetimi ve muhasebe modülüyle tahminler ve iş emri tümleştirmesini açıklamaktadır.
author: johanhoffmann
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b53dcf4e8796f808283b7bd5ea92b869ee0e59aac5359d74bcdc5de37ea7352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770348"
---
# <a name="forecasts-work-orders-and-projects"></a>Tahminler, iş emirleri ve projeler

[!include [banner](../../includes/banner.md)]

 

Varlık Yönetiminde, **Proje yönetimi ve muhasebe** modülüyle tümleştirme, kullanıcıların bakım işi türü tahminlerinde ve iş emri işlerinde maliyetleri izleyebilmesine izin vererek maliyet kontrolünü en iyi duruma getirmeye yardımcı olur.

Bakım işi türü tahminlerini izlemek için iki ayar gereklidir:

1. **Varlık Yönetimi** > **Kurulum** > **Varlık yönetimi parametreleri**'nde bir proje seçin ve ardından **Varlıklar** sekmesinde > **Proje** hızlı sekmesinde bulunan **Bakım tahmini projesi** alanında bir proje seçin.

2. **Bakım iş türü varsayılanları** sayfasında bir bakım işi türü varsayılan satırı oluşturduğunuzda, satır için otomatik olarak bir faaliyet numarası oluşturulur (**Varlık yönetimi** > **Kurulum** > **İşler** > **Bakım işi türü varsayılanları**).

Bakım işi türü tahminleri iki amaca hizmet eder: 

- **Proje yönetimi ve muhasebe** modülündeki bakım işi türü tahminlerinde maliyetleri izleyebilirsiniz. 
- Bir iş emri işinde bir bakım işi türü seçtiğinizde, tahminler otomatik olarak bir iş emri iş projesine transfer edilir.

İş emri işlerinde maliyetleri izlemek için, önce iş emri projeleri ayarlamanız gerekir. Daha fazla bilgi için bkz. [İş emri proje kurulumu](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>İş emri işi projeleri

Bir iş emrinde iş emri işi oluşturduğunuzda, iş emri projesi **İş emri proje kurulumu** sayfasındaki iş emirlerinin ana proje kurulumu tarafından belirlenir (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu**).

İş emri işi projeleri, aşağıdaki iş emri bilgilerinin bir birleşimi kullanılarak oluşturulur:

- İş emrinde seçilen iş emri türü 
- İş emri işindeki varlıkla ilgili işlem yapılacak yerleşim
- İş emri işindeki varlıkla ilgili olan varlık türü  
- İş emrinde ayarlanan beklenen başlangıç ve bitiş zamanı  

Bu bilgilerden bazıları bir iş emrinde bulunmayabilir. Bu nedenle, bir iş emri üst projesi için yapılan arama mevcut veri birleşimi kullanılarak ve iş emri verileriyle ilgili proje kodu seçilerek gerçekleştirilir.

Örneğin, aşağıdaki örnekte, **Kamyon Motoru** varlık türünün ayarlanma şekli nedeniyle,  **Kamyon Motoru** varlık türü ile oluşturulan her iş emri işi 000186 proje kodunun alt projesi olacaktır.

![Şekil 1.](media/01-integration-to-pma.png)

İş emri işindeki proje kodunun ve ilgili faaliyet numarasının amacı, iş emri işiyle ilgili maliyetleri ve bunun üzerinde seçilen varlığı **Proje yönetimi ve muhasebe** modülünde izlemektir. (Proje kodunu ve faaliyet numarasını görüntülemek için **Varlık yönetimi** > **Ortak** > **İş emirleri** > **Tüm iş emirleri** öğesini ve ardından iş emrini seçin. **Satır ayrıntıları** hızlı sekmesinde, **Proje kodu** alanı proje kodunu ve **Faaliyet numarası** alanı faaliyet numarasını gösterir.) Varlık Yönetiminde maliyet kontrolü ile ilgili daha fazla bilgi için bkz. [Maliyet ve tarih kontrolü](../controlling-and-reporting/cost-and-date-control.md).

Aşağıdaki örnekte, iş emri projelerinin ve ilgili proje faaliyetlerinin grafik genel görünümü gösterilmektedir.

![Şekil 2.](media/02-integration-to-pma.png)

Bir iş emrinde yeni bir iş emri işi oluşturulduğunda, iş için otomatik olarak bir iş emri projesi oluşturulur. İş emri işiyle ilgili olan varlığın mali boyutları otomatik olarak iş emri projesine transfer edilir.

İş emri işinde oluşturulan proje faaliyetine ilgili bilgiler eklenir. Bu bilgiler bakım işi türü, bakım iş türü varyantı ve zanaat ile ilgilidir. Bunlar, örneğin bir iş emrinden bir satınalma siparişi oluşturursanız (bkz. [Tedarik](../work-orders/procurement.md)) veya zaman kaydı için **Proje yönetimi ve muhasebe** modülünü kullanıyorsanız yararlıdır.

Varlık işlem yapılacak bir yerleşime yüklenmişse ancak daha sonra başka bir işlem yapılacak yerleşime yüklenmişse, yeni işlem yapılacak yerleşimle ilgili mali boyutlar varlıkta otomatik olarak güncelleştirilir. Ardından, varlık için bir iş emri işi oluşturduğunuzda, iş emri işi için iş emri projesi artık varlıkla ilgili olan mali boyutları otomatik olarak alır. Bu nedenle, işlem yapılacak yerleşimleri kullandığınızda, maliyetler herhangi bir zamanda yüklenmiş olduğu işlem yapılacak yerleşimlerde her zaman izlenebilir. Mali boyutların otomatik güncelleştirilmesi, proje denetleme ve raporlama maliyetlerinin eksiksiz olarak izlenebilmesini sağlamaya yardımcı olur.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>İş emri projeleri, iş emri yaşam döngüsü durumları, proje aşamaları ve proje türleri

İş emri yaşam döngüsü durumlarının ve iş emirlerindeki ilgili proje aşamalarının doğru şekilde kullanılmasını sağlamaya yardımcı olmak için **Proje yönetimi ve muhasebe** modülüyle ilişkili olarak bağımlılıkları göz önünde bulundurun:

- **Proje yönetimi ve muhasebe** modülünde, proje aşamaları **Proje yönetimi ve muhasebe parametreleri** sayfasındaki proje türlerinde ayarlanır.  
- **Proje yönetimi ve muhasebe parametrelerinde** sayfasında, kullanacağınız tüm proje türleri için ilgili proje aşamalarını seçmek için onay kutularını kullanın. Aşağıdaki örneklerde, **Zaman ve malzeme** ve **Dahili** proje türleri için beş aşama seçilmiştir: (**Oluşturuldu**, **Tahmin edildi**, **Zamanlandı**, **İşlemde** ve **Tamamlandı**). Bu beş aşama hem dahili bakım işleri hem de servis bakım işleri için geçerlidir.
- **Varlık Yönetimi** modülünde, proje türleri **İş emri proje kurulumu** sayfası > **Proje grubu** sekmesinde ayarlanan proje grupları tarafından tanımlanır (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu**).  
- **İş emri proje kurulumu** sayfasında ayarlanan proje grupları iş emirleri oluştururken kullanılır. Bir iş emri oluşturulduğunda, iş emri için otomatik olarak bir iş emri projesi oluşturulur.  
- Her iş emri yaşam döngüsü durumunun ilgili proje aşaması olması gerekir.  
- Bir iş emri yaşam döngüsü durumuyla ilgili olan proje aşaması, iş emri projesinde tanımlanan proje grubu için etkin bir aşama olarak tanımlanmalıdır. İş emri projesi, bir iş emrinde otomatik olarak oluşturulur.
- Yeni bir iş emri oluşturduğunuzda, iş emri projesi otomatik tahsisatı **İş emri projesi kurulumu** sayfasındaki kurulumu temel alır.  

Aşağıdaki örnekte iş emri proje grupları, ilgili proje türleri, proje aşamaları ve iş emri yaşam döngüsü durumları arasındaki ilişkilendirmeler gösterilmiştir.

![Şekil 3.](media/03-integration-to-pma.png)

![Şekil 4.](media/04-integration-to-pma.png)

![Şekil 5.](media/05-integration-to-pma.png)

İş emri projelerini ayarlamayla ilgili bilgi için bkz. [İş emri proje kurulumu](../setup-for-work-orders/work-order-project-setup.md). İş emri yaşam döngüsü durumları oluşturma hakkında bilgi için bkz. [İş emri yaşam döngüsü durumları](../setup-for-work-orders/work-order-lifecycle-states.md).

Aşağıdaki örnekte **Varlık yönetimi** modülünde **Proje yönetimi ve muhasebe** modülüyle tümleştirmeyi etkinleştirmek için oluşturulan çeşitli projelere ilişkin grafik genel görünüm gösterilmektedir. Ayrıca, projelerin ilişkili olduğu iş süreçlerini de gösterir.

![Şekil 6.](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]