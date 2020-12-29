---
title: Kısmi serbest bırakma ve kısmi sevkiyatlarla ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta kısmi serbest bırakma ve kısmi sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645960"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="55264-103">Kısmi serbest bırakma ve kısmi sevkiyatlarla ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="55264-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55264-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta kısmi serbest bırakma ve kısmi sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="55264-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="55264-105">Satış siparişi faturalandıktan sonra bile bir satış siparişinin serbest bırakma durumu Kısmi serbest bırakıldı olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="55264-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="55264-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="55264-106">Issue description</span></span>

<span data-ttu-id="55264-107">Satış siparişi bir teslimat siparişi ancak üzerindeki bir veya daha fazla madde farklı teslimat moduna sahip.</span><span class="sxs-lookup"><span data-stu-id="55264-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="55264-108">Sipariş faturalandıktan sonra, serbest bırakma durumu *Kısmi serbest bırakıldı* şeklindedir.</span><span class="sxs-lookup"><span data-stu-id="55264-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="55264-109">Örneğin, bir satış siparişinde iki madde vardır: biri teslimat için, diğeri ise malzeme çekme içindir.</span><span class="sxs-lookup"><span data-stu-id="55264-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="55264-110">Teslimat ve malzeme çekme tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="55264-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="55264-111">Bu nedenle, her iki satır da faturalanmıştır.</span><span class="sxs-lookup"><span data-stu-id="55264-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="55264-112">Ancak, serbest bırakma durumu hala *Kısmi serbest bırakıldı* olarak gösterilir ve bu yanıltıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="55264-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="55264-113">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="55264-113">Issue resolution</span></span>

<span data-ttu-id="55264-114">Serbest bırakma durumu, yalnızca maddelerin ambar yönetimi için etkinleştirildiği sipariş satırları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="55264-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="55264-115">Bu nedenle, serbest bırakma durumu, bu senaryoda *Kısmi serbest bırakıldı* olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="55264-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="55264-116">Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="55264-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="55264-117">Serbest bırakma durumunu güncelleştirmek için sevk irsaliyesi ve faturalama işleminin bir parçası olarak bir uzantı eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="55264-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
