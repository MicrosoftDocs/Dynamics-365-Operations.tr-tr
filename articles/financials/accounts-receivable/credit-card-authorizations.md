---
title: "Kredi kartı ayarlama, onaylama ve tutma"
description: "Bu makale, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da kredi kartı onayına genel bakışı sağlar. Nasıl ödeme hizmeti ayarlanacağı, satış emrine kredi kartı ekleneceği ve yetkilendirme iptal edileceğine dair bilgiler içerir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, Core, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 40d636cac477871f094286d29edc32cd5616ad44
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="9e923-104">Kredi kartı ayarlama, onaylama ve tutma</span><span class="sxs-lookup"><span data-stu-id="9e923-104">Credit card setup, authorization, and capture</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="9e923-105">Bu makale, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da kredi kartı onayına genel bakışı sağlar.</span><span class="sxs-lookup"><span data-stu-id="9e923-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="9e923-106">Nasıl ödeme hizmeti ayarlanacağı, satış emrine kredi kartı ekleneceği ve yetkilendirme iptal edileceğine dair bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="9e923-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="9e923-107">Kredi kartı ödeme hizmeti ayarlama</span><span class="sxs-lookup"><span data-stu-id="9e923-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="9e923-108">Kredi kartlarını kullanmak için, Ödeme hizmetleri sayfasından bir ödeme hizmeti ayarlamanız ve etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9e923-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="9e923-109">Ödeme hizmeti, tüzel kişiliğiniz ile müşterinin kredi kartı harcamalarını işleyen banka arasında bir köprü olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="9e923-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="9e923-110">Ödeme bağlayıcı alanında listelenen bir kredi kartı sağlayıcısıyla çalışmanız ve bu sağlayıcıyla bir hesap kurmanız gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="9e923-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="9e923-111">Ardından Ödeme hizmetleri sayfasında diğer seçenekleri belirlemeniz, Kredi kartı türleri sayfasında American Express, Discover, MasterCard ve Discover için kredi kartı türlerini ayarlamanız ve sağlayıcıyı varsayılan sağlayıcı olarak etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9e923-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="9e923-112">Ayrıca, ayarları tamamlamak için aşağıdaki adımları izlemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="9e923-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="9e923-113">Alacak hesapları parametreleri sayfasında, kredi kartı onaylarını kullanmak için parametreleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="9e923-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="9e923-114">Ödeme koşulları sayfasında, kredi kartları için ödeme koşullarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9e923-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="9e923-115">Ödeme türü alanında Kredi kartı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9e923-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="9e923-116">Müşteri kredi kartları sayfasında, müşteriler için kredi kartı bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="9e923-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="9e923-117">Yeni kredi kartı ekleme</span><span class="sxs-lookup"><span data-stu-id="9e923-117">Adding a new credit card</span></span>
<span data-ttu-id="9e923-118">Müşteri, Ayar, Kredi kartı öğelerini kullanarak Müşteriler sayfasında yeni kredi kartı kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e923-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="9e923-119">Ayrıca, Satış siparişi sayfasında siparişleri girerken Yönet, Müşteri, Kredi kartı, Kaydet öğelerini kullanarak da kredi kartı kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e923-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>
<span data-ttu-id="9e923-120">Bir satış siparişine kredi kartı ekleme</span><span class="sxs-lookup"><span data-stu-id="9e923-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="9e923-121">Satış siparişi sayfasındaki Fiyat ve iskontolar hızlı sekmesindeki kredi kartı arama alanından bir kredi kartı seçerek satış siparişine kredi kartı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e923-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="9e923-122">Onay işlemini başlatmak için, Eylem Bölmesindeki Yönet sekmesinde Kredi kartı ve Onay öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="9e923-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>
<span data-ttu-id="9e923-123">Kredi kartını onaylama</span><span class="sxs-lookup"><span data-stu-id="9e923-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="9e923-124">Bir kredi kartı onaylanırken, kart numarası ve kart sahibinin adı doğrulanır ve kullanılabilir kredi bakiyesi onaylanır.</span><span class="sxs-lookup"><span data-stu-id="9e923-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="9e923-125">İsteğe bağlı olarak, kart doğrulama değeri ve kart sahibinin adresi de doğrulanabilir.</span><span class="sxs-lookup"><span data-stu-id="9e923-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="9e923-126">Ardından, müşterinin kullanılabilir kredi bakiyesinden fatura tutarı düşülür.</span><span class="sxs-lookup"><span data-stu-id="9e923-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="9e923-127">Ödeme hizmeti, kredi kartının onaylandığı ya da reddedildiği bilgisini gönderir.</span><span class="sxs-lookup"><span data-stu-id="9e923-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="9e923-128">Satış siparişi faturalandırıldığında, kredi kartı fatura tutarı ile borçlandırılır (tutulan).</span><span class="sxs-lookup"><span data-stu-id="9e923-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="9e923-129">Kart doğrulama değeri</span><span class="sxs-lookup"><span data-stu-id="9e923-129">Card verification value</span></span>

