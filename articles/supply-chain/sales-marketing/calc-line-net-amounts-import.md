---
title: Satış siparişlerini ve teklifleri içe aktarırken satır net tutarlarını yeniden hesaplama
description: Bu makalede, satış siparişleri ve teklifler içe aktarıldığında sistemin satır net tutarlarını yeniden hesaplayıp hesaplamayacağı ve bunu nasıl yapacağı açıklanır. Ayrıca, Microsoft Dynamics 365 Supply Chain Management'ın farklı sürümlerindeki davranışı nasıl denetleyebileceğinizi de açıklar.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719347"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Satış siparişlerini ve teklifleri içe aktarırken satır net tutarlarını yeniden hesaplama

[!include [banner](../includes/banner.md)]

Bu makalede, satış siparişleri ve teklifler içe aktarıldığında sistemin satır net tutarlarını yeniden hesaplayıp hesaplamayacağı ve bunu nasıl yapacağı açıklanır. Ayrıca, Microsoft Dynamics 365 Supply Chain Management'ın farklı sürümlerindeki davranışı nasıl denetleyebileceğinizi de açıklar.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Net satır tutarları için yapılan güncelleştirmeler içe aktarma sırasında nasıl hesaplanır?

Supply Chain Management sürüm 10.0.23, [604418 numaralı hata düzeltmesini](https://fix.lcs.dynamics.com/issue/results/?q=604418) kullanıma sundu. Bu hata düzeltmesi, mevcut satış siparişlerine ve tekliflere yapılan güncelleştirmeler içe aktarılırken satırdaki **Net tutar** alanının güncelleştirilebileceği veya yeniden hesaplanabileceği koşulları değiştirdi. Sürüm 10.0.29'da *İçeri aktarma sırasında satır net tutarını hesapla* özelliğini etkinleştirerek bu hata düzeltmesini değiştirebilirsiniz. Bu özellik benzer bir etkiye sahiptir, ancak gerektiğinde eski davranışa dönmenize olanak tanıyan genel bir ayar sağlar. Yeni davranış, sistem çalışmasını daha sezgisel hale getirse de aşağıdaki koşulların tümünün karşılandığı belirli senaryolarda beklenmedik sonuçlara neden olabilir:

- Varolan kayıtları güncelleştiren veriler, Excel aracılığıyla ikili yazma, içe aktarma/dışa aktarma ve bazı üçüncü taraf tümleştirmeleri kullandığınız durumlar da dahil olmak üzere, Açık Veri Protokolü (OData) kullanılarak *Satış siparişi satırları V2*, *Satış teklifi satırları V2* veya *İade siparişi satırları* varlığı aracılığıyla içe aktarılır.
- Yürürlükteki [ticari sözleşme değerlendirme ilkeleri](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper), satış siparişi satırları, satış teklifi satırları ve/veya iade siparişi satırlarındaki **Net tutar** alanında yapılan güncelleştirmeleri kısıtlayan bir değişiklik ilkesi oluşturur. İade siparişi satırları için **Net tutar** alanının her zaman hesaplandığını ve el ile ayarlanamayacağını unutmayın.
- İçe aktarılan veriler, satırlardaki **Net tutar** alanındaki değişiklikleri veya satırlardaki **Net tutar** alanındaki değerin bir veya daha fazla mevcut satır kaydı için yeniden hesaplanmasını sağlayan değişiklikleri (birim fiyat, miktar veya iskonto gibi) içerir.

Bu belirli senaryolarda ticari sözleşme değerlendirme ilkesinin etkisi, satırdaki **Net tutar** alanına yapılan güncelleştirmeler için bir sınırlama koymaktır. Bu sınırlama, *değiştirme ilkesi* olarak bilinir. Bu ilke nedeniyle, alanı düzenlemek veya yeniden hesaplamak için kullanıcı arabirimini kullandığınızda sistem, değişikliği yapmak isteyip istemediğinizi sorar. Ancak, bir kaydı içe aktardığınızda, sistemin bu seçimi sizin için yapması gerekir. 10.0.23 sürümünden önce sistem, gelen satır net tutarı 0 (sıfır) olmadıkça satır net tutarını her zaman değişmeden bırakmaktaydı. Ancak daha yeni sürümlerde, bunu yapmaması açıkça belirtilmedikçe sistem, net tutarı her zaman gereken şekilde güncelleştirir veya yeniden hesaplar. Yeni davranış daha mantıklı olsa da, eski davranışın geçerli olduğunu varsayan süreçler veya tümleştirmeler çalıştırıyorsanız, bu durum sizin için sorunlara neden olabilir. Bu makalede, gerekiyorsa eski davranışa nasıl dönebileceğiniz anlatılmaktadır.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>10.0.29 ve sonraki sürümlerdeki satır net tutarlarının hesaplamalarını kontrol etme

Supply Chain Management sürüm 10.0.29 ile *İçeri aktarma sırasında satır net tutarını hesapla* adlı bir özellik kullanıma sunmuştur. Bu özellik, **Alacak hesapları parametreleri** sayfasına **Satır net tutarını hesapla** adlı bir seçenek ekler. Bu seçenek içe aktarma sırasında satır net tutarlarını hesaplamada kullanılacak yeni ve eski davranışlar arasından seçim yapmanızı sağlar.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>İçeri aktarma sırasında satır net tutarını hesapla özelliğini açma veya kapatma

10.0.29 sürümüne güncelleştirdiğinizde, *İçeri aktarma sırasında satır net tutarını hesapla* özelliği varsayılan olarak etkinleştirilir ve yeni **Satır net tutarını hesapla** seçeneği başlangıçta *Evet* olarak ayarlanır. *Evet* ayarı yeni standart davranışa karşılık gelir. Bu makalenin devamında açıklandığı gibi bu davranış, [CalculateLineAmount parametresinin](#CalculateLineAmount) işlevi hariç olmak üzere, özellik kapalı olduğunda sistem davranışıyla eşleşir. *Hayır* ayarı, 10.0.23 öncesi sürümlerde sistem davranışıyla eşleşir ve esas olarak eski tümleştirme senaryolarını desteklemek için sağlanmıştır.

Yöneticiler [Özellik yönetimi çalışma alanını](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanarak *İçeri aktarma sırasında satır net tutarını hesapla* özelliğini etkinleştirebilir veya devre dışı bırakabilir.

### <a name="set-the-calculate-line-net-amount-option"></a>İçeri aktarma sırasında satır net tutarını hesapla seçeneğini ayarlama

*İçeri aktarma sırasında satır net tutarını hesapla* özelliği açık olduğunda, aşağıdaki adımları izleyerek **Satır net tutarını hesapla** seçeneğini ayarlayabilirsiniz.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
1. **Fiyatlar** sekmesinde, **Tümleştirme yoluyla satır net tutarını hesaplama** hızlı sekmesinde **Satır net tutarını hesapla** seçeneğini aşağıdaki değerlerden birine ayarlayın:

    - *Evet* – Sistem gerektiğinde her durumda satır tutarlarını yeniden hesaplar ve güncelleştirir. (Bu nedenle, ticari sözleşme değerlendirme ilkesini yok sayacaktır.)
    - *Hayır* – Herhangi bir satırın mevcut veya gelen net tutarı 0 (sıfır) ise, o satırın değeri diğer değerlere göre (birim fiyat, miktar ve iskonto gibi) yeniden hesaplanır. Varolan veya gelen net tutar 0'dan (sıfır) farklıysa ve satırdaki **Net tutar** alanında bir değişiklik ilkesi ayarlanmışsa, satır fiyatı, miktar ve/veya iskontodaki gelen değişiklikler satır toplamının yeniden hesaplanması gerektiği anlamına gelse bile alan yeniden hesaplanmaz veya güncelleştirilmez. Bu davranış sürüm 10.0.22 ile aynıdır.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>İçeri aktarma sırasında satır net tutarını hesapla özelliği CalculateLineAmount parametresini nasıl etkiler?

*İçeri aktarma sırasında satır net tutarını hesapla* özelliği açık olduğunda, `SalesLine` ve `SalesQuotationLine` tablolarının `CalculateLineAmount` parametresinin değeri üzerinde hiçbir etkisi olmaz. Bunun yerine davranış, önceki bölümde anlatılan **Satır net tutarını hesapla** seçeneğiyle genel olarak kontrol edilir. Bu nedenle, özellik açık olduğunda, `CalculateLineAmount` değeri ile ilgili herhangi bir bağımlılık bulunmaması gerekir.

*İçeri aktarma sırasında satır net tutarını hesapla* özelliği kapatıldığında `SalesLine` ve `SalesQuotationLine` tablolarının `CalculateLineAmount` parametresi, sonraki bölümde açıklandığı gibi, Supply Chain Management 10.0.23 ile 10.0.28 arasındaki sürümlerle aynı şekilde çalışır.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>10.0.28 ve önceki sürümlerde satır net tutarı hesaplamalarını kontrol etme

[604418 numaralı hata düzeltmesi](https://fix.lcs.dynamics.com/issue/results/?q=604418) sürüm 10.0.23'te kullanıma sunulduğunda, bir satır net tutarı düzenlendiğinde veya satır net tutarının başka bir değişiklik (güncelleştirilmiş bir madde fiyatı gibi) nedeniyle yeniden hesaplanması gerektiğinde her ilgili veri varlığının nasıl davranacağını seçmek mümkün olmuştur. Bu davranışı, her bir satır için yeni `CalculateLineAmount` parametresini içe aktarılan dosyadaki aşağıdaki değerlerden birine ayarlayarak denetleyebilirsiniz:

- **`CalculateLineAmount` = *1*** – Alan için bir değişiklik ilkesinin ayarlanıp ayarlanmadığına bakılmaksızın ve gelen veya varolan satır net tutarının değeri ne olursa olsun satırdaki **Net tutar** alanı her zaman yeniden hesaplanır ve güncelleştirilir.
- **`CalculateLineAmount` = *0*** – Herhangi bir satırın mevcut veya gelen net tutarı 0 (sıfır) ise, o satırın değeri diğer değerlere göre (birim fiyat, miktar ve iskonto gibi) yeniden hesaplanır. Varolan veya gelen net tutar 0'dan (sıfır) farklıysa ve satırdaki **Net tutar** alanında bir değişiklik ilkesi ayarlanmışsa, alan yeniden hesaplanmaz veya güncelleştirilmez.  

Sistem davranışı, Supply Chain Management sürümünüze bağlıdır:

- Sürüm 10.0.22 ve önceki sürümlerde, sistem her zaman `CalculateLineAmount` parametresi *0* olarak ayarlanmış gibi davranır ve `CalculateLineAmount` parametresi *1* olarak ayarlanmış gibi davranmasının hiçbir yolu yoktur.
- 10.0.28 ile 10.0.23 arasındaki sürümlerde sistem, `CalculateLineAmount` parametresinin içe aktarma dosyasında açıkça *0* olarak ayarlanmadığı tüm satırlar için parametre *1* olarak ayarlanmış gibi davranır.
