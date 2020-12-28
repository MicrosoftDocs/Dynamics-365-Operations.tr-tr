---
title: Özel alanlar oluşturma ve bunlarla çalışma
description: Bu konu uygulamayı işletmenize uygun hale getirmek için kullanıcı arabiriminden nasıl özel alanlar oluşturabileceğinizi açıklar.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 5f74397bcdd59a1fe24f5b6046081cbd2bed461b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693557"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="02486-103">Özel alanlar oluşturma ve bunlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="02486-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02486-104">Çok sayıda iş sürecini yönetmek için kullanıma hazır kapsamlı bir alan kümesi olmasına karşın bazen bir şirketin sistemde ek bilgileri izlemesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="02486-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="02486-105">Bu alanları geliştirici araçlarında uzantı olarak eklemek için programlayıcılar kullanılabilir, özel alanlar özelliği alanların doğrudan kullanıcı arabiriminden eklenmesine olanak tanır ve web tarayıcınızı kullanarak uygulamanızı işletmenize uygun hale getirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="02486-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="02486-106">Özel alanlar ekleme yeteneği, platform güncelleştirmesi 13 ve sonraki sürümlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="02486-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="02486-107">Yalnızca özel izinlere sahip kullanıcıların bu özelliğe erişimi vardır.</span><span class="sxs-lookup"><span data-stu-id="02486-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="02486-108">Bu videoda bir sayfaya özel alan eklemenin ne kadar kolay olduğu gösterilmektedir: [Özel alanlar ekleme](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="02486-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="02486-109">Özel alanlar oluşturma</span><span class="sxs-lookup"><span data-stu-id="02486-109">Creating custom fields</span></span>