<span data-ttu-id="9e923-130">Bazen kredi kartı güvenlik kodu olarak belirtilen kart doğrulama değerini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e923-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="9e923-131">Bu, American Express için dört basamaklı bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="9e923-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="9e923-132">Discover, MasterCard ve Visa için bu değer üç basamaklıdır.</span><span class="sxs-lookup"><span data-stu-id="9e923-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="9e923-133">Adres doğrulama</span><span class="sxs-lookup"><span data-stu-id="9e923-133">Address verification</span></span>

<span data-ttu-id="9e923-134">Adres doğrulama bilgileri her zaman ödeme sağlayıcısına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="9e923-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="9e923-135">Bir hareketi kabul edilmesi için ne kadar bilginin gerekli olduğuna karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e923-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="9e923-136">Sağlayıcınızın bu bilgileri kabul edip edemeyeceğini kontrol ettiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="9e923-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="9e923-137">Adres doğrulama seçenekleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9e923-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="9e923-138">**Hareketi her zaman kabul et** – Adres doğrulama sonucuna bakılmaksınız hareketi kabul et.</span><span class="sxs-lookup"><span data-stu-id="9e923-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="9e923-139">**Hesap sahibi** – Harekette belirtilen kart sahibi adını kredi kartı şirketinin bilgileriyle karşılaştır.</span><span class="sxs-lookup"><span data-stu-id="9e923-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="9e923-140">**Fatura adresi** – Harekette belirtilen kart sahibi adını ve fatura adresini kredi kartı şirketinin bilgileriyle karşılaştır.</span><span class="sxs-lookup"><span data-stu-id="9e923-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="9e923-141">**Fatura posta kodu** – Harekette belirtilen kart sahibi adını, fatura adresini ve posta kodunu kredi kartı şirketinin bilgileriyle karşılaştır.</span><span class="sxs-lookup"><span data-stu-id="9e923-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="9e923-142">Veri desteği</span><span class="sxs-lookup"><span data-stu-id="9e923-142">Data support</span></span>
<span data-ttu-id="9e923-143">Desteklenen her kredi kartı türü için veri desteği düzeyini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e923-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="9e923-144">Bu düzey, bir hareketle ilgili ne kadar bilginin ödeme hizmetine aktarılacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="9e923-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="9e923-145">Sağlayıcınızın bu bilgileri sunup sunamayacağını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="9e923-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="9e923-146">Veri desteği düzeyi seçenekleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9e923-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="9e923-147">**Düzey 1** – Hareket tarihini, hareket tutarını ve açıklamayı aktar.</span><span class="sxs-lookup"><span data-stu-id="9e923-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="9e923-148">**Düzey 2** – Düzey 1'deki bilgilere ek olarak sevkiyat ve tüccar adresleri ile vergi bilgilerini aktar.</span><span class="sxs-lookup"><span data-stu-id="9e923-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="9e923-149">**Düzey 3** – Düzey 2'deki tüm bilgilere ek olarak sipariş satırı bilgilerini de aktar.</span><span class="sxs-lookup"><span data-stu-id="9e923-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="9e923-150">Kısmi ödemeler</span><span class="sxs-lookup"><span data-stu-id="9e923-150">Partial payments</span></span>
<span data-ttu-id="9e923-151">Bir siparişin parçası olarak gönderirseniz, kısmi siparişin tutarı yakalanır ve tüm siparişin tutarı için olan yetkilendirme, kapatılır.</span><span class="sxs-lookup"><span data-stu-id="9e923-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="9e923-152">Daha sonra yeni bir yetkilendirme, gönderilmemiş olan siparişin bir kalan tutarı için gönderilir.</span><span class="sxs-lookup"><span data-stu-id="9e923-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="9e923-153">Onayı hükümsüz kılma </span><span class="sxs-lookup"><span data-stu-id="9e923-153">Voiding an authorization</span></span>
<span data-ttu-id="9e923-154">Kredi kartı onayını hükümsüz kılmak için, ödeme türü Kredi kartı olmayan başka bir ödeme yöntemi belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e923-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>






