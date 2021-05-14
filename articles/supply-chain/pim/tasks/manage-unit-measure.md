---
title: Ölçü birimlerini yönetme
description: Bu konu; bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921353"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="c8835-103">Ölçü birimlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="c8835-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8835-104">Bu konu; bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8835-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="c8835-105">Birimler sayfasını açma</span><span class="sxs-lookup"><span data-stu-id="c8835-105">Open the Units page</span></span>

<span data-ttu-id="c8835-106">Sisteminizde kullanılabilen ölçü birimlerini oluşturmak ve bunlarla çalışmak için **Kuruluş Yönetimi \> Kurulum \> Birimler \>Birimler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c8835-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="c8835-107">Bu konunun geri kalan bölümleri, **Birimler** sayfasında neler yapabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c8835-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="c8835-108">Standart birimler ve dönüşümler oluşturma</span><span class="sxs-lookup"><span data-stu-id="c8835-108">Create standard units and conversions</span></span>

<span data-ttu-id="c8835-109">Sisteminiz metrik sistem ve/veya ABD geleneksel sistemi (USCS) için en sık kullanılan ölçü birimlerini içermiyorsa, birim kurulum sihirbazı, temel birim tanımları ve dönüştürmelere hızlı şekilde başlamanıza yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c8835-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="c8835-110">Sihirbazı tamamlamak için, Eylem Bölmesinde **Birim oluşturma sihirbazı**'nı seçin ve sonra ekrandaki talimatları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8835-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="c8835-111">Bir ölçü birimi oluşturma veya düzenleme</span><span class="sxs-lookup"><span data-stu-id="c8835-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="c8835-112">Bir ölçü birimi oluşturmak veya düzenlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8835-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="c8835-113">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="c8835-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="c8835-114">Varolan bir birimi düzenlemek için, birimi liste bölmesinde seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="c8835-115">Yeni bir birim oluşturmak için Eylem Bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="c8835-116">Kaydın üst bilgisinde aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c8835-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="c8835-117">**Birim** – Sistem dilinde birime başvuruda bulunmak için kullanılacak kodu veya simgeyi girin.</span><span class="sxs-lookup"><span data-stu-id="c8835-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="c8835-118">Bu kod veya simge genellikle birim için ortak bir kısaltmadır (örneğin, her biri için *beher* veya santimetre için *cm*).</span><span class="sxs-lookup"><span data-stu-id="c8835-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="c8835-119">**Açıklama** – Sistem dilinde birim için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c8835-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="c8835-120">Bu ad genellikle birimin tam adıdır. Örneğin *Her biri* veya *Santimetre* gibi.</span><span class="sxs-lookup"><span data-stu-id="c8835-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="c8835-121">**Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c8835-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="c8835-122">**Birim sınıfı** – Birimin ölçtüğü özelliği seçin (uzunluk, alan, kütle veya miktar gibi).</span><span class="sxs-lookup"><span data-stu-id="c8835-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="c8835-123">**Birim sistemi** – Birimin ait olduğu ölçü sistemini seçin (*Metrik birimler* veya *Amerika Birleşik Devletleri geleneksel birimler*).</span><span class="sxs-lookup"><span data-stu-id="c8835-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="c8835-124">**Temel birim** – Birim sınıfı için temel birim olarak geçerli birimi kullanmak için bu seçeneği *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="c8835-125">Bu durumda, temel birim ve birim sınıfındaki her ek birim arasında dönüştürme faktörünü belirtmeniz yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="c8835-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="c8835-126">Sistem daha sonra bu birim sınıfındaki tüm birimler arasında dönüştürme yapabilir.</span><span class="sxs-lookup"><span data-stu-id="c8835-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="c8835-127">Bu nedenle, dönüşümleri ayarlamak daha kolaydır.</span><span class="sxs-lookup"><span data-stu-id="c8835-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="c8835-128">Örneğin, galon, *Hacim* birim sınıfının taban birimiyse, litreden galona ve pintten galona dönüştürme faktörlerini ayarlamanız yeterli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="c8835-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="c8835-129">Sistem ardından litreden pinte dönüşümü gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="c8835-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="c8835-130">Her birim sınıfı için yalnızca bir temel birime sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8835-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="c8835-131">**Sistem birimi** – Birim sınıfında belirlenmemiş tüm ölçümler için varsayılan birim olarak geçerli birimi kullanmak için bu seçeneği *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="c8835-132">Örneğin, bir miktar girmek için kullanılan bir alan bir birimin belirtilmesine izin vermiyorsa (veya kullanıcı bir birim seçmezse), sistem *Miktar* birim sınıfı için sistem birimi olarak ayarlanan birimi kullanır .</span><span class="sxs-lookup"><span data-stu-id="c8835-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="c8835-133">Her birim sınıfı için yalnızca bir sistem birimine sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8835-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="c8835-134">**Ondalık duyarlık** – Geçerli birim için belirtilen veya kendisine dönüştürülen değerlerin yuvarlanacak ondalık basamak sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c8835-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="c8835-135">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="c8835-136">Birim çevirilerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="c8835-136">Define unit translations</span></span>

