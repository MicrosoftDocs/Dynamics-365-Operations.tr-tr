---
title: "Lifecycle Services&quot;dan Elektronik raporlama yapılandırmalarını karşıdan yükle"
description: "Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services&quot;dan (LCS) indirmeyi açıklar."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1e73cd38c33d88feaba825abb64721bc332a4d6e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle

[!include[banner](../includes/banner.md)]


Bu konu, Elektronik raporlama (ER) yapılandırmalarını Microsoft Dynamics Lifecycle Services'dan (LCS) indirmeyi açıklar.

Bu eğitim size Elektronik Raporlama (ER) yapılandırmalarının en yeni sürümlerinin, Microsoft Dynamics Lifecycle Services'dan (LCS) indirme sürecini öğretir.

1.  Aşağıdaki rollerden birini kullanarak Dynamics 365 for Operations'da oturum açın:
    -   Elektronik raporlama geliştirici
    -   Elektronik raporlama işlev danışmanı
    -   Sistem yöneticisi

2.  **Organizasyon yönetimi** &gt; **Elektronik raporlama**'ya gidin.
3.  **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.
4.  **Microsoft** kutucuğunda, **Depolar**'a tıklayın. [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  **Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin. Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:
    1.  Yeni bir depo eklemek için **Ekle**'ye tıklayın.
    2.  Havuz türü olarak **LCS**'yi seçin.
    3.  **Depo oluştur**'a tıklayın.
    4. İstenirse, yetkilendirme yönergelerini izleyin.
    5.  Depo için bir ad ve açıklama girin.
    6.  Yeni depo girişini onaylamak için **Tamam**'a tıklayın.
    7.  Kılavuzda **LCS** türündeki yeni depoyu seçin.

6.  Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın. [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Sol bölmedeki yapılandırmalar ağacında, gereksinim duyduğunuz ER yapılandırmalarını seçin.
8.  **Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.
9.  Seçili sürümü LCS'den mevcut Dynamics 365 for Operations örneğine indirmek için **İçe Aktarma**'ya tıklayın. **Not:** Mevcut Dynamics 365 for Operations örneğinde bulunan ER yapılandırma sürümleri için **İçe Aktarma** düğmesi kullanılamaz. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Not:** ER ayarlarına bağlı olarak, yapılandırmalar içe aktarıldıktan sonra doğrulanır. Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz. İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir. Daha fazla bilgi için bu konunun ilgili makaleleri listesine göz atın.

<a name="see-also"></a>Ayrıca bkz.
--------

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)




