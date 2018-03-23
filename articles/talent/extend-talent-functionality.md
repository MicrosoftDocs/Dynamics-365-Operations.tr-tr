---
title: "Microsoft Dynamics 365 for Talent işlevselliğini genişletme"
description: "Herhangi bir Microsoft PowerApps oluşturduysanız, bu uygulamaları Microsoft Dynamics 365 for Talent içindeki bağlantılardan başlatabilirsiniz."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="1a252-103">Microsoft Dynamics 365 for Talent işlevselliğini genişletme</span><span class="sxs-lookup"><span data-stu-id="1a252-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="1a252-104">Herhangi bir Microsoft PowerApps oluşturduysanız, bu uygulamaları Microsoft Dynamics 365 for Talent içindeki bağlantılardan başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a252-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="1a252-105">Uygulamalarınıza erişim ayarlamak için, Talent içinde bazı bilgileri **Sistem yönetimi** çalışma alanından açabileceğiniz bir yapılandırma sayfasında ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a252-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="1a252-106">Talent içinde katıştırılmış PowerApps yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1a252-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="1a252-107">PowerApps uygulamalarını başlatmak üzere Talent sayfalarını yapılandırmak için **Katıştırılmış Microsoft PowerApps ayarlama** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a252-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="1a252-108">**Katıştırılmış Microsoft PowerApps ayarlama** sayfasını açmak için, **Sistem yönetimi** çalışma alanını ve ardından **Bağlantılar** sekmesini açın. **Kurulum** grubundan **Microsoft PowerApps**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1a252-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="1a252-109">Aşağıdaki bilgileri bu sayfadan girilir veya ayarlanır:</span><span class="sxs-lookup"><span data-stu-id="1a252-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="1a252-110">Her PowerApps uygulaması için açıklayıcı bir ad veya bir tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="1a252-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="1a252-111">Talent sayfasına eklediğiniz her uygulama için benzersiz bir tanımlayıcı (GUID).</span><span class="sxs-lookup"><span data-stu-id="1a252-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="1a252-112">Uygulama kodu PowerApps sitesinde bulunur, [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="1a252-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="1a252-113">Kullanıcıların bir uygulama veya rapor açabilecekleri sayfa.</span><span class="sxs-lookup"><span data-stu-id="1a252-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="1a252-114">Tüm Talent sayfaları katıştırılmış PowerApps'i ve Power BI raporlarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="1a252-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="1a252-115">Sayfanın üstünde görüntülenen görünen ad yerine sayfanın dahili adını girin.</span><span class="sxs-lookup"><span data-stu-id="1a252-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="1a252-116">Dahili adı bulmak için, adını öğrenmek istediğiniz sayfası açın ve sayfada herhangi bir yere sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1a252-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="1a252-117">Menü açıldığında, **Form bilgileri** öğesinin üzerine gidin.</span><span class="sxs-lookup"><span data-stu-id="1a252-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="1a252-118">Dahili form adı menüdeki **Form bilgileri** öğesinin yanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1a252-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="1a252-119">Uygulamanın bağlam verilerini alabileceği form denetimini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1a252-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="1a252-120">Örneğin, bir uygulama bir çalışan hakkındaki verileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1a252-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="1a252-121">**Bağlam** alanındaki **Çalışan** sayfasına girerseniz, **Çalışan** sayfası uygulamayı başlattığınızda açılır.</span><span class="sxs-lookup"><span data-stu-id="1a252-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="1a252-122">**Bağlam alanındaki** bir giriş isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1a252-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="1a252-123">PowerApps uygulamasının çalıştırılacağı iletişim kutusunun boyutunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1a252-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="1a252-124">İletişim kutuları, uygulamanız bir telefonda veya geniş bir cihazda çalıştığında kullanıcı arabirimini en iyi duruma getirmek için sırasıyla "küçük" veya "büyük" olarak belirlenebilir.</span><span class="sxs-lookup"><span data-stu-id="1a252-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="1a252-125">Ayrıca bir uygulamanın hangi tüzel kişilikler tarafından kullanılabileceğini belirleyebilir veya uygulamanın tüm tüzel kişilikler tarafından kullanılabilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a252-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="1a252-126">Varsayılan olarak, PowerApps uygulamalarınız tüm tüzel kişiliklerin kullanımına sunulur.</span><span class="sxs-lookup"><span data-stu-id="1a252-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="1a252-127">Uygulama açma</span><span class="sxs-lookup"><span data-stu-id="1a252-127">Opening an application</span></span>
<span data-ttu-id="1a252-128">Katıştırılmış PowerApps uygulamaları yapılandırdığınızda, belirttiğiniz uygulama bağlantıları Talent içindeki sayfalara eklenir.</span><span class="sxs-lookup"><span data-stu-id="1a252-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="1a252-129">Bir uygulamayı açmak için bir bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1a252-129">Click a link to open an application.</span></span> 



