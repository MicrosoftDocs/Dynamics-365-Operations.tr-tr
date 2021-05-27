---
title: Satıcılar ve müşteriler için TDS grubu, PAN ve TAN bilgilerini ayarlama
description: Bu konu, satıcı ve müşteriler için Kaynakta Kesilen Vergi (TDS) grubu, kalıcı hesap numarası (PAN) ve vergi hesap numarası (TAN) hakkında bilgilerin nasıl ayarlanacağını açıklamaktadır.
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023659"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="09568-103">Satıcılar ve müşteriler için TDS grubu, PAN ve TAN bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="09568-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09568-104">Bu konu, satıcı ve müşteriler için Kaynakta Kesilen Vergi (TDS) grubu, kalıcı hesap numarası (PAN) ve vergi hesap numarası (TAN) hakkında bilgilerin nasıl ayarlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="09568-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="09568-105">**Borç hesapları \> Satıcılar \> Tüm satıcılar** veya **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="09568-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="09568-106">[![Tüm satıcılar sayfası](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="09568-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="09568-107">Eylem bölmesinde, satıcı veya müşteri oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="09568-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="09568-108">Alternatif olarak, varolan bir satıcı veya müşteriyi de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09568-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="09568-109">**Fatura ve teslimat** hızlı sekmesinde, **Stopaj vergisi** bölümünde, satıcı veya müşteri için stopaj vergisi, TDS veya Kaynakta Tahsil Edilen Vergiyi (TCS) hesaplamak için **Stopaj vergisini hesapla** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="09568-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="09568-110">Satınalma faturasının TDS'si, satıcı veya müşteri için tanımlanan varsayılan TDS grubu temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="09568-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="09568-111">**TDS grubu** alanında varsayılan TDS grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="09568-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="09568-112">**TDS grubu** alanında bir TDS grubunu seçtiğinizde, **Stopaj vergisi grubu** ve **TCS grubu** alanları kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="09568-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="09568-113">**Vergi bilgileri** hızlı sekmesinde, **PAN bilgileri** bölümünde, **Durum** alanında, satıcı veya müşteri için kalıcı hesap numarasının durumunu seçin:</span><span class="sxs-lookup"><span data-stu-id="09568-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="09568-114">**Mevcut değil** – Satıcı veya müşterinin bir PAN'ı yok.</span><span class="sxs-lookup"><span data-stu-id="09568-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="09568-115">**Alındı** – Satıcı veya müşterinin bir PAN'ı var.</span><span class="sxs-lookup"><span data-stu-id="09568-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="09568-116">**Başvurdu** – Satıcı veya müşteri, bir PAN için başvuruda bulunmuş.</span><span class="sxs-lookup"><span data-stu-id="09568-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="09568-117">**Geçersiz** – Satıcı veya müşterinin bir PAN'ı var ancak bu PAN geçerli değil.</span><span class="sxs-lookup"><span data-stu-id="09568-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="09568-118">Satıcının veya müşterinin bir PAN'ı olduğunu göstermek üzere **Durum** alanında **Alındı** seçeneğini belirlediyseniz PAN değerini **Numara** alanına girin.</span><span class="sxs-lookup"><span data-stu-id="09568-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="09568-119">PAN beş alfabetik karakterden, dört sayısal karakterden ve ardından tek bir alfabetik karakterden oluşmalıdır.</span><span class="sxs-lookup"><span data-stu-id="09568-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="09568-120">Aşağıda bir örnek verilmiştir: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="09568-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="09568-121">Satıcının veya müşterinin bir PAN için başvuruda bulunduğunu göstermek üzere **Durum** alanında **Başvurdu** seçeneğini belirlediyseniz referans numarasını **Referans numarası** alanına girin.</span><span class="sxs-lookup"><span data-stu-id="09568-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="09568-122">**Değerlendirilenin yapısı** alanında, satıcı veya müşterinin ait olduğu değerlendirilen yapısı kategorisini seçin:</span><span class="sxs-lookup"><span data-stu-id="09568-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="09568-123">Şirket</span><span class="sxs-lookup"><span data-stu-id="09568-123">Company</span></span>
    - <span data-ttu-id="09568-124">HUF</span><span class="sxs-lookup"><span data-stu-id="09568-124">HUF</span></span>
    - <span data-ttu-id="09568-125">Kesinleştir</span><span class="sxs-lookup"><span data-stu-id="09568-125">Firm</span></span>
    - <span data-ttu-id="09568-126">Tek tek</span><span class="sxs-lookup"><span data-stu-id="09568-126">Individual</span></span>
    - <span data-ttu-id="09568-127">AOP</span><span class="sxs-lookup"><span data-stu-id="09568-127">AOP</span></span>
    - <span data-ttu-id="09568-128">BOI</span><span class="sxs-lookup"><span data-stu-id="09568-128">BOI</span></span>
    - <span data-ttu-id="09568-129">Yerel makam</span><span class="sxs-lookup"><span data-stu-id="09568-129">Local authority</span></span>
    - <span data-ttu-id="09568-130">Diğerleri</span><span class="sxs-lookup"><span data-stu-id="09568-130">Others</span></span>

    <span data-ttu-id="09568-131">[![Vergi bilgileri hızlı sekmesi](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="09568-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="09568-132">Eylem Bölmesinde, **Satıcı** sekmesinde, **Kayıt** grubunda, **Adresleri yönet** sayfasını açmak için **Kayıt Kimlikleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="09568-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="09568-133">**Adresleri yönet** sayfasında, **Vergi bilgileri** hızlı sekmesinde, vergi kayıt girişlerini yönetebildiğiniz **Vergi bilgilerini yönet** sayfasını açmak için **Ekle** veya **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="09568-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="09568-134">**Vergi bilgilerini yönet** sayfasında, **Stopaj vergisi** hızlı sekmesinde, **Vergi Hesap Numarası (TAN)** alanında, TAN'ı girin.</span><span class="sxs-lookup"><span data-stu-id="09568-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="09568-135">TAN dört alfabetik karakterden, beş sayısal karakterden ve ardından tek bir alfabetik karakterden oluşmalıdır.</span><span class="sxs-lookup"><span data-stu-id="09568-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="09568-136">Aşağıda bir örnek verilmiştir: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="09568-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="09568-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="09568-137">Close the page.</span></span>
