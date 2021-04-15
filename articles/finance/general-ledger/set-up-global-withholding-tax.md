---
title: Global stopaj vergisini ayarlama
description: Bu konu, satışlar ve satın almalar için genel stopaj vergisi ödemesini ayarlamaya yönelik gereken adımları listeler.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3270b3f75d719fef9a7eb991c49e9d6585cd44d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815320"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="65c03-103">Global stopaj vergisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="65c03-103">Set up global withholding tax</span></span>

<span data-ttu-id="65c03-104">Bu konu, satışlar ve satın almalar için genel stopaj vergisi ödemesini ayarlamaya yönelik gereken adımları listeler.</span><span class="sxs-lookup"><span data-stu-id="65c03-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="65c03-105">**Stopaj vergisi daireleri** sayfasında stopaj vergisi dairelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="65c03-106">**Stopaj vergisi kapatma dönemleri** sayfasında stopaj kapatma dönemlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="65c03-107">**Stopaj vergisi > genel muhasebe deftere nakil grubu** sayfasında stopaj genel muhasebe deftere nakil grubunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="65c03-108">**Stopaj vergisi** hesabı, Stopaj vergisinin **Deftere nakil türüne** sahip bir ana hesaba atanır.</span><span class="sxs-lookup"><span data-stu-id="65c03-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="65c03-109">**Stopaj vergisi mahsubu** hesabı da **Deftere nakil türü** "Stopaj vergisi mahsubu" olan bir ana hesapa atanır.</span><span class="sxs-lookup"><span data-stu-id="65c03-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="65c03-110">**Genel muhasebe > Hesap planı > Hesaplar > Ana hesaplar**'a gidin, ana hesaplar için **Deftere nakil doğrulaması** alt formunda **Deftere nakil türünü** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="65c03-111">**Stopaj vergisi kodları** sayfasında stopaj vergisi kodlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="65c03-112">**Stopaj vergisi grupları** sayfasında stopaj vergisi grupları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="65c03-113">**Stopaj vergisi gelir** **türleri** sayfasında stopaj vergisi gelir türlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="65c03-114">Bir kalem veya hizmet için **Kalem stopaj vergisi grupları** sayfasında stopaj vergisi gruplarıı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="65c03-115">**Genel muhasebe parametreleri > Stopaj vergisi** sayfasında **Minimum fatura tutarını** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65c03-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]