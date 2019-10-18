---
title: Hızlı içe aktarma dışa aktarma
description: Hızlı içe aktarma dışa aktarma özelliğinin amacı birkaç adımda içe ve dışa aktarma işlemi yapmanızı sağlamaktır.
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 7655de1399c49328bae1736c796325e546796bd5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181163"
---
# <a name="quick-import-export"></a><span data-ttu-id="71d9f-103">Hızlı içe aktarma dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="71d9f-103">Quick import export</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71d9f-104">Hızlı içe aktarma dışa aktarma özelliğinin amacı birkaç adımda içe ve dışa aktarma işlemi yapmanızı sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="71d9f-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="71d9f-105">Kullanıcıların hızla yürütmek istediği basit işleri içe veya dışa aktarmasını sağlamak için Hızlı İçe Aktarma Dışa Aktarma özelliğini ekledik.</span><span class="sxs-lookup"><span data-stu-id="71d9f-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="71d9f-106">İdeal olarak bu özellik, bir dosyanın sisteme otomatik olarak eşlendiği ve kullanıcının gelişmiş eşleme yapmasına veya yinelenen içe veya dışa aktarma işleri oluşturmasına gerek kalmadığı senaryolarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="71d9f-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="71d9f-107">Bu özellik temel ve özel varlıklarla çalışmayı destekler.</span><span class="sxs-lookup"><span data-stu-id="71d9f-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="71d9f-108">Dosyalardan içe aktarma yapabilirsiniz ve ODBC veri kaynağı kullanıyorsanız, içe aktarma işleminizi tanımlamak için kullanmak üzere bir sorgu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="71d9f-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="71d9f-109">AX veya Dosya için önceden tanımlanmış kaynak veri biçimleriniz olmalı ve bunların nerede bulunduğunu biliyor olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="71d9f-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="71d9f-110">Hızlı içe aktarma/dışa aktarma özelliğini kullanmak için bir işlem grubu oluşturmanız gerekmez. İçe veya dışa aktarma işi yürütülürken sistem tarafından bir işlem grubu otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="71d9f-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="71d9f-111">Ayrıca hızlı içe aktarma/dışa aktarma özelliği ile içe aktarılan verilerin geçmişini tutmayı da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="71d9f-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="71d9f-112">Hızlı içe aktarma dışa aktarma özelliğinin DIXF kavramlarını bildiğinizi varsaydığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="71d9f-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>



