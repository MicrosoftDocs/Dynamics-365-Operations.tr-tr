---
title: Servis siparişi aşamalarını ayarla
description: Servis siparişi aşamalarını ayarlayın.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c7b632ea9c4574de8f9b0a128976429b2e2e786
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206761"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="09bbd-103">Servis siparişi aşamalarını ayarla</span><span class="sxs-lookup"><span data-stu-id="09bbd-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="09bbd-104">**Servis yönetimi** \> **Kurulum** \> **Servis siparişleri** \> **Servis aşamaları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09bbd-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="09bbd-105">Yeni bir kayıt oluşturmak için CTRL+N tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="09bbd-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="09bbd-106">**Servis aşaması** ve **Açıklama** alanlarında, bir servis aşaması kodu ve açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="09bbd-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="09bbd-107">Aşama için uygun parametreleri seçin.</span><span class="sxs-lookup"><span data-stu-id="09bbd-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="09bbd-108">Geçerli aşama için bir ana aşama seçin veya aşama kurulumundaki ilk aşama söz konusuysa **Ana** alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="09bbd-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="09bbd-109">Aşamayı kaydettikten sonra <STRONG>Ana</STRONG> alanını değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="09bbd-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="09bbd-110">Bunun yerine, kaydı silebilir ve <STRONG>Ana</STRONG> alanında farklı bir seçim yaparak yeniden oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09bbd-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="09bbd-111">Ayrıca, <STRONG>Ana</STRONG> alanı boş olan tek bir aşama oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09bbd-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="09bbd-112">Başka bir deyişle, yalnızca bir tane başlangıç aşamasına izin verilir.</span><span class="sxs-lookup"><span data-stu-id="09bbd-112">That is, only one initial stage is permitted.</span></span></P>


  


