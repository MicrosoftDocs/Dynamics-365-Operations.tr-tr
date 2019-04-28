---
title: Teklif yönetimini ayarlayın
description: Bu konu Talent'ta tekliflerin nasıl ayarlanacağını açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fa0e5d30c06db16e105631e492af022acfcfd66
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "857881"
---
# <a name="set-up-offer-management"></a><span data-ttu-id="fda2c-103">Teklif yönetimini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="fda2c-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="fda2c-104">Bir aday Dynamics 365 for Talent: Attract'ta bir teklif aşamasına geçtiğinde, tekliflerin aday için hızlı bir şekilde oluşturulduğundan, gerektiği gibi onaylandığından ve aday gönderildiğinden emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="fda2c-105">Çoğu teklif standart olduğu için yeniden kullanılabilir şablonlardan oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="fda2c-106">Attract'ta, tüm teklifler, bir veya daha fazla teklif belgesinden oluşan bir teklif paketine toplanır.</span><span class="sxs-lookup"><span data-stu-id="fda2c-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="fda2c-107">Bu konu, bir Attract yöneticisinin, Attract'taki teklif yönetim özelliklerinin bir parçası olarak farklı teklif paketi şablonları ayarlamak için izleyeceği tüm adımları listeler.</span><span class="sxs-lookup"><span data-stu-id="fda2c-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="fda2c-108">Yönetici olmayan rollere sahip kullanıcılar için bu yeteneklerin erişimi olmaz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="fda2c-109">Teklif yönetimi yetenekleri, Kapsamlı İşe aAlma Eklentisi parçası olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="fda2c-110">Teklif verileri</span><span class="sxs-lookup"><span data-stu-id="fda2c-110">Offer data</span></span> 

<span data-ttu-id="fda2c-111">Teklif verileri, teklif paketi şablonu içindeki en küçük birimdir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="fda2c-112">Tipik bir teklif standart metin ve bir dizi değerden oluşur.</span><span class="sxs-lookup"><span data-stu-id="fda2c-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="fda2c-113">Değer kümesi, teklifler arasında değişebilen tek parçadır.</span><span class="sxs-lookup"><span data-stu-id="fda2c-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="fda2c-114">Teklif oluşturma sırasında teklifi oluşturanın odaklanabileceği en önemli yön, teklif paketi şablonunda bluunan teklif veri yer tutucuları listesidir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="fda2c-115">Teklif verilerini kurmak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="fda2c-116">**Teklif yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="fda2c-117">Sol gezinti bölmesinde **Kitaplığı** genişletin, **Teklif verileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="fda2c-118">**Teklif verileri** sayfasında, **Aday ayrıntıları** ve **İş ayrıntıları** bölümleri vardır.</span><span class="sxs-lookup"><span data-stu-id="fda2c-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="fda2c-119">Attract, sıra dışı birkaç teklif verisi yer tutucusu sağlar.</span><span class="sxs-lookup"><span data-stu-id="fda2c-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="fda2c-120">Farklı teklif veri yer tutucularını mantıksal gruplar halinde düzenlemek için sayfada bölümler vardır.</span><span class="sxs-lookup"><span data-stu-id="fda2c-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="fda2c-121">Bu bölümler, teklif verilerinin bakımı ve verilerin teklif oluşturma işlemi sırasında doldurulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="fda2c-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="fda2c-122">Yeni bir teklif veri bölümü oluşturmak için **Bölüm ekle**'ye tıklayın ve bölüm için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="fda2c-123">Herhangi bir bölüm için teklif verisi yer tutucular eklemek için **Teklif verisi ekle**'ye tıklayın ve yer tutucu için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="fda2c-124">Her bölümün adını düzenlemek için bölüm adının üzerine getirin ve adı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="fda2c-125">Varolan bir teklif veri yer tutucu adını düzenlemek için önce yer tutucunun zaten bir şablon parçası olmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="fda2c-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="fda2c-126">Daha sonra teklif veri yer tutucu adına getirin ve adı gerektiği şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="fda2c-127">Varolan bir teklif veri yer tutucuyu silmek için önce yer tutucunun başka bir şablon parçası olmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="fda2c-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="fda2c-128">Daha sonra yer tutucuya getirin ve çöp tenekesi simgesini göründüğü zaman çöp tenekesine tıklayıp teklif veri yer tutucuyu silin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="fda2c-129">Bir teklif veri parçası yanında numara göstergesi parçası olarak kaç şablonun bir teklif verisi yer tutucu parçası oldğunu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="fda2c-130">Herhangi bir bölümü silmek için adın üzerine getirin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="fda2c-131">Teklif veri yer tutucular bölüm içindeki hiçbir şablonda görünmüyorsa, iletiyi silmek için çöp tenekesi simgesini tıklatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="fda2c-132">Bölümün silinmesi o bölümün içindeki tüm teklif veri yer tutucuları da siler.</span><span class="sxs-lookup"><span data-stu-id="fda2c-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="fda2c-133">Teklif veri yer tutucuları ayarlandıktan sonra belge şablonlarında kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="fda2c-134">Teklif veri yer tutucularının belirli bir şablona sınırlama yoktur, aynı grup tüm şablonlarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="fda2c-135">Teklif verisi kuralları</span><span class="sxs-lookup"><span data-stu-id="fda2c-135">Offer data rules</span></span>

