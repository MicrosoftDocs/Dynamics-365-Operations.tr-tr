---
title: Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle
description: Bu makalede, Elektronik raporlama (ER) yapılandırmalarının Microsoft Dynamics Lifecycle Services'dan (LCS) indirilmesi açıklanmaktadır.
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8ba720f997981e85ea08d532f23341a838533ac4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885308"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle

[!include [banner](../includes/banner.md)]

Bu makalede, yeni [Elektronik raporlama (ER) yapılandırmalarının](general-electronic-reporting.md#Configuration) en yeni sürümünün Microsoft Dynamics Lifecycle Services'daki (LCS) [Paylaşılan varlık kitaplığı](../lifecycle-services/asset-library.md)'ndan nasıl indirileceği açıklanmaktadır.

> [!IMPORTANT]
> LCS'nin, ER yapılandırmaları için saklama deposu olarak kullanılma özelliği [kullanım dışı bırakılıyor](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Daha fazla bilgi için bkz. [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) depolamasının kullanım dışı bırakılması](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

1. Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

2. **Organizasyon yönetimi** &gt; **Çalışma alanları** &gt; **Elektronik raporlama**'ya gidin.
3. **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.
4. **Microsoft** kutucuğunda, **Depolar**'a tıklayın.

    [![Yerelleştirme yapılandırmaları sayfasında Microsoft kutucuğu.](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. **Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin. Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:

    1. Yeni bir depo eklemek için **Ekle**'yi seçin.
    2. Havuz türü olarak **LCS**'yi seçin.
    3. **Depo oluştur**'u seçin.
    4. Yetkilendirme konusunda bir bildirim geldiğinde, ekrandaki yönergeleri izleyin.
    5. Depo için bir ad ve açıklama girin.
    6. Yeni depo girişini onaylamak için **Tamam**'ı seçin.
    7. Kılavuzda **LCS** türündeki yeni depoyu seçin.

6. Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.

    [![Yapılandırma havuzu sayfası.](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > LCS 'de Paylaşılan varlık kitaplığı'ndan yapılandırmaları indirmek için LCS deposuna erişmede sorun yaşıyorsanız, yapılandırmaları [Global havuzdan](er-download-configurations-global-repo.md) indirebilirsiniz.

7. Sol bölmedeki yapılandırmalar ağacında, gerekli ER yapılandırmalarını seçin.
8. **Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.
9. Seçili sürümü LCS'den mevcut örneğe indirmek için **İçe Aktar**'ı seçin.

    > [!NOTE]
    > Mevcut örnekte bulunan ER yapılandırma sürümleri için **İçe Aktar** düğmesi kullanılamaz.

    [![Yapılandırma deposu sayfası.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> ER ayarlarına bağlı olarak yapılandırmalar içeri aktarıldıktan sonra doğrulanır. Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz. İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir. Daha fazla bilgi için bu makalenin ilgili makaleler listesine göz atın.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
