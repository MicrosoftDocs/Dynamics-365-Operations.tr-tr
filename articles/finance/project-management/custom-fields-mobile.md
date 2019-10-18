---
title: iOS ve Android üzerinde Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulamak
description: Bu konu, özel alanları uygulamak için uzantıların kullanımıyla ilgili yaygın desenler sağlar.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175067"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="465f7-103">iOS ve Android üzerinde Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulamak</span><span class="sxs-lookup"><span data-stu-id="465f7-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="465f7-104">Bu konu, özel alanları uygulamak için uzantıların kullanımıyla ilgili yaygın desenler sağlar.</span><span class="sxs-lookup"><span data-stu-id="465f7-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="465f7-105">Aşağıdaki konular el alınmaktadır:</span><span class="sxs-lookup"><span data-stu-id="465f7-105">The following topics are covered:</span></span>

- <span data-ttu-id="465f7-106">Özel alan çerçevesinin desteklediği çeşitli veri türleri</span><span class="sxs-lookup"><span data-stu-id="465f7-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="465f7-107">Zaman çizelgesi girişlerinde salt okunur veya düzenlenebilir alanları gösterme ve kullanıcı tarafından sağlanan değerleri veritabanına geri kaydetme</span><span class="sxs-lookup"><span data-stu-id="465f7-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="465f7-108">Zaman çizelgesi üstbilgisinde salt okunur alanlar nasıl gösterilir</span><span class="sxs-lookup"><span data-stu-id="465f7-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="465f7-109">Diğer özel iş mantığı, alanlardaki varsayılan değerleri girmek ve ek doğrulama yapmak için nasıl tümleştirilir</span><span class="sxs-lookup"><span data-stu-id="465f7-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="465f7-110">Hedef Kitle</span><span class="sxs-lookup"><span data-stu-id="465f7-110">Audience</span></span>

