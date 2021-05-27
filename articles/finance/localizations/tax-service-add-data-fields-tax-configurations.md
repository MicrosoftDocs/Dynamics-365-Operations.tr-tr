---
title: Vergi yapılandırmalarına veri alanları Ekleme
description: Bu konu, veri alanları ekleyerek vergi yapılandırmalarının nasıl özelleştirileceğini açıklamaktadır.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ebb186a4cb9ca61399909625233b579acd2c0ec5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022799"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="a613a-103">Vergi yapılandırmalarına veri alanları Ekleme</span><span class="sxs-lookup"><span data-stu-id="a613a-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a613a-104">Bu konu [vergi tümleştirmesinde eklenen veri alanlarını](tax-service-add-data-fields-tax-integration-by-extension.md) kullanarak vergi yapılandırmalarının nasıl özelleştirileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a613a-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="a613a-105">Vergi veri modeli yapılandırmasını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="a613a-105">Customize the tax data model</span></span>

1. <span data-ttu-id="a613a-106">Microsoft Dynamics 365 Finance'te **Elektronik raporlama** \> **Vergi Yapılandırmaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a613a-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="a613a-107">Yapılandırma ağacında, **vergi veri modeli-Avrupa**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="a613a-108">Ardından Eylem bölmesinden **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="a613a-109">Açılan iletişim kutusunda, **Vergi veri modeli -- Avrupa, Microsoft adından türetilen vergiye tabi belge modelini** seçin, yeni vergi veri modeli için bir ad girin ve sonra **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="a613a-110">Oluşturduğunuz vergi veri modelini seçin ve sonra eylem bölmesinde **tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="a613a-111">Veri modeli ağacını genişletin, **Satırlar**'ı seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="a613a-112">**Düğüm oluştur** iletişim kutusunda bir ad girin, öğe türünü belirtin ve sonra **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="a613a-113">Gerekli sütunları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a613a-113">Add any required columns.</span></span>
8. <span data-ttu-id="a613a-114">Eylem Bölmesinde, **Kaydet**'i ve sonra **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="a613a-115">Sayfayı kapatın ve vergi veri modelinizin tamamlanan sürümünü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="a613a-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="a613a-116">Vergi yapılandırmasını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="a613a-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="a613a-117">Finance'te **Elektronik raporlama** \> **Vergi Yapılandırmaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a613a-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="a613a-118">Yapılandırma ağacında, **vergi yapılandırması -- Avrupa**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="a613a-119">Ardından Eylem bölmesinden **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="a613a-120">Açılan iletişim kutusunda, **Vergi Yapılandırması -- Avrupa, Microsoft adından türetilen vergi hizmeti yapılandırmasını** seçin, yeni vergi yapılandırması için bir ad girin ve sonra **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="a613a-121">Oluşturduğunuz vergi yapılandırmasını seçin ve sonra eylem bölmesinde **tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="a613a-122">**Özellikler** bölümünde, **veri modeli** alanında, önceden oluşturduğunuz özelleştirilmiş vergi veri modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="a613a-123">**Veri modeli sürümü** alanında, vergi veri modelinin tamamlanmış sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="a613a-124">**Ekle**'yi seçin ve gerekli vergi ölçümlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a613a-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="a613a-125">Eylem Bölmesinde, **Kaydet**'i ve sonra **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="a613a-126">Sayfayı kapatın ve vergi yapılandırmanızın tamamlanan sürümünü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="a613a-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="a613a-127">Özelleştirilmiş vergi yapılandırmasındaki vergi özelliklerini Uygulama</span><span class="sxs-lookup"><span data-stu-id="a613a-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="a613a-128">Regulatory Configuration Services'te (RCS) **Genelleştirme Özellikleri** \> **Vergi**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="a613a-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="a613a-129">**Ekle**'yi seçin, yeni özellik hakkındaki bilgileri girin ve sonra **Oluştur** özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="a613a-130">**Sürümler** sekmesinde özelliği seçin ve sonra **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="a613a-131">**Genel** sekmesinde, **Yapılandırma sürümü** alanında, özelleştirilmiş vergi yapılandırmasını ve sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="a613a-132">**Sütunları Yönet** iletişim kutusunda, özelleştirilmiş vergi ölçümünüzde olmasını istediğiniz başlık ve satır sütunlarını seçin ve bunları **Seçilen sütunlar** listesine eklemek için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a613a-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
