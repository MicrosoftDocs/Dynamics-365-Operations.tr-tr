---
title: Fatura bölme işlevi
description: Bu konu, faturaları teslimat adresine ve vergi hesap numarasına (TAN) göre bölmeye yönelik kurulum ve işlevleri açıklamaktadır.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023663"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="1d0f2-103">Fatura bölme işlevi</span><span class="sxs-lookup"><span data-stu-id="1d0f2-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d0f2-104">Bu konu, faturaları teslimat adresine ve vergi hesap numarasına (TAN) göre bölmeye yönelik kurulum ve işlevleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="1d0f2-105">**Satınalma siparişi** sayfasında farklı teslimat adresleri ve TAN'ları olan bir ürün girişini veya faturasını deftere nakletmek ve bölmek için **Borç hesapları parametreleri** sayfasında **Genel** sekmesinde **Ürün girişi** veya **Fatura** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="1d0f2-106">Deftere nakledilen fatura, teslimat adresine ve TAN'a göre bölünür.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="1d0f2-107">**Satış siparişi** sayfasında farklı fatura satırları için farklı teslimat adresleri ve TAN'lar belirlenmiş bir onayı, malzeme çekme listesini, sevk irsaliyesini ya da faturayı deftere nakletmek ve bölmek için **Özet güncelleştirmesi** sekmesinde, **Bölme temeli** hızlı sekmesinde, **Teslimat bilgileri** satırında, **Onay**, **Malzeme çekme listesi**, **Sevk irsaliyesi** veya **Fatura** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="1d0f2-108">Fatura öncelikle teslimat adresine göre ve ardından TAN'a göre bölünür.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="1d0f2-109">**Teslimat bilgileri** için hiçbir seçenek **Evet** olarak ayarlanmamışsa , fatura tek bir fatura olarak deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="1d0f2-110">Fatura bölme gerçekleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="1d0f2-111">Fatura satırlarının farklı teslimat adresleri ve TAN'ları bulunan bir sevk irsaliyesini ayırmak ve deftere nakletmek için **Teslimat bilgileri**'nin **Sevk irsaliyesi** seçeneğini **Evet** olarak ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="1d0f2-112">Fatura satırlarının farklı teslimat adresleri ve TAN'ları bulunan bir faturayı ayırmak ve deftere nakletmek için **Teslimat bilgileri**'nin **Fatura** seçeneğini **Evet** olarak ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="1d0f2-113">Fatura satırlarının teslimat adresleri farklı olup TAN'ları aynı olan faturayı ayırmak ve deftere nakletmek için **Teslimat bilgileri**'nin **Fatura** seçeneğini **Hayır** olarak ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="1d0f2-114">Fatura, teslimat adresine göre bölünür.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="1d0f2-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="1d0f2-115">Example</span></span>

<span data-ttu-id="1d0f2-116">Bu örnekte, **Teslimat bilgileri**'nin **Fatura** seçeneği **Borç hesapları parametreleri** sayfasındaki **Özet güncelleştirmesi** sekmesinde **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="1d0f2-117">Satırlarda teslimat adresleri ve TAN'ları için aşağıdaki ayarlara sahip olan bir satınalma faturası deftere nakledilir:</span><span class="sxs-lookup"><span data-stu-id="1d0f2-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="1d0f2-118">**Madde satırı 1:** Teslimat adresi 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="1d0f2-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="1d0f2-119">**Madde satırı 2:** Teslimat adresi 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="1d0f2-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="1d0f2-120">**Madde satırı 3:** Teslimat adresi 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="1d0f2-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="1d0f2-121">**Madde satırı 4:** Teslimat adresi 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="1d0f2-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="1d0f2-122">Bu durumda, orijinal fatura iki faturaya bölünür ve aşağıdaki şekilde deftere nakledilir:</span><span class="sxs-lookup"><span data-stu-id="1d0f2-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="1d0f2-123">İki satırın da teslimat adresi ve TAN'ı aynı olduğu için Fatura 1 madde satırı 1 ve madde satırı 2 için deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="1d0f2-124">Fatura 2, madde satırı 3 için deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="1d0f2-125">Fatura 3, madde satırı 4 için deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="1d0f2-125">Invoice 3 is posted for item line 4.</span></span>
