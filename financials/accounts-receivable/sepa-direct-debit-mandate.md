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
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>SEPA doğrudan hesaptan ödeme talimatı ayarlayın



Tek Euro ödeme alanı (SEPA) otomatik ödemesi, müşterinin alacaklıya imzalı yönerge vermiş olması koşuluyla, alacaklının müşterinin banka hesabından fon toplamak sağlar. Müşterinin imzaladığı yönerge, alacaklının tahsilat yapmasına izin verir ve müşteri bankasına ödemeyi yapması doğrultusunda talimat verir. Bu konuda SEPA doğrudan borç mandates ayarlama işlemi göstermek için düzenlenmiştir.

## <a name="prerequisites"></a>Önkoşullar
Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.

| Kategori       | Önkoşul                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ülke/bölge | Tüzel kişiliğin birincil adresi aşağıdaki ülkelerden birinde olmalıdır: Avusturya, Belçika, Almanya, İspanya, Fransa, İtalya veya Hollanda. |

1. Doğrudan borç mandates için bir numara serisi ayarlamak her hesaptan zorunluluğuna benzersiz bir numara olması gerekir. **Numara serileri** sayfasını kullanarak otomatik ödeme talimatları için bir numara sırası oluşturun. **Alacak hesapları parametreleri** sayfasında bu tanımlayıcıyı otomatik ödeme talimatına bir numara serisi atamak için kullanın.

2. Doğrudan borç mandates kullanmak için Alacak hesapları parametrelerini ayarlamak **Accounts receivable parameters** hesaptan mandates parametrelerini ayarlamak için sayfa. Parametreleri, on ayarlamak için **doğrudan borç** sekmesinde, varsayılan parametreleri gerekli şekilde değiştirin. Ardından üzerinde **Number sequences** sekmesinde, güncelleştirme **doğrudan borç zorunluluğuna kimliği** ile daha önce ayarladığınız numara serisi alanından.

3. Doğrudan borç, zorunlu kılar için bir ödeme yöntemi ayarlamak bir ödeme yöntemi doğrudan borç mandates için ayarlamanız gerekir. Hesaptan ödemeler oluşturmak için faturaları sorgulamak için bu ödeme yöntemi kullanın. **Ödeme yöntemleri** sayfasını ödeme yöntemini ayarlamak için kullanın. Hesaptan ödeme talimatları için bir ödeme yöntemi ayarlamak için, ödeme yöntemi için aşağıdaki bu ek adımları takip etmelisiniz:

-   **Ödeme türü** alaninda, **Elektronik ödeme**'yi seçin.
-   İsteğe bağlı: her biri için müşterilerinize düşünüyorsanız çok, buna zorunlu kılar **süre** alanında seçin **fatura**. Her fatura için ayrı bir ödeme oluşturulur ve her bir ödeme için fatura belirtilen zorunluluğuna kullanır.
-   **Talimat gerektirin** seçeneğini otomatik ödeme talimatlarını kullanarak ödeme oluşturmak için seçin. **Talimat gerektirin** seçeneği yalnızca **Elektronik ödeme** içinde **Ödeme türü** alanını seçerseniz kullanılabilir.

Ayrıca bkz: [Talimatlı genel bakış](sepa-direct-debit-overview.md) 

