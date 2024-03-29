---
title: Alacak dekontlarındaki orijinal faturalara başvurular
description: Bu makalede, ilgili alacak dekontlarında orijinal fatura numaralarının nasıl ayarlanacağı ve yazdırılacağı açıklanmaktadır.
author: mrolecki
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: f1f9ca3914aa02cc38ddfe9f8dd88eb7fc88fd4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281250"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Alacak dekontlarındaki orijinal faturalara başvurular

[!include [banner](../includes/banner.md)]


Bazı ülke/bölgelerde, yazdırılan alacak dekontlarının orijinal faturalara referanslar içermesi yasal bir gereksinim vardır. Bu makalede, ilgili alacak dekontlarında orijinal fatura numaralarının nasıl ayarlanacağı ve yazdırılacağı açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

- **Özellik yönetimi** çalışma alanında, **Satış ve proje faturası raporları için alacak faturalama düzeni**'ni açın. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Gerekli belgelerin yazdırılabilir biçimleri Yazdırma yönetimi'nde konfigüre edilmelidir.

Bu makalede açıklanan işlevsellik aşağıdaki belgeler için geçerlidir:

**Alacak hesapları**

- Serbest metinli alacak dekontu
- Müşteri alacak dekontu

**Proje yönetimi ve muhasebe**

- Proje alacak dekontu

## <a name="configure-accounts-receivable-parameters"></a>Alacak hesapları parametrelerini yapılandırma

Orijinal faturalara yapılan referansların ilgili alacak dekontlarına yazdırılıp yazdırılmadığını kontrol eden parametreyi ayarlamak için bu adımları izleyin.

1. **Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin.
2. **Güncelleştirmeler** sekmesinde, **Fatura** hızlı sekmesinde, **Alacak faturalama düzenini satış ve proje fatura raporlarına uygula** seçeneğini **Evet** olarak ayarlayın.

![Alacak hesapları parametrelerini yapılandırma.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Orijinal faturalara referansları tanımlama

Belge türüne göre orijinal faturalara referansları tanımlamak için aşağıdaki yordamları kullanın.

### <a name="free-text-credit-note"></a>Serbest metinli alacak dekontu

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. Yeni bir alacak dekontu oluşturun veya var olan bir alacak dekontunu seçin.
3. Faturayı açın.
4. Eylem Bölmesi'nde, **Fatura** sekmesindeki **İşlevler** grubunda **Alacak faturalaması**'nı seçin.
5. Orijinal faturaya olan referansı girin ve düzeltme nedenini seçin.

![Serbest metin faturası için referans tanımlama.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Müşteri alacak dekontu

1. **Alacak hesapları** \> **Siparişler** \> **Tüm satış siparişleri**'ne gidin.
2. Düzeltilmesi gereken faturalanmış satış siparişini seçin ve açın.
3. Eylem Bölmesi'nde, **Satış** sekmesindeki **Alacak dekontu** grubunda **Alacak dekontu**'nu seçin.
4. Düzeltme nedenini girin. Orijinal faturaya olan referans otomatik olarak kurulur.

![Satış siparişi için referans tanımlama.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Proje alacak dekontu

1. **Proje yönetimi ve muhasebe** \> **Proje faturaları** \> **Proje faturaları**'na gidin.
2. Düzeltilmesi gereken proje faturasını seçin ve açın.
3. Eylem Bölmesi'nde, **Proje faturası** sekmesindeki **İşlevler** grubunda **Alacak dekontu için seçin**'i seçin.
4. **Alacak faturalaması**'nı seçin.
5. Düzeltme nedenini girin. Orijinal faturaya olan referans otomatik olarak kurulur.

![Proje faturası için referans tanımlama.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Alacak dekontlarını yazdırma

Serbest metin, müşteri ve proje alacak dekontlarını yazdırdığınızda, orijinal faturaya referans ve düzeltme sebebini içerecektir.

![Yazdırılmış alacak dekontu.](media/credit-note-FTI.jpg)

> [!NOTE]
> Orijinal faturalara yapılan başvuruların yazdırılacağını varsayarak belgelerin yazdırılabilir biçimlerinin doğru yapılandırılmış olduğundan emin olun.

## <a name="references-to-original-invoices-in-debit-notes"></a>Borç dekontlarında özgün faturalarla ilgili referanslar

Varsayılan olarak, orijinal faturalara yapılan başvurular alacak dekontları için girilebilir. Örneğin, orijinal faturalardaki negatif (azalan) düzeltmeleri yaparken referanslar girebilirsiniz.

Orijinal faturaların pozitif (artan) düzeltmelerini yaptığınızda referans girmek için **Özellik yönetimi** çalışma alanındaki **Borç dekontlarına ait orijinal faturalara başvurular**'ı etkinleştirmelisiniz.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
