---
title: Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış
description: Servis sözleşmesi tipik bir servis ziyaretinde kullanılan kaynakları ve bu kaynakların müşteriye ne şekilde faturalandığını tanımlamanızı sağlar.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f906beb4f239add265cf280f6bfade66cb9eadc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835954"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="3c2ad-103">Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="3c2ad-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c2ad-104">Servis sözleşmesi tipik bir servis ziyaretinde kullanılan kaynakları ve bu kaynakların müşteriye ne şekilde faturalandığını tanımlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="3c2ad-105">Her servis sözleşmesi, hareketlerin deftere nakledildiği ve faturalandığı bir projeye iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="3c2ad-106">Ancak servis siparişi hareketlerini servis siparişini öncelikle bir servis sözleşmesine bağlamadan da doğrudan proje üzerinden faturalandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="3c2ad-107">Servis siparişinin yalnızca bir defalık servis ziyareti olması ve servis hareketlerini hızlı bir şekilde işleme gereksiniminin belirli bir dönem boyunca müşteri hakkında ayrıntılı servis sözleşmesi bilgileri tutma gereksinimine ağır basması durumunda bunu yapmaya karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="3c2ad-108">Servis anlaşması</span><span class="sxs-lookup"><span data-stu-id="3c2ad-108">Service agreement</span></span>

<span data-ttu-id="3c2ad-109">Her servis sözleşmesinde, bir proje, bir servis sözleşmesi kodu ve bir servis sözleşmesi grubu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="3c2ad-110">Servis sözleşmesi grubu servis sözleşmelerini sıralamak ve düzenlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="3c2ad-111">Servis sözleşmesi başlığı, iliştirilmiş tüm sözleşme satırları için geçerli olan ayarları içerir:</span><span class="sxs-lookup"><span data-stu-id="3c2ad-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="3c2ad-112">Servis anlaşmasının askıya alınıp alınmadığı.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="3c2ad-113">Servis anlaşması askıya alınmışsa, servis anlaşmasından servis siparişleri oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="3c2ad-114">Servis anlaşmasının süresi.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="3c2ad-115">Servis anlaşması satırlarının servis siparişleriyle ne şekilde birleştirileceği.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="3c2ad-116">Servis sözleşmesinin bir şablon olup olmadığı</span><span class="sxs-lookup"><span data-stu-id="3c2ad-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="3c2ad-117">Servis sözleşmesi başlığında sözleşmenin çeşitli satırlarına eklenecek belirli servis görevlerini veya servis nesnelerini girerek servis sözleşmesiyle birlikte kullanılabilecek tüm servis nesnelerini ve servis görevlerini de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="3c2ad-118">Ayrıca, servis sözleşmesi başlığından servis sözleşmesi satırlarını veya servis şablonu satırlarını alarak geçerli servis sözleşmesine kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="3c2ad-119">Servis sözleşmelerini askıya alabilir ve servis sözleşmesi satırlarını ayrı ayrı durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="3c2ad-120">Servis sözleşmesi satırında **Askıda** onay kutusunu seçerseniz şunları yapamazsınız:</span><span class="sxs-lookup"><span data-stu-id="3c2ad-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="3c2ad-121">Servis sözleşmesinden otomatik olarak veya el ile servis siparişleri oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="3c2ad-122">Servis sözleşmesi satırındaki **Durduruldu** onay kutusunu seçerseniz şunları yapamazsınız:</span><span class="sxs-lookup"><span data-stu-id="3c2ad-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="3c2ad-123">Servis sözleşmesi satırından otomatik olarak veya el ile servis siparişleri oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="3c2ad-124">Servis anlaşması satırını başka bir servis anlaşmasına veya servis siparişine kopyalayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="3c2ad-125">Servis sözleşmesi askıdaysa tüm iliştirilmiş satırların durumu tek tek dikkate alınmadan durdurulur.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="3c2ad-126">Servis sözleşmesi satırları</span><span class="sxs-lookup"><span data-stu-id="3c2ad-126">Service-agreement lines</span></span>

<span data-ttu-id="3c2ad-127">Her servis sözleşmesi satırı ayrıntılı şekilde servis işinin içeriğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="3c2ad-128">Satırlar aşağıdaki ayarları içerir:</span><span class="sxs-lookup"><span data-stu-id="3c2ad-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="3c2ad-129">Hareket tipi ve hareket tipinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="3c2ad-130">Servis işini gerçekleştiren çalışan</span><span class="sxs-lookup"><span data-stu-id="3c2ad-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="3c2ad-131">Servis anlaşması için servisin uygulanması gereken nesneler.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="3c2ad-132">İşin gerçekleştirilme sıklığı ve ilişkili madde, gider ve masraf hareketleri kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="3c2ad-133">Servis siparişi satırlarının bir servis siparişi dahilinde gruplandırılabileceği zaman penceresi.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="3c2ad-134">Sözleşme satırı kümelerini iş görevleri halinde gruplandırmak ve servis teknisyenleri ile müşterilere sağlanacak servis görevini özetlemek için kullanılan servis görevleri.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="3c2ad-135">Bir satırın durdurulup durdurulmadığı.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-135">Whether a line is stopped.</span></span> <span data-ttu-id="3c2ad-136">Bir satır durdurulmuşsa, siz konusu satır için servis siparişleri oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="3c2ad-137">Kategori ve satır özelliği gibi proje ayarları.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c2ad-138">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="3c2ad-138">Related topics</span></span>

[<span data-ttu-id="3c2ad-139">Servis sözleşmeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="3c2ad-139">Create service agreements</span></span>](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]