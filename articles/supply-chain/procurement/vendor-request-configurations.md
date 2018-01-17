---
title: "Satıcı talep konfigürasyonları"
description: "Bu konu, yeni bir satıcı talebinde doldurulması gerekli olan alanları açıklar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 57297a5798004f959a53513b88750866083beee7
ms.contentlocale: tr-tr
ms.lasthandoff: 01/17/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="dba38-103">Satıcı talep konfigürasyonları</span><span class="sxs-lookup"><span data-stu-id="dba38-103">Vendor request configurations</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="dba38-104">Bir satıcı talebini tamamlamak için satıcı ilgili kişisinin aday satıcı kayıt sihirbazını tamamlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dba38-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="dba38-105">**Satıcı talebi yapılandırmaları** formunda, aday satıcı kayıt sihirbazında gerekli alanları ve görülebilir alanları belirten profiller oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dba38-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="dba38-106">Satıcı kayıt sihirbazı, aday satısı kullanıcısına satıcının hangi ülkede/bölgede iş yaptığını sorarak başlar.</span><span class="sxs-lookup"><span data-stu-id="dba38-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="dba38-107">Bu bilgi uygulanacak yapılandırmayı belirler.</span><span class="sxs-lookup"><span data-stu-id="dba38-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="dba38-108">Ülke/bölge için özel bir yapılandırma tanımlanmamışsa, varsayılan yapılandırma kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dba38-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="dba38-109">Satıcı talebi yapılandırması ayarlama</span><span class="sxs-lookup"><span data-stu-id="dba38-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="dba38-110">Varsayılan olarak, Satıcı talebi yapılandırmaları formunda bir satıcı yapılandırması bulunur.</span><span class="sxs-lookup"><span data-stu-id="dba38-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="dba38-111">Varsayılan yapılandırma için ülke/bölge seçilemez, bu nedenle **Ülke/bölge** bölümü değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="dba38-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1.  <span data-ttu-id="dba38-112">**Tedarik ve kaynak atama** > **Kurulum** > **Satıcılar**'a ve ardından **Satıcı talebi yapılandırmaları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dba38-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="dba38-113">Listelenen alanların durumunu ayarlamak için **Alanlar** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dba38-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
-   <span data-ttu-id="dba38-114">Gizli (Görünmez)</span><span class="sxs-lookup"><span data-stu-id="dba38-114">Hidden (Not visible)</span></span>
-   <span data-ttu-id="dba38-115">Görüntülenen (Görünür, ancak zorunlu değildir)</span><span class="sxs-lookup"><span data-stu-id="dba38-115">Displayed (Visible but not mandatory)</span></span>
-   <span data-ttu-id="dba38-116">Gerekli (Görünür ve zorunlu)</span><span class="sxs-lookup"><span data-stu-id="dba38-116">Required (Visible and mandatory)</span></span>
3.  <span data-ttu-id="dba38-117">Metnin sihirbazda görünüp görünmeyeceğini ve aday satıcı kullanıcısının sihirbazda sonraki adıma geçmek için kabul etmesi gereken bir onay olup olmayacağını belirlemek için **İçerik** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dba38-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="dba38-118">Onay, kullanıcının devam etmek için kabul etmesi gereken tüm hüküm ve koşullar için istenecektir.</span><span class="sxs-lookup"><span data-stu-id="dba38-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="dba38-119">Ayrıca, sihirbaz tamamlandığı zaman gösterilecek bir onay iletisi girebilir ve bir veya daha fazla soru formu ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dba38-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="dba38-120">Belirli bir ülke/bölge için satıcı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="dba38-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="dba38-121">**Tedarik ve kaynak atama** > **Kurulum** > **Satıcılar**'a ve ardından **Satıcı talebi yapılandırmaları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dba38-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="dba38-122">Yeni bir yapılandırma oluşturmak için **Yeni**'ye tıklayın ve yapılandırma için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="dba38-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="dba38-123">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dba38-123">Click **Save**.</span></span>
4.  <span data-ttu-id="dba38-124">Yapılandırmanın kullanılacağı ülkeyi/bölgeyi seçmek için **Ülke/bölgeler** sekmesini açın.</span><span class="sxs-lookup"><span data-stu-id="dba38-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="dba38-125">Varsayılan yapılandırma talimatlarını izleyerek yapılandırmayı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="dba38-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


