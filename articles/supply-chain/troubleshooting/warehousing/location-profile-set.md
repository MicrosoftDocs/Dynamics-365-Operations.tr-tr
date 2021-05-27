---
title: Konum profili negatif stoka izin vermiyor ancak eksi eldeki stoka izin veriliyor
description: Konum profili için Negatif stoka izin ver seçeneği Hayır olarak ayarlanmış, ancak sistem yine de negatif eldeki stoka izin veriyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026981"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="e5655-103">Konum profili negatif stoka izin vermiyor ancak eksi eldeki stoka izin veriliyor</span><span class="sxs-lookup"><span data-stu-id="e5655-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="e5655-104">KB numarası: 4613622</span><span class="sxs-lookup"><span data-stu-id="e5655-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="e5655-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="e5655-105">Symptoms</span></span>

<span data-ttu-id="e5655-106">Konum profili için **Negatif stoka izin ver** seçeneği *Hayır* olarak ayarlanmış, ancak sistem yine de negatif eldeki stoka izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="e5655-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e5655-107">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="e5655-107">Example scenario</span></span>

<span data-ttu-id="e5655-108">Resmi düzenlemeye tabi hareketler için sistem, defter zararlarına negatif stok kaydedebilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e5655-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="e5655-109">Bir maddenin negatif stok gösterebilmesini ancak bunu sadece tanklar gibi atanan konumlarda yapmasını istersiniz.</span><span class="sxs-lookup"><span data-stu-id="e5655-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="e5655-110">Ancak, madde modeli grubu negatif stoka izin veriyor ise konumun negatif stoka izin verecek şekilde ayarlanıp ayarlanmadığı fark etmez.</span><span class="sxs-lookup"><span data-stu-id="e5655-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="e5655-111">Madde, negatif stoka izin verilmeyecek şekilde ayarlanmışsa, konum profilinin nasıl ayarlandığı önemli değildir.</span><span class="sxs-lookup"><span data-stu-id="e5655-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="e5655-112">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="e5655-112">Resolution</span></span>

<span data-ttu-id="e5655-113">Konum profilinden **Negatif stoka izin ver** ayarı, yalnızca malzeme çekme gibi ambar işlemlerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e5655-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="e5655-114">Ancak, negatif stoka izin verilecek şekilde ayarlanan madde modeli grupları, Stok yönetimi ve Ambar yönetimi modüllerinden tüm işlemleri etkiler ve konum profili ayarı geçersiz kılmaz.</span><span class="sxs-lookup"><span data-stu-id="e5655-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="e5655-115">Bir ambarın negatif stok taşıma izni olup olmadığını kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5655-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="e5655-116">Madde modeli gruplarınızı negatif fiziksel stoka izin vermeyecek şekilde ayarlayın ve yalnızca ilgili ambarı negatif stoka izin verecek şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5655-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