<span data-ttu-id="fda2c-136">Çoğu kuruluş teklifler nasıl oluşturulması gerektiğiyle ilgili kurallara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="fda2c-137">Örneğin, bir organizasyon belirli bir konum ve kıdem düzeyi birleşimi için maksimum yıllık teklifin belirli bir aralıkta olmasını veya yeni işe alım için teklif düzeyi için yalnızca birkaç belirli olası değer olmasını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="fda2c-138">Attract, şu anda bir CSV dosyası kullanarak tüm bu gibi verileri kurallarını destekler.</span><span class="sxs-lookup"><span data-stu-id="fda2c-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="fda2c-139">Veri kuralları CSV dosyasını hazırlamak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="fda2c-140">Kural kümesi için teklif veri yer tutucuyu belirleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="fda2c-141">Örneğin, **Yıllık Maaş**.</span><span class="sxs-lookup"><span data-stu-id="fda2c-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="fda2c-142">Bağımlı teklif veri yer tutucu değerlerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="fda2c-143">Örneğin, **İş Konum** ve **Düzeyi**.</span><span class="sxs-lookup"><span data-stu-id="fda2c-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="fda2c-144">Sütun 1 ve 2'yi **İş Yeri** ve **Düzey** olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="fda2c-145">Aralığı değerini yüklemek için , sütun 3 ve 4'ü **Yıllık ücret** yapın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="fda2c-146">Aralık yerine belirli bir değeri karşıya yüklemek için, yalnızca sütun 3'ü **Yıllık ücret** yapın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="fda2c-147">Microsoft Excel dosyasını gerekli rollere göre doldurun.</span><span class="sxs-lookup"><span data-stu-id="fda2c-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="fda2c-148">Her satırın, tüm değerlerin benzersiz birleşimini bir araya getirdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="fda2c-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="fda2c-149">Dosyayı CSV formatında kaydedin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="fda2c-150">Teklif veri kuralları dosyasını yüklemek için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="fda2c-151">**Teklif yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="fda2c-152">Sol gezinti bölmesinde **Kitaplığı** genişletin, **Teklif verileri kuralları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="fda2c-153">**Yeni veri kümesi**'ne tıklayıp **Karşıya yükle** iletişim kutusunu görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="fda2c-154">Kural kümesi için benzersiz bir ad belirtin ve kaydedilmiş CSV dosyasını karşıya yükleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="fda2c-155">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-155">Click **Add**.</span></span>
    <span data-ttu-id="fda2c-156">Kural kümesi arka planda işlenir ve tamamlandıktan sonra uygulama içinde ve e-posta yoluyla bildirilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="fda2c-157">Karşıya yükleme işlemi sırasında hatalar oluşursa size bildirilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="fda2c-158">Daha sonra hata günlüğünü indirip, dosyayı düzeltip yeniden yükleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="fda2c-159">Üç nokta (**...**) düğmesini, kural kümesini yüklemek ve değerler kümesini güncelleştirmek istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="fda2c-160">Güncelleştirmeden sonra dosyayı yeniden yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="fda2c-161">Tanımlanan yer tutucu başka bir belge şablonunda kullanılmıyorsa varolan kural kümesinin karşıya yüklemesini silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="fda2c-162">Her bir yer tutucu yalnızca bağımlı olduğu benzersiz sütunlar kümesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-162">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="fda2c-163">Örneğin, **Yıllık ücret**, **Şş yeri** ve **Düzey**'e bağlıysa **Yıllık ücret**'in farklı bir sütun kümesine bağlı olduğu başka bir kural kümesine yükleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-163">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="fda2c-164">Örnek teklif veri kuralı kümesini **Teklif veri kuralları** sayfasındaki **Örnekler** sekmesinden indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-164">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="fda2c-165">Teklifi oluşturan kişi, teklif veri kuralları tarafından önerilen değerleri değiştirdiğinde, teklifi standart olmayan olarak işaretlenir ve teklif onayı iş akışı zorunlu olur.</span><span class="sxs-lookup"><span data-stu-id="fda2c-165">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="fda2c-166">Belge şablonları</span><span class="sxs-lookup"><span data-stu-id="fda2c-166">Document templates</span></span>

