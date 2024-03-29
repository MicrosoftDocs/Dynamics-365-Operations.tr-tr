---
title: Mizan mali raporları
description: Bu makalede, mizanlar için varsayılan raporlar açıklanmaktadır. Ayrıca, bu raporlarla ilgili yapı taşları ve raporların iş gereksinimlerinize uyacak şekilde nasıl değiştirileceği açıklanmaktadır.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: kfend
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26d2ec261720499fc309a5fb850de2cb796bd8b
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802620"
---
# <a name="trial-balance-financial-reports"></a>Mizan mali raporları

[!include [banner](../includes/banner.md)]

Bu makalede, mizanlar için varsayılan raporlar açıklanmaktadır. Ayrıca, bu raporlarla ilgili yapı taşları ve raporların iş gereksinimlerinize uyacak şekilde nasıl değiştirileceği açıklanmaktadır. 

## <a name="default-trial-balance-reports"></a>Varsayılan mizan raporları

Mali raporlama için üç mizan raporu kullanılabilir.

| Varsayılan rapor                                 | Ne yapar                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| Ayrıntılı Mizan - Varsayılan               | Borç ve alacak bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve hareket tarihi, fiş ve günlük açıklamasıyla birlikte bunların net değerini gösterir.                  |
| Özet Mizan – Varsayılan                | Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve net farklarıyla birlikte borç ve alacak bakiyelerini gösterir.                                        |
| Özet Mizan Yıl Yıl – Varsayılan | Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve bu yıl ve geçen yıl için net farklarıyla birlikte borç ve alacak bakiyelerini gösterir. |

## <a name="building-blocks"></a>Yapı taşları
Mizan mali raporları aşağıdaki yapı taşlarını kullanır.

| Varsayılan rapor                                 | Satır tanımı          | Sütun tanımı                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Ayrıntılı Mizan - Varsayılan               | Mizan - Varsayılan | Ayrıntılı Mizan - Varsayılan               |
| Özet Mizan – Varsayılan                | Mizan - Varsayılan | Özet Mizan - Varsayılan                |
| Özet Mizan Yıl Yıl – Varsayılan | Mizan - Varsayılan | Özet Mizan Yıl Yıl - Varsayılan |

> [!NOTE] 
> Mali raporlamada **Mizan** raporunu çalıştırırken **Tutarsız satırları görüntüle** ve **Ayarlar** sekmesinde **etkin satır olmayan raporları görüntüle** onay kutularını seçtiğinizden emin olun.

### <a name="row-definition"></a>Satır tanımı

Satır tanımı, Mizan – Varsayılan, tüm ana hesaplardan veri çeken tek bir satır içerir. Bu nedenle, herhangi biri hiçbir değişiklik yapmasına gerek kalmadan rapor oluşturabilir. Raporu görüntülediğinizde, her bir hesap hakkında ayrıntılı bilgileri görmek için tek bir satıra bakarsınız. Satır tanımını daha fazla ayrıntı içerecek şekilde değiştirebilirsiniz. Mizan – Varsayılan satır tanımını tüm hesaplar için satırları içerecek şekilde değiştirmek için, bu adımları takip edin.

1.  **Düzenle**'ye ve ardından **Boyutlardan satır ekle**'ye tıklayın. **Boyutlardan satır ekle** komutu, satır tanımınızda olmasını istediğiniz boyutları seçmenize izin verir. Bu satır tanımı için **Ana hesap** kullanılacaktır.
2.  **Ana hesabın** tüm & işaretlerini içerdiğinden emin olun ve ardından **Tamam**'a tıklayın.

Satır tanımı şimdi varsayılan tüzel kişiliğiniz için tüm ana hesapları içermektedir.

### <a name="column-definition"></a>Sütun tanımı

Her bir mizan raporunu farklı bir sütun tanımı kullanır. Bu sütun tanımları, farklı ayrıntı ve mali veri düzeyleri sunmak üzere farklı türlerde sütunlar içerir.

-   **Ayrıntılı Mizan – Varsayılan sütun türleri:**
    -   **DESC** – Satır tanımının açıklaması
    -   **ACCT** – Hesap kodları
    -   **ATTR (3)** – Öznitelikler:
        -   Hareket Tarihi
        -   Fiş
        -   Günlük Tanımı
    -   **FD** – Yalnızca borçları içeren mali veriler
    -   **FD** – Yalnızca alacakları içeren mali veriler
    -   **CALC** – Net fark
-   **Özet Mizan – Varsayılan sütun türleri:**
    -   **ACCT** – Hesap kodları
    -   **DESC** – Satır tanımının açıklaması
    -   **ATTR** – Öznitelik:
        -   Fiş
    -   **FD** – Başlangıç bakiyesi mali verileri
    -   **FD** – Yalnızca borçları içeren mali veriler
    -   **FD** – Yalnızca alacakları içeren mali veriler
    -   **CALC** – Net fark
    -   **CALC** – Kapanış bakiyesi
-   **Özet Mizan Yıl Yıl – Varsayılan:**
    -   **ACCT** – Hesap kodları
    -   **DESC** – Satır tanımının açıklaması
    -   **ATTR** – Bir öznitelik
        -   Fiş
    -   **FD** – Mevcut yıl için başlangıç bakiyesi mali verileri
    -   **FD** – Geçerli yıl için yalnızca borçları içeren mali veriler
    -   **FD** – Geçerli yıl için yalnızca alacakları içeren mali veriler
    -   **CALC** – Net fark
    -   **CALC** – Kapanış bakiyesi
    -   **FD** – Geçen yıl için yalnızca borçları içeren mali veriler
    -   **FD** – Geçen yıl için yalnızca alacakları içeren mali veriler

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlamaya genel bakış](financial-reporting-getting-started.md)

[Mali raporları görüntüleme](view-financial-reports.md)

[Dynamics Mali Raporlama Blogu](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
