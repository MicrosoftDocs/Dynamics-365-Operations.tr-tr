---
title: Mali raporlama ile ilgili SSS
description: Bu konuda, Mali raporlama hakkında sık sorulan bazı soruların yanıtları sağlanmaktadır.
author: jiwo
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd493e855e45362c1681dc9cdfbbcb71f7627d64624cd093eadab32fd966c174
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733623"
---
# <a name="financial-reporting-faq"></a>Mali raporlama ile ilgili SSS

Bu konuda, Mali raporlama hakkında sık sorulan soruların yanıtları sağlanmaktadır.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Ağaç güvenliğini kullanarak bir rapora erişimi nasıl kısıtlayabilirim?

Aşağıdaki örnekte, ağaç güvenliği kullanılarak bir rapora erişimin nasıl kısıtlanacağı gösterilmektedir.

USMF demo şirketi, tüm Mali raporlama kullanıcılarının erişemeyeceği bir **Bilanço** raporuna sahiptir. Rapora yalnızca belirli kullanıcıların erişmesini sağlamak üzere tek bir rapora erişimi kısıtlamak için ağaç güvenliğini kullanabilirsiniz.

1. Financial Reporter Report Designer'da oturum açın.
2. Yeni bir ağaç tanımı oluşturmak için **Dosya \> Yeni \> Ağaç Tanımı**'nı seçin.
3. **Birim Güvenliği** sütununda **Özet** satırına çift dokunun (veya çift tıklayın).
4. **Kullanıcılar ve Gruplar**'ı seçin.
5. Rapora erişmesi gereken kullanıcıları veya grupları seçin.
6. **Kaydet**'i seçin.
7. Rapor tanımına yeni ağaç tanımınızı ekleyin.
8. Ağaç tanımında **Ayar**'ı seçin. Ardından, **Raporlama birimi seçimi** altında **Tüm birimleri dahil et**'i seçin.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hangi hesapların bakiyelerimle eşleşmediğini nasıl belirleyeceğim?

Eşleşen bakiyeleri olmayan bir raporunuz varsa her hesabı ve farkını tanımlamak için aşağıdaki yordamları kullanın.

### <a name="in-financial-reporter-report-designer"></a>Financial Reporter Report Designer'te

1. Yeni bir satır tanımı oluşturun.
2. **Düzenle \> Boyutlardan Satır Ekle**'yi seçin.
3. **MainAccount**'u seçin.
4. **Tamam**'ı seçin.
5. Satır tanımını kaydedin.
6. Yeni bir sütun tanımı oluşturun.
7. Yeni bir rapor tanımı oluşturun.
8. **Ayarlar**'ı seçin ve bu seçeneğin işaretini kaldırın.
9. Raporu oluşturun. 
10. Raporu Microsoft Excel'e dışarı aktarın.

### <a name="in-dynamics-365-finance"></a>Dynamics 365 Finance'te

1. **Genel muhasebe \> Sorgular ve raporlar \> Mizan**'a gidin.
2. Aşağıdaki alanları ayarlayın:

    - **Başlangıç Tarihi**: Mali yılın başlangıç tarihini girin.
    - **Bitiş Tarihi**: Raporu oluşturduğunuz tarihi girin.
    - **Mali Boyut**: Bu alanı **Ana hesap kümesi** olarak ayarlayın.

3. **Hesapla**'yı seçin.
4. Raporu Excel'e dışarı aktarın.

Artık Financial Reporter Excel raporundan **Mizan** raporuna veri kopyalayarak **Kapanış Bakiyesi** sütunlarını karşılaştırabilirsiniz.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Report Designer'da bir rapor tasarladığımda veya mali rapor oluşturduğumda şu iletiyi alıyorum: "Veri sağlayıcı altyapısındaki bir sorun nedeniyle işlem tamamlanamadı." Nasıl yanıt vermeliyim?

Bu ileti, Mali raporlama kullanılırken sistem veri reyonunda mali meta verileri almaya çalıştığında bir sorun oluştuğunu belirtir. Bu sorunu çözmenin iki yolu vardır:

- Report Designer'da **Araçlar \> Tümleştirme durumu**'na giderek verilerin tümleştirme durumunu inceleyin. Tümleştirme tamamlanmamışsa tamamlanmasını bekleyin. Ardından, iletiyi aldığınızda yaptığınız işlemi yeniden deneyin.
- Sorunu tanımlamak ve üzerinde çalışmak için Destek ile iletişime geçin. Sistemde tutarsız veriler olabilir. Destek mühendisleri, bu sorunu sunucuda tanımlamanıza ve güncelleştirme gerektirebilecek belirli verileri bulmanıza yardımcı olabilir.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Geçmiş kuru dönüştürme işleminin seçimi rapor performansını nasıl etkiler?

Geçmiş kur genellikle yedek akçe, kaynak, tesis, ekipman ve öz varlık hesaplarıyla birlikte kullanılır. Geçmiş kur, Mali Muhasebe Standartları Kurulu (FASB) veya genel kabul görmüş muhasebe ilkeleri (GAAP) yönergelerine göre gerekli olabilir. Daha fazla bilgi için bkz. [Mali raporlamada para birimi özellikleri](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Kaç çeşit döviz kuru vardır?

Üç tür kur vardır:

- **Geçerli kur**: Bu tür genellikle bilanço hesaplarında kullanılır. Genellikle *spot döviz kuru* olarak bilinir ve ayın son günü veya önceden belirlenmiş başka bir tarihteki kur olabilir.
- **Ortalama kur**: Bu tür genellikle gelir tablosu (kar/zarar) hesaplarında kullanılır. Ortalama kuru, basit ortalama veya ağırlıklı ortalama hesaplayacak şekilde ayarlayabilirsiniz.
- **Geçmiş kur**: Bu tür genellikle yedek akçe, kaynak, tesis, ekipman ve öz varlık hesaplarıyla birlikte kullanılır. Bu hesaplar, FASB veya GAAP yönergelerine göre gerekli olabilir.

## <a name="how-does-historical-currency-translation-work"></a>Geçmiş para birimi dönüştürme nasıl işler?

Kurlar hareket tarihine özgüdür. Bu nedenle her hareket, en yakın döviz kuruna göre ayrı ayrı dönüştürülür.

Geçmiş para birimi dönüştürmede, ayrı ayrı hareket ayrıntıları yerine önceden hesaplanmış dönem bakiyeleri kullanılabilir. Bu davranış, geçerli kuru dönüştürme davranışından farklıdır.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Geçmiş para birimi dönüştürme performansı nasıl etkiler?

Raporlarda sunulan veriler güncelleştirildiğinde hareket ayrıntıları denetlenerek tutarların yeniden hesaplanması gerektiğinden gecikme olabilir. Bu gecikme, kurlar her güncelleştirildiğinde veya daha fazla hareket deftere nakledildiğinde tetiklenir. Örneğin, geçmiş dönüştürme işlemi için günde birkaç kez binlerce hesap ayarlanıyorsa rapordaki verilerin güncelleştirilmesinden önce bir saat kadar gecikme olabilir. Diğer taraftan belirtilen hesaplar daha az sayıdaysa rapor verilerindeki güncelleştirmeler için işleme süresi dakikalara veya daha kısa bir süreye düşürülebilir.

Benzer şekilde geçmiş türü hesaplar için para birimi dönüştürme kullanılarak raporlar oluşturulduğunda harekat başına ek hesaplamalar yapılır. Hesap sayısına bağlı olarak rapor oluşturma süresi iki kat fazla olabilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
