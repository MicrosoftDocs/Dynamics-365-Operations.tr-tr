---
title: POS oturum açma için Azure Active Directory kimlik doğrulamasını etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce satış noktası (POS) için oturum açma deneyiminin Azure Active Directory kimlik doğrulaması kullanacak şekilde nasıl ayarlanacağını açıklar.
author: boycezhu
manager: annbe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 4f5a02348e8cef44424ae5d6a49de02d762ba245
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410047"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="7a3ed-103">POS oturum açma için Azure Active Directory kimlik doğrulamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7a3ed-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="7a3ed-104">Microsoft Dynamics 365 Commerce kullanan çoğu müşteri diğer Microsoft bulut hizmetlerini de kullanır ve bu hizmetler için kullanıcı kimlik bilgilerini yönetmek üzere Azure Active Directory (Azure AD) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="7a3ed-105">Bu gibi durumlarda, müşteriler uygulamalarda aynı Azure AD hesabını kullanmak isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="7a3ed-106">Bu konu, Microsoft Commerce satış noktası (POS) oturum açma deneyiminin Azure AD kimlik doğrulaması kullanmak üzere nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="7a3ed-107">Azure AD kimlik doğrulamasını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7a3ed-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="7a3ed-108">Mağaza için POS oturum açma için Azure AD'yi kimlik doğrulama yöntemi olarak kullanılabilir hale getirmek amacıyla, mağazanın işlevsel profilinin ayarlarını yapılandırmanız ve sonra bu ayarı POS istemcisine uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="7a3ed-109">İşlev profili yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="7a3ed-110">**Perakende ve ticaret** \> **Kanal kurulumu** \> **POS kurulumu** \> **POS profilleri** \> **İşlevsellik profilleri** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="7a3ed-111">Değiştirilecek işlev profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="7a3ed-112">**İşlevler** hızlı sekmesinde **POS personeli oturum açma** bölümünde, **Oturum Açma Kimlik Doğrulama Yöntemi** alanının değerini **Personel Kimliği ve Parola** yerine **Azure Active Directory** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="7a3ed-113">Varsayılan olarak, tüm işlev profilleri POS kimlik doğrulama yöntemi olarak **Personel Kimliği ve Parola** kullanır.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="7a3ed-114">Bu nedenle, Azure AD kullanmak istiyorsanız **Oturum Açma Kimlik Doğrulama Yöntemi** alanının değerini değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="7a3ed-115">Seçilen işlev profiline bağlı her perakende mağazası bu değişiklikten etkilenir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="7a3ed-116">Ayarları POS istemcilerine uygulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="7a3ed-117">**Retail ve Commerce** \> **Retail ve Commerce BT** \> **Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="7a3ed-118">**1070** (**Kanal yapılandırması**) dağıtım planını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="7a3ed-119">Azure AD kimlik doğrulaması internet bağlantısı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="7a3ed-120">POS çevrimdışı moddayken çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="7a3ed-121">Şu anda, **yönetici geçersiz kılma** işlevi Azure AD kimlik doğrulama yöntemi olarak desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="7a3ed-122">Azure AD, POS ile oturum açma için kimlik doğrulama yöntemi olarak yapılandırılmış olsa bile, bir operatör kodu ve parola gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="7a3ed-123">Azure AD hesabını bir çalışanla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="7a3ed-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="7a3ed-124">Bir mağaza çalışanının POS uygulamasında oturum açmak Azure AD hesabını kullanabilmesi için, Azure AD hesabının o çalışanla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="7a3ed-125">Azure AD hesabını bir çalışanla ilişkilendirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="7a3ed-126">**Retail ve Commerce** \> **Personel** \> **Çalışanlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="7a3ed-127">Çalışanın ayrıntılar sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="7a3ed-128">Eylem Bölmesinde, **Commerce** sekmesindeki **Harici kimlik** gurubunda **Mevcut kimliği ilişkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="7a3ed-129">**Mevcut harici kimliği kullan** iletişim kutusunda, **E-posta kullanarak ara**'yı seçin, bir Azure AD e-posta adresi girin ve sonra **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="7a3ed-130">Döndürülen Azure AD hesabını seçin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="7a3ed-131">Çalışanın ayrıntılar sayfasındaki **Commerce** sekmesinde bulunan **Diğer ad**, **UPN** ve **Harici alt kimlik tanımlayıcı** alanları doldurulacaktır.</span><span class="sxs-lookup"><span data-stu-id="7a3ed-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a3ed-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7a3ed-132">Additional resources</span></span>

[<span data-ttu-id="7a3ed-133">MPOS ve Bulut POS için genişletilmiş oturum açma işlevini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a3ed-133">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="7a3ed-134">Perakende işlevselliği profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a3ed-134">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="7a3ed-135"> Çalışanı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7a3ed-135">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
