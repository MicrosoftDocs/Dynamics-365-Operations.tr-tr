---
title: Servis görevi ilişkileri oluşturma
description: Sözleşme veya sipariş için tamamlanması gereken servis görevini açıklamak için Servis görevlerini servis sözleşmeleri veya servis siparişleriyle ilişkilendirebilirsiniz.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9a7808357916ed80ddfa46e1e4f362e0dde1671
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819076"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="888a0-103">Servis görevi ilişkileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="888a0-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="888a0-104">Sözleşme veya sipariş için tamamlanması gereken servis görevini açıklamak için Servis görevlerini servis sözleşmeleri veya servis siparişleriyle ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="888a0-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="888a0-105">Hem teknisyenler hem de müşteriler bu bilgileri görebilir.</span><span class="sxs-lookup"><span data-stu-id="888a0-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="888a0-106">Servis anlaşmasıyla bir ilişki oluşturma</span><span class="sxs-lookup"><span data-stu-id="888a0-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="888a0-107">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="888a0-107">Go to **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="888a0-108">Var olan bir servis anlaşmasını seçin veya yeni bir servis anlaşması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="888a0-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="888a0-109">Eylem Bölmesindeki **Servis görevleri** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="888a0-109">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="888a0-110">**Servis görevleri** formunda, yeni bir satır oluşturmak için **Yeni**'yi seçin ve **Servis görevi** listesinden bir servis görevi seçerek servis görevini servis sözleşmesine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="888a0-110">On the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="888a0-111">**Açıklama** sekmesinde, serbest metinli alanlara her türlü dahili veya harici not açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="888a0-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="888a0-112">Girişi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="888a0-112">Close the form to save the record.</span></span>

<span data-ttu-id="888a0-113">Servis anlaşması için gerekli tüm servis görevi ilişkilerini oluşturana kadar bu yordamı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="888a0-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="888a0-114">Artık bu servis görevlerini iliştirilen anlaşma satırları için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="888a0-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="888a0-115">Bir servis anlaşmasında oluşturulan bir servis görevi ilişkisi, servis anlaşmasına iliştirilmiş tüm servis siparişlerinden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="888a0-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="888a0-116">Servis siparişiyle bir ilişki oluşturma</span><span class="sxs-lookup"><span data-stu-id="888a0-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="888a0-117">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="888a0-117">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="888a0-118">Var olan bir servis siparişini seçin veya yeni bir servis siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="888a0-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="888a0-119">Eylem Bölmesindeki **Servis görevleri** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="888a0-119">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="888a0-120">**Servis görevleri** formunda, yeni bir satır oluşturmak için **Yeni**'yi seçin ve **Servis görevi** listesinden bir servis görevi seçerek servis görevlerini servis siparişine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="888a0-120">From the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="888a0-121">**Açıklama** sekmesinde, serbest metinli alanlara her türlü dahili veya harici not açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="888a0-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="888a0-122">Girişi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="888a0-122">Close the form to save the record.</span></span>

<span data-ttu-id="888a0-123">Servis siparişi için gerekli tüm servis görevi ilişkilerini oluşturana kadar bu yordamı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="888a0-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="888a0-124">Artık, servis siparişi satırları oluşturduğunuzda ilişkisini oluşturduğunuz servis görevini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="888a0-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="888a0-125">Bir servis siparişinde oluşturulan servis görevi ilişkileri belirli bir servis siparişinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="888a0-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="888a0-126">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="888a0-126">See also</span></span>

[<span data-ttu-id="888a0-127">Servis görevlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="888a0-127">Service tasks overview</span></span>](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]