<span data-ttu-id="02486-110">Uygulamada izlemek istediğiniz ek bilgileri tanımladıktan sonra ilgili tabloda özel alan oluşturabilir ve bu yeni alanı sayfa üzerinde gösterebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="02486-111">Aşağıdaki adımlar özel alan oluşturma ve bu alanı forma yerleştirme sürecini açıklar.</span><span class="sxs-lookup"><span data-stu-id="02486-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="02486-112">Yeni alanın gerekli olduğu forma gidin.</span><span class="sxs-lookup"><span data-stu-id="02486-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="02486-113">Son hedef bir formda özel alanı görüntülemek olduğundan, özel alanları oluşturmaya giriş noktası kişiselleştirme deneyimi içinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="02486-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="02486-114">**Seçenekler**'i seçip kişiselleştirme araç çubuğunu açın ve daha sonra **Bu formu kişiselleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="02486-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="02486-115">**Ekle**'ye ve ardından **Alan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02486-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="02486-116">Yeni alanı görüntülemek istediğiniz form bölgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="02486-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="02486-117">Seçim yaptıktan sonra **Alan ekle** iletişim kutusunda formun seçilen bölgesine eklenebilecek mevcut alanların listesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="02486-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="02486-118">İlgilendiğiniz alanın zaten listede bulunmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="02486-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="02486-119">Varsa, listeden alanı seçip **Ekle**'ye tıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="02486-120">Özel alan oluşturma işlemini başlatmak için listenin üstündeki **Yeni alan oluştur** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02486-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="02486-121">**Yeni alan oluştur** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="02486-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="02486-122">**Yeni alan oluştur** düğmesini görmüyorsanız, bu özelliği kullanmak için gerekli izinlere sahip değilsinizdir.</span><span class="sxs-lookup"><span data-stu-id="02486-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="02486-123">**Yeni alan oluştur** iletişim kutusuna, aşağıdaki bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="02486-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="02486-124">Bu alanın eklenmesi gereken veritabanı tablosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="02486-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="02486-125">Açılır listede yalnızca özel alanları destekleyen tabloların görüntülendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="02486-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="02486-126">Desteklenen tablolardaki teknik ayrıntılar için aşağıdaki bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="02486-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="02486-127">Yeni alanın veri türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="02486-127">Select the data type for the new field.</span></span> <span data-ttu-id="02486-128">Kullanılabilir veri türleri şunlardır: onay kutusu, tarih, tarih saat, ondalık, numara, seçim listesi ve metin.</span><span class="sxs-lookup"><span data-stu-id="02486-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="02486-129">Metin veri türünü seçerseniz, bu alana girilebilecek maksimum metnin uzunluğunu da belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="02486-130">Seçim listesi türünü seçerseniz, alan için geçerli değerler kümesini de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="02486-131">Alan için bir ad, etiket ve yardım metni girin.</span><span class="sxs-lookup"><span data-stu-id="02486-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="02486-132">Ad veritabanındaki fiziksel alan adına karşılık gelirken etiket ve yardım metni bu alanı kullanıcı arabiriminde temsil etmek üzere kullanılan metindir.</span><span class="sxs-lookup"><span data-stu-id="02486-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="02486-133">Bu alan bu form için oluşturmanız gereken tek alanda **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02486-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="02486-134">Ek alanlar oluşturmanız gerekiyorsa **Kaydet ve yeni**'ye tıklayın ve adım 7'ye dönün.</span><span class="sxs-lookup"><span data-stu-id="02486-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="02486-135">Şu anda **Tablo başına 20 özel alan** sınırı bulunduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="02486-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="02486-136">**Yeni alan oluştur** iletişim kutusundan çıktığınızda **Alan ekle** iletişim kutusuna geri dönersiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="02486-137">Yeni eklenen özel alanlar forma eklenecek alan listesinde otomatik olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="02486-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="02486-138">İşaretlenen alanları formun seçilen bölgesine eklemek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02486-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="02486-139">**İsteğe bağlı:** Yeni alanları seçilen bölümde istenen konuma taşımak için kişiselleştirme araç çubuğundaki **Taşı** modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="02486-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="02486-140">Kişisel kullanım için bir formu en iyi duruma getirmek amacıyla çeşitli kişiselleştirme özelliklerinin kullanılmasıyla ilgili daha fazla bilgi edinmek için [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="02486-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="02486-141">Özel alanları diğer kullanıcılarla paylaşma</span><span class="sxs-lookup"><span data-stu-id="02486-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="02486-142">Özel alan oluşturup formda görüntülenmesini sağladıktan sonra, güncelleştirilen ve yeni alanı içeren bu sayfa görünümünü sistemdeki diğer kullanıcılara sunmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="02486-143">Bunu üründeki kişiselleştirme özelliklerini kullanarak iki farklı yoldan yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="02486-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="02486-144">Önerilen yol bu işlemi bir kişiselleştirmeyi tüm kullanıcılara veya bir kullanıcı alt kümesine sunabilecek olan sistem yöneticisi aracılığıyla gerçekleştirmektir.</span><span class="sxs-lookup"><span data-stu-id="02486-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="02486-145">Daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="02486-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="02486-146">Alternatif olarak, değişikliklerinizi (*kişiselleştirmeler* denir) dışa aktarabilir, bir veya daha fazla kullanıcıya gönderebilir ve bu kullanıcıların değişikliklerini içe aktarmalarını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="02486-147">Kişiselleştirme araç çubuğundaki **Yönet** seçeneği kişiselleştirmeleri dışa ve içe aktarmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="02486-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="02486-148">Özel alanları yönetme</span><span class="sxs-lookup"><span data-stu-id="02486-148">Managing custom fields</span></span>

<span data-ttu-id="02486-149">Sistemdeki tüm özel alanların yönetimi Sistem yönetimi modülündeki **Özel alanlar** sayfası aracılığıyla gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="02486-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="02486-150">Bu sayfa kullanıcılara aşağıdakiler dahil birçok özelliğe erişime olanağı tanır:</span><span class="sxs-lookup"><span data-stu-id="02486-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="02486-151">Sistemdeki tüm özel alanların listesini görüntüleme.</span><span class="sxs-lookup"><span data-stu-id="02486-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="02486-152">Var olan özel alanlarını sınırlı düzenleme.</span><span class="sxs-lookup"><span data-stu-id="02486-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="02486-153">Özel alanları silme.</span><span class="sxs-lookup"><span data-stu-id="02486-153">Deleting custom fields.</span></span>
- <span data-ttu-id="02486-154">Özel alanları veri varlıklarında görüntüleme.</span><span class="sxs-lookup"><span data-stu-id="02486-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="02486-155">Özel alanların etiketleri ve yardım metninin çevirisini sağlama.</span><span class="sxs-lookup"><span data-stu-id="02486-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="02486-156">Tüm özel alanları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="02486-156">Viewing all custom fields</span></span>