<span data-ttu-id="465f7-111">Bu konu, kendi özel alanlarını Apple iOS ve Google Android için mevcut Microsoft Dynamics 365 Project Timesheet mobil uygulamasına tümleştirmek isteyen geliştiriciler içindir.</span><span class="sxs-lookup"><span data-stu-id="465f7-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="465f7-112">Varsayım, okuyucuların X++ geliştirme ve proje zaman çizelgesi işlevleri hakkında bilgi sahibi olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="465f7-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="465f7-113">Veri sözleşmesi – TSTimesheetCustomField X++ sınıfı</span><span class="sxs-lookup"><span data-stu-id="465f7-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="465f7-114">**TSTimesheetCustomField** sınıfı, zaman çizelgesi işlevselliği için özel bir alanla ilgili bilgileri temsil eden X++ veri sözleşmesi sınıfıdır.</span><span class="sxs-lookup"><span data-stu-id="465f7-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="465f7-115">Özel alan nesnelerinin listeleri, hem TSTimesheetDetails veri sözleşmesine hem de bir mobil uygulamadaki özel alanları göstermek için TSTimesheetEntry veri sözleşmesine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="465f7-116">**TSTimesheetDetails** - Zaman çizelgesi başlık sözleşmesi.</span><span class="sxs-lookup"><span data-stu-id="465f7-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="465f7-117">**TSTimesheetEntry** - Zaman çizelgesi hareket sözleşmesi.</span><span class="sxs-lookup"><span data-stu-id="465f7-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="465f7-118">Bu nesnelerin aynı proje bilgilerine ve **timesheetLineRecId** değerine sahip grupları bir satır oluşturur.</span><span class="sxs-lookup"><span data-stu-id="465f7-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="465f7-119">fieldBaseType (Türler)</span><span class="sxs-lookup"><span data-stu-id="465f7-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="465f7-120">**TsTimesheetCustom** nesnesindeki **FieldBaseType** özelliği, uygulamada görünen alanın türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="465f7-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="465f7-121">Desteklenen **Türler** değerleri aşağıdaki gibidir.</span><span class="sxs-lookup"><span data-stu-id="465f7-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="465f7-122">Türler değeri</span><span class="sxs-lookup"><span data-stu-id="465f7-122">Types value</span></span> | <span data-ttu-id="465f7-123">Türü</span><span class="sxs-lookup"><span data-stu-id="465f7-123">Type</span></span>              | <span data-ttu-id="465f7-124">Notlar</span><span class="sxs-lookup"><span data-stu-id="465f7-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="465f7-125">0</span><span class="sxs-lookup"><span data-stu-id="465f7-125">0</span></span>           | <span data-ttu-id="465f7-126">Dize (ve Enum)</span><span class="sxs-lookup"><span data-stu-id="465f7-126">String (and Enum)</span></span> | <span data-ttu-id="465f7-127">Alan bir metin alanı olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="465f7-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="465f7-128">1</span><span class="sxs-lookup"><span data-stu-id="465f7-128">1</span></span>           | <span data-ttu-id="465f7-129">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="465f7-129">Integer</span></span>           | <span data-ttu-id="465f7-130">Değer, ondalık basamak içermeyen bir sayı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="465f7-131">2</span><span class="sxs-lookup"><span data-stu-id="465f7-131">2</span></span>           | <span data-ttu-id="465f7-132">Gerçek</span><span class="sxs-lookup"><span data-stu-id="465f7-132">Real</span></span>              | <span data-ttu-id="465f7-133">Değer, ondalık basamak içeren bir sayı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="465f7-134">Gerçek değeri uygulamadaki bir para birimi olarak göstermek için **fieldExtenededType** özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="465f7-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="465f7-135">Gösterilen ondalık basamak sayısını ayarlamak için **numberOfDecimals** özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="465f7-136">3</span><span class="sxs-lookup"><span data-stu-id="465f7-136">3</span></span>           | <span data-ttu-id="465f7-137">Tarih</span><span class="sxs-lookup"><span data-stu-id="465f7-137">Date</span></span>              | <span data-ttu-id="465f7-138">Tarih biçimleri **Kullanıcı seçeneklerinde**, **Dil ve ülke/bölge tercihlerinde** altında belirtilen **Tarih, saat ve sayı biçimi** ayarıyla belirlenir.</span><span class="sxs-lookup"><span data-stu-id="465f7-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="465f7-139">4</span><span class="sxs-lookup"><span data-stu-id="465f7-139">4</span></span>           | <span data-ttu-id="465f7-140">Boole</span><span class="sxs-lookup"><span data-stu-id="465f7-140">Boolean</span></span>           | |
| <span data-ttu-id="465f7-141">15</span><span class="sxs-lookup"><span data-stu-id="465f7-141">15</span></span>          | <span data-ttu-id="465f7-142">GUID</span><span class="sxs-lookup"><span data-stu-id="465f7-142">GUID</span></span>              | |
| <span data-ttu-id="465f7-143">16</span><span class="sxs-lookup"><span data-stu-id="465f7-143">16</span></span>          | <span data-ttu-id="465f7-144">Int64</span><span class="sxs-lookup"><span data-stu-id="465f7-144">Int64</span></span>             | |

- <span data-ttu-id="465f7-145">**TSTimesheetCustomField** nesnesinde **stringOptions** özelliği sağlanmadıysa, kullanıcıya bir serbest metin alanı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="465f7-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="465f7-146">**stringLength**özelliği, kullanıcıların girebileceği maksimum dize uzunluğunu ayarlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="465f7-147">**TSTimesheetCustomField** nesnesinde **stringOptions**özelliği sağlanmışsa, kullanıcıların seçenek düğmelerini (radyo düğmeleri) kullanarak seçim yapabilen tek değerleri bu liste öğeleridir.</span><span class="sxs-lookup"><span data-stu-id="465f7-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="465f7-148">Bu durumda, dize alanı kullanıcı girişi amacıyla bir enum değeri olarak davranabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="465f7-149">Değeri veritabanına bir enum olarak kaydetmek için, komut zinciri kullanarak veritabanına kaydetmeden önce dize değerini el ile numaralama değerine geri eşleyin (bir zaman çizelgesi girdisini uygulamadan önce, bir Timesheet girişini kullanarak yeniden görüntülemek için "Veritabanına uygulamadan geri TSTimesheetEntryService sınıfı üzerinde bir komut zinciri kullanın" bölümünde bir örnek olarak da yer almaktadır).</span><span class="sxs-lookup"><span data-stu-id="465f7-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="465f7-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="465f7-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="465f7-151">Gerçek değerleri para birimi olarak biçimlendirmek için bu özelliği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="465f7-152">Bu yaklaşım yalnızca **fieldBaseType** değeri **Gerçek** ise uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="465f7-153">**TSCustomFieldExtendedType:None** – Biçimlendirme uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="465f7-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="465f7-154">**TSCustomFieldExtendedType::Currency** – Değeri para birimi olarak biçimlendir.</span><span class="sxs-lookup"><span data-stu-id="465f7-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="465f7-155">Para birimi biçimlendirmesi etkin olduğunda, **stringValue** alanı, uygulamada gösterilmesi gereken para birimi kodunu geçirebilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="465f7-156">Bu değer salt okunur bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="465f7-156">The value is a read-only value.</span></span>

    <span data-ttu-id="465f7-157">**realValue** alanı, veritabanına kaydedilmesi gereken para tutarını içerir.</span><span class="sxs-lookup"><span data-stu-id="465f7-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="465f7-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="465f7-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="465f7-159">Özel alanın uygulamada nerede görüneceğini belirtmek için bu özelliği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="465f7-160">**TSCustomFieldSection::Header** – Alan, uygulamanın **Daha fazla ayrıntı görüntüle** bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="465f7-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="465f7-161">Bu alanlar her zaman salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="465f7-161">These fields are always read-only.</span></span>
