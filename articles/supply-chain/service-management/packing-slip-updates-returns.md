---
title: İadeler için sevk irsaliyesi güncelleştirmeleri
description: İade edilen maddelerin stoka alınabilmesi için, ait oldukları sevk irsaliyesinin güncelleştirilmesi gerekir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87dfad2247c84f8e85074739cfff4a2d1b9f8567
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259710"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="cb6c0-103">İadeler için sevk irsaliyesi güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="cb6c0-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cb6c0-104">İade edilen maddelerin stoka alınabilmesi için, ait oldukları sevk irsaliyesinin güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="cb6c0-105">Fatura güncelleştirme süreci nasıl mali hareketin güncelleştirilmesi ise, sevk irsaliyesi güncelleştirme süreci de stok kaydının fiziksel olarak güncelleştirilmesidir; başka bir deyişle, değişiklikleri stoka kaydeder.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="cb6c0-106">İadelerde ise, elden çıkarma eylemine atanan adımlar, sevk irsaliyesinin güncelleştirilmesi sırasında uygulanır.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="cb6c0-107">Sevk irsaliyesi güncelleştirmesi, madde geliş günlüğünde veya iade siparişinde işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="cb6c0-108">Sevk irsaliyesi deftere nakletme sürecinin bir parçası olarak, müşterinin sevkiyat belgelerindeki sevk irsaliyesi referans numarası sipariş satırlarıyla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="cb6c0-109">Bu ilişkilendirme isteğe bağlıdır ve yalnızca referans amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-109">This association is optional and for reference only.</span></span> <span data-ttu-id="cb6c0-110">Bu, herhangi bir hareket güncelleştirmesi oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="cb6c0-111">Beklenen tüm iade edilen maddeler gelmediyse, yalnızca sevk irsaliyesi güncelleştirmesinde alınan miktarı dahil etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="cb6c0-112">İade sevkiyatının geri kalanı gelene kadar kalan maddeleri siparişte bırakın.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="cb6c0-113">Bir madde karantinadan Sevkiyat ve Teslim Alma departmanına gönderildiyse (karantina denetçisinin maddeyi stokta nereye depolayacağını bilmediği durumlar gibi), karantinanın bir sonucu olarak belirtilen elden çıkarma kodunu uygun şekilde kaydetmek ve uygun işlemi yapmak için ilgili sevk irsaliyesinin güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="cb6c0-114">Bir satış sözleşmesindeki iade edilen madde için sevk irsaliyesini güncelleştirildiğinizde, bu maddeye ilişkin satış sözleşmesi taahhüdü tutar veya miktar değişikliğini yansıtmak için otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="cb6c0-115">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="cb6c0-115">See also</span></span>

[<span data-ttu-id="cb6c0-116">İadeler için fatura güncelleştirmeleri gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="cb6c0-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]