---
title: "Lifecycle Services&quot;dan Elektronik raporlama yapılandırmalarını karşıdan yükle"
description: "Bu konu elektronik Raporlama (ER) yapılandırmaları Microsoft Dynamics ömrü Hizmetleri (LCS) dan karşıdan yükleme açıklar."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle

Bu konu elektronik Raporlama (ER) yapılandırmaları Microsoft Dynamics ömrü Hizmetleri (LCS) dan karşıdan yükleme açıklar.

Bu eğitim size Elektronik Raporlama (ER) yapılandırmalarının en yeni sürümlerinin, Microsoft Dynamics Lifecycle Services'dan (LCS) indirme sürecini öğretir.

1.  Aşağıdaki rollerden birini kullanarak Dynamics 365 for Operations'da oturum açın:
    -   Elektronik raporlama geliştirici
    -   Elektronik raporlama işlev danışmanı
    -   Sistem yöneticisi

2.  Git **kuruluş yönetim**&gt;**elektronik raporlama**.
3.  **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.
4.  **Microsoft** kutucuğunda, **Depolar**'a tıklayın. [![Update-er-from-LCS-for-MS-Open-MS-repositories-List](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  **Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **LCS** türünün deposunu seçin. Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:
    1.  Yeni bir depo eklemek için **Ekle**'ye tıklayın.
    2.  Havuz türü olarak **LCS**'yi seçin.
    3.  **Depo oluştur**'a tıklayın.
    4.  Depo için bir ad ve açıklama girin.
    5.  Yeni depo girişini onaylamak için **Tamam**'a tıklayın.
    6.  Kılavuzda **LCS** türündeki yeni depoyu seçin.

6.  Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın. [![Update-er-from-LCS-for-MS-Make-LCS-Repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Sol bölmedeki yapılandırmalar ağacında, gereksinim duyduğunuz ER yapılandırmalarını seçin.
8.  **Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.
9.  Seçili sürümü LCS'den mevcut Dynamics 365 for Operations örneğine indirmek için **İçe Aktarma**'ya tıklayın. **Not:** Mevcut Dynamics 365 for Operations örneğinde bulunan ER yapılandırma sürümleri için **İçe Aktarma** düğmesi kullanılamaz. [![Update-er-from-LCS-for-MS-download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Not:** ER ayarlarına bağlı olarak, yapılandırmalar içe aktarıldıktan sonra doğrulanır. Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz. İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir. Bu konu için ilgili makalelerin listesini daha fazla bilgi için bkz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)