<span data-ttu-id="02486-157">**Özel alanlar** sayfası sistemde tanımlanan tüm özel alanların görülmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="02486-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="02486-158">İlgilendiğiniz tabloyu seçmeniz yeterlidir; sayfa bu tabloyla ilişkili özel alanların listesini gösterecek şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="02486-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="02486-159">Listeden bir özal alan seçmek bu alanla ilgili tüm ayrıntıları görmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="02486-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="02486-160">Özel alanları düzenleme</span><span class="sxs-lookup"><span data-stu-id="02486-160">Editing custom fields</span></span>

<span data-ttu-id="02486-161">Özel alan oluşturulduktan sonra, **Özel alanlar** sayfasında özel alanla ilgili yalnızca bazı bilgi parçaları değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="02486-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="02486-162">Şu öznitelikleri *değiştirebilirsiniz*:</span><span class="sxs-lookup"><span data-stu-id="02486-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="02486-163">Etiket</span><span class="sxs-lookup"><span data-stu-id="02486-163">Label</span></span>
- <span data-ttu-id="02486-164">Yardım metni</span><span class="sxs-lookup"><span data-stu-id="02486-164">Help text</span></span>
- <span data-ttu-id="02486-165">Uzunluk, Metin alanları için</span><span class="sxs-lookup"><span data-stu-id="02486-165">Length, for Text fields</span></span>

<span data-ttu-id="02486-166">Şu öznitelikleri *düzenleyemezsiniz*:</span><span class="sxs-lookup"><span data-stu-id="02486-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="02486-167">Alan adı</span><span class="sxs-lookup"><span data-stu-id="02486-167">Field name</span></span>
- <span data-ttu-id="02486-168">Veri tipi</span><span class="sxs-lookup"><span data-stu-id="02486-168">Data type</span></span>

<span data-ttu-id="02486-169">Ek olarak, özel alanlar için geçerli değerler kümesi olan seçim listesi alanları yeniden sıralanabilir ve yeni değerler eklenebilir; ancak seçim listesi alanındaki mevcut değerler kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="02486-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="02486-170">Değişikliklerin kaydedilebilmesi için belirli bir tabloya ilişkin alanları düzenlemeyi tamamladıktan sonra **Değişiklikleri uygula**'ya tıklamayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="02486-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="02486-171">Özel alanları veri varlıklarında görüntüleme</span><span class="sxs-lookup"><span data-stu-id="02486-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="02486-172">Ayrıca özel alanların veri varlıklarında görünür olmasını sağlamak önemli olabilir.</span><span class="sxs-lookup"><span data-stu-id="02486-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="02486-173">Veri varlıkları [Office tümleştirmesine genel bakış](../../dev-itpro/office-integration/office-integration.md) özelliğinde ve veri içe aktarma/dışa aktarma senaryolarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="02486-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="02486-174">Bir veri varlığında özel alanın görünür olmasını sağlamak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="02486-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="02486-175">**Özel alanlar** formunda özel alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="02486-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="02486-176">İlgili varlıklar kümesini görmek için **Varlıklar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="02486-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="02486-177">**Düzenle** düğmesine basın.</span><span class="sxs-lookup"><span data-stu-id="02486-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="02486-178">Bu alanda görünmesi gereken her varlık için seçilecek **Etkin** alanını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="02486-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="02486-179">Seçimlerini kaydetmek için **Değişiklikleri uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02486-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="02486-180">Diğer dillerde görüntülenecek özel alanlara izin verme</span><span class="sxs-lookup"><span data-stu-id="02486-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="02486-181">Özel alanlara farklı dilleri kullanan kullanıcılar tarafından erişilmesi gerekebileceğinden, **Özel alanlar** sayfası bir özel alanın etiketinin ve yardım metninin diğer dillere çevrilmesine olanak tanıyan bir mekanizma sunar.</span><span class="sxs-lookup"><span data-stu-id="02486-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="02486-182">Aşağıdaki adımlar özel alanlaron diğer dillere çevrilmesi işlemini açıklar:</span><span class="sxs-lookup"><span data-stu-id="02486-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="02486-183">**Özel alanlar** sayfasında özel alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="02486-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="02486-184">Eylem Bölmesinde **Çeviriler** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="02486-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="02486-185">Bu alan için mevcut çevirileri içeren bir açılır menü açılır.</span><span class="sxs-lookup"><span data-stu-id="02486-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="02486-186">**Dil** açılır menüsü çevirisi zaten sağlanmış olan dilleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="02486-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="02486-187">Mevcut bir çeviriyi düzenlemek isterseniz, menüden istediğiniz dili seçip etiket ve yardım metni değerlerini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="02486-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="02486-188">Aksi halde, **Dil ekle** düğmesine tıklayın, menüden istediğiniz dili seçin ve etiket ve yardım metni için çevrilmiş değerleri sağlayın.</span><span class="sxs-lookup"><span data-stu-id="02486-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="02486-189">İşlemi tamamladığınızda **Tamam** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02486-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="02486-190">Özel alanları silme</span><span class="sxs-lookup"><span data-stu-id="02486-190">Deleting custom fields</span></span>

