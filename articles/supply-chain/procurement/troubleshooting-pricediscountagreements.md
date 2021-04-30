---
title: Fiyatlar, indirimler, sözleşmeler ve para iadeleri ile ilgili sorunları giderme
description: Bu konu, fiyatlar, iskontolar, sözleşmeler ve iadeler ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2ccc1d52b83f9319af1c6336c1876c795c70028a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908531"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="ca6c9-103">Fiyatlar, indirimler, sözleşmeler ve para iadeleri ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="ca6c9-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="ca6c9-104">Bu konu, fiyatlar, iskontolar, sözleşmeler ve iadeler ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="ca6c9-105">Satınalma siparişi oluşturulduktan sonra bir satınalma siparişi satırına bir satınalma sözleşmesini bağlayamıyorum.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="ca6c9-106">Satınalma siparişi oluşturulduğunda bir satınalma siparişinin bir satınalma sözleşmesi ile ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="ca6c9-107">Aksi takdirde, satınalma siparişi satırları satınalma sözleşmesi satırlarıyla ilişkilendirilemez.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="ca6c9-108">"El ile veya harici belge ile girilen fiyatları ve indirimleri güncelleştir" iletisinin görünmesine neden olan denetimler nelerdir?</span><span class="sxs-lookup"><span data-stu-id="ca6c9-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="ca6c9-109">Sevkiyat tarihini değiştirdiğinizde, "El ile veya harici belge ile girilen fiyatları ve indirimleri güncelleştir" şeklinde bir ileti alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="ca6c9-110">Bu iletiyi alırsınız; çünkü sevkiyat tarihi değiştirilirse farklı bir ticaret veya satış sözleşmesi tetiklenebilir ve bir fiyat değişikliğine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="ca6c9-111">Sevkiyat tarihinde yapılan bir değişiklik ambar zamanlamalarını ve diğer ilgili bilgileri de etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="ca6c9-112">İleti, herhangi bir tarih veya başka parametre değiştiğinde tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="ca6c9-113">İletinin amacı, bu değişikliklerden dolayı oluşabilecek fiyat değişikliklerinin farkında olduğunuzdan emin olmak içindir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="ca6c9-114">Bu ileti ticari sözleşme değerlendirme (TAE) istemidir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="ca6c9-115">Tam açıklama için bkz. [Ticari sözleşme değerlendirme ilkeleri](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="ca6c9-115">For a full description, see [Trade agreement evaluation policies](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="ca6c9-116">Satınalma siparişi girişi tüm giderleri içermez.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="ca6c9-117">Sorunu yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca6c9-117">Reproduce the issue</span></span>

<span data-ttu-id="ca6c9-118">Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="ca6c9-119">**Satın alma ve kaynak hizmeti parametreleri** sayfasındaki **Teslimat** sekmesinde, **Ürün girişinde masraf oluştur** seçeneğinin *Evet* olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="ca6c9-120">Masrafları içeren bir satınalma siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="ca6c9-121">Satınalma siparişini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="ca6c9-122">Satınalma siparişini teslim alın.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="ca6c9-123">Makbuz toplamına bakın ve beklenen toplamla karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="ca6c9-124">Tüm giderlerin satınalma siparişi girişine dahil edilmediğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca6c9-125">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="ca6c9-125">Issue resolution</span></span>

