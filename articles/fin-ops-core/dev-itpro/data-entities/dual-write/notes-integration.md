---
title: Not tümleştirmesi
description: Bu konu çift yazmada not verisinin tümleştirmesini açıklar.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: beab7f2fc4fd96ce7a28734d2449445b3b5d4451
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750848"
---
# <a name="note-integration"></a><span data-ttu-id="2f546-103">Not tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="2f546-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2f546-104">İş süreçleri sırasında, Microsoft Dynamics 365 kullanıcıları genellikle müşterileri hakkında bilgi toplar.</span><span class="sxs-lookup"><span data-stu-id="2f546-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="2f546-105">Bu bilgiler aktiviteler ve notlar olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2f546-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="2f546-106">Bu konu çift yazmada not verisinin tümleştirmesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="2f546-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="2f546-107">Müşteri bilgileri aşağıdaki yollarla sınıflandırılabilir:</span><span class="sxs-lookup"><span data-stu-id="2f546-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="2f546-108">**Bir Dynamics 365 kullanıcısının bir müşteri adına işlediği eyleme dönüştürülebilen bilgiler**: Örneğin, Contoso (bir Dynamics 365 kullanıcısı) bir oyun gösterisi yürütüyor.</span><span class="sxs-lookup"><span data-stu-id="2f546-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="2f546-109">Contoso müşterilerinden biri (bir müşteri) oyun gösterisine katılmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="2f546-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="2f546-110">Müşteri, bir contoso çalışanından kendisi için oyun gösterisinde bir yer ayırtmasını istiyor.</span><span class="sxs-lookup"><span data-stu-id="2f546-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="2f546-111">Kayıt, Contoso'nun etkinlik katılımcı takvimine işleniyor.</span><span class="sxs-lookup"><span data-stu-id="2f546-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="2f546-112">**Bir Dynamics 365 kullanıcısı için eyleme dönüştürülebilen bilgiler**: Örneğin, bir Surface birimi satın alan bir müşteri, cihazın teslim edilmeden önce hediye paketi yapılmasını belirten özel talimatlar giriyor.</span><span class="sxs-lookup"><span data-stu-id="2f546-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="2f546-113">Bu talimatlar paketlemeden sorumlu olan Contoso çalışanı tarafından işlenmesi gereken, eyleme dönüştürülebilen bilgilerdir.</span><span class="sxs-lookup"><span data-stu-id="2f546-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="2f546-114">**Eyleme dönüştürülemeyen bilgiler**: Örneğin, bir müşteri Contoso mağazasını ziyaret eder ve mağaza görevlisiyle konuşmaları sırasında *Halo* oyunları ve oyun aksesuarlarıyla ilgilendiğini ifade eder.</span><span class="sxs-lookup"><span data-stu-id="2f546-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="2f546-115">Mağaza görevlisi bu bilgiyi not eder.</span><span class="sxs-lookup"><span data-stu-id="2f546-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="2f546-116">Daha sonra, ürün öneri altyapısı bunu müşteriye önerilerde bulunmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="2f546-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="2f546-117">Genel olarak, eyleme dönüştürülebilen bilgiler, Finance and Operations uygulamalardaki ve customer engagement uygulamalarında *etkinlikler* olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2f546-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="2f546-118">Eyleme dönüştürülemeyen bilgiler, Finance and Operations uygulamalarda *notlar* ve customer engagement uygulamalarında *ek açıklamalar* olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2f546-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="2f546-119">Notlar, eyleme dönüştürülemeyen bilgiler için düşünülse de, uygulamalar bu notları bu şekilde kullanmak isterseniz bunları kaydedip eyleme dönüştürülebilir bilgi olarak kullanmanızı engellemez.</span><span class="sxs-lookup"><span data-stu-id="2f546-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="2f546-120">Microsoft, şu anda not tümleştirme işlevini yayımlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2f546-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="2f546-121">(Faaliyet entegrasyonu işlevi daha sonra yayımlanacaktır.) Not Tümleştirme, müşteriler, satıcılar, satış siparişleri ve satın alma siparişleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2f546-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="2f546-122">Customer engagement uygulamasında bir not oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f546-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="2f546-123">Bir customer engagement uygulamasında bir not oluşturmak ve sonra bir Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f546-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="2f546-124">Customer engagement uygulamasında bir müşteri için hesap kaydı açın.</span><span class="sxs-lookup"><span data-stu-id="2f546-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="2f546-125">**Zaman çizelgesi** bölmesinde artı işaretini (**+**) seçin ve sonra Not oluşturmak için **Not**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f546-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Customer engagement uygulamasında bir not oluşturma](media/notes-ce-1.png)

3. <span data-ttu-id="2f546-127">Bir başlık ve açıklama girin ve sonra **Not ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f546-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Bir başlık ve açıklama girme](media/notes-ce-2.png)

    <span data-ttu-id="2f546-129">Yeni Not Müşteri zaman çizelgesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="2f546-129">The new note is added to the customer timeline.</span></span>

    ![Müşteri zaman çizelgesindeki yeni Not](media/notes-ce-3.png)

4. <span data-ttu-id="2f546-131">Finance and Operations uygulamasında oturum açın ve aynı müşteri kaydını açın.</span><span class="sxs-lookup"><span data-stu-id="2f546-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="2f546-132">Sağ üst köşedeki **ekler** düğmesi (ataş simgesi) kaydın bir eki olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f546-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Ek hakkında bildirim](media/notes-ce-4.png)

