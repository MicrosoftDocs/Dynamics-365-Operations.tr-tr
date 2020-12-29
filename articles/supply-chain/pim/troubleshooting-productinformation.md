---
title: Ürün bilgileri ile ilgili sorunları giderme
description: Bu konuda, ürün bilgileri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 87b04998889b86a79fd8dabde422147c5494b003
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516897"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="b811a-103">Ürün bilgileri ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="b811a-103">Troubleshoot product information</span></span>

<span data-ttu-id="b811a-104">Bu konuda, ürün bilgileri ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b811a-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="b811a-105">Serbest bırakılan bir ürünü silemiyorum.</span><span class="sxs-lookup"><span data-stu-id="b811a-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-106">Issue description</span></span>

<span data-ttu-id="b811a-107">Serbest bırakılan bir ürünü ve tüm varyantlarını yalnızca serbest bırakılan ürünün ilgili işlemleri yoksa silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b811a-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-108">Issue resolution</span></span>

<span data-ttu-id="b811a-109">Serbest bırakılmış bir ürünü veya ürün yöneticisini silmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b811a-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="b811a-110">Maddeler için tüm açık hareketleri kapatın.</span><span class="sxs-lookup"><span data-stu-id="b811a-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="b811a-111">Stoğu 0'a (sıfır) düşürün.</span><span class="sxs-lookup"><span data-stu-id="b811a-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="b811a-112">Stok kapanışı gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="b811a-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="b811a-113">Silmek istediğiniz ana ürün için tüm ürün varyantlarını silin.</span><span class="sxs-lookup"><span data-stu-id="b811a-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="b811a-114">Serbest bırakılan bir ürünün madde numarasını değiştirebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="b811a-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="b811a-115">Çoğu durumda, bu değişiklik verilerin bozulmasına neden olacağından, serbest bırakılan ürünler için madde numaralarını değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b811a-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="b811a-116">Madde numarasını, [platform güncelleştirmesi 24 ile Finance and Operations 10.0.0 için kaldırılan veya azaltılan özellikler](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24) listesinde belirtildiği gibi, madde numarasını yalnızca serbest bırakılan ürünün birincil anahtarının önceki yeniden adlandırmanın neden olduğu veri bozulmasını onarmanız gerekiyorsa düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b811a-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="b811a-117">Serbest bırakılan ürünler için madde numaralarını da düzenlemek istiyorsanız [Fikirler portalında bu fikre oy verin](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="b811a-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="b811a-118">Üründeki varsayılan otomatik tüketim kuralı, malzeme satırının faturasına girilmiyor.</span><span class="sxs-lookup"><span data-stu-id="b811a-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-119">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-119">Issue description</span></span>

<span data-ttu-id="b811a-120">Bir maddeyi bir ürün reçetesi satırına eklediğinizde, sistem madde için ayarlanan varsayılan otomatik tüketim kuralı bilgilerini kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="b811a-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="b811a-121">Başka bir deyişle, maddeden otomatik tüketim kuralı **Ürün reçetesi satırı** sayfasında görünmez.</span><span class="sxs-lookup"><span data-stu-id="b811a-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-122">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-122">Issue resolution</span></span>

<span data-ttu-id="b811a-123">Bir ürün reçetesi satırında bir otomatik tüketim kuralı belirtirseniz bu, bu ürün reçetesi satırı için geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b811a-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="b811a-124">Ancak, otomatik tüketim kuralı boşsa veya ürün reçetesi satırına ayarlı değilse, madde üzerinde ayarlanan otomatik tüketim kuralı, ürün reçetesi satırında gösterilmese bile bu ürün reçetesi satırı geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b811a-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="b811a-125">Microsoft Dynamics 365 Supply Chain Management'taki diğer özellikler için varsayılan mantık genellikle bu şekilde çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b811a-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="b811a-126">Ancak geçerli davranış değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="b811a-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="b811a-127">Aksi takdirde, buna dayanan bazı mevcut özelleştirmeler bozulabilir.</span><span class="sxs-lookup"><span data-stu-id="b811a-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="b811a-128">Sistem, yinelenen barkodları farklı maddeler veya farklı boyutlara sahip aynı madde için kaydetmemi sağlıyor.</span><span class="sxs-lookup"><span data-stu-id="b811a-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="b811a-129">Sistem şu anda benzersiz barkodları uygulamaz ve bu kısıtlamanın eklenmesi, bozulmaya neden olan bir değişiklik olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b811a-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="b811a-130">Öyle ki, Microsoft'un bazı mevcut müşteri yüklemelerinin bu değişiklik nedeniyle bozulacağını gösteren kanıtları vardır.</span><span class="sxs-lookup"><span data-stu-id="b811a-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="b811a-131">Ancak, gelecekte bu özelliği etkinleştirmek için daha geniş bir tasarım değişikliği düşüneceğiz.</span><span class="sxs-lookup"><span data-stu-id="b811a-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="b811a-132">Madde kayıt şablonlarını düzenlerken aşağıdaki hata iletisini alıyorum: "Maddenin stoğu tutulmadığından ambar konumu oluşturulamıyor.</span><span class="sxs-lookup"><span data-stu-id="b811a-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="b811a-133">Maddeleri stoklamak için ilişkili madde modeli grubundaki Stoğu tutulan ürün seçeneğinin seçilmesi gerekir."</span><span class="sxs-lookup"><span data-stu-id="b811a-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-134">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-134">Issue description</span></span>