<span data-ttu-id="02486-191">Bazı ender durumlarda, bir özel alanın artık gerekli olmadığına karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02486-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="02486-192">Bu durumda, sistem yöneticisi bu alanı **Özel alanlar** sayfasından silmeyi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="02486-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="02486-193">Bunu yapmak için doğru alanın seçili olduğundan emin olun, **Sil**'e tıklayın, silme işlemini onaylamak için **Evet**'i seçin ve son olarak **Değişiklikleri uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02486-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="02486-194">Bu eylem geri alınamaz ve alanla ilişkili verilerin veritabanından tamamen silinmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="02486-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="02486-195">Ek</span><span class="sxs-lookup"><span data-stu-id="02486-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="02486-196">Özel alanları kimler oluşturabilir?</span><span class="sxs-lookup"><span data-stu-id="02486-196">Who can create custom fields?</span></span>

<span data-ttu-id="02486-197">Sistemi korumak amacıyla, varsayılan olarak yalnızca sistem yöneticileri özel alanlar oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="02486-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="02486-198">Ancak, kuruluşun gerekli gördüğü kullanıcılara sistem yöneticisi tarafından **Çalışma zamanında özelleştirme yetkili kullanıcısı** güvenlik rolü kullanılarak özel alanlar oluşturma hakkı verilebilir.</span><span class="sxs-lookup"><span data-stu-id="02486-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="02486-199">Bu güvenlik rolüne sahip olmayan kullanıcılar özel alanlar oluşturamaz ancak sistemdeki diğer kullanıcılar tarafından eklenen özel alanları görebilir ve bunlarla etkileşimde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="02486-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="02486-200">Hangi tablolar özel alanları destekler?</span><span class="sxs-lookup"><span data-stu-id="02486-200">What tables support custom fields?</span></span>

<span data-ttu-id="02486-201">Performans ve teknik nedenlerle, şu anda yalnızca aşağıdaki koşulları karşılayan tablolara özel alanlar eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="02486-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="02486-202">Tablo şu gruplardan biri olarak etiketlenmelidir:</span><span class="sxs-lookup"><span data-stu-id="02486-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="02486-203">Grup</span><span class="sxs-lookup"><span data-stu-id="02486-203">Group</span></span>
    - <span data-ttu-id="02486-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="02486-204">WorksheetHeader</span></span>
    - <span data-ttu-id="02486-205">Ana</span><span class="sxs-lookup"><span data-stu-id="02486-205">Main</span></span>
    - <span data-ttu-id="02486-206">Çeşitli</span><span class="sxs-lookup"><span data-stu-id="02486-206">Miscellaneous</span></span>
    - <span data-ttu-id="02486-207">Parametre</span><span class="sxs-lookup"><span data-stu-id="02486-207">Parameter</span></span>
    - <span data-ttu-id="02486-208">Referans</span><span class="sxs-lookup"><span data-stu-id="02486-208">Reference</span></span>
    - <span data-ttu-id="02486-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="02486-209">TransactionHeader</span></span>

- <span data-ttu-id="02486-210">Tablo başka bir tabloya genişletilemez.</span><span class="sxs-lookup"><span data-stu-id="02486-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="02486-211">Tablo bir sistem tablosu olarak işaretlenemez.</span><span class="sxs-lookup"><span data-stu-id="02486-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="02486-212">Tablo geçici bir tablo olamaz.</span><span class="sxs-lookup"><span data-stu-id="02486-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="02486-213">Geliştirici araçlarındaki özel alanlara başvurabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="02486-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="02486-214">Özel alanlar yalnızca kullanıcı arabiriminden yönetilebilir ve kod tarafından başvurulamaz.</span><span class="sxs-lookup"><span data-stu-id="02486-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
