---
title: Banka yönetimi çalışma alanı
description: Bu makalede, Banka yönetimi çalışma alanı hakkında bilgiler sağlanmaktadır. Bu çalışma alanı, şirket banka hesaplarıyla ilgili bilgileri gösterir.
author: angelad116
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f9880928281e704edcd24a75f99d4562761b7c82
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151566"
---
# <a name="bank-management-workspace"></a>Banka yönetimi çalışma alanı

[!include [banner](../includes/banner.md)]

**Banka yönetimi** çalışma alanı, şirket banka hesaplarıyla ilgili bilgileri gösterir. Bu çalışma alanı bir **Özet** görünümü ve bir **Analiz** sayfası içerir. Bu **Özet** görünümü, özet kutucuklarını, banka hesap bilgisini, bir bakiye grafiğini ve ilgili bilgileri gösterir. **Analiz** sayfası, Microsoft Power BI yeteneklerini, banka hesabı bakiyeleriyle ilgili görselleri göstermek için kullanır.

## <a name="summary-view"></a>Özet görünümü

### <a name="summary"></a>Özet

**Özet** bölümündeki kutucuklar, banka hesaplarınıza bir genel bakış sunar ve en sık kullanmanız gereken sayfalara hızlı erişim sağlar. Banka mutabakatı bilgisi, Gelişmiş banka mutabakatı işlevine özeldir. Bilgi, yalnızca **Gelişmiş banka mutabakatı** seçeneğinin **Banka hesabı** sayfasında **Evet** olarak ayarlanmış banka hesapları için dahildir. **Özet** bölümünden, elektronik banka dosyalarını, tüm tüzel varlıklar üzerindeki banka hesaplar için içe aktarabilirsiniz.

### <a name="bank-accounts"></a>Banka hesapları

Tüzel varlıktaki her bir banka hesabı, **Banka hesapları** bölümündeki bir kart ile temsil edilir. Mevcut bakiye gösterilir ve özet bakiye tutarını oluşturan hareketlerin ayrıntısına inebilirsiniz. **Köprülü hareketler** tutarı, özet tutarını oluşturan hareketlerin ayrıntısına inmenize de olanak sağlar. Köprülü hareketler, köprü işlevi kullanarak nakledilen, ancak henüz temizlenmemiş olan tüm bekleyen hareketlerdir. **Bekleyen bakiye** tutarı, geçerli bakiye eksi köprülü veya bekleyen hareketlerdir.

Kart, ayrıca banka hesabında en son ne zaman mutabakat sağlandığını da gösterir Bu bilgi, yalnızca banka hesabı için Gelişmiş banka mutabakatı etkinleştirilmişse gösterilir.

### <a name="balance"></a>Bilanço

**Bakiye** grafiği, **Banka hesapları** bölümünde seçili banka hesabı için tarihi bakiye bilgisini veya tüzel varlıktaki tüm banka hesapları için geçmiş bakiye bilgisini gösterir. Bu bilgiler, çeşitli dönemler için kullanılabilir: geçerli hafta, geçerli ay, geçerli yıl, son beş yıl ve tüm dönemler (banka hesabının tam geçmişi). 

Tek bir banka hesabı için **Bakiye** grafiğini görüntülüyorsanız, tarihi bakiye banka hesabı para biriminde gösterilir. Tüzel varlıktaki tüm banka hesaplarını görüntülüyorsanız, geçmiş bakiyeler muhasebe para birimi cinsinden gösterilir.

Verinin en son ne zaman güncelleştirilmiş olduğu, grafiğin üstünde görüntülenir. Veriyi ihtiyaç duyduğunuz gibi güncelleştirebilirsiniz.

### <a name="related-information"></a>İlgili bilgiler

**İlgili bilgi** bölümünde, **Genel günlük** sayfasını banka transferlerini görüntülemek için açabilirsiniz. **Banka hareketleri** ve **Köprülü hareketler** sayfalarını da hızlıca açabilirsiniz.

## <a name="analytics-view"></a>Analiz görünümü

**Analizler** sayfası, geçerli şirketteki banka hesapları hakkında önemli ölçümler sağlar. Aşağıdaki görselleştirmeler bir sayfada mevcuttur:

-   Sistem para biriminden toplam banka bakiyesi
-   Tüzel kişiliğe göre bakiye
-   Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması
-   Banka hesabına göre bakiye
-   Döviz cinsinden bakiye

Tüm şirket arasındaki banka analizlerini **Nakit genel bakışı – tüm şirketler** çalışma alanından görebilirsiniz. Daha fazla bilgi için bkz. [Nakde genel bakış Power BI içeriği](Cash-Overview-Power-BI-content.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
