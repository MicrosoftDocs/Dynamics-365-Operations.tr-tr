---
title: Alacak dekontlarındaki orijinal faturalara başvurular
description: Bu konu, ilgili alacak dekontlarında orijinal fatura numaralarının nasıl ayarlanacağını ve yazdırılacağını açıklamaktadır.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 798e38d7fea53a13d713734dd0521552974176ea
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347846"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Alacak dekontlarındaki orijinal faturalara başvurular

[!include [banner](../includes/banner.md)]


Bazı ülke/bölgelerde, yazdırılan alacak dekontlarının orijinal faturalara referanslar içermesi yasal bir gereksinim vardır. Bu konu, ilgili alacak dekontlarında orijinal fatura numaralarının nasıl ayarlanacağını ve yazdırılacağını açıklamaktadır.

## <a name="prerequisites"></a>Önkoşullar

- **Özellik yönetimi** çalışma alanında, **Satış ve proje faturası raporları için alacak faturalama düzeni**'ni açın. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Gerekli belgelerin yazdırılabilir biçimleri Yazdırma yönetimi'nde konfigüre edilmelidir.

Bu konuda açıklanan işlevsellik aşağıdaki belgeler için geçerlidir:

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]