- <span data-ttu-id="465f7-162">**TSCustomFieldSection::Line** – Alan, zaman çizelgesi girişlerinde diğer tüm kullanıma hazır satır alanlarından sonra görünür.</span><span class="sxs-lookup"><span data-stu-id="465f7-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="465f7-163">Bu alanlar düzenlenebilir ya da salt okunur olabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="465f7-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="465f7-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="465f7-165">Bu özellik, uygulamanın sağladığı değerler veritabanına geri kaydedildiğinde alanı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="465f7-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="465f7-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="465f7-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="465f7-167">Bu özellik, uygulamanın sağladığı değerler veritabanına geri kaydedildiğinde alanı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="465f7-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="465f7-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="465f7-168">isEditable (NoYes)</span></span>

<span data-ttu-id="465f7-169">Bu özelliği, alanın zaman çizelgesi girişi bölümünde kullanıcılar tarafından düzenlenebilir olduğunu belirtmek için **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="465f7-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="465f7-170">Özelliği **Hayır** olarak ayarlayarak alanı salt okunur yapın.</span><span class="sxs-lookup"><span data-stu-id="465f7-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="465f7-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="465f7-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="465f7-172">Bu özelliği, alanın zaman çizelgesi girişi bölümünde zorunlu olduğunu belirtmek için **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="465f7-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="465f7-173">etiket (str)</span><span class="sxs-lookup"><span data-stu-id="465f7-173">label (str)</span></span>

<span data-ttu-id="465f7-174">Bu özellik, uygulama içinde alanın yanında gösterilen etiketi belirtir.</span><span class="sxs-lookup"><span data-stu-id="465f7-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="465f7-175">stringOptions (Dizeler listesi)</span><span class="sxs-lookup"><span data-stu-id="465f7-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="465f7-176">Bu özellik, yalnızca **fieldBaseType**, **Dize** olarak ayarlandıysa uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="465f7-177">**stringOptions** ayarlanmışsa, seçenek düğmeleri (radyo düğmeleri) aracılığıyla seçim için kullanılabilen dize değerleri listedeki dizelerle belirtilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="465f7-178">Hiçbir dize sağlanmazsa, dize alanındaki serbest metin girişine izin verilir (Bu konunun ilerleyen kısımlarında yer alan "Uygulamadan bir zaman çizelgesi girdisini veritabanına geri kaydetmek için TSTimesheetEntryService sınıfı üzerinde komut zinciri kullan" bölümüne bakın).</span><span class="sxs-lookup"><span data-stu-id="465f7-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="465f7-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="465f7-179">stringLength (int)</span></span>

