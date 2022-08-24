---
title: İşlem tabanlı e-postalara ve makbuz e-postalarına QR kodu veya barkod ekleme
description: Bu makale, Microsoft Dynamics 365 Commerce'de işlem tabanlı e-postalara ve makbuz e-postalarına sıra kimliklerini temsil eden QR kodlarının ve barkodların nasıl ekleneceğini açıklamaktadır.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 2832d1df3893e124759e4719a64341494cea2204
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272057"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>İşlem tabanlı e-postalara ve makbuz e-postalarına QR kodu veya barkod ekleme

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'de işlem tabanlı e-postalara ve makbuz e-postalarına sıra kimliklerini temsil eden QR kodlarının ve barkodların nasıl ekleneceğini açıklamaktadır.

Bir perakende ortamında sipariş arama sürecini hızlandırmaya yardımcı olacak şekilde, işlem tabanlı e-postalara QR kodlarını ve barkodları kolayca dahil edebilirsiniz. E-postalara QR kodları ve Barkodlar eklemek için, oluşturma ve işleme servinden QR kodu veya barkod görüntüsü isteyen bir HTML **\<img\>** etiketi kullanın. Microsoft bu hizmeti sağlamaz. Ancak, bir sorgu dizesinde geçirilen bir değere dayalı olarak dinamik olarak oluşturulan QR kodları veya Barkod hizmeti veren birçok ücretsiz veya uygun fiyatlı hizmet vardır.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>İşlem tabanlı bir e-postaya QR kodu veya barkod ekleme

Bir e-ticaret satın alma işleminin parçası olarak gönderilen işlem tabanlı bir e-postaya bir QR kodu veya barkod eklemek için, aşağıdaki adımları izleyin.

1. İşlem tabanlı e-posta şablonu için kaynak HTML'i açın ve QR kodu veya barkod hizmetinize işaret eden bir HTML **\<img\>** etiketi ekleyin. Aşağıda bir örnek verilmiştir.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Önceki örnekle ilgili aşağıda bir açıklama verilmiştir:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** QR kodu veya barkod hizmetinizin etki alanını temsil eder.
    - **data**, QR kodu veya barkod hizmetinin, QR kodu veya barkod olarak işlenmesi gereken içeriği almak için kullandığı parametreyi temsil eder.

        **%salesid%** değeri bu parametreye atanmalıdır. Bu örnekte, değerin görüntü için alternatif metin olarak da kullanıldığına dikkat edin.

    - **param1** ve **param2** ek isteğe bağlı parametreleri temsil eder.

1. **Retail ve Commerce \> Headquarters kurulum \> parametreler \> kuruluş e-posta şablonları**'na gidin ve güncelleştirilmiş HTML'i uygun işlem tabanlı e-posta şablonuna yükleyin.

> [!NOTE]
> QR kodu ve barkod hizmeti sağlayıcıları arasında parametreler farklılık gösterebilir. Bu nedenle, değer atamanız gereken parametreleri onaylamak için servis sağlayıcınızla mutlaka iletişim kurun.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>Bir makbuz e-postasına QR kodu veya barkod ekleme 

Satış noktasında (POS) bir satın alma yapıldıktan sonra gönderilebilecek bir makbuz e-postasına QR kodu veya barkod eklemek için, aşağıdaki adımları izleyin.

1. Makbuz e-postası şablonu için kaynak HTML'i açın ve QR kodu veya barkod hizmetinize işaret eden bir HTML **\<img\>** etiketi ekleyin. Aşağıda bir örnek verilmiştir.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Önceki örnekle ilgili aşağıda bir açıklama verilmiştir:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** QR kodu veya barkod hizmetinizin etki alanını temsil eder.
    - **data**, QR kodu veya barkod hizmetinin, QR kodu veya barkod olarak işlenmesi gereken içeriği almak için kullandığı parametreyi temsil eder.

        **%receiptid%** değeri bu parametreye atanmalıdır. Bu örnekte, değerin görüntü için alternatif metin olarak da kullanıldığına dikkat edin.

    - **param1** ve **param2** ek isteğe bağlı parametreleri temsil eder.

1. **Retail ve Commerce \> Headquarters kurulum \> parametreler \> kuruluş e-posta şablonları**'na gidin ve güncelleştirilmiş HTML'i **emailrecpt** e-posta kimliğine yükleyin.

> [!NOTE]
> QR kodu ve barkod hizmeti sağlayıcıları arasında parametreler farklılık gösterebilir. Bu nedenle, değer atamanız gereken parametreleri onaylamak için servis sağlayıcınızla mutlaka iletişim kurun.

## <a name="additional-resources"></a>Ek kaynaklar

[Modern POS'tan (MPOS) e-posta makbuzları gönderme](email-receipts.md)

[Hareket olayları için e-posta şablonları oluşturma](email-templates-transactions.md)