5. <span data-ttu-id="2f546-134">**Ekler** sayfasını açmak için **ekler** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f546-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="2f546-135">Customer engagement uygulamasında oluşturduğunuz notu bulmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f546-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Customer engagement uygulamasındaki not](media/notes-ce-5.png)

<span data-ttu-id="2f546-137">Notta yapılan güncelleştirmeler, Finance and Operations uygulaması ve customer engagement uygulaması arasında eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="2f546-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="2f546-138">Finance and Operations uygulamasında bir not oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f546-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="2f546-139">Finance and Operations uygulamasında da bir not oluşturabilirsiniz ve bu not customer engagement uygulamasıyla eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="2f546-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="2f546-140">Finance and Operations uygulamasında bir not oluşturmak ve sonra notu bir customer engagement uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f546-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="2f546-141">Finance and Operations uygulamasında **ekler** sayfasında, **Yeni** \> **Not**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f546-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Finance and Operations uygulamasında bir not oluşturma](media/notes-fo-1.png)

2. <span data-ttu-id="2f546-143">Bir başlık ve kısa bir yönerge kümesi girip **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f546-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Bir başlık ve yönerge girme](media/notes-fo-2.png)

3. <span data-ttu-id="2f546-145">Customer engagement uygulamasında kaydı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2f546-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="2f546-146">Yeni notu zaman çizelgesinde bulmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f546-146">You should find the new note on the timeline.</span></span>

    ![Customer engagement uygulamasında zaman çizelgesindeki yeni Not](media/notes-fo-3.png)

<span data-ttu-id="2f546-148">Bir notu dahili veya harici olarak sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f546-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="2f546-149">Finance and Operations uygulamasında, **ekler** sayfasında notu açın ve sonra **sınırlama** alanında **dahili** veya **harici** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f546-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Sınırlama alanı](media/notes-fo-4.png)

<span data-ttu-id="2f546-151">Ayrıca bir URL oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f546-151">You can also create a URL.</span></span>

1. <span data-ttu-id="2f546-152">Finance and Operations uygulamasında **ekler** sayfasında, **Yeni** \> **URL**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f546-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="2f546-153">Bir başlık ve URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="2f546-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="2f546-154">**Sınırlama** alanında, **dahili** veya **harici** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f546-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Finance and Operations uygulamasında bir URL oluşturma](media/notes-fo-5.png)

4. <span data-ttu-id="2f546-156">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f546-156">Select **Save**.</span></span>

    <span data-ttu-id="2f546-157">Customer engagement uygulamalarının URL türleri olmadığından, URL not olarak çift yazmayla tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2f546-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![Customer engagement uygulamasında not olarak görünen URL](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="2f546-159">Dosya ekleri desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="2f546-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="2f546-160">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="2f546-160">Templates</span></span>

<span data-ttu-id="2f546-161">Not tümleştirmesi aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir tablo eşlemeleri koleksiyonu içerir.</span><span class="sxs-lookup"><span data-stu-id="2f546-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="2f546-162">Finance and Operations Uygulaması</span><span class="sxs-lookup"><span data-stu-id="2f546-162">Finance and Operations app</span></span> | <span data-ttu-id="2f546-163">Müşteri etkileşimi uygulaması</span><span class="sxs-lookup"><span data-stu-id="2f546-163">Customer engagement app</span></span> | <span data-ttu-id="2f546-164">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f546-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="2f546-165">Müşteri ekleri</span><span class="sxs-lookup"><span data-stu-id="2f546-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="2f546-166">Ek açıklamalar</span><span class="sxs-lookup"><span data-stu-id="2f546-166">Annotations</span></span> | <span data-ttu-id="2f546-167">Müşteriye özel bilgileri (hem kuruluşlar, hem de kişiler için) yakalamak üzere düz metin ve URL kullanan işletmeler.</span><span class="sxs-lookup"><span data-stu-id="2f546-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="2f546-168">Satıcı belgesi ekleri</span><span class="sxs-lookup"><span data-stu-id="2f546-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="2f546-169">Ek açıklamalar</span><span class="sxs-lookup"><span data-stu-id="2f546-169">Annotations</span></span> | <span data-ttu-id="2f546-170">Satıcıya özel bilgileri (hem kuruluşlar, hem de kişiler için) yakalamak üzere düz metin ve URL kullanan işletmeler.</span><span class="sxs-lookup"><span data-stu-id="2f546-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="2f546-171">Satış siparişi başlığı belge ekleri</span><span class="sxs-lookup"><span data-stu-id="2f546-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="2f546-172">Ek açıklamalar</span><span class="sxs-lookup"><span data-stu-id="2f546-172">Annotations</span></span> | <span data-ttu-id="2f546-173">Satış siparişi ile ilgili bilgileri yakalamak için düz metin ve URL kullanan işletmeler.</span><span class="sxs-lookup"><span data-stu-id="2f546-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="2f546-174">Satın alma siparişi başlığı belge ekleri</span><span class="sxs-lookup"><span data-stu-id="2f546-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="2f546-175">Ek açıklamalar</span><span class="sxs-lookup"><span data-stu-id="2f546-175">Annotations</span></span> | <span data-ttu-id="2f546-176">Satın alma siparişi ile ilgili bilgileri yakalamak için düz metin ve URL kullanan işletmeler.</span><span class="sxs-lookup"><span data-stu-id="2f546-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="2f546-177">Daha fazla bilgi için, bkz. [Çift yazma eşleme başvurusu](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2f546-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
