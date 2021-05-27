---
title: Tamamlandı bildirimi günlüğü deftere nakledildiğinde hata
description: Tamamlandı bildirimi günlüğü deftere nakledildiğinde, sipariş edilen miktarın azaltılamadığını belirten bir hata iletisi alırsınız.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026972"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="9562a-103">Tamamlandı bildirimi günlüğü deftere nakledildiğinde hata</span><span class="sxs-lookup"><span data-stu-id="9562a-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="9562a-104">KB numarası: 4612891</span><span class="sxs-lookup"><span data-stu-id="9562a-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="9562a-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="9562a-105">Symptoms</span></span>

<span data-ttu-id="9562a-106">**Tamamlandı bildirimi** günlüğünü deftere naklettiğinizde, bir hata oluşur ve aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="9562a-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="9562a-107">Siparişli durumda yeterli açık stok hareketi bulunmadığından, sipariş edilen miktar azaltılamaz.</span><span class="sxs-lookup"><span data-stu-id="9562a-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="9562a-108">Maddeler; Satın Alındı, Teslim Alındı veya Kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="9562a-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="9562a-109">Bu hata yalnızca **Hata miktarı** alanı, **Tamamlandı bildirimi** günlüğünün ilk satırında ayarlandığında ve en son satırda **Sağlam miktar** alanı ayarlandığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="9562a-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="9562a-110">**Hata miktarı** alanı son satırda ayarlanırsa bir hata oluşmaz.</span><span class="sxs-lookup"><span data-stu-id="9562a-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="9562a-111">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="9562a-111">Resolution</span></span>

<span data-ttu-id="9562a-112">Bu hatayı önlemek için, **Üretim denetim parametreleri** sayfasını açın ve **Genel** sekmesinde **Hata miktarı olan kalan miktarı artır** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9562a-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
