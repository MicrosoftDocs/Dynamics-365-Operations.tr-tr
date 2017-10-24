---
title: "Kuruluş yönetimi giriş sayfası"
description: "Bu konu sizi Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'u kuruluşunuzda kullanmanıza yardımcı olacak kaynaklara yönlendirir."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: eb8674a6401b11e8e33d3cba54add1fb4bca1cd3
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="b1869-103">Kuruluş yönetimi giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="b1869-103">Organization administration home page</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b1869-104">Bu konu yetkili kullanıcıların ve yöneticilerin Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'u yapılandırmasına yardımcı olacak içeriklere yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="b1869-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="b1869-105">Bu içerik onlara sistemi kuruluşunuz ve işiniz için sorunsuz ve etkili çalışmak üzere yapılandırmalarına yardımcı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b1869-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="b1869-106">Burada listelenen içeriğin büyük bölümü **Kuruluş yönetimi** modülündeki özelliklere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b1869-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="b1869-107">Ancak, bir kayıt şablonu oluşturmak ve kullanmak gibi bazı görevler, kuruluşunuzun daha verimli çalışmasına yardımcı olmak için her modülde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="b1869-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span> 

<a name="number-sequences"></a><span data-ttu-id="b1869-108">Numara serileri</span><span class="sxs-lookup"><span data-stu-id="b1869-108">Number sequences</span></span>
----------------
<span data-ttu-id="b1869-109">Numara serileri, ana veri kayıtları ve tanımlayıcı gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b1869-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="b1869-110">Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, *referans* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="b1869-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="b1869-111">Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b1869-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

