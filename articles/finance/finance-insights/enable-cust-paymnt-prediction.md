---
title: Müşteri ödeme tahminlerini etkinleştirme
description: Bu konuda, Mali içgörülerde Müşteri ödeme tahminleri özelliğinin nasıl açılacağı ve yapılandırılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a52d38e8fb842c7fbc8adf60a6daaef6cdc9d5ec
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713374"
---
# <a name="enable-customer-payment-predictions"></a>Müşteri ödeme tahminlerini etkinleştirme

[!include [banner](../includes/banner.md)]

Bu konuda, Mali içgörülerde Müşteri ödeme tahminleri özelliğinin nasıl açılacağı ve yapılandırılacağı açıklanmaktadır. Özelliği **Özellik yönetimi** çalışma alanında açabilir ve yapılandırma ayarlarını **Finance Insights yapılandırması** sayfasında girebilirsiniz. Bu konu ayrıca özelliği etkili şekilde kullanmanıza yardımcı olabilecek bilgiler de içerir.

> [!NOTE]
> Aşağıdaki adımları tamamlamadan önce, [Mali içgörüler için yapılandırma](configure-for-fin-insites.md) konusundaki ön koşul adımlarını tamamladığınızdan emin olun.

1. Müşteri ödeme tahminleri özelliğini açın:

    1. **Özellik yönetimi** çalışma alanını açın.
    2. **Güncelleştirmeleri denetle**'yi seçin.
    3. **Tümü** sekmesinde, **Müşteri ödeme tahminleri**'ni arayın. Bu özelliği bulamazsanız **(Önizleme) Müşteri ödeme tahminleri**'ni arayın. 
    4. Özelliği etkinleştirin.

    Müşteri ödeme tahminleri özelliği açılır ve yapılandırmaya hazır hale gelir.

2. Müşteri ödeme içgörüleri özelliğini yapılandırın:

    1. **Alacak ve tahsilatlar \> Kurulum \> Finance Insights \> Müşteri ödeme tahminleri** bölümüne gidin.
    2. **Finance Insights yapılandırması** sayfasındaki **Müşteri ödeme tahminleri** sekmesinde, **Tahmin modeli için veri alanları** sayfasını açmak için **Tahmin modelinde kullanılan veri alanlarını göster**'i seçin. Burada, müşteri ödeme tahminleriyle ilgili yapay zeka (AI) tahmin modeli oluşturmak için kullanılan varsayılan alanların listesini görüntüleyebilirsiniz.

        Tahmin modelini oluşturmak için varsayılan alan listesini kullanmak üzere, **Tahmin modeli için veri alanları** sayfasını kapatın ve sonra **Finance Insights yapılandırması** sayfasında, **Özelliği etkinleştir** seçeneğini **Evet** olarak ayarlayın.
        
   > [!NOTE]
   > **Müşteri ödeme tahminleri** özelliği, önceki altı-dokuz ay içinde yer alan 100'den fazla hareket gerektirir. Hareketler; serbest metin faturaları, satış siparişleri ve müşteri ödemelerini içerebilir. Bu veriler, **Zamanında**, **Geç** ve **Çok geç** ayarlarına yayılmalıdır.    
     

    3. İşletmeniz için **Çok geç** tahmin demetinin ne anlama geldiğini tanımlamak için "çok geç" hareket dönemini belirtin.

        Her açık fatura için sistem, ödemenin olasılığını üç demette tahmin eder: **Zamanında**, **Geç** ve **Çok geç**.

        - **Zamanında**: Bu demet, işlem vade tarihinde veya bu tarihten önce ödenmesi öngörülen ödemeleri içerir.
        - **Geç**: Bu demet, hareket vade tarihinden sonra ancak "çok geç" hareket döneminin başlangıcından önce ödenmesi öngörülen ödemeleri içerir.
        - **Çok geç**: Bu demet, "çok geç" hareket döneminin başlangıcından sonra ödenmesi öngörülen ödemeleri içerir.

        > [!NOTE]
        > "Çok geç" hareket dönemini değiştirirseniz ve müşteri ödemeleri için AI tahmin modeli oluşturulduktan sonra **Geç eşiğini değiştir**'i seçerseniz, mevcut tahmin modeli silinir ve yeni bir model oluşturulur. Yeni tahmin modeli, dönemi tanımlamak için girilmiş olan ayarlara göre hareketleri "çok geç" dönemine taşır.

    4. "Çok geç" hareket dönemini tanımlamayı bitirdikten sonra, tahmin modelini oluşturmak için **Tahmin modeli oluştur**'u seçin. **Finance Insights yapılandırması** sayfasındaki **Tahmin modeli** bölümü, tahmin modelinin durumunu gösterir.

        > [!NOTE]
        > Tahmin modeli oluşturulurken istediğiniz zaman, işlemi yeniden başlatmak için **Model oluşturma işlemini sıfırla**'yı seçebilirsiniz.

    Özellik şimdi yapılandırılmış ve kullanılmaya hazır olur.

Özellik açılıp yapılandırıldıktan ve tahmin model oluşturulup çalışmaya başladıktan sonra, **Finance Insights parametreleri** sayfasının **Tahmin modeli** bölümü modelin doğruluğunu gösterir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
