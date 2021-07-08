---
title: Mali raporlama ile ilgili SSS
description: Bu konuda, Mali raporlama hakkında sık sorulan bazı soruların yanıtları sağlanmaktadır.
author: jiwo
ms.date: 01/13/2021
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266645"
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