<span data-ttu-id="fda2c-167">Teklif belge şablonu, yöneticilerin teklif mektupları oluşturmasına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-167">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="fda2c-168">Teklif belge şablonu, tanımlanan teklif veri yer tutucularının yanı sıra teklifin parçası olan metnin birleşimidir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-168">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="fda2c-169">Teklif belge şablonu oluşturmak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-169">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="fda2c-170">**Teklif yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-170">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="fda2c-171">Sol gezinti bölmesinde **Kitaplığı** genişletin, **Şablonlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-171">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="fda2c-172">**Şablonlar** sayfası, önceden tanımlanmış belge şablonları listesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="fda2c-172">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="fda2c-173">Yeni bir belge şablonu oluşturmak için **Yeni Şablon**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-173">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="fda2c-174">Şablon için benzersiz bir ad girin ve **Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-174">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="fda2c-175">Teklif belge içeriğini girmek veya düzenlmek için zengin metin düzenleyici kullanın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-175">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="fda2c-176">Tablolar, resimler ve köprüleri metin düzenleyicisi üstündeki seçenekleri kullanarak ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-176">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="fda2c-177">Teklif şablonu belgesinde teklif veri yer tutucuları ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="fda2c-177">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="fda2c-178">Sağ bölmeden sürükleyip bırakarak.</span><span class="sxs-lookup"><span data-stu-id="fda2c-178">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="fda2c-179">Teklif veri yer tutucuyu doğrudan konumuna etiketleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-179">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="fda2c-180">**\#** yazın ve teklif veri yer tutucu adı yazmaya başlayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-180">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="fda2c-181">Seçenekler açılan listesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="fda2c-181">Options will appear in the drop-down list.</span></span> <span data-ttu-id="fda2c-182">Teklif veri yer tutucu eklemek için **Enter**'a tıklatın veya basın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-182">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="fda2c-183">Yer tutucuyu teklif belge şablonuyla ilişkilendirmek için, değerini adaya sunmadan, teklif veri yer tutucuya gidin ve  **Sabitle** simgesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-183">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="fda2c-184">Bu, yer tutucuyu teklif belge şablonunun **Sabitlenen teklif verisi** bölümüne gönderir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-184">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="fda2c-185">Bırakmak için aynı adımları uygulayın ancak teklif veri yer tutucular listesinde **Bırak**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-185">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="fda2c-186">Etkin teklif beri yer tutucular listesini görüntülemek için sağ bölmede **Etkin** sekmesine geçin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-186">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="fda2c-187">Teklif veri kuralı kümesi tarafından yönetilen bir yer tutucu eklemek isterseniz, teklif veri yer tutucunun diğer değerlere bağımlılığı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-187">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="fda2c-188">Alternatif olarak, içeriği yerel makinenizdeki bir .docx dosyasından **İçe Aktar** yapabilir ve gerektiği gibi düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-188">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="fda2c-189">Böylece, düzenleyicideki tüm içeriği yazmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="fda2c-189">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="fda2c-190">Teklif belgesinin önizlemesini yapmak için sayfanın üstündeki **Önizleme** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-190">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="fda2c-191">Teklifi oluşturan kişiin teklif belge içeriği düzenlemesini kontrol etmek için sayfanın üstündeki **İzni yönet** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-191">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="fda2c-192">Teklif oluşturanın yalnızca yer tutucu değerlerini eklemesini ve metni düzenlememesini isterseniz izin değerini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-192">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="fda2c-193">İlerlemenizi kaydetmek için **Kaydet**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-193">Click **Save** to save your progress.</span></span> <span data-ttu-id="fda2c-194">Şablon taslak durumunda kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-194">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="fda2c-195">Belgeyi son haline getirmek ve yayımlandı olarak işaretlemek için **Bitir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-195">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="fda2c-196">Hangi bölge şablonlarının şu anda aktif, hangilerinin taslak modunda ve hangilerinin arşivlendiğini veya artık belge şablonları kitaplığının deneyiminde kullanımda olmadığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-196">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="fda2c-197">Varolan bir teklif paketi şablonunun parçası olmayan teklif belgesi şablonlarını silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-197">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="fda2c-198">Teklif paketi şablonları</span><span class="sxs-lookup"><span data-stu-id="fda2c-198">Offer package templates</span></span>

