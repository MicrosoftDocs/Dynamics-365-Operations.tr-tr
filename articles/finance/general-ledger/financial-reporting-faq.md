---
title: Mali raporlama ile ilgili SSS
description: Bu konuda, diğer kullanıcıların mali raporlama ile ilgili soruları listelenmektedir.
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
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923037"
---
# <a name="financial-reporting-faq"></a>Mali raporlama ile ilgili SSS 

Bu konu, finansal raporlama hakkında sık sorulan soruların yanıtlarını sağlar. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Ağaç güvenliğini kullanarak bir rapora erişimi nasıl kısıtlayabilirim?

Aşağıdaki örnek, ağaç güvenliğini kullanarak bir rapora erişimin nasıl kısıtlanacağını gösterir.

USMF demo şirketi, tüm Financial Reporting kullanıcılarının erişemeyeceği bir Bilanço raporuna sahiptir. Erişimi sınırlamak için rapora yalnızca belirli kullanıcıların erişmesini sağlamak üzere tek bir rapora erişimi kısıtlamak için ağaç güvenliğini kullanabilirsiniz. Erişimi kısıtlamak için şu adımları izleyin: 

1. Financial Reporter Report Designer'da oturum açın.
2. Yeni ağaç tanımı oluşturun. **Dosya > Yeni > Ağaç Tanımı**'na gidin.
3. **Birim Güvenliği** sütununda **Özet** satırına çift tıklayın.
4. **Kullanıcılar ve Gruplar**'ı seçin.  
5. Bu rapora erişmesi gereken kullanıcıları veya grupları seçin. 
6. **Kaydet**'i seçin.
7. Rapor tanımına yeni ağaç tanımınızı ekleyin.
8. Ağaç tanımında **Ayar**'ı seçin. **Raporlama birimi seçimi** altında **Tüm birimleri dahil et**'i seçin.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Hangi hesapların bakiyelerimle eşleşmediğini nasıl belirleyeceğim?

Eşleşen bakiyeleri olmayan bir raporunuz varsa her hesabı ve farklarını tanımlamak için gerçekleştirebileceğiniz adımlar burada verilmiştir. 

**Financial Reporter Report Designer**
1. Financial Reporter Report Designer'da yeni satır tanımı oluşturun. 
2. **Düzenle > Boyutlardan Satır Ekle**'yi seçin.
3. **MainAccount**'u seçin.  
4. **Tamam**'ı seçin.
5. Satır tanımını kaydedin.
6. Yeni sütun tanımı oluşturun
7. Yeni rapor tanımı oluşturun.
8. **Ayarlar**'ı seçin ve bu seçeneğin işaretini kaldırın.  
9. Raporu oluşturun. 
10. Raporu Microsoft Excel'e dışarı aktarın.

**Dynamics 365 Finance** 
1. Dynamics 365 Finance'te **Genel Muhasebe > Sorgular ve Raporlar > Mizan**'a tıklayın.
2. Aşağıdaki parametreleri ayarlayın:
   - **Başlangıç Tarihi** - Mali yılın başlangıç tarihini girin.
   - **Bitiş Tarihi** - Raporu oluşturduğunuz tarihi girin.
   - **Finansal Boyut** - Bu alanı **Ana Hesap kümesi** olarak ayarlayın.
 3. **Hesapla**'yı seçin.
 4. Raporu Microsoft Excel'e dışarı aktarın.

Artık Mali Raporlayıcı Excel raporundan Mizan raporuna veri kopyalayabilirsiniz ve böylece **Kapanış Bakiyesi** sütunlarını karşılaştırabilirsiniz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]