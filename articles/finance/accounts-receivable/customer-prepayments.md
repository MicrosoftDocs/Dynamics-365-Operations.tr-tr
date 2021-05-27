---
title: Müşteri ön ödemeleri
description: Bu konu, müşteri ön ödemelerinin (müşteri mevduatı olarak da bilinir) nasıl ayarlanacağını ve işleneceği açıklamaktadır.
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019432"
---
# <a name="customer-prepayments"></a><span data-ttu-id="746e2-103">Müşteri ön ödemeleri</span><span class="sxs-lookup"><span data-stu-id="746e2-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="746e2-104">Müşteri ön ödemeleri, bir müşteriden ödeme aldığınızda ancak ödemeyle ilgili olarak kapatılabilecek bir fatura olmadığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="746e2-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="746e2-105">Bu ödeme türleri, müşteri mevduatları olarak da adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="746e2-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="746e2-106">Müşteri ön ödemelerinin ayarlanması ve bunlarla çalışmak, aşağıdaki temel adımlardan oluşur.</span><span class="sxs-lookup"><span data-stu-id="746e2-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="746e2-107">Ön ödemeler için müşteri deftere nakil profili oluşturun.</span><span class="sxs-lookup"><span data-stu-id="746e2-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="746e2-108">**Ön ödeme günlüğü fişi için nakil profili** parametresini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="746e2-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="746e2-109">Bir müşteri ödeme günlüğü oluşturun ve her satırda **Ön ödeme günlüğü fişi** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="746e2-110">Müşteri ödeme günlüğünü naklet.</span><span class="sxs-lookup"><span data-stu-id="746e2-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="746e2-111">Bir fatura oluşturulduktan sonra, **Açık hareketleri kapat** sayfasını kullanarak bu ön ödemeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="746e2-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="746e2-112">Ön ödemeler için müşteri deftere nakil profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="746e2-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="746e2-113">Genellikle, mal veya servisler teslim edilmeden veya sisteminizde bir fatura var olmadan önce müşteriden ön ödeme veya mevduat kabul ettiğinizde, hesap planında nakiti varlık olarak değil borç olarak kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="746e2-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="746e2-114">Ancak, bu tutarların genel muhasebenizdeki kayıt gereksinimleri ülkenize veya bölgenize göre farklılık gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="746e2-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="746e2-115">Bu nedenle, ilgili tüm yerel düzenlemeler hakkında muhasebecinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="746e2-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="746e2-116">Genel olarak, ön ödemeler için kullanılabilecek bir deftere nakil profili oluşturma işlemi, diğer deftere nakil profillerini oluşturma işlemiyle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="746e2-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="746e2-117">Temel fark, **Özet hesap** alanında seçtiğiniz ana hesaptır.</span><span class="sxs-lookup"><span data-stu-id="746e2-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="746e2-118">Daha fazla bilgi için [Müşteri deftere nakil profilleri](customer-posting-profiles.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="746e2-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="746e2-119">Müşteri ön ödemeleri için parametreleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="746e2-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="746e2-120">Müşteri ön ödemeleri için sistemi yapılandırırken dikkate almanız gereken iki ana alacak hesabı parametresi vardır.</span><span class="sxs-lookup"><span data-stu-id="746e2-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="746e2-121">Parametreleri yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="746e2-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="746e2-122">**Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="746e2-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="746e2-123">İsteğe bağlı: **Genel muhasebe ve satış vergisi** sekmesinde, **Ödeme** hızlı sekmesinde, **Ön ödeme günlüğü fişinde satış vergisi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="746e2-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="746e2-124">**Ön ödeme günlüğü fişiyle nakil profili** alanında, müşteri ön ödemeleri deftere nakledildiğinde kullanılacak müşteri nakil profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="746e2-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="746e2-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="746e2-126">Müşteri ön ödeme fişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="746e2-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="746e2-127">Müşteri ödeme günlüğünü oluşturduğunuzda, her ön ödeme için, **Müşteri ödeme günlüğü** sayfasında **Ön ödeme günlüğü fişi** seçeneğini **Evet** olarak ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="746e2-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="746e2-128">Müşteri ön ödemesi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="746e2-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="746e2-129">**Alacak hesapları \> Ödemeler \> Müşteri ödeme günlüğü** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="746e2-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="746e2-130">Bir günlük oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="746e2-131">**Ad** alanında, kullanılacak günlük adını seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="746e2-132">Önceki prosedürde **Ön ödeme günlüğü fişinde satış vergisi** seçeneğini **Evet** olarak ayarladıysanız, **Tutara satış vergisi dahildir** parametresinin seçili olduğu bir günlük adı seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="746e2-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="746e2-133">İsteğe bağlı: **Açıklama** alanına ayrıntılı bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="746e2-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="746e2-134">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-134">Select **Lines**.</span></span>
6. <span data-ttu-id="746e2-135">Boş bir satır yoksa, bir satır oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="746e2-136">**Tarih** alanına, ön ödemenin deftere nakledilmesi gereken tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="746e2-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="746e2-137">**Hesap** alanında, ön ödemenin müşterisini seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="746e2-138">İsteğe bağlı: **Açıklama** alanına hareketin ayrıntılı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="746e2-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="746e2-139">**Alacak** alanına, ön ödeme tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="746e2-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="746e2-140">**Mahsup hesabı** alanında, ödemenin mahsup edileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="746e2-141">Örneğin, ödemenin nakledileceği banka veya ana hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="746e2-142">**Ödeme yöntemi** alanında, müşterinin ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="746e2-143">**Ödeme** sekmesinde, **Ön ödeme günlüğü fişi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="746e2-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="746e2-144">Deftere nakledilmesi gereken her ek ön ödeme için 7 ile 13 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="746e2-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="746e2-145">Günlüğü tamamlamak için **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="746e2-146">Ön ödemeleri faturalarla kapatma</span><span class="sxs-lookup"><span data-stu-id="746e2-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="746e2-147">Tam olarak kapatılmayan ödemeleri kolayca bulmak ve kapatmak için **Müşteri ödemeleri** çalışma alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="746e2-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="746e2-148">**Giriş** panosunda, **Müşteri ödemeleri** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="746e2-149">**Müşteri hareketleri** bölümünde, **Ödemeler kapatılmadı** sekmesinde, kapatılacak ödemeyi arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="746e2-150">**Hareketleri kapat** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="746e2-151">Fatura ve kapatılacak ödeme için **İşaretle** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="746e2-152">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="746e2-152">Select **Post**.</span></span>

<span data-ttu-id="746e2-153">Açık hareketlerin nasıl kapatılacağı hakkında daha fazla bilgi için bkz. [Kapatmaya genel bakış](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="746e2-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