<span data-ttu-id="ca6c9-126">Çözüm, sair giderlerin ayarlandığı yönteme bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="ca6c9-127">Gereksinimlerinizi karşılamak amacıyla sair giderlerin nasıl ayarlanacağı hakkında bilgi için aşağıdaki blog yazısına bakın: [Ürün makbuzu oluşturulurken sair giderleri deftere nakletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="ca6c9-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="ca6c9-128">Ticari sözleşme fiyatları ve iskontolar veri yönetimi aracılığıyla içe aktarılan satış veya satınalma siparişi satırlarına uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca6c9-129">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="ca6c9-129">Issue description</span></span>

<span data-ttu-id="ca6c9-130">Satış veya satınalma siparişi için uygulanan ticari sözleşmeler veri yönetimi aracılığıyla içe aktarılan satırlara uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="ca6c9-131">Ancak, aynı ticari sözleşmeler el ile oluşturulan satış veya satınalma siparişi satırlarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="ca6c9-132">Sorunun nedeni</span><span class="sxs-lookup"><span data-stu-id="ca6c9-132">Reason for the issue</span></span>

<span data-ttu-id="ca6c9-133">Veri yönetimi aracılığıyla içe aktarılan satınalma siparişi satırları zaten fiyat bilgilerini içeriyorsa, ticaret sözleşmesi bu satırlar için yeniden değerlendirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="ca6c9-134">Örneğin **Satır iskontosu yüzdesi** veya fiyat ve iskonto değerlerinin herhangi biri bir satırla ilgili olarak ayarlanmışsa, ticari sözleşmeler bu satır için aranmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="ca6c9-135">Sorun geçici çözümü</span><span class="sxs-lookup"><span data-stu-id="ca6c9-135">Issue workaround</span></span>

<span data-ttu-id="ca6c9-136">Bu beklenen bir davranıştır ve hem satış siparişleri hem de satınalma siparişleri için benzerdir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="ca6c9-137">Geçici çözüm olarak, herhangi bir fiyat bilgisi ayarlamadan satınalma siparişi satırlarını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="ca6c9-138">Ticari sözleşmeler daha sonra uygulanır ve satınalma siparişi satırları tanımlanan ticari sözleşmelere göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="ca6c9-139">Satıcı indirimi, faturalara dayalı olarak kümülatif değildir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca6c9-140">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="ca6c9-140">Issue description</span></span>

<span data-ttu-id="ca6c9-141">Deftere nakledilen faturaların farklı vade tarihleri varsa, bu faturalar bunlardan oluşturulan satıcı indirimlerine yansıtılmazlar.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca6c9-142">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="ca6c9-142">Issue resolution</span></span>

<span data-ttu-id="ca6c9-143">Tasarım sırasında, satıcı indirimi hesaplanırken vade tarihi dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="ca6c9-144">Sistemi, gerçek satıcı indirimi açısından faturadaki vade sonu ve ilgili ilişki daha belirgin olacak şekilde özelleştirmeyi düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="ca6c9-145">Satınalma siparişlerindeki birim fiyatlar birim dönüştürmesi temel alınarak hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca6c9-146">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="ca6c9-146">Issue description</span></span>

<span data-ttu-id="ca6c9-147">Bir satınalma siparişinde bir birim değiştirildiğinde, ticari sözleşme fiyatları birim dönüştürme tanımlarına göre yeniden hesaplanmazlar.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca6c9-148">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="ca6c9-148">Issue resolution</span></span>

<span data-ttu-id="ca6c9-149">Fiyatlar her zaman ticari sözleşmelerden (veya satış sözleşmeleri veya malzeme fiyatları gibi sistemdeki diğer fiyat ayarlarından) elde edilir ve bunlar bir birim için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="ca6c9-150">Sipariş satırındaki birim değiştirilirse, sistem yeni birim için bir fiyat arar ve bu fiyatı uygular.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="ca6c9-151">Birim için bir fiyat bulunamazsa, sistem bir fiyat uygulamaz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="ca6c9-152">Birim dönüştürme fiyatı başka bir birime yeniden hesaplamak için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="ca6c9-153">Teorik olarak, içerisinde on parça bulunan bir kutunun fiyatı bir tek kutunun fiyatının on katına eşit olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="ca6c9-154">Sorun geçici çözümü</span><span class="sxs-lookup"><span data-stu-id="ca6c9-154">Issue workaround</span></span>

<span data-ttu-id="ca6c9-155">Bu sorunu geçici olarak gidermek için kullanabileceğiniz bir yöntem de, malzemenin sipariş satırlarında kullanılmasını beklediğiniz birimler için ticari sözleşmeler olduğundan emin olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="ca6c9-156">Ticari sözleşmelerde para birimi dönüştürme sorunları oluşur.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="ca6c9-157">Ticari sözleşme fiyatları, para birimi bir satınalma siparişinde farklılık gösterdiğinde para birimine göre yeniden hesaplanmazlar.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="ca6c9-158">*Genel para birimi* özelliği, fiyatları ve iskontoları yalnızca bir para biriminde tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="ca6c9-159">Daha sonra gerektiğinde diğer para birimlerine dönüştürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="ca6c9-160">Ayrıca, dönüştürme yapıldıktan sonra özellik otomatik olarak akıllı yuvarlama uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="ca6c9-161">Bir satır görünümü modunda Satınalma sözleşmesi sayfasını açtığımda, satırın genel görünümüne Fiyat birimi alanı ekleyerek sayfayı kişiselleştiremiyorum.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="ca6c9-162">Sözleşme çerçevesindeki bazı paylaşılan alanlar kişiselleştirmeler içine eklenemez.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="ca6c9-163">Bu sınırlama, uygulanan veri modeli nedeniyle oluşur.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="ca6c9-164">Bu nedenle, **Fiyat birimi** alanını kişiselleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="ca6c9-165">Satınalma sözleşmesindeki maksimum sınır, satınalma talebinde etkili değildir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ca6c9-166">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="ca6c9-166">Issue description</span></span>

<span data-ttu-id="ca6c9-167">Bir satınalma talebi bir satınalma sözleşmesine bağlandığında, satınalma sözleşmesinden maksimum limit satınalma talebi üzerinde etkili olmaz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="ca6c9-168">Varsayılan fiyat bilgileri doğru girilmiştir, ancak satınalma sözleşmesinden maksimum sınırdan fazlası satınalma talebinde sipariş edilebilir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ca6c9-169">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="ca6c9-169">Issue resolution</span></span>

<span data-ttu-id="ca6c9-170">Bu davranış beklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-170">This behavior is expected.</span></span> <span data-ttu-id="ca6c9-171">Talepler her zaman onaylanmadığından, satınalma sözleşmesinde bir miktar veya tutar rezerve edilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="ca6c9-172">Bu nedenle, satınalma sözleşmesinden maksimum sınırı karşılamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="ca6c9-173">Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="ca6c9-174">Bu nedenle, RFQ satırı kabul edilmediyse, sistem ticari sözleşme günlüklerinin oluşturulmasını engellemez.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="ca6c9-175">Kabul edilip edilmediğine bakılmaksızın, bir teklif talebi (RFQ) için herhangi bir yanıt için ticari sözleşmeler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca6c9-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="ca6c9-176">Daha fazla bilgi için bkz. [Teklif talebine (RFQ) genel bakış](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="ca6c9-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]