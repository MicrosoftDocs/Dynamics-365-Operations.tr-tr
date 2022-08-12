---
title: Ambar yönetimi işlemleri için etkinleştirilmiş maddeleri madde varış günlüğü kullanarak kaydetme
description: Bu makale, ambar yönetimi işlemlerini (WMS) kullanırken maddelerin madde varış günlüğü kullanılarak nasıl kaydedileceğini gösteren bir senaryo sunar.
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5241c982675d6b9a9bc9596b8ac9ed2798903287
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066982"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>Ambar yönetimi işlemleri için etkinleştirilmiş maddeleri madde varış günlüğü kullanarak kaydetme

[!include [banner](../../includes/banner.md)]

Bu makale, ambar yönetimi işlemlerini (WMS) kullanırken maddelerin madde varış günlüğü kullanılarak nasıl kaydedileceğini gösteren bir senaryo sunar. Bu genellikle bir teslim alma memuru tarafından yapılır.

## <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Bu makalede belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo aracılığıyla çalışmak için, standart gösteri verilerinin yüklendiği bir sistem kullanıyor olmanız ve başlamadan önce *USMF* hukuk varlığını seçmeniz gerekir.

Bunun yerine, aşağıdaki veriler kullanılabilir olduğu takdirde değerleri kendi verilerinizde değiştirerek bu senaryoya göre çalışabilirsiniz:

- Açık bir satın alma siparişi satırı ile onaylanmış bir satın alma siparişiniz olmalıdır.
- Satırdaki öğenin stoğunun tutulması gerekir Ürün varyantlarını kullanmamalı ve izleme boyutları olmamalıdır.
- Ürün ambar yönetimi işlemi etkin bir depolama boyut grubuyla ilişkilendirilmesi gerekir.
- Kullanılan ambar, WMS için etkinleştirilmelidir ve alım işlemi için kullanılan yerleşimin plakası kontrol edilmiş olmalıdır.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Ambar yönetimini kullanan bir madde varış günlüğü başlığı oluşturma

Aşağıdaki senaryo, ambar yönetimi kullanan bir madde varış günlüğü başlığının nasıl oluşturulacağını gösterir:

1. Sisteminizin, önceki bölümde özetlenen gereksinimleri karşılayan, onaylanmış bir satın alma siparişi içerdiğinden emin olun. Bu senaryoda, *USMF* şirketi, *1001* satıcı hesabı, *51* ambarı ve *M9200* madde numarası için *10 PL* (10 palet) ilgili sipariş satırı bulunan bir satın alma siparişi kullanılmıştır.
1. Kullanacağınız Satın alma siparişi numarasını not edin.
1. **Stok yönetimi \> Yevmiye defteri girişleri \> Madde varışı \> Madde varışı** öğesine gidin.
1. Eylem Bölmesi'nde **Yeni**'yi seçin.
1. **Ambar yönetimi günlüğü oluştur** iletişim kutusu açılır. **Ad** alanında bir günlük adı seçin.
    - *USMF* örnek verilerini kullanıyorsanız, *WHS* öğesini seçin.
    - Kendi verilerinizi kullanıyorsanız, seçtiğiniz günlükte **çekme konumunu denetle**'nin *Hayır* olarak ayarlanmış ve **karantina yönetimi**'nın *Hayır* olarak ayarlanmış olması gerekir.
1. **Referans**'ı *Satın alma emri* olarak ayarlayın.
1. **Hesap numarasını** *1001* olarak ayarlayın.
1. Bu alıştırma için tanımladığınız satın alma siparişinin numarasını **Numara** olarak ayarlayın.

    ![Gelen maddeler günlüğü.](../media/item-arrival-journal-header.png "Gelen maddeler günlüğü")

1. Günlük başlığını oluşturmak için **Tamam**'ı seçin.
1. **Yevmiye defteri satırları** bölümünde **satır ekle**'yi seçin ve aşağıdaki verileri girin:
    - **Öğe numarası** *M9200* olarak ayarlayın. **Tesis**, **Ambar** ve **miktar** 10 palet (her biri 1000) için stok işlemi verilerine dayalı olarak ayarlanır.
    - **Konum**: *001* olarak ayarlanır. Bu belirli konum plakaları izlemez.

    ![Gelen maddeler günlüğü satırı.](../media/item-arrival-journal-line.png "Gelen maddeler günlüğü satırı")

    > [!NOTE]
    > **Tarih** alanı, bu ürünün eldeki miktarın stokta kaydedileceği tarihi belirler.  
    >
    > **Lot kodu** sağlanan bilgilerden hareketle benzersiz şekilde tanımlanabiliyorsa, sistem tarafından doldurulur. Aksi halde, bunu el ile girmeniz gerekir. Bu, bu kaydı belirli bir kaynak belge satırına bağlayan gerekli bir alandır.  

1. Eylem bölmesinde **Doğrula**'yı seçin. Bu günlüğün deftere nakile hazır olup olmadığını denetler. Doğrulama başarısız olursa, günlüğü deftere nakledebilmek için hataları düzeltmeniz gerekir.  
1. **Günlüğü denetle** iletişim kutusu açılır. **Tamam**'ı seçin.
1. İleti çubuğunu inceleyin. İşlemin tamamlandığını belirten bir ileti görünmesi gerekir.  
1. Eylem Bölmesinde **Deftere naklet**'i seçin.
1. **Günlüğü deftere naklet** iletişim kutusu açılır. **Tamam**'ı seçin.
1. İleti çubuğunu inceleyin. İşlemin tamamlandığını belirten bir ileti görünmesi gerekir.
1. Satın alma sipariş satırını güncelleştirmek ve bir ürün girişini deftere nakletmek için eylem bölmesinde **İşlevler > ürün girişi** işlevlerini seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