<span data-ttu-id="b811a-135">Bu sorun, stoğu tutulmayan olmayan bir madde için şablon oluşturmaya çalışırken bu adımları izlerseniz oluşur.</span><span class="sxs-lookup"><span data-stu-id="b811a-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="b811a-136">Stoğu tutulmayan, serbest bırakılmış bir ürün açın.</span><span class="sxs-lookup"><span data-stu-id="b811a-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="b811a-137">Eylem Bölmesindeki **Seçenekler** sekmesinde, **Kayıt bilgileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b811a-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="b811a-138">**Kayıt bilgileri** iletişim kutusunda **Şirket hesapları şablonu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="b811a-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="b811a-139">Bu durumda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="b811a-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="b811a-140">Maddenin stoğu tutulmadığından ambar konumu oluşturulamıyor.</span><span class="sxs-lookup"><span data-stu-id="b811a-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="b811a-141">Maddeleri stoklamak için ilişkili madde modeli grubundaki Stoğu tutulan ürün seçeneğinin seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b811a-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-142">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-142">Issue resolution</span></span>

<span data-ttu-id="b811a-143">Ürün şablonları oluşturma işlemi, ürüne özel ekstra mantık gerektirir.</span><span class="sxs-lookup"><span data-stu-id="b811a-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="b811a-144">Bu nedenle, bu amaçla genel **Şirket hesapları şablonu** düğmesini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b811a-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="b811a-145">Bunun yerine, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b811a-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="b811a-146">Serbest bırakılan bir ürün açın.</span><span class="sxs-lookup"><span data-stu-id="b811a-146">Open a released product.</span></span>
1. <span data-ttu-id="b811a-147">Eylem Bölmesinde **Ürün** sekmesinde **Yeni** grubunda **Şablon \> Paylaşılan şablon oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b811a-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="b811a-148">Ürün özniteliklerine eklenen Varsayılan Yardım metni, serbest bırakılmış bir ürüne girilmez.</span><span class="sxs-lookup"><span data-stu-id="b811a-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="b811a-149">Ürün özniteliklerine eklenen açıklama ve Yardım metni, serbest bırakılan ürünlerde görünmez veya varsayılan olarak girilen bir metin değildir.</span><span class="sxs-lookup"><span data-stu-id="b811a-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="b811a-150">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="b811a-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="b811a-151">Girilen varsayılan miktar, bir ürün reçetesinden kaydedildiğinde ve ürün reçetesinden kaydedildiğinde farklıdır.</span><span class="sxs-lookup"><span data-stu-id="b811a-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-152">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-152">Issue description</span></span>

<span data-ttu-id="b811a-153">Varsayılan olarak, bir maddeyi bir ürün reçetesine eklediğinizde, seçili bir ürünün **Varsayılan sipariş ayarları** sayfasında **Min. sipariş miktarı** alanında tanımlanan miktar yerine miktar 1 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b811a-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="b811a-154">Ancak, bir ürün reçetesi versiyonundan bir madde eklediğinizde ve madde ve varyant seçildiğinde, varsayılan olarak girilen miktar, belirli boyutlar için varsayılan sipariş ayarlarında ayarlanan minimum miktarı dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="b811a-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-155">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-155">Issue resolution</span></span>

<span data-ttu-id="b811a-156">Bu davranış beklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="b811a-156">This behavior is expected.</span></span> <span data-ttu-id="b811a-157">Ancak, ürün reçetesi ile ürün reçetesi versiyonu arasında mantık farklı olması bilinen bir konudur.</span><span class="sxs-lookup"><span data-stu-id="b811a-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="b811a-158">Yine de, bir değişiklik birçok farklı müşteri senaryosunu etkileyebileceğinden, bu davranış değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="b811a-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="b811a-159">Serbest bırakılan ürün ayrıntılarında, Ürün belge ekleri veri varlığından yüklenen ekli görüntüleri değiştiremiyorum.</span><span class="sxs-lookup"><span data-stu-id="b811a-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-160">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-160">Issue description</span></span>

<span data-ttu-id="b811a-161">Bu sorun, *Ürün belge ekleri* veri varlığını kullanarak bir öğeye görüntü eklediğinizde oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="b811a-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="b811a-162">Bu durumda, madde için madde görüntüsü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b811a-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="b811a-163">Ancak, **Görüntüyü değiştir**'i seçerseniz, yüklenen görüntüler listesinde hiçbir şey gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="b811a-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="b811a-164">Ayrıca, madde için hiçbir ek gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="b811a-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-165">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-165">Issue resolution</span></span>

