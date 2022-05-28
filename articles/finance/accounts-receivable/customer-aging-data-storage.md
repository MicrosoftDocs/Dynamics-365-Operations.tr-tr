---
title: Müşteri yaşlandırma veri depolaması
description: Bu konu, müşteri yaşlandırma verileri için harici depolama kullanma sürecini açıklamaktadır. Çıktıyı, harici bir sisteme dışa aktarmak üzere kullanılabilir hale getirmek için Müşteri yaşlandırma verileri depolama sürecini çalıştırabilirsiniz.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1af4b4cbf503369565ee64ad8889ee9e59a92b3f
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735535"
---
# <a name="customer-aging-data-storage"></a>Müşteri yaşlandırma veri depolaması

[!include [banner](../includes/banner.md)]

Bu konu, müşteri yaşlandırma verileri için harici depolama kullanma sürecini açıklamaktadır. Microsoft Dynamics 365 Finance'te çıktıyı, harici bir sisteme dışa aktarmak üzere kullanılabilir hale getirmek için **Müşteri yaşlandırma verileri depolama** sürecini çalıştırabilirsiniz. İşlemi çalıştırdığınızda, sistemde kullanılabilen aynı yaşlandırma raporu seçenekleri harici sistemler tarafından kullanılabilir. Ayrıntılar her zaman dışa aktarılan verilere dahil edilir.

Çıktıda birçok müşteri ve/veya birçok hareket bulunduğu durumlarda, Müşteri yaşlandırma verilerinin bir harici sistem tarafından kullanılabilmesini sağlamak yararlı olabilir. Varolan **Müşteri yaşlandırma** raporu, yazdırılmak üzere çok fazla veri içerdiği için zaman aşımına uğrar; bu özellik aynı verileri elde etmek için alternatif bir yol sağlar.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Müşteri yaşlandırma verileri depolama özelliğini etkinleştir

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için özellik yönetimi ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** Alacak ve tahsilatlar
- **Özellik adı:** Müşteri yaşlandırma verileri depolama

## <a name="run-the-customer-aging-data-storage-process"></a>Müşteri yaşlandırma verileri depolama işlemini çalıştırın

1. **Kredi ve Tahsilatlar \> Sorgular ve raporlar \> Müşteri \> Müşteri yaşlandırma verileri depolaması** seçeneğine gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanına, işlem için bir ad girin.
4. Geri kalan parametreleri gereksinim duyduğunuz gibi ayarlayın.

    > [!NOTE]
    > Hareket ayrıntıları her zaman dahil edilir ve işlem her zaman bir toplu işte yapılır.

5. **Tamam**'ı seçin.
6. **İşlem durumu** değeriyle birlikte gösterilen **Toplu iş adını** ve **Toplu iş çalıştırma zamanı** değerlerini görmek için **Müşteri yaşlandırma verileri depolama** sayfasını yenileyin. Toplu işlem tamamlandığında, **İşlem durumu** alanı **Tamamlandı** olarak ayarlanır ve **Yaşlandırma satırları sayısı** alanı ayarlanır. Toplu işlem yinelense, **İşlem durumu** alanı **Bekleniyor** olarak ayarlanır.
7. Toplu iş için eklenen filtreleri gözden geçirmek üzere, **Yaşlandırma satırı sayısı** alanının yanındaki **Filtre** düğmesini seçin.

**Müşteri yaşlandırma verileri depolama** sayfası sonuçları içermiyor. Ancak, **Müşteri yaşlandırma verileri depolama** verileri varlığı, çıktıyı veri yönetiminin desteklediği herhangi bir biçime vermenize olanak sağlar.

> [!NOTE]
> Dışa aktarma yapmadan önce, dışa aktarılan sonuçları en son yaşlandırma ile sınırlandırmak için bir filtre ekleyin. Örneğin, en son toplu iş çalışmasını döndürmek için aşağıdaki ölçütleri ekleyin:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> Alternatif olarak, mevcut kullanıcı için en son toplu iş çalışmasını döndürmek için aşağıdaki ölçütleri ekleyin:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
