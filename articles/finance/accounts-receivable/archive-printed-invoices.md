---
title: Yazılı müşteri faturalarını karma numaralarla arşivleme
description: Bu makalede, basılı müşteri faturalarını karma numaralarla kaydetmek için arşivlemenin nasıl etkinleştirileceği açıklanmaktadır.
author: mrolecki
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.custom: 539093
ms.search.form: ''
ms.openlocfilehash: 4c9bd7ead1615a4e6b0e8e672e858312ba518b56
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291684"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Yazılı müşteri faturalarını karma numaralarla arşivleme

[!include [banner](../includes/banner.md)]

Bazı ülkelerde, Hesaplanmış karma numaraların sistemde bazı belgelerin çıktılarıyla birlikte kaydedilmesi için yasal bir gereksinim vardır. Karma numaralar, yetkililere rapor verirken ve denetimler sırasında kullanılabilir.

Bu makalede, basılı müşteri faturalarını karma numaralarla kaydetmek için arşivlemenin nasıl yapılandırılacağı açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

- **Özellik Yönetimi** çalışma alanında, **yazdırılmış müşteri faturalarını karma numaralarla arşivle** özelliğini etkinleştirin. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Gerekli belgelerin yazdırılabilir biçimleri **Yazdırma yönetimi**'nde yapılandırın.

Bu işlev aşağıdaki belgeler için geçerlidir.

**Alacak hesapları**
- Müşteri faturası
- Müşteri alacak dekontu
- Dekont / Serbest metin faturası
- Serbest metinli alacak dekontu

**Proje yönetimi ve muhasebe**
- Proje faturası
- Proje alacak dekontu

## <a name="configure-customer-master-data"></a>Müşteri asıl verisini yapılandırma
Müşteri verilerini yapılandırmak ve yazdırılan faturaları otomatik olarak ek olarak kaydetme özelliğini açmak için aşağıdaki adımları tamamlayın.

1. **Alacak hesapları** > **Tüm müşteriler**'e gidin. 
2. Müşteri seçin ve **Fatura ve teslimat** hızlı sekmesinde, **E-FATURA** bölümünde **E-Fatura eki** alanında **Evet**'i seçin.

## <a name="print-invoices"></a>Faturaları yazdır
Önceki yordamda yapılandırılan, müşteriye ait serbest metin, müşteri, proje faturası veya alacak dekontunu deftere nakledebilir ve yazdırabilirsiniz.

Yazdırılan fatura için **ekler** sayfasını açın. **Ek** hızlı sekmesinde, **Ek ayrıntılar** alan grubunda, **belge karması numarası** alanında, yazdırılan fatura için hesaplanan kaydedilmiş karma numarayı bulun.

![Ek karma numarası.](media/attach-hash-num.jpg)

