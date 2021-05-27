---
title: Fiziksel güncelleştirmede seçeneği devre dışıyken toplu iş numaraları için çoklu stok hareketleri
description: Toplu iş numarası grubu için Fiziksel güncelleştirmede seçeneğinin Hayır olarak ayarlandığı maddeler için bir satınalma siparişi satırı ayarladıktan sonra birden fazla stok hareketi oluşturulur.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026997"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Fiziksel güncelleştirmede seçeneği devre dışıyken toplu iş numaraları için çoklu stok hareketleri

KB numarası: 4613390

## <a name="symptoms"></a>Belirtiler

Toplu iş numarası grubu için **Fiziksel güncelleştirmede** seçeneğinin *Hayır* olarak ayarlandığı maddeler için bir satınalma siparişi satırı ayarladıktan sonra birden fazla stok hareketi oluşturulur.

Toplu iş numara grubunun **Fiziksel güncelleştirmede** seçeneğinin *Hayır* olarak ayarlandığı bir madde oluşturduğunuzda, bir satınalma satırı miktarını değiştirip satınalma siparişi sayfasını kaydederseniz, sistem otomatik olarak yeni bir toplu iş numarası oluşturur.

## <a name="resolution"></a>Çözünürlük

Toplu iş numarası grupları için **Fiziksel güncelleştirmede** ayarı aşağıdaki şekilde çalışır:

- Seçenek *Evet* olarak ayarlandığında, yeni toplu iş numaraları yalnızca fiziksel güncelleştirmeden sonra (örneğin, maddeler sevk edildiğinde veya teslim alındığında) oluşturulur.
- Seçenek *Hayır* olarak ayarlandığında, ilgili bir güncelleştirme her gerçekleştiğinde yeni bir toplu iş numarası oluşturulur (örneğin, bir satınalma siparişine yeni bir miktar eklendiğinde).
