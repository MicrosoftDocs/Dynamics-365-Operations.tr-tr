---
title: "Eldeki stokun maliyet değerlerini ayarlama"
description: "Bir stok kapanışı yürütüldükten sonra hazır stok miktarlarının maliyet değerini ayarlamak için, Eldeki stokların düzeltilmesi sayfasını kullanın."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 121b5e15912b9ecbf26f8831fdaef7637390cdd0
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="bdcf6-103">Eldeki stokun maliyet değerlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="bdcf6-103">Adjust on-hand inventory cost values</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bdcf6-104">Bir stok kapanışı yürütüldükten sonra hazır stok miktarlarının maliyet değerini ayarlamak için, Eldeki stokların düzeltilmesi sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="bdcf6-105">Bir envanter kapatma işlemi yürütüldükten sonra hazır envanter miktarlarının maliyet değerini ayarlamak için **Hazır envanterin ayarlanması** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="bdcf6-106">**Not:** **Hazır envanterin ayarlanması** sayfasını açmak için **Kapatma ve ayarlama** sayfasından bir tamamlanan envanter kapatma işlemi kaydı seçin ve **Ayar** &gt; **Hazır öğelerini** tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="bdcf6-107">**Örnek:** Şubat ayına ait şu işlemler bulunuyor olsun:</span><span class="sxs-lookup"><span data-stu-id="bdcf6-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="bdcf6-108">1 Şubat: 10.00 USD maliyetinde 2 adet için bir envanter finansal alındı</span><span class="sxs-lookup"><span data-stu-id="bdcf6-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="bdcf6-109">5 Şubat: Maliyeti 13.00 USD olan 1 adet için bir envanter finansal alındı</span><span class="sxs-lookup"><span data-stu-id="bdcf6-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="bdcf6-110">19 Şubat:Ortalama işletme maliyeti 11.00 olan 1 adet için bir envanter finansal işlemi</span><span class="sxs-lookup"><span data-stu-id="bdcf6-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="bdcf6-111">Bu madde ilk giren ilk çıkar (FIFO) stok modeliyle ayarlanmıştır ve stok kapanışı 28 Şubat tarihinde gerçekleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="bdcf6-112">11,00 USD tutarındaki Mali çıkış hareketi 1 Şubat tarihli mali girişine karşılık eşlenerek kapatılmıştır ve 1,00 USD tutarında bir düzeltme yapılacaktır.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="bdcf6-113">Bu durumda aşağıdaki stok girişleri açık stok miktarları içerir:</span><span class="sxs-lookup"><span data-stu-id="bdcf6-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="bdcf6-114">1 Şubat: 10.00 USD maliyetli 1 adet</span><span class="sxs-lookup"><span data-stu-id="bdcf6-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="bdcf6-115">5 Şubat: 13.00 USD maliyetli 1 adet</span><span class="sxs-lookup"><span data-stu-id="bdcf6-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="bdcf6-116">Bu iki maddenin maliyetini 15,00 USD olarak ayarlamak için eldeki açık miktarları son stok kapanış dönemi itibariyle ayarlamak için eldeki stoku düzeltme seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="bdcf6-117">**Not:** Hazır ayarlama işleminin nakil tarihi, son envanter kapatma tarihi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="bdcf6-118">Bu tarih değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="bdcf6-118">This date can't be modified.</span></span>

