---
title: Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle
description: Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4cc14860bd969048c4378b40d97a7940a8710e89
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934666"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lifecycle Services'dan Elektronik raporlama yapılandırmalarını indirme

[!include [banner](../includes/banner.md)]

Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.

Bu eğitim size Elektronik Raporlama (ER) yapılandırmalarının en yeni sürümlerinin, Microsoft Dynamics Lifecycle Services'dan (LCS) indirme sürecini öğretir.

1. Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

2. **Organizasyon yönetimi** &gt; **Çalışma alanları** &gt; **Elektronik raporlama**'ya gidin.
3. **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.
4. **Microsoft** kutucuğunda, **Depolar**'a tıklayın.

    [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. **Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin. Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:

    1. Yeni bir depo eklemek için **Ekle**'ye tıklayın.
    2. Havuz türü olarak **LCS**'yi seçin.
    3. **Depo oluştur**'a tıklayın.
    4. İstenirse, yetkilendirme yönergelerini izleyin.
    5. Depo için bir ad ve açıklama girin.
    6. Yeni depo girişini onaylamak için **Tamam**'a tıklayın.
    7. Kılavuzda **LCS** türündeki yeni depoyu seçin.

6. Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.

    [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. Sol bölmedeki yapılandırmalar ağacında, gereksinim duyduğunuz ER yapılandırmalarını seçin.
8. **Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.
9. Seçili sürümü LCS'den mevcut örneğe indirmek için **İçe Aktar**'a tıklayın.

    > [!NOTE]
    > Mevcut örnekte bulunan ER yapılandırma sürümleri için **İçe Aktar** düğmesi kullanılamaz.

    [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> ER ayarlarına bağlı olarak yapılandırmalar içeri aktarıldıktan sonra doğrulanır. Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz. İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir. Daha fazla bilgi için bu konunun ilgili makaleleri listesine göz atın.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
