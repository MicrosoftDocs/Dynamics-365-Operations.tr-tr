---
title: Stok eskime raporu depolama
description: Bu makalede, bir Stok yaşlandırma raporu çalıştırmanıza ve çıktının form ve grafik olarak kullanılabilmesini sağlamanıza olanak tanıyan işlevler açıklanmaktadır.
author: JennySong-SH
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d810ec90c85f2f7758ec01ef4b24611e026cc80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875640"
---
# <a name="inventory-aging-report-storage"></a>Stok eskime raporu depolama

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'ta, bir **Stok yaşlandırma raporu depolama** raporu çalıştırabilir ve çıktının form ve grafik olarak kullanılabilmesini sağlayabilirsiniz. Formda, sütunlar ve toplam bakiyeler yapılandırılan düzene göre dinamik olarak ayarlanır. Grafik, filtrelemeyi destekleyen ve ayrıntılara inmenizi sağlayan görsel bir genel bakış sunar. Ek olarak, **Stok yaşlandırma raporu** olarak adlandırılan bir veri varlığı, **Stok yaşlandırma raporu depolama** raporunun sonuçlarını Microsoft Excel dosyası veya PDF dosyası gibi bir biçimde dışa aktarmanıza olanak tanır.

Bu **Stok yaşlandırma raporu depolama** raporunu çalıştırma yöntemi, çıktının çok fazla satır içerdiği durumlarda yararlıdır. Örneğin, 50.000 madde ve ambar olarak oluşturulan 300 mağazanız varsa ve ürüne, tesise ve ambara göre stok yaşlandırma yapmak istiyorsanız çıktı çok fazla satır içerir.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Stok değeri depolama raporu özelliğini etkinleştirme

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. Burada, özellik şu şekilde listelenmiştir:

- **Modül**: Maliyet yönetimi
- **Özellik adı** - Stok yaşlandırma raporu depolama

## <a name="run-an-inventory-aging-report-storage"></a>Stok yaşlandırma raporu depolaması çalıştırma

1. **Maliyet yönetimi \> Sorgular ve raporlar \> Stok yaşlandırma raporu depolama alanı**'na gidin.
1. **Yeni**'yi seçin.
1. **İşlem Tanımlayıcısı – Ad** alanına rapor için benzersiz bir ad girin.
1. **Kimlik – Kod** raporunu seçin ve gerektiği şekilde filtreleyin.

    Rapor yürütme her zaman toplu işte yapılır.

1. Toplu iş tamamlandıktan sonra çıktı **Stok yaşlandırma raporu depolama alanı** sayfasında gösterilir.
1. Çıktıyı geleneksel ızgara düzenine sahip bir form olarak görüntülemek için **Ayrıntıları görüntüle**'yi seçin. Çıktıyı toplam grafiği olarak görüntülemek için **Grafiği görüntüle**'yi seçin.

    > [!NOTE]
    > Form, rapor düzeninde tanımlanan alt toplamları içermez.

**Stok yaşlandırma raporu** veri varlığı, **İşlem Tanımlayıcısı – Ad** alanı için bir filtre uygulayarak **Stok yaşlandırma raporu depolama** raporunun çıktısını Veri yönetiminin desteklediği herhangi bir biçimde dışa aktarmanıza olanak tanır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]