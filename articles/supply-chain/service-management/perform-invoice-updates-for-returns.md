---
title: İadeler için fatura güncelleştirmeleri gerçekleştirme
description: Bu işlev sipariş iadelerinin ve satış siparişlerinin aynı anda ve aynı kişi tarafından faturalanmasını isteyen kuruluşların iş süreçlerini destekler.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d99f067e93de57b5b13787f128f450f736660351
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006700"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="c5856-103">İadeler için fatura güncelleştirmeleri gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="c5856-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c5856-104">İade siparişi, iade edilen sipariş olarak işaretlenmiş bir satış siparişi türüdür.</span><span class="sxs-lookup"><span data-stu-id="c5856-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="c5856-105">Bu nedenle, iade siparişler için fatura oluşturmak üzere **İade siparişleri** formu yerine **Tüm satış siparişleri** liste sayfası kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c5856-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="c5856-106">Bu işlev sipariş iadelerinin ve satış siparişlerinin aynı anda ve aynı kişi tarafından faturalanmasını isteyen kuruluşların iş süreçlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="c5856-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="c5856-107">İade edilen maddenin faturası negatif bir tutar olduğu için buna alacak dekontu denir.</span><span class="sxs-lookup"><span data-stu-id="c5856-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="c5856-108">Fatura güncelleştirmesini toplu iş işlemesi için ayarladığınızda, **İade edilen sipariş** türündeki satış siparişi, siparişin sevk irsaliyesinin güncelleştirildiğini gösteren, **Alındı** iade satırı durumuna sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c5856-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="c5856-109">İade siparişine ait bir faturayı deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="c5856-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="c5856-110">**Alacak hesapları** \> **Genel** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5856-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="c5856-111">**Sipariş türü** alanında **İade edilen sipariş** olarak görünen bir satış siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="c5856-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="c5856-112">Eylem Bölmesinde, **Fatura** sekmesindeki **Oluştur** gurubunda **Fatura**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5856-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="c5856-113">**Parametreler** sekmesinde **Deftere nakil** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c5856-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="c5856-114">Formdaki bilgileri gözden geçirerek gerekli düzeltmeleri yapın.</span><span class="sxs-lookup"><span data-stu-id="c5856-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="c5856-115">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c5856-115">Click **OK**.</span></span> <span data-ttu-id="c5856-116">Alacak dekontu deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="c5856-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5856-117">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="c5856-117">See also</span></span>

[<span data-ttu-id="c5856-118">İadeler için sevk irsaliyesi güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="c5856-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


