---
title: Stopaj vergisi ödemesi oluşturma
description: Stopaj vergisi ödemesi işini yordamları, stopaj vergisi hesaplarında Borç hesaplarındaki stopaj vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin stopaj vergisi kapatma hesabına mahsup olarak işler. Bu konu, stopaj vergisi ödemesini ayarlamak için gereken adımları listeler.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060807"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="409ec-104">Stopaj vergisi ödemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="409ec-104">Create a withholding tax payment</span></span>

<span data-ttu-id="409ec-105">Stopaj vergisi ödemesi işini yordamları, stopaj vergisi hesaplarında Borç hesaplarındaki stopaj vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin stopaj vergisi kapatma hesabına mahsup olarak işler.</span><span class="sxs-lookup"><span data-stu-id="409ec-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="409ec-106">Bu konu, stopaj vergisi ödemesini ayarlamak için gereken adımları listeler.</span><span class="sxs-lookup"><span data-stu-id="409ec-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="409ec-107">Stopaj vergisi ödemesi hesaplanırken, stopaj vergisi mahsubu (alacak hesaplarından) dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="409ec-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="409ec-108">**Gezinme bölmesi > Modüller > Vergi > Beyannameler > Stopaj vergisi > Stopaj vergisi ödemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="409ec-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="409ec-109">**Kapatma dönemi** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="409ec-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="409ec-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="409ec-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="409ec-111">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="409ec-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="409ec-112">**Hareket tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="409ec-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="409ec-113">Stopaj vergisi ödeme fişinin stopaj vergisi kapatma hesabına nakli için **Güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="409ec-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="409ec-114">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="409ec-114">Click **OK**.</span></span>

![Stopaj vergisi ödemesine ilişkin parametreler](media/withholding-tax-payment.png)
