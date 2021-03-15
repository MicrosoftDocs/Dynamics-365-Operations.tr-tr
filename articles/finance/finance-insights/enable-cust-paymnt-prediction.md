---
title: Müşteri ödeme tahminlerini etkinleştirme (önizleme)
description: Bu konuda, Mali içgörülerde Müşteri ödeme tahminleri özelliğinin nasıl açılacağı ve yapılandırılacağı açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 584c1af5f9252a4b8c88a8866a64184bd0595b2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009430"
---
# <a name="enable-customer-payment-predictions-preview"></a>Müşteri ödeme tahminlerini etkinleştirme (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Mali içgörülerde Müşteri ödeme tahminleri özelliğinin nasıl açılacağı ve yapılandırılacağı açıklanmaktadır. Özelliği **Özellik yönetimi** çalışma alanında açabilir ve yapılandırma ayarlarını **Mali içgörüler parametreleri** sayfasında girebilirsiniz. Bu konu ayrıca özelliği etkili şekilde kullanmanıza yardımcı olabilecek bilgiler de içerir.

> [!NOTE]
> Aşağıdaki adımları tamamlamadan önce, [Mali içgörüler için yapılandırma](configure-for-fin-insites.md) konusundaki ön koşul adımlarını tamamladığınızdan emin olun.

1. Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın. Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın. (Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > Microsoft Dynamics 365 Finance dağıtımınız Service Fabric dağıtımıysa bu adımı atlayabilirsiniz. Mali içgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır. Özelliği **Özellik yönetimi** çalışma alanında görmüyorsanız veya özelliği açmaya çalışırken sorun yaşıyorsanız <fiap@microsoft.com> adresiyle iletişime geçin.

2. Müşteri ödeme içgörüleri özelliğini açın:

    1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
    2. **Müşteri ödeme içgörüleri (önizleme)** adlı özelliği bulun.
    3. **Şimdi etkinleştir**'i seçin.

    Müşteri ödeme içgörüleri özelliği açılır ve yapılandırmaya hazır hale gelir.

3. Müşteri ödeme içgörüleri özelliğini yapılandırın:

    1. **Alacak ve tahsilatlar \> Kurulum \> Mali içgörüler \> Mali içgörü parametreleri** bölümüne gidin.

        [![Özellik yapılandırılmadan önce mali içgörü parametreleri sayfası](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. **Mali içgörü parametreleri** sayfasındaki **Müşteri ödeme içgörüleri** sekmesinde, **Tahmin modeli için veri alanları** sayfasını açmak için **Tahmin modelinde kullanılan veri alanlarını göster** bağlantısını seçin. Burada, müşteri ödeme tahminleriyle ilgili yapay zeka (AI) tahmin modeli oluşturmak için kullanılan varsayılan alanların listesini görüntüleyebilirsiniz.

        Tahmin modelini oluşturmak için varsayılan alan listesini kullanmak üzere, **Tahmin modeli için veri alanları** sayfasını kapatın ve sonra **Mali içgörü parametreleri** sayfasında, **Özelliği etkinleştir** seçeneğini **Evet** olarak ayarlayın.

    3. İşletmeniz için **Çok geç** tahmin demetinin ne anlama geldiğini tanımlamak için "çok geç" hareket dönemini belirtin.

        Her açık fatura için sistem, ödemenin olasılığını üç demette tahmin eder: **Zamanında**, **Geç** ve **Çok geç**.

        - **Zamanında**: Bu demet, işlem vade tarihinde veya bu tarihten önce ödenmesi öngörülen ödemeleri içerir.
        - **Geç**: Bu demet, hareket vade tarihinden sonra ancak "çok geç" hareket döneminin başlangıcından önce ödenmesi öngörülen ödemeleri içerir.
        - **Çok geç**: Bu demet, "çok geç" hareket döneminin başlangıcından sonra ödenmesi öngörülen ödemeleri içerir.

        > [!NOTE]
        > "Çok geç" hareket dönemini değiştirirseniz ve müşteri ödemeleri için AI tahmin modeli oluşturulduktan sonra **Geç eşiğini değiştir**'i seçerseniz, mevcut tahmin modeli silinir ve yeni bir model oluşturulur. Yeni tahmin modeli, dönemi tanımlamak için girilmiş olan ayarlara göre hareketleri "çok geç" dönemine taşır.

    4. "Çok geç" hareket dönemini tanımlamayı bitirdikten sonra, tahmin modelini oluşturmak için **Tahmin modeli oluştur**'u seçin. **Mali içgörü parametreleri** sayfasındaki **Tahmin modeli** bölümü, tahmin modelinin durumunu gösterir.

        > [!NOTE]
        > Tahmin modeli oluşturulurken istediğiniz zaman, işlemi yeniden başlatmak için **Model oluşturma işlemini sıfırla**'yı seçebilirsiniz.

    Özellik şimdi yapılandırılmış ve kullanılmaya hazır olur.

Özellik açılıp yapılandırıldıktan ve tahmin model oluşturulup çalışmaya başladıktan sonra, aşağıdaki şekilde gösterildiği gibi, **Mali içgörü parametreleri** sayfasının **Tahmin modeli** bölümü modelin doğruluğunu gösterir.

[![Mali içgörü parametreleri sayfasında tahmin modelinin doğruluğu](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Serbest bırakma ayrıntıları

Mali içgörüler genel önizleme, Amerika Birleşik Devletleri, Avrupa ve Birleşik Krallık'ta denetim dağıtımları için kullanılabilir. Microsoft, destek sunduğu bölge sayısını kademeli olarak artırmaktadır.

Genel önizleme özellikleri, yalnızca Katman 2 korumalı alan ortamlarında açık olabilir ve açılmalıdır. Korumalı alan ortamında oluşturulan kurulum ve AI modelleri, üretim ortamına geçirilemez. Daha fazla bilgi için bkz. [Microsoft Dynamics 365 Önizlemeleri için Ek Kullanım Koşulları](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Gizlilik bildirimi

Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]