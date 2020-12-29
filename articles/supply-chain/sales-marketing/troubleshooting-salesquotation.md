---
title: Satış tekliflerinde sorun giderme
description: Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439253"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="2d235-103">Satış tekliflerinde sorun giderme</span><span class="sxs-lookup"><span data-stu-id="2d235-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="2d235-104">Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2d235-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="2d235-105">Bir servis malzemesi için satış teklifine ait satış miktarını değiştiremiyorum.</span><span class="sxs-lookup"><span data-stu-id="2d235-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2d235-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="2d235-106">Issue description</span></span>

<span data-ttu-id="2d235-107">Bir satış teklifi satırında *Servis* tipinde bulunan bir malzeme için satış miktarını (**SalesQty** alanı) ayarlamaya çalışırsanız, aşağıdaki iletiyi alırsınız: "Miktar alanı için güncelleştirmeye izin verilmez."</span><span class="sxs-lookup"><span data-stu-id="2d235-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2d235-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="2d235-108">Issue resolution</span></span>

<span data-ttu-id="2d235-109">Servis malzemeleri olan ürünler için bir satış miktarı ayarlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="2d235-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="2d235-110">Örneğin, bir ögeyi yüklemek için bir servis teklif ederseniz, fiziksel öge olmadığı için bir miktar kaydetmek anlamlı olmaz.</span><span class="sxs-lookup"><span data-stu-id="2d235-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="2d235-111">Yalnızca bir hizmet vardır.</span><span class="sxs-lookup"><span data-stu-id="2d235-111">There is only a service.</span></span>

