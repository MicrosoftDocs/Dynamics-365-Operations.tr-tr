---
title: Elektronik imzalar
description: "Bu makale, elektronik imzalara genel bir bakış sunar ve Microsoft Dynamics 365 for Finance and Operations'da nasıl kullanılabileceklerini açıklar."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 676510ef503d51d914ba762e7ac15e2c4811c6ba
ms.contentlocale: tr-tr
ms.lasthandoff: 12/18/2018

---

# <a name="electronic-signatures"></a><span data-ttu-id="25ad6-103">Elektronik imzalar</span><span class="sxs-lookup"><span data-stu-id="25ad6-103">Electronic signatures</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25ad6-104">Bu makale, elektronik imzalara genel bir bakış sunar ve Microsoft Dynamics 365 for Finance and Operations'da nasıl kullanılabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="25ad6-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="25ad6-105">Elektronik imza nedir?</span><span class="sxs-lookup"><span data-stu-id="25ad6-105">What is an electronic signature?</span></span>

<span data-ttu-id="25ad6-106">Elektronik imza bir hesaplama işlemi başlatmak veya onaylamak üzere olan kişinin kimliğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="25ad6-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="25ad6-107">Bazı sektörlerde, elektronik imza yasal açıdan elle atılmış imza kadar bağlayıcı olmaktadır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="25ad6-108">Elektronik imzalar ilaç, yiyecek ile içecek ve havacılık ve uzay ile savunma sanayileri gibi birtakım kontrol altındaki sektörlerle ilgili yönetmeliklere uyumluluk gereklilikleridir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="25ad6-109">Aynı zamanda ABD'de İlaç ve Gıda Dairesi (FDA) tarafından yayınlanmış 21 CFR Bölüm 11'deki yönetmeliklere uygunluk açısından da gereklidir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="25ad6-110">Elektronik imza kendi başına dijital imzayla aynı değildir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="25ad6-111">Dijital imza başka güvenlik önlemleri de sağlarken, elektronik imza sadece el yazısı imzanın yerini tutar.</span><span class="sxs-lookup"><span data-stu-id="25ad6-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="25ad6-112">Dijital imza verilere başka bir kullanıcı veya işlem tarafından müdahale edilip edilmediğini belirlemeye yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="25ad6-113">Dijital imzalar da doğrulanabilir ve bu doğrulama, verilerin imzalanmasında kullanılan sertifikanın sahibi tarafından reddedilemez.</span><span class="sxs-lookup"><span data-stu-id="25ad6-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="25ad6-114">Aşağıda açıklandığı gibi, Microsoft Dynamics 365 for Finance and Operations'daki elektronik imzaların yerleşik dijital imza işlevleri vardır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="25ad6-115">Microsoft Dynamics 365 for Finance and Operations uygulamasındaki elektronik imzalar</span><span class="sxs-lookup"><span data-stu-id="25ad6-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>

<span data-ttu-id="25ad6-116">Finance and Operations uygulamasında önemli iş süreçleri için elektronik imza kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25ad6-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="25ad6-117">Bazı işlemler yerleşik elektronik imza özelliklerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="25ad6-118">Ayrıca herhangi bir veritabanı tablosu ve alanı için özel imza gereklilikleri de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25ad6-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="25ad6-119">Elektronik imzaların yerleşik dijital imza işlevleri vardır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="25ad6-120">Belge imzalayan her bir kullanıcı geçerli bir kriptografik sertifika edinmelidir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="25ad6-121">Bir belge imzalandığında, o sertifika ile ilişkilendirilmiş olan özel anahtar doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="25ad6-122">Finance and Operations, denetim kılavuzu sağlamak için elektronik imza bilgilerini bir günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="25ad6-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="25ad6-123">Elektronik imzaları ayarlamak için, bkz. [Elektronik imza ayarlama (Görev kılavuzu)](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="25ad6-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="25ad6-124">Elektronik imza erişimi gerektiren kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="25ad6-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="25ad6-125">Elektronik imzalara güvenlik erişimine genellikle üç tür kullanıcının ihtiyacı olur: elektronik imza yöneticileri, imzalayanlar ve elektronik imza denetçileri.</span><span class="sxs-lookup"><span data-stu-id="25ad6-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="25ad6-126">Elektronik imza yöneticisi</span><span class="sxs-lookup"><span data-stu-id="25ad6-126">Electronic signature administrator</span></span>