<span data-ttu-id="465f7-180">Bu özellik bir dize alanı için maksimum uzunluğu belirtir.</span><span class="sxs-lookup"><span data-stu-id="465f7-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="465f7-181">Yalnızca **fieldBaseType**, **Dize** olarak ayarlandıysa uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="465f7-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="465f7-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="465f7-183">Bu özellik, gerçek bir alan için gösterilen ondalık basamak sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="465f7-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="465f7-184">Yalnızca **fieldBaseType**, **Gerçek** olarak ayarlandıysa uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="465f7-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="465f7-185">orderSequence (int)</span></span>

<span data-ttu-id="465f7-186">Bu özellik, birden çok özel alan belirtildiğinde, özel alanların uygulamada gösterilme sırasını denetler.</span><span class="sxs-lookup"><span data-stu-id="465f7-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="465f7-187">Daha düşük sayıya sahip alanlar önce gösterilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="465f7-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="465f7-188">booleanValue (boolean)</span></span>

<span data-ttu-id="465f7-189">**Boole** türü alanlar için bu özellik alanın Boole değerini sunucu ve uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="465f7-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="465f7-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="465f7-190">guidValue (guid)</span></span>

<span data-ttu-id="465f7-191">**GUID** türü alanlar için bu özellik alanın genel benzersiz kimlik tanımlayıcı (GUID) değerini sunucu ve uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="465f7-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="465f7-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="465f7-192">int64Value (int64)</span></span>

<span data-ttu-id="465f7-193">**Int64** türü alanlar için bu özellik alanın int64 değerini sunucu ve uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="465f7-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="465f7-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="465f7-194">intValue (int)</span></span>

<span data-ttu-id="465f7-195">**Int** türü alanlar için bu özellik alanın int değerini sunucu ve uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="465f7-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="465f7-196">realValue (gerçek)</span><span class="sxs-lookup"><span data-stu-id="465f7-196">realValue (real)</span></span>

<span data-ttu-id="465f7-197">**Gerçek** türü alanlar için bu özellik alanın gerçek değerini sunucu ve uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="465f7-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="465f7-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="465f7-198">stringValue (str)</span></span>

<span data-ttu-id="465f7-199">**Dize** türü alanlar için bu özellik alanın dize değerini sunucu ve uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="465f7-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="465f7-200">Ayrıca, **Gerçek** tür alanları için para birimi olarak biçimlendirilen alanlar için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="465f7-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="465f7-201">Bu alanlar için, özellik para birimi kodunu uygulamaya geçirmek amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="465f7-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="465f7-202">dateValue (tarih)</span><span class="sxs-lookup"><span data-stu-id="465f7-202">dateValue (date)</span></span>

<span data-ttu-id="465f7-203">**Tarih** türü alanlar için bu özellik alanın tarih değerini sunucu ve uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="465f7-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="465f7-204">Zaman çizelgesi girişi bölümünde özel alanı gösterir ve kaydeder</span><span class="sxs-lookup"><span data-stu-id="465f7-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="465f7-205">Aşağıda, zaman çizelgesi girdi oluşturmayla ilgili mobil uygulamadan alınan bir ekran görüntüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="465f7-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="465f7-206">Kullanıma hazır alanları ve "test dizesi" adı verilen "Ikinci seçenek" bölümünde zaten ayarlanmış olan bir özel alanı "İkinci seçenek" olarak gösterir.</span><span class="sxs-lookup"><span data-stu-id="465f7-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Uygulamadaki sınama dizesi özel alanı](media/timesheet-entry.jpg)



<span data-ttu-id="465f7-208">"Test dizesi" özel alanı için kullanılabilen enum seçeneklerinden birini seçerek, kullanıcının mobil uygulamasına ait bir ekran görüntüsü aşağıdadır.</span><span class="sxs-lookup"><span data-stu-id="465f7-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="465f7-209">Bu iki seçenek, radyo düğmeleri olarak gösterilen "İlk seçenek" ve "İkinci seçenek"dir.</span><span class="sxs-lookup"><span data-stu-id="465f7-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="465f7-210">İkinci seçenek şu anda seçilidir.</span><span class="sxs-lookup"><span data-stu-id="465f7-210">The second option is currently selected.</span></span>

