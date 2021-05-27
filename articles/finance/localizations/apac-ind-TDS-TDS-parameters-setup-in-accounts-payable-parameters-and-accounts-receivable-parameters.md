---
title: Borç hesapları ve Alacak hesaplarında TDS parametrelerini ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) kesintilerini desteklemek için Borç hesapları ve Alacak hesaplarının parametrelerinin nasıl ayarlanacağını açıklar.
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023658"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="c9a64-103">Borç hesapları ve Alacak hesaplarında TDS parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c9a64-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9a64-104">Bu konu, Kaynakta Kesilen Vergi (TDS) kesintilerini desteklemek için Borç hesapları ve Alacak hesaplarının parametrelerinin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c9a64-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="c9a64-105">**Vergi \> Kurulum \> Parametreler \> Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c9a64-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="c9a64-106">**Güncelleştirmeler** sekmesinde, **Sipariş satırlarını güncelleştir** iletişim kutusunu açmak için **Sipariş satırlarını güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c9a64-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="c9a64-107">**TDS grubu** bölümünde, **TDS grubunu güncelleştirme** alanında, satır düzeyinde TDS grubunu güncelleştirmek için kullanılacak yöntemi belirtin.</span><span class="sxs-lookup"><span data-stu-id="c9a64-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="c9a64-108">Bu ayar, bir sipariş başlığında TDS grubu güncelleştirildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c9a64-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="c9a64-109">Aşağıdaki seçenekler bulunur:</span><span class="sxs-lookup"><span data-stu-id="c9a64-109">The following options are available:</span></span>

    - <span data-ttu-id="c9a64-110">**Hiçbir zaman** – TDS grubu sipariş başlığında güncelleştirildiğinde, sipariş satırlarında güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="c9a64-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="c9a64-111">**Her zaman** – TDS grubu sipariş başlığında güncelleştirildiğinde, sipariş satırlarında otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c9a64-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="c9a64-112">**İstek** – Kullanıcılar, sipariş satırlarında TDS grubunu güncelleştirmelerini isteyen bir ileti alır.</span><span class="sxs-lookup"><span data-stu-id="c9a64-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="c9a64-113">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c9a64-113">Select **OK**.</span></span>

    <span data-ttu-id="c9a64-114">[![Sipariş satırlarını güncelleştirme iletişim kutusu](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="c9a64-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="c9a64-115">**Vergi \> Kurulum \> Parametreler \> Borç hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c9a64-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="c9a64-116">**Genel** sekmesinde **Teslimat bilgilerine göre böl** hızlı sekmesinde, farklı teslimat adresleri ve vergi hesap numaraları (TAN'lar) olan bir ürün girişini nakletmek ve bölmek için **Ürün girişi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c9a64-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="c9a64-117">Bu seçenek **Hayır** olarak ayarlanırsa, farklı teslimat adresleri ve TAN'ları bulunan bir satınalma sevk irsaliyesini deftere nakledemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9a64-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="c9a64-118">Farklı teslimat adresleri ve TAN'ları olan bir satınalma faturasını deftere nakletmek ve bölmek için **Fatura** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c9a64-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="c9a64-119">[![Teslimat bilgilerine göre böl hızlı sekmesi](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="c9a64-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="c9a64-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c9a64-120">Close the page.</span></span>
