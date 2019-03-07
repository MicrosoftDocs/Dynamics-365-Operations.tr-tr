---
title: Bir gider raporundaki kişisel giderler
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations içindeki bir çalışanın kişisel giderlerini el almak için iki yöntemi açıklar.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "344904"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="03a2a-103">Gider raporundaki kişisel giderler</span><span class="sxs-lookup"><span data-stu-id="03a2a-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03a2a-104">İş seyahati sırasında çalışanların bazen kişisel giderlerini şirket kredi kartlarından yaptığı durumlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="03a2a-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="03a2a-105">Kişisel giderlerin işlenmesi için bir işlem tanımlamazsanız, çalışanlar madde haline getirilmiş gider raporlarını gönderdiğinde gider raporu onay işlemi kesintiye uğrayabilir.</span><span class="sxs-lookup"><span data-stu-id="03a2a-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="03a2a-106">Microsoft Dynamics 365 for Finance and Operations içinde, bir çalışanın kişisel giderlerini ele almak için iki yöntem vardır:</span><span class="sxs-lookup"><span data-stu-id="03a2a-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="03a2a-107">**Çalışan tarafından ödenen** – Kuruluşunuz şirket Kredi kartı ekstresinde görünen kişisel giderleri ödemez.</span><span class="sxs-lookup"><span data-stu-id="03a2a-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="03a2a-108">Bunun yerine, kişisel giderleri şirket kredi kartına borçlandırılan kurumsal giderlerle birlikte gösteren bir rapor oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03a2a-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="03a2a-109">**Şirket tarafından ödenen** - Şirketiniz tüm şirket kredi kartı faturasını öder ve kişisel giderleri çalışanların hesabına borç kaydeder.</span><span class="sxs-lookup"><span data-stu-id="03a2a-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="03a2a-110">Şirketinizin kullanacağı yöntemi **Gider Yönetimi parametreleri** sayfasından seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03a2a-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
