---
title: Invoice Capture çözümü panosu
description: Bu makalede, Invoice Capture çözümü panosu açıklanmaktadır.
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690139"
---
# <a name="invoice-capture-solution-dashboard"></a>Invoice Capture çözümü panosu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Invoice Capture'da pano, içe aktarılan faturalara genel bakış sağlayan grafikler içerir. Bu grafikler, Borç Hesapları (AP) yöneticisinin fatura oluşturma işleminin performansını analiz etmesine yardımcı olabilir. AP yöneticisi, fatura oluşturma işleminin durumunu görüntüleyebilir ve ayrıca farklı filtreler uygulayarak ayrıntıları görüntüleyebilir.

## <a name="available-charts"></a>Mevcut grafikler

Panoda aşağıdaki grafikler bulunur:

- **Duruma göre tüm yakalanan faturalar**: Bu grafikte, yakalanan fatura için aşağıdaki durumlar gösterilir. Durum seçildiğinde, kullanıcılar ayrıntılı listedeki yakalanan faturaları filtreleyebilir.

    - Yakalandı
    - Tamamla
    - İncelemede
    - Kullanım dışı bırakıldı

- **Toplam yakalanan fatura hacmi**: Bu grafikte, döneme göre yakalanan faturaların sayısı gösterilir. Kullanıcılar, açılır listeyi kullanarak dönemi değiştirebilir.
- **En iyi satıcılardan yakalanan faturalar**: Bu grafikte, satıcıya göre faturaların toplam sayısı gösterilir. En çok faturaya sahip satıcılar en üstte görüntülenir.
- **Özel durumlara sahip bir faturanın tamamlanacağı gün sayısı**: Bu grafikte, bir faturanın yakalanması için gereken ortalama gün sayısı gösterilir. Bu bilgiler, el ile müdahale gerektiğinde AP yöneticisinin bir faturayı işleme süresini analiz etmesine yardımcı olabilir. Yukarı doğru bir eğilim varsa kullanıcılar, gereken gün sayısını azaltmaya yardımcı olmak için işlem ayrıntılarını gözden geçirebilir ve ayarları düzeltebilir.
- **Bekleme süresine göre tamamlanmamış faturalar**: Bu grafikte, kurumsal kaynak planlama (ERP) sisteminde yakalanan bir faturanın oluşturulmadığı gün sayısı gösterilir. Bekleme günü sayısı arttıkça fatura oluşturma işlemi de o kadar uzar. AP yöneticisi, ayrıntılı yakalanan faturalarda detaya gidebilir ve ERP sisteminde faturalar oluşturabilir.