<span data-ttu-id="c8835-137">Kod veya simge için çeviriler ve ölçü biriminin açıklamasını tanımlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8835-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="c8835-138">Çevirileri oluşturmak için birim oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="c8835-139">Eylem Bölmesi'nde, **Birim metinleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="c8835-140">**Birim metinleri** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c8835-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="c8835-141">Seçili birimin kimliğine veya simgesine ait çevirileri tanımlamak için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8835-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="c8835-142">Daha sonra bu çeviriler müşteriye özgü veya satıcıya özgü dillerdeki harici belgelerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c8835-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="c8835-143">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c8835-144">**Dil** alanında, birim kimliği veya simgesinin çevrileceği dili seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="c8835-145">**Metin** alanında, seçilen dilde birim kodunun veya sembolün çevirisini girin.</span><span class="sxs-lookup"><span data-stu-id="c8835-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="c8835-146">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c8835-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8835-147">Close the page.</span></span>
1. <span data-ttu-id="c8835-148">**Eylem Bölmesi**'nde, **Çevrilmiş birim açıklamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="c8835-149">**Çevrilen birim açıklamaları** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c8835-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="c8835-150">Bu sayfayı, seçili birimin dile özgü açıklamalarını tanımlamak için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="c8835-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="c8835-151">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c8835-152">**Dil** alanında, birim açıklamasının çevrileceği dili seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="c8835-153">**Açıklama** alanında, seçilen dilde birim açıklamasının çevirisini girin.</span><span class="sxs-lookup"><span data-stu-id="c8835-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="c8835-154">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c8835-155">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8835-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="c8835-156">Birim dönüştürme kurallarını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="c8835-156">Define unit conversion rules</span></span>

<span data-ttu-id="c8835-157">Ölçü birimleri arasında dönüştürmelere yönelik kurallar tanımlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8835-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="c8835-158">Dönüştürme kuralları için birim oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="c8835-159">Eylem Bölmesi'nde, **Birim dönüşümleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="c8835-160">**Birim dönüştürmeleri** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c8835-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="c8835-161">Bu sayfayı kullanarak seçili birimi birim sınıfında bir başka ölçü birimine dönüştürmek için kurallar tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="c8835-162">Ayarlamak istediğiniz dönüştürme türüne bağlı olarak aşağıdaki sekmelerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="c8835-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="c8835-163">**Standart dönüştürmeler** – Tüm ürünler için standart dönüştürme kuralları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="c8835-164">**Sınıf içi dönüştürmeler** – Aynı birim sınıfındaki birimler için ürüne özgü dönüştürme kuralları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="c8835-165">**Sınıf arası dönüştürmeler** – Birim sınıfları arasındaki birimler için ürüne özgü dönüştürme kuralları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="c8835-166">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="c8835-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="c8835-167">Yeni bir dönüştürme oluşturmak için araç çubuğunda **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="c8835-168">Varolan bir dönüştürmeyi düzenlemek için, ızgarada dönüştürmeyi seçin ve araç çubuğundan **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="c8835-169">Görüntülenen açılır iletişim kutusunda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c8835-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="c8835-170">**Ürün** - Dönüştürmenin uygulandığı belirli ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="c8835-171">Bu alan yalnızca sınıf içi ve sınıf arası dönüştürmeler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c8835-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="c8835-172">**Formül düzeni** – Tek etmene sahip basit bir dönüştürme belirtmek için bu alanı *Basit* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="c8835-173">Daha karmaşık bir denklem ayarlamak için bunu *Gelişmiş* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8835-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="c8835-174">Gelişmiş denklemler biçimi, birim sınıfa bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="c8835-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="c8835-175">**Kaynak birim** – Bu alan, seçilen birimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8835-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="c8835-176">Genellikle, değeri değiştirmemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c8835-176">Usually, you should not change the value.</span></span> <span data-ttu-id="c8835-177">(Değeri değiştirirseniz, kaydettikten sonra yeni dönüştürmeyi görüntülemek için seçili birime ait **Birim dönüştürmeleri** sayfasını kullanabilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="c8835-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="c8835-178">**Hedef birim** – Dönüştürülecek birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="c8835-179">**Yuvarlama** – Kesirlerin, seçilen birimin **Ondalık duyarlık** değerine ( *En yakına*, *Yukarı* veya *Aşağı*) göre nasıl yuvarlanacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="c8835-180">**Dönüştürme formülü** – İki birim arasındaki dönüştürme formülü belirtmek için açılır iletişim kutusunun üst kısmındaki kalan alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8835-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="c8835-181">Kullanılabilir alanlar, seçtiğiniz birim sınıfına ve formül düzenine göre değişir.</span><span class="sxs-lookup"><span data-stu-id="c8835-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="c8835-182">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8835-182">Select **OK**.</span></span>
1. <span data-ttu-id="c8835-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8835-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="c8835-184">Ayrıca, her bir ürün varyantı için birim dönüştürmeleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8835-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="c8835-185">Daha fazla bilgi için bkz. [Ürün çeşidi başına ölçü birimi dönüşümü](../uom-conversion-per-product-variant.md)</span><span class="sxs-lookup"><span data-stu-id="c8835-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
