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
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="a2f05-103">Fiziksel güncelleştirmede seçeneği devre dışıyken toplu iş numaraları için çoklu stok hareketleri</span><span class="sxs-lookup"><span data-stu-id="a2f05-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="a2f05-104">KB numarası: 4613390</span><span class="sxs-lookup"><span data-stu-id="a2f05-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="a2f05-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="a2f05-105">Symptoms</span></span>

<span data-ttu-id="a2f05-106">Toplu iş numarası grubu için **Fiziksel güncelleştirmede** seçeneğinin *Hayır* olarak ayarlandığı maddeler için bir satınalma siparişi satırı ayarladıktan sonra birden fazla stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a2f05-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="a2f05-107">Toplu iş numara grubunun **Fiziksel güncelleştirmede** seçeneğinin *Hayır* olarak ayarlandığı bir madde oluşturduğunuzda, bir satınalma satırı miktarını değiştirip satınalma siparişi sayfasını kaydederseniz, sistem otomatik olarak yeni bir toplu iş numarası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2f05-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2f05-108">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="a2f05-108">Resolution</span></span>

<span data-ttu-id="a2f05-109">Toplu iş numarası grupları için **Fiziksel güncelleştirmede** ayarı aşağıdaki şekilde çalışır:</span><span class="sxs-lookup"><span data-stu-id="a2f05-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="a2f05-110">Seçenek *Evet* olarak ayarlandığında, yeni toplu iş numaraları yalnızca fiziksel güncelleştirmeden sonra (örneğin, maddeler sevk edildiğinde veya teslim alındığında) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a2f05-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="a2f05-111">Seçenek *Hayır* olarak ayarlandığında, ilgili bir güncelleştirme her gerçekleştiğinde yeni bir toplu iş numarası oluşturulur (örneğin, bir satınalma siparişine yeni bir miktar eklendiğinde).</span><span class="sxs-lookup"><span data-stu-id="a2f05-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