<span data-ttu-id="25ad6-127">Elektronik imza yöneticisi, imza gerekliliklerini, genel parametreleri ve onaylayanları ayarlar ve imza doğrulanamadığında uyarılar alır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="25ad6-128">Varsayılan olarak, **Bilgi teknolojisi yöneticisi** güvenlik rolüne ait olan bir kullanıcı, elektronik imza yönetimi iznine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="25ad6-129">İmzalayan</span><span class="sxs-lookup"><span data-stu-id="25ad6-129">Signer</span></span>

<span data-ttu-id="25ad6-130">İmzalayan, imza gereken belge ve işlemler için elektronik imza sağlar.</span><span class="sxs-lookup"><span data-stu-id="25ad6-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="25ad6-131">Varsayılan olarak, **Sistem kullanıcısı** güvenlik rolüne ait bir kullanıcı belgeleri elektronik olarak imzalama iznine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="25ad6-132">İmzalayan, imzalanan belge veya işlemle ilgili verilere erişim sağlanmadan önce ek izinlere gereksinim duyabilir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="25ad6-133">Verilerde değişiklik yapan ve ardından bu değişiklikler için imzası gereken bir kullanıcının verileri değiştirme izni olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="25ad6-134">Başka bir kullanıcı adına imzalayan kullanıcının verilere erişmesi gerekmeyebilir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="25ad6-135">Bu tür bir kullanıcıya örnek olarak çalışanın değişikliklerini imzalayan gözetmen verilebilir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="25ad6-136">Elektronik imza denetçisi</span><span class="sxs-lookup"><span data-stu-id="25ad6-136">Electronic signature auditor</span></span>

<span data-ttu-id="25ad6-137">Elektronik imza denetçisi veritabanı günlüğünü ve veritabanı günlüğünde bulunan imza inceleme günlüğünü gözden geçirir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="25ad6-138">Varsayılan olarak, **Bilgi teknolojisi yöneticisi** güvenlik rolüne ait olan bir kullanıcı, elektronik imza denetimi iznine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="25ad6-139">**Bilgi teknolojisi yöneticisi** dışında bir rol kullanıyorsanız, role aşağıdaki ayrıcalıkların atandığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="25ad6-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="25ad6-140">Elektronik imza hatalarını görüntüle</span><span class="sxs-lookup"><span data-stu-id="25ad6-140">View electronic signature failures</span></span>
- <span data-ttu-id="25ad6-141">Veritabanı günlüğünü görüntüle</span><span class="sxs-lookup"><span data-stu-id="25ad6-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="25ad6-142">Belgeleri elektronik olarak imzalama</span><span class="sxs-lookup"><span data-stu-id="25ad6-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="25ad6-143">Sertifika alma</span><span class="sxs-lookup"><span data-stu-id="25ad6-143">Get a certificate</span></span>