![Test dizesi özel alanı için seçenek düğmeleri (radyo düğmeleri)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="465f7-212">TSTimesheetLine tablosunu, özel bir alana sahip olacağı şekilde genişletin</span><span class="sxs-lookup"><span data-stu-id="465f7-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="465f7-213">Tipik senaryolarda, zaman çizelgesi girişi bölümündeki özel bir alan için veriler TSTimesheetLine tablosuna kaydedilmesinden kaynaklanıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="465f7-214">Ancak, veriler sağlanan TSTimesheetTrans kaydına dayalı olarak alınacaksa veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="465f7-215">Özel alanların yedekleme veritabanı kayıtları içermemesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="465f7-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="465f7-216">Bunlar, X++ mantığına dayalı olarak dinamik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="465f7-217">Bu yaklaşım, salt okunur senaryolarda yararlı olabilir (dinamik olarak oluşturulmuş özel alan değerleri örneği için, TSTimesheetDetails sınıfındaki komut zinciri, buildCustomFieldListForHeader yöntemi).</span><span class="sxs-lookup"><span data-stu-id="465f7-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="465f7-218">Aşağıda Visual Studio'da yer alan Uygulama Nesne Ağacı bir ekran görüntüsü bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="465f7-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="465f7-219">TSTimesheetLine tablosunun bir uzantısını, TestLineString alanı özel alanı olarak eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="465f7-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Satır dizesi](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="465f7-221">Zaman çizelgesi girişi bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zinciri kullanın</span><span class="sxs-lookup"><span data-stu-id="465f7-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="465f7-222">Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="465f7-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="465f7-223">Örneğin, alan türünü, etiketini, alanın zorunlu olup olmayacağını ve alanın hangi bölümünde göründüğünü kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="465f7-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="465f7-224">Aşağıdaki örnek zaman girişlerinde bir dize alanını gösterir.</span><span class="sxs-lookup"><span data-stu-id="465f7-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="465f7-225">Bu alan, seçenek düğmeleri (radyo düğmeleri) ile **İlk seçenek** ve **İkinci seçenek** olan iki seçenek bulunur.</span><span class="sxs-lookup"><span data-stu-id="465f7-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="465f7-226">Uygulamadaki alan, TSTimesheetLine tablosuna eklenen **TestLineString** alanıyla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="465f7-227">**TSTimesheetCustomField::newFromMetatdata()** yönteminin özel alana başlatılmasını basitleştirilmiş: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ve **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="465f7-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="465f7-228">Bu parametreleri, dilerseniz el ile de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="465f7-229">TSTimesheetEntry sınıfının buildCustomFieldListForEntry yönteminde bir komut zinciri kullanarak bir zaman çizelgesi girişine değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="465f7-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="465f7-230">**buildCustomFieldListForEntry** yöntemi, mobil uygulamadaki kaydedilmiş zaman çizelgesi satırlarına değer girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="465f7-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="465f7-231">Bir TSTimesheetTrans kaydını parametre olarak alır.</span><span class="sxs-lookup"><span data-stu-id="465f7-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="465f7-232">Bu kayıttaki alanlar uygulamadaki özel alan değerini doldurmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="465f7-233">Bir zaman çizelgesi girdisini veritabanından veritabanına geri kaydetmek için TSTimesheetEntryService sınıfında zincir komutunu kullanın</span><span class="sxs-lookup"><span data-stu-id="465f7-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="465f7-234">Bir özel alanı normal kullanım sırasında veritabanına geri kaydetmek için, birden çok yöntemi genişletmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="465f7-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="465f7-235">**timesheetLineNeedsUpdating** yöntemi, satır kaydının uygulamadaki Kullanıcı tarafından değiştirilip değiştirilmediğini ve veritabanına kaydedilmesi gerekip alınmayacağını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="465f7-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="465f7-236">Performans sorun değilse, bu yöntem her zaman **doğru** dönen şekilde basitleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="465f7-237">**populateTimesheetLineFromEntryDuringCreate** ve **populateTimesheetLineFromEntryDuringUpdate** yöntemleri uzatılabilecek ve TSTimesheetLine'deki TSTimesheetEntry veritabanı kaydına değer girmeleri için genişletilebilir sağlanan veri sözleşme kaydı.</span><span class="sxs-lookup"><span data-stu-id="465f7-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="465f7-238">Aşağıdaki örnekte, veritabanı alanı ile giriş alanı arasındaki eşlemenin X++ kodu aracılığıyla el ile nasıl yapıldığı konusunda dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="465f7-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="465f7-239">**populateTimesheetWeekFromEntry** yöntemi, **TSTimesheetEntry** nesnesiyle eşlenen özel alan TSTimesheetLineweek veritabanı tablosuna geri yazması gerekiyorsa da genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="465f7-240">Aşağıdaki örnek kullanıcının veritabanına seçtiğini **firstOption** veya **secondOption** değerini bir ham dize değeri olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="465f7-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="465f7-241">Veritabanı alanı **Enum** türünde bir alan ise, bu değerler el ile bir Enum değeriyle eşleştirilebilir ve veritabanı tablosundaki bir Enum alanına kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="465f7-242">Zaman çizelgesi başlık bölümünde bir özel alan göster</span><span class="sxs-lookup"><span data-stu-id="465f7-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="465f7-243">Aşağıda, kullanıcı bir zaman çizelgesi görüntüleme ilgili mobil uygulamadan alınan bir ekran görüntüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="465f7-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="465f7-244">Sağ üst köşedeki "Daha fazla bilgi" düğmesi, "Daha fazla ayrıntı görüntüle" seçeneği gösterilsin şekilde seçildi.</span><span class="sxs-lookup"><span data-stu-id="465f7-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Diğer ayrıntıları görüntüle komutu](media/show-more.png)



<span data-ttu-id="465f7-246">Aşağıda, bir zaman çizelgesinin "Daha fazla" bölümünü gösterir ilgili mobil uygulamadan alınan bir ekran görüntüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="465f7-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="465f7-247">Zaman çizelgesi başlığı bölümüne, "Bu zaman çizelgesinin kullanım oranı (hesaplanan özel alan)" adında bir özel alan eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="465f7-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="465f7-248">Özel alanda "0,667" salt okunur değeri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="465f7-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Daha fazla bölümü](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="465f7-250">TSTimesheetTable tablosunu, özel bir alana sahip olacağı şekilde genişletin</span><span class="sxs-lookup"><span data-stu-id="465f7-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="465f7-251">Tipik senaryolarda, başlık bölümündeki özel bir alan için veriler TSTimesheetHeader tablosuna çekilmesinden kaynaklanıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="465f7-252">Ancak, veriler sağlanan TSTimesheetTable kaydına dayalı olarak alınacaksa veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="465f7-253">Özel alanların yedekleme veritabanı kayıtları içermemesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="465f7-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="465f7-254">Bunlar, X++ mantığına dayalı olarak dinamik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="465f7-255">Aşağıdaki örnek bu yaklaşımı gösterir.</span><span class="sxs-lookup"><span data-stu-id="465f7-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="465f7-256">Üst bilgi bölümündeki alanlar uygulamada her zaman salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="465f7-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="465f7-257">Başlık bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zinciri kullanın</span><span class="sxs-lookup"><span data-stu-id="465f7-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="465f7-258">Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="465f7-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="465f7-259">Örneğin, alan türünü, etiketini, alanın zorunlu olup olmayacağını ve alanın hangi bölümünde göründüğünü kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="465f7-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="465f7-260">Aşağıdaki örnek, uygulamadaki başlık bölümünde hesaplanan bir değeri gösterir.</span><span class="sxs-lookup"><span data-stu-id="465f7-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="465f7-261">TSTimesheetDetails sınıfının buildCustomFieldListForHeader yönteminde bir komut zinciri kullanarak bir zaman çizelgesi ayrıntıları değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="465f7-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="465f7-262">**buildCustomFieldListForHeader** yöntemi, mobil uygulamadaki zaman çizelgesi başlık ayrıntılarını doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="465f7-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="465f7-263">Bir TSTimesheetTable kaydını parametre olarak alır.</span><span class="sxs-lookup"><span data-stu-id="465f7-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="465f7-264">Bu kayıttaki alanlar uygulamadaki özel alan değerini doldurmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="465f7-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="465f7-265">Aşağıdaki örnek, veritabanından herhangi bir değeri okumaz.</span><span class="sxs-lookup"><span data-stu-id="465f7-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="465f7-266">Bunun yerine, uygulama içinde gösterilen bir hesaplanmış değer oluşturmak için X++ mantığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="465f7-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="465f7-267">Diğer yapılandırılabilirlik/genişletilebilirlik fırsatları</span><span class="sxs-lookup"><span data-stu-id="465f7-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="465f7-268">Uygulama için ek doğrulama ekleniyor</span><span class="sxs-lookup"><span data-stu-id="465f7-268">Adding additional validation for the app</span></span>

<span data-ttu-id="465f7-269">Veritabanı düzeyindeki zaman çizelgesi işlevselliği için varolan mantık yine de beklendiği gibi çalışır.</span><span class="sxs-lookup"><span data-stu-id="465f7-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="465f7-270">Kaydetme veya gönderme işlemlerinin tamamlanmasını durdurmak ve belirli bir hata iletisini göstermek için, komut uzantısı zinciri yoluyla koda **hata ver ("kullanıcıya ileti")** ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="465f7-271">İşte yararlı genişletilebilir yöntemlerine üç örnek:</span><span class="sxs-lookup"><span data-stu-id="465f7-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="465f7-272">**validateWrite**, TSTimesheetLine tablosunda kaydetme işlemi sırasında bir zaman çizelgesi satırı için **yanlış** dönerse, bir hata mesajı mobil uygulamada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="465f7-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="465f7-273">**validateSubmit**, TSTimesheetTable tablosunda bir zaman çizelgesi için uygulamaya gönderme sırasında **yanlış** dönerse, bir hata mesajı kullanıcıya görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="465f7-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="465f7-274">TSTimesheetLine tablosundaki **insert** yöntemi sırasında alanları dolduran (örneğin, **satır özelliği**) mantık çalışmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="465f7-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="465f7-275">Kullanıma alan alanları konfigürasyon aracılığıyla salt okunur gizleme ve işaretleme</span><span class="sxs-lookup"><span data-stu-id="465f7-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="465f7-276">Proje parametrelerinden, kullanıma hazır alanları mobil uygulamada salt okunur veya gizli yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="465f7-277">**Proje yönetimi ve hesap oluşturma parametreleri** sayfasının **zaman çizelgesi** sekmesindeki **mobil zaman çizelgeleri** bölümünde bulunan seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="465f7-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Proje parametreleri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="465f7-279">Uzantılar aracılığıyla seçim için kullanılabilen etkinlikleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="465f7-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="465f7-280">**getActivitiesForProject()** ve **getActivityQuery()** yöntemleri ile **TsTimesheetProjectService** sınıfında doldurulan bir proje için seçimde kullanılabilen etkinlikler.</span><span class="sxs-lookup"><span data-stu-id="465f7-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="465f7-281">Belirli bir proje için kullanılabilir olan etkinlikler için bu davranışı iş senaryonuz ile eşleştirmek üzere değiştirmek için komut zinciri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="465f7-282">Zaman çizelgesi girişlerine varsayılan proje kategorisi girme</span><span class="sxs-lookup"><span data-stu-id="465f7-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="465f7-283">Zaman çizelgesi girişlerinde varsayılan proje kategorisi girişi üç düzeyde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="465f7-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="465f7-284">İstenen davranışı elde etmek için bu düzeylerin herhangi birinin veya tümünün davranışını uzatmak amacıyla komut zinciri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="465f7-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="465f7-285">Aşağıdaki hiyerarşisi kullanılır:</span><span class="sxs-lookup"><span data-stu-id="465f7-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="465f7-286">Uygulama, proje kaynağındaki varsayılan kategoriyi yerleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="465f7-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="465f7-287">Bu varsayılan kategori **getCurrentUserResource** ve **getDelegatedResourcesForCurrentUser** yöntemleri, **TSTimesheetSettingsService** sınıfında ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="465f7-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="465f7-288">Proje kaynak düzeyinde varsayılan kategori sağlanmamışsa, uygulama bunu proje etkinliğinden almaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="465f7-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="465f7-289">Bu varsayılan kategori, **TSTimesheetProjectService** sınıfının **getActivitiesForProject** yönteminde ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="465f7-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="465f7-290">Proje etkinlik düzeyinde varsayılan kategori sağlanmamışsa, varsayılan kategori proje parametrelerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="465f7-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="465f7-291">Bu varsayılan kategori, **TSTimesheetProjectService** sınıfının **getProjectDetailsbyRule** yönteminde ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="465f7-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
