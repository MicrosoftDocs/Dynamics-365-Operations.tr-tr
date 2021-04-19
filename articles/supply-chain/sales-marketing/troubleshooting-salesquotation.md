---
title: Satış tekliflerinde sorun giderme
description: Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824762"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="1a51f-103">Satış tekliflerinde sorun giderme</span><span class="sxs-lookup"><span data-stu-id="1a51f-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="1a51f-104">Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="1a51f-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="1a51f-105">Bir servis malzemesi için satış teklifine ait satış miktarını değiştiremiyorum.</span><span class="sxs-lookup"><span data-stu-id="1a51f-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1a51f-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="1a51f-106">Issue description</span></span>

<span data-ttu-id="1a51f-107">Bir satış teklifi satırında *Servis* tipinde bulunan bir malzeme için satış miktarını (**SalesQty** alanı) ayarlamaya çalışırsanız, aşağıdaki iletiyi alırsınız: "Miktar alanı için güncelleştirmeye izin verilmez."</span><span class="sxs-lookup"><span data-stu-id="1a51f-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1a51f-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="1a51f-108">Issue resolution</span></span>

<span data-ttu-id="1a51f-109">Servis malzemeleri olan ürünler için bir satış miktarı ayarlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1a51f-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="1a51f-110">Örneğin, bir ögeyi yüklemek için bir servis teklif ederseniz, fiziksel öge olmadığı için bir miktar kaydetmek anlamlı olmaz.</span><span class="sxs-lookup"><span data-stu-id="1a51f-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="1a51f-111">Yalnızca bir hizmet vardır.</span><span class="sxs-lookup"><span data-stu-id="1a51f-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]