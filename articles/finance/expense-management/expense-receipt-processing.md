---
title: Gider makbuzu işleme
description: Bu konu, makbuzlar için optik karakter tanıma (OCR) işlemi hakkında bilgi vermektedir. Bu özellik, Microsoft Dynamics 365 Finance'te gider raporları oluşturulurken kullanıcı deneyiminin geliştirilmesi için tasarlanmıştır.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e819521828b054f70476b1eb061ee08c486d09f
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113698"
---
# <a name="public-preview-expense-receipt-processing"></a>Genel Önizleme: Gider makbuzu işleme

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Gider girişi, makbuzlar için optik karakter tanıma (OCR) işleminin devreye girmesiyle gelişim kaydetmiştir. Bu özellik, gider raporları oluşturulurken kullanıcı deneyiminin geliştirilmesi için tasarlanmıştır.

## <a name="key-features"></a>Önemli özellikler

- Satıcı adı, tarih ve toplam tutar makbuzlardan ayıklanır.
- Özellik, iliştirilmemiş makbuzları iliştirilmemiş gider hareketlerine eşlemeyi dener.
- Kullanıcılar, makbuzlardan el ile girilmiş gider hareketleri oluşturabilirler.

## <a name="usage-examples"></a>Kullanım örnekleri

- **Gider raporu oluşturulurken kredi kartı hareketleri içeren makbuzları otomatik olarak iliştirin.**

    1. **Gider yönetimi** çalışma alanını açın.
    2. **Makbuzlar** sekmesinde, iliştirilmemiş makbuzların olduğunu doğrulayın. Makbuzları **Makbuzlar** sekmesinde de yükleyebilirsiniz.
    3. **Giderler** sekmesinde, iliştirilmemiş giderlerin olduğunu doğrulayın. Genel olarak, gider yöneticisi bu giderleri kredi kartı sağlayıcısından içe aktarır.
    4. **Yeni gider raporu**'nu seçin. Artık, gider raporu oluştururken giderleri ve makbuzları da ekleyebildiğinizi bildirelim. Hem giderler hem de makbuzlar eklerseniz, makbuzların giderlere karşı otomatik eşleşmesi tetiklenir.

- **Bir gider oluşturun veya makbuzdan bir gideri eşleyin.**

    1. Bir gider raporunda, **Makbuzlar** sekmesinde, **Giriş ekle**'yi seçerek bir makbuz iliştirin.
    2. Makbuzun karşıya yüklenen resminin altındaki **Oluştur** ve **Eşleştir** seçeneklerine dikkat edin.

        - El ile girilmiş bir gider hareketi oluşturmak ve makbuzdan ayıklanan değerleri doldurmak için **Oluştur**'u seçin.
        - **Eşleştir**'i seçerseniz, sistem varolan bir gideri makbuza eşleştirmeye çalışır.

## <a name="installation"></a>Yükleme

Bu özellik, gider deneyimini basitleştirmeye yardımcı olmak için **Gider raporları yeniden tasarlandı** özelliğiyle birlikte çalışır.

Bu gelişmiş gider yeteneklerini kullanmak için, kurulumunuzda Microsoft Dynamics 365 Finance için Gider Yönetimi Hizmeti eklentisini yükleyin ve özellikleri etkinleştirin. Eklentiye, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden erişebilirsiniz.

1. LCS'de oturum açın ve istediğiniz ortamı açın.
2. **Tüm ayrıntılar**'a gidin.
3. **Bakım yap**'ı seçin veya **Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.
4. **Yeni eklenti yükle**'yi seçin.
5. **Gider Yönetimi Hizmeti**'ni seçin.
6. Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.
7. **Yükle**'yi seçin.

**Özellik yönetimi** çalışma alanında aşağıdaki özellikleri açın:

- Gider raporları yeniden tasarlandı
- Otomatik eşleştir ve makbuzdan gider oluştur

Bu özellikleri açtığınız zaman aşağıdaki eylemler gerçekleşir:

- Mevcut **Gider yönetimi** çalışma alanı yeni çalışma alanıyla değiştirilir.
- Gider alanı görünürlüğü için yeni bir menü öğesi eklenir.
- Önceki **Gider raporları** sayfasını **Gider yönetimi > Giderlerim > Gider raporları**'na giderek açmaya devam edebilirsiniz.
- İş akışları ve onayların sizi varolan gider raporları sayfasına götürmeye devam eder.
- Makbuzlar Microsoft Azure Cognitive Services üzerinden işlenir ve meta veriler ayıklanıp eklenir.
- Eşleşen iliştirilmemiş makbuzları içeren bir gider raporu oluşturmanıza olanak sağlayan bir seçenek eklenmiştir.
- Gider raporlarına eklenen bir seçenek, makbuzdan gider satırı oluşturmanıza olanak sağlar veya varolan bir makbuzu varolan bir gider satırıyla eşleştirmeye çalışır.

Gider raporları yeniden tasarlandı özelliği hakkında daha fazla bilgi için bkz. [Gider raporları yeniden tasarlandı](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

**Microsoft, modelleri için verilerimi kullanıyor mu?**

Hayır, Microsoft makbuz işleme hizmeti için genel bir makine öğrenimi modeli oluşturdu. Bu model, karşıya yüklediğiniz makbuzlara dayanmaz.

**Bu özellik nerede kullanılıyor ve işleniyor?**

Şu anda Amerika Birleşik Devletleri destekleniyor.

**Makbuzlarım nereye gidiyor?**

Finance, alan verilerini ayıklamak için Cognitive Services ile bağlantı kuracaktır. Cognitive Services, işlem yapılırken makbuzunuzun bir kopyasını 24 saate kadar koruyacaktır. İşlem tamamlandıktan sonra, Cognitive Services makbuzu kaldırır. Makbuzlar Finance'te depolanmaya devam eder.

Daha fazla bilgi için bkz. [Form Tanıma'nın yeni yeteneğiyle makbuz kavramayı etkinleştirme](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
