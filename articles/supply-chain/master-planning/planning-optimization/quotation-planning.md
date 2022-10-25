---
title: Tekliflere ve RFQ'lara dayalı planlar
description: Bu makalede, planlı siparişleri oluştururken teklifleri ve teklif taleplerini (RFQ'lar) dikkate almak için master planlamanın nasıl ayarlanacağı açıklanır.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690102"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Tekliflere ve RFQ'lara dayalı plan

[!include [banner](../../includes/banner.md)]

Fiyat teklifleri ve fiyat teklifi talepleri (RFQ'lar) gelecekteki olası ve hatta muhtemel siparişleri temsil eder. Bu nedenle, master planlama sırasında bunların dikkate alınması mantıklıdır, böylece mevcut RFQ'lara ve her teklifin gerçek bir siparişe dönüşme olasılığına göre ekstra tedarik planlanabilir. Bu makalede, planlı siparişleri oluştururken teklifleri ve RFQ'ları dikkate almak için master planlamanın nasıl ayarlanacağı açıklanır.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Satış tekliflerini ve/veya RFQ'ları dikkate almak için master planlama ayarlama

Satış tekliflerini ve/veya RFQ'ları dikkate almak üzere master planlama ayarlamak için aşağıdaki yordamı kullanın.

1. **Master Planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Liste bölmesinden mevcut bir planı seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir öznitelik oluşturun.
1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Satış tekliflerini dahil et** – Geçerli plan çalıştırıldığında satış tekliflerini dikkate almak için bu seçeneği *Evet* olarak ayarlayın. Bunları yoksaymak için *Hayır* olarak ayarlayın.
    - **Olasılık %** – Bir teklifin master planlamaya dahil edilmesi için gereken minimum güvenilirlik seviyesini belirleyin. Master planlama hesaplaması, bu olasılık yüzdesi veya daha yüksek olan fırsatlardan oluşturulan tüm teklifleri içerir. Kendilerine olasılık atanmamış veya kendileriyle ilişkili bir fırsat bulunmayan teklifler de dahil olmak üzere tüm teklifleri dahil etmek için bu alanı *0* (sıfır) olarak ayarlayın. Tekliflerin olasılıkları hakkında daha fazla bilgi için sonraki bölüme bakın.
    - **Teklif taleplerini dahil et** – Geçerli plan çalıştırıldığında RFQ'ları dikkate almak için bu seçeneği *Evet* olarak ayarlayın. Bunları yoksaymak için *Hayır* olarak ayarlayın. RFQ'ları dikkate almayı seçerseniz sistem, bunlar için planlı satın alma siparişleri oluşturur, ancak RFQ çözümlenene kadar satıcıyı belirtmez. RFQ'lar için oluşturulan planlanan satın alma siparişleri, diğer planlı siparişlerin miktarlarını etkileyebilir.

1. Master planınızı her zamanki şekilde oluşturmaya devam edin.

## <a name="assign-and-view-probabilities-for-quotations"></a>Teklifler için olasılıklar atama ve görüntüleme

Önceki bölümde belirtildiği gibi, bir master plan yalnızca plan için tanımlanan olasılık eşiğini karşılayan veya aşan teklifleri dikkate alır (bir eşik tanımlanmışsa). Ancak olasılık her bir teklifte doğrudan belirlenmez. Bunun yerine, teklifi oluşturmak için kullanılan fırsattan devralınır. Bu nedenle, doğrudan **Tüm teklifler** sayfasında oluşturulan teklifler, bunlara atanmış olasılığa veya kendileriyle ilişkilendirilmiş bir fırsata sahip olmaz ve master planlama tarafından hiçbir zaman dikkate alınmaz (**Olasılık %** alanı *0* \[sıfır\]) olarak ayarlanır. Kendisine bir olasılık atanmış olması için bir teklifin bir fırsattan oluşturulması gerekir.

### <a name="create-a-quotation-from-an-opportunity"></a>Fırsattan bir teklifi oluşturma

Bir fırsata olasılık atamak ve ardından bu fırsattan bir teklif oluşturmak için aşağıdaki yordamı kullanın.

1. **Satış ve pazarlama \> İlişkiler \> Fırsatlar \> Tüm fırsatlar** seçeneğine gidin.
1. Mevcut bir fırsat seçin ya da yeni bir fırsat oluşturmak için Eylem Bölmesi'nde **Yeni**'yi seçin.
1. Fırsatı istediğiniz şekilde tanımlamak için fırsat sayfasını doldurun. **Olasılık** alanında uygun değeri ayarladığınızdan emin olun. Yalnızca bu değeri veya daha yüksek olasılıkları aramak üzere ayarlanmış master planlar, bu fırsattan oluşturulan teklifleri dikkate alır.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem Bölmesi'ndeki **Fırsat** sekmesinde yer alan **Yeni** grubu içinde, oluşturmak istediğiniz teklif türüne göre **Satış teklifi** veya **Proje teklifi**'ni seçin.
1. **Teklif oluştur** iletişim kutusunda, alanları istediğiniz gibi ayarlayın ve sonra **Tamam**'ı seçin.
1. Yeni bir teklif oluşturulur ve açılır. **Satırlar** hızlı sekmesinde, teklifin içeriğini tanımlamak üzere gerektiği şekilde satış satırları veya proje satırları eklemek için araç çubuğunu kullanın.
1. Eylem bölmesinde, **Kaydet**'i seçin. Ardından teklifi kapatın.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Teklife atanan olasılığı görüntüleme

Bir teklife atanan olasılığı görüntülemek için tek yol, teklifi oluşturmak için kullanılan fırsatı aşağıdaki yordamda açıklandığı gibi açmaktır.

1. **Satış ve pazarlama \> Satış teklifleri \> Tüm teklifler** bölümüne gidin.
1. **Fırsat kimliği** sütunu gösterilmiyorsa (varsayılan kurulumda gizli) geçici olarak göstermek için aşağıdaki adımları izleyin. (Alternatif olarak **Fırsat kimliği** sütununu kullanılabilir tutmak için bunu içeren [kaydedilmiş görünüm](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json) oluşturun.)

    1. Kılavuzu seçin ve tutun (veya sağ tıklayın) ve sonra **Sütun ekle**'yi seçin.
    1. **Sütun ekle** iletişim kutusunda **Alan** alanının *Fırsat* olarak ayarlandığı satırı bulun ve bu satır için **Seç** onay kutusunu seçin.
    1. Seçilen sütunu **Tüm teklifler** sayfasına eklemek için **Güncelle**'yi seçin.

1. Kılavuzda, ilgili teklife ait satırı bulun. Ardından **Fırsat kimliği** sütununda bu satır için değerini seçin.

    > [!NOTE]
    > Proje teklifi arıyorsanız **Teklif türü** sütun üst bilgisini seçmeniz ve filtresini temizlemeniz gerekebilir. Varsayılan kurulumda, bu filtre yalnızca satış teklifleri gösterilecek şekilde ayarlanır.

1. İlgili fırsat açılır. Artık **Olasılık** değerini istediğiniz gibi görüntüleyebilir ve düzenleyebilirsiniz.