<span data-ttu-id="b811a-166">*EcoResProductDocumentAttachmentEntity* varlığı (*Ürün belge ekleri*) *ürünler* için belge eklerini içeri aktarır ancak *serbest bırakılan ürünler* için aktarmaz.</span><span class="sxs-lookup"><span data-stu-id="b811a-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="b811a-167">(Serbest bırakılan ürünler *maddeler* olarak da bilinir.) **Serbest bırakılan ürün ayrıntıları** sayfasında bir maddenin eklerini görüntülemek için bunun yerine *EcoResReleasedProductDocumentAttachmentEntity* varlığını *(Serbest bırakılmış ürün belgesi ekleri)* kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b811a-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="b811a-168">Microsoft Flow bağlayıcısı aşağıdaki hata iletisini gösteriyor: "'ProductNumber' alanı için güncelleştirmeye izin verilmiyor."</span><span class="sxs-lookup"><span data-stu-id="b811a-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-169">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-169">Issue description</span></span>

<span data-ttu-id="b811a-170">Bu sorun, *Serbest bırakılan ürünler* varlığı V2 ve Microsoft Flow kullanılarak **Ürün numarası**'nı güncelleştirmeye çalıştığınızda oluşur.</span><span class="sxs-lookup"><span data-stu-id="b811a-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-171">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-171">Issue resolution</span></span>

<span data-ttu-id="b811a-172">Bu davranış beklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="b811a-172">This behavior is expected.</span></span> <span data-ttu-id="b811a-173">Serbest bırakılan bir ürünün ürün numarasını güncelleştirme özelliği, veri bozulmasını önlemeye yardımcı olmak için platform güncelleştirmesi 24'te Dynamics 365 Finance and Operations 10.0.0'dan kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="b811a-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="b811a-174">Serbest bırakılmış bir ürünün birincil anahtarının önceki bir yeniden adlandırmanın neden olduğu veri bozulmasını onarmanız gereken özel durumlarda, Microsoft Destek'ten bu kısıtlamayı geçici olarak kaldırmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b811a-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="b811a-175">Başka bir tüzel kişiliğe serbest bırakılmış bir ürün varyantı oluşturamıyorum.</span><span class="sxs-lookup"><span data-stu-id="b811a-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-176">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-176">Issue description</span></span>

<span data-ttu-id="b811a-177">Varyantları olmayan bir ana ürünü serbest bırakmaya çalışır ve her tüzel kişide (şirket) varyantları gerektiği gibi oluşturursanız varyant önerilerini kullanarak varyantları serbest bırakamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b811a-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="b811a-178">Ayrıca varyantları el ile de oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b811a-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-179">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-179">Issue resolution</span></span>

<span data-ttu-id="b811a-180">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="b811a-180">This behavior is by design.</span></span> <span data-ttu-id="b811a-181">Bir ana ürünün ilişkileri ve ana ürünün alabileceği boyutlar, ortak bir düzeyde tutulur.</span><span class="sxs-lookup"><span data-stu-id="b811a-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="b811a-182">Bu nedenle, bu boyutların serbest bırakıldığı belirli bir tüzel kişilikte paylaşılan bir ana ürün için kullanılabilir boyutlar oluşturamaz ve boyutların gerekli olduğu her tüzel kişilikte işlemi kopyalayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b811a-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="b811a-183">Bunun yerine, tasarlanan işleme uyum sağlamak için serbest bırakma işleminizi değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b811a-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="b811a-184">Ürünleri serbest bırakma işlemi burada verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b811a-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="b811a-185">Paylaşılan ana ürünü ve tüzel kişilere serbest bırakılabilecek boyutları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b811a-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="b811a-186">Ürünleri varyant önerilerini kullanarak veya serbest bırakılması gereken kombinasyonları el ile ekleyerek tüzel kişiliklere serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="b811a-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="b811a-187">Alternatif olarak, serbest bırakılan ürünü doğrudan oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b811a-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="b811a-188">Başka bir şirkete bir varyant serbest bıraktığımda, aşağıdaki hata iletisini alıyorum: "Belirtilen boyutlardaki ürün çeşidi zaten oluşturuldu."</span><span class="sxs-lookup"><span data-stu-id="b811a-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b811a-189">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b811a-189">Issue description</span></span>

<span data-ttu-id="b811a-190">Bir ürün varyantı A şirketine zaten serbest bırakılmışsa ve **Serbest bırakılan ürün varyantları** sayfasındaki **Yeni** düğmesini kullanarak B şirketine serbest bırakmaya çalışırsanız aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="b811a-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="b811a-191">Belirtilen boyutlardaki ürün çeşidi zaten oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="b811a-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b811a-192">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b811a-192">Issue resolution</span></span>

<span data-ttu-id="b811a-193">**Serbest bırakılan ürün varyantları** sayfasındaki **Yeni** düğmesi varyantı oluşturur ve şirket bağlamında serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="b811a-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="b811a-194">Varyant zaten oluşturulduysa **Yeni** düğmesini, başka bir şirkete serbest bırakma için kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b811a-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="b811a-195">Sorunu gidermek için **Ana ürün** sayfasını açın ve istenen şirketteki var olan varyantı serbest bırakmak için **Ürünü serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b811a-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>