-   [<span data-ttu-id="b1869-112">Numara serilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b1869-112">Number sequence overview</span></span>](number-sequence-overview.md)
-   <span data-ttu-id="b1869-113">[Bir sihirbaz kullanarak satınalma için numara serilerini ayarlama](tasks/set-up-number-sequences-wizard.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
-   <span data-ttu-id="b1869-114">[Bireysel olarak numara serileri ayarlama](tasks/set-up-number-sequences-individual-basis.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="b1869-115">Kuruluşlar</span><span class="sxs-lookup"><span data-stu-id="b1869-115">Organizations</span></span>
<span data-ttu-id="b1869-116">Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır.</span><span class="sxs-lookup"><span data-stu-id="b1869-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="b1869-117">Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b1869-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="b1869-118">Finance and Operations'da kuruluşlar ve kuruluş hiyerarşilerini ayarlamadan önce işinizin nasıl modellendirileceğini planladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b1869-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="b1869-119">Kuruluş modelinin Finance and Operations'ın uygulanması ve iş süreçleri üzerinde önemli bir etkisi vardır.</span><span class="sxs-lookup"><span data-stu-id="b1869-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

-   [<span data-ttu-id="b1869-120">Kuruluşlar ve kuruluş hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="b1869-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
-   [<span data-ttu-id="b1869-121">Kuruluş hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="b1869-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
-   <span data-ttu-id="b1869-122">[Bir kuruluş hiyerarşisi oluşturma](tasks/create-organization-hierarchy.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
-   <span data-ttu-id="b1869-123">[Tüzel kişilik oluşturma](tasks/create-legal-entity.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
-   <span data-ttu-id="b1869-124">[Bir işletme birimi oluşturma](tasks/create-operating-unit.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="b1869-125">Adres defterleri</span><span class="sxs-lookup"><span data-stu-id="b1869-125">Address books</span></span>
<span data-ttu-id="b1869-126">Genel adres defteri, şirketin etkileşimde bulunduğu tüm iç ve dış kişiler ve kuruluşların depolanması gereken verilerini barındıran merkezi bir depodur.</span><span class="sxs-lookup"><span data-stu-id="b1869-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="b1869-127">Taraf kayıtları ile ilişkilendirilen veri, tarafın adını, adresini ve ilgili kişi bilgisini içerir.</span><span class="sxs-lookup"><span data-stu-id="b1869-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span> 

<span data-ttu-id="b1869-128">Genel Adres Defteri'ni oluşturduktan sonra her iş kolu veya kuruluşunuzdaki her şirket için bir ayrı bir adres defterini, gerektiği gibi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1869-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> 

-   [<span data-ttu-id="b1869-129">Genel adres defteri</span><span class="sxs-lookup"><span data-stu-id="b1869-129">Global address book</span></span>](overview-global-address-book.md)
-   [<span data-ttu-id="b1869-130">Genel adres defteri ve diğer adres defterlerini yapılandırmayı planlama</span><span class="sxs-lookup"><span data-stu-id="b1869-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="b1869-131">Genel adres defterini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b1869-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
-   [<span data-ttu-id="b1869-132">Adres defterleriyle ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="b1869-132">Address books FAQ</span></span>](qa-address-books.md)


## <a name="workflow"></a><span data-ttu-id="b1869-133">İş akışı</span><span class="sxs-lookup"><span data-stu-id="b1869-133">Workflow</span></span>
<span data-ttu-id="b1869-134">İş akışı, Finance and Operations ile yüklenen ve tek iş akışları veya iş süreçleri oluşturmakta kullanabileceğiniz bir sistemdir.</span><span class="sxs-lookup"><span data-stu-id="b1869-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="b1869-135">Bir iş akışı oluşturduğunuzda, bir görevin kimin tarafından tamamlanacağını, bir kararın kimin tarafından verileceğini veya bir belgenin kimin tarafından onaylanacağını göstererek bir belgenin sistem üzerinde nasıl aktığını veya taşındığını tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="b1869-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> 

-   [<span data-ttu-id="b1869-136">İş akışı özeti</span><span class="sxs-lookup"><span data-stu-id="b1869-136">Workflow overview</span></span>](overview-workflow-system.md)
-   [<span data-ttu-id="b1869-137">İş akışı öğeleri</span><span class="sxs-lookup"><span data-stu-id="b1869-137">Workflow elements</span></span>](workflow-elements.md)
-   [<span data-ttu-id="b1869-138">İş akışı eylemleri</span><span class="sxs-lookup"><span data-stu-id="b1869-138">Workflow actions</span></span>](workflow-actions.md)
-   [<span data-ttu-id="b1869-139">İş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1869-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="b1869-140">Elektronik imzalar</span><span class="sxs-lookup"><span data-stu-id="b1869-140">Electronic signatures</span></span>
<span data-ttu-id="b1869-141">Elektronik imza bir hesaplama işlemi başlatmak veya onaylamak üzere olan kişinin kimliğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="b1869-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="b1869-142">Bazı sektörlerde, elektronik imza yasal açıdan elle atılmış imza kadar bağlayıcı olmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b1869-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="b1869-143">Elektronik imzalar ilaç, yiyecek ile içecek ve havacılık ve uzay ile savunma sanayileri gibi birtakım kontrol altındaki sektörlerle ilgili yönetmeliklere uyumluluk gereklilikleridir.</span><span class="sxs-lookup"><span data-stu-id="b1869-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="b1869-144">Finance and Operations uygulamasında önemli iş süreçleri için elektronik imza kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1869-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="b1869-145">Bazı işlemler yerleşik elektronik imza özelliklerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="b1869-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="b1869-146">Ayrıca herhangi bir veritabanı tablosu ve alanı için özel imza gereklilikleri de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1869-146">You can also create custom signature requirements for any database table and field.</span></span>

-   [<span data-ttu-id="b1869-147">Elektronik imzalara genel bakış</span><span class="sxs-lookup"><span data-stu-id="b1869-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
-   <span data-ttu-id="b1869-148">[Elektronik imzaları ayarlama](tasks/set-up-electronic-signatures.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="b1869-149">Servis talebi yönetimi</span><span class="sxs-lookup"><span data-stu-id="b1869-149">Case management</span></span>
<span data-ttu-id="b1869-150">Planlayarak, izleyerek ve durumları analiz ederek, benzer sorunlarda kullanılabilecek verimli çözümler geliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1869-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="b1869-151">Örneğin, bir müşteri servis temsilcisi veya İnsan Kaynakları kişisi vakalar oluşturduğunda, bir vaka ile çalışma veya bunu çözümlemek için yardımcı olabilecek bilgileri bilgi bankası makalelerinde bulabilirler.</span><span class="sxs-lookup"><span data-stu-id="b1869-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span> 

-   [<span data-ttu-id="b1869-152">Servis talebi yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b1869-152">Case management overview</span></span>](cases.md)
-   [<span data-ttu-id="b1869-153">Servis talebi güvenliğini, işlemlerini ve kategorilerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b1869-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="b1869-154">Kayıt şablonları</span><span class="sxs-lookup"><span data-stu-id="b1869-154">Record templates</span></span>
<span data-ttu-id="b1869-155">Kayıt şablonları, kayıtları daha hızlı oluşturmaya yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b1869-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="b1869-156">Sıklıkla kullanılan alan değerlerinin her yeni bir kayıt için açık olarak girilmesi gerekmeden bir kayıt şablonunu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1869-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> 

-   [<span data-ttu-id="b1869-157">Kayıt şablonları</span><span class="sxs-lookup"><span data-stu-id="b1869-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="b1869-158">[Veri girişini kolaylaştırmak için bir kayıt şablonu oluşturma](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="b1869-159">[Yeni kayıt oluşturmak için kayıt şablonu kullanma](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="b1869-160">Genel kuruluş yönetimi</span><span class="sxs-lookup"><span data-stu-id="b1869-160">General organization administration</span></span>
-   <span data-ttu-id="b1869-161">[Başlık resmi veya logoyu değiştirme](../get-started/tasks/change-banner-or-logo.md) (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="b1869-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="b1869-162">Belge yönetimini konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="b1869-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="b1869-163">E-postayı yapılandırma ve gönderme</span><span class="sxs-lookup"><span data-stu-id="b1869-163">Configure and send email</span></span>](configure-email.md)
-   [<span data-ttu-id="b1869-164">Tarih/saat tarih ve saat dilimleri</span><span class="sxs-lookup"><span data-stu-id="b1869-164">Date/time data and time zones</span></span>](date-time-zones.md)








