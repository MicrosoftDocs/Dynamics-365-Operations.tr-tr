---
title: Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir
description: Bu konu, genel amaçlı yapılandırma havuzundan elektronik raporlama (ER) yapılandırmalarının nasıl indirileceğini açıklamaktadır.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 53d01756d803a0ebc9eb366deded4bf3bef3b1f6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351758"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir

[!include [banner](../includes/banner.md)]

Bu konu, genel amaçlı yapılandırma havuzundan [elektronik raporlama (ER) yapılandırmalarının](general-electronic-reporting.md#Configuration) nasıl indirileceğini açıklamaktadır. Daha fazla bilgi için, bkz [Microsoft Dynamics 365 for Finance and Operations - Regulatory services yapılandırma hizmeti](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Yapılandırmaların havuzu açın

1. Aşağıdaki rollerden birini kullanarak Dynamics 365 Finance uygulamada oturum açın:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

2. **Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.
3. **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** kutucuğunu seçin.
3. **Microsoft** kutucuğunda, **Depolar**'a tıklayın.

    ![Elektronik raporlama çalışma alanı.](./media/er-download-configurations-global-repo-er-workspace.png)

4. **Yapılandırma depoları** sayfasında, kılavuz içerisinde, mevcut **Genel** türünün deposunu seçin. Bu depo kılavuzda görünmüyorsa, aşağıdaki adımları izleyin:

    1. Yeni bir depo eklemek için **Ekle**'ye tıklayın.
    2. Havuz türü olarak **Global** 'i seçin ve sonra **Havuz oluştur** 'u seçin .
    3. İstenirse, yetkilendirme yönergelerini izleyin.
    4. Havuz için bir ad ve açıklama girin ve sonra yeni havuz girişini onaylamak için **Tamam** 'ı seçin.
    5. Kılavuzda **Global** türündeki yeni depoyu seçin.

5. Seçilmiş depo için ER yapılandırmalarını görüntülemek için **Aç**'a tıklayın.

    ![Yapılandırma havuzu sayfası.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Tekli yapılandırmasını içe aktarma

1. **Konfigürasyon depoları** sayfasında, yapılandırmalar ağacında, istediğiniz er yapılandırmasını seçin.
2. **Sürümler** FastTab üzerinde, seçili ER yapılandırmasının gerekli sürümünü seçin.
3. Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.

    > [!NOTE]
    > Mevcut Finance örnekte bulunan ER yapılandırma sürümleri için **İçe Aktar** düğmesi kullanılamaz.

    ![Yapılandırma deposu sayfası.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Filtreli yapılandırmasını içe aktarma

1. **Konfigürasyon depoları** sayfasında, yapılandırmalar ağacında, **Filtre** hızlı sekmesini genişletin.
2. **Etiketler** kılavuzunda, gerekli tüm etiketleri ekleyin.
3. **Ülke/bölge uygulanabilirlik** alanında, ilgili ülke/bölge kodlarını seçin ve **Filtre Uygula**'yı seçin.

    > [!NOTE]
    > **Konfigürasyonlar** Hızlı sekmesi, belirtilen seçim koşullarını karşılayan tüm konfigürasyonları gösterir.

4. Filtre uygulanan konfigürasyonları Global depodan geçerli örneğe indirmek için **konfigürasyonlar** hızlı sekmesinde **içe aktar**'ı seçin.
5. **Konfigürasyonlar** hızlı sekmesinde, belirtilen seçim koşullarını temizlemek için **filtreyi Sıfırla**'yı seçin.

    ![Yapılandırma deposu sayfası.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> ER ayarlarına bağlı olarak yapılandırmalar içeri aktarıldıktan sonra doğrulanır. Bulunan tutarsızlık sorunları hakkında haberdar edileceksiniz. İçe aktarılmış yapılandırma sürümünü kullanmadan önce bu sorunları çözümlemeniz gerekir. Daha fazla bilgi için bu konunun ilgili kaynaklar listesine göz atın.

> [!NOTE]
> ER konfigürasyonları diğer konfigürasyonlara bağlı olarak konfigüre edilebilir. Bu nedenle, seçili konfigürasyonla birlikte, diğer yapılandırmalar otomatik olarak içe aktarılabilir. Konfigürasyon bağımlılıkları hakkında daha fazla bilgi için, [diğer bileşenlerde ER yapılandırmalarının bağımlılığını tanımlama konusuna](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) bakın.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]