---
title: Abonelik Faturalaması Power BI içerikleri
description: Bu makale, Abonelik faturalaması Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: 6cee01eb5b8bb8296b6e7f638b565c999ccc023e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849974"
---
# <a name="subscription-billing-power-bi-content"></a>Abonelik Faturalaması Power BI içerikleri

[!include[banner](../includes/banner.md)]

Bu makale, Abonelik faturalaması Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar. 

## <a name="overview"></a>Genel Bakış

Abonelik fatura Power BI içeriği, abonelik faturalama görevlileri ve yöneticileri için oluşturuldu. Faturalama zamanlamaları için aylık yinelenen gelir (MRR) ve erteleme zamanlamalarına ilişkin azalan bakiye ve şelale bilgileri gibi anahtar abonelik faturalama ölçümleri sağlar. Yinelenen gelir ve gelirin özetini sağlamak için ödeme zamanlamalarında bulunan verileri kullanır ve ertelemeyi yeniden zamanlar.

Power BI içeriğinde, toplam dört analiz raporu sağlayan aşağıdaki üç sekme vardır: 

- **Analizler - MRR** – Bu sekme **Aylık yinelenen faturalama** raporunu ve **Faturalama zamanlaması ayrıntıları** raporunu sağlar.
- **Analitik - Şelale** – Bu sekme **Gelir şelale** raporunu sağlar.
- **Analiz - Azalan bakiye** – Bu sekme **Azalan bakiye** raporunu sağlar.

## <a name="view-data-on-the-analytical-reports"></a>Analitik raporlardaki verileri görüntüle

Analitik raporlardaki verileri görüntülemeden önce, her rapor için raporlama verilerini oluşturan bir periyodik işlem çalıştırmanız gerekir. Raporların gerektirdiği bu veriler doğrudan veritabanında depolanmadığından oluşturulmalıdır. 

1. **Abonelik faturalama \> Yinelenen sözleşme faturalama \> Periyodik görevler \> MRR analitik raporu toplu işleme**'ye gidin ve şu adımları izleyin:

    1. Üç yıldan fazla olmayacak şekilde bir tarih aralığı girin.
    2. İsteğe bağlı: Verileri düzenli olarak yenilemek üzere tekrarlayan bir toplu işlem işi ayarlayın.
    3. **Tamam**'ı seçin.

2. Toplu işlem tamamlandıktan sonra, **Sistem Yönetimi \> Kurulum \> Varlık deposu**'na gidin ve **MRR raporu** toplam ölçümünü yenileyin. 
3. **Abonelik faturalama \> Gelir ve gider ertelemeleri \> Periyodik görevler \> Şelale analitik raporu toplu işleme**'ye gidin ve şu adımları izleyin:

    1. En fazla 26 dönem içeren bir başlangıç ve bitiş tarihi girin. 
    2. Geçmiş dönemlerin tahmini tutarını geçerli dönemde görüntülemek istiyorsanız, **Geçerli dönemdeki tahmin edilen tutarları** **Evet** olarak ayarlayın.
    3. İsteğe bağlı: Verileri düzenli olarak yenilemek üzere tekrarlayan bir toplu işlem işi ayarlayın.
    4. **Tamam**'ı seçin. 

4. Toplu işlem tamamlandıktan sonra, **Sistem Yönetimi \> Kurulum \> Varlık deposu**'na gidin ve **Şelale raporu** toplam ölçümünü yenileyin.
5. **Abonelik faturalama \> Gelir ve gider ertelemeleri \> Periyodik görevler \> Azalan bakiye analitik raporu toplu işleme**'ye gidin ve şu adımları izleyin:

    1. En fazla 26 dönem içeren bir başlangıç ve bitiş tarihi girin. 
    2. Geçmiş dönemlerin tahmini tutarını geçerli dönemde görüntülemek istiyorsanız, **Geçerli dönemdeki tahmin edilen tutarları** **Evet** olarak ayarlayın.
    3. İsteğe bağlı: Verileri düzenli olarak yenilemek üzere tekrarlayan bir toplu işlem işi ayarlayın.
    4. **Tamam**'ı seçin.

6. Toplu işlem tamamlandıktan sonra, **Sistem Yönetimi \> Kurulum \> Varlık deposu**'na gidin ve **Azalan bakiye raporu** toplam ölçümünü yenileyin.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim

Abonelik faturalama Power BI içeriği, **Abonelik faturalama** çalışma alanında gösterilir.
