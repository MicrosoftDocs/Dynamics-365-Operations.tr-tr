---
title: Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme
description: Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001289"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="90304-103">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="90304-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="90304-104">Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="90304-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="90304-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="90304-105">Overview</span></span>

<span data-ttu-id="90304-106">Müşterilerinizin sitem ile nasıl etkileştiğini anlamak ve maksimum dönüştürme deneyimini en iyi duruma getirmeye yardımcı olacak kararlar vermek istediğinizde, Web analizi önemli bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="90304-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="90304-107">Birçok web analizi paketi, Google Analytics, Click, Moz Analytics ve KISSMetrics gibi bu hedeflere ulaşmanıza yardımcı olacak şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="90304-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="90304-108">Çoğu Web analizi paketi, sitenizin tüm sayfaları için HTML'nin **\<baş\>** öğesine istemci tarafı kodu eklemenizi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="90304-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="90304-109">Bu konudaki yönergeler, Microsoft Dynamics 365 Commerce'un doğal olarak sunmadığı diğer özel istemci tarafı işlevleri için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="90304-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="90304-110">Komut dosyası kodunuz için yeniden kullanılabilir bir parça oluşturun</span><span class="sxs-lookup"><span data-stu-id="90304-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="90304-111">Kodunuz için bir parça oluşturduktan sonra, sitenizdeki tüm sayfalar arasında yeniden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="90304-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="90304-112">**Parçalar \> Yeni sayfa parçası**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="90304-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="90304-113">**Harici kod** seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="90304-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="90304-114">Parça hiyerarşisinde, az önce oluşturduğunuz parçanın **Komut dosyası enjektörleri** alt modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="90304-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="90304-115">Sağdaki Özellik bölmesinde, istemci tarafı komut dosyanızı ekleyin ve istediğiniz şekilde diğer yapılandırma seçeneklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="90304-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="90304-116">Parçayı şablonlara Ekle</span><span class="sxs-lookup"><span data-stu-id="90304-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="90304-117">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="90304-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="90304-118">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="90304-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="90304-119">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **parça Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="90304-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="90304-120">Kodunuz için oluşturduğunuz parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="90304-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="90304-121">Şablonu kaydedin ve giriş yapın.</span><span class="sxs-lookup"><span data-stu-id="90304-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="90304-122">İşlemi bitirdikten sonra, parçayı ve ana şablonu yayımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="90304-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="90304-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="90304-123">Additional resources</span></span>

[<span data-ttu-id="90304-124">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="90304-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="90304-125">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="90304-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="90304-126">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="90304-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="90304-127">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="90304-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="90304-128">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="90304-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="90304-129">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="90304-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="90304-130">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="90304-130">Add languages to your site</span></span>](add-languages-to-site.md)