<span data-ttu-id="fda2c-199">Teklif paketleri, adayla paylaşılan ve bir veya daha falza teklik belge şablonu birleşiminden oluşan teklif parçalarıdır.</span><span class="sxs-lookup"><span data-stu-id="fda2c-199">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="fda2c-200">Teklif paketi oluşturmak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-200">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="fda2c-201">**Teklif yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-201">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="fda2c-202">Sol gezinti bölgesinden **Paketler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-202">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="fda2c-203">Teklif oluşturanlar için kullanılabilir olan etkin paket şablonları listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-203">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="fda2c-204">Yeni bir teklif paketi oluşturmak için **Yeni Paket**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-204">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="fda2c-205">Benzersiz bir ad girin ve **Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-205">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="fda2c-206">**Şablon ekle**’yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-206">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="fda2c-207">Yeni bir şablon oluşturmayı veya mevcut bir modelden seçmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-207">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="fda2c-208">Varolan bir şablonu eklemek isterseniz, teklif belge şablonunun kaydedilmiş, sonlandırılmış ve etkin olarak işaretlenmiş olduğundan emin olmak gerekir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-208">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="fda2c-209">İstediğiniz sayıda belge şablonu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-209">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="fda2c-210">**Paket yönetimi**'ne dönmek için **Bitti**'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-210">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="fda2c-211">Belge sırasını yapılandırın ve belirli teklif belgesinin tekli oluşturma sırasında gerekip gerekmediğini de işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-211">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="fda2c-212">Teklif oluşturan, **Gereksiz** olarak işaretlenen belgeleri silme seçeneğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-212">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="fda2c-213">Teklif paketi şablonunun tüm teklif oluşturan kullanıcılar tarafından kullanılabilir olması için **Kaydet ve yayınla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda2c-213">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="fda2c-214">Taslak teklif paketi şablonlarını görüntülemek için **Taslaklar** sekmesine gidin. Teklif paket şablonuna değişiklik yapılırsa, kaydedilmesi ve yeniden yayınlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-214">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="fda2c-215">Teklif sürecini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fda2c-215">Configure an offer process</span></span>

<span data-ttu-id="fda2c-216">Attract yöneticisi tarafından yapılandırılabilir teklif oluşturma işleminin birden çok bölümü vardır.</span><span class="sxs-lookup"><span data-stu-id="fda2c-216">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="fda2c-217">**Teklif onayları** - Teklif onaylarının, teklifini adaya gönderilebilmesi için gerekip gerekmediğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-217">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="fda2c-218">Yönetici olarak, tüm teklif onaylarının sıralı bir şekilde veya paralel onay iş akışıyla olacağını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-218">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="fda2c-219">Teklif onaylayanların, teklifi onaylarının yanı sıra bir açıklama eklemesini gerektirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-219">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="fda2c-220">Teklif onayları, standart olmayan teklifler için zorunludur.</span><span class="sxs-lookup"><span data-stu-id="fda2c-220">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="fda2c-221">**Adayın teklif deneyimi** - Yönetici olarak, tüm tekliflerin bitiş tarihi olmasını seçebilirsiniz, bu durumda bitiş tarihinin varsayılan mahsubunun ne olması gerektiğini de seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-221">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="fda2c-222">Adayların bir teklif reddedip reddemeyeceğini de yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-222">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="fda2c-223">**e-İmzalar** - Bir yönetici olarak, adayların tekliflere imza atabilecekleri yöntemleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda2c-223">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="fda2c-224">Adobe Sign - Tüm teklif paketleri Adobe Sign ile gönderilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-224">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="fda2c-225">Teklifi yayınlayan her teklif oluşturucusunun kendi Adobe Sign hesabını Attract'e bağlamış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-225">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="fda2c-226">Adobe Sign için lisanslar ve bir ücretsiz Deneme için lütfen bu [bağlantıyı](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html) ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="fda2c-226">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="fda2c-227">DocuSign - Tüm teklif paketleri DocuSign ile gönderilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-227">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="fda2c-228">Teklifi yayınlayan her teklif oluşturucusunun kendi DocuSign hesabını Attract'e bağlamış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-228">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="fda2c-229">ESign - Bu varsayılan seçenektir, kullanıma hazırdır, kullanıcı kendi adını ve baş harflerini yazarak imza atabilir.</span><span class="sxs-lookup"><span data-stu-id="fda2c-229">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="fda2c-230">Teklif oluşturma işlemi hakkında daha fazla bilgi için bkz: [Teklif oluşturma, onaylama ve imzalama](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="fda2c-230">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>
