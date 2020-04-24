---
title: Bir konşimento oluştur
description: Bu konu, ambar yönetimi işlemleri kullanırken bir konşimentonun nasıl oluşturulacağını açıklar.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05ad5d4b49f1fa50bde7df9c835ee99a981420c4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206323"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="cb3db-103">Bir konşimento oluştur</span><span class="sxs-lookup"><span data-stu-id="cb3db-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb3db-104">Bu konu, ambar yönetimi işlemleri kullanırken bir konşimentonun nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="cb3db-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="cb3db-105">Bir konşimento, maddeleri sevk eden şirket ve taşıyıcı arasındaki yasal bir belgedir.</span><span class="sxs-lookup"><span data-stu-id="cb3db-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="cb3db-106">Belge sevk edilen maddelere eşlik eder ve öğeler varış noktasında teslim edildiğinde sevk irsaliyesi alış irsaliyesi olarak hizmet verir.</span><span class="sxs-lookup"><span data-stu-id="cb3db-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="cb3db-107">Ambar yönetimi kullanıyorsanız, konşimento oluşturmanın iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="cb3db-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="cb3db-108">**Konşimento** sayfası kullanarak raporu el ile oluşturma.</span><span class="sxs-lookup"><span data-stu-id="cb3db-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="cb3db-109">Raporu **Yük planlama workbench** üzerinden oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="cb3db-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="cb3db-110">Konşimentoyu **Yük planlama workbench** üzerinden oluşturursanız, yük durumu **Sevk edilmiş.** olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cb3db-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="cb3db-111">Yükte birden fazla sevkiyat varsa, her bir sevkiyat için bir konşimento oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cb3db-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="cb3db-112">Bir konşimento oluşturulduktan sonra **Konşimento** sayfasında onun üzerinde değişiklik yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb3db-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="cb3db-113">Ana konşimento</span><span class="sxs-lookup"><span data-stu-id="cb3db-113">Master bill of lading</span></span>
<span data-ttu-id="cb3db-114">Eğer yükte birden fazla sevkiyat varsa, bir ana konşimento oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb3db-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="cb3db-115">Bu konşimento ile aynı biçime ve bilgilere sahiptir, ancak tüm sevkiyatların özetlenmiş bir içeriğini de içerir.</span><span class="sxs-lookup"><span data-stu-id="cb3db-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="cb3db-116">Eğer **Bir yükte birden fazla sevkiyat olduğunda bir ana konşimento oluştur** seçeneği **Taşıma yönetim parametreleri** sayfasında **Evet** olarak ayarlanmışsa, bir konşimentoyu **Yük planlama workbench** üzerinden oluşturduğunuzda ve birden fazla sevkiyat bulunduğunda, otomatik olarak bir ana konşimento oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb3db-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="cb3db-117">Ayrıca konşimento listelerini **İlgili bilgi** &gt; **Konşimento** üzerine tıklayarak da alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb3db-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="cb3db-118">Konşimentoları el ile oluşturuyorsanız, bir ana konşimentoyu **Konşimento** sayfası üzerinde oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb3db-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



