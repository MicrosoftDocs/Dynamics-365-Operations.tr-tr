---
title: "SEPA doğrudan hesaptan ödeme talimatı ayarlayın"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8cc0a11109fe5521586ea8abd7c0b97dce2c1591
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA doğrudan hesaptan ödeme talimatı ayarlayın

[!include[banner](../includes/banner.md)]




Tek Euro ödeme alanı (SEPA) otomatik ödemesi, müşterinin alacaklıya imzalı yönerge vermiş olması koşuluyla, alacaklının müşterinin banka hesabından fon toplamak sağlar. Müşterinin imzaladığı yönerge, alacaklının tahsilat yapmasına izin verir ve müşteri bankasına ödemeyi yapması doğrultusunda talimat verir. Bu konu, SEPA otomatik ödeme talimatlarını ayarlama işlemini göstermek için düzenlenmiştir.

## <a name="prerequisites"></a>Önkoşullar
Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.

| Kategori       | Önkoşul                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ülke/bölge | Tüzel kişiliğin birincil adresi aşağıdaki ülkelerden birinde olmalıdır: Avusturya, Belçika, Almanya, İspanya, Fransa, İtalya veya Hollanda. |

1. Otomatik ödeme talimatları için bir numara sırası ayarlama: Her otomatik ödeme talimatının benzersiz bir numarası olmalıdır. **Numara serileri** sayfasını kullanarak otomatik ödeme talimatları için bir numara sırası oluşturun. **Alacak hesapları parametreleri** sayfasında bu tanımlayıcıyı otomatik ödeme talimatına bir numara serisi atamak için kullanın.

2. Otomatik ödeme talimatları için Alacak hesapları parametrelerini ayarlama: Otomatik ödeme talimatlarına ilişkin parametreleri ayarlamak için **Alacak hesapları parametreleri** sayfasını kullanın. Parametreleri ayarlamak için **Hesaptan ödeme** sekmesinde, varsayılan parametreleri gerekli şekilde değiştirin. Ardından **Numara serileri** sekmesinde, **Hesaptan ödeme talimatı kodu** alanını daha önce ayarladığınız numara serisiyle güncelleştirin.

3. Otomatik ödeme talimatları için bir ödeme yöntemi ayarlama: Otomatik ödeme talimatları için bir yöntemi ayarlamanız gerekir. Hesaptan ödemeler oluşturmak için faturaları sorgulamak için bu ödeme yöntemi kullanın. **Ödeme yöntemleri** sayfasını ödeme yöntemini ayarlamak için kullanın. Hesaptan ödeme talimatları için bir ödeme yöntemi ayarlamak için, ödeme yöntemi için aşağıdaki bu ek adımları takip etmelisiniz:

-   **Ödeme türü** alaninda, **Elektronik ödeme**'yi seçin.
-   İsteğe bağlı: Her müşterinizin birden fazla talimatı olacağını düşünüyorsanız **Dönem** alanında **Fatura**'yı seçin. Her fatura için ayrı bir ödeme oluşturulur ve her bir ödeme, fatura için belirtilen talimatı kullanır.
-   **Talimat gerektirin** seçeneğini otomatik ödeme talimatlarını kullanarak ödeme oluşturmak için seçin. **Talimat gerektirin** seçeneği yalnızca **Elektronik ödeme** içinde **Ödeme türü** alanını seçerseniz kullanılabilir.

Ayrıca bkz. [Otomatik ödemeye genel bakış](sepa-direct-debit-overview.md) 


