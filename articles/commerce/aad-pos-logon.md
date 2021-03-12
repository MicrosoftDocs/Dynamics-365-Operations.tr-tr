---
title: POS oturum açma için Azure Active Directory kimlik doğrulamasını etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce satış noktası (POS) için oturum açma deneyiminin Azure Active Directory kimlik doğrulaması kullanacak şekilde nasıl ayarlanacağını açıklar.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982752"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="4e9f1-103">POS oturum açma için Azure Active Directory kimlik doğrulamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4e9f1-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="4e9f1-104">Microsoft Dynamics 365 Commerce kullanan çoğu müşteri diğer Microsoft bulut hizmetlerini de kullanır ve bu hizmetler için kullanıcı kimlik bilgilerini yönetmek üzere Azure Active Directory (Azure AD) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="4e9f1-105">Bu gibi durumlarda, müşteriler uygulamalarda aynı Azure AD hesabını kullanmak isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="4e9f1-106">Bu konu, Microsoft Commerce satış noktası (POS) oturum açma deneyiminin Azure AD kimlik doğrulaması kullanmak üzere nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="4e9f1-107">Azure AD kimlik doğrulamasını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4e9f1-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="4e9f1-108">Mağaza için POS oturum açma için Azure AD'yi kimlik doğrulama yöntemi olarak kullanılabilir hale getirmek amacıyla, mağazanın işlevsel profilinin ayarlarını yapılandırmanız ve sonra bu ayarı POS istemcisine uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="4e9f1-109">İşlev profili yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="4e9f1-110">**Perakende ve ticaret** \> **Kanal kurulumu** \> **POS kurulumu** \> **POS profilleri** \> **İşlevsellik profilleri** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="4e9f1-111">Değiştirilecek işlev profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="4e9f1-112">**İşlevler** hızlı sekmesinde **POS personeli oturum açma** bölümünde, **Oturum Açma Kimlik Doğrulama Yöntemi** alanının değerini **Personel Kimliği ve Parola** yerine **Azure Active Directory** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="4e9f1-113">Varsayılan olarak, tüm işlev profilleri POS kimlik doğrulama yöntemi olarak **Personel Kimliği ve Parola** kullanır.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="4e9f1-114">Bu nedenle, Azure AD kullanmak istiyorsanız **Oturum Açma Kimlik Doğrulama Yöntemi** alanının değerini değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="4e9f1-115">Seçilen işlev profiline bağlı her perakende mağazası bu değişiklikten etkilenir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="4e9f1-116">Ayarları POS istemcilerine uygulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="4e9f1-117">**Retail ve Commerce** \> **Retail ve Commerce BT** \> **Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="4e9f1-118">**1070** (**Kanal yapılandırması**) dağıtım planını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="4e9f1-119">Azure AD kimlik doğrulaması internet bağlantısı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="4e9f1-120">POS çevrimdışı moddayken çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="4e9f1-121">Şu anda, **yönetici geçersiz kılma** işlevi Azure AD kimlik doğrulama yöntemi olarak desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="4e9f1-122">Azure AD, POS ile oturum açma için kimlik doğrulama yöntemi olarak yapılandırılmış olsa bile, bir operatör kodu ve parola gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="4e9f1-123">Azure AD hesabını bir çalışanla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="4e9f1-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="4e9f1-124">Bir mağaza çalışanının POS uygulamasında oturum açmak Azure AD hesabını kullanabilmesi için, Azure AD hesabının o çalışanla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="4e9f1-125">Azure AD hesabını bir çalışanla ilişkilendirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="4e9f1-126">**Retail ve Commerce** \> **Personel** \> **Çalışanlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="4e9f1-127">Çalışanın ayrıntılar sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="4e9f1-128">Eylem Bölmesinde, **Commerce** sekmesindeki **Harici kimlik** gurubunda **Mevcut kimliği ilişkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="4e9f1-129">**Mevcut harici kimliği kullan** iletişim kutusunda, **E-posta kullanarak ara**'yı seçin, bir Azure AD e-posta adresi girin ve sonra **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="4e9f1-130">Döndürülen Azure AD hesabını seçin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="4e9f1-131">Çalışanın ayrıntılar sayfasındaki **Commerce** sekmesinde bulunan **Diğer ad**, **UPN** ve **Harici alt kimlik tanımlayıcı** alanları doldurulacaktır.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="4e9f1-132">Bir çalışan kaydı güncelleştirildikten sonra, örneğin yeni bir Azure AD hesabı ilişkilendirilmişse, parola değiştirilirse veya bir çalışan adres defteri güncelleştirilirse, en son personel bilgilerini kanalla eşitlemek için **1060** (**Personel**) dağıtım zamanlamasını çalıştırmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="4e9f1-133">Bu şekilde, POS uygulaması kullanıcı kimlik doğrulaması ve yetkilendirme denetimi için doğru verileri alabilir.</span><span class="sxs-lookup"><span data-stu-id="4e9f1-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e9f1-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4e9f1-134">Additional resources</span></span>

[<span data-ttu-id="4e9f1-135">MPOS ve Bulut POS için genişletilmiş oturum açma işlevini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4e9f1-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="4e9f1-136">Perakende işlevselliği profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="4e9f1-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="4e9f1-137"> Çalışanı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4e9f1-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
