---
title: SEPA hesaptan ödeme talimatı ayarlama
description: Tek Euro ödeme alanı (SEPA) otomatik ödemesi, müşterinin alacaklıya imzalı yönerge vermiş olması koşuluyla, alacaklının müşterinin banka hesabından fon toplamak sağlar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45cabc7d263299763b6ee457063c96cdf384eeeb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189028"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="2eca2-103">SEPA hesaptan ödeme talimatı ayarlama</span><span class="sxs-lookup"><span data-stu-id="2eca2-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2eca2-104">Tek Euro ödeme alanı (SEPA) otomatik ödemesi, müşterinin alacaklıya imzalı yönerge vermiş olması koşuluyla, alacaklının müşterinin banka hesabından fon toplamak sağlar.</span><span class="sxs-lookup"><span data-stu-id="2eca2-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="2eca2-105">Müşterinin imzaladığı yönerge, alacaklının tahsilat yapmasına izin verir ve müşteri bankasına ödemeyi yapması doğrultusunda talimat verir.</span><span class="sxs-lookup"><span data-stu-id="2eca2-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="2eca2-106">Bu konu, SEPA otomatik ödeme talimatlarını ayarlama işlemini göstermek için düzenlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="2eca2-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2eca2-107">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="2eca2-107">Prerequisites</span></span>
<span data-ttu-id="2eca2-108">Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2eca2-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="2eca2-109">Kategori</span><span class="sxs-lookup"><span data-stu-id="2eca2-109">Category</span></span>       | <span data-ttu-id="2eca2-110">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="2eca2-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eca2-111">Ülke/bölge</span><span class="sxs-lookup"><span data-stu-id="2eca2-111">Country/region</span></span> | <span data-ttu-id="2eca2-112">Tüzel kişiliğin birincil adresi aşağıdaki ülkelerden birinde olmalıdır: Avusturya, Belçika, Almanya, İspanya, Fransa, İtalya veya Hollanda.</span><span class="sxs-lookup"><span data-stu-id="2eca2-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="2eca2-113">Otomatik ödeme talimatları için bir numara sırası ayarlama: Her otomatik ödeme talimatının benzersiz bir numarası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2eca2-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="2eca2-114">**Numara serileri** sayfasını kullanarak otomatik ödeme talimatları için bir numara sırası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2eca2-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="2eca2-115">**Alacak hesapları parametreleri** sayfasında bu tanımlayıcıyı otomatik ödeme talimatına bir numara serisi atamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="2eca2-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="2eca2-116">Otomatik ödeme talimatları için Alacak hesapları parametrelerini ayarlama: Otomatik ödeme talimatlarına ilişkin parametreleri ayarlamak için **Alacak hesapları parametreleri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="2eca2-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="2eca2-117">Parametreleri ayarlamak için **Hesaptan ödeme** sekmesinde, varsayılan parametreleri gerekli şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2eca2-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="2eca2-118">Ardından **Numara serileri** sekmesinde, **Hesaptan ödeme talimatı kodu** alanını daha önce ayarladığınız numara serisiyle güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2eca2-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="2eca2-119">Otomatik ödeme talimatları için bir ödeme yöntemi ayarlama: Otomatik ödeme talimatları için bir yöntemi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2eca2-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="2eca2-120">Hesaptan ödemeler oluşturmak için faturaları sorgulamak için bu ödeme yöntemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2eca2-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="2eca2-121">**Ödeme yöntemleri** sayfasını ödeme yöntemini ayarlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="2eca2-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="2eca2-122">Hesaptan ödeme talimatları için bir ödeme yöntemi ayarlamak için, ödeme yöntemi için aşağıdaki bu ek adımları takip etmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="2eca2-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="2eca2-123">**Ödeme türü** alaninda, **Elektronik ödeme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2eca2-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="2eca2-124">İsteğe bağlı: Her müşterinizin birden fazla talimatı olacağını düşünüyorsanız **Dönem** alanında **Fatura**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2eca2-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="2eca2-125">Her fatura için ayrı bir ödeme oluşturulur ve her bir ödeme, fatura için belirtilen talimatı kullanır.</span><span class="sxs-lookup"><span data-stu-id="2eca2-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="2eca2-126">**Talimat gerektirin** seçeneğini otomatik ödeme talimatlarını kullanarak ödeme oluşturmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="2eca2-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="2eca2-127">**Talimat gerektirin** seçeneği yalnızca **Elektronik ödeme** içinde **Ödeme türü** alanını seçerseniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2eca2-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="2eca2-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2eca2-128">Additional resources</span></span>

[<span data-ttu-id="2eca2-129">Otomatik ödeme genel bakış</span><span class="sxs-lookup"><span data-stu-id="2eca2-129">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="2eca2-130">Müşteri için hesaptan ödeme talimatı oluşturma</span><span class="sxs-lookup"><span data-stu-id="2eca2-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

