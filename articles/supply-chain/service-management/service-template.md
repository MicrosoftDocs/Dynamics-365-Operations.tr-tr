---
title: Servis şablonları
description: Servis sözleşmesini bir şablon olarak tanımlayabilir ve daha sonra şablonun satırlarını başka bir servis sözleşmesine veya servis siparişine kopyalayabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c4bde1869b2be6e4cbbf979dae1b84c2a4974a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "327332"
---
# <a name="service-templates"></a><span data-ttu-id="4c347-103">Servis şablonları</span><span class="sxs-lookup"><span data-stu-id="4c347-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c347-104">Servis sözleşmesini bir şablon olarak tanımlayabilir ve daha sonra şablonun satırlarını başka bir servis sözleşmesine veya servis siparişine kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c347-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="4c347-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="4c347-105">Example</span></span>

<span data-ttu-id="4c347-106">Servis sağladığınız müşteri beş farklı konumda aynı servis asansörlerine sahip.</span><span class="sxs-lookup"><span data-stu-id="4c347-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="4c347-107">Müşteri için, her site başına birer anlaşma şeklinde beş servis anlaşması ayarlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="4c347-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="4c347-108">Tekrarlayan kurulum işlerini sınırlamak ve servis anlaşmalarında kurulum bilgilerinin aynı olduğundan emin olmak için bir servis anlaşması oluşturup asansörler üzerindeki servis işi için bir şablon olarak belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c347-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="4c347-109">Artık şablon satırlarını, her servis sözleşmesi şablondan gelen satırlarla doldurulacak şekilde beş yeni servis sözleşmesine kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c347-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="4c347-110">Şablon oluştur</span><span class="sxs-lookup"><span data-stu-id="4c347-110">Create a template</span></span>

<span data-ttu-id="4c347-111">Servis şablonu oluşturduğunuzda bir servis sözleşmesi oluşturur, üzerinde gerekli satırları oluşturur ve servis sözleşmesini bir servis şablonu grubuna iliştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c347-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="4c347-112">Servis sözleşmesi, yalnızca kendisine iliştirilmiş servis siparişleri yoksa bir şablon olarak tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4c347-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="4c347-113">Ayrıca, şablon olarak tanımlanan servis sözleşmesinden hiçbir servis siparişi oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="4c347-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="4c347-114">Şablon satırlarını kopyala</span><span class="sxs-lookup"><span data-stu-id="4c347-114">Copy template lines</span></span>

<span data-ttu-id="4c347-115">Şablon satırlarını bir servis şablonundan başka bir servis anlaşmasına veya bir servis siparişine kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c347-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="4c347-116">Şablon satırlarını servis siparişlerinize veya servis sözleşmelerinize kopyaladığınızda, şablon grupları her grubun genişletilebildiği bir ağaç görünümünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4c347-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="4c347-117">Bu görünüm, her şablonu ve şablon satırını görüntülemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4c347-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="4c347-118">Şablonları, şablonların kullanımını yansıtan adlar altında grupladıysanız kopyalamak istediğiniz servis şablonu satırlarını belirlemek daha kolay olur.</span><span class="sxs-lookup"><span data-stu-id="4c347-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c347-119">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="4c347-119">Related topics</span></span>

[<span data-ttu-id="4c347-120">Servis şablonları satırlarını kopyalama</span><span class="sxs-lookup"><span data-stu-id="4c347-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
