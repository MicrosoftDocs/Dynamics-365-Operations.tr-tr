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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795021"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="6d7b9-103">Gider raporundaki kişisel giderler</span><span class="sxs-lookup"><span data-stu-id="6d7b9-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d7b9-104">İş seyahati sırasında çalışanların bazen kişisel giderlerini şirket kredi kartlarından yaptığı durumlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="6d7b9-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="6d7b9-105">Kişisel giderlerin işlenmesi için bir işlem tanımlamazsanız, çalışanlar madde haline getirilmiş gider raporlarını gönderdiğinde gider raporu onay işlemi kesintiye uğrayabilir.</span><span class="sxs-lookup"><span data-stu-id="6d7b9-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="6d7b9-106">Microsoft Dynamics 365 for Finance and Operations içinde, bir çalışanın kişisel giderlerini ele almak için iki yöntem vardır:</span><span class="sxs-lookup"><span data-stu-id="6d7b9-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="6d7b9-107">**Çalışan tarafından ödenen** – Kuruluşunuz şirket Kredi kartı ekstresinde görünen kişisel giderleri ödemez.</span><span class="sxs-lookup"><span data-stu-id="6d7b9-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="6d7b9-108">Bunun yerine, kişisel giderleri şirket kredi kartına borçlandırılan kurumsal giderlerle birlikte gösteren bir rapor oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d7b9-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="6d7b9-109">**Şirket tarafından ödenen** - Şirketiniz tüm şirket kredi kartı faturasını öder ve kişisel giderleri çalışanların hesabına borç kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6d7b9-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="6d7b9-110">Şirketinizin kullanacağı yöntemi **Gider Yönetimi parametreleri** sayfasından seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d7b9-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