<span data-ttu-id="25ad6-144">Finance and Operations uygulamasında belgeleri elektronik olarak imzalamadan önce, bir sertifika istemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="25ad6-145">Finance and Operations sertifika oluşturmak ve elektronik imzalamaya olanak vermek için Microsoft SQL Server özelliklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-145">Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="25ad6-146">Başka sertifika veya ortak anahtar altyapısı (PKI) gerekmez.</span><span class="sxs-lookup"><span data-stu-id="25ad6-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="25ad6-147">Bir sertifika istediğinizde, Finance and Opeations veritabanında sizin için bir ortak anahtar ve bir özel anahtar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="25ad6-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="25ad6-148">Özel anahtar yalnızca sizin bildiğiniz bir parola kullanılarak şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="25ad6-149">Bir belgeyi elektronik olarak imzaladığınız zaman, parolanızı girdiğinizde kimliğiniz doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="25ad6-150">Sertifika istemek için, **Seçenekler** sayfasında **Hesaplar** sekmesinde **Sertifika al** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25ad6-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="25ad6-151">İmzalamak için kullanacağınız parolayı girmeli ve onaylamalısınız.</span><span class="sxs-lookup"><span data-stu-id="25ad6-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="25ad6-152">Parola, özel anahtarınızı korumak ve sertifika kullanımını yetkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="25ad6-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="25ad6-153">Bu parola, veritabanında saklanmaz ve Finance and Operations yöneticisi de dahil olmak üzere başka kimse tarafından kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="25ad6-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span>

<span data-ttu-id="25ad6-154">Sertifikanızla bağlantılı parolayı unutursanız, sertifikanın sıfırlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="25ad6-155">Sertifikayı sıfırlarsanız, önceki sertifikayı kullanarak imzaladığınız belgeleri etkilemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="25ad6-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="25ad6-156">Sertifikayı sıfırlamak için **Seçenekler** sayfasında **Sertifikayı sıfırla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25ad6-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="25ad6-157">Belgeyi elektronik olarak imzalama</span><span class="sxs-lookup"><span data-stu-id="25ad6-157">Sign a document electronically</span></span>

<span data-ttu-id="25ad6-158">Elektronik imza gerektiren bir değişiklik yaptığınızda **Belgeyi imzala** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="25ad6-159">Belgede yapılan değişiklikleri gözden geçirmek için **Belgeyi imzala** sayfasında **Belge** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25ad6-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="25ad6-160">**İmza** sekmesinde, bir neden kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="25ad6-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="25ad6-161">Açıklama gerekirse bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="25ad6-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="25ad6-162">Kullanıcı kimliğiniz **İmzalayan** alanında görünmezse, listeden seçin.</span><span class="sxs-lookup"><span data-stu-id="25ad6-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="25ad6-163">Bu bilgi gerekiyorsa, konumunuzu girin.</span><span class="sxs-lookup"><span data-stu-id="25ad6-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="25ad6-164">**Tamam** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25ad6-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="25ad6-165">Başka bir kullanıcının değişiklikleri için imzalama</span><span class="sxs-lookup"><span data-stu-id="25ad6-165">Sign for another user's changes</span></span>

<span data-ttu-id="25ad6-166">Bazen bir kullanıcının, başka bir kullanıcının değişiklikleri için imza atmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25ad6-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="25ad6-167">Örneğin, bir çalışanın ürün reçetelerinde yaptığı değişiklikler için bir gözetmenin imzalaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="25ad6-168">Bir Finance and Operations kullanıcısını başka bir kullanıcı için imzalayan olarak belirtmek için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="25ad6-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="25ad6-169">Bir kullanıcı başka bir kullanıcının değişikliği için imzaladığında, imzanın, değişikliği yapan kullanıcının iş istasyonundan girilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="25ad6-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="25ad6-170">İmza girilene kadar kullanıcı değişikliği kaydedemez.</span><span class="sxs-lookup"><span data-stu-id="25ad6-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="25ad6-171">Onaylayanları belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="25ad6-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="25ad6-172">**Seçenekler** sayfasında **Hesaplar** sekmesinde **Onaylayanı belirle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25ad6-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="25ad6-173">**Onaylayan kullanıcının kimliği** alanında, başka bir kullanıcının değişikliklerini imzalaması gereken kullanıcı kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="25ad6-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="25ad6-174">**Kullanıcı kimliği için imza yetkisi** alanında, değişiklikleri imzalanacak kullanıcının kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="25ad6-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>

