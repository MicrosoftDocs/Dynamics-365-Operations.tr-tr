---
title: "Servis görevi ilişkileri oluşturma"
description: "Sözleşme veya sipariş için tamamlanması gereken servis görevini açıklamak için Servis görevlerini servis sözleşmeleri veya servis siparişleriyle ilişkilendirebilirsiniz."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-task-relations"></a><span data-ttu-id="4296a-103">Servis görevi ilişkileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="4296a-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4296a-104">Sözleşme veya sipariş için tamamlanması gereken servis görevini açıklamak için Servis görevlerini servis sözleşmeleri veya servis siparişleriyle ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4296a-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="4296a-105">Hem teknisyenler hem de müşteriler bu bilgileri görebilir.</span><span class="sxs-lookup"><span data-stu-id="4296a-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="4296a-106">Servis anlaşmasıyla bir ilişki oluşturma</span><span class="sxs-lookup"><span data-stu-id="4296a-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="4296a-107">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4296a-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="4296a-108">Varolan bir servis anlaşmasını seçin veya yeni bir servis anlaşması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4296a-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="4296a-109">Eylem Bölmesindeki **Servis görevleri** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4296a-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="4296a-110">**Servis görevleri** formunda, yeni bir satır oluşturmak için CTRL+N tuşlarına basın ve **Servis görevi** listesinden bir servis görevi seçerek servis görevini servis sözleşmesine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4296a-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="4296a-111">**Açıklama** sekmesinde, serbest metinli alanlara her türlü dahili veya harici not açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="4296a-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="4296a-112">Girişi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="4296a-112">Close the form to save the record.</span></span>

<span data-ttu-id="4296a-113">Servis anlaşması için gerekli tüm servis görevi ilişkilerini oluşturana kadar bu yordamı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="4296a-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="4296a-114">Artık bu servis görevlerini iliştirilen anlaşma satırları için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4296a-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="4296a-115">Bir servis anlaşmasında oluşturulan bir servis görevi ilişkisi, servis anlaşmasına iliştirilmiş tüm servis siparişlerinden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4296a-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="4296a-116">Servis siparişiyle bir ilişki oluşturma</span><span class="sxs-lookup"><span data-stu-id="4296a-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="4296a-117">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4296a-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="4296a-118">Varolan bir servis siparişini seçin veya yeni bir servis siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4296a-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="4296a-119">Eylem Bölmesindeki **Servis görevleri** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4296a-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="4296a-120">**Servis görevleri** formunda, yeni bir satır oluşturmak için CTRL+N tuşlarına basın ve **Servis görevi** listesinden bir servis görevi seçerek servis görevlerini servis siparişine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4296a-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="4296a-121">**Açıklama** sekmesinde, serbest metinli alanlara her türlü dahili veya harici not açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="4296a-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="4296a-122">Girişi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="4296a-122">Close the form to save the record.</span></span>

<span data-ttu-id="4296a-123">Servis siparişi için gerekli tüm servis görevi ilişkilerini oluşturana kadar bu yordamı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="4296a-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="4296a-124">Artık, servis siparişi satırları oluşturduğunuzda ilişkisini oluşturduğunuz servis görevini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4296a-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="4296a-125">Bir servis siparişinde oluşturulan servis görevi ilişkileri belirli bir servis siparişinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4296a-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="4296a-126">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="4296a-126">See also</span></span>

[<span data-ttu-id="4296a-127">Servis görevleri</span><span class="sxs-lookup"><span data-stu-id="4296a-127">Service tasks</span></span>](service-tasks.md)


  



